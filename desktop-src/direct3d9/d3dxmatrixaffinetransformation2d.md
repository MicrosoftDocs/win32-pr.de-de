---
description: Erstellt eine 2D-affine-Transformationsmatrix in der XY-Ebene. NULL-Argumente werden als Identitäts Transformationen behandelt.
ms.assetid: 335de919-ae4d-405d-b6bb-ca6bdc2d568a
title: D3DXMatrixAffineTransformation2D-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6edd0658eb80ec53d19b6c136a672cb78a2087b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366453"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx9mathh"></a><span data-ttu-id="da2a1-104">D3DXMatrixAffineTransformation2D-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="da2a1-104">D3DXMatrixAffineTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="da2a1-105">Erstellt eine 2D-affine-Transformationsmatrix in der XY-Ebene.</span><span class="sxs-lookup"><span data-stu-id="da2a1-105">Builds a 2D affine transformation matrix in the xy plane.</span></span> <span data-ttu-id="da2a1-106">**Null** -Argumente werden als Identitäts Transformationen behandelt.</span><span class="sxs-lookup"><span data-stu-id="da2a1-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="da2a1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="da2a1-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_          FLOAT       Scaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="da2a1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="da2a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da2a1-109">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="da2a1-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="da2a1-110">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="da2a1-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="da2a1-111">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="da2a1-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="da2a1-112">*Skalieren* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da2a1-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da2a1-113">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da2a1-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da2a1-114">Skalierungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="da2a1-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="da2a1-115">*protationcenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da2a1-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da2a1-116">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="da2a1-116">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="da2a1-117">Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, ein Punkt, der den Mittelpunkt der Drehung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="da2a1-117">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="da2a1-118">Wenn dieses Argument **null** ist, wird eine identitätsm <sub>RC</sub> -Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="da2a1-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="da2a1-119">*Drehung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da2a1-119">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da2a1-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da2a1-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da2a1-121">Der Rotationswinkel.</span><span class="sxs-lookup"><span data-stu-id="da2a1-121">The angle of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="da2a1-122">*ptranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da2a1-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da2a1-123">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="da2a1-123">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="da2a1-124">Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die die Übersetzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="da2a1-124">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, representing the translation.</span></span> <span data-ttu-id="da2a1-125">Wenn dieses Argument **null** ist, wird eine Identity MT-Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="da2a1-125">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da2a1-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da2a1-126">Return value</span></span>

<span data-ttu-id="da2a1-127">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="da2a1-127">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="da2a1-128">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die eine affine Transformationsmatrix ist.</span><span class="sxs-lookup"><span data-stu-id="da2a1-128">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="da2a1-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da2a1-129">Remarks</span></span>

<span data-ttu-id="da2a1-130">Diese Funktion berechnet die affine Transformationsmatrix mit der folgenden Formel, wobei die Matrix Verkettung in der Reihenfolge von links nach rechts ausgewertet wird:</span><span class="sxs-lookup"><span data-stu-id="da2a1-130">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="da2a1-131">M<sub>out</sub> = MS \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* M<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="da2a1-131">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="da2a1-132">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="da2a1-132">where:</span></span>

<span data-ttu-id="da2a1-133">M <sub>out</sub> = Ausgabe Matrix (*Pout*)</span><span class="sxs-lookup"><span data-stu-id="da2a1-133">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="da2a1-134">MS = Skalierungs Matrix (*Skalierung*)</span><span class="sxs-lookup"><span data-stu-id="da2a1-134">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="da2a1-135">M <sub>RC</sub> = Mitte der Rotations Matrix (*protationcenter*)</span><span class="sxs-lookup"><span data-stu-id="da2a1-135">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="da2a1-136">M <sub>r</sub> = Rotations Matrix (*Drehung*)</span><span class="sxs-lookup"><span data-stu-id="da2a1-136">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="da2a1-137">MT = Übersetzungs Matrix (*ptranslation*)</span><span class="sxs-lookup"><span data-stu-id="da2a1-137">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="da2a1-138">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="da2a1-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="da2a1-139">Auf diese Weise kann die **D3DXMatrixAffineTransformation2D** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da2a1-139">In this way, the **D3DXMatrixAffineTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="da2a1-140">Verwenden Sie für 3D-affine Transformationen [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).</span><span class="sxs-lookup"><span data-stu-id="da2a1-140">For 3D affine transformations, use [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da2a1-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da2a1-141">Requirements</span></span>



| <span data-ttu-id="da2a1-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da2a1-142">Requirement</span></span> | <span data-ttu-id="da2a1-143">Wert</span><span class="sxs-lookup"><span data-stu-id="da2a1-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da2a1-144">Header</span><span class="sxs-lookup"><span data-stu-id="da2a1-144">Header</span></span><br/>  | <dl> <span data-ttu-id="da2a1-145"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="da2a1-145"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="da2a1-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="da2a1-146">Library</span></span><br/> | <dl> <span data-ttu-id="da2a1-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da2a1-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="da2a1-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da2a1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da2a1-149">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="da2a1-149">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="da2a1-150">**D3DXMatrixTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="da2a1-150">**D3DXMatrixTransformation2D**</span></span>](d3dxmatrixtransformation2d.md)
</dt> <dt>

[<span data-ttu-id="da2a1-151">Transformationen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="da2a1-151">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
