package(default_visibility = ["//visibility:public"])

load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "env.go",
        "logger.go",
        "manager.go",
        "registry.go",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "//mixer/pkg/adapter:go_default_library",
        "//mixer/pkg/aspect:go_default_library",
        "//mixer/pkg/attribute:go_default_library",
        "//mixer/pkg/config:go_default_library",
        "//mixer/pkg/config/descriptor:go_default_library",
        "//mixer/pkg/config/proto:go_default_library",
        "//mixer/pkg/expr:go_default_library",
        "//mixer/pkg/pool:go_default_library",
        "//mixer/pkg/status:go_default_library",
        "@com_github_gogo_protobuf//proto:go_default_library",
        "@com_github_golang_glog//:go_default_library",
        "@com_github_googleapis_googleapis//:google/rpc",
        "@com_github_opentracing_opentracing_go//:go_default_library",
        "@com_github_opentracing_opentracing_go//log:go_default_library",
        "@com_github_prometheus_client_golang//prometheus:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    size = "small",
    srcs = [
        "env_test.go",
        "manager_test.go",
        "registry_test.go",
    ],
    library = ":go_default_library",
    deps = [
        "//mixer/pkg/adapter:go_default_library",
        "//mixer/pkg/aspect:go_default_library",
        "//mixer/pkg/attribute:go_default_library",
        "//mixer/pkg/config:go_default_library",
        "//mixer/pkg/config/descriptor:go_default_library",
        "//mixer/pkg/config/proto:go_default_library",
        "//mixer/pkg/expr:go_default_library",
        "//mixer/pkg/pool:go_default_library",
        "//mixer/pkg/status:go_default_library",
        "@com_github_googleapis_googleapis//:google/rpc",
    ],
)
