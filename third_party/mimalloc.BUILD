licenses(["notice"])  # MIT

exports_files(["LICENSE"])

cc_library(
    name = "mimalloc",
    srcs = ["src/static.c"],
    textual_hdrs = glob(
        ["src/*.c", "src/*.h", "src/prim/prim.c", "src/prim/**/*.c", "src/prim/**/*.h"],
        exclude = ["src/static.c"]
    ),
    hdrs = glob(["include/*.h", "include/mimalloc/*.h"]),
    includes = ["include"],
    copts = [
        "-DMI_SECURE",
        "-O2",
        "-Wall",
        "-Wextra",
        "--std=c++17",
    ],
    visibility = ["//visibility:public"],
)
