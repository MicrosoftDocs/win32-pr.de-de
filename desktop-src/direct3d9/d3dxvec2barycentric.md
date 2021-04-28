---
description: 'D3DXVec2BaryCentric-Funktion (D3dx9math.h): Gibt unter Verwendung der angegebenen 2D-Vektoren einen Punkt in baryzentrierten Koordinaten zurück.'
ms.assetid: afbffe6d-d786-4d65-b737-ae201613d1ac
title: D3DXVec2BaryCentric-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3210624087a3d1d5a612ba1eb628e7d85ba4fea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117788"
---
# <a name="d3dxvec2barycentric-function-d3dx9mathh"></a><span data-ttu-id="34a45-103">D3DXVec2BaryCentric-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="34a45-103">D3DXVec2BaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="34a45-104">Gibt unter Verwendung der angegebenen 2D-Vektoren einen Punkt in baryzentrierten Koordinaten zurück.</span><span class="sxs-lookup"><span data-stu-id="34a45-104">Returns a point in Barycentric coordinates, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a45-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34a45-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2BaryCentric(
  _Out_       D3DXVECTOR2 *pOut,
  _In_  const D3DXVECTOR2 *pV1,
  _In_  const D3DXVECTOR2 *pV2,
  _In_  const D3DXVECTOR2 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="34a45-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34a45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34a45-107">*pOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="34a45-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34a45-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="34a45-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="34a45-109">Zeiger auf die [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="34a45-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="34a45-110">*pV1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="34a45-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a45-111">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="34a45-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="34a45-112">Zeiger auf eine [**D3DXVECTOR2-Quellstruktur.**](d3dxvector2.md)</span><span class="sxs-lookup"><span data-stu-id="34a45-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="34a45-113">*pV2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="34a45-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a45-114">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="34a45-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="34a45-115">Zeiger auf eine [**D3DXVECTOR2-Quellstruktur.**](d3dxvector2.md)</span><span class="sxs-lookup"><span data-stu-id="34a45-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="34a45-116">*pV3* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="34a45-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a45-117">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="34a45-117">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="34a45-118">Zeiger auf eine [**D3DXVECTOR2-Quellstruktur.**](d3dxvector2.md)</span><span class="sxs-lookup"><span data-stu-id="34a45-118">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="34a45-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34a45-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a45-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34a45-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34a45-121">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="34a45-121">Weighting factor.</span></span> <span data-ttu-id="34a45-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="34a45-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="34a45-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34a45-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a45-124">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34a45-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34a45-125">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="34a45-125">Weighting factor.</span></span> <span data-ttu-id="34a45-126">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="34a45-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34a45-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34a45-127">Return value</span></span>

<span data-ttu-id="34a45-128">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="34a45-128">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="34a45-129">Zeiger auf eine [**D3DXVECTOR2-Struktur**](d3dxvector2.md) in baryzentrischen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="34a45-129">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="34a45-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34a45-130">Remarks</span></span>

<span data-ttu-id="34a45-131">Die **D3DXVec2BaryCentric-Funktion** bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet.</span><span class="sxs-lookup"><span data-stu-id="34a45-131">The **D3DXVec2BaryCentric** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="34a45-132">Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: V1 + f(V2-V1) + g(V3-V1).</span><span class="sxs-lookup"><span data-stu-id="34a45-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="34a45-133">Jeder Punkt in der Ebene V1V2V3 kann durch die Barycentric-Koordinate (f,g) dargestellt werden. Der Parameter *f* steuert, wie viel V2 in das Ergebnis gewichtet wird, und der Parameter *g* steuert, wie viel V3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="34a45-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter *f* controls how much V2 gets weighted into the result, and the parameter *g* controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="34a45-134">Schließlich steuert 1-f-g, wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="34a45-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="34a45-135">Beachten Sie die folgenden Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="34a45-135">Note the following relations.</span></span>

-   <span data-ttu-id="34a45-136">Wenn (f>=0 &, & g>=0 &, & 1-f-g>=0), befindet sich der Punkt innerhalb des Dreiecks V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="34a45-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="34a45-137">Wenn (f==0 &, & g>=0 &, & 1-f-g>=0), befindet sich der Punkt in der Zeile V1V3.</span><span class="sxs-lookup"><span data-stu-id="34a45-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="34a45-138">Wenn (f>=0 &, & g==0 &, & 1-f-g>=0), befindet sich der Punkt in der Zeile V1V2.</span><span class="sxs-lookup"><span data-stu-id="34a45-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="34a45-139">Wenn (f>=0 &, & g>=0 &, & 1-f-g==0), befindet sich der Punkt in der Zeile V2V3.</span><span class="sxs-lookup"><span data-stu-id="34a45-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="34a45-140">Barycentric-Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="34a45-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="34a45-141">In diesem Kontext stellt die Verwendung von Barycentric-Koordinaten eine Änderung der Koordinatensysteme dar.</span><span class="sxs-lookup"><span data-stu-id="34a45-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="34a45-142">Was für kartesische Koordinaten gilt, gilt für baryzentrische Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="34a45-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="34a45-143">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="34a45-143">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="34a45-144">Auf diese Weise kann die **D3DXVec2BaryCentric-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34a45-144">In this way, the **D3DXVec2BaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="34a45-145">Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="34a45-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="34a45-146">Eine ausführlichere Beschreibung der baryzentrischen Koordinaten finden Sie unter [Mathworld es Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="34a45-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span> <span data-ttu-id="34a45-147">(Diese Ressource ist in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="34a45-147">(This resource may not be available in some languages and countries.)</span></span>

## <a name="requirements"></a><span data-ttu-id="34a45-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34a45-148">Requirements</span></span>



| <span data-ttu-id="34a45-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34a45-149">Requirement</span></span> | <span data-ttu-id="34a45-150">Wert</span><span class="sxs-lookup"><span data-stu-id="34a45-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34a45-151">Header</span><span class="sxs-lookup"><span data-stu-id="34a45-151">Header</span></span><br/>  | <dl> <span data-ttu-id="34a45-152"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="34a45-152"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="34a45-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34a45-153">Library</span></span><br/> | <dl> <span data-ttu-id="34a45-154"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="34a45-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="34a45-155">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="34a45-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a45-156">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="34a45-156">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
