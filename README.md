# no-runtime

To get rid of C++ run-time, add

* Compile options
```
target_compile_options(
    no-runtime PRIVATE
    "/GS-"
)
```

* Link options
```
target_link_options(
    no-runtime PRIVATE
    "/ENTRY:<your_entry_point>" "/NODEFAULTLIB"
)
```
