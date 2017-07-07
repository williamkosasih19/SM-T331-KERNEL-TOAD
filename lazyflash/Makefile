
EXCLUDE := Makefile README.md *.git* kernel.zip

all: 
	@echo "Creating ZIP: kernel_test.zip"
	@zip -r9 "kernel.zip" . -x $(EXCLUDE)
	@echo "Done."
	@cp kernel.zip ../test_kernel/test_kernel.zip
