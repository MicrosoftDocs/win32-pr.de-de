---
description: 'D3DXVec4CatmullRom-Funktion (D3dx9math.h): Führt unter Verwendung der angegebenen 4D-Vektoren eine Catmull-Rom Interpolation durch.'
ms.assetid: 24c26e70-b02c-4621-8b7e-db16f99dddb5
title: D3DXVec4CatmullRom-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4CatmullRom
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 06ba24374ee2ad4e6fd008d90c55d2990dc166f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115528"
---
# <a name="d3dxvec4catmullrom-function-d3dx9mathh"></a><span data-ttu-id="849ef-103">D3DXVec4CatmullRom-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="849ef-103">D3DXVec4CatmullRom function (D3dx9math.h)</span></span>

<span data-ttu-id="849ef-104">Führt eine Catmull-Rom Interpolation unter Verwendung der angegebenen 4D-Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="849ef-104">Performs a Catmull-Rom interpolation, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="849ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="849ef-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="849ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="849ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="849ef-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="849ef-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="849ef-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="849ef-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="849ef-109">Zeiger auf die [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="849ef-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="849ef-110">*pV0* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="849ef-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="849ef-111">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="849ef-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="849ef-112">Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Positionsvektor.</span><span class="sxs-lookup"><span data-stu-id="849ef-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="849ef-113">*pV1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="849ef-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="849ef-114">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="849ef-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="849ef-115">Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Positionsvektor.</span><span class="sxs-lookup"><span data-stu-id="849ef-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="849ef-116">*pV2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="849ef-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="849ef-117">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="849ef-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="849ef-118">Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Positionsvektor.</span><span class="sxs-lookup"><span data-stu-id="849ef-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="849ef-119">*pV3* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="849ef-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="849ef-120">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="849ef-120">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="849ef-121">Zeiger auf eine [**D3DXVECTOR4-Quellstruktur,**](d3dxvector4.md) einen Positionsvektor.</span><span class="sxs-lookup"><span data-stu-id="849ef-121">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="849ef-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="849ef-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="849ef-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="849ef-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="849ef-124">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="849ef-124">Weighting factor.</span></span> <span data-ttu-id="849ef-125">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="849ef-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="849ef-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="849ef-126">Return value</span></span>

<span data-ttu-id="849ef-127">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="849ef-127">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="849ef-128">Zeiger auf eine [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Ergebnis der Catmull-Rom ist.</span><span class="sxs-lookup"><span data-stu-id="849ef-128">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="849ef-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="849ef-129">Remarks</span></span>

<span data-ttu-id="849ef-130">Suchen Sie bei vier Punkten (p1, p2, p3, p4) eine Funktion Q(s) so, dass:</span><span class="sxs-lookup"><span data-stu-id="849ef-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="849ef-131">Die Catmull-Rom spline kann durch Festlegen von vom Hermite-Spline abgeleitet werden:</span><span class="sxs-lookup"><span data-stu-id="849ef-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="849ef-132">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="849ef-132">where:</span></span>

<span data-ttu-id="849ef-133">v1 ist der Inhalt von pV0.</span><span class="sxs-lookup"><span data-stu-id="849ef-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="849ef-134">v2 im Inhalt von pV1.</span><span class="sxs-lookup"><span data-stu-id="849ef-134">v2 in the contents of pV1.</span></span>

<span data-ttu-id="849ef-135">p3 ist der Inhalt von pV2.</span><span class="sxs-lookup"><span data-stu-id="849ef-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="849ef-136">p4 ist der Inhalt von pV3.</span><span class="sxs-lookup"><span data-stu-id="849ef-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="849ef-137">Verwenden der Splinegleichung "Hermite":</span><span class="sxs-lookup"><span data-stu-id="849ef-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="849ef-138">und der Ersatz für v1, v2, t1, t2 ergibt:</span><span class="sxs-lookup"><span data-stu-id="849ef-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="849ef-139">Dies kann neu angeordnet werden wie:</span><span class="sxs-lookup"><span data-stu-id="849ef-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="849ef-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="849ef-140">Requirements</span></span>



| <span data-ttu-id="849ef-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="849ef-141">Requirement</span></span> | <span data-ttu-id="849ef-142">Wert</span><span class="sxs-lookup"><span data-stu-id="849ef-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="849ef-143">Header</span><span class="sxs-lookup"><span data-stu-id="849ef-143">Header</span></span><br/>  | <dl> <span data-ttu-id="849ef-144"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="849ef-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="849ef-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="849ef-145">Library</span></span><br/> | <dl> <span data-ttu-id="849ef-146"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="849ef-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="849ef-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="849ef-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="849ef-148">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="849ef-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="849ef-149">**D3DXVec2CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="849ef-149">**D3DXVec2CatmullRom**</span></span>](d3dxvec2catmullrom.md)
</dt> <dt>

[<span data-ttu-id="849ef-150">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="849ef-150">**D3DXVec3CatmullRom**</span></span>](d3dxvec3catmullrom.md)
</dt> </dl>

 

 
