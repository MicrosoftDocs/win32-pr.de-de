---
description: Erstellt eine Transformationsmatrix. NULL-Argumente werden als Identitäts Transformationen behandelt.
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: D3DXMatrixTransformation-Funktion (D3dx9math. h)
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
ms.openlocfilehash: f2174329e01e3e624ef27608ca56b33181b770db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050834"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a><span data-ttu-id="1a78c-104">D3DXMatrixTransformation-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1a78c-104">D3DXMatrixTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="1a78c-105">Erstellt eine Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="1a78c-105">Builds a transformation matrix.</span></span> <span data-ttu-id="1a78c-106">**Null** -Argumente werden als Identitäts Transformationen behandelt.</span><span class="sxs-lookup"><span data-stu-id="1a78c-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a78c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a78c-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1a78c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a78c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a78c-109">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1a78c-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a78c-110">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a78c-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1a78c-111">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="1a78c-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1a78c-112">*pscalingcenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a78c-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a78c-113">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a78c-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1a78c-114">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den Skalierungs Mittelpunkt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1a78c-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the scaling center point.</span></span> <span data-ttu-id="1a78c-115">Wenn dieses Argument **null** ist, wird eine identitätsm-<sub>SC</sub> -Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="1a78c-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1a78c-116">*pscalingrotation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a78c-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a78c-117">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a78c-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1a78c-118">Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die die Skalierungs Drehung angibt.</span><span class="sxs-lookup"><span data-stu-id="1a78c-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the scaling rotation.</span></span> <span data-ttu-id="1a78c-119">Wenn dieses Argument **null** ist, wird in den Hinweisen eine identitätsm <sub>SR</sub> -Matrix auf die Formel angewendet.</span><span class="sxs-lookup"><span data-stu-id="1a78c-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1a78c-120">*pscaling* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a78c-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a78c-121">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a78c-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1a78c-122">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, den Skalierungs Vektor.</span><span class="sxs-lookup"><span data-stu-id="1a78c-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, the scaling vector.</span></span> <span data-ttu-id="1a78c-123">Wenn dieses Argument **null** ist, wird eine Identitäts-MS-Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="1a78c-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1a78c-124">*protationcenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a78c-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a78c-125">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a78c-125">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1a78c-126">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, ein Punkt, der den Mittelpunkt der Drehung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1a78c-126">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="1a78c-127">Wenn dieses Argument **null** ist, wird eine identitätsm <sub>RC</sub> -Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="1a78c-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1a78c-128">*protation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a78c-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a78c-129">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a78c-129">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1a78c-130">Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die die Drehung angibt.</span><span class="sxs-lookup"><span data-stu-id="1a78c-130">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="1a78c-131">Wenn dieses Argument **null** ist, wird eine M <sub>r</sub> -Identitätsmatrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="1a78c-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1a78c-132">*ptranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a78c-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a78c-133">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a78c-133">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1a78c-134">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Übersetzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a78c-134">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, representing the translation.</span></span> <span data-ttu-id="1a78c-135">Wenn dieses Argument **null** ist, wird eine Identity MT-Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="1a78c-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a78c-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a78c-136">Return value</span></span>

<span data-ttu-id="1a78c-137">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a78c-137">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1a78c-138">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Transformationsmatrix ist.</span><span class="sxs-lookup"><span data-stu-id="1a78c-138">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a78c-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a78c-139">Remarks</span></span>

<span data-ttu-id="1a78c-140">Diese Funktion berechnet die Transformationsmatrix mit der folgenden Formel, wobei die Matrix Verkettung in der Reihenfolge von links nach rechts ausgewertet wird:</span><span class="sxs-lookup"><span data-stu-id="1a78c-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="1a78c-141">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* M<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="1a78c-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="1a78c-142">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="1a78c-142">where:</span></span>

<span data-ttu-id="1a78c-143">M <sub>out</sub> = Ausgabe Matrix (*Pout*)</span><span class="sxs-lookup"><span data-stu-id="1a78c-143">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="1a78c-144">M <sub>SC</sub> = Skalierungs Center Matrix (*pscalingcenter*)</span><span class="sxs-lookup"><span data-stu-id="1a78c-144">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="1a78c-145">M <sub>SR</sub> = Skalierungs Rotations Matrix (*pscalingrotation*)</span><span class="sxs-lookup"><span data-stu-id="1a78c-145">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="1a78c-146">MS = Skalierungs Matrix (*pscaling*)</span><span class="sxs-lookup"><span data-stu-id="1a78c-146">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="1a78c-147">M <sub>RC</sub> = Mitte der Rotations Matrix (*protationcenter*)</span><span class="sxs-lookup"><span data-stu-id="1a78c-147">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="1a78c-148">M <sub>r</sub> = Rotations Matrix (*protation*)</span><span class="sxs-lookup"><span data-stu-id="1a78c-148">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="1a78c-149">MT = Übersetzungs Matrix (*ptranslation*)</span><span class="sxs-lookup"><span data-stu-id="1a78c-149">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="1a78c-150">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1a78c-150">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1a78c-151">Auf diese Weise kann die **D3DXMatrixTransformation** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a78c-151">In this way, the **D3DXMatrixTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1a78c-152">Verwenden Sie [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md)für 2D-Transformationen.</span><span class="sxs-lookup"><span data-stu-id="1a78c-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a78c-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a78c-153">Requirements</span></span>



| <span data-ttu-id="1a78c-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a78c-154">Requirement</span></span> | <span data-ttu-id="1a78c-155">Wert</span><span class="sxs-lookup"><span data-stu-id="1a78c-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a78c-156">Header</span><span class="sxs-lookup"><span data-stu-id="1a78c-156">Header</span></span><br/>  | <dl> <span data-ttu-id="1a78c-157"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a78c-157"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1a78c-158">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1a78c-158">Library</span></span><br/> | <dl> <span data-ttu-id="1a78c-159"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a78c-159"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1a78c-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a78c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a78c-161">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1a78c-161">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1a78c-162">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="1a78c-162">**D3DXMatrixAffineTransformation**</span></span>](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[<span data-ttu-id="1a78c-163">Transformationen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1a78c-163">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




