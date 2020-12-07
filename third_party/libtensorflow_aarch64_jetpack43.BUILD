"""
Copyright (c) 2019, NVIDIA CORPORATION. All rights reserved.

NVIDIA CORPORATION and its licensors retain all intellectual property
and proprietary rights in and to this software, related documentation
and any modifications thereto. Any use, reproduction, disclosure or
distribution of this software and related documentation without an express
license agreement from NVIDIA CORPORATION is strictly prohibited.
"""

# Tensorflow binaries built on Jetson Xavier with CUDA and CuDNN support
cc_library(
    name = "libtensorflow_aarch64_jetpack43",
    srcs = [
        "lib/libtensorflow.so",
        "lib/libtensorflow.so.1",
        "lib/libtensorflow.so.1.15.0",
        "lib/libtensorflow_framework.so",
        "lib/libtensorflow_framework.so.1",
        "lib/libtensorflow_framework.so.1.15.0",
    ],
    hdrs = [
        "include/tensorflow/c/c_api.h",
        "include/tensorflow/c/c_api_experimental.h",
        "include/tensorflow/c/tf_attrtype.h",
        "include/tensorflow/c/tf_datatype.h",
        "include/tensorflow/c/tf_status.h",
        "include/tensorflow/c/tf_tensor.h",
    ],
    linkstatic = True,
    strip_include_prefix = "include",
    visibility = ["//visibility:public"],
)
