
VERSION ?= 0.0
CENTER ?= ytnef-tools

PODS := $(wildcard *.pod)
MANPAGES := $(PODS:%.pod=%.1)

P2M := pod2man -s 1 -u -c $(CENTER) -r $(VERSION)

all: $(MANPAGES)

clean:
	@rm -f $(MANPAGES)

%.1: %.pod
	@$(P2M) $< > $@

.PHONY: all clean
