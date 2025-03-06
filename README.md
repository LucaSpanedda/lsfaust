# lsfaust
# Automating Faust Repository customization and installation

Customizing and installing faust. The process ensures that only the corresponding files in `faust` folder are replaced before the installation, while keeping the overall structure intact.

## Steps to Customize Faust

1. **Clone the Faust repository:**
   ```bash
   git clone https://github.com/LucaSpanedda/faust.git
   ```

2. **Clone the custom repository (`lsfaust`):**
   ```bash
   git clone https://github.com/LucaSpanedda/lsfaust.git
   ```

3. **Navigate into the `faust` directory:**
   ```bash
   cd faust
   ```

4. **Copy the custom files from `lsfaust` into `faust`, preserving the directory structure:**
   ```bash
   cp -r ../lsfaust/* .
   ```

5. **(Optional) Remove the `lsfaust` directory to clean up:**
   ```bash
   rm -rf ../lsfaust
   ```

6. **Confirm that the custom files have been correctly placed:**
   ```bash
   git status
   ```

## How It Works
- The first repository (`faust`) contains the official Faust code.
- The second repository (`lsfaust`) contains only the modified files that should replace the original ones.
- The `cp -r` command ensures that the structure remains consistent while overwriting the necessary files.

## Notes
- Ensure that your `lsfaust` repository mirrors the structure of `faust`, so files are correctly replaced.
- You can add further customization by tracking your changes in a separate Git branch.

With this method, you can efficiently maintain and update a customized version of Faust while keeping it in sync with the official repository.
