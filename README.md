# push_swap

A stack-based sorting program developed as part of the 42 curriculum.
`push_swap` is a sorting program that works with two stacks and a limited set of allowed operations.

It was a good way to build solid foundations in algorithmic thinking, data structure manipulation and optimization under strict constraints in C.

## Features
- Sorting with two stacks: `a` and `b`
- Restricted instruction set for stack manipulation
- Small-input specialized sorting logic
- Radix-sort-based strategy for larger inputs
- Integrated local `libft`

## Project structure
- `inc/push_swap.h` — main header file and stack structure definition
- `src/push_swap.c` — argument validation and program entry point
- `src/push.c` — push operations between stacks
- `src/swap.c` — swap operations
- `src/rotate.c` — rotate and reverse rotate operations
- `src/sort.c` — sorting logic for small stack sizes
- `src/radix_sort.c` — radix-sort-based strategy for larger inputs
- `src/stack_utils.c` — stack initialization and management helpers
- `src/utils.c` — parsing and utility helpers
- `libft/` — local library used by the project
- `Makefile` — builds the `push_swap` executable

## Mandatory part
The mandatory part focuses on the sorting logic required to sort the input with the allowed stack operations.

### Program
- `push_swap` — takes a list of integers as arguments, computes a valid sorting sequence and prints the required operations to standard output

### Core behavior
- validates input arguments
- rejects invalid values and duplicates
- initializes stack `a` from the input
- uses stack `b` as auxiliary storage
- prints only the operations needed to sort the values in ascending order

### Allowed operations
- `sa` — swaps the first two elements of stack `a`
- `sb` — swaps the first two elements of stack `b`
- `ss` — performs `sa` and `sb` at the same time
- `pa` — pushes the top element of `b` onto `a`
- `pb` — pushes the top element of `a` onto `b`
- `ra` — rotates stack `a` upward
- `rb` — rotates stack `b` upward
- `rr` — performs `ra` and `rb` at the same time
- `rra` — reverse rotates stack `a`
- `rrb` — reverse rotates stack `b`
- `rrr` — performs `rra` and `rrb` at the same time

### Sorting approach
- dedicated logic for very small inputs
- custom handling for 2, 3, 4 and 5 numbers
- radix-sort-based approach for larger inputs after index normalization

## Build
Build the project:

```bash
make
```

Clean object files:

```bash
make clean
```

Remove object files and executable:

```bash
make fclean
```

Rebuild everything:

```bash
make re
```

## Usage
Example:

```bash
./push_swap 2 1 3 6 5 8
```

The program prints the sequence of operations needed to sort the input.

## Learning outcomes
This project was my first real introduction to constrained algorithm design in C.
It helped build solid foundations in:
- stack-based data manipulation
- algorithmic complexity awareness
- input validation and error handling
- operation-driven sorting logic
- normalization strategies for sorting
- performance-oriented problem solving
