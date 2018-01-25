cmake_minimum_required(VERSION 3.9)
project(emacs)

#set(CMAKE_CXX_STANDARD 11)
#set (CMAKE_C_STANDARD 99)
#set(CMAKE_C_FLAGS "-std=c99")
macro(use_c99)
    if (CMAKE_VERSION VERSION_LESS "3.1")
        if (CMAKE_C_COMPILER_ID STREQUAL "GNU")
            set (CMAKE_C_FLAGS "-std=gnu99 ${CMAKE_C_FLAGS}")
        endif ()
    else ()
        set (CMAKE_C_STANDARD 99)
    endif ()
endmacro(use_c99)

use_c99()

add_executable(emacs
lib-src/ctags.c
lib-src/ebrowse.c
lib-src/emacsclient.c
lib-src/etags.c
lib-src/hexl.c
lib-src/make-docfile.c
lib-src/movemail.c
lib-src/ntlib.c
lib-src/ntlib.h
lib-src/pop.c
lib-src/pop.h
lib-src/profile.c
lib-src/update-game-score.c
src/alloc.c
src/atimer.c
src/atimer.h
src/bidi.c
src/blockinput.h
src/buffer.c
src/buffer.h
src/buildobj.h
src/bytecode.c
src/callint.c
src/callproc.c
src/casefiddle.c
src/casetab.c
src/category.c
src/category.h
src/ccl.c
src/ccl.h
src/character.c
src/character.h
src/charset.c
src/charset.h
src/chartab.c
src/cm.c
src/cm.h
src/cmds.c
src/coding.c
src/coding.h
src/commands.h
src/composite.c
src/composite.h
src/conf_post.h
src/config.h
src/cygw32.c
src/cygw32.h
src/data.c
src/dbusbind.c
src/decompress.c
src/dired.c
src/dispextern.h
src/dispnew.c
src/disptab.h
src/doc.c
src/doprnt.c
src/dosfns.c
src/dosfns.h
src/dynlib.c
src/dynlib.h
src/editfns.c
src/emacs-icon.h
src/emacs-module.c
src/emacs-module.h
src/emacs.c
src/emacsgtkfixed.c
src/emacsgtkfixed.h
src/epaths.h
src/eval.c
src/fileio.c
src/filelock.c
src/firstfile.c
src/floatfns.c
src/fns.c
src/font.c
src/font.h
src/fontset.c
src/fontset.h
src/frame.c
src/frame.h
src/fringe.c
src/ftcrfont.c
src/ftfont.c
src/ftfont.h
src/ftxfont.c
src/getpagesize.h
src/gfilenotify.c
src/globals.h
src/gmalloc.c
src/gnutls.c
src/gnutls.h
src/gtkutil.c
src/gtkutil.h
src/image.c
src/indent.c
src/indent.h
src/inotify.c
src/insdel.c
src/intervals.c
src/intervals.h
src/json.c
src/keyboard.c
src/keyboard.h
src/keymap.c
src/keymap.h
src/kqueue.c
src/lastfile.c
src/lcms.c
src/lisp.h
src/lread.c
src/macfont.h
src/macros.c
src/macros.h
src/macuvs.h
src/marker.c
src/menu.c
src/menu.h
src/minibuf.c
src/module-env-25.h
src/module-env-26.h
src/msdos.c
src/msdos.h
src/nsgui.h
src/nsterm.h
src/print.c
src/process.c
src/process.h
src/profiler.c
src/ptr-bounds.h
src/puresize.h
src/ralloc.c
src/regex.c
src/regex.h
src/region-cache.c
src/region-cache.h
src/scroll.c
src/search.c
src/sheap.c
src/sheap.h
src/sound.c
src/syntax.c
src/syntax.h
src/sysdep.c
src/sysselect.h
src/syssignal.h
src/sysstdio.h
src/systhread.c
src/systhread.h
src/systime.h
src/systty.h
src/syswait.h
src/term.c
src/termcap.c
src/termchar.h
src/termhooks.h
src/terminal.c
src/terminfo.c
src/termopts.h
src/textprop.c
src/thread.c
src/thread.h
src/tparam.c
src/tparam.h
src/undo.c
src/unexaix.c
src/unexcoff.c
src/unexcw.c
src/unexec.h
src/unexelf.c
src/unexhp9k800.c
src/unexmacosx.c
src/unexsol.c
src/unexw32.c
src/vm-limit.c
src/w16select.c
src/w32.c
src/w32.h
src/w32common.h
src/w32console.c
src/w32fns.c
src/w32font.c
src/w32font.h
src/w32gui.h
src/w32heap.c
src/w32heap.h
src/w32inevt.c
src/w32inevt.h
src/w32menu.c
src/w32notify.c
src/w32proc.c
src/w32reg.c
src/w32select.c
src/w32select.h
src/w32term.c
src/w32term.h
src/w32uniscribe.c
src/w32xfns.c
src/widget.c
src/widget.h
src/widgetprv.h
src/window.c
src/window.h
src/xdisp.c
src/xfaces.c
src/xfns.c
src/xfont.c
src/xftfont.c
src/xgselect.c
src/xgselect.h
src/xmenu.c
src/xml.c
src/xrdb.c
src/xselect.c
src/xsettings.c
src/xsettings.h
src/xsmfns.c
src/xterm.c
src/xterm.h
src/xwidget.c
src/xwidget.h

)

#        admin/alloc-colors.c
#        lib/sys/select.h
#        lib/sys/stat.h
#        lib/sys/time.h
#        lib/sys/types.h
#        lib/_Noreturn.h
#        lib/acl-errno-valid.c
#        lib/acl-internal.c
#        lib/acl-internal.h
#        lib/acl.h
#        lib/acl_entries.c
#        lib/alloca.h
#        lib/alloca.in.h
#        lib/allocator.c
#        lib/allocator.h
#        lib/arg-nonnull.h
#        lib/at-func.c
#        lib/binary-io.c
#        lib/binary-io.h
#        lib/byteswap.h
#        lib/byteswap.in.h
#        lib/c++defs.h
#        lib/c-ctype.c
#        lib/c-ctype.h
#        lib/c-strcase.h
#        lib/c-strcasecmp.c
#        lib/c-strncasecmp.c
#        lib/careadlinkat.c
#        lib/careadlinkat.h
#        lib/close-stream.c
#        lib/close-stream.h
#        lib/count-leading-zeros.c
#        lib/count-leading-zeros.h
#        lib/count-one-bits.c
#        lib/count-one-bits.h
#        lib/count-trailing-zeros.c
#        lib/count-trailing-zeros.h
#        lib/dirent.h
#        lib/dirent.in.h
#        lib/dirfd.c
#        lib/dosname.h
#        lib/dtoastr.c
#        lib/dtotimespec.c
#        lib/dup2.c
#        lib/errno.in.h
#        lib/euidaccess.c
#        lib/execinfo.c
#        lib/execinfo.in.h
#        lib/faccessat.c
#        lib/fcntl.c
#        lib/fcntl.h
#        lib/fcntl.in.h
#        lib/fdatasync.c
#        lib/fdopendir.c
#        lib/filemode.c
#        lib/filemode.h
#        lib/filevercmp.c
#        lib/filevercmp.h
#        lib/flexmember.h
#        lib/fpending.c
#        lib/fpending.h
#        lib/fstatat.c
#        lib/fsync.c
#        lib/ftoastr.c
#        lib/ftoastr.h
#        lib/get-permissions.c
#        lib/getdtablesize.c
#        lib/getgroups.c
#        lib/getloadavg.c
#        lib/getopt-cdefs.h
#        lib/getopt-cdefs.in.h
#        lib/getopt-core.h
#        lib/getopt-ext.h
#        lib/getopt-pfx-core.h
#        lib/getopt-pfx-ext.h
#        lib/getopt.c
#        lib/getopt.h
#        lib/getopt.in.h
#        lib/getopt1.c
#        lib/gettext.h
#        lib/gettime.c
#        lib/gettimeofday.c
#        lib/group-member.c
#        lib/ignore-value.h
#        lib/intprops.h
#        lib/inttypes.h
#        lib/inttypes.in.h
#        lib/limits.h
#        lib/limits.in.h
#        lib/lstat.c
#        lib/md5.c
#        lib/md5.h
#        lib/memrchr.c
#        lib/min-max.h
#        lib/mkostemp.c
#        lib/mktime-internal.h
#        lib/mktime.c
#        lib/openat-die.c
#        lib/openat-priv.h
#        lib/openat-proc.c
#        lib/openat.h
#        lib/pipe2.c
#        lib/pselect.c
#        lib/pthread_sigmask.c
#        lib/putenv.c
#        lib/qcopy-acl.c
#        lib/readlink.c
#        lib/readlinkat.c
#        lib/root-uid.h
#        lib/save-cwd.c
#        lib/save-cwd.h
#        lib/secure_getenv.c
#        lib/set-permissions.c
#        lib/sha1.c
#        lib/sha1.h
#        lib/sha256.c
#        lib/sha256.h
#        lib/sha512.c
#        lib/sha512.h
#        lib/sig2str.c
#        lib/sig2str.h
#        lib/signal.h
#        lib/signal.in.h
#        lib/stat-time.c
#        lib/stat-time.h
#        lib/stat.c
#        lib/stdalign.h
#        lib/stdalign.in.h
#        lib/stddef.in.h
#        lib/stdint.h
#        lib/stdint.in.h
#        lib/stdio-impl.h
#        lib/stdio.h
#        lib/stdio.in.h
#        lib/stdlib.h
#        lib/stdlib.in.h
#        lib/stpcpy.c
#        lib/strftime.c
#        lib/strftime.h
#        lib/string.h
#        lib/string.in.h
#        lib/strtoimax.c
#        lib/strtol.c
#        lib/strtoll.c
#        lib/strtoul.c
#        lib/strtoull.c
#        lib/strtoumax.c
#        lib/symlink.c
#        lib/sys_select.in.h
#        lib/sys_stat.in.h
#        lib/sys_time.in.h
#        lib/sys_types.in.h
#        lib/tempname.c
#        lib/tempname.h
#        lib/time-internal.h
#        lib/time.h
#        lib/time.in.h
#        lib/time_r.c
#        lib/time_rz.c
#        lib/timegm.c
#        lib/timespec-add.c
#        lib/timespec-sub.c
#        lib/timespec.c
#        lib/timespec.h
#        lib/u64.c
#        lib/u64.h
#        lib/unistd.c
#        lib/unistd.h
#        lib/unistd.in.h
#        lib/utimens.c
#        lib/utimens.h
#        lib/verify.h
#        lib/vla.h
#        lib/warn-on-use.h
#        lib/xalloc-oversized.h
#        lib-src/ctags.c
#        lib-src/ebrowse.c
#        lib-src/emacsclient.c
#        lib-src/etags.c
#        lib-src/hexl.c
#        lib-src/make-docfile.c
#        lib-src/movemail.c
#        lib-src/ntlib.c
#        lib-src/ntlib.h
#        lib-src/pop.c
#        lib-src/pop.h
#        lib-src/profile.c
#        lib-src/update-game-score.c
#        lwlib/lwlib-int.h
#        lwlib/lwlib-utils.c
#        lwlib/lwlib-utils.h
#        lwlib/lwlib-widget.h
#        lwlib/lwlib-Xaw.c
#        lwlib/lwlib-Xaw.h
#        lwlib/lwlib-Xlw.c
#        lwlib/lwlib-Xlw.h
#        lwlib/lwlib-Xm.c
#        lwlib/lwlib-Xm.h
#        lwlib/lwlib.c
#        lwlib/lwlib.h
#        lwlib/xlwmenu.c
#        lwlib/xlwmenu.h
#        lwlib/xlwmenuP.h
#        modules/mod-test/mod-test.c
#        msdos/inttypes.h
#        nt/inc/arpa/inet.h
#        nt/inc/netinet/in.h
#        nt/inc/sys/acl.h
#        nt/inc/sys/file.h
#        nt/inc/sys/ioctl.h
#        nt/inc/sys/mman.h
#        nt/inc/sys/param.h
#        nt/inc/sys/resource.h
#        nt/inc/sys/socket.h
#        nt/inc/sys/stat.h
#        nt/inc/sys/time.h
#        nt/inc/sys/wait.h
#        nt/inc/dirent.h
#        nt/inc/grp.h
#        nt/inc/inttypes.h
#        nt/inc/langinfo.h
#        nt/inc/mingw_time.h
#        nt/inc/ms-w32.h
#        nt/inc/netdb.h
#        nt/inc/nl_types.h
#        nt/inc/pwd.h
#        nt/inc/stdalign.h
#        nt/inc/stdbool.h
#        nt/inc/stdint.h
#        nt/inc/unistd.h
#        nt/addpm.c
#        nt/cmdproxy.c
#        nt/ddeclient.c
#        nt/preprep.c
#        nt/runemacs.c
#        oldXMenu/Activate.c
#        oldXMenu/AddPane.c
#        oldXMenu/AddSel.c
#        oldXMenu/ChgPane.c
#        oldXMenu/ChgSel.c
#        oldXMenu/copyright.h
#        oldXMenu/Create.c
#        oldXMenu/DelPane.c
#        oldXMenu/DelSel.c
#        oldXMenu/Destroy.c
#        oldXMenu/Error.c
#        oldXMenu/EvHand.c
#        oldXMenu/FindPane.c
#        oldXMenu/FindSel.c
#        oldXMenu/InsPane.c
#        oldXMenu/insque.c
#        oldXMenu/InsSel.c
#        oldXMenu/Internal.c
#        oldXMenu/Locate.c
#        oldXMenu/Post.c
#        oldXMenu/Recomp.c
#        oldXMenu/SetAEQ.c
#        oldXMenu/SetFrz.c
#        oldXMenu/SetPane.c
#        oldXMenu/SetSel.c
#        oldXMenu/X10.h
#        oldXMenu/XCrAssoc.c
#        oldXMenu/XDelAssoc.c
#        oldXMenu/XDestAssoc.c
#        oldXMenu/XLookAssoc.c
#        oldXMenu/XMakeAssoc.c
#        oldXMenu/XMenu.h
#        oldXMenu/XMenuInt.h
#        src/alloc.c
#        src/atimer.c
#        src/atimer.h
#        src/bidi.c
#        src/blockinput.h
#        src/buffer.c
#        src/buffer.h
#        src/buildobj.h
#        src/bytecode.c
#        src/callint.c
#        src/callproc.c
#        src/casefiddle.c
#        src/casetab.c
#        src/category.c
#        src/category.h
#        src/ccl.c
#        src/ccl.h
#        src/character.c
#        src/character.h
#        src/charset.c
#        src/charset.h
#        src/chartab.c
#        src/cm.c
#        src/cm.h
#        src/cmds.c
#        src/coding.c
#        src/coding.h
#        src/commands.h
#        src/composite.c
#        src/composite.h
#        src/conf_post.h
#        src/config.h
#        src/cygw32.c
#        src/cygw32.h
#        src/data.c
#        src/dbusbind.c
#        src/decompress.c
#        src/dired.c
#        src/dispextern.h
#        src/dispnew.c
#        src/disptab.h
#        src/doc.c
#        src/doprnt.c
#        src/dosfns.c
#        src/dosfns.h
#        src/dynlib.c
#        src/dynlib.h
#        src/editfns.c
#        src/emacs-icon.h
#        src/emacs-module.c
#        src/emacs-module.h
#        src/emacs.c
#        src/emacsgtkfixed.c
#        src/emacsgtkfixed.h
#        src/epaths.h
#        src/eval.c
#        src/fileio.c
#        src/filelock.c
#        src/firstfile.c
#        src/floatfns.c
#        src/fns.c
#        src/font.c
#        src/font.h
#        src/fontset.c
#        src/fontset.h
#        src/frame.c
#        src/frame.h
#        src/fringe.c
#        src/ftcrfont.c
#        src/ftfont.c
#        src/ftfont.h
#        src/ftxfont.c
#        src/getpagesize.h
#        src/gfilenotify.c
#        src/globals.h
#        src/gmalloc.c
#        src/gnutls.c
#        src/gnutls.h
#        src/gtkutil.c
#        src/gtkutil.h
#        src/image.c
#        src/indent.c
#        src/indent.h
#        src/inotify.c
#        src/insdel.c
#        src/intervals.c
#        src/intervals.h
#        src/keyboard.c
#        src/keyboard.h
#        src/keymap.c
#        src/keymap.h
#        src/kqueue.c
#        src/lastfile.c
#        src/lisp.h
#        src/lread.c
#        src/macfont.h
#        src/macros.c
#        src/macros.h
#        src/macuvs.h
#        src/marker.c
#        src/menu.c
#        src/menu.h
#        src/minibuf.c
#        src/msdos.c
#        src/msdos.h
#        src/nsgui.h
#        src/nsterm.h
#        src/print.c
#        src/process.c
#        src/process.h
#        src/profiler.c
#        src/puresize.h
#        src/ralloc.c
#        src/regex.c
#        src/regex.h
#        src/region-cache.c
#        src/region-cache.h
#        src/scroll.c
#        src/search.c
#        src/sheap.c
#        src/sheap.h
#        src/sound.c
#        src/syntax.c
#        src/syntax.h
#        src/sysdep.c
#        src/sysselect.h
#        src/syssignal.h
#        src/sysstdio.h
#        src/systhread.c
#        src/systhread.h
#        src/systime.h
#        src/systty.h
#        src/syswait.h
#        src/term.c
#        src/termcap.c
#        src/termchar.h
#        src/termhooks.h
#        src/terminal.c
#        src/terminfo.c
#        src/termopts.h
#        src/textprop.c
#        src/thread.c
#        src/thread.h
#        src/tparam.c
#        src/tparam.h
#        src/undo.c
#        src/unexaix.c
#        src/unexcoff.c
#        src/unexcw.c
#        src/unexec.h
#        src/unexelf.c
#        src/unexhp9k800.c
#        src/unexmacosx.c
#        src/unexsol.c
#        src/unexw32.c
#        src/vm-limit.c
#        src/w16select.c
#        src/w32.c
#        src/w32.h
#        src/w32common.h
#        src/w32console.c
#        src/w32fns.c
#        src/w32font.c
#        src/w32font.h
#        src/w32gui.h
#        src/w32heap.c
#        src/w32heap.h
#        src/w32inevt.c
#        src/w32inevt.h
#        src/w32menu.c
#        src/w32notify.c
#        src/w32proc.c
#        src/w32reg.c
#        src/w32select.c
#        src/w32select.h
#        src/w32term.c
#        src/w32term.h
#        src/w32uniscribe.c
#        src/w32xfns.c
#        src/widget.c
#        src/widget.h
#        src/widgetprv.h
#        src/window.c
#        src/window.h
#        src/xdisp.c
#        src/xfaces.c
#        src/xfns.c
#        src/xfont.c
#        src/xftfont.c
#        src/xgselect.c
#        src/xgselect.h
#        src/xmenu.c
#        src/xml.c
#        src/xrdb.c
#        src/xselect.c
#        src/xsettings.c
#        src/xsettings.h
#        src/xsmfns.c
#        src/xterm.c
#        src/xterm.h
#        src/xwidget.c
#        src/xwidget.h
#        test/lisp/progmodes/flymake-resources/test.c
#        test/manual/cedet/tests/test.c
#        test/manual/cedet/tests/testdoublens.cpp
#        test/manual/cedet/tests/testdoublens.hpp
#        test/manual/cedet/tests/testfriends.cpp
#        test/manual/cedet/tests/testnsp.cpp
#        test/manual/cedet/tests/testpolymorph.cpp
#        test/manual/cedet/tests/testspp.c
#        test/manual/cedet/tests/testsppcomplete.c
#        test/manual/cedet/tests/testsppreplace.c
#        test/manual/cedet/tests/testsppreplaced.c
#        test/manual/cedet/tests/testsubclass.cpp
#        test/manual/cedet/tests/testsubclass.hh
#        test/manual/cedet/tests/testtypedefs.cpp
#        test/manual/cedet/tests/testvarnames.c
#        test/manual/etags/c-src/a/b/b.c
#        test/manual/etags/c-src/emacs/src/gmalloc.c
#        test/manual/etags/c-src/emacs/src/keyboard.c
#        test/manual/etags/c-src/emacs/src/lisp.h
#        test/manual/etags/c-src/emacs/src/regex.h
#        test/manual/etags/c-src/abbrev.c
#        test/manual/etags/c-src/c.c
#        test/manual/etags/c-src/dostorture.c
#        test/manual/etags/c-src/etags.c
#        test/manual/etags/c-src/exit.c
#        test/manual/etags/c-src/fail.c
#        test/manual/etags/c-src/getopt.h
#        test/manual/etags/c-src/h.h
#        test/manual/etags/c-src/machsyscalls.c
#        test/manual/etags/c-src/machsyscalls.h
#        test/manual/etags/c-src/sysdep.h
#        test/manual/etags/c-src/tab.c
#        test/manual/etags/c-src/torture.c
#        test/manual/etags/cp-src/burton.cpp
#        test/manual/etags/cp-src/c.C
#        test/manual/etags/cp-src/clheir.hpp
#        test/manual/etags/cp-src/conway.cpp
#        test/manual/etags/cp-src/conway.hpp
#        test/manual/etags/cp-src/fail.C
#        test/manual/etags/cp-src/functions.cpp
#        test/manual/etags/cp-src/MDiagArray2.h
#        test/manual/etags/cp-src/Range.h
#        test/manual/etags/cp-src/screen.cpp
#        test/manual/etags/cp-src/screen.hpp
#        test/manual/etags/cp-src/x.cc
#        test/manual/etags/objc-src/PackInsp.h
#        test/manual/etags/objc-src/Subprocess.h
#        test/manual/etags/objcpp-src/SimpleCalc.H
#        test/manual/etags/y-src/cccp.c
#        test/manual/etags/y-src/parse.c)
