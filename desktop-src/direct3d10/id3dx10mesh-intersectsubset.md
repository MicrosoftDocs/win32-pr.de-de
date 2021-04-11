---
description: Bestimmt, ob sich ein Strahl mit einer Teilmenge dieses Netzes schneidet.
ms.assetid: 31f90141-60be-4c7f-8d6a-a1a97ff26d9d
title: ID3DX10Mesh::IntersectSubset-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.IntersectSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a08d4db92dc75f40d0073367dda9a9ea26863418
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219613"
---
# <a name="id3dx10meshintersectsubset-method"></a><span data-ttu-id="16254-103">ID3DX10Mesh:: intersectsubset-Methode</span><span class="sxs-lookup"><span data-stu-id="16254-103">ID3DX10Mesh::IntersectSubset method</span></span>

<span data-ttu-id="16254-104">Bestimmt, ob sich ein Strahl mit einer Teilmenge dieses Netzes schneidet.</span><span class="sxs-lookup"><span data-stu-id="16254-104">Determines if a ray intersects with a subset of this mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="16254-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="16254-105">Syntax</span></span>


```C++
HRESULT IntersectSubset(
  [in]  UINT        AttribId,
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a><span data-ttu-id="16254-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="16254-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16254-107">*Atungbid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16254-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16254-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16254-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16254-109">Attribut-ID, die die Teilmenge des Netzes identifiziert.</span><span class="sxs-lookup"><span data-stu-id="16254-109">Attribute ID identifying the subset of the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="16254-110">" *praypos* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="16254-110">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16254-111">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="16254-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="16254-112">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die den Punkt angibt, an dem das Ray beginnt.</span><span class="sxs-lookup"><span data-stu-id="16254-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="16254-113">" *praydir* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="16254-113">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16254-114">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="16254-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="16254-115">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="16254-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="16254-116">*phitcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16254-116">*pHitCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16254-117">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="16254-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="16254-118">Gibt an, wie oft sich der Strahl mit dem Mesh interniert hat.</span><span class="sxs-lookup"><span data-stu-id="16254-118">The number of times the ray intersected with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="16254-119">*pfakeingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16254-119">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16254-120">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="16254-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="16254-121">Zeiger auf einen Indexwert der Oberfläche, die dem Ray-Ursprung am nächsten ist, wenn Phit **true** ist.</span><span class="sxs-lookup"><span data-stu-id="16254-121">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="16254-122">*pU* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16254-122">*pU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16254-123">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="16254-123">Type: **float\***</span></span>

<span data-ttu-id="16254-124">Zeiger auf eine baryzentrierte Treffer Koordinate, U.</span><span class="sxs-lookup"><span data-stu-id="16254-124">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="16254-125">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16254-125">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16254-126">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="16254-126">Type: **float\***</span></span>

<span data-ttu-id="16254-127">Zeiger auf eine baryzentrierte Treffer Koordinate, V.</span><span class="sxs-lookup"><span data-stu-id="16254-127">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="16254-128">*pdist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16254-128">*pDist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16254-129">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="16254-129">Type: **float\***</span></span>

<span data-ttu-id="16254-130">Zeiger auf eine Strahl Schnittstellen-Parameter Entfernung.</span><span class="sxs-lookup"><span data-stu-id="16254-130">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="16254-131">*ppallhits* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="16254-131">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16254-132">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="16254-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="16254-133">Zeiger auf eine [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), die ein Array von [**d3dx10 \_ Intersect \_ Info**](d3dx10-intersect-info.md) -Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="16254-133">Pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), containing an array of [**D3DX10\_INTERSECT\_INFO**](d3dx10-intersect-info.md) structures.</span></span> <span data-ttu-id="16254-134">Dies ist eine Liste aller Treffer, die im schnittschnitttest aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="16254-134">This is a list of all the hits that occurred in the intersection test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16254-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16254-135">Return value</span></span>

<span data-ttu-id="16254-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="16254-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="16254-137">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="16254-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="16254-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16254-138">Remarks</span></span>

<span data-ttu-id="16254-139">Diese API bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet.</span><span class="sxs-lookup"><span data-stu-id="16254-139">This API provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="16254-140">Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: v1 + U (V2-V1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="16254-140">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="16254-141">Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (U, V) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="16254-141">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="16254-142">Mit dem Parameter U wird gesteuert, wie viel v2 in das Ergebnis gewichtet wird, und mit dem Parameter V wird gesteuert, wie viel v3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="16254-142">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="16254-143">Schließlich steuert der Wert von \[ 1-(U + V), \] wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="16254-143">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="16254-144">Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="16254-144">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="16254-145">In diesem Kontext stellt die Verwendung von barzentrischen Koordinaten eine Änderung in Koordinatensystemen dar.</span><span class="sxs-lookup"><span data-stu-id="16254-145">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="16254-146">Was für kartesische Koordinaten true ist, ist für barzentrierte Koordinaten "true".</span><span class="sxs-lookup"><span data-stu-id="16254-146">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="16254-147">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="16254-147">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="16254-148">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="16254-148">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="16254-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16254-149">Requirements</span></span>



| <span data-ttu-id="16254-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16254-150">Requirement</span></span> | <span data-ttu-id="16254-151">Wert</span><span class="sxs-lookup"><span data-stu-id="16254-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16254-152">Header</span><span class="sxs-lookup"><span data-stu-id="16254-152">Header</span></span><br/>  | <dl> <span data-ttu-id="16254-153"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="16254-153"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="16254-154">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="16254-154">Library</span></span><br/> | <dl> <span data-ttu-id="16254-155"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16254-155"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16254-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16254-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16254-157">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="16254-157">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="16254-158">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="16254-158">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
