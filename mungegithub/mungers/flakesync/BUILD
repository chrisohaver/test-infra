package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["cache_test.go"],
    importpath = "k8s.io/test-infra/mungegithub/mungers/flakesync",
    library = ":go_default_library",
    deps = ["//vendor/github.com/google/gofuzz:go_default_library"],
)

go_library(
    name = "go_default_library",
    srcs = ["cache.go"],
    importpath = "k8s.io/test-infra/mungegithub/mungers/flakesync",
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
