---
description: Gibt unter Verwendung der angegebenen 3D-Vektoren einen Punkt in der unter-/codezentrierten Koordinaten zurück.
ms.assetid: 572e151d-8044-480e-92b2-3f973d92d03e
title: D3DXVec3BaryCentric-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 3c14d01acc71a13cabb810d5b26d0afaf7f67f7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355809"
---
# <a name="d3dxvec3barycentric-function-d3dx10mathh"></a><span data-ttu-id="73853-103">D3DXVec3BaryCentric-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="73853-103">D3DXVec3BaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="73853-104">Gibt unter Verwendung der angegebenen 3D-Vektoren einen Punkt in der unter-/codezentrierten Koordinaten zurück.</span><span class="sxs-lookup"><span data-stu-id="73853-104">Returns a point in Barycentric coordinates, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="73853-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73853-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="73853-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73853-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73853-107">*Pout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73853-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73853-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="73853-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="73853-109">Zeiger auf das [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="73853-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="73853-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73853-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73853-111">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="73853-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="73853-112">Zeiger auf eine Quell-D3DXVECTOR3-Struktur.</span><span class="sxs-lookup"><span data-stu-id="73853-112">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="73853-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73853-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73853-114">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="73853-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="73853-115">Zeiger auf eine Quell-D3DXVECTOR3-Struktur.</span><span class="sxs-lookup"><span data-stu-id="73853-115">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="73853-116">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73853-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73853-117">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="73853-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="73853-118">Zeiger auf eine Quell-D3DXVECTOR3-Struktur.</span><span class="sxs-lookup"><span data-stu-id="73853-118">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="73853-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73853-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73853-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73853-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73853-121">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="73853-121">Weighting factor.</span></span> <span data-ttu-id="73853-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="73853-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="73853-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73853-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73853-124">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73853-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73853-125">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="73853-125">Weighting factor.</span></span> <span data-ttu-id="73853-126">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="73853-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73853-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73853-127">Return value</span></span>

<span data-ttu-id="73853-128">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="73853-128">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="73853-129">Zeiger auf eine D3DXVECTOR3-Struktur in den baryzentrierten Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="73853-129">Pointer to a D3DXVECTOR3 structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="73853-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73853-130">Remarks</span></span>

<span data-ttu-id="73853-131">Die D3DXVec3BaryCentric-Funktion bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet.</span><span class="sxs-lookup"><span data-stu-id="73853-131">The D3DXVec3BaryCentric function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="73853-132">Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: v1 + f (V2-V1) + g (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="73853-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="73853-133">Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (f, g) dargestellt werden. Mit dem Parameter f wird gesteuert, wie viel v2 in das Ergebnis gewichtet wird, und der Parameter g steuert, wie viel v3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="73853-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter f controls how much V2 gets weighted into the result and the parameter g controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="73853-134">Schließlich steuert 1-f-g, wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="73853-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="73853-135">Beachten Sie die folgenden Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="73853-135">Note the following relations.</span></span>

-   <span data-ttu-id="73853-136">Wenn (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), befindet sich der Punkt innerhalb des Dreiecks V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="73853-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="73853-137">Wenn (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), befindet sich der Punkt in der Zeile V1V3.</span><span class="sxs-lookup"><span data-stu-id="73853-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="73853-138">Wenn (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), befindet sich der Punkt in der Zeile v1v2.</span><span class="sxs-lookup"><span data-stu-id="73853-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="73853-139">Wenn (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), befindet sich der Punkt in der Zeile V2V3.</span><span class="sxs-lookup"><span data-stu-id="73853-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="73853-140">Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="73853-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="73853-141">In diesem Kontext stellt die Verwendung von barzentrischen Koordinaten eine Änderung in Koordinatensystemen dar.</span><span class="sxs-lookup"><span data-stu-id="73853-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="73853-142">Was für kartesische Koordinaten true ist, ist für barzentrierte Koordinaten "true".</span><span class="sxs-lookup"><span data-stu-id="73853-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="73853-143">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="73853-143">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="73853-144">Auf diese Weise kann die D3DXVec3BaryCentric-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73853-144">In this way, the D3DXVec3BaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="73853-145">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="73853-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="73853-146">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="73853-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="73853-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73853-147">Requirements</span></span>



| <span data-ttu-id="73853-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73853-148">Requirement</span></span> | <span data-ttu-id="73853-149">Wert</span><span class="sxs-lookup"><span data-stu-id="73853-149">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73853-150">Header</span><span class="sxs-lookup"><span data-stu-id="73853-150">Header</span></span><br/> | <dl> <span data-ttu-id="73853-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="73853-151"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73853-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73853-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73853-153">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="73853-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
