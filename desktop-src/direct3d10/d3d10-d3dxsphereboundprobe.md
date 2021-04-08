---
description: Bestimmt, ob ein Strahl das Volume des Begrenzungs Rahmens einer Kugel schneidet.
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: D3DXSphereBoundProbe-Funktion (D3DX10math. h)
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
ms.openlocfilehash: 09116e13582bbb75bc15ed04360ce02c4983f986
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762234"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a><span data-ttu-id="ffd2b-103">D3DXSphereBoundProbe-Funktion (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="ffd2b-103">D3DXSphereBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="ffd2b-104">Bestimmt, ob ein Strahl das Volume des Begrenzungs Rahmens einer Kugel schneidet.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffd2b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffd2b-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="ffd2b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffd2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffd2b-107">*pcenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffd2b-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd2b-108">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ffd2b-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ffd2b-109">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die Mittelpunkt Koordinate der Kugel angibt.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="ffd2b-110">*RADIUS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffd2b-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd2b-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ffd2b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ffd2b-112">Der Radius der Kugel.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="ffd2b-113">" *prayposition* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="ffd2b-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd2b-114">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ffd2b-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ffd2b-115">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die Ursprungs Koordinate des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="ffd2b-116">" *praydirection* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="ffd2b-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd2b-117">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ffd2b-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ffd2b-118">Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="ffd2b-119">Dieser Vektor sollte nicht (0, 0, 0) sein, muss jedoch nicht normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffd2b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffd2b-120">Return value</span></span>

<span data-ttu-id="ffd2b-121">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ffd2b-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ffd2b-122">Gibt **true** zurück, wenn der Strahl das Volume des umgebenden Felds der Kugel schneidet.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="ffd2b-123">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffd2b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffd2b-124">Remarks</span></span>

<span data-ttu-id="ffd2b-125">**D3DXSphereBoundProbe** bestimmt, ob der Strahl das Volume des umgebenden Felds der Kugel schneidet, nicht nur die Oberfläche der Kugel.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffd2b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffd2b-126">Requirements</span></span>



| <span data-ttu-id="ffd2b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffd2b-127">Requirement</span></span> | <span data-ttu-id="ffd2b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ffd2b-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd2b-129">Header</span><span class="sxs-lookup"><span data-stu-id="ffd2b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ffd2b-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffd2b-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="ffd2b-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ffd2b-131">Library</span></span><br/> | <dl> <span data-ttu-id="ffd2b-132"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffd2b-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ffd2b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffd2b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffd2b-134">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ffd2b-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
