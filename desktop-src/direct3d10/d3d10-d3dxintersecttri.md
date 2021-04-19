---
description: Berechnet die Schnittmenge eines Strahls und eines Dreiecks.
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: D3DXIntersectTri-Funktion (D3DX10math. h)
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
ms.openlocfilehash: af96d25b4f13995d60e7926ec5da2d15ff86f282
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370431"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a><span data-ttu-id="3912b-103">D3DXIntersectTri-Funktion (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="3912b-103">D3DXIntersectTri function (D3DX10math.h)</span></span>

<span data-ttu-id="3912b-104">Berechnet die Schnittmenge eines Strahls und eines Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="3912b-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="3912b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3912b-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="3912b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3912b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3912b-107">*P0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3912b-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3912b-108">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3912b-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3912b-109">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die Position des ersten Dreiecks Scheitel Punkts beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3912b-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="3912b-110">*P1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3912b-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3912b-111">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3912b-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3912b-112">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die Position des zweiten Dreiecks Vertex beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3912b-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="3912b-113">*P2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3912b-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3912b-114">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3912b-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3912b-115">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die dritte Position des Dreiecks Vertex beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3912b-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="3912b-116">" *praypos* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="3912b-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3912b-117">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3912b-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3912b-118">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die den Punkt angibt, an dem das Ray beginnt.</span><span class="sxs-lookup"><span data-stu-id="3912b-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="3912b-119">" *praydir* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="3912b-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3912b-120">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3912b-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3912b-121">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="3912b-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="3912b-122">*pU* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3912b-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3912b-123">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3912b-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3912b-124">Baryzentrierte Treffer Koordinaten, U.</span><span class="sxs-lookup"><span data-stu-id="3912b-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="3912b-125">*PV* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3912b-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3912b-126">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3912b-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3912b-127">Für den baryzentrischen Treffer, V.</span><span class="sxs-lookup"><span data-stu-id="3912b-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="3912b-128">*pdist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3912b-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3912b-129">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3912b-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3912b-130">Der Ray-schnittungsparameter.</span><span class="sxs-lookup"><span data-stu-id="3912b-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3912b-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3912b-131">Return value</span></span>

<span data-ttu-id="3912b-132">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3912b-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3912b-133">Gibt " **true** " zurück, wenn das Strahl den Bereich des Dreiecks schneidet.</span><span class="sxs-lookup"><span data-stu-id="3912b-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="3912b-134">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3912b-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3912b-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3912b-135">Remarks</span></span>

<span data-ttu-id="3912b-136">Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (U, V) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3912b-136">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="3912b-137">Mit dem Parameter U wird gesteuert, wie viel v2 in das Ergebnis gewichtet wird, und mit dem Parameter V wird gesteuert, wie viel v3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="3912b-137">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="3912b-138">Schließlich steuert der Wert von \[ 1-(U + V), \] wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="3912b-138">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="3912b-139">Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="3912b-139">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="3912b-140">In diesem Kontext stellt die Verwendung von barzentrischen Koordinaten eine Änderung in Koordinatensystemen dar.</span><span class="sxs-lookup"><span data-stu-id="3912b-140">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="3912b-141">Was für kartesische Koordinaten true ist, ist für barzentrierte Koordinaten "true".</span><span class="sxs-lookup"><span data-stu-id="3912b-141">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="3912b-142">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="3912b-142">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="3912b-143">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="3912b-143">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="3912b-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3912b-144">Requirements</span></span>



| <span data-ttu-id="3912b-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3912b-145">Requirement</span></span> | <span data-ttu-id="3912b-146">Wert</span><span class="sxs-lookup"><span data-stu-id="3912b-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3912b-147">Header</span><span class="sxs-lookup"><span data-stu-id="3912b-147">Header</span></span><br/>  | <dl> <span data-ttu-id="3912b-148"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3912b-148"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="3912b-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3912b-149">Library</span></span><br/> | <dl> <span data-ttu-id="3912b-150"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3912b-150"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3912b-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3912b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3912b-152">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3912b-152">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
