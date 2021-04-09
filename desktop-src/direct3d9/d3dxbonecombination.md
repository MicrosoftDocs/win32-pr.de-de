---
description: Beschreibt eine Teilmenge des Netzes, das über das gleiche Attribut und die gleiche Kombination aus dem gleichen Knoten verfügt.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: D3DXBONECOMBINATION-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 3553ba37d0d9376fa5912143fb58849f03c5a83a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050873"
---
# <a name="d3dxbonecombination-structure"></a><span data-ttu-id="0dcd3-103">D3DXBONECOMBINATION-Struktur</span><span class="sxs-lookup"><span data-stu-id="0dcd3-103">D3DXBONECOMBINATION structure</span></span>

<span data-ttu-id="0dcd3-104">Beschreibt eine Teilmenge des Netzes, das über das gleiche Attribut und die gleiche Kombination aus dem gleichen Knoten verfügt.</span><span class="sxs-lookup"><span data-stu-id="0dcd3-104">Describes a subset of the mesh that has the same attribute and bone combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dcd3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dcd3-105">Syntax</span></span>


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a><span data-ttu-id="0dcd3-106">Member</span><span class="sxs-lookup"><span data-stu-id="0dcd3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0dcd3-107">**Atungbid**</span><span class="sxs-lookup"><span data-stu-id="0dcd3-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="0dcd3-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dcd3-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0dcd3-109">Attribut Tabellen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="0dcd3-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0dcd3-110">**Fakestart**</span><span class="sxs-lookup"><span data-stu-id="0dcd3-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="0dcd3-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dcd3-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0dcd3-112">Startseite.</span><span class="sxs-lookup"><span data-stu-id="0dcd3-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="0dcd3-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="0dcd3-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="0dcd3-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dcd3-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0dcd3-115">Anzahl der Gesichter.</span><span class="sxs-lookup"><span data-stu-id="0dcd3-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="0dcd3-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="0dcd3-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="0dcd3-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dcd3-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0dcd3-118">Der Scheitelpunkt wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="0dcd3-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="0dcd3-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="0dcd3-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="0dcd3-120">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dcd3-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0dcd3-121">Vertex-Anzahl.</span><span class="sxs-lookup"><span data-stu-id="0dcd3-121">Vertex count.</span></span>

</dd> <dt>

<span data-ttu-id="0dcd3-122">**Boneid**</span><span class="sxs-lookup"><span data-stu-id="0dcd3-122">**BoneId**</span></span>
</dt> <dd>

<span data-ttu-id="0dcd3-123">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0dcd3-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="0dcd3-124">Ein Zeiger auf ein Array von Werten, die jeden der Knochen identifizieren, die in einem einzelnen Zeichnungs Befehl gezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="0dcd3-124">Pointer to an array of values that identify each of the bones that can be drawn in a single drawing call.</span></span> <span data-ttu-id="0dcd3-125">Beachten Sie, dass das Array eine Variable Länge aufweisen kann, um die Kombination der Variablen mit variabler Länge von [**convertumindexedblendedmesh**](id3dxskininfo--converttoindexedblendedmesh.md)zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0dcd3-125">Note that the array can be of variable length to accommodate variable length bone combinations of [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).</span></span>

<span data-ttu-id="0dcd3-126">Die Größe des Arrays variiert je nach Typ des generierten Diagrammtyps.</span><span class="sxs-lookup"><span data-stu-id="0dcd3-126">The size of the array varies based on the type of mesh generated.</span></span> <span data-ttu-id="0dcd3-127">Eine nicht indizierte Gitter Array Größe ist gleich der Anzahl der Gewichtungen pro Scheitelpunkt (pmaxvertexinfl in [**convertumblendedmesh**](id3dxskininfo--converttoblendedmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="0dcd3-127">A non-indexed mesh array size is equal to the number of weights per vertex (pMaxVertexInfl in [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)).</span></span> <span data-ttu-id="0dcd3-128">Die Größe eines indizierten Mesh-Arrays entspricht der Anzahl der Einträge in der Band Matrix Palette (palettesize in [**convertumindexedblendedmesh**](id3dxskininfo--converttoindexedblendedmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="0dcd3-128">An indexed mesh array size is equal to the number of bone matrix palette entries (paletteSize in [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0dcd3-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0dcd3-129">Remarks</span></span>

<span data-ttu-id="0dcd3-130">Die Teilmenge des von **D3DXBONECOMBINATION** beschriebenen Netzes kann in einem einzelnen Zeichnungs Befehl gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="0dcd3-130">The subset of the mesh described by **D3DXBONECOMBINATION** can be rendered in a single drawing call.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dcd3-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0dcd3-131">Requirements</span></span>



| <span data-ttu-id="0dcd3-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0dcd3-132">Requirement</span></span> | <span data-ttu-id="0dcd3-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0dcd3-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dcd3-134">Header</span><span class="sxs-lookup"><span data-stu-id="0dcd3-134">Header</span></span><br/> | <dl> <span data-ttu-id="0dcd3-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dcd3-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dcd3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dcd3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dcd3-137">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="0dcd3-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
