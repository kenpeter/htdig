# Generated automatically from Makefile.in by configure.
# @(#)Makefile.in	10.62 (Sleepycat) 12/7/98

srcdir=	./..
CPPFLAGS=-I. -I$(srcdir)/include 
CFLAGS=	-c -O $(CPPFLAGS)
CC=	gcc
CXXFLAGS=-c -O $(CPPFLAGS)
CXX=	
LDFLAGS=
LIBS=	

SHELL=	/bin/sh
ar=	/usr/bin/ar cr
chmod=	/bin/chmod
cp=	/bin/cp
mkdir=	/bin/mkdir
ranlib= /usr/bin/ranlib
rm=	/bin/rm
strip=	/usr/bin/strip

OBJS=   bt_compare.o bt_conv.o bt_curadj.o bt_cursor.o bt_delete.o \
	bt_open.o bt_page.o bt_put.o bt_rec.o bt_recno.o bt_rsearch.o \
	bt_search.o bt_split.o bt_stat.o btree_auto.o db.o db_appinit.o \
	db_am.o db_apprec.o db_auto.o db_byteorder.o db_conv.o \
	db_dispatch.o db_dup.o db_err.o db_iface.o db_join.o db_log2.o \
	db_overflow.o db_pr.o db_rec.o db_region.o db_ret.o db_salloc.o \
	db_shash.o dbm.o hash.o hash_auto.o hash_conv.o hash_dup.o \
	hash_func.o hash_page.o hash_rec.o hash_stat.o hsearch.o lock.o \
	lock_conflict.o lock_deadlock.o lock_util.o lock_region.o log.o \
	log_archive.o log_auto.o log_compare.o log_findckp.o log_get.o \
	log_put.o log_rec.o log_register.o mp_bh.o mp_fget.o mp_fopen.o \
	mp_fput.o mp_fset.o mp_open.o mp_pr.o mp_region.o mp_sync.o \
	mutex.o os_abs.o os_alloc.o os_config.o os_dir.o os_fid.o \
	os_fsync.o os_map.o os_oflags.o os_open.o os_rpath.o os_rw.o \
	os_seek.o os_sleep.o os_spin.o os_stat.o os_tmpdir.o os_unlink.o \
	txn.o txn_auto.o txn_rec.o xa.o xa_db.o xa_map.o
COBJS=	cxx_app.o cxx_except.o cxx_lock.o cxx_log.o cxx_mpool.o cxx_table.o \
	cxx_txn.o

PROGS=	 db_archive db_checkpoint db_deadlock \
	db_dump db_load db_printlog db_recover db_stat

LOBJS=	
POBJS=	err.o getlong.o

libdb=	libdb.a
all: $(libdb) $(PROGS)

$(libdb): db.h $(OBJS) $(LOBJS)
	$(rm) -f $@
	$(ar) $@ $(OBJS) $(LOBJS)
	test ! -f $(ranlib) || $(ranlib) $@

DBA=	db_archive.o $(POBJS)
db_archive: $(DBA) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBA) $(libdb) $(LIBS)

DBB=	db_checkpoint.o $(POBJS)
db_checkpoint: $(DBB) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBB) $(libdb) $(LIBS)

DBC=	db_deadlock.o $(POBJS)
db_deadlock: $(DBC) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBC) $(libdb) $(LIBS)

DBD=	db_dump.o $(POBJS)
db_dump: $(DBD) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBD) $(libdb) $(LIBS)

DBE=	db_dump185.o $(POBJS)
db_dump185: $(DBE)
	$(CC) -o $@ $(LDFLAGS) $(DBE) $(LIBS)

DBF=	db_load.o $(POBJS)
db_load: $(DBF) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBF) $(libdb) $(LIBS)

DBG=	db_printlog.o $(POBJS)
db_printlog: $(DBG) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBG) $(libdb) $(LIBS)

DBH=	db_recover.o $(POBJS)
db_recover: $(DBH) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBH) $(libdb) $(LIBS)

DBI=	db_stat.o $(POBJS)
db_stat: $(DBI) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBI) $(libdb) $(LIBS)

EPROGS=	ex_access ex_appinit ex_btrec ex_lock ex_mpool ex_thread ex_tpcb
DBJ=	ex_access.o
ex_access: $(DBJ) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBJ) $(libdb) $(LIBS)

DBK=	ex_appinit.o
ex_appinit: $(DBK) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBK) $(libdb) $(LIBS)

DBL=	ex_btrec.o
ex_btrec: $(DBL) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBL) $(libdb) $(LIBS)

DBM=	ex_lock.o $(POBJS)
ex_lock: $(DBM) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBM) $(libdb) $(LIBS)

DBN=	ex_mpool.o
ex_mpool: $(DBN) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBN) $(libdb) $(LIBS)

DBO=	ex_thread.o
ex_thread: $(DBO) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBO) $(libdb) $(LIBS)

DBP=	ex_tpcb.o $(POBJS)
ex_tpcb: $(DBP) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBP) $(libdb) $(LIBS)

DBT=	tclAppInit.o tcl_dbm.o tcl_hsearch.o tcl_lock.o tcl_log.o tcl_mpool.o \
	tcl_mutex.o tcl_ndbm.o tcl_txn.o utils.o $(POBJS)

dbtest: .dbtestrc
dbtest: $(DBT) $(libdb)
	$(CC) -o $@ $(LDFLAGS) $(DBT) $(libdb) $(LIBS)

AOBJS=	err.o getcwd.o getlong.o getopt.o memcmp.o memcpy.o memmove.o \
	raise.o snprintf.o strerror.o strsep.o vsnprintf.o

clean:
	$(rm) -f $(OBJS) $(AOBJS)
	$(rm) -f $(DBA) $(DBB) $(DBC) $(DBD) $(DBE) $(DBF) $(DBG) $(DBH)
	$(rm) -f $(DBI) $(DBJ) $(DBK) $(DBL) $(DBM) $(DBN) $(DBO) $(DBP)
	$(rm) -f $(DBT)
	$(rm) -f $(PROGS) $(EPROGS) $(POBJS) $(LOBJS) @build_test@
	$(rm) -f core *.core .dbtestrc $(libdb)

depend obj:

realclean distclean: clean
	$(rm) -f Makefile config.cache config.h config.log config.status
	$(rm) -f confdefs.h db.h db_int.h db_185.h include.tcl

prefix=	/var/www/test/testme/sounddesign
bindir=	$(prefix)/BerkeleyDB/bin
datadir=$(prefix)/BerkeleyDB/share
includedir=$(prefix)/BerkeleyDB/include
libdir=	$(prefix)/BerkeleyDB/lib
mandir=	$(prefix)/BerkeleyDB/docs

dmode=	755
emode=	555
fmode=	444

transform=s,x,x,

install: all
	@test -f $(chmod) || (echo 'chmod not found.'; exit 1)
	@test -f $(cp) || (echo 'cp not found.'; exit 1)
	@test -f $(mkdir) || (echo 'mkdir not found.'; exit 1)
	@test -f $(rm) || (echo 'rm not found.'; exit 1)
	@echo "Installing DB include files: $(includedir) ..."
	@test -d $(includedir) || \
	    ($(mkdir) -p $(includedir) && $(chmod) $(dmode) $(includedir))
	@cd $(includedir) && $(rm) -f db.h db_185.h db_cxx.h
	@$(cp) -p db.h db_185.h $(srcdir)/include/db_cxx.h $(includedir)
	@cd $(includedir) && $(chmod) $(fmode) db.h db_185.h db_cxx.h
	@echo "Installing DB library: $(libdir) ..."
	@test -d $(libdir) || \
	    ($(mkdir) -p $(libdir) && $(chmod) $(dmode) $(libdir))
	@cd $(libdir) && $(rm) -f $(libdb)
	@$(cp) -p $(libdb) $(libdir)
	@cd $(libdir) && $(chmod) $(fmode) $(libdb)
	@echo "Installing DB utilities: $(bindir) ..."
	@test -d $(bindir) || \
	    ($(mkdir) -p $(bindir) && $(chmod) $(dmode) $(bindir))
	@cd $(bindir) && $(rm) -f $(PROGS)
	@$(cp) -p $(PROGS) $(bindir)
	@cd $(bindir) && (test ! -f $(strip) || $(strip) $(PROGS))
	@cd $(bindir) && $(chmod) $(emode) $(PROGS)
	@echo "Installing documentation: $(mandir) ..."
	@test -d $(mandir) || \
	    ($(mkdir) -p $(mandir) && $(chmod) $(dmode) $(mandir))
	@cd $(srcdir)/docs && $(cp) -pr * $(mandir)/

uninstall:
	-cd $(bindir) && $(rm) -f $(PROGS)
	-cd $(includedir) && $(rm) -f db.h db_185.h db_cxx.h
	-cd $(libdir) && $(rm) -f $(libdb)
	-cd $(mandir) && $(rm) -rf docs

# Programs.
db_archive.o: $(srcdir)/db_archive/db_archive.c
	$(CC) $(CFLAGS) $?
db_checkpoint.o: $(srcdir)/db_checkpoint/db_checkpoint.c
	$(CC) $(CFLAGS) $?
db_deadlock.o: $(srcdir)/db_deadlock/db_deadlock.c
	$(CC) $(CFLAGS) $?
db_dump.o: $(srcdir)/db_dump/db_dump.c
	$(CC) $(CFLAGS) $?
db_dump185.o: $(srcdir)/db_dump185/db_dump185.c
	$(CC) $(CFLAGS) $?
db_load.o: $(srcdir)/db_load/db_load.c
	$(CC) $(CFLAGS) $?
db_printlog.o: $(srcdir)/db_printlog/db_printlog.c
	$(CC) $(CFLAGS) $?
db_recover.o: $(srcdir)/db_recover/db_recover.c
	$(CC) $(CFLAGS) $?
db_stat.o: $(srcdir)/db_stat/db_stat.c
	$(CC) $(CFLAGS) $?

# Examples.
ex_access.o: $(srcdir)/examples/ex_access.c
	$(CC) $(CFLAGS) $?
ex_appinit.o: $(srcdir)/examples/ex_appinit.c
	$(CC) $(CFLAGS) $?
ex_btrec.o: $(srcdir)/examples/ex_btrec.c
	$(CC) $(CFLAGS) $?
ex_lock.o: $(srcdir)/examples/ex_lock.c
	$(CC) $(CFLAGS) $?
ex_mpool.o: $(srcdir)/examples/ex_mpool.c
	$(CC) $(CFLAGS) $?
ex_thread.o: $(srcdir)/examples/ex_thread.c
	$(CC) $(CFLAGS) $?
ex_tpcb.o: $(srcdir)/examples/ex_tpcb.c
	$(CC) $(CFLAGS) $?

# DB files.
db.o: $(srcdir)/db/db.c
	$(CC) $(CFLAGS) $?
db_am.o: $(srcdir)/db/db_am.c
	$(CC) $(CFLAGS) $?
db_auto.o: $(srcdir)/db/db_auto.c
	$(CC) $(CFLAGS) $?
db_conv.o: $(srcdir)/db/db_conv.c
	$(CC) $(CFLAGS) $?
db_dispatch.o: $(srcdir)/db/db_dispatch.c
	$(CC) $(CFLAGS) $?
db_dup.o: $(srcdir)/db/db_dup.c
	$(CC) $(CFLAGS) $?
db_iface.o: $(srcdir)/db/db_iface.c
	$(CC) $(CFLAGS) $?
db_join.o: $(srcdir)/db/db_join.c
	$(CC) $(CFLAGS) $?
db_overflow.o: $(srcdir)/db/db_overflow.c
	$(CC) $(CFLAGS) $?
db_pr.o: $(srcdir)/db/db_pr.c
	$(CC) $(CFLAGS) $?
db_rec.o: $(srcdir)/db/db_rec.c
	$(CC) $(CFLAGS) $?
db_ret.o: $(srcdir)/db/db_ret.c
	$(CC) $(CFLAGS) $?

# Btree source files.
bt_compare.o: $(srcdir)/btree/bt_compare.c
	$(CC) $(CFLAGS) $?
bt_conv.o: $(srcdir)/btree/bt_conv.c
	$(CC) $(CFLAGS) $?
bt_curadj.o: $(srcdir)/btree/bt_curadj.c
	$(CC) $(CFLAGS) $?
bt_cursor.o: $(srcdir)/btree/bt_cursor.c
	$(CC) $(CFLAGS) $?
bt_delete.o: $(srcdir)/btree/bt_delete.c
	$(CC) $(CFLAGS) $?
bt_open.o: $(srcdir)/btree/bt_open.c
	$(CC) $(CFLAGS) $?
bt_page.o: $(srcdir)/btree/bt_page.c
	$(CC) $(CFLAGS) $?
bt_put.o: $(srcdir)/btree/bt_put.c
	$(CC) $(CFLAGS) $?
bt_rec.o: $(srcdir)/btree/bt_rec.c
	$(CC) $(CFLAGS) $?
bt_recno.o: $(srcdir)/btree/bt_recno.c
	$(CC) $(CFLAGS) $?
bt_rsearch.o: $(srcdir)/btree/bt_rsearch.c
	$(CC) $(CFLAGS) $?
bt_search.o: $(srcdir)/btree/bt_search.c
	$(CC) $(CFLAGS) $?
bt_split.o: $(srcdir)/btree/bt_split.c
	$(CC) $(CFLAGS) $?
bt_stack.o: $(srcdir)/btree/bt_stack.c
	$(CC) $(CFLAGS) $?
bt_stat.o: $(srcdir)/btree/bt_stat.c
	$(CC) $(CFLAGS) $?
btree_auto.o: $(srcdir)/btree/btree_auto.c
	$(CC) $(CFLAGS) $?

# C++ interface files.
cxx_app.o: $(srcdir)/cxx/cxx_app.cpp
	$(CXX) $(CXXFLAGS) $?
cxx_except.o: $(srcdir)/cxx/cxx_except.cpp
	$(CXX) $(CXXFLAGS) $?
cxx_lock.o: $(srcdir)/cxx/cxx_lock.cpp
	$(CXX) $(CXXFLAGS) $?
cxx_log.o: $(srcdir)/cxx/cxx_log.cpp
	$(CXX) $(CXXFLAGS) $?
cxx_mpool.o: $(srcdir)/cxx/cxx_mpool.cpp
	$(CXX) $(CXXFLAGS) $?
cxx_table.o: $(srcdir)/cxx/cxx_table.cpp
	$(CXX) $(CXXFLAGS) $?
cxx_txn.o: $(srcdir)/cxx/cxx_txn.cpp
	$(CXX) $(CXXFLAGS) $?

# Hash source files.
hash_auto.o: $(srcdir)/hash/hash_auto.c
	$(CC) $(CFLAGS) $?
hash.o: $(srcdir)/hash/hash.c
	$(CC) $(CFLAGS) $?
hash_conv.o: $(srcdir)/hash/hash_conv.c
	$(CC) $(CFLAGS) $?
hash_dup.o: $(srcdir)/hash/hash_dup.c
	$(CC) $(CFLAGS) $?
hash_func.o: $(srcdir)/hash/hash_func.c
	$(CC) $(CFLAGS) $?
hash_page.o: $(srcdir)/hash/hash_page.c
	$(CC) $(CFLAGS) $?
hash_rec.o: $(srcdir)/hash/hash_rec.c
	$(CC) $(CFLAGS) $?
hash_stat.o: $(srcdir)/hash/hash_stat.c
	$(CC) $(CFLAGS) $?

# Lock source files.
lock.o: $(srcdir)/lock/lock.c
	$(CC) $(CFLAGS) $?
lock_conflict.o:$(srcdir)/lock/lock_conflict.c
	$(CC) $(CFLAGS) $?
lock_deadlock.o:$(srcdir)/lock/lock_deadlock.c
	$(CC) $(CFLAGS) $?
lock_region.o:$(srcdir)/lock/lock_region.c
	$(CC) $(CFLAGS) $?
lock_util.o:$(srcdir)/lock/lock_util.c
	$(CC) $(CFLAGS) $?

# Log source files.
log.o: $(srcdir)/log/log.c
	$(CC) $(CFLAGS) $?
log_archive.o: $(srcdir)/log/log_archive.c
	$(CC) $(CFLAGS) $?
log_auto.o: $(srcdir)/log/log_auto.c
	$(CC) $(CFLAGS) $?
log_compare.o: $(srcdir)/log/log_compare.c
	$(CC) $(CFLAGS) $?
log_findckp.o: $(srcdir)/log/log_findckp.c
	$(CC) $(CFLAGS) $?
log_get.o: $(srcdir)/log/log_get.c
	$(CC) $(CFLAGS) $?
log_put.o: $(srcdir)/log/log_put.c
	$(CC) $(CFLAGS) $?
log_rec.o: $(srcdir)/log/log_rec.c
	$(CC) $(CFLAGS) $?
log_register.o: $(srcdir)/log/log_register.c
	$(CC) $(CFLAGS) $?

# Mpool source files.
mp_bh.o: $(srcdir)/mp/mp_bh.c
	$(CC) $(CFLAGS) $?
mp_fget.o: $(srcdir)/mp/mp_fget.c
	$(CC) $(CFLAGS) $?
mp_fopen.o: $(srcdir)/mp/mp_fopen.c
	$(CC) $(CFLAGS) $?
mp_fput.o: $(srcdir)/mp/mp_fput.c
	$(CC) $(CFLAGS) $?
mp_fset.o: $(srcdir)/mp/mp_fset.c
	$(CC) $(CFLAGS) $?
mp_open.o: $(srcdir)/mp/mp_open.c
	$(CC) $(CFLAGS) $?
mp_pr.o: $(srcdir)/mp/mp_pr.c
	$(CC) $(CFLAGS) $?
mp_region.o: $(srcdir)/mp/mp_region.c
	$(CC) $(CFLAGS) $?
mp_sync.o: $(srcdir)/mp/mp_sync.c
	$(CC) $(CFLAGS) $?

# Mutex source files.
mutex.o: $(srcdir)/mutex/mutex.c
	$(CC) $(CFLAGS) $?
# XXX
# UTS4 spinlocks
uts4_cc.o: $(srcdir)/mutex/uts4_cc.s
	$(AS) $(ASFLAGS) -o $@ $?

# Transaction source files.
txn.o: $(srcdir)/txn/txn.c
	$(CC) $(CFLAGS) $?
txn_auto.o: $(srcdir)/txn/txn_auto.c
	$(CC) $(CFLAGS) $?
txn_rec.o: $(srcdir)/txn/txn_rec.c
	$(CC) $(CFLAGS) $?

# XA source files.
xa.o: $(srcdir)/xa/xa.c
	$(CC) $(CFLAGS) $?
xa_db.o: $(srcdir)/xa/xa_db.c
	$(CC) $(CFLAGS) $?
xa_map.o: $(srcdir)/xa/xa_map.c
	$(CC) $(CFLAGS) $?

# Historic interfaces.
hsearch.o: $(srcdir)/hsearch/hsearch.c
	$(CC) $(CFLAGS) $?
dbm.o: $(srcdir)/dbm/dbm.c
	$(CC) $(CFLAGS) $?
db185.o: $(srcdir)/db185/db185.c
	$(CC) $(CFLAGS) $?

# Common source files.
db_appinit.o: $(srcdir)/common/db_appinit.c
	$(CC) $(CFLAGS) $?
db_apprec.o: $(srcdir)/common/db_apprec.c
	$(CC) $(CFLAGS) $?
db_byteorder.o: $(srcdir)/common/db_byteorder.c
	$(CC) $(CFLAGS) $?
db_err.o: $(srcdir)/common/db_err.c
	$(CC) $(CFLAGS) $?
db_log2.o: $(srcdir)/common/db_log2.c
	$(CC) $(CFLAGS) $?
db_region.o: $(srcdir)/common/db_region.c
	$(CC) $(CFLAGS) $?
db_salloc.o: $(srcdir)/common/db_salloc.c
	$(CC) $(CFLAGS) $?
db_shash.o: $(srcdir)/common/db_shash.c
	$(CC) $(CFLAGS) $?

# OS specific source files.
os_abs.o: $(srcdir)/os/os_abs.c
	$(CC) $(CFLAGS) $?
os_alloc.o: $(srcdir)/os/os_alloc.c
	$(CC) $(CFLAGS) $?
os_config.o: $(srcdir)/os/os_config.c
	$(CC) $(CFLAGS) $?
os_dir.o: $(srcdir)/os/os_dir.c
	$(CC) $(CFLAGS) $?
os_fid.o: $(srcdir)/os/os_fid.c
	$(CC) $(CFLAGS) $?
os_fsync.o: $(srcdir)/os/os_fsync.c
	$(CC) $(CFLAGS) $?
os_map.o: $(srcdir)/os/os_map.c
	$(CC) $(CFLAGS) $?
os_oflags.o: $(srcdir)/os/os_oflags.c
	$(CC) $(CFLAGS) $?
os_open.o: $(srcdir)/os/os_open.c
	$(CC) $(CFLAGS) $?
os_rpath.o: $(srcdir)/os/os_rpath.c
	$(CC) $(CFLAGS) $?
os_rw.o: $(srcdir)/os/os_rw.c
	$(CC) $(CFLAGS) $?
os_seek.o: $(srcdir)/os/os_seek.c
	$(CC) $(CFLAGS) $?
os_sleep.o: $(srcdir)/os/os_sleep.c
	$(CC) $(CFLAGS) $?
os_spin.o: $(srcdir)/os/os_spin.c
	$(CC) $(CFLAGS) $?
os_stat.o: $(srcdir)/os/os_stat.c
	$(CC) $(CFLAGS) $?
os_tmpdir.o: $(srcdir)/os/os_tmpdir.c
	$(CC) $(CFLAGS) $?
os_unlink.o: $(srcdir)/os/os_unlink.c
	$(CC) $(CFLAGS) $?

# Test programs.
.dbtestrc: db.h $(srcdir)/test/test.tcl
	$(rm) -f $@
	cat $(srcdir)/test/test.tcl > $@
tclAppInit.o: $(srcdir)/test/tclAppInit.c
	$(CC) $(CFLAGS) $?
tcl_dbm.o: $(srcdir)/test/tcl_dbm.c
	$(CC) $(CFLAGS) $?
tcl_hsearch.o: $(srcdir)/test/tcl_hsearch.c
	$(CC) $(CFLAGS) $?
tcl_lock.o: $(srcdir)/test/tcl_lock.c
	$(CC) $(CFLAGS) $?
tcl_log.o: $(srcdir)/test/tcl_log.c
	$(CC) $(CFLAGS) $?
tcl_mpool.o: $(srcdir)/test/tcl_mpool.c
	$(CC) $(CFLAGS) $?
tcl_mutex.o: $(srcdir)/test/tcl_mutex.c
	$(CC) $(CFLAGS) $?
tcl_ndbm.o: $(srcdir)/test/tcl_ndbm.c
	$(CC) $(CFLAGS) $?
tcl_txn.o: $(srcdir)/test/tcl_txn.c
	$(CC) $(CFLAGS) $?
utils.o: $(srcdir)/test/utils.c
	$(CC) $(CFLAGS) $?

# Replacement source files.
err.o: $(srcdir)/clib/err.c
	$(CC) $(CFLAGS) $?
getcwd.o: $(srcdir)/clib/getcwd.c
	$(CC) $(CFLAGS) $?
getlong.o: $(srcdir)/clib/getlong.c
	$(CC) $(CFLAGS) $?
getopt.o: $(srcdir)/clib/getopt.c
	$(CC) $(CFLAGS) $?
memcmp.o: $(srcdir)/clib/memcmp.c
	$(CC) $(CFLAGS) $?
memcpy.o: $(srcdir)/clib/memmove.c
	$(CC) -DMEMCOPY $(CFLAGS) $? -o $@
memmove.o: $(srcdir)/clib/memmove.c
	$(CC) -DMEMMOVE $(CFLAGS) $?
raise.o: $(srcdir)/clib/raise.c
	$(CC) $(CFLAGS) $?
snprintf.o: $(srcdir)/clib/snprintf.c
	$(CC) $(CFLAGS) $?
strerror.o: $(srcdir)/clib/strerror.c
	$(CC) $(CFLAGS) $?
strsep.o: $(srcdir)/clib/strsep.c
	$(CC) $(CFLAGS) $?
vsnprintf.o: $(srcdir)/clib/vsnprintf.c
	$(CC) $(CFLAGS) $?
