# Yoriito Tutorial Application

A tutorial for running the Yoriito reference application, including the PAL, HeadlessApp, and Flutter UI.

<img width="1113" height="583" alt="Dummy" src="https://github.com/user-attachments/assets/7e684c74-d9a4-477b-89fc-f4a25e829cff" />


## Components

- `ref_pal`  
  Reference PAL (Platform Abstraction Layer) implementation.

- `ref_app`  
  Reference HeadlessApp demonstrating the core functionality.

- `ref_ui`  
  Reference user interface built with Flutter.

---
## Getting Started

Run the components in this order:

1. PAL (`ref_pal`)
2. HeadlessApp (`ref_app`)
3. UI (`ref_ui`)

# How to Run

## Prerequisites

Install the following before starting:

- Git
- Node.js 20+
- Docker Desktop
- Python 3.11+ *(if required)*

Check that they are installed:
```bash
git --version
node --version
docker --version
```

## Run on WSL

All components run on WSL.

### 1) Run the PAL

```bash
cd /work/yoriito-tutorial/ref_pal
npm install
./init_pal.sh
npx electron . --no-sandbox
```

---

### 2) Run the HeadlessApp

Open a new WSL terminal and run:

```bash
cd /work/yoriito-tutorial/ref_app
cmake -S . -B build
cmake --build build -j
./build/ref_app
```
