# Advent of Code 2022

# Start

## For each new day:

1. Make a copy of days/template.rs, name it days/dayX.rs, and run a find/replace inside it to replace `NUM` with X.
2. Add it to days/mod.rs.
3. Add a call to run your new day by adding `day!(X);` to the bottom of main.
4. Use [cargo-aoc](https://github.com/gobanos/cargo-aoc] to download the input.

## Features:

-   Once a solution to a part is known, it can be added like so: `day!(X, part1_answer, part2_answer)`. This will verify that your code continues to return the correct values.
-   Running in debug mode will use the `dhat` crate to profile your memory allocations. See its documentation for more details.
-   Specifying no command line arguments will run each day once.
-   Specifying a space-separated list of numbers, or the letter `a` (for "all"), will benchmark the given days with criterion.

## Notes:

I specifically chose to read input files at runtime instead of compile-time (using something like include_bytes!) in order to obtain more "fair" performance characteristics when comparing against other implementations and languages. If the compiler had access to the inputs there is the possibility that it would perform additional optimizations, essentially solving part (or all) of the problem at compile-time.

This project was setup using [smmalis37/aoc_template](https://github.com/smmalis37/aoc_template).
