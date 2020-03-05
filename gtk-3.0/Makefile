## Developer Tasks

all: sass

sass: sass-command
	@$(SASS) --update --sourcemap=none .


## Run Recipes w/Automated Requirements

include .Makefile.d-init.mk
include .Makefile.d/ruby.mk

SASS := $(GEM_HOME)/bin/sass

$(SASS): Gemfile | bundle-command
	@$(BUNDLE) install
	@touch $@

sass-command: $(SASS)
	@true
