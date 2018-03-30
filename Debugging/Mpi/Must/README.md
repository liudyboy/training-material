# Must
Must is a tool to detect a number of issues in MPI code at runtime.

## What is it?
1. `buffer_overlap.f90`: send and receive buffer overlap.
1. `buffer_size.f90`: buffer size in collectives odesn't match.
1. `message_init_size.f90`: data and message type differs, undetected by
    Must.
1. ``message_size.f90`: send and receive buffer have different sizes in
    peer-to-peer communication.
1. `message_type.f90`: send and receive buffer have different types.
1. `Makefile`: make file to build the applications.

## How to use?
To build the applications, use make:
```bash
$ make
```

To run with Must:
```bash
$ mustrun -np 2 <appl>
```
Use a web browser to view the HGML report.