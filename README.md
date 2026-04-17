# PES VCS - A Git-like Version Control System in C

## Student Information
Name: SHRIYA K 
USN: pes1ug24cs448  
Course: OS LAB

---

# Project Summary

This project implements a simplified version control system inspired by Git.  
It demonstrates how modern VCS tools work internally by building:

- Content-addressable object storage
- Tree-based directory snapshots
- Staging area (index)
- Commit history with parent linking

The system stores snapshots efficiently instead of storing file differences.

---

# Core Design Philosophy

The system is built on four core concepts:

1. Objects are stored using SHA-256 hashing  
2. Files are stored as blobs  
3. Directories are stored as tree objects  
4. Commits point to complete snapshots (trees)

This ensures immutability, deduplication, and integrity.

---

# Repository Structure


pes1ug24cs448-pes-vcs/
├── object.c
├── tree.c
├── index.c
├── commit.c
├── pes.c
├── Makefile
├── screenshots/
└── README.md


---

# Implementation Phases

## Phase 1 - Object Storage System
- Implemented SHA-256 based object hashing
- Stored file contents as immutable blobs
- Verified integrity using hash matching

## Phase 2 - Tree Construction
- Built recursive directory tree structure
- Supported nested file paths
- Generated deterministic tree objects

## Phase 3 - Index (Staging Area)
- Implemented staging system for files
- Tracked file metadata and changes
- Enabled `pes status` functionality

## Phase 4 - Commits and History
- Implemented commit creation
- Linked commits using parent pointers
- Maintained full history using HEAD reference

---

# Key Features

- Content-addressable storage system
- Deduplicated file storage
- Tree-based snapshot system
- Staging area (index)
- Persistent commit history
- SHA-based integrity verification

---


