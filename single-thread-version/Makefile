##
# @file This file is part of stockast.
#
# @section LICENSE
# MIT License
# 
# Copyright (c) 2017-2019 Rajdeep Konwar
#
# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to deal
# in the Software without restriction, including without limitation the rights
# to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
# copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:
#
# The above copyright notice and this permission notice shall be included in all
# copies or substantial portions of the Software.
#
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
# AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
# SOFTWARE.
#
# @section DESCRIPTION
# Makefile.
##

#CXX = clang++
CXX ?= g++
#CXXFLAGS=-std=c++11 -O2 
CXXFLAGS=-std=c++14 -O3 

stockast.o: stockast.cpp
stockast-no-syscall.o: stockast-no-syscall.cpp

OBJECT=stockast.o
OBJECT_NO_SYSCALL=stockast-no-syscall.o


stockast: $(OBJECTS)
	$(CXX) $(CXXFLAGS) $(OBJECT) -o stockast

stockast-no-syscall: stockast-no-syscall.o
	$(CXX) $(CXXFLAGS) $(OBJECT_NO_SYSCALL) -o stockast-no-syscall


.PHONY: clean

clean:
			rm -f *.o stockast stockast-no-syscall
