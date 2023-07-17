# Meshx Documentation

Meshx is a class that represents a mesh and provides methods for manipulating its vertices, triangles, and points.

## Class: BaseX

Represents a mesh and provides methods for manipulating its vertices, triangles, and points.

### Constructor: BaseX

Creates a new instance of the BaseX class.

### Properties

- `VertexCount` (int): Gets the total number of vertices in the mesh.
- `TotalTriangleCount` (int): Gets the total number of triangles in the mesh.
- `TotalPointCount` (int): Gets the total number of points in the mesh.
- `SubmeshCount` (int): Gets the number of submeshes in the mesh.
- `HasNormals` (bool): Gets a value indicating whether the mesh has vertex normals.
- `HasTangents` (bool): Gets a value indicating whether the mesh has vertex tangents.
- `HasColors` (bool): Gets a value indicating whether the mesh has vertex colors.
- `HasBoneBindings` (bool): Gets a value indicating whether the mesh has bone bindings.
- `HasFlags` (bool): Gets a value indicating whether the mesh has flags.
- `TrackRemovals` (bool): Gets or sets a value indicating whether removals should be tracked in the mesh.

### Methods

- `AddSubmesh(TopologyType topology)`: Adds a new submesh to the mesh with the specified topology type.
- `TryGetSubmesh<T>(int submeshIndex)`: Tries to get a submesh at the specified index with the specified type.
- `IncreaseVertexCount(int count)`: Increases the vertex count of the mesh by the specified amount.
- `AddVertex()`: Adds a new vertex to the mesh.
- `AddVertex(in float3 pos)`: Adds a new vertex to the mesh with the specified position.
- `AddTriangle(int submesh = 0)`: Adds a new triangle to the mesh in the specified submesh.
- `AddTriangles(int count, int submesh = 0, TriangleCollection trigs = null)`: Adds the specified number of triangles to the mesh in the specified submesh.
- `AddTriangle(int v0, int v1, int v2, int submesh = 0)`: Adds a new triangle to the mesh with the specified vertex indices and in the specified submesh.
- `AddTriangle(Vertex v0, Vertex v1, Vertex v2, int submesh = 0)`: Adds a new triangle to the mesh with the specified vertices and in the specified submesh.
- `AddPoint(int submesh)`: Adds a new point to the mesh in the specified submesh.
- `AddPoints(int count, int submesh, PointCollection points = null)`: Adds the specified number of points to the mesh in the specified submesh.
- `GetVertex(int index)`: Retrieves the vertex at the specified index.
- `GetTriangle(int index, int submesh = 0)`: Retrieves the triangle at the specified index in the specified submesh.
- `GetPoint(int index, int submesh = 0)`: Retrieves the point at the specified index in the specified submesh.
- `GetTriangleByFaceIndex(int faceIndex)`: Retrieves the triangle at the specified face index across all triangle submeshes.
- `GetTriangleFromAllTriangleSubmeshes(int triangleIndex)`: Retrieves the triangle at the specified index across all triangle submeshes.
- `RemoveVertices(int index, int count, bool updateSubmeshes = true)`: Removes the specified number of vertices starting from the specified index.

