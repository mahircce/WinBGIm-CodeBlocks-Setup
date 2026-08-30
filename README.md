# WinBGIm (graphics.h) Setup in Code::Blocks

A complete guide and required files to set up the `graphics.h` library in Code::Blocks using the 32-bit TDM-GCC compiler for Computer Animation &;Graphics lab projects.

## 🚀 Setup Instructions

### Step 1: Install TDM-GCC Compiler
1. Download the MinGW.org based [TDM-GCC 10.3.0 (32-bit)](https://jmeubank.github.io/tdm-gcc/articles/2021-05/10.3.0-release).
2. Install it in the default directory: `C:\TDM-GCC-32`.
3. Make sure to uncheck the "update" option during installation.

### Step 2: Place Library Files
Download the required WinBGIm files and place them carefully:
* Copy `graphics.h` & `winbgim.h` ➔ Paste into `C:\TDM-GCC-32\include`
* Copy `libbgi.a` ➔ Paste into `C:\TDM-GCC-32\lib`

### Step 3: Configure Code::Blocks Compiler
1. Open Code::Blocks.
2. Go to **Settings > Compiler > Toolchain executables**.
3. Set the "Compiler's installation directory" to `C:\TDM-GCC-32`.

### Step 4: Configure Linker Settings
1. Go to **Settings > Compiler > Linker settings**.
2. Under *Link libraries*, click 'Add' and select the `libbgi.a` file.
3. Under *Other linker options*, paste the following parameters exactly:
   ```text
   -lbgi -lgdi32 -lcomdlg32 -luuid -loleaut32 -lole32
