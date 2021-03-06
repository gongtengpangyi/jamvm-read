cmake_minimum_required(VERSION 3.9)
project(jamvm_2_0_0)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES
        src/arch/arm.h
        src/arch/i386.h
        src/arch/mips.h
        src/arch/parisc.h
        src/arch/powerpc.h
        src/arch/sparc.h
        src/arch/x86_64.h
        src/classlib/gnuclasspath/alloc.c
        src/classlib/gnuclasspath/annotations.c
        src/classlib/gnuclasspath/class.c
        src/classlib/gnuclasspath/classlib-defs.h
        src/classlib/gnuclasspath/classlib-excep.h
        src/classlib/gnuclasspath/classlib-symbol.h
        src/classlib/gnuclasspath/classlib.h
        src/classlib/gnuclasspath/dll.c
        src/classlib/gnuclasspath/excep.c
        src/classlib/gnuclasspath/frame.c
        src/classlib/gnuclasspath/gnuclasspath.h
        src/classlib/gnuclasspath/jni.c
        src/classlib/gnuclasspath/natives.c
        src/classlib/gnuclasspath/properties.c
        src/classlib/gnuclasspath/reflect.c
        src/classlib/gnuclasspath/thread.c
        src/classlib/openjdk/access.c
        src/classlib/openjdk/alloc.c
        src/classlib/openjdk/class.c
        src/classlib/openjdk/classlib-defs.h
        src/classlib/openjdk/classlib-excep.h
        src/classlib/openjdk/classlib-symbol.h
        src/classlib/openjdk/classlib.h
        src/classlib/openjdk/dll.c
        src/classlib/openjdk/excep.c
        src/classlib/openjdk/frame.c
        src/classlib/openjdk/jmm.h
        src/classlib/openjdk/jni.c
        src/classlib/openjdk/jvm.c
        src/classlib/openjdk/management.c
        src/classlib/openjdk/mh.c
        src/classlib/openjdk/natives.c
        src/classlib/openjdk/openjdk.h
        src/classlib/openjdk/perf.c
        src/classlib/openjdk/properties.c
        src/classlib/openjdk/reflect.c
        src/classlib/openjdk/shutdown.c
        src/classlib/openjdk/thread.c
        src/classlib/openjdk/trace.h
        src/interp/engine/compute_relocatability.c
        src/interp/engine/interp-direct-common.h
        src/interp/engine/interp-direct.h
        src/interp/engine/interp-indirect.h
        src/interp/engine/interp-inlining.h
        src/interp/engine/interp-threading.h
        src/interp/engine/interp.c
        src/interp/engine/interp.h
        src/interp/engine/interp2.c
        src/interp/engine/relocatability.c
        src/interp/direct.c
        src/interp/inlining.c
        src/interp/inlining.h
        src/interp/shared.h
        src/os/bsd/arm/dll_md.c
        src/os/bsd/arm/init.c
        src/os/bsd/i386/dll_md.c
        src/os/bsd/i386/init.c
        src/os/bsd/powerpc/dll_md.c
        src/os/bsd/powerpc/init.c
        src/os/bsd/sparc/init.c
        src/os/bsd/x86_64/dll_md.c
        src/os/bsd/x86_64/init.c
        src/os/bsd/os.c
        src/os/darwin/arm/dll_md.c
        src/os/darwin/arm/init.c
        src/os/darwin/i386/dll_md.c
        src/os/darwin/i386/init.c
        src/os/darwin/powerpc/dll_md.c
        src/os/darwin/powerpc/init.c
        src/os/darwin/os.c
        src/os/linux/arm/dll_md.c
        src/os/linux/arm/init.c
        src/os/linux/i386/dll_md.c
        src/os/linux/i386/init.c
        src/os/linux/i386/jni-stubs.c
        src/os/linux/i386/stubs_md.c
        src/os/linux/mips/dll_md.c
        src/os/linux/mips/init.c
        src/os/linux/parisc/init.c
        src/os/linux/powerpc/dll_md.c
        src/os/linux/powerpc/init.c
        src/os/linux/x86_64/dll_md.c
        src/os/linux/x86_64/init.c
        src/os/linux/os.c
        src/os/solaris/x86/dll_md.c
        src/os/solaris/x86/init.c
        src/os/solaris/os.c
        src/access.c
        src/alloc.c
        src/alloc.h
        src/annotations.h
        src/cast.c
        src/class.c
        src/class.h
        src/dll.c
        src/dll_ffi.c
        src/excep.c
        src/excep.h
        src/execute.c
        src/frame.c
        src/frame.h
        src/hash.c
        src/hash.h
        src/hooks.c
        src/init.c
        src/jam.c
        src/jam.h
        src/jni-internal.h
        src/jni-stubs.c
        src/jni.c
        src/jni.h
        src/lock.c
        src/lock.h
        src/natives.c
        src/natives.h
        src/properties.c
        src/properties.h
        src/reflect.c
        src/reflect.h
        src/resolve.c
        src/shutdown.c
        src/sig.c
        src/sig.h
        src/string.c
        src/stubs.c
        src/stubs.h
        src/symbol.c
        src/symbol.h
        src/thread.c
        src/thread.h
        src/time.c
        src/utf8.c
        src/zip.c
        src/zip.h)

include_directories("src")
include_directories("src/classlib/gnuclasspath")
include_directories("src/classlib/openjdk")

add_executable(jamvm_2_0_0 ${SOURCE_FILES})