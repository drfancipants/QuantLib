
AM_CPPFLAGS = -I${top_builddir} -I${top_srcdir}

if AUTO_EXAMPLES
bin_PROGRAMS = MarketModels
TESTS = MarketModels$(EXEEXT)
else
noinst_PROGRAMS = MarketModels
endif
MarketModels_SOURCES = MarketModels.cpp
MarketModels_LDADD = ../../ql/libQuantLib.la ${BOOST_THREAD_LIB}

EXTRA_DIST = \
    CMakeLists.txt \
    MarketModels.vcxproj \
    MarketModels.vcxproj.filters

.PHONY: examples check-examples

examples: MarketModels$(EXEEXT)

check-examples: examples
	./MarketModels$(EXEEXT)

dist-hook:
	mkdir -p $(distdir)/bin
	mkdir -p $(distdir)/build

