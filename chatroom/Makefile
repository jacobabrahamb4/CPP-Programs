CXX = g++
CXXFLAGS = -std=c++20 -Wall -Wextra -g
LDFLAGS = -thread
LDLIBS = -lboost_system -lBoost_thread

SERVER_SRC = chatRoom.cpp
CLIENT_SRC = client.cpp

SERVER_OBJ = $(SERVER_SRC:.cpp=.o)
CLIENT_OBJ = $(CLIENT_SRC:.cpp=.o)

all: chatApp clientApp

chatApp: $(SERVER_OBJ)
	$(CXX) $(LDFLAGS) $(SERVER_OBJ) $(LDLIBS) -o chatApp

cleintApp: $(SERVER_OBJ)
	$(CXX) $(LDFLAGS) $(SERVER_OBJ) $(LDLIBS) -o cleintApp

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $< -o $@

clean:
	rm -f *.o chatApp clientApp