---
description: 'D3DXMatrixOrthoOffCenterRH-Funktion (D3dx9math.h): Erstellt eine benutzerdefinierte, rechtshändige orthografische Projektionsmatrix.'
ms.assetid: d6171e28-b138-4ccf-9f12-fb977a30aca1
title: D3DXMatrixOrthoOffCenterRH-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 8519dca07a4475ff043491802ae173ecc61c0bd3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107458"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="2ffcf-103">D3DXMatrixOrthoOffCenterRH-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="2ffcf-103">D3DXMatrixOrthoOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="2ffcf-104">Erstellt eine angepasste, rechtshändige orthografische Projektionsmatrix.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ffcf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ffcf-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2ffcf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ffcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ffcf-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2ffcf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffcf-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ffcf-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ffcf-109">Zeiger auf die resultierende [**D3DXMATRIX.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="2ffcf-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ffcf-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ffcf-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffcf-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ffcf-112">Minimaler x-Wert des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="2ffcf-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ffcf-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffcf-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ffcf-115">Maximaler x-Wert des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="2ffcf-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ffcf-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffcf-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ffcf-118">Minimaler y-Wert des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="2ffcf-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ffcf-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffcf-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ffcf-121">Maximaler y-Wert des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="2ffcf-122">*zn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ffcf-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffcf-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ffcf-124">Minimaler Z-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="2ffcf-125">*NSD* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ffcf-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffcf-126">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ffcf-127">Maximaler Z-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ffcf-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ffcf-128">Return value</span></span>

<span data-ttu-id="2ffcf-129">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ffcf-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ffcf-130">Zeiger auf die resultierende [**D3DXMATRIX.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="2ffcf-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2ffcf-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ffcf-131">Remarks</span></span>

<span data-ttu-id="2ffcf-132">Die [**D3DXMatrixOrthoRH-Funktion**](d3dxmatrixorthorh.md) ist ein Sonderfall der **D3DXMatrixOrthoOffCenterRH-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-132">The [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) function is a special case of the **D3DXMatrixOrthoOffCenterRH** function.</span></span> <span data-ttu-id="2ffcf-133">Um dieselbe Projektion mit **D3DXMatrixOrthoOffCenterRH** zu erstellen, verwenden Sie die folgenden Werte: l = -w/2, r = w/2, b = -h/2 und t = h/2.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-133">To create the same projection using **D3DXMatrixOrthoOffCenterRH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="2ffcf-134">Alle Parameter der **D3DXMatrixOrthoOffCenterRH-Funktion** sind Entfernungen im Kameraraum.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-134">All the parameters of the **D3DXMatrixOrthoOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="2ffcf-135">Die Parameter beschreiben die Dimensionen des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="2ffcf-136">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2ffcf-137">Auf diese Weise kann die **D3DXMatrixOrthoOffCenterRH-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-137">In this way, the **D3DXMatrixOrthoOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2ffcf-138">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="2ffcf-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="2ffcf-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ffcf-139">Requirements</span></span>



| <span data-ttu-id="2ffcf-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ffcf-140">Requirement</span></span> | <span data-ttu-id="2ffcf-141">Wert</span><span class="sxs-lookup"><span data-stu-id="2ffcf-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ffcf-142">Header</span><span class="sxs-lookup"><span data-stu-id="2ffcf-142">Header</span></span><br/>  | <dl> <span data-ttu-id="2ffcf-143"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2ffcf-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2ffcf-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ffcf-144">Library</span></span><br/> | <dl> <span data-ttu-id="2ffcf-145"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ffcf-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2ffcf-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2ffcf-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ffcf-147">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2ffcf-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2ffcf-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="2ffcf-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="2ffcf-150">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="2ffcf-150">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
