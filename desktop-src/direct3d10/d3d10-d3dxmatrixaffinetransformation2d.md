---
description: Erstellt eine 2D-affine-Transformationsmatrix in der x-y-Ebene. NULL-Argumente werden als Identitäts Transformationen behandelt.
ms.assetid: f46a307c-4566-42c8-8def-fb189116144e
title: D3DXMatrixAffineTransformation2D-Funktion (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 223ef5d2d9a68c993553d52f5d4cf63e8b95dd3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353394"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx10mathh"></a><span data-ttu-id="9cec1-104">D3DXMatrixAffineTransformation2D-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="9cec1-104">D3DXMatrixAffineTransformation2D function (D3DX10Math.h)</span></span>

<span data-ttu-id="9cec1-105">Erstellt eine 2D-affine-Transformationsmatrix in der x-y-Ebene.</span><span class="sxs-lookup"><span data-stu-id="9cec1-105">Builds a 2D affine transformation matrix in the x-y plane.</span></span> <span data-ttu-id="9cec1-106">**Null** -Argumente werden als Identitäts Transformationen behandelt.</span><span class="sxs-lookup"><span data-stu-id="9cec1-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cec1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cec1-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _In_       D3DXMATRIX  *pOut,
  _In_       FLOAT       Scaling,
  _In_ const D3DXVECTOR2 *pRotationCenter,
  _In_       FLOAT       Rotation,
  _In_ const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="9cec1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cec1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cec1-109">*Pout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9cec1-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cec1-110">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9cec1-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9cec1-111">Zeiger auf das [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="9cec1-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9cec1-112">*Skalieren* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9cec1-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cec1-113">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9cec1-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9cec1-114">Skalierungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="9cec1-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="9cec1-115">*protationcenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9cec1-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cec1-116">Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9cec1-116">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="9cec1-117">Zeiger auf ein [**D3DXVECTOR2**](d3d10-d3dxvector2.md), ein Punkt, der den Mittelpunkt der Drehung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9cec1-117">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="9cec1-118">Wenn dieses Argument **null** ist, wird eine identitätsm <sub>RC</sub> -Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="9cec1-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9cec1-119">*Drehung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9cec1-119">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cec1-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9cec1-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9cec1-121">Der Rotationswinkel.</span><span class="sxs-lookup"><span data-stu-id="9cec1-121">The angle of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="9cec1-122">*ptranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9cec1-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cec1-123">Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9cec1-123">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="9cec1-124">Zeiger auf ein [**D3DXVECTOR2**](d3d10-d3dxvector2.md)-Objekt, das die Übersetzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="9cec1-124">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), representing the translation.</span></span> <span data-ttu-id="9cec1-125">Wenn dieses Argument **null** ist, wird eine Identity MT-Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="9cec1-125">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cec1-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9cec1-126">Return value</span></span>

<span data-ttu-id="9cec1-127">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9cec1-127">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9cec1-128">Zeiger auf eine D3DXMATRIX-Struktur, die eine affine Transformationsmatrix ist.</span><span class="sxs-lookup"><span data-stu-id="9cec1-128">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cec1-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9cec1-129">Remarks</span></span>

<span data-ttu-id="9cec1-130">Diese Funktion berechnet die affine Transformationsmatrix mit der folgenden Formel, wobei die Matrix Verkettung in der Reihenfolge von links nach rechts ausgewertet wird:</span><span class="sxs-lookup"><span data-stu-id="9cec1-130">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="9cec1-131">M<sub>out</sub> = MS \* (m<sub>RC</sub>)-1 \* M<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="9cec1-131">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="9cec1-132">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="9cec1-132">where:</span></span>

<span data-ttu-id="9cec1-133">M<sub>out</sub> = Ausgabe Matrix (Pout)</span><span class="sxs-lookup"><span data-stu-id="9cec1-133">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="9cec1-134">MS = Skalierungs Matrix (Skalierung)</span><span class="sxs-lookup"><span data-stu-id="9cec1-134">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="9cec1-135">M<sub>RC</sub> = Mitte der Rotations Matrix (protationcenter)</span><span class="sxs-lookup"><span data-stu-id="9cec1-135">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="9cec1-136">M<sub>r</sub> = Rotations Matrix (Drehung)</span><span class="sxs-lookup"><span data-stu-id="9cec1-136">M<sub>r</sub> = rotation matrix (Rotation)</span></span>

<span data-ttu-id="9cec1-137">MT = Übersetzungs Matrix (ptranslation)</span><span class="sxs-lookup"><span data-stu-id="9cec1-137">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="9cec1-138">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9cec1-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9cec1-139">Auf diese Weise kann die D3DXMatrixAffineTransformation2D-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9cec1-139">In this way, the D3DXMatrixAffineTransformation2D function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9cec1-140">Verwenden Sie für 3D-affine Transformationen D3DXMatrixAffineTransformation.</span><span class="sxs-lookup"><span data-stu-id="9cec1-140">For 3D affine transformations, use D3DXMatrixAffineTransformation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cec1-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cec1-141">Requirements</span></span>



| <span data-ttu-id="9cec1-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cec1-142">Requirement</span></span> | <span data-ttu-id="9cec1-143">Wert</span><span class="sxs-lookup"><span data-stu-id="9cec1-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cec1-144">Header</span><span class="sxs-lookup"><span data-stu-id="9cec1-144">Header</span></span><br/>  | <dl> <span data-ttu-id="9cec1-145"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cec1-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9cec1-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9cec1-146">Library</span></span><br/> | <dl> <span data-ttu-id="9cec1-147"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9cec1-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9cec1-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cec1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cec1-149">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="9cec1-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
