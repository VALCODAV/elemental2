# This package contains the build rule to build elemental2-webstorage.

package(default_visibility = [
    "//third_party/java/elemental2:__subpackages__",
    "//:__subpackages__",
])

# Apache2
licenses(["notice"])

load("@com_google_jsinterop_generator//:jsinterop_generator.bzl", "jsinterop_generator")

filegroup(
    name = "externs",
    srcs = ["//third_party:webstorage.js"],
)

# SVG api
jsinterop_generator(
    name = "webstorage",
    srcs = [":externs"],
    extension_type_prefix = "WebStorage",
    deps = [
        "//java/elemental2/core",
        "//java/elemental2/dom",
    ],
)
