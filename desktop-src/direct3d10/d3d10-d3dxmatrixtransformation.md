---
description: 'D3DXMatrixTransformation-Funktion (D3DX10Math.h): Erstellt eine Transformationsmatrix. NULL-Argumente werden als Identitätstransformationen behandelt.'
ms.assetid: 99c75ce9-3683-4753-b635-760eb8aaf46e
title: D3DXMatrixTransformation-Funktion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 10ed63b292dd69acb58d8567e6336b5aab4f7997
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108898"
---
# <a name="d3dxmatrixtransformation-function-d3dx10mathh"></a><span data-ttu-id="21eb3-104">D3DXMatrixTransformation-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="21eb3-104">D3DXMatrixTransformation function (D3DX10Math.h)</span></span>

<span data-ttu-id="21eb3-105">Erstellt eine Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="21eb3-105">Builds a transformation matrix.</span></span> <span data-ttu-id="21eb3-106">**NULL-Argumente** werden als Identitätstransformationen behandelt.</span><span class="sxs-lookup"><span data-stu-id="21eb3-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="21eb3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="21eb3-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="21eb3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="21eb3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21eb3-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="21eb3-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="21eb3-110">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="21eb3-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="21eb3-111">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="21eb3-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="21eb3-112">*pScalingCenter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="21eb3-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21eb3-113">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="21eb3-113">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="21eb3-114">Zeiger auf einen [**D3DXVECTOR3,**](d3d10-d3dxvector3.md)der den Mittelpunkt der Skalierung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="21eb3-114">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the scaling center point.</span></span> <span data-ttu-id="21eb3-115">Wenn dieses Argument **NULL** ist, wird eine M <sub>sc-Identitätsmatrix</sub> auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="21eb3-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="21eb3-116">*pScalingRotation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="21eb3-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21eb3-117">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="21eb3-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="21eb3-118">Zeiger auf ein [**D3DXQUATERNION-Element,**](d3d10-d3dxquaternion.md) das die Skalierungsrotation angibt.</span><span class="sxs-lookup"><span data-stu-id="21eb3-118">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that specifies the scaling rotation.</span></span> <span data-ttu-id="21eb3-119">Wenn dieses Argument **NULL** ist, wird eine M <sub>SR-Identitätsmatrix</sub> auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="21eb3-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="21eb3-120">*pScaling* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="21eb3-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21eb3-121">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="21eb3-121">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="21eb3-122">Zeiger auf eine D3DXVECTOR3-Struktur, den Skalierungsvektor.</span><span class="sxs-lookup"><span data-stu-id="21eb3-122">Pointer to a D3DXVECTOR3 structure, the scaling vector.</span></span> <span data-ttu-id="21eb3-123">Wenn dieses Argument **NULL ist,** wird eine Ms-Identitätsmatrix auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="21eb3-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="21eb3-124">*pRotationCenter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="21eb3-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21eb3-125">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="21eb3-125">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="21eb3-126">Zeiger auf eine D3DXVECTOR3-Struktur, ein Punkt, der den Mittelpunkt der Drehung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="21eb3-126">Pointer to a D3DXVECTOR3 structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="21eb3-127">Wenn dieses Argument **NULL ist,** wird eine M <sub>RC-Matrix</sub> der Identität auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="21eb3-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="21eb3-128">*pRotation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="21eb3-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21eb3-129">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="21eb3-129">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="21eb3-130">Zeiger auf eine D3DXQUATERNION-Struktur, die die Drehung angibt.</span><span class="sxs-lookup"><span data-stu-id="21eb3-130">Pointer to a D3DXQUATERNION structure that specifies the rotation.</span></span> <span data-ttu-id="21eb3-131">Wenn dieses Argument **NULL ist,** wird eine M <sub>r-Matrix</sub> der Identität auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="21eb3-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="21eb3-132">*pTranslation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="21eb3-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21eb3-133">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="21eb3-133">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="21eb3-134">Zeiger auf eine D3DXVECTOR3-Struktur, die die Übersetzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="21eb3-134">Pointer to a D3DXVECTOR3 structure, representing the translation.</span></span> <span data-ttu-id="21eb3-135">Wenn dieses Argument **NULL ist,** wird eine Identitäts-Mt-Matrix auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="21eb3-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21eb3-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21eb3-136">Return value</span></span>

<span data-ttu-id="21eb3-137">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="21eb3-137">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="21eb3-138">Zeiger auf eine D3DXMATRIX-Struktur, die die Transformationsmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="21eb3-138">Pointer to a D3DXMATRIX structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="21eb3-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21eb3-139">Remarks</span></span>

<span data-ttu-id="21eb3-140">Diese Funktion berechnet die Transformationsmatrix mit der folgenden Formel, bei der die Matrixverkettung in der Reihenfolge von links nach rechts ausgewertet wird:</span><span class="sxs-lookup"><span data-stu-id="21eb3-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="21eb3-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻. \* (M<sub>sr</sub>)⁻. Ms \* M \* <sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻. \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="21eb3-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="21eb3-142">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="21eb3-142">where:</span></span>

<span data-ttu-id="21eb3-143">M<sub>out</sub> = Ausgabematrix (pOut)</span><span class="sxs-lookup"><span data-stu-id="21eb3-143">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="21eb3-144">M<sub>sc</sub> = Skalierungscentermatrix (pScalingCenter)</span><span class="sxs-lookup"><span data-stu-id="21eb3-144">M<sub>sc</sub> = scaling center matrix (pScalingCenter)</span></span>

<span data-ttu-id="21eb3-145">M<sub>sr</sub> = Skalierungsrotationsmatrix (pScalingRotation)</span><span class="sxs-lookup"><span data-stu-id="21eb3-145">M<sub>sr</sub> = scaling rotation matrix (pScalingRotation)</span></span>

<span data-ttu-id="21eb3-146">Ms = Skalierungsmatrix (pScaling)</span><span class="sxs-lookup"><span data-stu-id="21eb3-146">Mₛ = scaling matrix (pScaling)</span></span>

<span data-ttu-id="21eb3-147">M<sub>rc</sub> = Mittelpunkt der Rotationsmatrix (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="21eb3-147">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="21eb3-148">M<sub>r</sub> = Rotationsmatrix (pRotation)</span><span class="sxs-lookup"><span data-stu-id="21eb3-148">M<sub>r</sub> = rotation matrix (pRotation)</span></span>

<span data-ttu-id="21eb3-149">Mt = Übersetzungsmatrix (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="21eb3-149">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="21eb3-150">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="21eb3-150">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="21eb3-151">Auf diese Weise kann die D3DXMatrixTransformation-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21eb3-151">In this way, the D3DXMatrixTransformation function can be used as a parameter for another function.</span></span>

<span data-ttu-id="21eb3-152">Verwenden Sie für 2D-Transformationen [**D3DXMatrixTransformation2D.**](d3d10-d3dxmatrixtransformation2d.md)</span><span class="sxs-lookup"><span data-stu-id="21eb3-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3d10-d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21eb3-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21eb3-153">Requirements</span></span>



| <span data-ttu-id="21eb3-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21eb3-154">Requirement</span></span> | <span data-ttu-id="21eb3-155">Wert</span><span class="sxs-lookup"><span data-stu-id="21eb3-155">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21eb3-156">Header</span><span class="sxs-lookup"><span data-stu-id="21eb3-156">Header</span></span><br/>  | <dl> <span data-ttu-id="21eb3-157"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="21eb3-157"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="21eb3-158">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="21eb3-158">Library</span></span><br/> | <dl> <span data-ttu-id="21eb3-159"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="21eb3-159"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21eb3-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="21eb3-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21eb3-161">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="21eb3-161">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
