set(LLVM_LINK_COMPONENTS
  ${LLVM_TARGETS_TO_BUILD}
  BitReader
  BitWriter
  Core
  ExecutionEngine
  MC
  MCJIT
  MCParser
  Object
  Option
  Support
)

add_llvm_tool(alley
  alley.cpp
)
target_link_libraries(alley
  liball
  AOTCompile
  Cache
  ExecutionYengine
  ResourcePaths
)

add_definitions(${LLVM_DEFINITIONS})
