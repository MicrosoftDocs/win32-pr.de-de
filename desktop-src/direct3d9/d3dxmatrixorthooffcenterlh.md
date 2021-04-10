---
description: Erstellt eine angepasste, Links vergebene orthografische Projektions Matrix.
ms.assetid: e4f087e5-63d9-49ca-9d8e-3a25070e1a51
title: D3DXMatrixOrthoOffCenterLH-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e286197233b2abb2b19138b8fc9d154df355a6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961694"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="68106-103">D3DXMatrixOrthoOffCenterLH-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="68106-103">D3DXMatrixOrthoOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="68106-104">Erstellt eine angepasste, Links vergebene orthografische Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="68106-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="68106-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="68106-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="68106-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68106-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68106-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="68106-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="68106-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="68106-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="68106-109">Zeiger auf das resultierende [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="68106-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="68106-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68106-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68106-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68106-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68106-112">Minimaler x-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="68106-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="68106-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68106-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68106-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68106-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68106-115">Maximaler x-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="68106-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="68106-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68106-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68106-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68106-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68106-118">Minimaler y-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="68106-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="68106-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68106-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68106-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68106-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68106-121">Maximaler y-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="68106-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="68106-122">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68106-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68106-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68106-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68106-124">Der minimale z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="68106-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="68106-125">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68106-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68106-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68106-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68106-127">Maximaler z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="68106-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68106-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68106-128">Return value</span></span>

<span data-ttu-id="68106-129">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="68106-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="68106-130">Zeiger auf das resultierende [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="68106-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="68106-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68106-131">Remarks</span></span>

<span data-ttu-id="68106-132">Die [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) -Funktion ist ein Sonderfall der **D3DXMatrixOrthoOffCenterLH** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="68106-132">The [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) function is a special case of the **D3DXMatrixOrthoOffCenterLH** function.</span></span> <span data-ttu-id="68106-133">Wenn Sie dieselbe Projektion mithilfe von **D3DXMatrixOrthoOffCenterLH** erstellen möchten, verwenden Sie die folgenden Werte: l =-w/2, r = w/2, b =-h/2 und t = h/2.</span><span class="sxs-lookup"><span data-stu-id="68106-133">To create the same projection using **D3DXMatrixOrthoOffCenterLH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="68106-134">Alle Parameter der **D3DXMatrixOrthoOffCenterLH** -Funktion sind Abstände im Kamerabereich.</span><span class="sxs-lookup"><span data-stu-id="68106-134">All the parameters of the **D3DXMatrixOrthoOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="68106-135">Die Parameter beschreiben die Dimensionen des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="68106-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="68106-136">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="68106-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="68106-137">Auf diese Weise kann die **D3DXMatrixOrthoOffCenterLH** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68106-137">In this way, the **D3DXMatrixOrthoOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="68106-138">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="68106-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="68106-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68106-139">Requirements</span></span>



| <span data-ttu-id="68106-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68106-140">Requirement</span></span> | <span data-ttu-id="68106-141">Wert</span><span class="sxs-lookup"><span data-stu-id="68106-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68106-142">Header</span><span class="sxs-lookup"><span data-stu-id="68106-142">Header</span></span><br/>  | <dl> <span data-ttu-id="68106-143"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="68106-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="68106-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="68106-144">Library</span></span><br/> | <dl> <span data-ttu-id="68106-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68106-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68106-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68106-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68106-147">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="68106-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="68106-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="68106-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="68106-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="68106-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="68106-150">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="68106-150">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> </dl>

 

 
