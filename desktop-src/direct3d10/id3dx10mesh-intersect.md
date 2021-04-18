---
description: Bestimmt, ob sich ein Strahl mit diesem Mesh schneidet.
ms.assetid: 74565d4a-94e6-4faa-bf70-9c1b35e5e5d8
title: ID3DX10Mesh::Intersect-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Intersect
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8ceed03ab21debf61371da9e53b5150d2dc83e4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365094"
---
# <a name="id3dx10meshintersect-method"></a><span data-ttu-id="8151e-103">ID3DX10Mesh:: Intersect-Methode</span><span class="sxs-lookup"><span data-stu-id="8151e-103">ID3DX10Mesh::Intersect method</span></span>

<span data-ttu-id="8151e-104">Bestimmt, ob sich ein Strahl mit diesem Mesh schneidet.</span><span class="sxs-lookup"><span data-stu-id="8151e-104">Determines if a ray intersects with this mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="8151e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8151e-105">Syntax</span></span>


```C++
HRESULT Intersect(
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



## <a name="parameters"></a><span data-ttu-id="8151e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8151e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8151e-107">" *praypos* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="8151e-107">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8151e-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="8151e-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8151e-109">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die den Punkt angibt, an dem das Ray beginnt.</span><span class="sxs-lookup"><span data-stu-id="8151e-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="8151e-110">" *praydir* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="8151e-110">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8151e-111">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="8151e-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8151e-112">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="8151e-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="8151e-113">*phitcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8151e-113">*pHitCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8151e-114">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8151e-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8151e-115">Gibt an, wie oft sich der Strahl mit dem Mesh interniert hat.</span><span class="sxs-lookup"><span data-stu-id="8151e-115">The number of times the ray intersected with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8151e-116">*pfakeingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8151e-116">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8151e-117">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8151e-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8151e-118">Zeiger auf einen Indexwert der Oberfläche, die dem Ray-Ursprung am nächsten ist, wenn Phit **true** ist.</span><span class="sxs-lookup"><span data-stu-id="8151e-118">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="8151e-119">*pU* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8151e-119">*pU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8151e-120">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="8151e-120">Type: **float\***</span></span>

<span data-ttu-id="8151e-121">Zeiger auf eine baryzentrierte Treffer Koordinate, U.</span><span class="sxs-lookup"><span data-stu-id="8151e-121">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="8151e-122">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8151e-122">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8151e-123">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="8151e-123">Type: **float\***</span></span>

<span data-ttu-id="8151e-124">Zeiger auf eine baryzentrierte Treffer Koordinate, V.</span><span class="sxs-lookup"><span data-stu-id="8151e-124">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="8151e-125">*pdist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8151e-125">*pDist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8151e-126">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="8151e-126">Type: **float\***</span></span>

<span data-ttu-id="8151e-127">Zeiger auf eine Strahl Schnittstellen-Parameter Entfernung.</span><span class="sxs-lookup"><span data-stu-id="8151e-127">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="8151e-128">*ppallhits* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8151e-128">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8151e-129">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="8151e-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="8151e-130">Zeiger auf eine [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), die ein Array von [**d3dx10 \_ Intersect \_ Info**](d3dx10-intersect-info.md) -Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="8151e-130">Pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), containing an array of [**D3DX10\_INTERSECT\_INFO**](d3dx10-intersect-info.md) structures.</span></span> <span data-ttu-id="8151e-131">Dies ist eine Liste aller Treffer, die im schnittschnitttest aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="8151e-131">This is a list of all the hits that occurred in the intersection test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8151e-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8151e-132">Return value</span></span>

<span data-ttu-id="8151e-133">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8151e-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8151e-134">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="8151e-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8151e-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8151e-135">Remarks</span></span>

<span data-ttu-id="8151e-136">Diese API bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet.</span><span class="sxs-lookup"><span data-stu-id="8151e-136">This API provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="8151e-137">Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: v1 + U (V2-V1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="8151e-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="8151e-138">Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (U, V) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8151e-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="8151e-139">Mit dem Parameter U wird gesteuert, wie viel v2 in das Ergebnis gewichtet wird, und mit dem Parameter V wird gesteuert, wie viel v3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="8151e-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="8151e-140">Schließlich steuert der Wert von \[ 1-(U + V), \] wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="8151e-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="8151e-141">Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="8151e-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="8151e-142">In diesem Kontext stellt die Verwendung von barzentrischen Koordinaten eine Änderung in Koordinatensystemen dar.</span><span class="sxs-lookup"><span data-stu-id="8151e-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="8151e-143">Was für kartesische Koordinaten true ist, ist für barzentrierte Koordinaten "true".</span><span class="sxs-lookup"><span data-stu-id="8151e-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="8151e-144">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="8151e-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="8151e-145">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="8151e-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="8151e-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8151e-146">Requirements</span></span>



| <span data-ttu-id="8151e-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8151e-147">Requirement</span></span> | <span data-ttu-id="8151e-148">Wert</span><span class="sxs-lookup"><span data-stu-id="8151e-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8151e-149">Header</span><span class="sxs-lookup"><span data-stu-id="8151e-149">Header</span></span><br/>  | <dl> <span data-ttu-id="8151e-150"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8151e-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8151e-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8151e-151">Library</span></span><br/> | <dl> <span data-ttu-id="8151e-152"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8151e-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8151e-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8151e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8151e-154">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="8151e-154">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="8151e-155">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8151e-155">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
