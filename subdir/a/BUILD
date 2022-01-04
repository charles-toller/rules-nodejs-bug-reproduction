load("@build_bazel_rules_nodejs//:index.bzl", "nodejs_binary")
load("@npm_a//@bazel/typescript:index.bzl", "ts_project")
ts_project(
    name = "typescript",
    srcs = [
        "src/index.ts"
    ],
    deps = [
        "@npm_a//@types/node",
    ]
)
nodejs_binary(
    name = "server",
    data = [
        ":typescript",
    ],
    entry_point = "src/index.js",
)
