MODULE_TOPDIR = ..

SHELL_OUTPUT := $(shell python dependency.py 2>&1)
ifeq ($(filter File dependency.py,$(SHELL_OUTPUT)),)
    $(info $(SHELL_OUTPUT))
else
    $(error $(SHELL_OUTPUT))
endif

SUBDIRS = \
    mdlib \
    profiles \
    config \
    r.info.iso \
    v.info.iso \
    t.info.iso \
    db.csw.admin \
    db.csw.run \
    db.csw.harvest \
    g.gui.cswbrowser \
    g.gui.metadata

include $(MODULE_TOPDIR)/include/Make/Dir.make

default: parsubdirs

install: installsubdirs
