 Mini Database Engine in C++

A lightweight, file-based database engine built from scratch in C++, implementing core DBMS concepts such as indexing, query execution, storage management, and record retrieval.

Features:

Custom Storage Engine — Stores records in binary files with fixed/variable-length serialization.
B+ Tree Indexing — Fast O(log n) search and range queries for large datasets.
Query Processor — Supports simple commands:

INSERT <record>
SELECT * / SELECT <key>
DELETE <key>

Buffer Management — Minimizes disk access by caching recently accessed pages.
Record Management — Handles insertion, lookup, deletion, and scanning.
Modular Architecture — Separated components for storage, indexing, parser, and executor.


Tech Stack:

C++17
File I/O for persistence
Object-oriented architecture
STL for memory-safe containers


Project Structure:
/src
  ├── storage/       # file manager, page system
  ├── index/         # B+ tree implementation
  ├── parser/        # command parser
  ├── executor/      # query executor
  └── main.cpp       # CLI interface


Sample Commands:
INSERT 101 "Alice" 22
INSERT 102 "Bob" 24
SELECT *
SELECT 101
DELETE 102


Learning Outcomes

Understood how databases manage data on disk
Implemented indexing + balanced trees
Built a functional query execution pipeline
Applied low-level systems programming principles


Future Enhancements

WAL (Write Ahead Logging)
Concurrency control (locking)
SQL-like query language
Cost-based query optimizer
