load("//tools:defs.bzl", "go_library", "proto_library")

package(licenses = ["notice"])

go_library(
    name = "strace",
    srcs = [
        "capability.go",
        "clone.go",
        "futex.go",
        "linux64_amd64.go",
        "linux64_arm64.go",
        "open.go",
        "poll.go",
        "ptrace.go",
        "select.go",
        "signal.go",
        "socket.go",
        "strace.go",
        "syscalls.go",
    ],
    visibility = ["//:sandbox"],
    deps = [
        ":strace_go_proto",
        "//pkg/abi",
        "//pkg/abi/linux",
        "//pkg/binary",
        "//pkg/bits",
        "//pkg/eventchannel",
        "//pkg/seccomp",
        "//pkg/sentry/arch",
        "//pkg/sentry/kernel",
        "//pkg/sentry/socket/control",
        "//pkg/sentry/socket/netlink",
        "//pkg/sentry/socket/netstack",
        "//pkg/sentry/syscalls/linux",
        "//pkg/usermem",
    ],
)

proto_library(
    name = "strace",
    srcs = ["strace.proto"],
    visibility = ["//visibility:public"],
)
