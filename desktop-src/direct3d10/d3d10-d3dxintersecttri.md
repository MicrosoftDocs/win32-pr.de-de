---
description: 'D3DXIntersectTri-Funktion (D3DX10math.h): Berechnet die Schnittmenge eines Strahls und eines Dreiecks.'
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: D3DXIntersectTri-Funktion (D3DX10math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectTri
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c8bf502cca48701a7d71a083e515f9988cafe303
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113238"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a><span data-ttu-id="9082a-103">D3DXIntersectTri-Funktion (D3DX10math.h)</span><span class="sxs-lookup"><span data-stu-id="9082a-103">D3DXIntersectTri function (D3DX10math.h)</span></span>

<span data-ttu-id="9082a-104">Berechnet die Schnittmenge eines Strahls und eines Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="9082a-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="9082a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9082a-105">Syntax</span></span>


```C++
BOOL D3DXIntersectTri(
  _In_  const D3DXVECTOR3 *p0,
  _In_  const D3DXVECTOR3 *p1,
  _In_  const D3DXVECTOR3 *p2,
  _In_  const D3DXVECTOR3 *pRayPos,
  _In_  const D3DXVECTOR3 *pRayDir,
  _Out_       FLOAT       *pU,
  _Out_       FLOAT       *pV,
  _Out_       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="9082a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9082a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9082a-107">*p0* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9082a-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9082a-108">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9082a-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9082a-109">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die Erste Dreiecksvertexposition beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9082a-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="9082a-110">*p1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9082a-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9082a-111">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9082a-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9082a-112">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die Position des zweiten Dreiecks vertex beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9082a-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="9082a-113">*p2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9082a-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9082a-114">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9082a-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9082a-115">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die Position des dritten Dreiecks vertex beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9082a-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="9082a-116">*pRayPos* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9082a-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9082a-117">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9082a-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9082a-118">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) wobei der Punkt angegeben wird, an dem der Strahl beginnt.</span><span class="sxs-lookup"><span data-stu-id="9082a-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="9082a-119">*pRayDir* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9082a-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9082a-120">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9082a-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9082a-121">Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3d10-d3dxvector3.md) unter Angabe der Richtung des Strahls.</span><span class="sxs-lookup"><span data-stu-id="9082a-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="9082a-122">*pU* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9082a-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9082a-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9082a-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9082a-124">Barycentric-Trefferkoordinaten, U.</span><span class="sxs-lookup"><span data-stu-id="9082a-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="9082a-125">*pV* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9082a-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9082a-126">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9082a-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9082a-127">Barycentric-Trefferkoordinaten, V.</span><span class="sxs-lookup"><span data-stu-id="9082a-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="9082a-128">*pDist* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9082a-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9082a-129">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9082a-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9082a-130">Entfernung des Ray-Intersection-Parameters.</span><span class="sxs-lookup"><span data-stu-id="9082a-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9082a-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9082a-131">Return value</span></span>

<span data-ttu-id="9082a-132">Typ: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9082a-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9082a-133">Gibt **TRUE** zurück, wenn der Strahl den Bereich des Dreiecks überschneidet.</span><span class="sxs-lookup"><span data-stu-id="9082a-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="9082a-134">Andernfalls gibt **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="9082a-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9082a-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9082a-135">Remarks</span></span>

<span data-ttu-id="9082a-136">Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (U,V) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9082a-136">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="9082a-137">Der Parameter U steuert, wie viel V2 in das Ergebnis gewichtet wird, und der Parameter V steuert, wie viel V3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="9082a-137">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="9082a-138">Schließlich steuert der Wert von 1 – \[ (U + V), \] wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="9082a-138">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="9082a-139">Barycentric-Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="9082a-139">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="9082a-140">In diesem Kontext stellt die Verwendung von baryzentrischen Koordinaten eine Änderung der Koordinatensysteme dar.</span><span class="sxs-lookup"><span data-stu-id="9082a-140">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="9082a-141">Was für kartesische Koordinaten gilt, gilt für baryzentrische Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="9082a-141">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="9082a-142">Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="9082a-142">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="9082a-143">Eine ausführlichere Beschreibung der baryzentrischen Koordinaten finden Sie unter [Mathworld es Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="9082a-143">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="9082a-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9082a-144">Requirements</span></span>



| <span data-ttu-id="9082a-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9082a-145">Requirement</span></span> | <span data-ttu-id="9082a-146">Wert</span><span class="sxs-lookup"><span data-stu-id="9082a-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9082a-147">Header</span><span class="sxs-lookup"><span data-stu-id="9082a-147">Header</span></span><br/>  | <dl> <span data-ttu-id="9082a-148"><dt>D3DX10math.h</dt></span><span class="sxs-lookup"><span data-stu-id="9082a-148"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="9082a-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9082a-149">Library</span></span><br/> | <dl> <span data-ttu-id="9082a-150"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9082a-150"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9082a-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9082a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9082a-152">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9082a-152">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
