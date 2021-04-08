---
description: Beschreibt eine Schnittmenge an Ray-Dreiecks.
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: D3DX10_INTERSECT_INFO-Struktur (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_INTERSECT_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 87490e734299cba57952bb43d1ee4ffad8e014c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762114"
---
# <a name="d3dx10_intersect_info-structure"></a><span data-ttu-id="a45c6-103">D3dx10 \_ Intersect- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="a45c6-103">D3DX10\_INTERSECT\_INFO structure</span></span>

<span data-ttu-id="a45c6-104">Beschreibt eine Schnittmenge an Ray-Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="a45c6-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a45c6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a45c6-105">Syntax</span></span>


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a><span data-ttu-id="a45c6-106">Member</span><span class="sxs-lookup"><span data-stu-id="a45c6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a45c6-107">**Fakeidex**</span><span class="sxs-lookup"><span data-stu-id="a45c6-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="a45c6-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a45c6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a45c6-109">Index des Dreiecks, das auf den Strahl trifft.</span><span class="sxs-lookup"><span data-stu-id="a45c6-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="a45c6-110">**U**</span><span class="sxs-lookup"><span data-stu-id="a45c6-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="a45c6-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a45c6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a45c6-112">Die barzentrische Koordinate innerhalb des Dreiecks, an dem sich der Strahl schneidet.</span><span class="sxs-lookup"><span data-stu-id="a45c6-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="a45c6-113">**B**</span><span class="sxs-lookup"><span data-stu-id="a45c6-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="a45c6-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a45c6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a45c6-115">Die barzentrische Koordinate innerhalb des Dreiecks, an dem sich der Strahl schneidet.</span><span class="sxs-lookup"><span data-stu-id="a45c6-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="a45c6-116">**Dirigent**</span><span class="sxs-lookup"><span data-stu-id="a45c6-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="a45c6-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a45c6-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a45c6-118">Abstand entlang des Strahls, an dem die Schnittmenge aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a45c6-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a45c6-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a45c6-119">Remarks</span></span>

<span data-ttu-id="a45c6-120">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="a45c6-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="a45c6-121">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="a45c6-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="a45c6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a45c6-122">Requirements</span></span>



| <span data-ttu-id="a45c6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a45c6-123">Requirement</span></span> | <span data-ttu-id="a45c6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a45c6-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a45c6-125">Header</span><span class="sxs-lookup"><span data-stu-id="a45c6-125">Header</span></span><br/> | <dl> <span data-ttu-id="a45c6-126"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a45c6-126"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a45c6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a45c6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a45c6-128">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a45c6-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
