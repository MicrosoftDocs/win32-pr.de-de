---
description: Führt eine Catmull-Rom interpolung mithilfe der angegebenen 2D-Vektoren aus.
ms.assetid: 8ec1abfa-0fa9-486a-b86d-bbb8f1d63849
title: D3DXVec2CatmullRom-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CatmullRom
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 71f499313a31c200b5cc657664b10b43dde47ba6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363164"
---
# <a name="d3dxvec2catmullrom-function-d3dx10mathh"></a><span data-ttu-id="db023-103">D3DXVec2CatmullRom-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="db023-103">D3DXVec2CatmullRom function (D3DX10Math.h)</span></span>

<span data-ttu-id="db023-104">Führt eine Catmull-Rom interpolung mithilfe der angegebenen 2D-Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="db023-104">Performs a Catmull-Rom interpolation, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="db023-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="db023-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2CatmullRom(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV0,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="db023-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="db023-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db023-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="db023-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="db023-108">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="db023-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="db023-109">Zeiger auf das [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="db023-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="db023-110">*pV0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db023-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db023-111">Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="db023-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="db023-112">Zeiger auf eine Quell-D3DXVECTOR2-Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="db023-112">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="db023-113">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db023-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db023-114">Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="db023-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="db023-115">Zeiger auf eine Quell-D3DXVECTOR2-Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="db023-115">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="db023-116">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db023-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db023-117">Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="db023-117">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="db023-118">Zeiger auf eine Quell-D3DXVECTOR2-Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="db023-118">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="db023-119">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db023-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db023-120">Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="db023-120">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="db023-121">Zeiger auf eine Quell-D3DXVECTOR2-Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="db023-121">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="db023-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db023-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db023-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db023-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db023-124">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="db023-124">Weighting factor.</span></span> <span data-ttu-id="db023-125">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="db023-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db023-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db023-126">Return value</span></span>

<span data-ttu-id="db023-127">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="db023-127">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="db023-128">Zeiger auf eine D3DXVECTOR2-Struktur, die das Ergebnis der Catmull-Rom interpolung ist.</span><span class="sxs-lookup"><span data-stu-id="db023-128">Pointer to a D3DXVECTOR2 structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="db023-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db023-129">Remarks</span></span>

<span data-ttu-id="db023-130">In den vier Punkten (P1, P2, P3, P4) finden Sie eine f (s)-Funktion wie folgt:</span><span class="sxs-lookup"><span data-stu-id="db023-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="db023-131">Die Catmull-Rom Spline kann von der Hermite Spline abgeleitet werden, indem Sie Folgendes festlegen:</span><span class="sxs-lookup"><span data-stu-id="db023-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="db023-132">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="db023-132">where:</span></span>

<span data-ttu-id="db023-133">v1 ist der Inhalt von pV0.</span><span class="sxs-lookup"><span data-stu-id="db023-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="db023-134">v2 ist der Inhalt von pV1.</span><span class="sxs-lookup"><span data-stu-id="db023-134">v2 is the contents of pV1.</span></span>

<span data-ttu-id="db023-135">P3 ist der Inhalt von pV2.</span><span class="sxs-lookup"><span data-stu-id="db023-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="db023-136">P4 ist der Inhalt von pV3.</span><span class="sxs-lookup"><span data-stu-id="db023-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="db023-137">Verwenden der Hermite-Spline-Gleichung:</span><span class="sxs-lookup"><span data-stu-id="db023-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="db023-138">und ersetzen Sie durch die Ergebnisse v1, v2, T1, T2:</span><span class="sxs-lookup"><span data-stu-id="db023-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2)/2
```



<span data-ttu-id="db023-139">Dies kann wie folgt neu angeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="db023-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="db023-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db023-140">Requirements</span></span>



| <span data-ttu-id="db023-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db023-141">Requirement</span></span> | <span data-ttu-id="db023-142">Wert</span><span class="sxs-lookup"><span data-stu-id="db023-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db023-143">Header</span><span class="sxs-lookup"><span data-stu-id="db023-143">Header</span></span><br/>  | <dl> <span data-ttu-id="db023-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="db023-144"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="db023-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="db023-145">Library</span></span><br/> | <dl> <span data-ttu-id="db023-146"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db023-146"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db023-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db023-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db023-148">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="db023-148">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
