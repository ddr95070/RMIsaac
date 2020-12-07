"""
Copyright (c) 2019, NVIDIA CORPORATION. All rights reserved.

NVIDIA CORPORATION and its licensors retain all intellectual property
and proprietary rights in and to this software, related documentation
and any modifications thereto. Any use, reproduction, disclosure or
distribution of this software and related documentation without an express
license agreement from NVIDIA CORPORATION is strictly prohibited.
"""

exports_files(["LICENSE.TXT"])

cc_import(
    name = "libsl_zed",
    shared_library = "x64/lib/libsl_zed.so",
)

cc_import(
    name = "libsl_input",
    shared_library = "x64/lib/libsl_input.so",
)

cc_import(
    name = "libsl_core",
    shared_library = "x64/lib/libsl_core.so",
)

cc_library(
    name = "zed_x86_64",
    hdrs = glob(["include/**/*.hpp"]),
    includes = ["include"],
    visibility = ["//visibility:public"],
    deps = [
        # Intentionally put libsl_input before others to have proper dependencies
        # for modules as bazel mangle shared lib paths
        ":libsl_input",
        ":libsl_core",
        ":libsl_zed",
        "@com_nvidia_isaac//third_party:cuda",
        "@com_nvidia_isaac//third_party:npps",
        "@libjpeg//:jpeg",
        "@libusb",
        "@openmp//:openmp_dynamic",
    ],
)
