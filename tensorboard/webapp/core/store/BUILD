package(default_visibility = ["//tensorboard:internal"])

load("@npm_angular_bazel//:index.bzl", "ng_module")
load("//tensorboard/defs:defs.bzl", "tf_ts_library")

ng_module(
    name = "store",
    srcs = [
        "core_initial_state_provider.ts",
        "core_reducers.ts",
        "core_selectors.ts",
        "core_types.ts",
        "index.ts",
    ],
    deps = [
        "//tensorboard/webapp/core/actions",
        "//tensorboard/webapp/deeplink",
        "//tensorboard/webapp/types",
        "@npm//@angular/core",
        "@npm//@ngrx/store",
        "@npm//rxjs",
    ],
)

tf_ts_library(
    name = "core_store_test_lib",
    testonly = True,
    srcs = [
        "core_initial_state_provider_test.ts",
        "core_reducers_test.ts",
    ],
    tsconfig = "//:tsconfig-test",
    deps = [
        ":store",
        "//tensorboard/webapp/core/actions",
        "//tensorboard/webapp/core/testing",
        "//tensorboard/webapp/deeplink",
        "//tensorboard/webapp/types",
        "@npm//@types/jasmine",
    ],
)
