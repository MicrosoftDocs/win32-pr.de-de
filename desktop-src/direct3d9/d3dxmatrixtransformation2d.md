---
description: 'D3DXMatrixTransformation2D-Funktion (D3dx9math.h): Erstellt eine 2D-Transformationsmatrix, die Transformationen in der XY-Ebene darstellt. NULL-Argumente werden als Identitätstransformationen behandelt.'
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: D3DXMatrixTransformation2D-Funktion (D3dx9math.h)
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
ms.openlocfilehash: b92a5489569765ef059af9b1023b40fc681b5d0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098118"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a><span data-ttu-id="387c1-104">D3DXMatrixTransformation2D-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="387c1-104">D3DXMatrixTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="387c1-105">Erstellt eine 2D-Transformationsmatrix, die Transformationen in der XY-Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="387c1-105">Builds a 2D transformation matrix that represents transformations in the xy plane.</span></span> <span data-ttu-id="387c1-106">**NULL-Argumente** werden als Identitätstransformationen behandelt.</span><span class="sxs-lookup"><span data-stu-id="387c1-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="387c1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="387c1-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="387c1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="387c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="387c1-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="387c1-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="387c1-110">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="387c1-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="387c1-111">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis der Transformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="387c1-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the result of the transformations.</span></span>

</dd> <dt>

<span data-ttu-id="387c1-112">*pScalingCenter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="387c1-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="387c1-113">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="387c1-113">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="387c1-114">Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) ein Punkt, der das Skalierungscenter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="387c1-114">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scaling center.</span></span> <span data-ttu-id="387c1-115">Wenn dieses Argument **NULL ist,** wird eine M <sub>sc-Matrix</sub> der Identität auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="387c1-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="387c1-116">*pScalingRotation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="387c1-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="387c1-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="387c1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="387c1-118">Der Skalierungsrotationsfaktor.</span><span class="sxs-lookup"><span data-stu-id="387c1-118">The scaling rotation factor.</span></span>

</dd> <dt>

<span data-ttu-id="387c1-119">*pScaling* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="387c1-119">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="387c1-120">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="387c1-120">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="387c1-121">Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) ein Punkt, der die Skala identifiziert.</span><span class="sxs-lookup"><span data-stu-id="387c1-121">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scale.</span></span> <span data-ttu-id="387c1-122">Wenn dieses Argument **NULL ist,** wird eine Ms-Identitätsmatrix auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="387c1-122">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="387c1-123">*pRotationCenter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="387c1-123">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="387c1-124">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="387c1-124">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="387c1-125">Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) ein Punkt, der den Drehmittelpunkt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="387c1-125">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the rotation center.</span></span> <span data-ttu-id="387c1-126">Wenn dieses Argument **NULL** ist, wird eine Rc-Matrix <sub></sub> für identität M auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="387c1-126">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="387c1-127">*Drehung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="387c1-127">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="387c1-128">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="387c1-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="387c1-129">Der Drehwinkel im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="387c1-129">The angle of rotation in radians.</span></span>

</dd> <dt>

<span data-ttu-id="387c1-130">*pTranslation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="387c1-130">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="387c1-131">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="387c1-131">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="387c1-132">Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die die Übersetzung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="387c1-132">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, identifying the translation.</span></span> <span data-ttu-id="387c1-133">Wenn dieses Argument **NULL** ist, wird eine Mt-Identitätsmatrix auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="387c1-133">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="387c1-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="387c1-134">Return value</span></span>

<span data-ttu-id="387c1-135">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="387c1-135">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="387c1-136">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Transformationsmatrix enthält.</span><span class="sxs-lookup"><span data-stu-id="387c1-136">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="387c1-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="387c1-137">Remarks</span></span>

<span data-ttu-id="387c1-138">Diese Funktion berechnet die Transformationsmatrix mit der folgenden Formel, wobei die Matrixverkettung in der Reihenfolge von links nach rechts ausgewertet wird:</span><span class="sxs-lookup"><span data-stu-id="387c1-138">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="387c1-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹ \* Ms \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="387c1-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹\* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="387c1-140">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="387c1-140">where:</span></span>

<span data-ttu-id="387c1-141">M <sub>out</sub> = Ausgabematrix (*pOut*)</span><span class="sxs-lookup"><span data-stu-id="387c1-141">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="387c1-142">M <sub>sc</sub> = Skalierungscentermatrix (*pScalingCenter*)</span><span class="sxs-lookup"><span data-stu-id="387c1-142">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="387c1-143">M <sub>sr</sub> = Skalierungsrotationsmatrix (*pScalingRotation*)</span><span class="sxs-lookup"><span data-stu-id="387c1-143">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="387c1-144">Ms =*Skalierungsmatrix ( pScaling*)</span><span class="sxs-lookup"><span data-stu-id="387c1-144">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="387c1-145">M <sub>rc</sub> = Mittelpunkt der Rotationsmatrix (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="387c1-145">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="387c1-146">M <sub>r</sub> = Drehungsmatrix (*Drehung*)</span><span class="sxs-lookup"><span data-stu-id="387c1-146">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="387c1-147">Mt = Übersetzungsmatrix (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="387c1-147">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="387c1-148">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="387c1-148">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="387c1-149">Auf diese Weise kann die **D3DXMatrixTransformation2D-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="387c1-149">In this way, the **D3DXMatrixTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="387c1-150">Verwenden Sie für 3D-Transformationen [**D3DXMatrixTransformation.**](d3dxmatrixtransformation.md)</span><span class="sxs-lookup"><span data-stu-id="387c1-150">For 3D transformations, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="387c1-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="387c1-151">Requirements</span></span>



| <span data-ttu-id="387c1-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="387c1-152">Requirement</span></span> | <span data-ttu-id="387c1-153">Wert</span><span class="sxs-lookup"><span data-stu-id="387c1-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="387c1-154">Header</span><span class="sxs-lookup"><span data-stu-id="387c1-154">Header</span></span><br/>  | <dl> <span data-ttu-id="387c1-155"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="387c1-155"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="387c1-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="387c1-156">Library</span></span><br/> | <dl> <span data-ttu-id="387c1-157"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="387c1-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="387c1-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="387c1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="387c1-159">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="387c1-159">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="387c1-160">**D3DXMatrixAffineTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="387c1-160">**D3DXMatrixAffineTransformation2D**</span></span>](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[<span data-ttu-id="387c1-161">Transformationen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="387c1-161">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
