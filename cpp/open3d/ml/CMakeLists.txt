if (BUILD_TENSORFLOW_OPS AND WIN32)
    message( FATAL_ERROR "Building Tensorflow ops on Windows is currently not supported." )
    # see https://github.com/tensorflow/custom-op/issues/24
endif ()

if (BUILD_TENSORFLOW_OPS)
    add_subdirectory(TensorFlow)
endif ()

if (BUILD_PYTORCH_OPS)
    add_subdirectory(PyTorch)
endif ()

add_subdirectory(contrib)
