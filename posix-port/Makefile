ROOT=..
include ../Make.config
LIB=../libmachdep.a

OFILES=\
	getcallerpc.$O\

default: $(LIB)
$(LIB): $(OFILES)
	$(AR) r $(LIB) $(OFILES)
	$(RANLIB) $(LIB)

%.$O: %.c
	$(CC) $(CFLAGS) $*.c

%.$O: %.s
	$(AS) -o $*.$O $*.s

%.s: %.spp
	cpp $*.spp >$*.s


