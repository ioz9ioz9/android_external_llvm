include_directories( ${CMAKE_CURRENT_BINARY_DIR}/.. ${CMAKE_CURRENT_SOURCE_DIR}/.. )

add_llvm_library(LLVMARMInfo
  ARMTargetInfo.cpp
  )

add_dependencies(LLVMARMInfo ARMCommonTableGen)

add_llvm_library_dependencies(LLVMARMInfo
  LLVMMC
  LLVMSupport
  LLVMTarget
  )
