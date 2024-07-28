# Multi Ligands Docking with AutoDock Vina

This repository provides standalone executables for preparing ligands and performing multi-ligand docking using AutoDock Vina.

## Contents

- **`obabel_prep_ligands`**: Executable for preparing ligands.
- **`vina_dock_multi_ligands`**: Executable for docking ligands with AutoDock Vina.
- **`config.txt`**: Sample configuration file for docking.
- **`README.md`**: This file, providing instructions on how to use the executables.

## Instructions

### 1. Ligand Preparation

**Using `obabel_prep_ligands`**

1. **Setup:**
   - Ensure the executable `obabel_prep_ligands` and your ligand file are in the same folder.
   - For ligand preparation from a single file:
     - Place your SDF file (e.g., `raw_ligand.sdf`) in the same folder.
   - For ligand preparation from multiple files:
     - Place all ligand files (e.g., `.mol2`, `.pdb`, `.sdf`) in a folder.

2. **Run the Executable:**
   - Open a terminal or command prompt in the folder containing `obabel_prep_ligands`.
   - Execute the file:
     - On Windows:
       ```bash
       obabel_prep_ligands.exe
       ```
     - On macOS/Linux:
       ```bash
       ./obabel_prep_ligands
       ```

3. **Follow the Prompts:**
   - For a single file, enter the name of your ligand file when prompted.
   - For multiple files, specify the folder containing your ligand files.

4. **Output:**
   - The prepared ligands will be saved in a folder named `prepared_ligands`.

### 2. Docking Ligands

**Using `vina_dock_multi_ligands`**

1. **Setup:**
   - Ensure the executable `vina_dock_multi_ligands`, your prepared ligands, receptor file (`protein.pdbqt`), and `config.txt` are in the same folder.

2. **Run the Executable:**
   - Open a terminal or command prompt in the folder containing `vina_dock_multi_ligands`.
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
   - Enter the path to the folder containing your prepared ligands when prompted.

4. **Output:**
   - The docking results will be saved in a folder named `docking_results`.

## Requirements

- **Operating System**: The executables are compatible with Windows, macOS, and Linux.
- **Dependencies**: The executables are standalone and do not require additional dependencies.

## Support

For issues or support, please contact [onahemma111@gmail.com].

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
