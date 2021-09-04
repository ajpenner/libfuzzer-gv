cmake_minimum_required (VERSION 3.4)

project (
    Fuzzer
    CXX
)

# make compile_database.json for VS code
set (CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(SOURCE
    FuzzerCrossOver.cpp
    FuzzerDriver.cpp
    FuzzerExtFunctionsDlsym.cpp
    FuzzerExtFunctionsDlsymWin.cpp
    FuzzerExtFunctionsWeakAlias.cpp
    FuzzerExtFunctionsWeak.cpp
    FuzzerExtraCounters.cpp
    FuzzerIO.cpp
    FuzzerIOPosix.cpp
    FuzzerIOWindows.cpp
    FuzzerLoop.cpp
    FuzzerMain.cpp
    FuzzerMerge.cpp
    FuzzerMutate.cpp
    FuzzerSHA1.cpp
    FuzzerShmemPosix.cpp
    FuzzerShmemWindows.cpp
    FuzzerTracePC.cpp
    FuzzerTraceState.cpp
    FuzzerUtil.cpp
    FuzzerUtilDarwin.cpp
    FuzzerUtilLinux.cpp
    FuzzerUtilPosix.cpp
    FuzzerUtilWindows.cpp
)

add_library (
    ${PROJECT_NAME}
  STATIC
  ${SOURCE}
)
