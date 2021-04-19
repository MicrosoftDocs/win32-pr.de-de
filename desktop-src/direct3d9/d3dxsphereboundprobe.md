---
description: Bestimmt, ob ein Strahl das Volume des Begrenzungs Rahmens einer Kugel schneidet.
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: D3DXSphereBoundProbe-Funktion (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbab8a49165a87f73037ae25230d67b02222fc15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363133"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a><span data-ttu-id="03d66-103">D3DXSphereBoundProbe-Funktion (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="03d66-103">D3DXSphereBoundProbe function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="03d66-104">Bestimmt, ob ein Strahl das Volume des Begrenzungs Rahmens einer Kugel schneidet.</span><span class="sxs-lookup"><span data-stu-id="03d66-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d66-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03d66-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="03d66-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03d66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03d66-107">*pcenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03d66-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03d66-108">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="03d66-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="03d66-109">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Mittelpunkt Koordinate der Kugel angibt.</span><span class="sxs-lookup"><span data-stu-id="03d66-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="03d66-110">*RADIUS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03d66-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03d66-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03d66-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="03d66-112">Der Radius der Kugel.</span><span class="sxs-lookup"><span data-stu-id="03d66-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="03d66-113">" *prayposition* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="03d66-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03d66-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="03d66-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="03d66-115">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Ursprungs Koordinate des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="03d66-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="03d66-116">" *praydirection* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="03d66-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03d66-117">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="03d66-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="03d66-118">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="03d66-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="03d66-119">Dieser Vektor sollte nicht (0, 0, 0) sein, muss jedoch nicht normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="03d66-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03d66-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03d66-120">Return value</span></span>

<span data-ttu-id="03d66-121">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03d66-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="03d66-122">Gibt **true** zurück, wenn der Strahl das Volume des umgebenden Felds der Kugel schneidet.</span><span class="sxs-lookup"><span data-stu-id="03d66-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="03d66-123">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="03d66-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="03d66-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03d66-124">Remarks</span></span>

<span data-ttu-id="03d66-125">**D3DXSphereBoundProbe** bestimmt, ob der Strahl das Volume des umgebenden Felds der Kugel schneidet, nicht nur die Oberfläche der Kugel.</span><span class="sxs-lookup"><span data-stu-id="03d66-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="03d66-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03d66-126">Requirements</span></span>



| <span data-ttu-id="03d66-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03d66-127">Requirement</span></span> | <span data-ttu-id="03d66-128">Wert</span><span class="sxs-lookup"><span data-stu-id="03d66-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03d66-129">Header</span><span class="sxs-lookup"><span data-stu-id="03d66-129">Header</span></span><br/>  | <dl> <span data-ttu-id="03d66-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="03d66-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="03d66-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="03d66-131">Library</span></span><br/> | <dl> <span data-ttu-id="03d66-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03d66-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="03d66-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03d66-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d66-134">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="03d66-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
