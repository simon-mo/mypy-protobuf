load("@rules_proto//proto:defs.bzl", "proto_library")
load("//:plugin.bzl", "mypy_proto_compile")

proto_library(
    name = "test_proto",
    srcs = ["testproto/nopackage.proto"]
)

mypy_proto_compile(
    name = "test_mypy_proto",
    deps = [":test_proto"]
)