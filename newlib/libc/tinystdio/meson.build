#
# SPDX-License-Identifier: BSD-3-Clause
#
# Copyright © 2019 Keith Packard
#
# Redistribution and use in source and binary forms, with or without
# modification, are permitted provided that the following conditions
# are met:
#
# 1. Redistributions of source code must retain the above copyright
#    notice, this list of conditions and the following disclaimer.
#
# 2. Redistributions in binary form must reproduce the above
#    copyright notice, this list of conditions and the following
#    disclaimer in the documentation and/or other materials provided
#    with the distribution.
#
# 3. Neither the name of the copyright holder nor the names of its
#    contributors may be used to endorse or promote products derived
#    from this software without specific prior written permission.
#
# THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
# "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
# LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS
# FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE
# COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT,
# INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
# (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
# SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
# HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT,
# STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
# ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED
# OF THE POSSIBILITY OF SUCH DAMAGE.
#
subdir('sys')

srcs_tinystdio = [
    'clearerr.c',
    'dtoa_engine.c',
    'dtoa_data.c',
    'fclose.c',
    'fdevopen.c',
    'feof.c',
    'ferror.c',
    'fgetc.c',
    'fgets.c',
    'fiprintf.c',
    'fiscanf.c',
    'fprintf.c',
    'fputc.c',
    'fputs.c',
    'fread.c',
    'fscanf.c',
    'ftoa_engine.c',
    'fwrite.c',
    'getc.c',
    'getchar.c',
    'gets.c',
    'iprintf.c',
    'iscanf.c',
    'printf.c',
    'putc.c',
    'putchar.c',
    'puts.c',
    'scanf.c',
    'siprintf.c',
    'siscanf.c',
    'sniprintf.c',
    'snprintf.c',
    'sprintf.c',
    'sscanf.c',
    'strtof.c',
    'strtod.c',
    'ungetc.c',
    'vfiprintf.c',
    'vfiscanf.c',
    'vfprintf.c',
    'vfscanf.c',
    'viprintf.c',
    'viscanf.c',
    'vprintf.c',
    'vscanf.c',
    'vsiprintf.c',
    'vsniprintf.c',
    'vsnprintf.c',
    'vsprintf.c',
]

srcs_tinystdio_flt = [
    'vfprintf.c',
    'vfscanf.c',
]

hdrs_tinystdio = [
    'dtoa_engine.h',
    'ftoa_engine.h',
    'stdio.h',
    'stdio_private.h',
    'xtoa_fast.h',
]

install_headers(
  'stdio.h'
)

foreach target : targets
	value = get_variable('target_' + target)
	set_variable('lib_tinystdio' + target,
		     static_library('tinystdio' + target,
				    srcs_tinystdio,
				    pic: false,
				    include_directories: inc,
				    c_args: value[1]))
endforeach
