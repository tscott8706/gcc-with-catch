CPP_FILES := $(wildcard src/*.cpp)
OBJ_FILES := $(addprefix obj/,$(notdir $(CPP_FILES:.cpp=.o)))
LD_FLAGS :=
CC_FLAGS :=

all: out

out: $(OBJ_FILES)
	g++ $(LD_FLAGS) -o $@ $^

clean:
	rm -f obj/* out

obj/%.o: src/%.cpp
	g++ $(CC_FLAGS) -c -o $@ $<
