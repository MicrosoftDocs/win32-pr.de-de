---
description: 'ID3DX10Mesh::GenerateAdjaencyAndPointReps-Methode: Generieren Sie eine Liste von Gitternetzkanten sowie eine Liste von Gesichtern, die die einzelnen Kanten gemeinsam nutzen.'
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: ID3DX10Mesh::GenerateAdjaencyAndPointReps-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e496f96f36805d411c71e9aba1e2560b0dcbe3c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083978"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a><span data-ttu-id="000c3-103">ID3DX10Mesh::GenerateAdjaencyAndPointReps-Methode</span><span class="sxs-lookup"><span data-stu-id="000c3-103">ID3DX10Mesh::GenerateAdjacencyAndPointReps method</span></span>

<span data-ttu-id="000c3-104">Generieren Sie eine Liste von Gitternetzrändern sowie eine Liste von Gesichtern, die die einzelnen Kanten gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="000c3-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="000c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="000c3-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a><span data-ttu-id="000c3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="000c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="000c3-107">*Epsilon* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="000c3-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="000c3-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="000c3-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="000c3-109">Gibt an, dass Scheitelpunkte, die sich in der Position um weniger als epsilon unterscheiden, als zufällig behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="000c3-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="000c3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="000c3-110">Return value</span></span>

<span data-ttu-id="000c3-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="000c3-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="000c3-112">Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.</span><span class="sxs-lookup"><span data-stu-id="000c3-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="000c3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="000c3-113">Remarks</span></span>

<span data-ttu-id="000c3-114">Nachdem eine Anwendung Adjazenzinformationen für ein Gitternetz generiert hat, können die Gitternetzdaten optimiert werden, um eine bessere Zeichnungsleistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="000c3-114">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="000c3-115">Die Reihenfolge der Einträge im Adjazenzpuffer wird durch die Reihenfolge der Scheitelpunktindizes im Indexpuffer bestimmt.</span><span class="sxs-lookup"><span data-stu-id="000c3-115">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="000c3-116">Das angrenzende Dreieck 0 entspricht immer dem Rand zwischen den Indizes der Ecken 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="000c3-116">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="000c3-117">Das angrenzende Dreieck 1 entspricht immer dem Rand zwischen den Indizes der Ecken 1 und 2, während das angrenzende Dreieck 2 dem Rand zwischen den Indizes der Ecken 2 und 0 entspricht.</span><span class="sxs-lookup"><span data-stu-id="000c3-117">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="000c3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="000c3-118">Requirements</span></span>



| <span data-ttu-id="000c3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="000c3-119">Requirement</span></span> | <span data-ttu-id="000c3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="000c3-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="000c3-121">Header</span><span class="sxs-lookup"><span data-stu-id="000c3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="000c3-122"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="000c3-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="000c3-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="000c3-123">Library</span></span><br/> | <dl> <span data-ttu-id="000c3-124"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="000c3-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="000c3-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="000c3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="000c3-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="000c3-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="000c3-127">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="000c3-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
