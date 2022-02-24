load("@io_bazel_rules_go//go:def.bzl", "go_library")
load("@bazel_gazelle//:def.bzl", "gazelle")

# gazelle:prefix github.com/k0kubun/sqldef
gazelle(name = "gazelle")

go_library(
    name = "sqldef",
    srcs = [
        "sqldef.go",
        "tools.go",
    ],
    importpath = "github.com/k0kubun/sqldef",
    visibility = ["//visibility:public"],
    deps = [
        "//adapter",
        "//schema",
        "@com_github_k0kubun_pp_v3//:pp",
    ],
)

alias(
    name = "psqldef",
    actual = "//cmd/psqldef:psqldef",
)
