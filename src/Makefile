PROGRAM := winnfsd.exe
SRCS := conv.cpp DatagramSocket.cpp FileTable.cpp FileTree.cpp MountProg.cpp NFS3Prog.cpp NFSProg.cpp PortmapProg.cpp RPCProg.cpp RPCServer.cpp ServerSocket.cpp Socket.cpp SocketStream.cpp winnfsd.cpp
OBJS = $(subst .cpp,.o,$(SRCS))

RM  := rm
CC=g++
CXX=g++

CPPFLAGS:=-Ofast -std=c++11 -D_WIN32_WINNT=0x600
LDFLAGS:=-s -mconsole
LIBS:=-lws2_32 -lshlwapi

$(PROGRAM): $(OBJS)
	$(LINK.o) $^ -o $@ $(LIBS)

.PHONY: clean

clean:
	$(RM) $(OBJS) $(PROGRAM)
