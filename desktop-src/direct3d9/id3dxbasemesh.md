---
description: Anwendungen verwenden die Methoden der ID3DXBaseMesh-Schnittstelle, um Mesh-und Progressive Mesh-Objekte zu bearbeiten und abzufragen.
ms.assetid: ec4ccd77-e370-470c-9325-3d794a8f7f16
title: ID3DXBaseMesh-Schnittstelle (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58029639852b30f5de357bb2643583615c45485c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355027"
---
# <a name="id3dxbasemesh-interface"></a><span data-ttu-id="4cc08-103">ID3DXBaseMesh-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4cc08-103">ID3DXBaseMesh interface</span></span>

<span data-ttu-id="4cc08-104">Anwendungen verwenden die Methoden der **ID3DXBaseMesh** -Schnittstelle, um Mesh-und Progressive Mesh-Objekte zu bearbeiten und abzufragen.</span><span class="sxs-lookup"><span data-stu-id="4cc08-104">Applications use the methods of the **ID3DXBaseMesh** interface to manipulate and query mesh and progressive mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="4cc08-105">Member</span><span class="sxs-lookup"><span data-stu-id="4cc08-105">Members</span></span>

<span data-ttu-id="4cc08-106">Die **ID3DXBaseMesh** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4cc08-106">The **ID3DXBaseMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4cc08-107">**ID3DXBaseMesh** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4cc08-107">**ID3DXBaseMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="4cc08-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="4cc08-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4cc08-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="4cc08-109">Methods</span></span>

<span data-ttu-id="4cc08-110">Die **ID3DXBaseMesh** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4cc08-110">The **ID3DXBaseMesh** interface has these methods.</span></span>



| <span data-ttu-id="4cc08-111">Methode</span><span class="sxs-lookup"><span data-stu-id="4cc08-111">Method</span></span>                                                                            | <span data-ttu-id="4cc08-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cc08-112">Description</span></span>                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4cc08-113">**Clonemesh**</span><span class="sxs-lookup"><span data-stu-id="4cc08-113">**CloneMesh**</span></span>](id3dxbasemesh--clonemesh.md)                                     | <span data-ttu-id="4cc08-114">Klont ein Mesh mit einem Deklarator.</span><span class="sxs-lookup"><span data-stu-id="4cc08-114">Clones a mesh using a declarator.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="4cc08-115">**Clonemeshf VF**</span><span class="sxs-lookup"><span data-stu-id="4cc08-115">**CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)                               | <span data-ttu-id="4cc08-116">Klont ein Mesh mit einem flexiblen Scheitelpunkt Formatierungs Code (FVF).</span><span class="sxs-lookup"><span data-stu-id="4cc08-116">Clones a mesh using a flexible vertex format (FVF) code.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="4cc08-117">**Convertadjackocytopointreps**</span><span class="sxs-lookup"><span data-stu-id="4cc08-117">**ConvertAdjacencyToPointReps**</span></span>](id3dxbasemesh--convertadjacencytopointreps.md) | <span data-ttu-id="4cc08-118">Konvertiert Gitter Informations Informationen in ein Array von Punkt Vertretern.</span><span class="sxs-lookup"><span data-stu-id="4cc08-118">Converts mesh adjacency information to an array of point representatives.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="4cc08-119">**Convertpointrepstoannäherency**</span><span class="sxs-lookup"><span data-stu-id="4cc08-119">**ConvertPointRepsToAdjacency**</span></span>](id3dxbasemesh--convertpointrepstoadjacency.md) | <span data-ttu-id="4cc08-120">Konvertiert Punkt repräsentative Daten in Gitter Informations Informationen.</span><span class="sxs-lookup"><span data-stu-id="4cc08-120">Converts point representative data to mesh adjacency information.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="4cc08-121">**DrawSubset**</span><span class="sxs-lookup"><span data-stu-id="4cc08-121">**DrawSubset**</span></span>](id3dxbasemesh--drawsubset.md)                                   | <span data-ttu-id="4cc08-122">Zeichnet eine Teilmenge eines Mesh.</span><span class="sxs-lookup"><span data-stu-id="4cc08-122">Draws a subset of a mesh.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="4cc08-123">**Generateency**</span><span class="sxs-lookup"><span data-stu-id="4cc08-123">**GenerateAdjacency**</span></span>](id3dxbasemesh--generateadjacency.md)                     | <span data-ttu-id="4cc08-124">Generieren Sie eine Liste mit Gitter Kanten sowie eine Liste der Flächen, die die einzelnen Kanten gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="4cc08-124">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="4cc08-125">**GetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="4cc08-125">**GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)                     | <span data-ttu-id="4cc08-126">Ruft entweder eine Attribut Tabelle für ein Mesh oder die Anzahl der in einer Attribut Tabelle gespeicherten Einträge für ein Mesh ab.</span><span class="sxs-lookup"><span data-stu-id="4cc08-126">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span><br/>                                                                                          |
| [<span data-ttu-id="4cc08-127">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="4cc08-127">**GetDeclaration**</span></span>](id3dxbasemesh--getdeclaration.md)                           | <span data-ttu-id="4cc08-128">Ruft eine Deklaration ab, die die Scheitel Punkte im Mesh beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4cc08-128">Retrieves a declaration describing the vertices in the mesh.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="4cc08-129">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="4cc08-129">**GetDevice**</span></span>](id3dxbasemesh--getdevice.md)                                     | <span data-ttu-id="4cc08-130">Ruft das dem Mesh zugeordnete Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="4cc08-130">Retrieves the device associated with the mesh.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="4cc08-131">**Getf VF**</span><span class="sxs-lookup"><span data-stu-id="4cc08-131">**GetFVF**</span></span>](id3dxbasemesh--getfvf.md)                                           | <span data-ttu-id="4cc08-132">Ruft den Scheitelpunkt Wert fester Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="4cc08-132">Gets the fixed function vertex value.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="4cc08-133">**Getindexbuffer**</span><span class="sxs-lookup"><span data-stu-id="4cc08-133">**GetIndexBuffer**</span></span>](id3dxbasemesh--getindexbuffer.md)                           | <span data-ttu-id="4cc08-134">Ruft die Daten in einem Index Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="4cc08-134">Retrieves the data in an index buffer.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="4cc08-135">**Getnumbytespervertex**</span><span class="sxs-lookup"><span data-stu-id="4cc08-135">**GetNumBytesPerVertex**</span></span>](id3dxbasemesh--getnumbytespervertex.md)               | <span data-ttu-id="4cc08-136">Ruft die Anzahl der Bytes pro Scheitelpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="4cc08-136">Gets the number of bytes per vertex.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="4cc08-137">**Getnumgesichter**</span><span class="sxs-lookup"><span data-stu-id="4cc08-137">**GetNumFaces**</span></span>](id3dxbasemesh--getnumfaces.md)                                 | <span data-ttu-id="4cc08-138">Ruft die Anzahl der Gesichter im Mesh ab.</span><span class="sxs-lookup"><span data-stu-id="4cc08-138">Retrieves the number of faces in the mesh.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="4cc08-139">**Getnumvertices**</span><span class="sxs-lookup"><span data-stu-id="4cc08-139">**GetNumVertices**</span></span>](id3dxbasemesh--getnumvertices.md)                           | <span data-ttu-id="4cc08-140">Ruft die Anzahl der Scheitel Punkte im Mesh ab.</span><span class="sxs-lookup"><span data-stu-id="4cc08-140">Retrieves the number of vertices in the mesh.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="4cc08-141">**GetOptions**</span><span class="sxs-lookup"><span data-stu-id="4cc08-141">**GetOptions**</span></span>](id3dxbasemesh--getoptions.md)                                   | <span data-ttu-id="4cc08-142">Ruft die Gitter Optionen ab, die für dieses Mesh zum Zeitpunkt der Erstellung aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="4cc08-142">Retrieves the mesh options enabled for this mesh at creation time.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="4cc08-143">**Getvertexbuffer**</span><span class="sxs-lookup"><span data-stu-id="4cc08-143">**GetVertexBuffer**</span></span>](id3dxbasemesh--getvertexbuffer.md)                         | <span data-ttu-id="4cc08-144">Ruft den dem Mesh zugeordneten Vertex-Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="4cc08-144">Retrieves the vertex buffer associated with the mesh.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="4cc08-145">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="4cc08-145">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)                         | <span data-ttu-id="4cc08-146">Sperrt einen Index Puffer und erhält einen Zeiger auf den Speicher des Index Puffers.</span><span class="sxs-lookup"><span data-stu-id="4cc08-146">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="4cc08-147">**Lockvertexbuffer**</span><span class="sxs-lookup"><span data-stu-id="4cc08-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)                       | <span data-ttu-id="4cc08-148">Sperrt einen Scheitelpunkt Puffer und erhält einen Zeiger auf den Vertex-Pufferspeicher.</span><span class="sxs-lookup"><span data-stu-id="4cc08-148">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="4cc08-149">**Unlockindexbuffer**</span><span class="sxs-lookup"><span data-stu-id="4cc08-149">**UnlockIndexBuffer**</span></span>](id3dxbasemesh--unlockindexbuffer.md)                     | <span data-ttu-id="4cc08-150">Entsperrt einen Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="4cc08-150">Unlocks an index buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="4cc08-151">**Unlockvertexbuffer**</span><span class="sxs-lookup"><span data-stu-id="4cc08-151">**UnlockVertexBuffer**</span></span>](id3dxbasemesh--unlockvertexbuffer.md)                   | <span data-ttu-id="4cc08-152">Entsperrt einen Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="4cc08-152">Unlocks a vertex buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="4cc08-153">**Updatesemantics**</span><span class="sxs-lookup"><span data-stu-id="4cc08-153">**UpdateSemantics**</span></span>](id3dxbasemesh--updatesemantics.md)                         | <span data-ttu-id="4cc08-154">Mit dieser Methode kann der Benutzer die Mesh-Deklaration ändern, ohne das Datenlayout des Vertexpuffers zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4cc08-154">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="4cc08-155">Der-Rückruf ist nur gültig, wenn die alten und neuen Deklarations Formate die gleiche Scheitelpunkt Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4cc08-155">The call is valid only if the old and new declaration formats have the same vertex size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4cc08-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cc08-156">Remarks</span></span>

<span data-ttu-id="4cc08-157">Ein Mesh ist ein Objekt, das aus einem Satz von polygonalen Flächen besteht.</span><span class="sxs-lookup"><span data-stu-id="4cc08-157">A mesh is an object made up of a set of polygonal faces.</span></span> <span data-ttu-id="4cc08-158">Ein Mesh definiert einen Satz von Scheitel Punkten und eine Gruppe von Gesichtern (die Flächen werden in Bezug auf die Scheitel Punkte und die normale des Netzes definiert).</span><span class="sxs-lookup"><span data-stu-id="4cc08-158">A mesh defines a set of vertices and a set of faces (the faces are defined in terms of the vertices and normals of the mesh).</span></span>

<span data-ttu-id="4cc08-159">Der LPD3DXBASEMESH-Typ wird als Zeiger auf die **ID3DXBaseMesh** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="4cc08-159">The LPD3DXBASEMESH type is defined as a pointer to the **ID3DXBaseMesh** interface.</span></span>


```
typedef struct ID3DXBaseMesh *LPD3DXBASEMESH;
```



## <a name="requirements"></a><span data-ttu-id="4cc08-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cc08-160">Requirements</span></span>



| <span data-ttu-id="4cc08-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cc08-161">Requirement</span></span> | <span data-ttu-id="4cc08-162">Wert</span><span class="sxs-lookup"><span data-stu-id="4cc08-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cc08-163">Header</span><span class="sxs-lookup"><span data-stu-id="4cc08-163">Header</span></span><br/>  | <dl> <span data-ttu-id="4cc08-164"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cc08-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4cc08-165">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4cc08-165">Library</span></span><br/> | <dl> <span data-ttu-id="4cc08-166"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cc08-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4cc08-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cc08-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc08-168">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4cc08-168">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
