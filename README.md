# Outline

## Motivation

Much of modern software uses domain sockets for same-machine IPC. Such as PostGres, HyPer etc.

But how good are Domain sockets really?

## Comparison of IPC Methods

Compare:
1. Domain Sockets
2. TCP Sockets
3. Shared Memory
4. FIFOs

Shared memory is the way to go, so how do we use it?

## Basic Idea

Overwrite syscalls and redirect reads and writes to custom shared memory channels. LD_PRELOAD, no re-compilation!

## Communication Model

Two channels, circular read/write buffers

escalation levels

## Results

PostGres, Hyper

## Isn't all of this obvious?

## Problems we had

select/poll, keys, multi-process synchronization

## Outlook

RDMA (Alex)
