---
description: Die D3DXBoxBoundProbe-Funktion (D3DX10math. h) bestimmt, ob ein Strahl das Volume des Begrenzungs Rahmens eines Felds schneidet.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: D3DXBoxBoundProbe-Funktion (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1a8d1a7b879814cff43e31b060cc2af53167818
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106358187"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a><span data-ttu-id="06c10-103">D3DXBoxBoundProbe-Funktion (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="06c10-103">D3DXBoxBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="06c10-104">Bestimmt, ob ein Strahl das Volume des umgebenden Felds eines Felds schneidet.</span><span class="sxs-lookup"><span data-stu-id="06c10-104">Determines whether a ray intersects the volume of a box's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c10-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06c10-105">Syntax</span></span>


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="06c10-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06c10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c10-107">*Pmin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06c10-107">*pMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c10-108">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="06c10-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="06c10-109">Ein Zeiger auf einen [**D3DXVECTOR3**](d3d10-d3dxvector3.md), der die untere linke Ecke des umgebenden Felds beschreibt.</span><span class="sxs-lookup"><span data-stu-id="06c10-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), describing the lower-left corner of the bounding box.</span></span> <span data-ttu-id="06c10-110">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="06c10-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="06c10-111">*pmax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06c10-111">*pMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c10-112">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="06c10-112">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="06c10-113">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die obere rechte Ecke des Begrenzungs Rahmens beschreibt.</span><span class="sxs-lookup"><span data-stu-id="06c10-113">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the upper-right corner of the bounding box.</span></span> <span data-ttu-id="06c10-114">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="06c10-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="06c10-115">" *prayposition* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="06c10-115">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c10-116">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="06c10-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="06c10-117">Zeiger auf eine D3DXVECTOR3-Struktur, die die Ursprungs Koordinate des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="06c10-117">Pointer to a D3DXVECTOR3 structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="06c10-118">" *praydirection* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="06c10-118">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c10-119">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="06c10-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="06c10-120">Zeiger auf eine D3DXVECTOR3-Struktur, die die Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="06c10-120">Pointer to a D3DXVECTOR3 structure, specifying the direction of the ray.</span></span> <span data-ttu-id="06c10-121">Dieser Vektor sollte nicht (0, 0, 0) sein, muss jedoch nicht normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="06c10-121">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c10-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06c10-122">Return value</span></span>

<span data-ttu-id="06c10-123">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06c10-123">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06c10-124">Gibt " **true** " zurück, wenn der Strahl das Volume des umgebenden Felds der Box schneidet.</span><span class="sxs-lookup"><span data-stu-id="06c10-124">Returns **TRUE** if the ray intersects the volume of the box's bounding box.</span></span> <span data-ttu-id="06c10-125">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06c10-125">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="06c10-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06c10-126">Remarks</span></span>

<span data-ttu-id="06c10-127">**D3DXBoxBoundProbe** bestimmt, ob der Strahl das Volume des umgebenden Felds der Box, nicht nur die Oberfläche des Felds, schneidet.</span><span class="sxs-lookup"><span data-stu-id="06c10-127">**D3DXBoxBoundProbe** determines if the ray intersects the volume of the box's bounding box, not just the surface of the box.</span></span>

<span data-ttu-id="06c10-128">Die an **D3DXBoxBoundProbe** über gebenden Werte sind xmin, xmax, ymin, ymax, zmin und zmax.</span><span class="sxs-lookup"><span data-stu-id="06c10-128">The values passed to **D3DXBoxBoundProbe** are xmin, xmax, ymin, ymax, zmin, and zmax.</span></span> <span data-ttu-id="06c10-129">Folglich werden im folgenden die Ecken des umgebenden Felds definiert.</span><span class="sxs-lookup"><span data-stu-id="06c10-129">Thus, the following defines the corners of the bounding box.</span></span>


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



<span data-ttu-id="06c10-130">Die Tiefe des umgebenden Felds in der z-Richtung ist zmax-zmin, in der y-Richtung ist ymax-ymin, und in der x-Richtung ist xmax-xmin.</span><span class="sxs-lookup"><span data-stu-id="06c10-130">The depth of the bounding box in the z direction is zmax - zmin, in the y direction is ymax - ymin, and in the x direction is xmax - xmin.</span></span> <span data-ttu-id="06c10-131">Beispielsweise wird mit den folgenden minimalen und maximalen Vektoren min (-1,-1,-1) und Max (1, 1, 1) das umgebende Feld wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="06c10-131">For example, with the following minimum and maximum vectors, min (-1, -1, -1) and max (1, 1, 1), the bounding box is defined in the following manner.</span></span>


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a><span data-ttu-id="06c10-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06c10-132">Requirements</span></span>



| <span data-ttu-id="06c10-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06c10-133">Requirement</span></span> | <span data-ttu-id="06c10-134">Wert</span><span class="sxs-lookup"><span data-stu-id="06c10-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06c10-135">Header</span><span class="sxs-lookup"><span data-stu-id="06c10-135">Header</span></span>  | <span data-ttu-id="06c10-136">D3DX10math. h</span><span class="sxs-lookup"><span data-stu-id="06c10-136">D3DX10math.h</span></span> |
| <span data-ttu-id="06c10-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="06c10-137">Library</span></span> | <span data-ttu-id="06c10-138">D3dx10. lib</span><span class="sxs-lookup"><span data-stu-id="06c10-138">D3DX10.lib</span></span>  |



## <a name="see-also"></a><span data-ttu-id="06c10-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06c10-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c10-140">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="06c10-140">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
