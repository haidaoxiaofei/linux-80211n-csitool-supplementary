all: print_packets get_first_bfee parse_log log_to_file nl_bf_to_eff

KERNEL = $(strip $(shell uname -r))
KERNEL_INCLUDE = -I /usr/src/linux-headers-$(KERNEL)/include
CFLAGS = -Wall -Werror $(KERNEL_INCLUDE) -lm
CC = gcc

log_to_file: log_to_file.c

nl_bf_to_eff: nl_bf_to_eff.c bf_to_eff.o iwl_nl.o util.o q_approx.o

clean:
	rm -f get_first_bfee log_to_file print_packets parse_log
