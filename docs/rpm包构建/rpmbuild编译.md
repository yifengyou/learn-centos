# rpmbuild编译

## rpmbuild man帮助

```
Usage: rpmbuild [OPTION...]

Build options with [ <specfile> | <tarball> | <source package> ]:
  -bp                           build through %prep (unpack sources and apply patches) from <specfile>
  -bc                           build through %build (%prep, then compile) from <specfile>
  -bi                           build through %install (%prep, %build, then install) from <specfile>
  -bl                           verify %files section from <specfile>
  -ba                           build source and binary packages from <specfile>
  -bb                           build binary package only from <specfile>
  -bs                           build source package only from <specfile>
  -tp                           build through %prep (unpack sources and apply patches) from <tarball>
  -tc                           build through %build (%prep, then compile) from <tarball>
  -ti                           build through %install (%prep, %build, then install) from <tarball>
  -ta                           build source and binary packages from <tarball>
  -tb                           build binary package only from <tarball>
  -ts                           build source package only from <tarball>
  --rebuild                     build binary package from <source package>
  --recompile                   build through %install (%prep, %build, then install) from <source package>
  --buildroot=DIRECTORY         override build root
  --clean                       remove build tree when done
  --nobuild                     do not execute any stages of the build
  --nodeps                      do not verify build dependencies
  --nodirtokens                 generate package header(s) compatible with (legacy) rpm v3 packaging
  --noclean                     do not execute %clean stage of the build
  --nocheck                     do not execute %check stage of the build
  --rmsource                    remove sources when done
  --rmspec                      remove specfile when done
  --short-circuit               skip straight to specified stage (only for c,i)
  --target=CPU-VENDOR-OS        override target platform

Common options for all rpm modes and executables:
  -D, --define='MACRO EXPR'     define MACRO with value EXPR
  --undefine=MACRO              undefine MACRO
  -E, --eval='EXPR'             print macro expansion of EXPR
  --macros=<FILE:...>           read <FILE:...> instead of default file(s)
  --noplugins                   don't enable any plugins
  --nodigest                    don't verify package digest(s)
  --nosignature                 don't verify package signature(s)
  --rcfile=<FILE:...>           read <FILE:...> instead of default file(s)
  -r, --root=ROOT               use ROOT as top level directory (default: "/")
  --dbpath=DIRECTORY            use database in DIRECTORY
  --querytags                   display known query tags
  --showrc                      display final rpmrc and macro configuration
  --quiet                       provide less detailed output
  -v, --verbose                 provide more detailed output
  --version                     print the version of rpm being used

Options implemented via popt alias/exec:
  --with=<option>               enable configure <option> for build
  --without=<option>            disable configure <option> for build
  --buildpolicy=<policy>        set buildroot <policy> (e.g. compress man pages)
  --sign                        generate GPG signature (deprecated, use command rpmsign instead)

Help options:
  -?, --help                    Show this help message
  --usage                       Display brief usage message

```

## rpmbuild常用方法

```
rpmbuild -ba ./FILENAME.spec
```

```
-ba                           build source and binary packages from <specfile>
```


## 参考

* <https://www.cnblogs.com/jing99/p/9672295.html>
