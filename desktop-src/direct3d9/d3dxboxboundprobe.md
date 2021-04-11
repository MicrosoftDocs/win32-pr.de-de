---
description: Bestimmt, ob ein Strahl das Volume des umgebenden Felds eines Felds schneidet.
ms.assetid: 45ff8540-ed5c-4f54-b3b7-3385087a6863
title: D3DXBoxBoundProbe-Funktion (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 707ab21a3babe7d9a93f776f438cbaab7137849b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132353"
---
# <a name="d3dxboxboundprobe-function"></a><span data-ttu-id="478b5-103">D3DXBoxBoundProbe-Funktion</span><span class="sxs-lookup"><span data-stu-id="478b5-103">D3DXBoxBoundProbe function</span></span>

<span data-ttu-id="478b5-104">Bestimmt, ob ein Strahl das Volume des umgebenden Felds eines Felds schneidet.</span><span class="sxs-lookup"><span data-stu-id="478b5-104">Determines whether a ray intersects the volume of a box's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="478b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="478b5-105">Syntax</span></span>


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="478b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="478b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="478b5-107">*Pmin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="478b5-107">*pMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="478b5-108">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="478b5-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="478b5-109">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die linke untere Ecke des Begrenzungs Rahmens beschreibt.</span><span class="sxs-lookup"><span data-stu-id="478b5-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the lower-left corner of the bounding box.</span></span> <span data-ttu-id="478b5-110">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="478b5-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="478b5-111">*pmax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="478b5-111">*pMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="478b5-112">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="478b5-112">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="478b5-113">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die obere rechte Ecke des Begrenzungs Rahmens beschreibt.</span><span class="sxs-lookup"><span data-stu-id="478b5-113">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the upper-right corner of the bounding box.</span></span> <span data-ttu-id="478b5-114">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="478b5-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="478b5-115">" *prayposition* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="478b5-115">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="478b5-116">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="478b5-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="478b5-117">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Ursprungs Koordinate des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="478b5-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="478b5-118">" *praydirection* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="478b5-118">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="478b5-119">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="478b5-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="478b5-120">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="478b5-120">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="478b5-121">Dieser Vektor sollte nicht (0, 0, 0) sein, muss jedoch nicht normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="478b5-121">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="478b5-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="478b5-122">Return value</span></span>

<span data-ttu-id="478b5-123">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="478b5-123">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="478b5-124">Gibt " **true** " zurück, wenn der Strahl das Volume des umgebenden Felds der Box schneidet.</span><span class="sxs-lookup"><span data-stu-id="478b5-124">Returns **TRUE** if the ray intersects the volume of the box's bounding box.</span></span> <span data-ttu-id="478b5-125">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="478b5-125">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="478b5-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="478b5-126">Remarks</span></span>

<span data-ttu-id="478b5-127">**D3DXboxBoundProbe** bestimmt, ob der Strahl das Volume des umgebenden Felds der Box, nicht nur die Oberfläche des Felds, schneidet.</span><span class="sxs-lookup"><span data-stu-id="478b5-127">**D3DXboxBoundProbe** determines if the ray intersects the volume of the box's bounding box, not just the surface of the box.</span></span>

<span data-ttu-id="478b5-128">Die an **D3DXboxBoundProbe** über gebenden Werte sind xmin, xmax, ymin, ymax, zmin und zmax.</span><span class="sxs-lookup"><span data-stu-id="478b5-128">The values passed to **D3DXboxBoundProbe** are xmin, xmax, ymin, ymax, zmin, and zmax.</span></span> <span data-ttu-id="478b5-129">Folglich werden im folgenden die Ecken des umgebenden Felds definiert.</span><span class="sxs-lookup"><span data-stu-id="478b5-129">Thus, the following defines the corners of the bounding box.</span></span>


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



<span data-ttu-id="478b5-130">Die Tiefe des umgebenden Felds in der z-Richtung ist zmax-zmin, in der y-Richtung ist ymax-ymin, und in der x-Richtung ist xmax-xmin.</span><span class="sxs-lookup"><span data-stu-id="478b5-130">The depth of the bounding box in the z direction is zmax - zmin, in the y direction is ymax - ymin, and in the x direction is xmax - xmin.</span></span> <span data-ttu-id="478b5-131">Beispielsweise wird mit den folgenden minimalen und maximalen Vektoren min (-1,-1,-1) und Max (1, 1, 1) das umgebende Feld wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="478b5-131">For example, with the following minimum and maximum vectors, min (-1, -1, -1) and max (1, 1, 1), the bounding box is defined in the following manner.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="478b5-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="478b5-132">Requirements</span></span>



| <span data-ttu-id="478b5-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="478b5-133">Requirement</span></span> | <span data-ttu-id="478b5-134">Wert</span><span class="sxs-lookup"><span data-stu-id="478b5-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="478b5-135">Header</span><span class="sxs-lookup"><span data-stu-id="478b5-135">Header</span></span><br/>  | <dl> <span data-ttu-id="478b5-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="478b5-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="478b5-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="478b5-137">Library</span></span><br/> | <dl> <span data-ttu-id="478b5-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="478b5-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="478b5-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="478b5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="478b5-140">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="478b5-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="478b5-141">**D3DXComputeBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="478b5-141">**D3DXComputeBoundingBox**</span></span>](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
