# Copyright 2018 Amazon.com, Inc. or its affiliates. All Rights Reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License"). You may not use
# this file except in compliance with the License. A copy of the License is
# located at
#
#     http://aws.amazon.com/apache2.0/
#
# or in the "license" file accompanying this file. This file is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
# implied. See the License for the specific language governing permissions and
# limitations under the License.

###########
#NOTE: If we don't use the unwindset, leave it empty
CBMC_UNWINDSET = --unwindset
CBMC_UNWINDSET += __builtin___memcpy_chk.0:5,
CBMC_UNWINDSET := $(CBMC_UNWINDSET)aws_mem_release:1,
CBMC_UNWINDSET := $(CBMC_UNWINDSET)memcpy.0:5,
CBMC_UNWINDSET := $(CBMC_UNWINDSET)strlen.0:5

CBMCFLAGS +=

DEPENDENCIES =  $(HELPERDIR)/source/make_common_data_structures.c \
		   $(HELPERDIR)/stubs/error.c \
	       $(HELPERDIR)/stubs/memcpy_override.c \
	       $(SRCDIR)/source/array_list.c \
	       $(SRCDIR)/source/common.c

ENTRY = aws_array_list_set_at_harness
###########

include ../Makefile.common
