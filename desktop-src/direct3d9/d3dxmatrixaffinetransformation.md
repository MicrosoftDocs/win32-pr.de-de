---
description: 'D3DXMatrixAffineTransformation-Funktion (D3dx9math.h): Erstellt eine 3D-affine Transformationsmatrix. NULL-Argumente werden als Identitätstransformationen behandelt.'
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: D3DXMatrixAffineTransformation-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7329ffbffe5ffd89ed64e5386246f39699618960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094168"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a><span data-ttu-id="f8c93-104">D3DXMatrixAffineTransformation-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="f8c93-104">D3DXMatrixAffineTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="f8c93-105">Erstellt eine 3D-affine Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="f8c93-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="f8c93-106">**NULL-Argumente** werden als Identitätstransformationen behandelt.</span><span class="sxs-lookup"><span data-stu-id="f8c93-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c93-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8c93-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="f8c93-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8c93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8c93-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f8c93-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c93-110">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8c93-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f8c93-111">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="f8c93-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f8c93-112">*Skalierung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f8c93-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c93-113">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8c93-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8c93-114">Skalierungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="f8c93-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="f8c93-115">*pRotationCenter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f8c93-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c93-116">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8c93-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f8c93-117">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) ein Punkt, der den Mittelpunkt der Drehung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f8c93-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="f8c93-118">Wenn dieses Argument **NULL** ist, wird eine Rc-Matrix <sub></sub> für identität M auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="f8c93-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f8c93-119">*pRotation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f8c93-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c93-120">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8c93-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f8c93-121">Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die die Drehung angibt.</span><span class="sxs-lookup"><span data-stu-id="f8c93-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="f8c93-122">Wenn dieses Argument **NULL** ist, wird eine M <sub>r-Identitätsmatrix</sub> auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="f8c93-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f8c93-123">*pTranslation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f8c93-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c93-124">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8c93-124">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f8c93-125">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Übersetzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="f8c93-125">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure representing the translation.</span></span> <span data-ttu-id="f8c93-126">Wenn dieses Argument **NULL ist,** wird eine Identitäts-Mt-Matrix auf die Formel in "Hinweise" angewendet.</span><span class="sxs-lookup"><span data-stu-id="f8c93-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8c93-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8c93-127">Return value</span></span>

<span data-ttu-id="f8c93-128">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8c93-128">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f8c93-129">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die eine affine Transformationsmatrix ist.</span><span class="sxs-lookup"><span data-stu-id="f8c93-129">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8c93-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8c93-130">Remarks</span></span>

<span data-ttu-id="f8c93-131">Diese Funktion berechnet die affine Transformationsmatrix mit der folgenden Formel, bei der die Matrixverkettung in der Reihenfolge von links nach rechts ausgewertet wird:</span><span class="sxs-lookup"><span data-stu-id="f8c93-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="f8c93-132">M<sub>out</sub> = Ms \* (M<sub>rc</sub>)⁻. \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span><span class="sxs-lookup"><span data-stu-id="f8c93-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="f8c93-133">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="f8c93-133">where:</span></span>

<span data-ttu-id="f8c93-134">M <sub>out</sub> = Ausgabematrix (*pOut*)</span><span class="sxs-lookup"><span data-stu-id="f8c93-134">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="f8c93-135">Ms = Skalierungsmatrix (*Skalierung*)</span><span class="sxs-lookup"><span data-stu-id="f8c93-135">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="f8c93-136">M <sub>rc</sub> = Mitte der Rotationsmatrix (*pRotationCenter*)</span><span class="sxs-lookup"><span data-stu-id="f8c93-136">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="f8c93-137">M <sub>r</sub> = Rotationsmatrix (*pRotation*)</span><span class="sxs-lookup"><span data-stu-id="f8c93-137">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="f8c93-138">Mt = Übersetzungsmatrix (*pTranslation*)</span><span class="sxs-lookup"><span data-stu-id="f8c93-138">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="f8c93-139">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f8c93-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f8c93-140">Auf diese Weise kann die **D3DXMatrixAffineTransformation-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8c93-140">In this way, the **D3DXMatrixAffineTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f8c93-141">Verwenden Sie für 2D-affine Transformationen [**D3DXMatrixAffineTransformation2D.**](d3dxmatrixaffinetransformation2d.md)</span><span class="sxs-lookup"><span data-stu-id="f8c93-141">For 2D affine transformations, use [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c93-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8c93-142">Requirements</span></span>



| <span data-ttu-id="f8c93-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8c93-143">Requirement</span></span> | <span data-ttu-id="f8c93-144">Wert</span><span class="sxs-lookup"><span data-stu-id="f8c93-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c93-145">Header</span><span class="sxs-lookup"><span data-stu-id="f8c93-145">Header</span></span><br/>  | <dl> <span data-ttu-id="f8c93-146"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f8c93-146"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f8c93-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f8c93-147">Library</span></span><br/> | <dl> <span data-ttu-id="f8c93-148"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8c93-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8c93-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f8c93-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c93-150">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="f8c93-150">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f8c93-151">**D3DXMatrixTransformation**</span><span class="sxs-lookup"><span data-stu-id="f8c93-151">**D3DXMatrixTransformation**</span></span>](d3dxmatrixtransformation.md)
</dt> <dt>

[<span data-ttu-id="f8c93-152">Transformationen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f8c93-152">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
