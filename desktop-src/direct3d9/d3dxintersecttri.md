---
description: 'D3DXIntersectTri-Funktion (D3DX9Mesh.h): Berechnet die Schnittmenge eines Strahls und eines Dreiecks.'
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: D3DXIntersectTri-Funktion (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33d45beda51a7a2c80debafbab864c2accb33653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098268"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a><span data-ttu-id="0fbdb-103">D3DXIntersectTri-Funktion (D3DX9Mesh.h)</span><span class="sxs-lookup"><span data-stu-id="0fbdb-103">D3DXIntersectTri function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="0fbdb-104">Berechnet die Schnittmenge eines Strahls und eines Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fbdb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fbdb-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0fbdb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fbdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fbdb-107">*p0* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0fbdb-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbdb-108">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0fbdb-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0fbdb-109">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die position des ersten Dreiecksvertex beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="0fbdb-110">*p1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0fbdb-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbdb-111">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0fbdb-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0fbdb-112">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die position des zweiten Dreiecksvertex beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="0fbdb-113">*p2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0fbdb-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbdb-114">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0fbdb-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0fbdb-115">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Position des dritten Dreiecksvertex beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="0fbdb-116">*pRayPos* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0fbdb-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbdb-117">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0fbdb-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0fbdb-118">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) der den Punkt angibt, an dem der Strahl beginnt.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="0fbdb-119">*pRayDir* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0fbdb-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbdb-120">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0fbdb-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0fbdb-121">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="0fbdb-122">*pU* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0fbdb-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbdb-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0fbdb-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0fbdb-124">Barycentric-Trefferkoordinaten, U.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="0fbdb-125">*pV* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0fbdb-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbdb-126">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0fbdb-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0fbdb-127">Barycentric-Trefferkoordinaten, V.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="0fbdb-128">*pDist* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0fbdb-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbdb-129">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0fbdb-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0fbdb-130">Entfernung des Ray-Intersection-Parameters.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fbdb-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fbdb-131">Return value</span></span>

<span data-ttu-id="0fbdb-132">Typ: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0fbdb-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0fbdb-133">Gibt **TRUE** zurück, wenn der Strahl den Bereich des Dreiecks überschneidet.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="0fbdb-134">Andernfalls gibt **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fbdb-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fbdb-135">Remarks</span></span>

<span data-ttu-id="0fbdb-136">Die [**D3DXIntersect-Funktion**](d3dxintersect.md) bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-136">The [**D3DXIntersect**](d3dxintersect.md) function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="0fbdb-137">Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: V1 + U(V2 - V1) + V(V3 - V1).</span><span class="sxs-lookup"><span data-stu-id="0fbdb-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="0fbdb-138">Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (U,V) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="0fbdb-139">Der Parameter U steuert, wie viel V2 in das Ergebnis gewichtet wird, und der Parameter V steuert, wie viel V3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="0fbdb-140">Schließlich steuert der Wert von 1 – \[ (U + V), \] wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="0fbdb-141">Barycentric-Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="0fbdb-142">In diesem Kontext stellt die Verwendung von baryzentrischen Koordinaten eine Änderung der Koordinatensysteme dar.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="0fbdb-143">Was für kartesische Koordinaten gilt, gilt für baryzentrische Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="0fbdb-144">Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="0fbdb-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="0fbdb-145">Eine detailliertere Beschreibung der baryzentrierten Koordinaten finden Sie unter [Beschreibung der baryzentrierten Koordinaten von Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)</span><span class="sxs-lookup"><span data-stu-id="0fbdb-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fbdb-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fbdb-146">Requirements</span></span>



| <span data-ttu-id="0fbdb-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fbdb-147">Requirement</span></span> | <span data-ttu-id="0fbdb-148">Wert</span><span class="sxs-lookup"><span data-stu-id="0fbdb-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fbdb-149">Header</span><span class="sxs-lookup"><span data-stu-id="0fbdb-149">Header</span></span><br/>  | <dl> <span data-ttu-id="0fbdb-150"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="0fbdb-150"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0fbdb-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0fbdb-151">Library</span></span><br/> | <dl> <span data-ttu-id="0fbdb-152"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fbdb-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0fbdb-153">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0fbdb-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fbdb-154">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="0fbdb-154">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
