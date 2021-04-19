---
description: Erstellt eine angepasste, Links vergebene orthografische Projektions Matrix.
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: D3DXMatrixOrthoOffCenterLH-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4292f2996b4a19b71531094e5bf39bf7c213b972
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350708"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a><span data-ttu-id="76ca2-103">D3DXMatrixOrthoOffCenterLH-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="76ca2-103">D3DXMatrixOrthoOffCenterLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="76ca2-104">Erstellt eine angepasste, Links vergebene orthografische Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="76ca2-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ca2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76ca2-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="76ca2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76ca2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76ca2-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="76ca2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76ca2-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="76ca2-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="76ca2-109">Zeiger auf das resultierende [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="76ca2-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="76ca2-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76ca2-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ca2-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76ca2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76ca2-112">Minimaler x-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="76ca2-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="76ca2-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76ca2-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ca2-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76ca2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76ca2-115">Maximaler x-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="76ca2-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="76ca2-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76ca2-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ca2-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76ca2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76ca2-118">Minimaler y-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="76ca2-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="76ca2-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76ca2-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ca2-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76ca2-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76ca2-121">Maximaler y-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="76ca2-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="76ca2-122">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76ca2-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ca2-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76ca2-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76ca2-124">Der minimale z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="76ca2-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="76ca2-125">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76ca2-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ca2-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76ca2-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76ca2-127">Maximaler z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="76ca2-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76ca2-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76ca2-128">Return value</span></span>

<span data-ttu-id="76ca2-129">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="76ca2-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="76ca2-130">Zeiger auf das resultierende [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="76ca2-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="76ca2-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76ca2-131">Remarks</span></span>

<span data-ttu-id="76ca2-132">[**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) ist ein Sonderfall der D3DXMatrixOrthoOffCenterLH-Funktion.</span><span class="sxs-lookup"><span data-stu-id="76ca2-132">The [**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) is a special case of the D3DXMatrixOrthoOffCenterLH function.</span></span> <span data-ttu-id="76ca2-133">Verwenden Sie die folgenden Werte, um dieselbe Projektion mithilfe von D3DXMatrixOrthoOffCenterLH zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="76ca2-133">To create the same projection using D3DXMatrixOrthoOffCenterLH, use the following values:</span></span>

<span data-ttu-id="76ca2-134">l =-w/2,</span><span class="sxs-lookup"><span data-stu-id="76ca2-134">l = -w/2,</span></span>

<span data-ttu-id="76ca2-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="76ca2-135">r = w/2,</span></span>

<span data-ttu-id="76ca2-136">b =-h/2, und</span><span class="sxs-lookup"><span data-stu-id="76ca2-136">b = -h/2, and</span></span>

<span data-ttu-id="76ca2-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="76ca2-137">t = h/2.</span></span>

<span data-ttu-id="76ca2-138">Alle Parameter der D3DXMatrixOrthoOffCenterLH-Funktion sind Abstände im Kamerabereich.</span><span class="sxs-lookup"><span data-stu-id="76ca2-138">All the parameters of the D3DXMatrixOrthoOffCenterLH function are distances in camera space.</span></span> <span data-ttu-id="76ca2-139">Die Parameter beschreiben die Dimensionen des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="76ca2-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="76ca2-140">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="76ca2-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="76ca2-141">Auf diese Weise kann die D3DXMatrixOrthoOffCenterLH-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76ca2-141">In this way, the D3DXMatrixOrthoOffCenterLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="76ca2-142">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="76ca2-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="76ca2-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76ca2-143">Requirements</span></span>



| <span data-ttu-id="76ca2-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76ca2-144">Requirement</span></span> | <span data-ttu-id="76ca2-145">Wert</span><span class="sxs-lookup"><span data-stu-id="76ca2-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76ca2-146">Header</span><span class="sxs-lookup"><span data-stu-id="76ca2-146">Header</span></span><br/>  | <dl> <span data-ttu-id="76ca2-147"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="76ca2-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="76ca2-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76ca2-148">Library</span></span><br/> | <dl> <span data-ttu-id="76ca2-149"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76ca2-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="76ca2-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76ca2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ca2-151">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="76ca2-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
