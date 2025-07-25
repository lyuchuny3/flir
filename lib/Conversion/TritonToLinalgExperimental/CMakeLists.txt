#===------------------------------------------------------------------------===#
#
# Copyright (c) Triton Project Contributors.
#
#===------------------------------------------------------------------------===#

add_triton_library(TritonToLinalgExperimental
  TritonToLinalgExperimentalPass.cpp
  ReconcilePtrCastsPass.cpp
  TritonToPtrPass.cpp

  DEPENDS
  TritonToLinalgExperimentalConversionPassIncGen

  LINK_LIBS PUBLIC
  TritonTilingExtIR
  MLIRArithDialect
  MLIRDialectUtils
  MLIRIR
  MLIRMathDialect
  MLIRMathExtDialect
  MLIRPass
  MLIRTensorDialect
  MLIRTransforms
  MLIRSupport
  TPtrIR
  TritonIR
  TritonTransforms
  TritonSharedAnalysis
  TritonSharedUtils

  TritonArithToLinalg
  StructuredToMemref
  MemrefCopyToDMAFlagTree
  TritonToStructured
  TritonToUnstructured
  TritonPtrToMemref
  UnstructuredToMemref
)
