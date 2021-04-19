---
description: Erstellt eine angepasste, rechts vergebene orthografische Projektions Matrix.
ms.assetid: d6171e28-b138-4ccf-9f12-fb977a30aca1
title: D3DXMatrixOrthoOffCenterRH-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7de5e4b3a872ea7466840e511fc0a57448861b55
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365331"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="a3332-103">D3DXMatrixOrthoOffCenterRH-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a3332-103">D3DXMatrixOrthoOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="a3332-104">Erstellt eine angepasste, rechts vergebene orthografische Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="a3332-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3332-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3332-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a3332-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3332-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3332-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a3332-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3332-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3332-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a3332-109">Zeiger auf das resultierende [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="a3332-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3332-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3332-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3332-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3332-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3332-112">Minimaler x-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="a3332-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="a3332-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3332-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3332-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3332-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3332-115">Maximaler x-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="a3332-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="a3332-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3332-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3332-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3332-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3332-118">Minimaler y-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="a3332-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="a3332-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3332-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3332-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3332-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3332-121">Maximaler y-Wert des Ansichts Volumens.</span><span class="sxs-lookup"><span data-stu-id="a3332-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="a3332-122">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3332-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3332-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3332-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3332-124">Der minimale z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="a3332-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="a3332-125">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3332-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3332-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3332-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3332-127">Maximaler z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="a3332-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3332-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3332-128">Return value</span></span>

<span data-ttu-id="a3332-129">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3332-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a3332-130">Zeiger auf das resultierende [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="a3332-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a3332-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3332-131">Remarks</span></span>

<span data-ttu-id="a3332-132">Die [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) -Funktion ist ein Sonderfall der **D3DXMatrixOrthoOffCenterRH** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="a3332-132">The [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) function is a special case of the **D3DXMatrixOrthoOffCenterRH** function.</span></span> <span data-ttu-id="a3332-133">Wenn Sie dieselbe Projektion mithilfe von **D3DXMatrixOrthoOffCenterRH** erstellen möchten, verwenden Sie die folgenden Werte: l =-w/2, r = w/2, b =-h/2 und t = h/2.</span><span class="sxs-lookup"><span data-stu-id="a3332-133">To create the same projection using **D3DXMatrixOrthoOffCenterRH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="a3332-134">Alle Parameter der **D3DXMatrixOrthoOffCenterRH** -Funktion sind Abstände im Kamerabereich.</span><span class="sxs-lookup"><span data-stu-id="a3332-134">All the parameters of the **D3DXMatrixOrthoOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="a3332-135">Die Parameter beschreiben die Dimensionen des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="a3332-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="a3332-136">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a3332-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a3332-137">Auf diese Weise kann die **D3DXMatrixOrthoOffCenterRH** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3332-137">In this way, the **D3DXMatrixOrthoOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a3332-138">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="a3332-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="a3332-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3332-139">Requirements</span></span>



| <span data-ttu-id="a3332-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3332-140">Requirement</span></span> | <span data-ttu-id="a3332-141">Wert</span><span class="sxs-lookup"><span data-stu-id="a3332-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3332-142">Header</span><span class="sxs-lookup"><span data-stu-id="a3332-142">Header</span></span><br/>  | <dl> <span data-ttu-id="a3332-143"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3332-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a3332-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3332-144">Library</span></span><br/> | <dl> <span data-ttu-id="a3332-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3332-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a3332-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3332-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3332-147">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a3332-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a3332-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="a3332-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="a3332-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="a3332-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="a3332-150">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="a3332-150">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
