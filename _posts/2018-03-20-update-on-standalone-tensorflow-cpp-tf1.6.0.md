---
layout: post
title: Updates on Standalone C++ Tensorflow version 1.6.0 with Opencv.
---

This post is an udate of the last [post](https://tuanphuc.github.io/standalone-tensorflow-cpp/) on how to make a standalone C++ project with tensorflow without using Bazel. This post aims at upgrading tensorflow to the latest stable version 1.6.0 and some tweaks that help tensorflow work nicely with **opencv**.

I was quite happy with the setup that I had from the last post. However, one thing that frustrates me is that I cannot use some of opencv's functions like imread or imshow when including tensorflow headers in my codes. The reasons are likely to be the conflict of symbols between tensorflow and opencv around the protobuf library. For more details you can look at issues [14267](https://github.com/tensorflow/tensorflow/issues/14267#issuecomment-351780041), [13278](https://github.com/tensorflow/tensorflow/issues/13278) and [1924](https://github.com/tensorflow/tensorflow/issues/1924). The solution for this problem will be showed in the next part. 

Update tensorflow to version 1.6.0:
```sh
git pull origin master
git fetch --tags
git checkout v1.6.0
```

Now you can built your libtensorflow_cc.so in adding the flag `--config=monolithic` which will condense everything together into one shared object (no libtensorflow_framework dependence) and seal off non-TensorFlow symbols. This prevents the symbol conflict with opencv. I add also some flags that will help your tensorflow run faster: `--copt=-mavx --copt=-mavx2 --copt=-mfma --copt=-mfpmath=both --copt=-msse4.1`.

```sh
bazel build -c opt --copt=-mavx --copt=-mavx2 --copt=-mfma --copt=-mfpmath=both --copt=-msse4.1 --copt=-msse4.2 --config=monolithic //tensorflow:libtensorflow_cc.so
```

You will get a libtensorflow_cc.so as the output of the command above. Use it in your project (you don'n need libtensorflow_framework.so anymore) peacefully with your opencv. One last thing you have to do is to replace your protobuf in the last [post](https://tuanphuc.github.io/standalone-tensorflow-cpp/) which is the version 3.4.0 with the protobuf version 3.5.0 in order to compile sucessfully your project.

If you have any question, feel free to contact me to: [phan at tuanphuc dot com](mailto:phan@tuanphuc.com).
