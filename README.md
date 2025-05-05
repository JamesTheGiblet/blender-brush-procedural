# Blender Brush-Driven Procedural Modeling System

[![License](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
![Blender Version](https://img.shields.io/badge/Blender-3.x+-yellow.svg)
![Python Version](https://img.shields.io/badge/Python-3.x-brightgreen.svg)

## Overview

This Blender add-on aims to revolutionize sculpting workflows by seamlessly integrating real-time brush input with the power of procedural transformations, all within Blender. By combining the intuitive control of manual sculpting with the efficiency and flexibility of Geometry Nodes and Python scripting, this system opens up new avenues for creativity and productivity.

## Key Features

* **Real-Time Brush Tracking:** Captures detailed brush movement data (pressure, direction, velocity) with minimal latency, providing a responsive foundation for procedural effects.
* **Dynamic Procedural Deformation:** Leverages Blender's Geometry Nodes to apply non-destructive procedural modifications to the sculpted mesh, driven directly by brush input. This includes dynamic displacement and the potential for more complex deformations.
* **Intelligent Workflow Automation:** Utilizes Python scripting to automate common and repetitive sculpting tasks, such as adaptive remeshing and auto-smooth adjustments, triggered by user actions or procedural changes.
* **Topology Awareness & Error Handling:** Implements mechanisms to monitor and address potential topology issues that may arise from procedural operations, ensuring mesh integrity.
* **Customizable Brush Sensitivity:** Offers user-adjustable controls to fine-tune how brush pressure, direction, and velocity influence the intensity and nature of procedural effects.

## Project Structure

```
blender-brush-procedural/
├── .git/
├── .gitignore
├── LICENSE
├── README.md
└── addon/
    ├── __init__.py
    ├── brush_tracking/
    │   ├── __init__.py
    │   └── brush_data_handler.py
    │   └── operators.py
    │   └── ui.py
    ├── procedural_nodes/
    │   ├── __init__.py
    │   └── dynamic_displacement_node.py
    │   └── topology_management_node.py
    ├── automation/
    │   ├── __init__.py
    │   └── auto_smoother.py
    │   └── remesher.py
    ├── core/
    │   ├── __init__.py
    │   └── communication.py
    │   └── utils.py
    └── preferences.py
├── tests/          # (Optional) For unit and integration tests
│   ├── __init__.py
│   ├── test_brush_tracking.py
│   └── test_procedural_nodes.py
└── docs/           # (Optional) For more extensive documentation
    └── ...
```

* **`.git/`:** Contains Git repository information.
* **`.gitignore`:** Specifies intentionally untracked files that Git should ignore.
* **`LICENSE`:** Contains the GNU General Public License (GPL) text.
* **`README.md`:** This file, providing an overview of the project.
* **`addon/`:** The main directory containing the Blender add-on Python code.
    * **`__init__.py`:** The entry point for the Blender add-on.
    * **`brush_tracking/`:** Modules for capturing and processing brush input.
        * `__init__.py`: Initializes the package.
        * `brush_data_handler.py`: Logic for handling and analyzing brush data.
        * `operators.py`: Blender operators for starting/stopping brush tracking and related actions.
        * `ui.py`: Custom user interface elements for brush tracking settings.
    * **`procedural_nodes/`:** Definitions for custom Geometry Nodes or Python-driven node groups for procedural effects.
        * `__init__.py`: Initializes the package.
        * `dynamic_displacement_node.py`: Implementation of dynamic displacement based on brush input.
        * `topology_management_node.py`: Logic for real-time topology refinement.
    * **`automation/`:** Scripts for automating sculpting workflows.
        * `__init__.py`: Initializes the package.
        * `auto_smoother.py`: Script for automatic smooth shading adjustments.
        * `remesher.py`: Script for triggering adaptive remeshing.
    * **`core/`:** Core utility functions and communication logic.
        * `__init__.py`: Initializes the package.
        * `communication.py`: Functions for data exchange between Python and Geometry Nodes.
        * `utils.py`: General utility functions.
    * **`preferences.py`:** User-configurable preferences for the add-on.
* **`tests/`:** (Optional) Directory for unit and integration tests.
* **`docs/`:** (Optional) Directory for more extensive documentation.

## Getting Started

### Prerequisites

* **Blender:** Version 3.0 or higher (required for Geometry Nodes).
* **Python:** Blender's built-in Python interpreter will be used.
* **A graphics tablet (recommended):** For pressure and tilt sensitivity, enhancing the brush input data.

### Installation

1.  **Clone the Repository:**
    ```bash
    git clone <repository_url>
    cd blender-brush-procedural
    ```
    (Replace `<repository_url>` with the URL of your GitHub repository.)

2.  **Install as a Blender Add-on:**
    * Open Blender.
    * Go to `Edit` > `Preferences...`.
    * In the Preferences window, navigate to the `Add-ons` tab.
    * Click the `Install...` button.
    * Browse to the `addon` directory within your cloned repository and select the `__init__.py` file.
    * Enable the add-on by checking the box next to its name (it will likely appear under a category like "Sculpt" or have a name derived from your repository).

## Development

We are actively developing this exciting add-on! Contributions and feedback are welcome. Please see the `CONTRIBUTING.md` file (to be created later) for guidelines on how to contribute.

## License

This project is licensed under the **GNU General Public License v3.0** - see the [`LICENSE`](./LICENSE) file for details.

## Future Enhancements

We have ambitious plans for the future of this add-on, including:

* Refining brush-driven input sensitivity for even greater sculpting accuracy.
* Enhancing adaptive topology remeshing algorithms for improved procedural surface detail.
* Exploring the integration of machine learning techniques for intelligent stroke prediction and more intuitive sculpting workflows.
* Expanding the range of procedural effects that can be driven by brush input.
* Developing a user-friendly interface for managing brush settings and procedural parameters.

## Support

For bug reports, feature requests, or general questions, please [create an issue](https://github.com/JamesTheGiblet/blender-brush-procedural/issues) on this GitHub repository.
