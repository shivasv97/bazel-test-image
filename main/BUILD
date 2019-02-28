load("@io_bazel_rules_docker//cc:image.bzl", "cc_image")
load("@io_bazel_rules_docker//container:container.bzl", "container_push", "container_image")

cc_image(
	name ="hello-worldio",
	srcs = ["hello.c"],
)

#cc_binary(
#	name = "hello",
#	srcs = ["hello.c"],
#)

#pkg_tar(
#	name = "hello_tar",
#	srcs = [":hello"],
#	mode = "0755",
#	package_dir = "/opt",
#	visibility = ["//visibility:public"],
#)

container_push(
  name = "hello_push",
  format = "Docker",
  image = "hello-worldio",
  registry = "index.docker.io",
  repository = "shivassv97/helloc",
  tag="latest",
)

