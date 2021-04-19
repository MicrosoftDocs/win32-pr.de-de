---
description: Erstellt eine 3D-affine-Transformationsmatrix. NULL-Argumente werden als Identitäts Transformationen behandelt.
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: D3DXMatrixAffineTransformation-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 27fee5a620d75c3930b1bc2f8a85415db1320a47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350723"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a><span data-ttu-id="1a24a-104">D3DXMatrixAffineTransformation-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1a24a-104">D3DXMatrixAffineTransformation function (D3DX10Math.h)</span></span>

<span data-ttu-id="1a24a-105">Erstellt eine 3D-affine-Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="1a24a-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="1a24a-106">**Null** -Argumente werden als Identitäts Transformationen behandelt.</span><span class="sxs-lookup"><span data-stu-id="1a24a-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a24a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a24a-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="1a24a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a24a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a24a-109">*Pout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a24a-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a24a-110">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a24a-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1a24a-111">Zeiger auf das [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="1a24a-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1a24a-112">*Skalieren* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a24a-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a24a-113">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a24a-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a24a-114">Skalierungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="1a24a-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="1a24a-115">*protationcenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a24a-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a24a-116">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a24a-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1a24a-117">Zeiger auf ein [**D3DXVECTOR3**](d3d10-d3dxvector3.md), ein Punkt, der den Mittelpunkt der Drehung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1a24a-117">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="1a24a-118">Wenn dieses Argument **null** ist, wird eine identitätsm <sub>RC</sub> -Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="1a24a-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1a24a-119">*protation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a24a-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a24a-120">Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a24a-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1a24a-121">Zeiger auf ein [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) -Wert, der die Drehung angibt.</span><span class="sxs-lookup"><span data-stu-id="1a24a-121">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that specifies the rotation.</span></span> <span data-ttu-id="1a24a-122">Wenn dieses Argument **null** ist, wird eine M <sub>r</sub> -Identitätsmatrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="1a24a-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1a24a-123">*ptranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a24a-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a24a-124">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a24a-124">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1a24a-125">Zeiger auf eine D3DXVECTOR3-Struktur, die die Übersetzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a24a-125">Pointer to a D3DXVECTOR3 structure representing the translation.</span></span> <span data-ttu-id="1a24a-126">Wenn dieses Argument **null** ist, wird eine Identity MT-Matrix auf die Formel in den Hinweisen angewendet.</span><span class="sxs-lookup"><span data-stu-id="1a24a-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a24a-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a24a-127">Return value</span></span>

<span data-ttu-id="1a24a-128">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a24a-128">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1a24a-129">Zeiger auf eine D3DXMATRIX-Struktur, die eine affine Transformationsmatrix ist.</span><span class="sxs-lookup"><span data-stu-id="1a24a-129">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a24a-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a24a-130">Remarks</span></span>

<span data-ttu-id="1a24a-131">Diese Funktion berechnet die affine Transformationsmatrix mit der folgenden Formel, wobei die Matrix Verkettung in der Reihenfolge von links nach rechts ausgewertet wird:</span><span class="sxs-lookup"><span data-stu-id="1a24a-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="1a24a-132">M<sub>out</sub> = MS \* (m<sub>RC</sub>)-1 \* M<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="1a24a-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="1a24a-133">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="1a24a-133">where:</span></span>

<span data-ttu-id="1a24a-134">M<sub>out</sub> = Ausgabe Matrix (Pout)</span><span class="sxs-lookup"><span data-stu-id="1a24a-134">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="1a24a-135">MS = Skalierungs Matrix (Skalierung)</span><span class="sxs-lookup"><span data-stu-id="1a24a-135">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="1a24a-136">M<sub>RC</sub> = Mitte der Rotations Matrix (protationcenter)</span><span class="sxs-lookup"><span data-stu-id="1a24a-136">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="1a24a-137">M<sub>r</sub> = Rotations Matrix (protation)</span><span class="sxs-lookup"><span data-stu-id="1a24a-137">M<sub>r</sub> = rotation matrix (pRotation)</span></span>

<span data-ttu-id="1a24a-138">MT = Übersetzungs Matrix (ptranslation)</span><span class="sxs-lookup"><span data-stu-id="1a24a-138">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="1a24a-139">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1a24a-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1a24a-140">Auf diese Weise kann die D3DXMatrixAffineTransformation-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a24a-140">In this way, the D3DXMatrixAffineTransformation function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1a24a-141">Verwenden Sie für 2D-affine Transformationen D3DXMatrixAffineTransformation2D.</span><span class="sxs-lookup"><span data-stu-id="1a24a-141">For 2D affine transformations, use D3DXMatrixAffineTransformation2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a24a-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a24a-142">Requirements</span></span>



| <span data-ttu-id="1a24a-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a24a-143">Requirement</span></span> | <span data-ttu-id="1a24a-144">Wert</span><span class="sxs-lookup"><span data-stu-id="1a24a-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a24a-145">Header</span><span class="sxs-lookup"><span data-stu-id="1a24a-145">Header</span></span><br/>  | <dl> <span data-ttu-id="1a24a-146"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a24a-146"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1a24a-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1a24a-147">Library</span></span><br/> | <dl> <span data-ttu-id="1a24a-148"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a24a-148"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1a24a-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a24a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a24a-150">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1a24a-150">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
