cmake_minimum_required (VERSION 2.8)
project (matio)

set(LIBRARY_OUTPUT_PATH ..)

include_directories (
./getopt
./src
)

set(SOURCES
./getopt/getopt_long.c
./src/endian.c
./src/inflate.c
./src/io.c
./src/mat.c
./src/mat4.c
./src/mat5.c
./src/mat73.c
./src/matvar_cell.c
./src/matvar_struct.c
./src/read_data.c
./src/snprintf.c
./test/test_mat.c
./test/test_snprintf.c
./tools/matdump.c
)


add_library(matio ${SOURCES})

