---
description: Verwendet effiziente Ray-Tracing in PRT-Simulationen (preberechneten Radiance Transfer), um zu bestimmen, ob ein Strahl ein Mesh schneidet.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'ID3DXPRTEngine:: closestrayintersekten-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4fd802f636077c9ec2a9f0f1060ffd43493aabf1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219673"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a><span data-ttu-id="43a06-103">ID3DXPRTEngine:: closestrayintersekten-Methode</span><span class="sxs-lookup"><span data-stu-id="43a06-103">ID3DXPRTEngine::ClosestRayIntersects method</span></span>

<span data-ttu-id="43a06-104">Verwendet effiziente Ray-Tracing in PRT-Simulationen (preberechneten Radiance Transfer), um zu bestimmen, ob ein Strahl ein Mesh schneidet.</span><span class="sxs-lookup"><span data-stu-id="43a06-104">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="43a06-105">Wenn eine Schnittmenge gefunden wird, gibt die Methode den Index der nächstgelegenen Mesh-Oberfläche zurück, die vom Strahl und den baryzentrischen Koordinaten des Schnittstellen Punkts getroffen wird.</span><span class="sxs-lookup"><span data-stu-id="43a06-105">If an intersection is found, the method returns the index of the closest mesh face hit by the ray and the barycentric coordinates of the intersection point.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a06-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="43a06-106">Syntax</span></span>


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="43a06-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="43a06-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a06-108">" *praypos* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="43a06-108">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a06-109">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="43a06-109">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="43a06-110">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den Punkt angibt, an dem das Ray beginnt.</span><span class="sxs-lookup"><span data-stu-id="43a06-110">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="43a06-111">" *praydir* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="43a06-111">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a06-112">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="43a06-112">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="43a06-113">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die normalisierte Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="43a06-113">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="43a06-114">*pfakeingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43a06-114">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a06-115">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="43a06-115">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43a06-116">Ein Zeiger auf den Index der aktuellen Gitterfläche, die zuerst vom angegebenen Strahl getroffen wird, basierend auf dem Stapeln aller blocknetz Flächen vor dem aktuellen Mesh.</span><span class="sxs-lookup"><span data-stu-id="43a06-116">Pointer to the index of the current mesh face that is first hit by the given ray, based upon stacking all blocker mesh faces in front of the current mesh.</span></span>

</dd> <dt>

<span data-ttu-id="43a06-117">*pU* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="43a06-117">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43a06-118">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="43a06-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43a06-119">Zeiger auf eine baryzentrierte Treffer Koordinate, U, für Vertex 0 des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="43a06-119">Pointer to a barycentric hit coordinate, U, for vertex 0 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="43a06-120">*PV* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="43a06-120">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43a06-121">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="43a06-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43a06-122">Zeiger auf eine baryzentrierte Treffer Koordinate, V, für Scheitelpunkt 1 des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="43a06-122">Pointer to a barycentric hit coordinate, V, for vertex 1 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="43a06-123">*pdist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="43a06-123">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43a06-124">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="43a06-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43a06-125">Zeiger auf den Abstand des Schnittpunkt entlang des Strahls.</span><span class="sxs-lookup"><span data-stu-id="43a06-125">Pointer to the distance of the intersection point along the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a06-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43a06-126">Return value</span></span>

<span data-ttu-id="43a06-127">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43a06-127">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43a06-128">Gibt " **true** " zurück, wenn der Strahl das aktuelle Mesh überschneidet. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="43a06-128">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="43a06-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43a06-129">Remarks</span></span>

<span data-ttu-id="43a06-130">Verwenden Sie [**ID3DXPRTEngine:: setminmaxschnittstrente**](id3dxprtengine--setminmaxintersection.md) , um den minimalen und maximalen Abstand der Schnittmenge mit dem Ray festzulegen.</span><span class="sxs-lookup"><span data-stu-id="43a06-130">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="43a06-131">Die barzentrische Koordinate des dritten Vertex (Vertex 2) des Dreiecks ist 1-(U + V).</span><span class="sxs-lookup"><span data-stu-id="43a06-131">The barycentric coordinate of the third vertex (vertex 2) of the triangle is 1 - ( U + V ).</span></span>

<span data-ttu-id="43a06-132">Diese Methode wird langsamer ausgeführt als [**ID3DXPRTEngine:: shadowrayintersekten**](id3dxprtengine--shadowrayintersects.md).</span><span class="sxs-lookup"><span data-stu-id="43a06-132">This method executes slower than [**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md).</span></span> <span data-ttu-id="43a06-133">Verwenden Sie **ID3DXPRTEngine:: shadowrayintersekten** , wenn die Position des Schnitt Punkts nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="43a06-133">Use **ID3DXPRTEngine::ShadowRayIntersects** if the location of the intersection point is not needed.</span></span>

<span data-ttu-id="43a06-134">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="43a06-134">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="43a06-135">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="43a06-135">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="43a06-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43a06-136">Requirements</span></span>



| <span data-ttu-id="43a06-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43a06-137">Requirement</span></span> | <span data-ttu-id="43a06-138">Wert</span><span class="sxs-lookup"><span data-stu-id="43a06-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43a06-139">Header</span><span class="sxs-lookup"><span data-stu-id="43a06-139">Header</span></span><br/>  | <dl> <span data-ttu-id="43a06-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a06-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="43a06-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43a06-141">Library</span></span><br/> | <dl> <span data-ttu-id="43a06-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43a06-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43a06-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43a06-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a06-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="43a06-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="43a06-145">**ID3DXPRTEngine:: shadowrayintersekten**</span><span class="sxs-lookup"><span data-stu-id="43a06-145">**ID3DXPRTEngine::ShadowRayIntersects**</span></span>](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[<span data-ttu-id="43a06-146">**ID3DXPRTEngine:: setminmaxschnitt Menge**</span><span class="sxs-lookup"><span data-stu-id="43a06-146">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
