---
description: 'D3DXSphereBoundProbe-Funktion (D3DX10math.h): Bestimmt, ob ein Strahl das Volumen des umgebenden Felds einer Kugel überschneidet.'
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: D3DXSphereBoundProbe-Funktion (D3DX10math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fb5a329e39631dff626ff1c7945ad4b05f9dcd58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108468"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a><span data-ttu-id="6ac7b-103">D3DXSphereBoundProbe-Funktion (D3DX10math.h)</span><span class="sxs-lookup"><span data-stu-id="6ac7b-103">D3DXSphereBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="6ac7b-104">Bestimmt, ob ein Strahl das Volumen des umgebenden Felds einer Kugel überschneidet.</span><span class="sxs-lookup"><span data-stu-id="6ac7b-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac7b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ac7b-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="6ac7b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ac7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ac7b-107">*pCenter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6ac7b-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac7b-108">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ac7b-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6ac7b-109">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die Mittelpunktkoordinate der Kugel angibt.</span><span class="sxs-lookup"><span data-stu-id="6ac7b-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="6ac7b-110">*Radius* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6ac7b-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac7b-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ac7b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ac7b-112">Radius der Kugel.</span><span class="sxs-lookup"><span data-stu-id="6ac7b-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="6ac7b-113">*pRayPosition* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6ac7b-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac7b-114">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ac7b-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6ac7b-115">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die Ursprungskoordinate des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="6ac7b-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="6ac7b-116">*pRayDirection* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6ac7b-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac7b-117">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ac7b-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6ac7b-118">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="6ac7b-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="6ac7b-119">Dieser Vektor sollte nicht (0,0,0) sein, muss aber nicht normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6ac7b-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ac7b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ac7b-120">Return value</span></span>

<span data-ttu-id="6ac7b-121">Typ: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ac7b-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ac7b-122">Gibt **TRUE** zurück, wenn der Strahl das Volumen des umgebenden Felds der Kugel überschneidet.</span><span class="sxs-lookup"><span data-stu-id="6ac7b-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="6ac7b-123">Andernfalls gibt **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="6ac7b-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ac7b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ac7b-124">Remarks</span></span>

<span data-ttu-id="6ac7b-125">**D3DXSphereBoundProbe** bestimmt, ob der Strahl das Volumen des Begrenzungsfelds der Kugel überschneidet, nicht nur die Oberfläche der Kugel.</span><span class="sxs-lookup"><span data-stu-id="6ac7b-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ac7b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ac7b-126">Requirements</span></span>



| <span data-ttu-id="6ac7b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ac7b-127">Requirement</span></span> | <span data-ttu-id="6ac7b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6ac7b-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac7b-129">Header</span><span class="sxs-lookup"><span data-stu-id="6ac7b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6ac7b-130"><dt>D3DX10math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6ac7b-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="6ac7b-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6ac7b-131">Library</span></span><br/> | <dl> <span data-ttu-id="6ac7b-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ac7b-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ac7b-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6ac7b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac7b-134">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="6ac7b-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
