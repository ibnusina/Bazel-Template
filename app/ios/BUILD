load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")

swift_library(
    name = "mylib",
    srcs = glob(['**/*.swift']),
    deps = ["//app/screen-lib:ScreenLib"]
)

ios_application(
    name = "ios-app",
    bundle_id = "ibnu.sina.com",
    families = [
        "iphone",
        "ipad",
    ],
    infoplists = ["info.plist"],
    minimum_os_version = "15.0",
    # provisioning_profile = "<your_profile_name>.mobileprovision", # Uncomment and set your own profile.
    visibility = ["//visibility:public"],
    deps = ["//app/ios:mylib"],
)