AC_PREREQ(2.57)
AC_INIT(sipXiso, 4.2.1, sipx-dev@list.sipfoundry.org)
AC_CONFIG_SRCDIR([src/ks.m4])
AC_ARG_VAR(ISO_DIR, [Directory containing your CentOS CD disk 1 ISO])
if test "x$ISO_DIR" == "x"; then
   ISO_DIR=./ISO
fi
if [ ! test -d $ISO_DIR ]; then
   AC_MSG_ERROR(Directory $ISO_DIR is missing)
fi
AC_ARG_VAR(REPO_DIR, [Directory containing your sipx rpms])
if test "x$REPO_DIR" == "x"; then
   REPO_DIR=./repo
fi
if [ ! test -d $REPO_DIR ]; then
   AC_MSG_ERROR(Directory $REPO_DIR is missing)
fi
if [ ! grep -q CentOS /etc/redhat-release 2>/dev/null ] ; then
   AC_MSG_ERROR(This needs to be run on CentOS machine only)
fi
AC_PATH_PROG(CREATEREPO, createrepo)
if test "x$CREATEREPO" == "x"; then
  AC_MSG_ERROR(createrepo needs to be installed)
fi
AC_CONFIG_FILES([Makefile])
AC_OUTPUT