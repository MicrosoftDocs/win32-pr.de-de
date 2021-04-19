---
description: Beschreibt eine Schnittmenge an Ray-Dreiecks.
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: D3DXINTERSECTINFO-Struktur (D3dx9mesh. h)
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
ms.openlocfilehash: 31a98e9a7095e81e962b2996dedb9bdf5871533d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355009"
---
# <a name="d3dxintersectinfo-structure"></a><span data-ttu-id="b8ed2-103">D3DXINTERSECTINFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="b8ed2-103">D3DXINTERSECTINFO structure</span></span>

<span data-ttu-id="b8ed2-104">Beschreibt eine Schnittmenge an Ray-Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="b8ed2-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8ed2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8ed2-105">Syntax</span></span>


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a><span data-ttu-id="b8ed2-106">Member</span><span class="sxs-lookup"><span data-stu-id="b8ed2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b8ed2-107">**Fakeidex**</span><span class="sxs-lookup"><span data-stu-id="b8ed2-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="b8ed2-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8ed2-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b8ed2-109">Index des Dreiecks, das auf den Strahl trifft.</span><span class="sxs-lookup"><span data-stu-id="b8ed2-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed2-110">**U**</span><span class="sxs-lookup"><span data-stu-id="b8ed2-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="b8ed2-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8ed2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b8ed2-112">Die barzentrische Koordinate innerhalb des Dreiecks, an dem sich der Strahl schneidet.</span><span class="sxs-lookup"><span data-stu-id="b8ed2-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed2-113">**B**</span><span class="sxs-lookup"><span data-stu-id="b8ed2-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="b8ed2-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8ed2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b8ed2-115">Die barzentrische Koordinate innerhalb des Dreiecks, an dem sich der Strahl schneidet.</span><span class="sxs-lookup"><span data-stu-id="b8ed2-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="b8ed2-116">**Dirigent**</span><span class="sxs-lookup"><span data-stu-id="b8ed2-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="b8ed2-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8ed2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b8ed2-118">Abstand entlang des Strahls, an dem die Schnittmenge aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b8ed2-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8ed2-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8ed2-119">Remarks</span></span>

<span data-ttu-id="b8ed2-120">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="b8ed2-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="b8ed2-121">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="b8ed2-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ed2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8ed2-122">Requirements</span></span>



| <span data-ttu-id="b8ed2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8ed2-123">Requirement</span></span> | <span data-ttu-id="b8ed2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b8ed2-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ed2-125">Header</span><span class="sxs-lookup"><span data-stu-id="b8ed2-125">Header</span></span><br/> | <dl> <span data-ttu-id="b8ed2-126"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8ed2-126"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8ed2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8ed2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ed2-128">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b8ed2-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
