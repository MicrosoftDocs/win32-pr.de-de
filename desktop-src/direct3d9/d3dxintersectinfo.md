---
description: 'D3DXINTERSECTINFO-Struktur: Beschreibt eine Strahldreieck-Schnittmenge.'
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: D3DXINTERSECTINFO-Struktur (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINTERSECTINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: f4a63c7f4a479bfbe9dcb49f485ce0acb8db6486
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098288"
---
# <a name="d3dxintersectinfo-structure"></a><span data-ttu-id="7f919-103">D3DXINTERSECTINFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="7f919-103">D3DXINTERSECTINFO structure</span></span>

<span data-ttu-id="7f919-104">Beschreibt eine Schnittmenge eines Strahldreiecks.</span><span class="sxs-lookup"><span data-stu-id="7f919-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f919-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f919-105">Syntax</span></span>


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a><span data-ttu-id="7f919-106">Member</span><span class="sxs-lookup"><span data-stu-id="7f919-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f919-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="7f919-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="7f919-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f919-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f919-109">Index des Dreiecks, das auf den Strahl trifft.</span><span class="sxs-lookup"><span data-stu-id="7f919-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="7f919-110">**U**</span><span class="sxs-lookup"><span data-stu-id="7f919-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="7f919-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f919-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f919-112">Barycentric-Koordinate innerhalb des Dreiecks, in dem sich der Strahl überschneidet.</span><span class="sxs-lookup"><span data-stu-id="7f919-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="7f919-113">**B**</span><span class="sxs-lookup"><span data-stu-id="7f919-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="7f919-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f919-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f919-115">Barycentric-Koordinate innerhalb des Dreiecks, in dem sich der Strahl überschneidet.</span><span class="sxs-lookup"><span data-stu-id="7f919-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="7f919-116">**Dist**</span><span class="sxs-lookup"><span data-stu-id="7f919-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="7f919-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f919-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f919-118">Abstand entlang des Strahls, in dem die Schnittmenge aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7f919-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f919-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f919-119">Remarks</span></span>

<span data-ttu-id="7f919-120">Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="7f919-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="7f919-121">Eine ausführlichere Beschreibung der baryzentrischen Koordinaten finden Sie unter [Mathworld es Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="7f919-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f919-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f919-122">Requirements</span></span>



| <span data-ttu-id="7f919-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f919-123">Requirement</span></span> | <span data-ttu-id="7f919-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7f919-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f919-125">Header</span><span class="sxs-lookup"><span data-stu-id="7f919-125">Header</span></span><br/> | <dl> <span data-ttu-id="7f919-126"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="7f919-126"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f919-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7f919-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f919-128">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7f919-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
