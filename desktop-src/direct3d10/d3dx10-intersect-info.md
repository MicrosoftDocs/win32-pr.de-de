---
description: 'D3DX10_INTERSECT_INFO-Struktur: Beschreibt eine Schnittmenge von Strahldreiecken.'
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: D3DX10_INTERSECT_INFO-Struktur (D3DX10.h)
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
ms.openlocfilehash: 203daa48e766edd545bf232c4f8d94c4f17b5b2a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105458"
---
# <a name="d3dx10_intersect_info-structure"></a><span data-ttu-id="28285-103">D3DX10 \_ INTERSECT \_ INFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="28285-103">D3DX10\_INTERSECT\_INFO structure</span></span>

<span data-ttu-id="28285-104">Beschreibt eine Schnittmenge eines Strahldreiecks.</span><span class="sxs-lookup"><span data-stu-id="28285-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="28285-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28285-105">Syntax</span></span>


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a><span data-ttu-id="28285-106">Member</span><span class="sxs-lookup"><span data-stu-id="28285-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="28285-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="28285-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="28285-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28285-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="28285-109">Index des Dreiecks, das auf den Strahl trifft.</span><span class="sxs-lookup"><span data-stu-id="28285-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="28285-110">**U**</span><span class="sxs-lookup"><span data-stu-id="28285-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="28285-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28285-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="28285-112">Barycentric-Koordinate innerhalb des Dreiecks, in dem sich der Strahl überschneidet.</span><span class="sxs-lookup"><span data-stu-id="28285-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="28285-113">**B**</span><span class="sxs-lookup"><span data-stu-id="28285-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="28285-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28285-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="28285-115">Barycentric-Koordinate innerhalb des Dreiecks, in dem sich der Strahl überschneidet.</span><span class="sxs-lookup"><span data-stu-id="28285-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="28285-116">**Dist**</span><span class="sxs-lookup"><span data-stu-id="28285-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="28285-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28285-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="28285-118">Abstand entlang des Strahls, in dem die Schnittmenge aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="28285-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28285-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28285-119">Remarks</span></span>

<span data-ttu-id="28285-120">Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="28285-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="28285-121">Eine ausführlichere Beschreibung der baryzentrischen Koordinaten finden Sie unter [Mathworld es Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="28285-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="28285-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28285-122">Requirements</span></span>



| <span data-ttu-id="28285-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28285-123">Requirement</span></span> | <span data-ttu-id="28285-124">Wert</span><span class="sxs-lookup"><span data-stu-id="28285-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="28285-125">Header</span><span class="sxs-lookup"><span data-stu-id="28285-125">Header</span></span><br/> | <dl> <span data-ttu-id="28285-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="28285-126"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28285-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="28285-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28285-128">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="28285-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
