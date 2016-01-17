PRODUCTNAME=danlisp

CXX=clang++
RM=rm -f
CPPFLAGS=-g -Wall -Werror -std=c++11
LDFLAGS=-g

SRCS=repl.cpp
OBJS=$(subst .cpp,.o,$(SRCS))

all: danlisp

danlisp: $(OBJS)
	$(CXX) $(LDFLAGS) -o $(PRODUCTNAME) $(OBJS)

depend: .depend

.depend: $(SRCS)
	rm -f ./.depend
	$(CXX) $(CPPFLAGS) -MM $^>>./.depend

clean:
	$(RM) $(OBJS) $(PRODUCTNAME) .depend

include .depend
