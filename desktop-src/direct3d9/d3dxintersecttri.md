---
description: Berechnet die Schnittmenge eines Strahls und eines Dreiecks.
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: D3DXIntersectTri-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 41c7012cea0a533dc447db0575def6b418d0e59e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363137"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a><span data-ttu-id="1b8e1-103">D3DXIntersectTri-Funktion (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="1b8e1-103">D3DXIntersectTri function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="1b8e1-104">Berechnet die Schnittmenge eines Strahls und eines Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b8e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b8e1-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1b8e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b8e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b8e1-107">*P0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b8e1-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8e1-108">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1b8e1-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1b8e1-109">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Position des ersten Dreiecks Scheitel Punkts beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="1b8e1-110">*P1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b8e1-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8e1-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1b8e1-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1b8e1-112">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Position des zweiten Dreiecks Vertex beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="1b8e1-113">*P2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b8e1-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8e1-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1b8e1-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1b8e1-115">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die dritte Position des Dreiecks Vertex beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="1b8e1-116">" *praypos* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="1b8e1-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8e1-117">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1b8e1-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1b8e1-118">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den Punkt angibt, an dem das Ray beginnt.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="1b8e1-119">" *praydir* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="1b8e1-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8e1-120">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1b8e1-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1b8e1-121">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="1b8e1-122">*pU* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b8e1-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8e1-123">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b8e1-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1b8e1-124">Baryzentrierte Treffer Koordinaten, U.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="1b8e1-125">*PV* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b8e1-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8e1-126">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b8e1-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1b8e1-127">Für den baryzentrischen Treffer, V.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="1b8e1-128">*pdist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b8e1-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8e1-129">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b8e1-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1b8e1-130">Der Ray-schnittungsparameter.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b8e1-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b8e1-131">Return value</span></span>

<span data-ttu-id="1b8e1-132">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b8e1-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b8e1-133">Gibt " **true** " zurück, wenn das Strahl den Bereich des Dreiecks schneidet.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="1b8e1-134">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b8e1-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b8e1-135">Remarks</span></span>

<span data-ttu-id="1b8e1-136">Die [**D3DXIntersect**](d3dxintersect.md) -Funktion bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-136">The [**D3DXIntersect**](d3dxintersect.md) function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="1b8e1-137">Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: v1 + U (V2-V1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="1b8e1-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="1b8e1-138">Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (U, V) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="1b8e1-139">Mit dem Parameter U wird gesteuert, wie viel v2 in das Ergebnis gewichtet wird, und mit dem Parameter V wird gesteuert, wie viel v3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="1b8e1-140">Schließlich steuert der Wert von \[ 1-(U + V), \] wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="1b8e1-141">Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="1b8e1-142">In diesem Kontext stellt die Verwendung von barzentrischen Koordinaten eine Änderung in Koordinatensystemen dar.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="1b8e1-143">Was für kartesische Koordinaten true ist, ist für barzentrierte Koordinaten "true".</span><span class="sxs-lookup"><span data-stu-id="1b8e1-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="1b8e1-144">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="1b8e1-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="1b8e1-145">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="1b8e1-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b8e1-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b8e1-146">Requirements</span></span>



| <span data-ttu-id="1b8e1-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b8e1-147">Requirement</span></span> | <span data-ttu-id="1b8e1-148">Wert</span><span class="sxs-lookup"><span data-stu-id="1b8e1-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8e1-149">Header</span><span class="sxs-lookup"><span data-stu-id="1b8e1-149">Header</span></span><br/>  | <dl> <span data-ttu-id="1b8e1-150"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b8e1-150"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1b8e1-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1b8e1-151">Library</span></span><br/> | <dl> <span data-ttu-id="1b8e1-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b8e1-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1b8e1-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b8e1-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b8e1-154">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1b8e1-154">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
