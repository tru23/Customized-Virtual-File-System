

# Customized Virtual File System

## Project Overview

The Customized Virtual File System (CVFS) is a file management system that emulates the functionalities of a traditional file system. 
It allows users to perform various file operations such as creating, reading, writing, opening, closing, and deleting files. Additionally,
it provides mechanisms to manipulate and retrieve file metadata and content. This project is designed to help users understand the basic operations 
of a file system in an educational context.

## Key Features

- **File Operations**:
  - Create: Allows the creation of new regular files with specified permissions.
  - Open: Opens an existing file in a specified mode (read, write, or read/write).
  - Close: Closes an open file by its name or file descriptor.
  - Close All: Closes all open files.
  - Read: Reads data from a file into a buffer.
  - Write: Writes data from a buffer into a file.
  - Delete (rm): Deletes a file by its name.
  - Truncate: Removes all data from a file without deleting the file itself.

- **Metadata Operations**:
  - stat: Displays metadata information about a file by its name.
  - fstat: Displays metadata information about a file by its file descriptor.
  - ls: Lists all files along with their inode numbers, sizes, and link counts.

- **File Positioning**:
  - lseek: Changes the read/write offset of an open file based on a specified position (start, current, or end).

- **User Assistance**:
  - man: Provides a manual for various commands describing their usage and functionality.
  - help: Displays a list of available commands and their descriptions.

## Technology Used

- **Programming Language**: C
- **User Interface**: Command Line Interface (CLI)
- **Platform Required**: Linux-based operating system (e.g., Ubuntu, Kali Linux), Windows

## Hardware Requirements

- Minimum 4GB RAM
- Minimum 2GHz dual-core processor
- 100MB free disk space for development environment and project files

## Project Initialization

1. **CreateDILB**: Dynamically allocates inodes and links them in a linked list.
2. **InitialiseSuperBlock**: Initializes the superblock and UFDT array.

## Error Handling

The system provides comprehensive error messages for various failure cases, such as invalid parameters, file not found, insufficient permissions, and more.

## Data Structures

- **Inode Structure**: Stores metadata about a file.
- **Superblock Structure**: Maintains the overall file system status.
- **File Table Structure**: Manages information about open files.
- **User File Descriptor Table (UFDT)**: Holds specific entries from the file table.

## Example Usage

- **Creating a File**: `CreateFile("filename", permission)`
- **Opening a File**: `OpenFile("filename", mode)`
- **Reading from a File**: `ReadFile(file_descriptor, buffer, size)`
- **Writing to a File**: `WriteFile(file_descriptor, buffer, size)`
- **Closing a File**: `CloseFileByFD(file_descriptor)`

## Commands

- `create`: Create a new file.
- `read`: Read data from a file.
- `write`: Write data to a file.
- `ls`: List all files.
- `stat`: Display file metadata.
- `fstat`: Display file metadata using file descriptor.
- `truncate`: Remove data from a file.
- `open`: Open an existing file.
- `close`: Close a file.
- `closeall`: Close all open files.
- `lseek`: Change the file offset.
- `rm`: Delete a file.

