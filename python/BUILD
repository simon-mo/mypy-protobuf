load("@rules_python//python:defs.bzl", "py_binary")
load("@rules_proto_grpc//:plugin.bzl", "proto_plugin")
load("@mypy_protobuf_dep//:requirements.bzl", "requirement")

py_binary(
    name = "mypy_protobuf",
    srcs = ["mypy_protobuf.py"],
    deps = [requirement("protobuf")],
)

proto_plugin(
    name = "mypy_protobuf_plugin",
    outputs = ["{protopath}_pb2.pyi"],
    tool = "mypy_protobuf",
    options = ["quiet"],
    visibility = ["//visibility:public"],
)
