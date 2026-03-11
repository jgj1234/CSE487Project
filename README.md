# Usage

Create a recompression RLSLP for a given string using the directions provided in the README of fast-recompression.

To build the `recomp_query` binary, run the following command in the same directory as this README.

```bash
$ make
```

Create a file of queries where each line is in the following format.

```
type_number index length
```

Type 1 queries report all occurrences of the substring starting at index with the given length in the string (0-indexed).

Type 2 queries report the leftmost occurrence of the substring starting at index with the given length in the string (0-indexed).

Type 3 queries report the number of occurrences of the substring starting at index with the given length in the entire string.

The index passed in to each query is 0-indexed.

# Example: Running the Recompression Query Program

```
./recomp_query -i input.rlslp -qf queries.txt [-o output.txt]
```

In this execution, the program uses the Recompression RLSLP file located at `input.rlslp` and the query file located at `queries.txt`. Optionally, the `-o output.txt` flag can also be provided to specify a file where query results will be written to. If this flag is not provided, the program defaults to printing query responses to standard output.