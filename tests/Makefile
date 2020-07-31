#test for Raft_C
SRC_DIR := src
BIN_DIR := bin

EXE := $(BIN_DIR)/raft_tests
SRC := $(wildcard $(SRC_DIR)/*.c)

CPPFLAGS := -I /home/ubuntu/raft_C/include -I /usr/include -MMD -MP
CFLAGS := -Wall
LDFLAGS := -Llib
LDLIBS := -lm -luv

.PHONY: all clean

all: $(EXE)

$(EXE): $(BIN_DIR)
	$(CC) $(LDFLAGS) $^ $(LDLIBS) -o $@



$(BIN_DIR):
	mkdir -p $@

clean:
	@$(RM) -rv $(BIN_DIR)