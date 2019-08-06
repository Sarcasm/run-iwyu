cmake_minimum_required(VERSION 3.0.2)

project(RunIWYUTestProject)

add_library(run-iwyu-test-project
  src/bar.cpp
  src/foo.cpp
  src/foo_test.cpp
  include/foo/foo.h
)

target_include_directories(run-iwyu-test-project PRIVATE include)
