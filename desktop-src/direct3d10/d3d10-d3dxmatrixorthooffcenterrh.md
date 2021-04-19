---
description: Erstellt eine angepasste, rechts vergebene orthografische Projektions Matrix.
ms.assetid: 01d4d61e-de7b-4431-a168-68a50b1d6021
title: D3DXMatrixOrthoOffCenterRH-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3b5b544a4144ebc283686385638435ec42b4d801
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367387"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="629eb-103">D3DXMatrixOrthoOffCenterRH-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="629eb-103">D3DXMatrixOrthoOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="629eb-104">Erstellt eine angepasste, rechts vergebene orthografische Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="629eb-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="629eb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="629eb-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="629eb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="629eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="629eb-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="629eb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="629eb-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="629eb-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="629eb-109">Zeiger auf das resultierende [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="629eb-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="629eb-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="629eb-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="629eb-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="629eb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="629eb-112">Minimaler x-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="629eb-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="629eb-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="629eb-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="629eb-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="629eb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="629eb-115">Maximaler x-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="629eb-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="629eb-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="629eb-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="629eb-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="629eb-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="629eb-118">Minimaler y-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="629eb-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="629eb-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="629eb-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="629eb-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="629eb-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="629eb-121">Maximaler y-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="629eb-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="629eb-122">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="629eb-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="629eb-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="629eb-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="629eb-124">Der minimale z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="629eb-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="629eb-125">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="629eb-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="629eb-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="629eb-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="629eb-127">Maximaler z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="629eb-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="629eb-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="629eb-128">Return value</span></span>

<span data-ttu-id="629eb-129">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="629eb-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="629eb-130">Zeiger auf das resultierende [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="629eb-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="629eb-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="629eb-131">Remarks</span></span>

<span data-ttu-id="629eb-132">Die [**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) -Funktion ist ein Sonderfall der D3DXMatrixOrthoOffCenterRH-Funktion.</span><span class="sxs-lookup"><span data-stu-id="629eb-132">The [**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) function is a special case of the D3DXMatrixOrthoOffCenterRH function.</span></span> <span data-ttu-id="629eb-133">Verwenden Sie die folgenden Werte, um dieselbe Projektion mithilfe von D3DXMatrixOrthoOffCenterRH zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="629eb-133">To create the same projection using D3DXMatrixOrthoOffCenterRH, use the following values:</span></span>

<span data-ttu-id="629eb-134">l =-w/2,</span><span class="sxs-lookup"><span data-stu-id="629eb-134">l = -w/2,</span></span>

<span data-ttu-id="629eb-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="629eb-135">r = w/2,</span></span>

<span data-ttu-id="629eb-136">b =-h/2, und</span><span class="sxs-lookup"><span data-stu-id="629eb-136">b = -h/2, and</span></span>

<span data-ttu-id="629eb-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="629eb-137">t = h/2.</span></span>

<span data-ttu-id="629eb-138">Alle Parameter der D3DXMatrixOrthoOffCenterRH-Funktion sind Abstände im Kamerabereich.</span><span class="sxs-lookup"><span data-stu-id="629eb-138">All the parameters of the D3DXMatrixOrthoOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="629eb-139">Die Parameter beschreiben die Dimensionen des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="629eb-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="629eb-140">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="629eb-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="629eb-141">Auf diese Weise kann die D3DXMatrixOrthoOffCenterRH-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="629eb-141">In this way, the D3DXMatrixOrthoOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="629eb-142">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="629eb-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="629eb-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="629eb-143">Requirements</span></span>



| <span data-ttu-id="629eb-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="629eb-144">Requirement</span></span> | <span data-ttu-id="629eb-145">Wert</span><span class="sxs-lookup"><span data-stu-id="629eb-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="629eb-146">Header</span><span class="sxs-lookup"><span data-stu-id="629eb-146">Header</span></span><br/>  | <dl> <span data-ttu-id="629eb-147"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="629eb-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="629eb-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="629eb-148">Library</span></span><br/> | <dl> <span data-ttu-id="629eb-149"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="629eb-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="629eb-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="629eb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="629eb-151">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="629eb-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
