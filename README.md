# Axis Calculator PM

A powerful **matrix multiplication tool** for [The Foundry's Nuke](https://www.foundry.com/products/nuke-family/nuke) that enables combining and manipulating transformation matrices from Axis nodes.

Inspired by the work of **Masahiro Teraoka**.

---

## Overview

Axis Calculator PM allows you to multiply 4×4 transformation matrices from multiple Axis nodes in Nuke, enabling complex 3D transformations to be combined, inverted, or manipulated with precision. This is particularly useful for:

- Combining multiple Axis transformations into a single result
- Creating inverse transformations for camera rigs and projections
- Chaining and baking complex transformation hierarchies
- Re-parenting 3D objects while preserving world-space position

## Installation

### Method 1: Copy to .nuke folder

1. Download `Axis_Calculator_PM_231024.tcl`
2. Place the file in your `.nuke` folder:
   - **Linux:** `~/.nuke/`
   - **macOS:** `~/.nuke/`
   - **Windows:** `C:\Users\<username>\.nuke\`
3. Add the following line to your `init.py` or `menu.py`:
   ```python
   nuke.load("Axis_Calculator_PM_231024.tcl")
   ```

### Method 2: Direct import

Copy and paste the contents of `Axis_Calculator_PM_231024.tcl` directly into Nuke's Script Editor, or import the example script `Axis_Calculator_script.nk` to see it in action.

## Usage

1. Create or import Axis nodes with your desired transformations
2. Connect them to the Axis Calculator inputs
3. The tool will compute the matrix multiplication result
4. Use the output for your 3D pipeline needs

## Files

| File | Description |
|------|-------------|
| `Axis_Calculator_PM_231024.tcl` | The main TCL gizmo/tool definition |
| `Axis_Calculator_script.nk` | Example Nuke script demonstrating usage |
| `LICENSE.txt` | MIT License |

## Requirements

- **Nuke 11.0** or later (compatible with Nuke 12.x, 13.x, 14.x, 15.x)
- No external dependencies

## How It Works

In Nuke's 3D system, each Axis node contains a 4×4 transformation matrix that represents translation, rotation, scale, and skew. When you parent one Axis to another, Nuke multiplies their matrices to compute the world-space transformation.

Axis Calculator PM exposes this matrix multiplication explicitly, giving you control over how transformations are combined. This is especially useful when you need to:

- Extract the relative transformation between two objects
- Compute the inverse of a complex transformation chain
- Bake animation from a hierarchy into a single Axis

## Credits

- **Author:** Peter Mercell
- **Inspiration:** Masahiro Teraoka
- **Website:** [petermercell.com](https://www.petermercell.com)

## License

This project is licensed under the **MIT License** – see the [LICENSE.txt](LICENSE.txt) file for details.

---

## Related Resources

- [Nukepedia](https://www.nukepedia.com) – Community repository for Nuke tools
- [Nuke Python Math Module](https://www.nukepedia.com/written-tutorials/using-the-nukemath-python-module-to-do-vector-and-matrix-operations/) – Tutorial on nuke.math for matrix operations
- [Nuke Vector Matrix Toolset](https://github.com/mapoga/nuke-vector-matrix) – Comprehensive vector and matrix tools by Mathieu Goulet-Aubin & Erwan Leroy

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to open an issue or submit a pull request.
