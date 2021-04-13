---
description: Anwendungen verwenden die Methoden der ID3DXMesh-Schnittstelle zum Bearbeiten von Mesh-Objekten.
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: ID3DXMesh-Schnittstelle (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c2a677edba4bad5e908b6dd69aa21a467b2a245
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355716"
---
# <a name="id3dxmesh-interface"></a><span data-ttu-id="e2a83-103">ID3DXMesh-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e2a83-103">ID3DXMesh interface</span></span>

<span data-ttu-id="e2a83-104">Anwendungen verwenden die Methoden der ID3DXMesh-Schnittstelle zum Bearbeiten von Mesh-Objekten.</span><span class="sxs-lookup"><span data-stu-id="e2a83-104">Applications use the methods of the ID3DXMesh interface to manipulate mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="e2a83-105">Member</span><span class="sxs-lookup"><span data-stu-id="e2a83-105">Members</span></span>

<span data-ttu-id="e2a83-106">Die **ID3DXMesh** -Schnittstelle erbt von [**ID3DXBaseMesh**](id3dxbasemesh.md).</span><span class="sxs-lookup"><span data-stu-id="e2a83-106">The **ID3DXMesh** interface inherits from [**ID3DXBaseMesh**](id3dxbasemesh.md).</span></span> <span data-ttu-id="e2a83-107">**ID3DXMesh** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e2a83-107">**ID3DXMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="e2a83-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="e2a83-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e2a83-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="e2a83-109">Methods</span></span>

<span data-ttu-id="e2a83-110">Die **ID3DXMesh** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e2a83-110">The **ID3DXMesh** interface has these methods.</span></span>



| <span data-ttu-id="e2a83-111">Methode</span><span class="sxs-lookup"><span data-stu-id="e2a83-111">Method</span></span>                                                            | <span data-ttu-id="e2a83-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2a83-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2a83-113">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="e2a83-113">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)     | <span data-ttu-id="e2a83-114">Sperrt den Gitter Puffer, der die Daten des Mesh-Attributs enthält, und gibt einen Zeiger darauf zurück.</span><span class="sxs-lookup"><span data-stu-id="e2a83-114">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span><br/>                                   |
| [<span data-ttu-id="e2a83-115">**Optimieren**</span><span class="sxs-lookup"><span data-stu-id="e2a83-115">**Optimize**</span></span>](id3dxmesh--optimize.md)                           | <span data-ttu-id="e2a83-116">Generiert ein neues Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="e2a83-116">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span><br/>                                     |
| [<span data-ttu-id="e2a83-117">**Optimizanplace**</span><span class="sxs-lookup"><span data-stu-id="e2a83-117">**OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)             | <span data-ttu-id="e2a83-118">Generiert ein Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="e2a83-118">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="e2a83-119">Diese Methode ordnet das vorhandene Mesh neu an.</span><span class="sxs-lookup"><span data-stu-id="e2a83-119">This method reorders the existing mesh.</span></span><br/> |
| [<span data-ttu-id="e2a83-120">**""-Tributetable "**</span><span class="sxs-lookup"><span data-stu-id="e2a83-120">**SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)         | <span data-ttu-id="e2a83-121">Legt die Attribut Tabelle für ein Mesh und die Anzahl der in der Tabelle gespeicherten Einträge fest.</span><span class="sxs-lookup"><span data-stu-id="e2a83-121">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span><br/>                                          |
| [<span data-ttu-id="e2a83-122">**UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="e2a83-122">**UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md) | <span data-ttu-id="e2a83-123">Entsperrt einen Attribut Puffer.</span><span class="sxs-lookup"><span data-stu-id="e2a83-123">Unlocks an attribute buffer.</span></span><br/>                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="e2a83-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2a83-124">Remarks</span></span>

<span data-ttu-id="e2a83-125">Rufen Sie zum Abrufen der **ID3DXMesh** -Schnittstelle entweder die [**D3DXCreateMesh**](d3dxcreatemesh.md) -oder die [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="e2a83-125">To obtain the **ID3DXMesh** interface, call either the [**D3DXCreateMesh**](d3dxcreatemesh.md) or [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) function.</span></span>

<span data-ttu-id="e2a83-126">Diese Schnittstelle erbt zusätzliche Funktionen von der [**ID3DXBaseMesh**](id3dxbasemesh.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e2a83-126">This interface inherits additional functionality from the [**ID3DXBaseMesh**](id3dxbasemesh.md) interface.</span></span>

<span data-ttu-id="e2a83-127">Der LPD3DXMESH-Typ wird als Zeiger auf die **ID3DXMesh** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="e2a83-127">The LPD3DXMESH type is defined as a pointer to the **ID3DXMesh** interface.</span></span>


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a><span data-ttu-id="e2a83-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2a83-128">Requirements</span></span>



| <span data-ttu-id="e2a83-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2a83-129">Requirement</span></span> | <span data-ttu-id="e2a83-130">Wert</span><span class="sxs-lookup"><span data-stu-id="e2a83-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a83-131">Header</span><span class="sxs-lookup"><span data-stu-id="e2a83-131">Header</span></span><br/>  | <dl> <span data-ttu-id="e2a83-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2a83-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e2a83-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2a83-133">Library</span></span><br/> | <dl> <span data-ttu-id="e2a83-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2a83-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e2a83-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2a83-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a83-136">**ID3DXBaseMesh**</span><span class="sxs-lookup"><span data-stu-id="e2a83-136">**ID3DXBaseMesh**</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="e2a83-137">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e2a83-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e2a83-138">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e2a83-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




