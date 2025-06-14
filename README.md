# origami_files
---
## .cp
### \`.cp File Format Overview

The `.cp` file format is designed to store crease patterns, consisting of a series of line segment data. Each line segment is represented by five values: the segment type, and the coordinates of the start point (x1, y1) and end point (x2, y2). The segment type is typically mapped to a color, which can be used to represent different kinds of creases, such as valley, mountain, or auxiliary lines.

### Data Format

A typical `.cp` file consists of the following structure:

```
Segment Type x1 y1 x2 y2
Segment Type x1 y1 x2 y2
```

Each line represents one line segment, with the following details:

* **Segment Type**: This indicates the color of the line segment. The mapping is as follows:

  * Type 1: Black line segment
  * Type 2: Red line segment
  * Type 3: Blue line segment
  * Other types are used for auxiliary lines and are mapped to the following colors:

    * 0000FF: Valley lines (Blue)
    * FF0000: Mountain lines (Red)
    * 000000: Black lines
    * Gray: Auxiliary lines

* **x1, y1**: The coordinates of the start point of the line segment.

* **x2, y2**: The coordinates of the end point of the line segment.

### Purpose

The `.cp` file format is specifically used for storing crease patterns in origami or related fields, where precise control over the line segments representing different crease types (mountain, valley, or auxiliary) is required. This format can be used for creating, sharing, and processing crease patterns for folding models.

### Usage

* `.cp` files are typically used in applications or tools designed to visualize and manipulate crease patterns, especially in the context of origami design.
* These files can be processed by various tools to create visual representations of crease patterns and to manipulate the folding process.
* The format is optimized for easy conversion between different representations of crease patterns, including conversion from formats like SVG.

This format provides a flexible and effective way to store and manage crease patterns, ensuring consistency and clarity in the folding process.
---
## .fold
### \`.fold File Format Overview

The `.fold` file format is designed to store and represent origami models, particularly crease patterns, folding states, and the relationships between different parts of the model. It allows for the storage of a mesh structure consisting of vertices, edges, and faces, along with optional 2D or 3D geometry and the topological stacking order of faces.

### Data Format

A typical `.fold` file structure consists of the following elements:

```
<vertex data>
<edge data>
<face data>
<topological data>
```

Each element of the `.fold` file is explained as follows:

* **Vertices**: Points in 2D or 3D space that define the shape of the origami model.
* **Edges**: Lines that connect the vertices and define the structure of the model.
* **Faces**: Surfaces formed by the edges and vertices that make up the mesh of the model.
* **Topological Data**: Describes the stacking order of faces that overlay each other in the folded model. This data helps to understand the final 3D configuration of the origami model.

### Purpose

The `.fold` file format is used for representing origami models in a flexible and extensible manner. It can describe:

* **Crease patterns**: The layout of creases on a flat sheet of paper.
* **Mountain-valley patterns**: Indicating which creases are folded in the "mountain" or "valley" direction.
* **Folded states**: The 3D shape of the origami model after folding.

The format is highly suitable for applications that need to visualize, analyze, or simulate the process of folding and unfolding models.

### Usage

* `.fold` files are used in tools designed for visualizing and manipulating origami models.
* They can store a comprehensive description of the folding structure, including both the crease pattern and the folded state.
* The `.fold` format is also compatible with various programs that allow for the creation, modification, and simulation of origami models, offering both 2D and 3D representations.

### Conversion and Visualization

* `.fold` files can be easily converted to or from other file formats, such as SVG, for use in different tools and platforms.
* The format is also suitable for use in web-based visualizers and desktop applications, providing a way to display and interact with origami models.

This format enables a seamless integration of geometric and topological data, making it an ideal choice for anyone working with origami design or related fields.
---
# viwer
## [fold](https://edemaine.github.io/fold/examples/foldviewer.html)
## [cp](https://wiorigami.github.io/cp_viewer.github.io/)

