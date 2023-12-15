### Compiling an eBPF Object File
```bash
hello.bpf.o: %.o: %.c
    clang \
	-target bpf \
	-I/usr/include/$(shell uname -m)-linux-gnu \ 
	-g \
	-O2 -c $< -o $@
```