# FS_Recovery_Lab
FS Recovery Lab is a browser-based file system simulation web app built with HTML, CSS, and JavaScript. It visualizes disk blocks, file allocation, free-space management, deletion, crash simulation, file recovery, defragmentation, logs, and disk health analysis.

## Web Application URL
https://fs-recovery-lab.netlify.app/

## Project Overview

This project is designed as a simulation tool for understanding basic file system management concepts in Operating Systems. It does not recover real files from a computer. Instead, it creates a virtual disk environment where users can create files, delete files, simulate disk crashes, recover deleted files, and optimize disk space.

The main aim of this project is to visually explain how file systems work internally and how recovery and optimization tools can restore or improve disk structure after errors or fragmentation.

## Features

- Virtual disk block visualization
- File creation with custom file name and size
- File deletion simulation
- Free-space management representation
- Directory structure display
- Contiguous allocation simulation
- Linked allocation simulation
- Indexed allocation simulation
- Disk crash simulation
- File recovery system
- Disk optimization and defragmentation
- Corrupted block detection
- Disk health score calculation
- Operation logs
- Recovery report generation
- Responsive and modern user interface

## How It Works

The web app creates a virtual disk made up of multiple blocks. Each block can have a different status such as free, used, fragmented, deleted, corrupted, or recovered.

When a file is created, the simulator assigns disk blocks to that file using the selected allocation method. The user can choose between contiguous, linked, and indexed allocation.

When a file is deleted, its blocks are not immediately removed permanently. Instead, they are marked as deleted and recoverable. This simulates how real file systems often mark space as available instead of instantly erasing all data.

When a disk crash is simulated, some active file blocks become corrupted. These corrupted blocks represent damaged data or bad sectors.

During recovery, the simulator scans the virtual disk and attempts to restore deleted files if their blocks have not been corrupted. Recovered files are moved to a recovered folder.

During optimization, the simulator compacts active files, reduces fragmentation, organizes used blocks together, and isolates corrupted blocks.

## File Allocation Methods Used

### 1. Contiguous Allocation

In contiguous allocation, a file is stored in continuous disk blocks. This makes file access faster, but it can fail if there is not enough continuous free space.

### 2. Linked Allocation

In linked allocation, file blocks can be stored anywhere on the disk and are connected logically. This reduces external fragmentation but can make direct access slower.

### 3. Indexed Allocation

In indexed allocation, file block addresses are managed through an index-like structure. This allows flexible file storage and better random access compared to linked allocation.

## Disk Block Status

The simulator uses different block states:

- **Free**: Available block
- **Used**: Block currently used by a file
- **Fragmented**: File block stored non-contiguously
- **Deleted**: Deleted but recoverable block
- **Corrupted**: Damaged or bad block
- **Recovered**: Successfully restored block

## Tech Stack

- **HTML**: Structure of the web app
- **CSS**: Styling, layout, animations, and responsive design
- **JavaScript**: Simulation logic, file operations, recovery system, optimization, and dynamic UI updates

## How to Run the Project

1. Download or clone this repository.

```bash
git clone https://github.com/your-username/fs-recovery-optimizer.git
