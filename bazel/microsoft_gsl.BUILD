# Copyright 2022 Ant Group Co., Ltd.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

load("@psi//bazel:psi.bzl", "psi_cmake_external")

package(default_visibility = ["//visibility:public"])

filegroup(
    name = "all_srcs",
    srcs = glob(["**"]),
)

psi_cmake_external(
    name = "gsl",
    cache_entries = {
        "GSL_INSTALL": "ON",
        "GSL_STANDALONE_PROJECT": "OFF",
        "GSL_TEST": "OFF",
    },
    lib_source = ":all_srcs",
    out_headers_only = True,
    out_include_dir = "include",
)
