######################################################################
# Copyright (C) 2011 Hewlett-Packard Development Company, L.P.
#
# This program is free software; you can redistribute it and/or
# modify it under the terms of the GNU General Public License
# version 2 as published by the Free Software Foundation.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License along
# with this program; if not, write to the Free Software Foundation, Inc.,
# 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.
######################################################################
TOP = ../../../..
VARS = $(TOP)/Makefile.conf
include $(VARS)

TESTFILE = ft_cliPkgagentTest.php
AGENTDIR = ../../agent

all:
	$(MAKE) -C $(AGENTDIR)/ $@

test: all
	@echo "make pkgagent functional test"
	phpunit --log-junit pkgagent-Xunit.xml $(TESTFILE)

coverage:
	@echo "no coverage for agent_tests/Functional"


clean:
	rm -f *.xml

.PHONY: all test coverage clean
