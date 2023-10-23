# Multi-Level Feedback Queue (MLFQ) with Round Robin Scheduling

## Overview
The `mlfq.c` file is an implementation of a Multi-Level Feedback Queue (MLFQ) scheduling algorithm with round-robin scheduling. This program reads a set of instructions from an input file and simulates the scheduling of tasks among multiple queues with varying priorities.

## Table of Contents
- [Introduction](#introduction)
- [Usage](#usage)
- [Implementation Details](#implementation-details)
- [Compiling the Code](#compiling-the-code)
- [Running the Program](#running-the-program)
- [Sample Input File](#sample-input-file)
- [Sample Output](#sample-output)

## Introduction
The Multi-Level Feedback Queue (MLFQ) is a popular scheduling algorithm that divides tasks into multiple priority queues. Each queue has a different priority level, and tasks move between queues based on their behavior. In this implementation, we use three priority queues with different time quantum values for each queue.

## Usage
To use this program, follow these steps:

1. **Compile the Code**: Compile the `mlfq.c` code to create an executable.
2. **Create an Input File**: Prepare an input file containing a list of instructions for task scheduling.
3. **Run the Program**: Execute the compiled program with the input file as an argument.
4. **View Output**: The program will display the scheduling actions and the status of tasks at each clock tick.

## Implementation Details
- The program simulates task scheduling based on the instructions in the input file.
- Tasks are categorized into three priority queues (queues 1, 2, and 3), with decreasing priority.
- The time quantum for each queue is defined by the `QUEUE_TIME_QUANTUMS` array.
- A boost operation is performed periodically to move tasks from lower-priority queues to higher-priority queues.
- The program tracks waiting time and execution time for each task to calculate turnaround time.
- The scheduler selects the task with the highest priority for execution.
- The code handles task arrivals, terminations, and bursts, updating task information accordingly.

## Compiling the Code
Compile the `mlfq.c` code using a C compiler (e.g., GCC) with the following command:
```shell
gcc -o mlfq mlfq.c
