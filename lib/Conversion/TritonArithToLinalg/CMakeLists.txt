add_triton_library(TritonArithToLinalg
  TritonArithToLinalg.cpp
  TritonArithToLinalgPass.cpp

  DEPENDS
  TritonArithToLinalgConversionPassIncGen

  LINK_LIBS PUBLIC
  MLIRLinalgTransforms
  MLIRArithDialect
  MLIRDialectUtils
  MLIRIR
  MLIRMathDialect
  MLIRMathExtDialect
  MLIRPass
  MLIRTensorDialect
  MLIRTransforms
  MLIRSupport
  TritonIR
  TritonTransforms
  TritonTilingExtIR
  TritonStructuredIR
  TritonSharedUtils
)
