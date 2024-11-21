# Bazel Python-Go Monorepo

This repository is a monorepo containing Python and Go projects, managed using Bazel. It provides seamless build and execution capabilities for both languages, leveraging the power of [Bazelisk](https://github.com/bazelbuild/bazelisk) for efficient and consistent builds.

## Prerequisites

Before running any commands, ensure the following tools are installed:

1. **Bazelisk**  
   Bazelisk is a user-friendly launcher for Bazel. Install it by following the [official installation guide](https://github.com/bazelbuild/bazelisk?tab=readme-ov-file#installation).  

## Directory Structure

```plaintext
.
├── projects/
│   ├── python_server/       # Python server project
│   └── go_server/           # Go server project
├── WORKSPACE                # Bazel workspace file
└── BUILD                    # Build rules
```

## Usage

### Run the Python Server

To run the Python server, use the following command:

```
bazelisk run //projects/python_server:python_server_bin
```

### Run the Go Server

To run the Go server, execute:

```
bazelisk run //projects/go_server:go_server
```

### Run Gazelle

To regenerate Bazel build files for the repository:

```
bazelisk run //:gazelle
```
