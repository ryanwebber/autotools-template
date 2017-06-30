# C++ Plus Autotools
Basic template repository for quickly spinning up c++ projects on linux with autotools.


## Building the template:
```
$ sh ./autogen.sh
$ ./configure
$ make
```

## Modifying the template:
 1. Modify code in `src/`
 2. Modify the source files in `src/makefile.am`

## Adding Libraries:
 1. Add library folder to `lib/`
 2. Add library code to folder
 3. Create a `Makefile.am` with contents mocking `lib/xxx/Makefile.am` in the library folder
 4. Add the subdirectory to `lib/Makefile.am`
 5. Add an entry to `AC_CONFIG_FILES` in the root `configure.ac`
 6. Add an entry to the `main_LDADD` in `src/Makefile.am` containing: `$(top_srcdir)/lib/<libname>/<library>.la`
