---
description: Verwendet effiziente Ray-Tracing in PRT-Simulationen (preberechneten Radiance Transfer), um zu bestimmen, ob ein Strahl ein Mesh schneidet. Wird normalerweise verwendet, um zu bestimmen, ob ein bestimmter Punkt im Schatten ist.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'ID3DXPRTEngine:: shadowrayintersekten-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 701aa4c89ee6a9d657721d872565c9b2056bb435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050877"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a><span data-ttu-id="5c5ba-104">ID3DXPRTEngine:: shadowrayintersekten-Methode</span><span class="sxs-lookup"><span data-stu-id="5c5ba-104">ID3DXPRTEngine::ShadowRayIntersects method</span></span>

<span data-ttu-id="5c5ba-105">Verwendet effiziente Ray-Tracing in PRT-Simulationen (preberechneten Radiance Transfer), um zu bestimmen, ob ein Strahl ein Mesh schneidet.</span><span class="sxs-lookup"><span data-stu-id="5c5ba-105">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="5c5ba-106">Wird normalerweise verwendet, um zu bestimmen, ob ein bestimmter Punkt im Schatten ist.</span><span class="sxs-lookup"><span data-stu-id="5c5ba-106">Typically used to determine whether a given point is in shadow.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c5ba-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c5ba-107">Syntax</span></span>


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
);
```



## <a name="parameters"></a><span data-ttu-id="5c5ba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c5ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c5ba-109">" *praypos* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="5c5ba-109">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c5ba-110">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5c5ba-110">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5c5ba-111">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den Punkt angibt, an dem das Ray beginnt.</span><span class="sxs-lookup"><span data-stu-id="5c5ba-111">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="5c5ba-112">" *praydir* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="5c5ba-112">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c5ba-113">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5c5ba-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5c5ba-114">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die normalisierte Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="5c5ba-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c5ba-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c5ba-115">Return value</span></span>

<span data-ttu-id="5c5ba-116">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c5ba-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c5ba-117">Gibt " **true** " zurück, wenn der Strahl das aktuelle Mesh überschneidet. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5c5ba-117">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c5ba-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c5ba-118">Remarks</span></span>

<span data-ttu-id="5c5ba-119">Verwenden Sie [**ID3DXPRTEngine:: setminmaxschnittstrente**](id3dxprtengine--setminmaxintersection.md) , um den minimalen und maximalen Abstand der Schnittmenge mit dem Ray festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5c5ba-119">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="5c5ba-120">Diese Methode wird schneller ausgeführt als [**ID3DXPRTEngine:: closestrayintersekten**](id3dxprtengine--closestrayintersects.md).</span><span class="sxs-lookup"><span data-stu-id="5c5ba-120">This method executes faster than [**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c5ba-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c5ba-121">Requirements</span></span>



| <span data-ttu-id="5c5ba-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c5ba-122">Requirement</span></span> | <span data-ttu-id="5c5ba-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5c5ba-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c5ba-124">Header</span><span class="sxs-lookup"><span data-stu-id="5c5ba-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5c5ba-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c5ba-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5c5ba-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5c5ba-126">Library</span></span><br/> | <dl> <span data-ttu-id="5c5ba-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c5ba-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5c5ba-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c5ba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c5ba-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="5c5ba-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="5c5ba-130">**ID3DXPRTEngine:: closestrayintersekten**</span><span class="sxs-lookup"><span data-stu-id="5c5ba-130">**ID3DXPRTEngine::ClosestRayIntersects**</span></span>](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[<span data-ttu-id="5c5ba-131">**ID3DXPRTEngine:: setminmaxschnitt Menge**</span><span class="sxs-lookup"><span data-stu-id="5c5ba-131">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
