# Multi Ligands Docking with AutoDock Vina

### This repository provides standalone executables (`obabel_prep_ligands.exe` and `vina_dock_multi_ligands.exe`) for preparing ligands and performing multi-ligand docking using AutoDock Vina.

# Instructions

## To use the executables, Download from the [Releases page](https://github.com/OnahPmi/Multiple-Ligand-Docking-with-Vina/releases/tag/v1.0.0).

### 1. Ligand Preparation

**Using the `obabel_prep_ligands.exe` executable**

1. **Setup:**
   - Ensure that Open Babel is installed and added to your system path variables.
   - Ensure the executable `obabel_prep_ligands` and your ligand file are in the same folder or add the directory of the executable to your system path variables.
   - For ligand preparation from a single file:
     - Place your SDF file (e.g., `raw_ligand.sdf`) in the same folder as the executable.
   - For ligand preparation from multiple files:
     - Place all ligand files (e.g., `.mol2`, `.pdb`, `.sdf`) in a folder (e.g. `raw_ligands` folder) and place the folder in the same directory as the executable.

3. **Run the Executable:**
   - Open a terminal or command prompt in the folder containing the ligand files or ligands folder.
   - Run the following command:'
     - On Windows:
       ```bash
       obabel_prep_ligands.exe
       ```
     - On macOS/Linux:
       ```bash
       ./obabel_prep_ligands
       ```
       
4. **Follow the Prompts:**
   - For the question "Are your ligands contained in a single file [y/n]?", type `y` if the contained in a single file or `n` if not.
   - For a single file, enter the name of your ligand file when prompted. E.g., `raw_ligand.sdf`
   - For multiple files, specify the folder containing your ligand files. E.g., `raw_ligands`

5. **Completion**:
   - Once the conversion is complete, a new folder named `prepared_ligands` will be created.
   - This folder will contain the prepared ligands in PDBQT format.

### Notes
- Verify that both `obabel_prep_ligands` and `raw_ligand.sdf` are in the same directory for the executable to work correctly.

### 2. Docking Ligands

**Using the `vina_dock_multi_ligands.exe` executable**

1. **Setup:**
   - Ensure that AutoDock Vina is installed and added to your system path variables.
   - Ensure that the `receptor name`, `binding pocket coordinates and sizes`, `exhaustiveness`, etc., are contained in the `config.txt` file.
   - Place the `vina_dock_multi_ligands` executable, the prepared protein (e.g. `protein.pdbqt`), `config.txt` file, and the `prepared_ligands` folder in the same directory.
   - Alternatively, add the directory of the executable to your system path variables to be able to run it from any folder without placing it in the folder.

2. **Run the Executable:**
   - Open a terminal or command prompt in the folder containing the `prepared proteins`, `prepared ligands` and `config.txt file`.
   - Execute the file:
     - On Windows:
       ```bash
       vina_dock_multi_ligands.exe
       ```
     - On macOS/Linux:
       ```bash
       ./vina_dock_multi_ligands
       ```

3. **Follow the Prompts:**
    - For the question "Input path to ligands directory:", type the name of the prepared ligands folder (e.g., `prepared_ligands`) and hit enter.

4. **Completion:**
   - Once the docking is complete, a new folder named `docking_results` will be created.
   - This folder will contain the docking results and the log files.

### Notes
- Verify that `vina_dock_multi_ligands`, the prepared protein (`protein.pdbqt`), `config.txt` file, and the `prepared_ligands` folder are in the same directory for the executable to work correctly.

## Requirements

- **Operating System**: The executables are compatible with Windows, macOS, and Linux.
- **Dependencies**: The executables are standalone and do not require additional dependencies.

## Support

For issues or support, please contact [onahemma111@gmail.com].

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
