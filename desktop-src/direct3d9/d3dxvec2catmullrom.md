---
description: 'D3DXVec2CatmullRom-Funktion (D3dx9math.h): Führt eine Catmull-Rom-Interpolation mithilfe der angegebenen 2D-Vektoren aus.'
ms.assetid: dacda32d-b4c4-4d8b-9d20-9a4bb1d3ce6c
title: D3DXVec2CatmullRom-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c734727f3f2f44c9094885e0e743f605f16c91d2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114318"
---
# <a name="d3dxvec2catmullrom-function-d3dx9mathh"></a><span data-ttu-id="9c6e9-103">D3DXVec2CatmullRom-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="9c6e9-103">D3DXVec2CatmullRom function (D3dx9math.h)</span></span>

<span data-ttu-id="9c6e9-104">Führt eine Catmull-Rom Interpolation mit den angegebenen 2D-Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="9c6e9-104">Performs a Catmull-Rom interpolation, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c6e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c6e9-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="9c6e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c6e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c6e9-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9c6e9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6e9-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c6e9-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9c6e9-109">Zeiger auf die [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="9c6e9-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9c6e9-110">*pV0* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9c6e9-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6e9-111">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9c6e9-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9c6e9-112">Zeiger auf eine [**D3DXVECTOR2-Quellstruktur,**](d3dxvector2.md) einen Positionsvektor.</span><span class="sxs-lookup"><span data-stu-id="9c6e9-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="9c6e9-113">*pV1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9c6e9-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6e9-114">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9c6e9-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9c6e9-115">Zeiger auf eine [**D3DXVECTOR2-Quellstruktur,**](d3dxvector2.md) einen Positionsvektor.</span><span class="sxs-lookup"><span data-stu-id="9c6e9-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="9c6e9-116">*pV2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9c6e9-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6e9-117">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9c6e9-117">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9c6e9-118">Zeiger auf eine [**D3DXVECTOR2-Quellstruktur,**](d3dxvector2.md) einen Positionsvektor.</span><span class="sxs-lookup"><span data-stu-id="9c6e9-118">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="9c6e9-119">*pV3* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9c6e9-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6e9-120">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9c6e9-120">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9c6e9-121">Zeiger auf eine [**D3DXVECTOR2-Quellstruktur,**](d3dxvector2.md) einen Positionsvektor.</span><span class="sxs-lookup"><span data-stu-id="9c6e9-121">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="9c6e9-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c6e9-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c6e9-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c6e9-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c6e9-124">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="9c6e9-124">Weighting factor.</span></span> <span data-ttu-id="9c6e9-125">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9c6e9-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c6e9-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c6e9-126">Return value</span></span>

<span data-ttu-id="9c6e9-127">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c6e9-127">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9c6e9-128">Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die das Ergebnis der Catmull-Rom Interpolation ist.</span><span class="sxs-lookup"><span data-stu-id="9c6e9-128">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c6e9-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c6e9-129">Remarks</span></span>

<span data-ttu-id="9c6e9-130">Suchen Sie bei vier Punkten (p1, p2, p3, p4) eine Funktion Q(s) so, dass:</span><span class="sxs-lookup"><span data-stu-id="9c6e9-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="9c6e9-131">Die Catmull-Rom Spline kann durch Festlegen von vom Hermite-Spline abgeleitet werden:</span><span class="sxs-lookup"><span data-stu-id="9c6e9-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="9c6e9-132">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="9c6e9-132">where:</span></span>

<span data-ttu-id="9c6e9-133">v1 ist der Inhalt von pV0.</span><span class="sxs-lookup"><span data-stu-id="9c6e9-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="9c6e9-134">v2 ist der Inhalt von pV1.</span><span class="sxs-lookup"><span data-stu-id="9c6e9-134">v2 is the contents of pV1.</span></span>

<span data-ttu-id="9c6e9-135">p3 ist der Inhalt von pV2.</span><span class="sxs-lookup"><span data-stu-id="9c6e9-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="9c6e9-136">p4 ist der Inhalt von pV3.</span><span class="sxs-lookup"><span data-stu-id="9c6e9-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="9c6e9-137">Verwenden der Hermite-Splinegleichung:</span><span class="sxs-lookup"><span data-stu-id="9c6e9-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="9c6e9-138">und Ersetzen durch v1, v2, t1, t2 ergibt:</span><span class="sxs-lookup"><span data-stu-id="9c6e9-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2)/2
```



<span data-ttu-id="9c6e9-139">Dies kann wie hier erläutert neu angeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="9c6e9-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="9c6e9-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c6e9-140">Requirements</span></span>



| <span data-ttu-id="9c6e9-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c6e9-141">Requirement</span></span> | <span data-ttu-id="9c6e9-142">Wert</span><span class="sxs-lookup"><span data-stu-id="9c6e9-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c6e9-143">Header</span><span class="sxs-lookup"><span data-stu-id="9c6e9-143">Header</span></span><br/>  | <dl> <span data-ttu-id="9c6e9-144"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="9c6e9-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9c6e9-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9c6e9-145">Library</span></span><br/> | <dl> <span data-ttu-id="9c6e9-146"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c6e9-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9c6e9-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9c6e9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c6e9-148">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="9c6e9-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9c6e9-149">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="9c6e9-149">**D3DXVec3CatmullRom**</span></span>](d3dxvec3catmullrom.md)
</dt> <dt>

[<span data-ttu-id="9c6e9-150">**D3DXVec4CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="9c6e9-150">**D3DXVec4CatmullRom**</span></span>](d3dxvec4catmullrom.md)
</dt> </dl>

 

 
