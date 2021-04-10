---
description: Führt eine Catmull-Rom interpolung mithilfe der angegebenen 4D-Vektoren aus.
ms.assetid: e3a10989-e25e-46fa-b72e-bade936cacf1
title: D3DXVec4CatmullRom-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4CatmullRom
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 8e027272a038f17a77dbeda861d6be909afa2f7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961575"
---
# <a name="d3dxvec4catmullrom-function-d3dx10mathh"></a><span data-ttu-id="1f570-103">D3DXVec4CatmullRom-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1f570-103">D3DXVec4CatmullRom function (D3DX10Math.h)</span></span>

<span data-ttu-id="1f570-104">Führt eine Catmull-Rom interpolung mithilfe der angegebenen 4D-Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="1f570-104">Performs a Catmull-Rom interpolation, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f570-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f570-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4CatmullRom(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV0,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="1f570-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f570-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f570-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1f570-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f570-108">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1f570-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1f570-109">Zeiger auf das [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="1f570-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1f570-110">*pV0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f570-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f570-111">Typ: **Konstanten [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f570-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1f570-112">Zeiger auf eine Quell-D3DXVECTOR4-Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="1f570-112">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="1f570-113">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f570-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f570-114">Typ: **Konstanten [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f570-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1f570-115">Zeiger auf eine Quell-D3DXVECTOR4-Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="1f570-115">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="1f570-116">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f570-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f570-117">Typ: **Konstanten [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f570-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1f570-118">Zeiger auf eine Quell-D3DXVECTOR4-Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="1f570-118">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="1f570-119">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f570-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f570-120">Typ: **Konstanten [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f570-120">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1f570-121">Zeiger auf eine Quell-D3DXVECTOR4-Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="1f570-121">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="1f570-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f570-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f570-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f570-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f570-124">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="1f570-124">Weighting factor.</span></span> <span data-ttu-id="1f570-125">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="1f570-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f570-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f570-126">Return value</span></span>

<span data-ttu-id="1f570-127">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1f570-127">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1f570-128">Zeiger auf eine D3DXVECTOR4-Struktur, die das Ergebnis der Catmull-Rom interpolung ist.</span><span class="sxs-lookup"><span data-stu-id="1f570-128">Pointer to a D3DXVECTOR4 structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f570-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f570-129">Remarks</span></span>

<span data-ttu-id="1f570-130">In den vier Punkten (P1, P2, P3, P4) finden Sie eine f (s)-Funktion wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1f570-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="1f570-131">Die Catmull-Rom Spline kann von der Hermite Spline abgeleitet werden, indem Sie Folgendes festlegen:</span><span class="sxs-lookup"><span data-stu-id="1f570-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="1f570-132">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="1f570-132">where:</span></span>

<span data-ttu-id="1f570-133">v1 ist der Inhalt von pV0.</span><span class="sxs-lookup"><span data-stu-id="1f570-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="1f570-134">v2 im Inhalt von pV1.</span><span class="sxs-lookup"><span data-stu-id="1f570-134">v2 in the contents of pV1.</span></span>

<span data-ttu-id="1f570-135">P3 ist der Inhalt von pV2.</span><span class="sxs-lookup"><span data-stu-id="1f570-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="1f570-136">P4 ist der Inhalt von pV3.</span><span class="sxs-lookup"><span data-stu-id="1f570-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="1f570-137">Verwenden der Hermite-Spline-Gleichung:</span><span class="sxs-lookup"><span data-stu-id="1f570-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="1f570-138">und ersetzen Sie durch die Ergebnisse v1, v2, T1, T2:</span><span class="sxs-lookup"><span data-stu-id="1f570-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="1f570-139">Dies kann wie folgt neu angeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="1f570-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="1f570-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f570-140">Requirements</span></span>



| <span data-ttu-id="1f570-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f570-141">Requirement</span></span> | <span data-ttu-id="1f570-142">Wert</span><span class="sxs-lookup"><span data-stu-id="1f570-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f570-143">Header</span><span class="sxs-lookup"><span data-stu-id="1f570-143">Header</span></span><br/> | <dl> <span data-ttu-id="1f570-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f570-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f570-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f570-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f570-146">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1f570-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
