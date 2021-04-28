---
description: 'D3DXVec3BaryCentric-Funktion (D3DX10Math.h): Gibt unter Verwendung der angegebenen 3D-Vektoren einen Punkt in barycentric-Koordinaten zurück.'
ms.assetid: 572e151d-8044-480e-92b2-3f973d92d03e
title: D3DXVec3BaryCentric-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3BaryCentric
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: e350bde6d1b898088ccb9b68d10a9a346935bfd5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108248"
---
# <a name="d3dxvec3barycentric-function-d3dx10mathh"></a><span data-ttu-id="37081-103">D3DXVec3BaryCentric-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="37081-103">D3DXVec3BaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="37081-104">Gibt unter Verwendung der angegebenen 3D-Vektoren einen Punkt in Barycentric-Koordinaten zurück.</span><span class="sxs-lookup"><span data-stu-id="37081-104">Returns a point in Barycentric coordinates, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="37081-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37081-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3BaryCentric(
  _In_       D3DXVECTOR3 *pOut,
  _In_ const D3DXVECTOR3 *pV1,
  _In_ const D3DXVECTOR3 *pV2,
  _In_ const D3DXVECTOR3 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="37081-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="37081-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37081-107">*pOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="37081-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37081-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="37081-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37081-109">Zeiger auf [**D3DXVECTOR3,**](d3d10-d3dxvector3.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="37081-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="37081-110">*pV1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="37081-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37081-111">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="37081-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37081-112">Zeiger auf eine D3DXVECTOR3-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="37081-112">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="37081-113">*pV2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="37081-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37081-114">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="37081-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37081-115">Zeiger auf eine D3DXVECTOR3-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="37081-115">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="37081-116">*pV3* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="37081-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37081-117">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="37081-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37081-118">Zeiger auf eine D3DXVECTOR3-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="37081-118">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="37081-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37081-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37081-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37081-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37081-121">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="37081-121">Weighting factor.</span></span> <span data-ttu-id="37081-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="37081-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="37081-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37081-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37081-124">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37081-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37081-125">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="37081-125">Weighting factor.</span></span> <span data-ttu-id="37081-126">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="37081-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37081-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37081-127">Return value</span></span>

<span data-ttu-id="37081-128">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="37081-128">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37081-129">Zeiger auf eine D3DXVECTOR3-Struktur in baryzentrierten Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="37081-129">Pointer to a D3DXVECTOR3 structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="37081-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37081-130">Remarks</span></span>

<span data-ttu-id="37081-131">Die D3DXVec3BaryCentric-Funktion bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet.</span><span class="sxs-lookup"><span data-stu-id="37081-131">The D3DXVec3BaryCentric function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="37081-132">Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: V1 + f(V2-V1) + g(V3-V1).</span><span class="sxs-lookup"><span data-stu-id="37081-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="37081-133">Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrierte Koordinate (f,g) dargestellt werden. Der Parameter f steuert, wie viel V2 in das Ergebnis gewichtet wird, und der Parameter g steuert, wie viel V3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="37081-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter f controls how much V2 gets weighted into the result and the parameter g controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="37081-134">Schließlich steuert 1-f-g, wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="37081-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="37081-135">Beachten Sie die folgenden Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="37081-135">Note the following relations.</span></span>

-   <span data-ttu-id="37081-136">Wenn (f>=0 &, & g>=0 &, & 1-f-g>=0), befindet sich der Punkt innerhalb des Dreiecks V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="37081-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="37081-137">Wenn (f==0 &, & g>=0 &, & 1-f-g>=0), befindet sich der Punkt in der Zeile V1V3.</span><span class="sxs-lookup"><span data-stu-id="37081-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="37081-138">Wenn (f>=0 &, & g==0 &, & 1-f-g>=0), befindet sich der Punkt in der Zeile V1V2.</span><span class="sxs-lookup"><span data-stu-id="37081-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="37081-139">Wenn (f>=0 &, & g>=0 &, & 1-f-g==0), befindet sich der Punkt in der Zeile V2V3.</span><span class="sxs-lookup"><span data-stu-id="37081-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="37081-140">Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="37081-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="37081-141">In diesem Kontext stellt die Verwendung von baryzentrierten Koordinaten eine Änderung der Koordinatensysteme dar.</span><span class="sxs-lookup"><span data-stu-id="37081-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="37081-142">Was für kartesische Koordinaten zutrifft, gilt für baryzentrierte Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="37081-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="37081-143">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="37081-143">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="37081-144">Auf diese Weise kann die D3DXVec3BaryCentric-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37081-144">In this way, the D3DXVec3BaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="37081-145">Baryzentrierte Koordinaten definieren einen Punkt innerhalb eines Dreiecks in Bezug auf die Scheitelpunkt des Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="37081-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="37081-146">Eine detailliertere Beschreibung der baryzentrierten Koordinaten finden Sie unter [Beschreibung der baryzentrierten Koordinaten von Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)</span><span class="sxs-lookup"><span data-stu-id="37081-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="37081-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37081-147">Requirements</span></span>



| <span data-ttu-id="37081-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37081-148">Requirement</span></span> | <span data-ttu-id="37081-149">Wert</span><span class="sxs-lookup"><span data-stu-id="37081-149">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37081-150">Header</span><span class="sxs-lookup"><span data-stu-id="37081-150">Header</span></span><br/> | <dl> <span data-ttu-id="37081-151"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="37081-151"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37081-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="37081-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37081-153">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="37081-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
