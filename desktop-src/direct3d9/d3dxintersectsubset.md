---
description: Schneidet das angegebene Ray mit der angegebenen Mesh-Teilmenge ab. Dies bietet eine ähnliche Funktionalität wie D3DXIntersect.
ms.assetid: 4a757b9e-18eb-424e-9f3e-cdf917c23787
title: D3DXIntersectSubset-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectSubset
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 621f45d7c2a6d8ff162f539ef62153d3ae70f6e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219509"
---
# <a name="d3dxintersectsubset-function"></a><span data-ttu-id="bd736-104">D3DXIntersectSubset-Funktion</span><span class="sxs-lookup"><span data-stu-id="bd736-104">D3DXIntersectSubset function</span></span>

<span data-ttu-id="bd736-105">Schneidet das angegebene Ray mit der angegebenen Mesh-Teilmenge ab.</span><span class="sxs-lookup"><span data-stu-id="bd736-105">Intersects the specified ray with the given mesh subset.</span></span> <span data-ttu-id="bd736-106">Dies bietet eine ähnliche Funktionalität wie [**D3DXIntersect**](d3dxintersect.md).</span><span class="sxs-lookup"><span data-stu-id="bd736-106">This provides similar functionality to [**D3DXIntersect**](d3dxintersect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd736-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd736-107">Syntax</span></span>


```C++
HRESULT D3DXIntersectSubset(
  _In_        LPD3DXBASEMESH pMesh,
  _In_        DWORD          AttribId,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a><span data-ttu-id="bd736-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd736-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd736-109">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd736-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd736-110">Typ: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="bd736-110">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="bd736-111">Zeiger auf eine [**ID3DXBaseMesh**](id3dxbasemesh.md) -Schnittstelle, die das zu testende Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="bd736-111">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span> <span data-ttu-id="bd736-112">Das Mesh muss Attribut sortiert sein.</span><span class="sxs-lookup"><span data-stu-id="bd736-112">The mesh must be attribute sorted.</span></span>

</dd> <dt>

<span data-ttu-id="bd736-113">*Atungbid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd736-113">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd736-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd736-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd736-115">Der Attribut Bezeichner der Teilmenge, mit der Intersect werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd736-115">Attribute identifier of the subset to intersect with.</span></span>

</dd> <dt>

<span data-ttu-id="bd736-116">" *praypos* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="bd736-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd736-117">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bd736-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bd736-118">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den Punkt angibt, an dem das Ray beginnt.</span><span class="sxs-lookup"><span data-stu-id="bd736-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="bd736-119">" *praydir* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="bd736-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd736-120">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bd736-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bd736-121">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="bd736-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="bd736-122">*Phit* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd736-122">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd736-123">Typ: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd736-123">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bd736-124">Zeiger auf einen booleschen Werten.</span><span class="sxs-lookup"><span data-stu-id="bd736-124">Pointer to a BOOL.</span></span> <span data-ttu-id="bd736-125">Wenn das Strahl eine Dreiecksfläche im Mesh schneidet, wird dieser Wert auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bd736-125">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="bd736-126">Andernfalls wird dieser Wert auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bd736-126">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bd736-127">*pfakeingedex* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd736-127">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd736-128">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd736-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bd736-129">Zeiger auf einen Indexwert der Oberfläche, die dem Ray-Ursprung am nächsten ist, wenn Phit **true** ist.</span><span class="sxs-lookup"><span data-stu-id="bd736-129">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="bd736-130">*pU* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd736-130">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd736-131">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd736-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bd736-132">Zeiger auf eine baryzentrierte Treffer Koordinate, U.</span><span class="sxs-lookup"><span data-stu-id="bd736-132">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="bd736-133">*PV* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd736-133">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd736-134">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd736-134">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bd736-135">Zeiger auf eine baryzentrierte Treffer Koordinate, V.</span><span class="sxs-lookup"><span data-stu-id="bd736-135">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="bd736-136">*pdist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd736-136">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd736-137">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd736-137">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bd736-138">Zeiger auf eine Strahl Schnittstellen-Parameter Entfernung.</span><span class="sxs-lookup"><span data-stu-id="bd736-138">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="bd736-139">*ppallhits* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd736-139">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd736-140">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd736-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bd736-141">Ein Array von [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) -Strukturen, das alle Treffer darstellt, nicht nur die nächstgelegenen Treffer.</span><span class="sxs-lookup"><span data-stu-id="bd736-141">Array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures, representing all hits, not just closest hits.</span></span>

</dd> <dt>

<span data-ttu-id="bd736-142">*pgräfin-Steuer Treffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd736-142">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd736-143">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd736-143">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bd736-144">Anzahl von Elementen im Array, die von ppallhits zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bd736-144">Number of elements in the array returned from ppAllHits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd736-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd736-145">Return value</span></span>

<span data-ttu-id="bd736-146">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bd736-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bd736-147">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bd736-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bd736-148">Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Wert sein: E \_ outo-Memory.</span><span class="sxs-lookup"><span data-stu-id="bd736-148">If the function fails, the return value can be the following value: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd736-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd736-149">Remarks</span></span>

<span data-ttu-id="bd736-150">Die **D3DXIntersectSubset** -Funktion bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet.</span><span class="sxs-lookup"><span data-stu-id="bd736-150">The **D3DXIntersectSubset** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="bd736-151">Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: v1 + U (V2-V1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="bd736-151">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="bd736-152">Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (U, V) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="bd736-152">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="bd736-153">Mit dem Parameter U wird gesteuert, wie viel v2 in das Ergebnis gewichtet wird. mit dem Parameter V wird gesteuert, wie viel v3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="bd736-153">The parameter U controls how much V2 gets weighted into the result and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="bd736-154">Schließlich steuert der Wert von \[ 1-(U + V), \] wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="bd736-154">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="bd736-155">Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="bd736-155">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="bd736-156">In diesem Kontext stellt die Verwendung von barzentrischen Koordinaten eine Änderung in Koordinatensystemen dar.</span><span class="sxs-lookup"><span data-stu-id="bd736-156">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="bd736-157">Was für kartesische Koordinaten true ist, ist für barzentrierte Koordinaten "true".</span><span class="sxs-lookup"><span data-stu-id="bd736-157">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="bd736-158">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="bd736-158">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="bd736-159">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="bd736-159">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd736-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd736-160">Requirements</span></span>



| <span data-ttu-id="bd736-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd736-161">Requirement</span></span> | <span data-ttu-id="bd736-162">Wert</span><span class="sxs-lookup"><span data-stu-id="bd736-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd736-163">Header</span><span class="sxs-lookup"><span data-stu-id="bd736-163">Header</span></span><br/>  | <dl> <span data-ttu-id="bd736-164"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd736-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bd736-165">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bd736-165">Library</span></span><br/> | <dl> <span data-ttu-id="bd736-166"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd736-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bd736-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd736-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd736-168">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="bd736-168">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
