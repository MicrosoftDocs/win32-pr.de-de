---
description: Führt eine Catmull-Rom interpolung mithilfe der angegebenen 3D-Vektoren aus.
ms.assetid: 324bd4b5-b0df-4dd3-b370-3c365c9f2db1
title: D3DXVec3CatmullRom-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3CatmullRom
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 70c6f605358bfc561e3e630fa4e4e1b87c455768
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355039"
---
# <a name="d3dxvec3catmullrom-function-d3dx10mathh"></a><span data-ttu-id="35123-103">D3DXVec3CatmullRom-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="35123-103">D3DXVec3CatmullRom function (D3DX10Math.h)</span></span>

<span data-ttu-id="35123-104">Führt eine Catmull-Rom interpolung mithilfe der angegebenen 3D-Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="35123-104">Performs a Catmull-Rom interpolation, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="35123-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35123-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3CatmullRom(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV0,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="35123-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35123-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35123-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="35123-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35123-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="35123-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="35123-109">Zeiger auf das [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="35123-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="35123-110">*pV0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35123-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35123-111">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="35123-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="35123-112">Zeiger auf eine Quell-D3DXVECTOR3-Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="35123-112">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="35123-113">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35123-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35123-114">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="35123-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="35123-115">Zeiger auf eine Quell-D3DXVECTOR3-Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="35123-115">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="35123-116">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35123-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35123-117">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="35123-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="35123-118">Zeiger auf eine Quell-D3DXVECTOR3-Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="35123-118">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="35123-119">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35123-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35123-120">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="35123-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="35123-121">Zeiger auf eine Quell-D3DXVECTOR3-Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="35123-121">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="35123-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35123-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35123-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35123-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35123-124">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="35123-124">Weighting factor.</span></span> <span data-ttu-id="35123-125">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="35123-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35123-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35123-126">Return value</span></span>

<span data-ttu-id="35123-127">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="35123-127">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="35123-128">Zeiger auf eine D3DXVECTOR3-Struktur, die das Ergebnis der Catmull-Rom interpolung ist.</span><span class="sxs-lookup"><span data-stu-id="35123-128">Pointer to a D3DXVECTOR3 structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="35123-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35123-129">Remarks</span></span>

<span data-ttu-id="35123-130">In den vier Punkten (P1, P2, P3, P4) finden Sie eine f (s)-Funktion wie folgt:</span><span class="sxs-lookup"><span data-stu-id="35123-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="35123-131">Die Catmull-Rom Spline kann von der Hermite Spline abgeleitet werden, indem Sie Folgendes festlegen:</span><span class="sxs-lookup"><span data-stu-id="35123-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="35123-132">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="35123-132">where:</span></span>

<span data-ttu-id="35123-133">v1 ist der Inhalt von pV0.</span><span class="sxs-lookup"><span data-stu-id="35123-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="35123-134">v2 ist der Inhalt von pV1.</span><span class="sxs-lookup"><span data-stu-id="35123-134">v2 is the contents of pV1.</span></span>

<span data-ttu-id="35123-135">P3 ist der Inhalt von pV2.</span><span class="sxs-lookup"><span data-stu-id="35123-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="35123-136">P4 ist der Inhalt von pV3.</span><span class="sxs-lookup"><span data-stu-id="35123-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="35123-137">Verwenden der Hermite-Spline-Gleichung:</span><span class="sxs-lookup"><span data-stu-id="35123-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="35123-138">und ersetzen Sie durch die Ergebnisse v1, v2, T1, T2:</span><span class="sxs-lookup"><span data-stu-id="35123-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="35123-139">Dies kann wie folgt neu angeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="35123-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="35123-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35123-140">Requirements</span></span>



| <span data-ttu-id="35123-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35123-141">Requirement</span></span> | <span data-ttu-id="35123-142">Wert</span><span class="sxs-lookup"><span data-stu-id="35123-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35123-143">Header</span><span class="sxs-lookup"><span data-stu-id="35123-143">Header</span></span><br/> | <dl> <span data-ttu-id="35123-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="35123-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35123-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35123-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35123-146">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="35123-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
