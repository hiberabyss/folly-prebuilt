cc_import(
  name = 'libfolly',
  hdrs = glob(['include/**']),
  static_library = 'libfolly.a',
)

cc_library(
  name = 'folly',
  linkopts = [
    # '-L/usr/local/lib',
    # '-lfolly',
    # '$(BINDIR)/external/fmt/libfmt/lib64/libfmt.a',
    '-ldl',
  ],
  includes = [
    '../double-conversion',
    'include',
  ],
  visibility = ["//visibility:public"],
  deps = [
    ':libfolly',
    '@fmt//:fmt',
    '@com_github_gflags_gflags//:gflags',
    '@com_github_google_glog//:glog',
    '@boost//:preprocessor',
    '@boost//:regex',
    '@double-conversion//:double-conversion',
  ],
)
