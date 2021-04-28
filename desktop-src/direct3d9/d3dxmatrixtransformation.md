---
description: 'D3DXMatrixTransformation-Funktion (D3dx9math.h): Erstellt eine Transformationsmatrix. NULL-Argumente werden als Identitätstransformationen behandelt.'
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: D3DXMatrixTransformation-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc3b6502a8015564207f208166cec15227d3b18a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098128"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a><span data-ttu-id="0e9d1-104">D3DXMatrixTransformation-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="0e9d1-104">D3DXMatrixTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="0e9d1-105">Erstellt eine Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-105">Builds a transformation matrix.</span></span> <span data-ttu-id="0e9d1-106">**NULL-Argumente** werden als Identitätstransformationen behandelt.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9d1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e9d1-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="0e9d1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e9d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e9d1-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0e9d1-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9d1-110">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e9d1-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0e9d1-111">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0e9d1-112">*pScalingCenter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0e9d1-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9d1-113">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e9d1-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0e9d1-114">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die den Skalierungsmittelpunkt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the scaling center point.</span></span> <span data-ttu-id="0e9d1-115">Wenn dieses Argument **NULL ist,** wird eine M <sub>sc-Matrix</sub> der Identität auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0e9d1-116">*pScalingRotation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0e9d1-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9d1-117">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e9d1-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0e9d1-118">Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die die Skalierungsrotation angibt.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the scaling rotation.</span></span> <span data-ttu-id="0e9d1-119">Wenn dieses Argument **NULL ist,** wird eine M <sub>sr-Matrix der</sub> Identität auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0e9d1-120">*pScaling* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0e9d1-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9d1-121">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e9d1-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0e9d1-122">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) den Skalierungsvektor.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, the scaling vector.</span></span> <span data-ttu-id="0e9d1-123">Wenn dieses Argument **NULL** ist, wird eine Ms-Identitätsmatrix auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0e9d1-124">*pRotationCenter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0e9d1-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9d1-125">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e9d1-125">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0e9d1-126">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) ein Punkt, der den Mittelpunkt der Drehung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-126">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="0e9d1-127">Wenn dieses Argument **NULL** ist, wird eine M <sub>RC-Matrix</sub> der Identität auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0e9d1-128">*pRotation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0e9d1-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9d1-129">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e9d1-129">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0e9d1-130">Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die die Drehung angibt.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-130">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="0e9d1-131">Wenn dieses Argument **NULL** ist, wird eine M <sub>r-Identitätsmatrix</sub> auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0e9d1-132">*pTranslation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0e9d1-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9d1-133">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e9d1-133">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0e9d1-134">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Übersetzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-134">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, representing the translation.</span></span> <span data-ttu-id="0e9d1-135">Wenn dieses Argument **NULL** ist, wird eine Mt-Identitätsmatrix auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e9d1-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e9d1-136">Return value</span></span>

<span data-ttu-id="0e9d1-137">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e9d1-137">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0e9d1-138">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Transformationsmatrix ist.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-138">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e9d1-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e9d1-139">Remarks</span></span>

<span data-ttu-id="0e9d1-140">Diese Funktion berechnet die Transformationsmatrix mit der folgenden Formel, wobei die Matrixverkettung in der Reihenfolge von links nach rechts ausgewertet wird:</span><span class="sxs-lookup"><span data-stu-id="0e9d1-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="0e9d1-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹ \* Ms \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="0e9d1-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="0e9d1-142">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="0e9d1-142">where:</span></span>

<span data-ttu-id="0e9d1-143">M <sub>out</sub> = Ausgabematrix (*pOut*)</span><span class="sxs-lookup"><span data-stu-id="0e9d1-143">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="0e9d1-144">M <sub>sc</sub> = Skalierungscentermatrix (*pScalingCenter*)</span><span class="sxs-lookup"><span data-stu-id="0e9d1-144">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="0e9d1-145">M <sub>sr</sub> = Skalierungsrotationsmatrix (*pScalingRotation*)</span><span class="sxs-lookup"><span data-stu-id="0e9d1-145">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="0e9d1-146">Ms =*Skalierungsmatrix ( pScaling*)</span><span class="sxs-lookup"><span data-stu-id="0e9d1-146">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="0e9d1-147">M <sub>rc</sub> = Mittelpunkt der Rotationsmatrix (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="0e9d1-147">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="0e9d1-148">M <sub>r</sub> = Drehungsmatrix (*pRotation*)</span><span class="sxs-lookup"><span data-stu-id="0e9d1-148">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="0e9d1-149">Mt = Übersetzungsmatrix (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="0e9d1-149">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="0e9d1-150">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-150">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0e9d1-151">Auf diese Weise kann die **D3DXMatrixTransformation-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e9d1-151">In this way, the **D3DXMatrixTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0e9d1-152">Verwenden Sie für 2D-Transformationen [**D3DXMatrixTransformation2D.**](d3dxmatrixtransformation2d.md)</span><span class="sxs-lookup"><span data-stu-id="0e9d1-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e9d1-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e9d1-153">Requirements</span></span>



| <span data-ttu-id="0e9d1-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e9d1-154">Requirement</span></span> | <span data-ttu-id="0e9d1-155">Wert</span><span class="sxs-lookup"><span data-stu-id="0e9d1-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e9d1-156">Header</span><span class="sxs-lookup"><span data-stu-id="0e9d1-156">Header</span></span><br/>  | <dl> <span data-ttu-id="0e9d1-157"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0e9d1-157"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0e9d1-158">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e9d1-158">Library</span></span><br/> | <dl> <span data-ttu-id="0e9d1-159"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e9d1-159"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0e9d1-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0e9d1-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e9d1-161">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="0e9d1-161">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0e9d1-162">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="0e9d1-162">**D3DXMatrixAffineTransformation**</span></span>](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[<span data-ttu-id="0e9d1-163">Transformationen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0e9d1-163">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




