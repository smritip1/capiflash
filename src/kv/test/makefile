# IBM_PROLOG_BEGIN_TAG
# This is an automatically generated prolog.
#
# $Source: src/kv/test/makefile $
#
# IBM Data Engine for NoSQL - Power Systems Edition User Library Project
#
# Contributors Listed Below - COPYRIGHT 2014,2015
# [+] International Business Machines Corp.
#
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
# implied. See the License for the specific language governing
# permissions and limitations under the License.
#
# IBM_PROLOG_END_TAG

UNAME=$(shell uname)

ALLOW_WARNINGS = yes

ROOTPATH = ../../..
SUBDIRS  =
VPATH   += ..
LCFLAGS  = -D__FVT__ -D__STDC_FORMAT_MACROS -I$(ROOTPATH)/src/kv -I$(GTESTINC) 

GTESTS   = \
 fvt_kv_fixme1 \
 fvt_ark_io fvt_ark_mcio fvt_ark_mc_aio fvt_ark_perf \
 fvt_ark_perf2 fvt_ark_perf_check fvt_ark_io_inject\
 run_sync_async run_fvt_kv run_simple run_scenarios run_sync_pth run_async_cb\
 run_err fvt_kv_tst_persist

GTESTS_NO_MAIN = fvt_ark_perf_tool

fvt_ark_perf_tool_OFILES = kv_utils_db.o fvt_kv_utils.o fvt_kv_utils_async_cb.o\
  fvt_kv_utils_sync_pth.o fvt_trace.o
fvt_kv_tst_persist_OFILES = kv_utils_db.o fvt_kv_utils.o fvt_trace.o
fvt_ark_perf_OFILES   = kv_utils_db.o fvt_kv_utils.o fvt_kv_utils_async_cb.o \
  fvt_kv_utils_sync_pth.o fvt_trace.o
fvt_ark_perf_check_OFILES = kv_utils_db.o fvt_kv_utils.o \
  fvt_kv_utils_async_cb.o fvt_kv_utils_sync_pth.o fvt_trace.o
fvt_ark_perf2_OFILES  = kv_utils_db.o fvt_kv_utils.o fvt_kv_utils_async_cb.o \
  fvt_kv_utils_sync_pth.o fvt_trace.o
fvt_ark_io_inject_OFILES = kv_utils_db.o fvt_kv_utils_async_cb.o \
  fvt_kv_utils_ark_io.o fvt_trace.o
fvt_ark_io_OFILES     = kv_utils_db.o fvt_kv_utils_async_cb.o \
  fvt_kv_utils_ark_io.o fvt_trace.o
fvt_ark_mcio_OFILES   = kv_utils_db.o fvt_kv_utils.o fvt_kv_utils_sync_pth.o \
   fvt_trace.o
fvt_ark_mc_aio_OFILES = kv_utils_db.o fvt_kv_utils.o fvt_kv_utils_async_cb.o \
   fvt_trace.o
fvt_kv_fixme1_OFILES  = kv_utils_db.o fvt_kv_utils_async_cb.o fvt_kv_utils.o \
  fvt_kv_utils_sync_pth.o fvt_kv_utils_ark_io.o fvt_trace.o
run_fvt_kv_OFILES  = \
  fvt_kv_tst_simple.o fvt_kv_tst_scenario.o \
  fvt_kv_tst_sync_pth.o fvt_kv_tst_async_cb.o fvt_kv_tst_sync_async.o \
  fvt_kv_tst_errors.o fvt_kv_tst_persist.o fvt_kv_utils_ark_io.o \
  fvt_kv_utils_async_cb.o kv_utils_db.o fvt_kv_utils.o fvt_kv_utils_sync_pth.o \
  fvt_trace.o
run_simple_OFILES  = fvt_kv_tst_simple.o kv_utils_db.o fvt_kv_utils.o \
  fvt_trace.o
run_scenarios_OFILES = fvt_kv_tst_scenario.o kv_utils_db.o fvt_kv_utils.o \
   fvt_trace.o
run_sync_pth_OFILES = fvt_kv_tst_sync_pth.o fvt_kv_utils_sync_pth.o \
  fvt_kv_utils.o kv_utils_db.o fvt_trace.o
run_async_cb_OFILES  = fvt_kv_tst_async_cb.o kv_utils_db.o \
  fvt_kv_utils_async_cb.o fvt_kv_utils.o fvt_trace.o
run_sync_async_OFILES = fvt_kv_tst_sync_async.o kv_utils_db.o \
  fvt_kv_utils_async_cb.o fvt_kv_utils.o fvt_kv_utils_sync_pth.o \
  fvt_kv_utils_ark_io.o fvt_trace.o
run_err_OFILES = fvt_kv_tst_errors.o fvt_kv_utils.o kv_utils_db.o \
  fvt_kv_utils_async_cb.o fvt_kv_utils_ark_io.o fvt_trace.o

include ${ROOTPATH}/config.mk
include $(ROOTPATH)/src/test/framework/gtest.objtests.mk

LINKLIBS += -lcflshcom$(SOVER) -lcflsh_block$(SOVER) -larkdb$(SOVER) -larkalloc$(SOVER)

unit:
	@$(TESTDIR)/run_fvt_kv$(BITS) --gtest_output=xml:$(TESTDIR)/kv_fvt_results.xml;
