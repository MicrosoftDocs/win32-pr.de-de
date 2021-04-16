---
description: Generieren Sie eine Liste mit Gitter Kanten sowie eine Liste der Flächen, die die einzelnen Kanten gemeinsam verwenden.
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: 'ID3DXBaseMesh:: generateaccessency-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5b1d304878a4977bb14d6ef98ad7256b6c3181f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394194"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a><span data-ttu-id="324da-103">ID3DXBaseMesh:: generateaccessency-Methode</span><span class="sxs-lookup"><span data-stu-id="324da-103">ID3DXBaseMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="324da-104">Generieren Sie eine Liste mit Gitter Kanten sowie eine Liste der Flächen, die die einzelnen Kanten gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="324da-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="324da-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="324da-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="324da-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="324da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="324da-107">*Epsilon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="324da-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="324da-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="324da-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="324da-109">Gibt an, dass Scheitel Punkte, die sich an einer Position um weniger als Epsilon unterscheiden, als Coincident behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="324da-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> <dt>

<span data-ttu-id="324da-110">*padjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="324da-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="324da-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="324da-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="324da-112">Ein Zeiger auf ein Array von drei DWORDs pro Gesicht, das mit den Indizes der angrenzenden Gesichter aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="324da-112">Pointer to an array of three DWORDs per face to be filled with the indices of adjacent faces.</span></span> <span data-ttu-id="324da-113">Die Anzahl der Bytes in diesem Array muss mindestens 3 \* [**ID3DXBaseMesh:: getnumgesichter**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD) betragen.</span><span class="sxs-lookup"><span data-stu-id="324da-113">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="324da-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="324da-114">Return value</span></span>

<span data-ttu-id="324da-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="324da-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="324da-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="324da-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="324da-117">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="324da-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="324da-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="324da-118">Remarks</span></span>

<span data-ttu-id="324da-119">Nachdem eine Anwendung Informationen zu einem Mesh generiert hat, können die Mesh-Daten optimiert werden, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="324da-119">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="324da-120">Die Reihenfolge der Einträge im Anfügungs Puffer wird durch die Reihenfolge der Scheitelpunkt Indizes im Index Puffer bestimmt.</span><span class="sxs-lookup"><span data-stu-id="324da-120">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="324da-121">Das angrenzende Dreieck 0 entspricht immer dem Rand zwischen den Indizes der Ecken 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="324da-121">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="324da-122">Das angrenzende Dreieck 1 entspricht immer dem Rand zwischen den Indizes der Ecken 1 und 2, während das angrenzende Dreieck 2 dem Rand zwischen den Indizes der Ecken 2 und 0 entspricht.</span><span class="sxs-lookup"><span data-stu-id="324da-122">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="324da-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="324da-123">Requirements</span></span>



| <span data-ttu-id="324da-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="324da-124">Requirement</span></span> | <span data-ttu-id="324da-125">Wert</span><span class="sxs-lookup"><span data-stu-id="324da-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="324da-126">Header</span><span class="sxs-lookup"><span data-stu-id="324da-126">Header</span></span><br/>  | <dl> <span data-ttu-id="324da-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="324da-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="324da-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="324da-128">Library</span></span><br/> | <dl> <span data-ttu-id="324da-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="324da-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="324da-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="324da-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="324da-131">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="324da-131">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="324da-132">**ID3DXMesh:: optimieren**</span><span class="sxs-lookup"><span data-stu-id="324da-132">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> <dt>

[<span data-ttu-id="324da-133">**ID3DXMesh:: optimizeingeplace**</span><span class="sxs-lookup"><span data-stu-id="324da-133">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
