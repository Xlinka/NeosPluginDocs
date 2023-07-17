# MeshX_Extensions Documentation

The `MeshX_Extensions` class provides extension methods for the `BaseX.MeshX` class, offering additional functionality for adding and manipulating triangles, connecting triangle fans, setting quads as triangles, and working with point clouds.

## Class: MeshX_Extensions

Provides extension methods for the `BaseX.MeshX` class.

### Method: AddQuadAsTriangles

```csharp
public static QuadTriangles AddQuadAsTriangles(this TriangleSubmesh triangles, Vertex v0, Vertex v1, Vertex v2, Vertex v3, bool reverse = false)
public static QuadTriangles AddQuadAsTriangles(this TriangleSubmesh triangles, int v0, int v1, int v2, int v3, bool reverse = false)
```
Adds a quad as two triangles to the specified TriangleSubmesh and returns the created triangles. The quad can be specified either by vertex objects or by vertex indices.

### Method: AddQuadAsTriangles (overload)
```csharp
public static QuadTriangles AddQuadAsTriangles(this MeshX mesh, Vertex v0, Vertex v1, Vertex v2, Vertex v3, int submesh = 0, bool reverse = false)
public static QuadTriangles AddQuadAsTriangles(this MeshX mesh, int v0, int v1, int
```
Adds a quad as two triangles to the specified MeshX object and returns the created triangles. The quad can be specified either by vertex objects or by vertex indices.

### Method: SetQuadAsTriangles
```csharp
public static void SetQuadAsTriangles(this TriangleSubmesh triangles, int v0, int v1, int v2, int v3, int t0, int t1, bool reverse = false)
public static void SetQuadAsTriangles(this TriangleSubmesh triangles, Vertex v0, Vertex v1, Vertex v2, Vertex v3, int t0, int t1, bool reverse = false)
public static void SetQuadAsTriangles(this TriangleSubmesh triangles, Vertex v0, Vertex v1, Vertex v2, Vertex v3, Triangle t0, Triangle t1, bool reverse = false)
```
Sets a quad as two triangles in the specified TriangleSubmesh. The quad can be specified either by vertex objects or by vertex indices.

### Method: SetQuadAsTriangles (overload)
```csharp
public static void SetQuadAsTriangles(this MeshX mesh, int v0, int v1, int v2, int v3, int t0, int t1, bool reverse = false, int submesh = 0)
public static void SetQuadAsTriangles(this MeshX mesh, Vertex v0, Vertex v1, Vertex v2, Vertex v3, int t0, int t1, bool reverse = false, int submesh = 0)
public static void SetQuadAsTriangles(this MeshX mesh, Vertex v0, Vertex v1, Vertex v2, Vertex v3, Triangle t0, Triangle t1, bool reverse = false, int submesh =0)
```
Sets a quad as two triangles in the specified MeshX object. The quad can be specified either by vertex objects or by vertex indices.

### Method: AddTriangleFan
```csharp
public static void AddTriangleFan(this TriangleSubmesh submesh, IList<int> vertices, bool reverseOrder = false, TriangleCollection triangles = null)
public static void AddTriangleFan(this TriangleSubmesh submesh, IList<Vertex> vertices, bool reverseOrder = false, TriangleCollection triangles = null)
public static void AddTriangleFan<T>(this TriangleSubmesh submesh, IList<T> vertices, Func<T, int> getIndex, bool reverseOrder = false, TriangleCollection triangles = null)
public static void AddTriangleFan(this TriangleSubmesh submesh, IList<int> vertices, int offset, int count, bool reverseOrder = false, TriangleCollection triangles = null)
public static void AddTriangleFan(this TriangleSubmesh submesh, IList<Vertex> vertices, int offset, int count, bool reverseOrder = false, TriangleCollection triangles = null)
public static void AddTriangleFan<T>(this TriangleSubmesh submesh, IList<T> vertices, int offset, int count, Func<T, int> getIndex, bool reverseOrder = false, TriangleCollection triangles = null)
public static void AddTriangleFan(this TriangleSubmesh submesh, int vertexCount, Func<int, int> getVertexIndex, bool reverseOrder = false)
```
Adds a triangle fan to the specified TriangleSubmesh using the provided vertices. The triangle fan can be specified by vertex objects, vertex indices, or a custom index mapping function.

### Method: ConnectTriangleFan
```csharp
public static void ConnectTriangleFan(this TriangleSubmesh submesh, IList<int> vertices, Func<int> getNextTriangle, bool reverseOrder = false, TriangleCollection triangles = null)
public static void ConnectTriangleFan(this TriangleSubmesh submesh, int vertexOffset, int vertexCount, Func<int, int> getVertexIndex, Func<int> getNextTriangle, bool reverseOrder = false)
```
Connects a triangle fan in the specified TriangleSubmesh using the provided vertices and triangle index generation function. The triangle fan can be specified by vertex objects or vertex indices.

### Method: AddTriangleFan (overload)
```csharp
public static void AddTriangleFan(this MeshX mesh, IList<int> vertices, bool reverseOrder = false, int submesh = 0, TriangleCollection triangles = null)
public static void AddTriangleFan(this MeshX mesh, IList<Vertex> vertices, bool reverseOrder = false, int submesh = 0, TriangleCollection triangles = null)
public static void AddTriangleFan<T>(this MeshX mesh, IList<T> vertices, Func<T, int> getIndex, bool reverseOrder = false, int submesh = 0, TriangleCollection triangles = null)
public static void AddTriangleFan(this MeshX mesh, int vertexCount, Func<int, int> getVertexIndex, bool reverseOrder = false, int submesh = 0)
```
Adds a triangle fan to the specified MeshX object using the provided vertices. The triangle fan can be specified by vertex objects, vertex indices, or a custom index mapping function.

### Method: ConnectTriangleFan (overload)
```csharp
public static void ConnectTriangleFan(this MeshX mesh, IList<int> vertices, Func<int> getNextTriangle, bool reverseOrder = false, int submesh = 0, TriangleCollection triangles = null)
public static void ConnectTriangleFan(this MeshX mesh, int vertexOffset, int vertexCount, Func<int, int> getVertexIndex, Func<int> getNextTriangle, bool reverseOrder = false, int submesh = 0, TriangleCollection triangles = null)
```
Connects a triangle fan in the specified MeshX object using the provided vertices and triangle index generation function. The triangle fan can be specified by vertex objects or vertex indices.

### Method: SetupAsPointCloud
```csharp
public static void SetupAsPointCloud(this MeshX mesh)
```
Sets up the specified MeshX object as a point cloud, where each vertex represents a separate point.

### Method: ConvertToPointCloud
```csharp
public static void ConvertToPointCloud(this MeshX mesh)
```
Converts the specified MeshX object to a point cloud representation by removing all other submeshes and keeping only the points.

