# Pybind11

jucer_project_files("BespokeSynth/libs/pybind11/detail"
# Compile   Xcode     Binary    File
#           Resource  Resource
  .         .         .         "detail/class.h"
  .         .         .         "detail/common.h"
  .         .         .         "detail/descr.h"
  .         .         .         "detail/init.h"
  .         .         .         "detail/internals.h"
  .         .         .         "detail/typeid.h"
)

jucer_project_files("BespokeSynth/libs/pybind11"
# Compile   Xcode     Binary    File
#           Resource  Resource
  .         .         .         "attr.h"
  .         .         .         "buffer_info.h"
  .         .         .         "cast.h"
  .         .         .         "chrono.h"
  .         .         .         "common.h"
  .         .         .         "complex.h"
  .         .         .         "eigen.h"
  .         .         .         "embed.h"
  .         .         .         "eval.h"
  .         .         .         "functional.h"
  .         .         .         "iostream.h"
  .         .         .         "numpy.h"
  .         .         .         "operators.h"
  .         .         .         "options.h"
  .         .         .         "pybind11.h"
  .         .         .         "pytypes.h"
  .         .         .         "stl.h"
  .         .         .         "stl_bind.h"
)

