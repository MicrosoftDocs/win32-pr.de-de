---
description: 'ID3DXBaseMesh::GenerateAdjaency-Methode: Generieren Sie eine Liste von Gitternetzkanten sowie eine Liste von Gesichtern, die die einzelnen Kanten gemeinsam nutzen.'
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: ID3DXBaseMesh::GenerateAdencyency-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: 783ed7ad61337e606793b9b467e4b17fddd7ecd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115458"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a><span data-ttu-id="49771-103">ID3DXBaseMesh::GenerateAdjaency-Methode</span><span class="sxs-lookup"><span data-stu-id="49771-103">ID3DXBaseMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="49771-104">Generieren Sie eine Liste von Gitternetzrändern sowie eine Liste von Gesichtern, die die einzelnen Kanten gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="49771-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="49771-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49771-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="49771-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="49771-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49771-107">*Epsilon* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="49771-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49771-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49771-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49771-109">Gibt an, dass Scheitelpunkte, die sich in der Position um weniger als epsilon unterscheiden, als zufällig behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="49771-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> <dt>

<span data-ttu-id="49771-110">*pAdjazenz* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="49771-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49771-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="49771-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="49771-112">Zeiger auf ein Array von drei DWORDs pro Gesicht, das mit den Indizes benachbarter Gesichter gefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="49771-112">Pointer to an array of three DWORDs per face to be filled with the indices of adjacent faces.</span></span> <span data-ttu-id="49771-113">Die Anzahl der Bytes in diesem Array muss mindestens \* [**3 ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD) betragen.</span><span class="sxs-lookup"><span data-stu-id="49771-113">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49771-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49771-114">Return value</span></span>

<span data-ttu-id="49771-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49771-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49771-116">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="49771-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="49771-117">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="49771-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="49771-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49771-118">Remarks</span></span>

<span data-ttu-id="49771-119">Nachdem eine Anwendung Adjazenzinformationen für ein Gitternetz generiert hat, können die Gitternetzdaten optimiert werden, um eine bessere Zeichnungsleistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="49771-119">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="49771-120">Die Reihenfolge der Einträge im Adjazenzpuffer wird durch die Reihenfolge der Scheitelpunktindizes im Indexpuffer bestimmt.</span><span class="sxs-lookup"><span data-stu-id="49771-120">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="49771-121">Das angrenzende Dreieck 0 entspricht immer dem Rand zwischen den Indizes der Ecken 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="49771-121">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="49771-122">Das angrenzende Dreieck 1 entspricht immer dem Rand zwischen den Indizes der Ecken 1 und 2, während das angrenzende Dreieck 2 dem Rand zwischen den Indizes der Ecken 2 und 0 entspricht.</span><span class="sxs-lookup"><span data-stu-id="49771-122">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="49771-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49771-123">Requirements</span></span>



| <span data-ttu-id="49771-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49771-124">Requirement</span></span> | <span data-ttu-id="49771-125">Wert</span><span class="sxs-lookup"><span data-stu-id="49771-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49771-126">Header</span><span class="sxs-lookup"><span data-stu-id="49771-126">Header</span></span><br/>  | <dl> <span data-ttu-id="49771-127"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="49771-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="49771-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="49771-128">Library</span></span><br/> | <dl> <span data-ttu-id="49771-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="49771-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="49771-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="49771-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49771-131">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="49771-131">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="49771-132">**ID3DXMesh::Optimize**</span><span class="sxs-lookup"><span data-stu-id="49771-132">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> <dt>

[<span data-ttu-id="49771-133">**ID3DXMesh::OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="49771-133">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
