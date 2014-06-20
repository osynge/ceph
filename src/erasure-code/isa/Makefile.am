# ISA
noinst_HEADERS += \
	erasure-code/isa/isa-l/include/erasure_code.h

isa_sources = \
	erasure-code/isa/isa-l/erasure_code/ec_base.c \
	erasure-code/isa/isa-l/erasure_code/ec_highlevel_func.c \
	erasure-code/isa/isa-l/erasure_code/ec_multibinary.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_2vect_dot_prod_avx2.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_2vect_dot_prod_avx.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_2vect_dot_prod_sse.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_3vect_dot_prod_avx2.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_3vect_dot_prod_avx.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_3vect_dot_prod_sse.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_4vect_dot_prod_avx2.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_4vect_dot_prod_avx.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_4vect_dot_prod_sse.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_5vect_dot_prod_avx2.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_5vect_dot_prod_avx.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_5vect_dot_prod_sse.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_6vect_dot_prod_avx2.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_6vect_dot_prod_avx.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_6vect_dot_prod_sse.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_vect_dot_prod_avx2.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_vect_dot_prod_avx.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_vect_dot_prod_sse.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_vect_mul_avx.asm.s \
	erasure-code/isa/isa-l/erasure_code/gf_vect_mul_sse.asm.s \
	erasure-code/isa/ErasureCodeIsa.cc \
	erasure-code/isa/ErasureCodePluginIsa.cc \
	erasure-code/isa/xor_op.cc

libec_isa_la_SOURCES = ${isa_sources}

libec_isa_la_CFLAGS = ${AM_CFLAGS} -I erasure-code/isa/isa-l/include/
libec_isa_la_CXXFLAGS = ${AM_CXXFLAGS} -I erasure-code/isa/isa-l/include/
libec_isa_la_CCASFLAGS = ${AM_CCASFLAGS} -i erasure-code/isa/isa-l/include/

libec_isa_la_LIBADD = $(LIBCRUSH) $(PTHREAD_LIBS) $(EXTRALIBS)
libec_isa_la_LDFLAGS = ${AM_LDFLAGS} -version-info 2:10:0
if LINUX
libec_isa_la_LDFLAGS += -export-symbols-regex '.*__erasure_code_.*'
endif
libec_isa_la_LIBTOOLFLAGS = --tag=CC

erasure_codelib_LTLIBRARIES += libec_isa.la

