---
description: 'D3DXVec4BaryCentric-Funktion (D3DX10Math.h): Gibt unter Verwendung der angegebenen 4D-Vektoren einen Punkt in baryzentrierten Koordinaten zurück.'
ms.assetid: 44406135-3270-4f2e-bb53-29affb2510f2
title: D3DXVec4BaryCentric-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 935432d1634a7fd35401d92471b1f366075ac8b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102988"
---
# <a name="d3dxvec4barycentric-function-d3dx10mathh"></a><span data-ttu-id="1c029-103">D3DXVec4BaryCentric-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="1c029-103">D3DXVec4BaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="1c029-104">Gibt unter Verwendung der angegebenen 4D-Vektoren einen Punkt in baryzentrierten Koordinaten zurück.</span><span class="sxs-lookup"><span data-stu-id="1c029-104">Returns a point in Barycentric coordinates, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c029-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c029-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _In_       D3DXVECTOR4 *pOut,
  _In_ const D3DXVECTOR4 *pV1,
  _In_ const D3DXVECTOR4 *pV2,
  _In_ const D3DXVECTOR4 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="1c029-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c029-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c029-107">*pOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1c029-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c029-108">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c029-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1c029-109">Zeiger auf [**D3DXVECTOR4,**](d3d10-d3dxvector4.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="1c029-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1c029-110">*pV1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1c029-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c029-111">Typ: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1c029-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1c029-112">Zeiger auf eine D3DXVECTOR4-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="1c029-112">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="1c029-113">*pV2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1c029-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c029-114">Typ: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1c029-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1c029-115">Zeiger auf eine D3DXVECTOR4-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="1c029-115">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="1c029-116">*pV3* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1c029-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c029-117">Typ: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1c029-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1c029-118">Zeiger auf eine D3DXVECTOR4-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="1c029-118">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="1c029-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c029-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c029-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c029-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c029-121">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="1c029-121">Weighting factor.</span></span> <span data-ttu-id="1c029-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="1c029-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1c029-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c029-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c029-124">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c029-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c029-125">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="1c029-125">Weighting factor.</span></span> <span data-ttu-id="1c029-126">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="1c029-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c029-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c029-127">Return value</span></span>

<span data-ttu-id="1c029-128">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c029-128">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1c029-129">Zeiger auf eine D3DXVECTOR4-Struktur in baryzentrischen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="1c029-129">Pointer to a D3DXVECTOR4 structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c029-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c029-130">Remarks</span></span>

<span data-ttu-id="1c029-131">Die D3DXVec4BaryCentric-Funktion bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet.</span><span class="sxs-lookup"><span data-stu-id="1c029-131">The D3DXVec4BaryCentric function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="1c029-132">Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: V1 + f(V2-V1) + g(V3-V1).</span><span class="sxs-lookup"><span data-stu-id="1c029-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="1c029-133">Jeder Punkt in der Ebene V1V2V3 kann durch die Barycentric-Koordinate (f,g) dargestellt werden. Der Parameter f steuert, wie viel V2 in das Ergebnis gewichtet wird, und der Parameter g steuert, wie viel V3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="1c029-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter f controls how much V2 gets weighted into the result and the parameter g controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="1c029-134">Schließlich steuert 1-f-g, wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="1c029-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="1c029-135">Beachten Sie die folgenden Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="1c029-135">Note the following relations.</span></span>

-   <span data-ttu-id="1c029-136">Wenn (f>=0 &, & g>=0 &, & 1-f-g>=0), befindet sich der Punkt innerhalb des Dreiecks V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="1c029-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="1c029-137">Wenn (f==0 &, & g>=0 &, & 1-f-g>=0), befindet sich der Punkt in der Zeile V1V3.</span><span class="sxs-lookup"><span data-stu-id="1c029-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="1c029-138">Wenn (f>=0 &, & g==0 &, & 1-f-g>=0), befindet sich der Punkt in der Zeile V1V2.</span><span class="sxs-lookup"><span data-stu-id="1c029-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="1c029-139">Wenn (f>=0 &, & g>=0 &, & 1-f-g==0), befindet sich der Punkt in der Zeile V2V3.</span><span class="sxs-lookup"><span data-stu-id="1c029-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="1c029-140">Barycentric-Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="1c029-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="1c029-141">In diesem Kontext stellt die Verwendung von Barycentric-Koordinaten eine Änderung der Koordinatensysteme dar.</span><span class="sxs-lookup"><span data-stu-id="1c029-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="1c029-142">Was für kartesische Koordinaten gilt, gilt für baryzentrische Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="1c029-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="1c029-143">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1c029-143">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1c029-144">Auf diese Weise kann die D3DXVec4BaryCentric-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c029-144">In this way, the D3DXVec4BaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1c029-145">Barycentric-Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkte des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="1c029-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="1c029-146">Eine ausführlichere Beschreibung der baryzentrischen Koordinaten finden Sie unter [Mathworld es Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="1c029-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c029-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c029-147">Requirements</span></span>



| <span data-ttu-id="1c029-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c029-148">Requirement</span></span> | <span data-ttu-id="1c029-149">Wert</span><span class="sxs-lookup"><span data-stu-id="1c029-149">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c029-150">Header</span><span class="sxs-lookup"><span data-stu-id="1c029-150">Header</span></span><br/> | <dl> <span data-ttu-id="1c029-151"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1c029-151"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c029-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1c029-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c029-153">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1c029-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
