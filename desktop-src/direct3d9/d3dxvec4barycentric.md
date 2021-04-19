---
description: Gibt unter Verwendung der angegebenen 4D-Vektoren einen Punkt in der unter-/ein-basierten Koordinaten zurück.
ms.assetid: 80d73232-76bf-4f40-add2-dd1bdcc5cd98
title: D3DXVec4BaryCentric-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 75f0d068d1545f1b8b55dc3b976d3585e6f9bc88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355017"
---
# <a name="d3dxvec4barycentric-function-d3dx9mathh"></a><span data-ttu-id="55d60-103">D3DXVec4BaryCentric-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="55d60-103">D3DXVec4BaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="55d60-104">Gibt unter Verwendung der angegebenen 4D-Vektoren einen Punkt in der unter-/ein-basierten Koordinaten zurück.</span><span class="sxs-lookup"><span data-stu-id="55d60-104">Returns a point in Barycentric coordinates, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="55d60-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="55d60-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _Out_       D3DXVECTOR4 *pOut,
  _In_  const D3DXVECTOR4 *pV1,
  _In_  const D3DXVECTOR4 *pV2,
  _In_  const D3DXVECTOR4 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="55d60-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55d60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55d60-107">*Pout* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="55d60-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55d60-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="55d60-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="55d60-109">Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="55d60-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="55d60-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55d60-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55d60-111">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="55d60-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="55d60-112">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="55d60-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="55d60-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55d60-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55d60-114">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="55d60-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="55d60-115">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="55d60-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="55d60-116">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55d60-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55d60-117">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="55d60-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="55d60-118">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="55d60-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="55d60-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55d60-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55d60-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55d60-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55d60-121">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="55d60-121">Weighting factor.</span></span> <span data-ttu-id="55d60-122">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="55d60-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="55d60-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55d60-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55d60-124">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55d60-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55d60-125">Gewichtungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="55d60-125">Weighting factor.</span></span> <span data-ttu-id="55d60-126">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="55d60-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55d60-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55d60-127">Return value</span></span>

<span data-ttu-id="55d60-128">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="55d60-128">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="55d60-129">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur in den baryzentrierten Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="55d60-129">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="55d60-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55d60-130">Remarks</span></span>

<span data-ttu-id="55d60-131">Die **D3DXVec4BaryCentric** -Funktion bietet eine Möglichkeit, Punkte in und um ein Dreieck zu verstehen, unabhängig davon, wo sich das Dreieck tatsächlich befindet.</span><span class="sxs-lookup"><span data-stu-id="55d60-131">The **D3DXVec4BaryCentric** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="55d60-132">Diese Funktion gibt den resultierenden Punkt mithilfe der folgenden Gleichung zurück: v1 + f (V2-V1) + g (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="55d60-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="55d60-133">Jeder Punkt in der Ebene V1V2V3 kann durch die baryzentrische Koordinate (f, g) dargestellt werden. Mit dem Parameter *f* wird gesteuert, wie viel v2 in das Ergebnis gewichtet wird, und der Parameter *g* steuert, wie viel v3 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="55d60-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter *f* controls how much V2 gets weighted into the result and the parameter *g* controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="55d60-134">Schließlich steuert 1-f-g, wie viel V1 in das Ergebnis gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="55d60-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="55d60-135">Beachten Sie die folgenden Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="55d60-135">Note the following relations.</span></span>

-   <span data-ttu-id="55d60-136">Wenn (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), befindet sich der Punkt innerhalb des Dreiecks V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="55d60-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="55d60-137">Wenn (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), befindet sich der Punkt in der Zeile V1V3.</span><span class="sxs-lookup"><span data-stu-id="55d60-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="55d60-138">Wenn (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), befindet sich der Punkt in der Zeile v1v2.</span><span class="sxs-lookup"><span data-stu-id="55d60-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="55d60-139">Wenn (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), befindet sich der Punkt in der Zeile V2V3.</span><span class="sxs-lookup"><span data-stu-id="55d60-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="55d60-140">Baryzentrierte Koordinaten sind eine Form allgemeiner Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="55d60-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="55d60-141">In diesem Kontext stellt die Verwendung von barzentrischen Koordinaten eine Änderung in Koordinatensystemen dar.</span><span class="sxs-lookup"><span data-stu-id="55d60-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="55d60-142">Was für kartesische Koordinaten true ist, ist für barzentrierte Koordinaten "true".</span><span class="sxs-lookup"><span data-stu-id="55d60-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="55d60-143">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="55d60-143">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="55d60-144">Auf diese Weise kann die **D3DXVec4BaryCentric** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55d60-144">In this way, the **D3DXVec4BaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="55d60-145">In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert.</span><span class="sxs-lookup"><span data-stu-id="55d60-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="55d60-146">Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="55d60-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="55d60-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55d60-147">Requirements</span></span>



| <span data-ttu-id="55d60-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55d60-148">Requirement</span></span> | <span data-ttu-id="55d60-149">Wert</span><span class="sxs-lookup"><span data-stu-id="55d60-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55d60-150">Header</span><span class="sxs-lookup"><span data-stu-id="55d60-150">Header</span></span><br/>  | <dl> <span data-ttu-id="55d60-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="55d60-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="55d60-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="55d60-152">Library</span></span><br/> | <dl> <span data-ttu-id="55d60-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55d60-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="55d60-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55d60-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55d60-155">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="55d60-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
