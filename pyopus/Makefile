# PLATFORM may be "MINGW32" or "UNIX"
export PLATFORM = MINGW32
#export PLATFORM = UNIX

# for system with "PIC" compiled static libraries
export CONFIGURE_OPTS = ""
#export CONFIGURE_OPTS = "--with-pic"
#-------------------------
ifeq ($(PLATFORM), MINGW32)
	MOD_EXT = pyd
endif
ifeq ($(PLATFORM), UNIX)
	MOD_EXT = so
endif

all : opus_mod

opus_mod: opus
	cp copus/copus.$(MOD_EXT) ./

opus :
	$(MAKE) -C copus

clean :
	$(MAKE) clean -C copus
		
