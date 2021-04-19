---
description: Führt eine Catmull-Rom interpolung mithilfe der angegebenen 3D-Vektoren aus.
ms.assetid: 779f067c-ac46-4fde-9e18-e31b1504b490
title: D3DXVec3CatmullRom-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3CatmullRom
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d56c4551f6451d5b817ca0a312ceea6961d3fcce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367405"
---
# <a name="d3dxvec3catmullrom-function-d3dx9mathh"></a><span data-ttu-id="1ae0c-103">D3DXVec3CatmullRom-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1ae0c-103">D3DXVec3CatmullRom function (D3dx9math.h)</span></span>

<span data-ttu-id="1ae0c-104">Führt eine Catmull-Rom interpolung mithilfe der angegebenen 3D-Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="1ae0c-104">Performs a Catmull-Rom interpolation, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae0c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ae0c-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1ae0c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ae0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ae0c-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1ae0c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae0c-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ae0c-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1ae0c-109">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="1ae0c-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1ae0c-110">*pV0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae0c-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae0c-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1ae0c-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1ae0c-112">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="1ae0c-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="1ae0c-113">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae0c-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae0c-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1ae0c-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1ae0c-115">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="1ae0c-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="1ae0c-116">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae0c-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae0c-117">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1ae0c-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1ae0c-118">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="1ae0c-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="1ae0c-119">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae0c-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae0c-120">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1ae0c-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1ae0c-121">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, ein Positions Vektor.</span><span class="sxs-lookup"><span data-stu-id="1ae0c-121">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="1ae0c-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae0c-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae0c-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ae0c-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ae0c-124">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="1ae0c-124">Weighting factor.</span></span> <span data-ttu-id="1ae0c-125">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="1ae0c-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ae0c-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ae0c-126">Return value</span></span>

<span data-ttu-id="1ae0c-127">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ae0c-127">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1ae0c-128">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis der Catmull-Rom interpolung ist.</span><span class="sxs-lookup"><span data-stu-id="1ae0c-128">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ae0c-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ae0c-129">Remarks</span></span>

<span data-ttu-id="1ae0c-130">In den vier Punkten (P1, P2, P3, P4) finden Sie eine f (s)-Funktion wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1ae0c-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="1ae0c-131">Die Catmull-Rom Spline kann von der Hermite Spline abgeleitet werden, indem Sie Folgendes festlegen:</span><span class="sxs-lookup"><span data-stu-id="1ae0c-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="1ae0c-132">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="1ae0c-132">where:</span></span>

<span data-ttu-id="1ae0c-133">v1 ist der Inhalt von pV0.</span><span class="sxs-lookup"><span data-stu-id="1ae0c-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="1ae0c-134">v2 ist der Inhalt von pV1.</span><span class="sxs-lookup"><span data-stu-id="1ae0c-134">v2 is the contents of pV1.</span></span>

<span data-ttu-id="1ae0c-135">P3 ist der Inhalt von pV2.</span><span class="sxs-lookup"><span data-stu-id="1ae0c-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="1ae0c-136">P4 ist der Inhalt von pV3.</span><span class="sxs-lookup"><span data-stu-id="1ae0c-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="1ae0c-137">Verwenden der Hermite-Spline-Gleichung:</span><span class="sxs-lookup"><span data-stu-id="1ae0c-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="1ae0c-138">und ersetzen Sie durch die Ergebnisse v1, v2, T1, T2:</span><span class="sxs-lookup"><span data-stu-id="1ae0c-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="1ae0c-139">Dies kann wie folgt neu angeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="1ae0c-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="1ae0c-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ae0c-140">Requirements</span></span>



| <span data-ttu-id="1ae0c-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ae0c-141">Requirement</span></span> | <span data-ttu-id="1ae0c-142">Wert</span><span class="sxs-lookup"><span data-stu-id="1ae0c-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae0c-143">Header</span><span class="sxs-lookup"><span data-stu-id="1ae0c-143">Header</span></span><br/>  | <dl> <span data-ttu-id="1ae0c-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ae0c-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1ae0c-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1ae0c-145">Library</span></span><br/> | <dl> <span data-ttu-id="1ae0c-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ae0c-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ae0c-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ae0c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae0c-148">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1ae0c-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1ae0c-149">**D3DXVec2CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="1ae0c-149">**D3DXVec2CatmullRom**</span></span>](d3dxvec2catmullrom.md)
</dt> <dt>

[<span data-ttu-id="1ae0c-150">**D3DXVec4CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="1ae0c-150">**D3DXVec4CatmullRom**</span></span>](d3dxvec4catmullrom.md)
</dt> </dl>

 

 
