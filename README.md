# Yoriito Tutorial Application

A tutorial for running the Yoriito reference application, including the PAL, HeadlessApp, and Flutter UI.

<img width="1048" height="358" alt="yoriito-tutorial" src="https://github.com/user-attachments/assets/2fd028b4-e845-47f8-86bc-aec019d70c9a" />


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

### 1) Run the PAL on the PC

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

---

### 3) Run the UI

Open a new WSL terminal and run:

```bash
cd /work/yoriito-tutorial/ref_ui
flutter clean
flutter pub get
flutter run -d linux
```

## Run on Yocto

> `ref_pal` does not support Raspberry Pi directly. Run `ref_pal` on your PC first, then connect it to a target device such as a Raspberry Pi.
### 1) Run the PAL on the PC

```bash
cd /work/yoriito-tutorial/ref_pal
npm install
./init_pal.sh
npx electron . --no-sandbox
```
