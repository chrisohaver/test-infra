package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = [
        "hook_test.go",
        "server_test.go",
    ],
    importpath = "k8s.io/test-infra/prow/hook",
    library = ":go_default_library",
    deps = [
        "//prow/config:go_default_library",
        "//prow/github:go_default_library",
        "//prow/phony:go_default_library",
        "//prow/plugins:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "events.go",
        "metrics.go",
        "plugins.go",
        "server.go",
    ],
    importpath = "k8s.io/test-infra/prow/hook",
    deps = [
        "//prow/commentpruner:go_default_library",
        "//prow/config:go_default_library",
        "//prow/github:go_default_library",
        "//prow/plugins:go_default_library",
        "//prow/plugins/approve:go_default_library",
        "//prow/plugins/assign:go_default_library",
        "//prow/plugins/blockade:go_default_library",
        "//prow/plugins/cla:go_default_library",
        "//prow/plugins/close:go_default_library",
        "//prow/plugins/docs-no-retest:go_default_library",
        "//prow/plugins/golint:go_default_library",
        "//prow/plugins/heart:go_default_library",
        "//prow/plugins/hold:go_default_library",
        "//prow/plugins/label:go_default_library",
        "//prow/plugins/lgtm:go_default_library",
        "//prow/plugins/milestonestatus:go_default_library",
        "//prow/plugins/releasenote:go_default_library",
        "//prow/plugins/reopen:go_default_library",
        "//prow/plugins/shrug:go_default_library",
        "//prow/plugins/sigmention:go_default_library",
        "//prow/plugins/size:go_default_library",
        "//prow/plugins/slackevents:go_default_library",
        "//prow/plugins/trigger:go_default_library",
        "//prow/plugins/updateconfig:go_default_library",
        "//prow/plugins/wip:go_default_library",
        "//prow/plugins/yuks:go_default_library",
        "//vendor/github.com/prometheus/client_golang/prometheus:go_default_library",
        "//vendor/github.com/sirupsen/logrus:go_default_library",
    ],
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
