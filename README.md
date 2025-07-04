# Blender Node Group Collection

Collection of node groups (for shader or geometry nodes)

## List of node groups (Table of Contents)
- [:pushpin: ClampVector (for shader)](#pushpin-clampvector-for-shader)
  - [Implementation](#implementation)
- [:pushpin: PointRate (for geometry nodes)](#pushpin-pointrate-for-geometry-nodes)
  - [Implementation](#implementation-1)
- [:pushpin: ToInstance (for geometry nodes)](#pushpin-toinstance-for-geometry-nodes)
  - [Implementation](#implementation-2)
- [:pushpin: Vertex Color Alpha (for shader)](#pushpin-vertex-color-alpha-for-shader)
  - [Implementation](#implementation-3)
- [:pushpin: Unlit Shader (for shader)](#pushpin-unlit-shader-for-shader)
  - [Implementation](#implementation-4)

## Install

- Install [Node Presets](https://extensions.blender.org/add-ons/node-presets/) addon from blender extension.
- Put `xxx.blend` file into your directory of Node Presets.
- You can now add my utility nodes by "Node > Add > Template > XXX".

## Usage

### :pushpin: ClampVector (for shader)

![docs/screenshot_clampvector.png](docs/screenshot_clampvector.png)

Clamps vector by min / max.

#### Implementation

![docs/clampvector/implementation.png](docs/clampvector/implementation.png)

### :pushpin: PointRate (for geometry nodes)

Get rate of point (ID / count) from mesh or curve

(always returns 0.0 to 1.0 on each points, in order by ID)

![docs/pointrate/example.png](docs/pointrate/example.png)

![docs/pointrate/node.png](docs/pointrate/node.png)

#### Implementation

![docs/pointrate/implementation.png](docs/pointrate/implementation.png)

### Side note

- to detect of mesh or curves, used reference: https://blender.stackexchange.com/questions/305209/geometry-nodes-how-to-check-object-type

### :pushpin: ToInstance (for geometry nodes)

**DEPRECATED**: use [Geometry to Instance](https://docs.blender.org/manual/en/latest/modeling/geometry_nodes/geometry/geometry_to_instance.html) node instead.

![docs/toinstance/screenshot.png](docs/toinstance/screenshot.png)

![docs/toinstance/example.png](docs/toinstance/example.png)

![docs/toinstance/node.png](docs/toinstance/node.png)

Make geometry into single instance. This is useful when creating instance collection for `Pick Instance` on `Instance On Points`. (For detail, see the movie below.)

https://www.youtube.com/watch?v=nReSOasTuYs

#### Implementation

![docs/toinstance/implementation.png](docs/toinstance/implementation.png)

### :pushpin: Vertex Color Alpha (for shader)

Vertex Color Unlit shader (kind of like a grease pencil). This is useful in combination with [GP to Colored Curves](https://github.com/funatsufumiya/GP_to_colored_curves) mesh.

![docs/vertexcoloralpha/example.png](docs/vertexcoloralpha/example.png)

![docs/vertexcoloralpha/node.png](docs/vertexcoloralpha/node.png)

#### Implementation

![docs/vertexcoloralpha/implementation.png](docs/vertexcoloralpha/implementation.png)

### :pushpin: Unlit Shader (for shader)

Unlit shader with alpha. (This is minimalist version of Vertex Color Alpha. Probably useful for Toon shading with alpha.)

![docs/unlitshader/example.png](docs/unlitshader/example.png)

![docs/unlitshader/node.png](docs/unlitshader/node.png)

#### Implementation

![docs/unlitshader/implementation.png](docs/unlitshader/implementation.png)

## License

WTFPL
