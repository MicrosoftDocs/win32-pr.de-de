---
description: 'D3DXVec3BaryCentric-Funktion (D3dx9math.h): Gibt unter Verwendung der angegebenen 3D-Vektoren einen Punkt in baryzentrierten Koordinaten zurück.'
ms.assetid: ecbabc76-9936-4f31-adec-1ec807984787
title: D3DXVec3BaryCentric-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c966eeabe78deabefb2877405f649f3d162f9d73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097894"
---
# <a name="d3dxvec3barycentric-function-d3dx9mathh"></a><span data-ttu-id="3e180-103">D3DXVec3BaryCentric-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="3e180-103">D3DXVec3BaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="3e180-104">Gibt unter Verwendung der angegebenen 3D-Vektoren einen Punkt in baryzentrierten Koordinaten zurück.</span><span class="sxs-lookup"><span data-stu-id="3e180-104">Returns a point in Barycentric coordinates, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e180-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e180-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3BaryCentric(
  _Out_       D3DXVECTOR3 *pOut,
  _In_  const D3DXVECTOR3 *pV1,
  _In_  const D3DXVECTOR3 *pV2,
  _In_  const D3DXVECTOR3 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="3e180-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e180-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e180-107">*pOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3e180-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e180-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e180-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3e180-109">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="3e180-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3e180-110">*pV1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3e180-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e180-111">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3e180-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3e180-112">Zeiger auf eine [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="3e180-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3e180-113">*pV2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3e180-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e180-114">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3e180-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3e180-115">Zeiger auf eine [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="3e180-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3e180-116">*pV3* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3e180-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e180-117">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3e180-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3e180-118">Zeiger auf eine [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="3e180-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3e180-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e180-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e180-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e180-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e180-121">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="3e180-121">Weighting factor.</span></span> <span data-ttu-id="3e180-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="3e180-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3e180-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e180-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e180-124">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e180-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e180-125">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="3e180-125">Weighting factor.</span></span> <span data-ttu-id="3e180-126">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="3e180-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e180-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e180-127">Return value</span></span>

<span data-ttu-id="3e180-128">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e180-128">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3e180-129">Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3dxvector3.md) in baryzentrischen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="3e180-129">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e180-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e180-130">Remarks</span></span>

<span data-ttu-id="3e180-131">Die **D3DXVec3BaryCentric-Funktion** bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet.</span><span class="sxs-lookup"><span data-stu-id="3e180-131">The **D3DXVec3BaryCentric** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="3e180-132">Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: V1 + f(V2-V1) + g(V3-V1).</span><span class="sxs-lookup"><span data-stu-id="3e180-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="3e180-133">Jeder Punkt in der Ebene V1V2V3 kann durch die Barycentric-Koordinate (f,g) dargestellt werden. Der Parameter *f* steuert, wie viel V2 in das Ergebnis gewichtet wird, und der Parameter *g* steuert, wie viel V3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="3e180-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter *f* controls how much V2 gets weighted into the result and the parameter *g* controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="3e180-134">Schließlich steuert 1-f-g, wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="3e180-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="3e180-135">Beachten Sie die folgenden Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="3e180-135">Note the following relations.</span></span>

-   <span data-ttu-id="3e180-136">Wenn (f>=0 &, & g>=0 &, & 1-f-g>=0), befindet sich der Punkt innerhalb des Dreiecks V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="3e180-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="3e180-137">Wenn (f==0 &, & g>=0 &, & 1-f-g>=0), befindet sich der Punkt in der Zeile V1V3.</span><span class="sxs-lookup"><span data-stu-id="3e180-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="3e180-138">Wenn (f>=0 &, & g==0 &, & 1-f-g>=0), befindet sich der Punkt in der Zeile V1V2.</span><span class="sxs-lookup"><span data-stu-id="3e180-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="3e180-139">Wenn (f>=0 &, & g>=0 &, & 1-f-g==0), befindet sich der Punkt in der Zeile V2V3.</span><span class="sxs-lookup"><span data-stu-id="3e180-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="3e180-140">Barycentric-Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="3e180-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="3e180-141">In diesem Kontext stellt die Verwendung von Barycentric-Koordinaten eine Änderung der Koordinatensysteme dar.</span><span class="sxs-lookup"><span data-stu-id="3e180-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="3e180-142">Was für kartesische Koordinaten gilt, gilt für baryzentrische Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="3e180-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="3e180-143">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3e180-143">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="3e180-144">Auf diese Weise kann die **D3DXVec3BaryCentric-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e180-144">In this way, the **D3DXVec3BaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="3e180-145">Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="3e180-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="3e180-146">Eine ausführlichere Beschreibung der baryzentrischen Koordinaten finden Sie unter [Mathworld es Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="3e180-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e180-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e180-147">Requirements</span></span>



| <span data-ttu-id="3e180-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e180-148">Requirement</span></span> | <span data-ttu-id="3e180-149">Wert</span><span class="sxs-lookup"><span data-stu-id="3e180-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e180-150">Header</span><span class="sxs-lookup"><span data-stu-id="3e180-150">Header</span></span><br/>  | <dl> <span data-ttu-id="3e180-151"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="3e180-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3e180-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3e180-152">Library</span></span><br/> | <dl> <span data-ttu-id="3e180-153"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e180-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3e180-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3e180-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e180-155">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="3e180-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
