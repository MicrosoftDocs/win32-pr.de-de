---
description: Bestimmt, ob sich ein Strahl mit einem Mesh schneidet.
ms.assetid: 325f5b40-80ba-4400-a143-bae41146ab07
title: D3DXIntersect-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc877fb1301e01b05184625ba2e92a2c680cfa9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366461"
---
# <a name="d3dxintersect-function"></a><span data-ttu-id="f0793-103">D3DXIntersect-Funktion</span><span class="sxs-lookup"><span data-stu-id="f0793-103">D3DXIntersect function</span></span>

<span data-ttu-id="f0793-104">Bestimmt, ob sich ein Strahl mit einem Mesh schneidet.</span><span class="sxs-lookup"><span data-stu-id="f0793-104">Determines if a ray intersects with a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0793-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0793-105">Syntax</span></span>


```C++
HRESULT D3DXIntersect(
  _In_        LPD3DXBASEMESH pMesh,
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



## <a name="parameters"></a><span data-ttu-id="f0793-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0793-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0793-107">*pmesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0793-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0793-108">Typ: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="f0793-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="f0793-109">Zeiger auf eine [**ID3DXBaseMesh**](id3dxbasemesh.md) -Schnittstelle, die das zu testende Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="f0793-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="f0793-110">" *praypos* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="f0793-110">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0793-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0793-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f0793-112">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den Punkt angibt, an dem das Ray beginnt.</span><span class="sxs-lookup"><span data-stu-id="f0793-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="f0793-113">" *praydir* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="f0793-113">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0793-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0793-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f0793-115">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="f0793-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="f0793-116">*Phit* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0793-116">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0793-117">Typ: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0793-117">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f0793-118">Zeiger auf einen booleschen Werten.</span><span class="sxs-lookup"><span data-stu-id="f0793-118">Pointer to a BOOL.</span></span> <span data-ttu-id="f0793-119">Wenn das Strahl eine Dreiecksfläche im Mesh schneidet, wird dieser Wert auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f0793-119">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="f0793-120">Andernfalls wird dieser Wert auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f0793-120">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f0793-121">*pfakeingedex* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0793-121">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0793-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0793-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f0793-123">Zeiger auf einen Indexwert der Oberfläche, die dem Ray-Ursprung am nächsten ist, wenn Phit **true** ist.</span><span class="sxs-lookup"><span data-stu-id="f0793-123">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="f0793-124">*pU* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0793-124">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0793-125">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0793-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f0793-126">Zeiger auf eine baryzentrierte Treffer Koordinate, U.</span><span class="sxs-lookup"><span data-stu-id="f0793-126">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="f0793-127">*PV* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0793-127">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0793-128">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0793-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f0793-129">Zeiger auf eine baryzentrierte Treffer Koordinate, V.</span><span class="sxs-lookup"><span data-stu-id="f0793-129">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="f0793-130">*pdist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0793-130">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0793-131">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0793-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f0793-132">Zeiger auf eine Strahl Schnittstellen-Parameter Entfernung.</span><span class="sxs-lookup"><span data-stu-id="f0793-132">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="f0793-133">*ppallhits* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0793-133">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0793-134">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0793-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="f0793-135">Zeiger auf ein [**ID3DXBuffer**](id3dxbuffer.md) -Objekt, das ein Array von [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) -Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="f0793-135">Pointer to an [**ID3DXBuffer**](id3dxbuffer.md) object, containing an array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="f0793-136">*pgräfin-Steuer Treffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f0793-136">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0793-137">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0793-137">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f0793-138">Zeiger auf ein DWORD, das die Anzahl der Einträge im ppallhits-Array enthält.</span><span class="sxs-lookup"><span data-stu-id="f0793-138">Pointer to a DWORD that contains the number of entries in the ppAllHits array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0793-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0793-139">Return value</span></span>

<span data-ttu-id="f0793-140">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f0793-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f0793-141">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f0793-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f0793-142">Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: E \_ outo-Memory.</span><span class="sxs-lookup"><span data-stu-id="f0793-142">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0793-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0793-143">Remarks</span></span>

<span data-ttu-id="f0793-144">Die **D3DXIntersect** -Funktion bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet.</span><span class="sxs-lookup"><span data-stu-id="f0793-144">The **D3DXIntersect** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="f0793-145">Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: v1 + U (V2-V1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="f0793-145">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="f0793-146">Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (U, V) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f0793-146">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="f0793-147">Mit dem Parameter U wird gesteuert, wie viel v2 in das Ergebnis gewichtet wird, und mit dem Parameter V wird gesteuert, wie viel v3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="f0793-147">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="f0793-148">Schließlich steuert der Wert von \[ 1-(U + V), \] wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="f0793-148">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="f0793-149">Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="f0793-149">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="f0793-150">In diesem Kontext stellt die Verwendung von barzentrischen Koordinaten eine Änderung in Koordinatensystemen dar.</span><span class="sxs-lookup"><span data-stu-id="f0793-150">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="f0793-151">Was für kartesische Koordinaten true ist, ist für barzentrierte Koordinaten "true".</span><span class="sxs-lookup"><span data-stu-id="f0793-151">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="f0793-152">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="f0793-152">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="f0793-153">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="f0793-153">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0793-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0793-154">Requirements</span></span>



| <span data-ttu-id="f0793-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0793-155">Requirement</span></span> | <span data-ttu-id="f0793-156">Wert</span><span class="sxs-lookup"><span data-stu-id="f0793-156">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0793-157">Header</span><span class="sxs-lookup"><span data-stu-id="f0793-157">Header</span></span><br/>  | <dl> <span data-ttu-id="f0793-158"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0793-158"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f0793-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0793-159">Library</span></span><br/> | <dl> <span data-ttu-id="f0793-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0793-160"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f0793-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0793-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0793-162">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="f0793-162">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
