package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["storage_test.go"],
    embed = [":go_default_library"],
    deps = [
        "//pkg/apis/core:go_default_library",
        "//pkg/registry/core/service/allocator:go_default_library",
        "//pkg/registry/registrytest:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/storage/etcd3/testing:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/storage/storagebackend:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = ["storage.go"],
    importpath = "k8s.io/kubernetes/pkg/registry/core/service/allocator/storage",
    deps = [
        "//pkg/apis/core:go_default_library",
        "//pkg/registry/core/rangeallocation:go_default_library",
        "//pkg/registry/core/service/allocator:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/registry/generic:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/registry/generic/registry:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/storage:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/storage/errors:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/storage/storagebackend:go_default_library",
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
