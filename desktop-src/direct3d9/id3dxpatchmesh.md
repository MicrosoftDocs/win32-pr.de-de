---
description: Diese Schnittstelle kapselt die patchmesh-Funktionalität.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: ID3DXPatchMesh-Schnittstelle (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1f13e6abe3a164e8027ddcb6bb33e9f0ca618fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355207"
---
# <a name="id3dxpatchmesh-interface"></a><span data-ttu-id="1e24f-103">ID3DXPatchMesh-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1e24f-103">ID3DXPatchMesh interface</span></span>

<span data-ttu-id="1e24f-104">Diese Schnittstelle kapselt die patchmesh-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="1e24f-104">This interface encapsulates patch mesh functionality.</span></span>

## <a name="members"></a><span data-ttu-id="1e24f-105">Member</span><span class="sxs-lookup"><span data-stu-id="1e24f-105">Members</span></span>

<span data-ttu-id="1e24f-106">Die **ID3DXPatchMesh** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1e24f-106">The **ID3DXPatchMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1e24f-107">**ID3DXPatchMesh** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1e24f-107">**ID3DXPatchMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="1e24f-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="1e24f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1e24f-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="1e24f-109">Methods</span></span>

<span data-ttu-id="1e24f-110">Die **ID3DXPatchMesh** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1e24f-110">The **ID3DXPatchMesh** interface has these methods.</span></span>



| <span data-ttu-id="1e24f-111">Methode</span><span class="sxs-lookup"><span data-stu-id="1e24f-111">Method</span></span>                                                                           | <span data-ttu-id="1e24f-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e24f-112">Description</span></span>                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e24f-113">**Clonemesh**</span><span class="sxs-lookup"><span data-stu-id="1e24f-113">**CloneMesh**</span></span>](id3dxpatchmesh--clonemesh.md)                                   | <span data-ttu-id="1e24f-114">Erstellt ein neues patchmesh mit der angegebenen Scheitelpunkt Deklaration.</span><span class="sxs-lookup"><span data-stu-id="1e24f-114">Creates a new patch mesh with the specified vertex declaration.</span></span><br/>                      |
| [<span data-ttu-id="1e24f-115">**Generateency**</span><span class="sxs-lookup"><span data-stu-id="1e24f-115">**GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)                   | <span data-ttu-id="1e24f-116">Generiert eine Liste der Gitter Kanten und der Patches, die die einzelnen Kanten gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e24f-116">Generate a list of mesh edges and the patches that share each edge.</span></span><br/>                  |
| [<span data-ttu-id="1e24f-117">**Getcontrolverticesperpatch**</span><span class="sxs-lookup"><span data-stu-id="1e24f-117">**GetControlVerticesPerPatch**</span></span>](id3dxpatchmesh--getcontrolverticesperpatch.md) | <span data-ttu-id="1e24f-118">Ruft die Anzahl der Steuerelement Vertices pro Patch ab.</span><span class="sxs-lookup"><span data-stu-id="1e24f-118">Gets the number of control vertices per patch.</span></span><br/>                                       |
| [<span data-ttu-id="1e24f-119">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="1e24f-119">**GetDeclaration**</span></span>](id3dxpatchmesh--getdeclaration.md)                         | <span data-ttu-id="1e24f-120">Ruft die Vertex-Deklaration ab.</span><span class="sxs-lookup"><span data-stu-id="1e24f-120">Gets the vertex declaration.</span></span><br/>                                                         |
| [<span data-ttu-id="1e24f-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="1e24f-121">**GetDevice**</span></span>](id3dxpatchmesh--getdevice.md)                                   | <span data-ttu-id="1e24f-122">Ruft das Gerät ab, das das Mesh erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="1e24f-122">Gets the device that created the mesh.</span></span><br/>                                               |
| [<span data-ttu-id="1e24f-123">**Getverdräneparam**</span><span class="sxs-lookup"><span data-stu-id="1e24f-123">**GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)                     | <span data-ttu-id="1e24f-124">Ruft Mesh-Geometrie-Verschiebungs Parameter ab.</span><span class="sxs-lookup"><span data-stu-id="1e24f-124">Gets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="1e24f-125">**Getindexbuffer**</span><span class="sxs-lookup"><span data-stu-id="1e24f-125">**GetIndexBuffer**</span></span>](id3dxpatchmesh--getindexbuffer.md)                         | <span data-ttu-id="1e24f-126">Ruft den Mesh-Index Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="1e24f-126">Gets the mesh index buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="1e24f-127">**Getnumpatches**</span><span class="sxs-lookup"><span data-stu-id="1e24f-127">**GetNumPatches**</span></span>](id3dxpatchmesh--getnumpatches.md)                           | <span data-ttu-id="1e24f-128">Ruft die Anzahl der Patches im Mesh ab.</span><span class="sxs-lookup"><span data-stu-id="1e24f-128">Gets the number of patches in the mesh.</span></span><br/>                                              |
| [<span data-ttu-id="1e24f-129">**Getnumvertices**</span><span class="sxs-lookup"><span data-stu-id="1e24f-129">**GetNumVertices**</span></span>](id3dxpatchmesh--getnumvertices.md)                         | <span data-ttu-id="1e24f-130">Ruft die Anzahl der Scheitel Punkte im Mesh ab.</span><span class="sxs-lookup"><span data-stu-id="1e24f-130">Gets the number of vertices in the mesh.</span></span><br/>                                             |
| [<span data-ttu-id="1e24f-131">**GetOptions**</span><span class="sxs-lookup"><span data-stu-id="1e24f-131">**GetOptions**</span></span>](id3dxpatchmesh--getoptions.md)                                 | <span data-ttu-id="1e24f-132">Ruft den Typ des Patches ab.</span><span class="sxs-lookup"><span data-stu-id="1e24f-132">Gets the type of patch.</span></span><br/>                                                              |
| [<span data-ttu-id="1e24f-133">**Getpatchinfo**</span><span class="sxs-lookup"><span data-stu-id="1e24f-133">**GetPatchInfo**</span></span>](id3dxpatchmesh--getpatchinfo.md)                             | <span data-ttu-id="1e24f-134">Ruft die Attribute des Patches ab.</span><span class="sxs-lookup"><span data-stu-id="1e24f-134">Gets the attributes of the patch.</span></span><br/>                                                    |
| [<span data-ttu-id="1e24f-135">**Gettesssize**</span><span class="sxs-lookup"><span data-stu-id="1e24f-135">**GetTessSize**</span></span>](id3dxpatchmesh--gettesssize.md)                               | <span data-ttu-id="1e24f-136">Ruft die Größe des Mosaik Netzes ab, wenn eine Mosaik Ebene angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1e24f-136">Gets the size of the tessellated mesh, given a tessellation level.</span></span><br/>                   |
| [<span data-ttu-id="1e24f-137">**Getvertexbuffer**</span><span class="sxs-lookup"><span data-stu-id="1e24f-137">**GetVertexBuffer**</span></span>](id3dxpatchmesh--getvertexbuffer.md)                       | <span data-ttu-id="1e24f-138">Ruft den mesvertexpuffer ab.</span><span class="sxs-lookup"><span data-stu-id="1e24f-138">Gets the mesh vertex buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="1e24f-139">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="1e24f-139">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)               | <span data-ttu-id="1e24f-140">Sperrt den Attribut Puffer.</span><span class="sxs-lookup"><span data-stu-id="1e24f-140">Locks the attribute buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="1e24f-141">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="1e24f-141">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)                       | <span data-ttu-id="1e24f-142">Sperren Sie den Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="1e24f-142">Lock the index buffer.</span></span><br/>                                                               |
| [<span data-ttu-id="1e24f-143">**Lockvertexbuffer**</span><span class="sxs-lookup"><span data-stu-id="1e24f-143">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)                     | <span data-ttu-id="1e24f-144">Sperren Sie den Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="1e24f-144">Lock the vertex buffer.</span></span><br/>                                                              |
| [<span data-ttu-id="1e24f-145">**Optimieren**</span><span class="sxs-lookup"><span data-stu-id="1e24f-145">**Optimize**</span></span>](id3dxpatchmesh--optimize.md)                                     | <span data-ttu-id="1e24f-146">Optimiert das patchemesh für effizientes Mosaik.</span><span class="sxs-lookup"><span data-stu-id="1e24f-146">Optimizes the patch mesh for efficient tessellation.</span></span><br/>                                 |
| [<span data-ttu-id="1e24f-147">**Setverdräneparam**</span><span class="sxs-lookup"><span data-stu-id="1e24f-147">**SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)                     | <span data-ttu-id="1e24f-148">Legt Mesh-Geometrie-Verschiebungs Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="1e24f-148">Sets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="1e24f-149">**& Nbsp;**</span><span class="sxs-lookup"><span data-stu-id="1e24f-149">**Tessellate**</span></span>](id3dxpatchmesh--tessellate.md)                                 | <span data-ttu-id="1e24f-150">Führt ein einheitliches Mosaik basierend auf der Mosaik Ebene aus.</span><span class="sxs-lookup"><span data-stu-id="1e24f-150">Performs uniform tessellation based on the tessellation level.</span></span><br/>                       |
| [<span data-ttu-id="1e24f-151">**Tbitellateadaptive**</span><span class="sxs-lookup"><span data-stu-id="1e24f-151">**TessellateAdaptive**</span></span>](id3dxpatchmesh--tessellateadaptive.md)                 | <span data-ttu-id="1e24f-152">Führt ein adaptives Mosaik basierend auf dem z-basierten adaptiven Mosaik Kriterium aus.</span><span class="sxs-lookup"><span data-stu-id="1e24f-152">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span><br/> |
| [<span data-ttu-id="1e24f-153">**UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="1e24f-153">**UnlockAttributeBuffer**</span></span>](id3dxpatchmesh--unlockattributebuffer.md)           | <span data-ttu-id="1e24f-154">Entsperren Sie den Attribut Puffer.</span><span class="sxs-lookup"><span data-stu-id="1e24f-154">Unlock the attribute buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="1e24f-155">**Unlockindexbuffer**</span><span class="sxs-lookup"><span data-stu-id="1e24f-155">**UnlockIndexBuffer**</span></span>](id3dxpatchmesh--unlockindexbuffer.md)                   | <span data-ttu-id="1e24f-156">Entsperren Sie den Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="1e24f-156">Unlock the index buffer.</span></span><br/>                                                             |
| [<span data-ttu-id="1e24f-157">**Unlockvertexbuffer**</span><span class="sxs-lookup"><span data-stu-id="1e24f-157">**UnlockVertexBuffer**</span></span>](id3dxpatchmesh--unlockvertexbuffer.md)                 | <span data-ttu-id="1e24f-158">Entsperren Sie den Vertex-Puffer.</span><span class="sxs-lookup"><span data-stu-id="1e24f-158">Unlock the vertex buffer.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="1e24f-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e24f-159">Remarks</span></span>

<span data-ttu-id="1e24f-160">Ein patchmesh ist ein Mesh, das aus einer Reihe von Patches besteht.</span><span class="sxs-lookup"><span data-stu-id="1e24f-160">A patch mesh is a mesh that consists of a series of patches.</span></span>

<span data-ttu-id="1e24f-161">Rufen Sie zum Abrufen der **ID3DXPatchMesh** -Schnittstelle die [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="1e24f-161">To obtain the **ID3DXPatchMesh** interface, call the [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) function.</span></span>

<span data-ttu-id="1e24f-162">Der LPD3DXPATCHMESH-Typ wird wie folgt als Zeiger auf die **ID3DXPatchMesh** -Schnittstelle definiert:</span><span class="sxs-lookup"><span data-stu-id="1e24f-162">The LPD3DXPATCHMESH type is defined as a pointer to the **ID3DXPatchMesh** interface, as follows:</span></span>


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a><span data-ttu-id="1e24f-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e24f-163">Requirements</span></span>



| <span data-ttu-id="1e24f-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e24f-164">Requirement</span></span> | <span data-ttu-id="1e24f-165">Wert</span><span class="sxs-lookup"><span data-stu-id="1e24f-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e24f-166">Header</span><span class="sxs-lookup"><span data-stu-id="1e24f-166">Header</span></span><br/>  | <dl> <span data-ttu-id="1e24f-167"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e24f-167"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1e24f-168">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e24f-168">Library</span></span><br/> | <dl> <span data-ttu-id="1e24f-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e24f-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1e24f-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e24f-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e24f-171">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1e24f-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1e24f-172">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1e24f-172">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
