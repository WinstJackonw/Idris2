include ../config.mk

.PHONY: build build-c build-chez

build: build-c build-chez

build-c:
	@${MAKE} -C c

build-chez:
	@${MAKE} -C chez

.PHONY: clean clean-c clean-chez

clean: clean-c clean-chez

clean-c:
	@${MAKE} -C c cleandep

clean-chez:
	@${MAKE} -C chez clean

.PHONY: install install-docs install-c install-chez

install: install-docs install-c install-chez

install-docs:
	mkdir -p ${DESTDIR}${PREFIX}/${NAME_VERSION}/support/docs
	install -m 644 docs/*.css ${DESTDIR}${PREFIX}/${NAME_VERSION}/support/docs

install-c:
	@${MAKE} -C c install

install-chez:
	@${MAKE} -C chez install
