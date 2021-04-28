---
description: 'D3DXMatrixAffineTransformation-Funktion (D3DX10Math.h): Erstellt eine 3D-affine Transformationsmatrix. NULL-Argumente werden als Identitätstransformationen behandelt.'
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: D3DXMatrixAffineTransformation-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01c6b3c3ffe2de9b7c7003b78f1b07a0f35cc3a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113178"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a><span data-ttu-id="5ab5d-104">D3DXMatrixAffineTransformation-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="5ab5d-104">D3DXMatrixAffineTransformation function (D3DX10Math.h)</span></span>

<span data-ttu-id="5ab5d-105">Erstellt eine 3D-affine Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="5ab5d-106">**NULL-Argumente** werden als Identitätstransformationen behandelt.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab5d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ab5d-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="5ab5d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ab5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ab5d-109">*pOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ab5d-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab5d-110">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ab5d-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ab5d-111">Zeiger auf die [**D3DXMATRIX,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ab5d-112">*Skalierung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ab5d-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab5d-113">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ab5d-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ab5d-114">Skalierungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="5ab5d-115">*pRotationCenter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ab5d-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab5d-116">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ab5d-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5ab5d-117">Zeiger auf ein [**D3DXVECTOR3**](d3d10-d3dxvector3.md), ein Punkt, der den Mittelpunkt der Drehung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-117">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="5ab5d-118">Wenn dieses Argument **NULL** ist, wird eine Rc-Matrix <sub></sub> für identität M auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5ab5d-119">*pRotation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ab5d-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab5d-120">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ab5d-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5ab5d-121">Zeiger auf ein [**D3DXQUATERNION-Element,**](d3d10-d3dxquaternion.md) das die Drehung angibt.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-121">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that specifies the rotation.</span></span> <span data-ttu-id="5ab5d-122">Wenn dieses Argument **NULL** ist, wird eine M <sub>r-Identitätsmatrix</sub> auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5ab5d-123">*pTranslation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5ab5d-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab5d-124">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ab5d-124">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5ab5d-125">Zeiger auf eine D3DXVECTOR3-Struktur, die die Übersetzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-125">Pointer to a D3DXVECTOR3 structure representing the translation.</span></span> <span data-ttu-id="5ab5d-126">Wenn dieses Argument **NULL ist,** wird eine Identitäts-Mt-Matrix auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ab5d-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ab5d-127">Return value</span></span>

<span data-ttu-id="5ab5d-128">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ab5d-128">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ab5d-129">Zeiger auf eine D3DXMATRIX-Struktur, die eine affine Transformationsmatrix ist.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-129">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ab5d-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ab5d-130">Remarks</span></span>

<span data-ttu-id="5ab5d-131">Diese Funktion berechnet die affine Transformationsmatrix mit der folgenden Formel, bei der die Matrixverkettung in der Reihenfolge von links nach rechts ausgewertet wird:</span><span class="sxs-lookup"><span data-stu-id="5ab5d-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="5ab5d-132">M<sub>out</sub> = Ms \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="5ab5d-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="5ab5d-133">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="5ab5d-133">where:</span></span>

<span data-ttu-id="5ab5d-134">M<sub>out</sub> = Ausgabematrix (pOut)</span><span class="sxs-lookup"><span data-stu-id="5ab5d-134">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="5ab5d-135">Ms = Skalierungsmatrix (Skalierung)</span><span class="sxs-lookup"><span data-stu-id="5ab5d-135">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="5ab5d-136">M<sub>rc</sub> = Mitte der Rotationsmatrix (pRotationCenter)</span><span class="sxs-lookup"><span data-stu-id="5ab5d-136">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="5ab5d-137">M<sub>r</sub> = Rotationsmatrix (pRotation)</span><span class="sxs-lookup"><span data-stu-id="5ab5d-137">M<sub>r</sub> = rotation matrix (pRotation)</span></span>

<span data-ttu-id="5ab5d-138">Mt = Übersetzungsmatrix (pTranslation)</span><span class="sxs-lookup"><span data-stu-id="5ab5d-138">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="5ab5d-139">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5ab5d-140">Auf diese Weise kann die D3DXMatrixAffineTransformation-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-140">In this way, the D3DXMatrixAffineTransformation function can be used as a parameter for another function.</span></span>

<span data-ttu-id="5ab5d-141">Verwenden Sie für 2D-affine Transformationen D3DXMatrixAffineTransformation2D.</span><span class="sxs-lookup"><span data-stu-id="5ab5d-141">For 2D affine transformations, use D3DXMatrixAffineTransformation2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ab5d-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ab5d-142">Requirements</span></span>



| <span data-ttu-id="5ab5d-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ab5d-143">Requirement</span></span> | <span data-ttu-id="5ab5d-144">Wert</span><span class="sxs-lookup"><span data-stu-id="5ab5d-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab5d-145">Header</span><span class="sxs-lookup"><span data-stu-id="5ab5d-145">Header</span></span><br/>  | <dl> <span data-ttu-id="5ab5d-146"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5ab5d-146"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5ab5d-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5ab5d-147">Library</span></span><br/> | <dl> <span data-ttu-id="5ab5d-148"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ab5d-148"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5ab5d-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5ab5d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab5d-150">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5ab5d-150">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
