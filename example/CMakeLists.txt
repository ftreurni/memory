# Copyright (C) 2015-2016 Jonathan Müller <jonathanmueller.dev@gmail.com>
# This file is subject to the license terms in the LICENSE file
# found in the top-level directory of this distribution.

# builds examples

macro(_foonathan_add_example name)
    add_executable(foonathan_memory_example_${name} ${name}.cpp)
    target_link_libraries(foonathan_memory_example_${name} PRIVATE foonathan_memory)
    comp_target_features(foonathan_memory_example_${name} PUBLIC CPP11)
endmacro()

_foonathan_add_example(using_allocators)
_foonathan_add_example(taking_allocators)
_foonathan_add_example(allocator_storage)
_foonathan_add_example(tracking)
