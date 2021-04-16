---
description: Generieren Sie eine Liste mit Gitter Kanten sowie eine Liste der Flächen, die die einzelnen Kanten gemeinsam verwenden.
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'ID3DX10Mesh:: generateaccessumcyandpointreps-Methode (d3dx10. h)'
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
ms.openlocfilehash: c46cf83931c95116132798ca971f9d4e61da2af8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530992"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a><span data-ttu-id="71da4-103">ID3DX10Mesh:: generateaccessumcyandpointreps-Methode</span><span class="sxs-lookup"><span data-stu-id="71da4-103">ID3DX10Mesh::GenerateAdjacencyAndPointReps method</span></span>

<span data-ttu-id="71da4-104">Generieren Sie eine Liste mit Gitter Kanten sowie eine Liste der Flächen, die die einzelnen Kanten gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="71da4-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="71da4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="71da4-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a><span data-ttu-id="71da4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="71da4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71da4-107">*Epsilon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71da4-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71da4-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71da4-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71da4-109">Gibt an, dass Scheitel Punkte, die sich an einer Position um weniger als Epsilon unterscheiden, als Coincident behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71da4-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71da4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71da4-110">Return value</span></span>

<span data-ttu-id="71da4-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="71da4-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="71da4-112">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="71da4-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="71da4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71da4-113">Remarks</span></span>

<span data-ttu-id="71da4-114">Nachdem eine Anwendung Informationen zu einem Mesh generiert hat, können die Mesh-Daten optimiert werden, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="71da4-114">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="71da4-115">Die Reihenfolge der Einträge im Anfügungs Puffer wird durch die Reihenfolge der Scheitelpunkt Indizes im Index Puffer bestimmt.</span><span class="sxs-lookup"><span data-stu-id="71da4-115">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="71da4-116">Das angrenzende Dreieck 0 entspricht immer dem Rand zwischen den Indizes der Ecken 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="71da4-116">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="71da4-117">Das angrenzende Dreieck 1 entspricht immer dem Rand zwischen den Indizes der Ecken 1 und 2, während das angrenzende Dreieck 2 dem Rand zwischen den Indizes der Ecken 2 und 0 entspricht.</span><span class="sxs-lookup"><span data-stu-id="71da4-117">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="71da4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71da4-118">Requirements</span></span>



| <span data-ttu-id="71da4-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71da4-119">Requirement</span></span> | <span data-ttu-id="71da4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="71da4-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71da4-121">Header</span><span class="sxs-lookup"><span data-stu-id="71da4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="71da4-122"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="71da4-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="71da4-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71da4-123">Library</span></span><br/> | <dl> <span data-ttu-id="71da4-124"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71da4-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71da4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71da4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71da4-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="71da4-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="71da4-127">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="71da4-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
