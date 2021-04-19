---
description: Erstellt eine 2D-Transformationsmatrix, die Transformationen in der XY-Ebene darstellt. NULL-Argumente werden als Identitäts Transformationen behandelt.
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: D3DXMatrixTransformation2D-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ead4d403917b5328776b33563bc477c28983d6ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355184"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a><span data-ttu-id="57fb9-104">D3DXMatrixTransformation2D-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="57fb9-104">D3DXMatrixTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="57fb9-105">Erstellt eine 2D-Transformationsmatrix, die Transformationen in der XY-Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="57fb9-105">Builds a 2D transformation matrix that represents transformations in the xy plane.</span></span> <span data-ttu-id="57fb9-106">**Null** -Argumente werden als Identitäts Transformationen behandelt.</span><span class="sxs-lookup"><span data-stu-id="57fb9-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="57fb9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="57fb9-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       pScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="57fb9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="57fb9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57fb9-109">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="57fb9-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="57fb9-110">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="57fb9-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="57fb9-111">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis der Transformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="57fb9-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the result of the transformations.</span></span>

</dd> <dt>

<span data-ttu-id="57fb9-112">*pscalingcenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57fb9-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57fb9-113">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="57fb9-113">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="57fb9-114">Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, ein Punkt, der die Skalierungs Mitte identifiziert.</span><span class="sxs-lookup"><span data-stu-id="57fb9-114">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scaling center.</span></span> <span data-ttu-id="57fb9-115">Wenn dieses Argument **null** ist, wird eine identitätsm-<sub>SC</sub> -Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="57fb9-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="57fb9-116">*pscalingrotation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57fb9-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57fb9-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57fb9-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="57fb9-118">Der Faktor für die Skalierungs Drehung.</span><span class="sxs-lookup"><span data-stu-id="57fb9-118">The scaling rotation factor.</span></span>

</dd> <dt>

<span data-ttu-id="57fb9-119">*pscaling* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57fb9-119">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57fb9-120">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="57fb9-120">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="57fb9-121">Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, ein Punkt, der die Skala identifiziert.</span><span class="sxs-lookup"><span data-stu-id="57fb9-121">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scale.</span></span> <span data-ttu-id="57fb9-122">Wenn dieses Argument **null** ist, wird eine Identitäts-MS-Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="57fb9-122">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="57fb9-123">*protationcenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57fb9-123">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57fb9-124">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="57fb9-124">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="57fb9-125">Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, ein Punkt, der das Drehzentrum identifiziert.</span><span class="sxs-lookup"><span data-stu-id="57fb9-125">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the rotation center.</span></span> <span data-ttu-id="57fb9-126">Wenn dieses Argument **null** ist, wird eine identitätsm <sub>RC</sub> -Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="57fb9-126">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="57fb9-127">*Drehung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57fb9-127">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57fb9-128">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57fb9-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="57fb9-129">Der Drehwinkel im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="57fb9-129">The angle of rotation in radians.</span></span>

</dd> <dt>

<span data-ttu-id="57fb9-130">*ptranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57fb9-130">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57fb9-131">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="57fb9-131">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="57fb9-132">Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die die Übersetzung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="57fb9-132">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, identifying the translation.</span></span> <span data-ttu-id="57fb9-133">Wenn dieses Argument **null** ist, wird eine Identity MT-Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="57fb9-133">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57fb9-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57fb9-134">Return value</span></span>

<span data-ttu-id="57fb9-135">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="57fb9-135">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="57fb9-136">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Transformationsmatrix enthält.</span><span class="sxs-lookup"><span data-stu-id="57fb9-136">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="57fb9-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57fb9-137">Remarks</span></span>

<span data-ttu-id="57fb9-138">Diese Funktion berechnet die Transformationsmatrix mit der folgenden Formel, wobei die Matrix Verkettung in der Reihenfolge von links nach rechts ausgewertet wird:</span><span class="sxs-lookup"><span data-stu-id="57fb9-138">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="57fb9-139">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* M<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="57fb9-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹\* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="57fb9-140">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="57fb9-140">where:</span></span>

<span data-ttu-id="57fb9-141">M <sub>out</sub> = Ausgabe Matrix (*Pout*)</span><span class="sxs-lookup"><span data-stu-id="57fb9-141">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="57fb9-142">M <sub>SC</sub> = Skalierungs Center Matrix (*pscalingcenter*)</span><span class="sxs-lookup"><span data-stu-id="57fb9-142">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="57fb9-143">M <sub>SR</sub> = Skalierungs Rotations Matrix (*pscalingrotation*)</span><span class="sxs-lookup"><span data-stu-id="57fb9-143">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="57fb9-144">MS = Skalierungs Matrix (*pscaling*)</span><span class="sxs-lookup"><span data-stu-id="57fb9-144">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="57fb9-145">M <sub>RC</sub> = Mitte der Rotations Matrix (*protationcenter*)</span><span class="sxs-lookup"><span data-stu-id="57fb9-145">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="57fb9-146">M <sub>r</sub> = Rotations Matrix (*Drehung*)</span><span class="sxs-lookup"><span data-stu-id="57fb9-146">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="57fb9-147">MT = Übersetzungs Matrix (*ptranslation*)</span><span class="sxs-lookup"><span data-stu-id="57fb9-147">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="57fb9-148">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="57fb9-148">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="57fb9-149">Auf diese Weise kann die **D3DXMatrixTransformation2D** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57fb9-149">In this way, the **D3DXMatrixTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="57fb9-150">Verwenden Sie für 3D-Transformationen [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span><span class="sxs-lookup"><span data-stu-id="57fb9-150">For 3D transformations, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57fb9-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57fb9-151">Requirements</span></span>



| <span data-ttu-id="57fb9-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57fb9-152">Requirement</span></span> | <span data-ttu-id="57fb9-153">Wert</span><span class="sxs-lookup"><span data-stu-id="57fb9-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57fb9-154">Header</span><span class="sxs-lookup"><span data-stu-id="57fb9-154">Header</span></span><br/>  | <dl> <span data-ttu-id="57fb9-155"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="57fb9-155"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="57fb9-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="57fb9-156">Library</span></span><br/> | <dl> <span data-ttu-id="57fb9-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57fb9-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="57fb9-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57fb9-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57fb9-159">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="57fb9-159">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="57fb9-160">**D3DXMatrixAffineTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="57fb9-160">**D3DXMatrixAffineTransformation2D**</span></span>](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[<span data-ttu-id="57fb9-161">Transformationen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="57fb9-161">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
