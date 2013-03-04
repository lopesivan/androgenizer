#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([androgenizer], [1.0], [victor.lavaud@gmail.com])
AM_INIT_AUTOMAKE
AC_LANG(C)
AC_CONFIG_SRCDIR([emit.h])
AC_CONFIG_HEADERS([config.h])

AC_ARG_ENABLE([debug],
  [  --enable-debug	adds asserts and debug code to the build.],
  [debug_mode=${enableval}],
  [debug_mode=no])
  
if test "x$debug_mode" = "xno"
then
  CFLAGS="$CFLAGS -DNDEBUG"
fi


# Checks for programs.
AC_PROG_CC

# Checks for libraries.

# Checks for header files.
AC_CHECK_HEADERS([malloc.h stdlib.h string.h sys/param.h])

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.
AC_FUNC_MALLOC
AC_FUNC_REALLOC
AC_CHECK_FUNCS([strdup strncasecmp strstr])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
