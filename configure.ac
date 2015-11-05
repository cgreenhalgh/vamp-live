
AC_INIT(vamp-live, 1.0, chris.greenhalgh@nottingham.ac.uk)

AC_CONFIG_SRCDIR(host/system.h)

AC_PROG_CXX
AC_HEADER_STDC
AC_C_BIGENDIAN

PKG_CHECK_MODULES([VAMP_HOSTSDK],[vamp-hostsdk])

AC_SUBST(VAMP_HOSTSDK_CFLAGS)
AC_SUBST(VAMP_HOSTSDK_LIBS)

AC_SEARCH_LIBS([dlopen],[dl])

PKG_CHECK_MODULES([SNDFILE],[sndfile])

AC_SUBST(SNDFILE_CFLAGS)
AC_SUBST(SNDFILE_LIBS)

changequote(,)dnl
if test "x$GCC" = "xyes"; then
  case " $CXXFLAGS " in
    *[\ \	]-fPIC\ -Wall[\ \	]*) ;;
    *) CXXFLAGS="$CXXFLAGS -fPIC -Wall -Wextra" ;;
  esac
  case " $CFLAGS " in
    *[\ \	]-fPIC\ -Wall[\ \	]*) ;;
    *) CFLAGS="$CFLAGS -fPIC -Wall -Wextra" ;;
  esac
fi
changequote([,])dnl

AC_SUBST(CXXFLAGS)
AC_SUBST(CFLAGS)
AC_OUTPUT([Makefile])

