---
description: 'D3DXMatrixOrthoOffCenterLH-Funktion (D3DX10Math.h): Erstellt eine angepasste, linkshändige orthografische Projektionsmatrix.'
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: D3DXMatrixOrthoOffCenterLH-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 2eb10963372519827eb544371ebb0df04df2e178
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109138"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a><span data-ttu-id="6a2e5-103">D3DXMatrixOrthoOffCenterLH-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="6a2e5-103">D3DXMatrixOrthoOffCenterLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="6a2e5-104">Erstellt eine angepasste, linkshändige orthografische Projektionsmatrix.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a2e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a2e5-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="6a2e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a2e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a2e5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6a2e5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2e5-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a2e5-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6a2e5-109">Zeiger auf die resultierende [**D3DXMATRIX.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="6a2e5-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a2e5-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a2e5-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2e5-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a2e5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a2e5-112">Minimaler x-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6a2e5-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a2e5-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2e5-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a2e5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a2e5-115">Maximaler x-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6a2e5-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a2e5-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2e5-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a2e5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a2e5-118">Minimaler y-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6a2e5-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a2e5-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2e5-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a2e5-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a2e5-121">Maximaler y-Wert des Anzeigevolumes.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6a2e5-122">*zn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6a2e5-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2e5-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a2e5-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a2e5-124">Minimaler Z-Wert des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="6a2e5-125">*( )* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6a2e5-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2e5-126">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a2e5-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a2e5-127">Maximaler Z-Wert des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a2e5-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a2e5-128">Return value</span></span>

<span data-ttu-id="6a2e5-129">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a2e5-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6a2e5-130">Zeiger auf die resultierende [**D3DXMATRIX.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="6a2e5-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6a2e5-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a2e5-131">Remarks</span></span>

<span data-ttu-id="6a2e5-132">[**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) ist ein Sonderfall der D3DXMatrixOrthoOffCenterLH-Funktion.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-132">The [**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) is a special case of the D3DXMatrixOrthoOffCenterLH function.</span></span> <span data-ttu-id="6a2e5-133">Verwenden Sie die folgenden Werte, um dieselbe Projektion mit D3DXMatrixOrthoOffCenterLH zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="6a2e5-133">To create the same projection using D3DXMatrixOrthoOffCenterLH, use the following values:</span></span>

<span data-ttu-id="6a2e5-134">l = -w/2,</span><span class="sxs-lookup"><span data-stu-id="6a2e5-134">l = -w/2,</span></span>

<span data-ttu-id="6a2e5-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="6a2e5-135">r = w/2,</span></span>

<span data-ttu-id="6a2e5-136">b = -h/2 und</span><span class="sxs-lookup"><span data-stu-id="6a2e5-136">b = -h/2, and</span></span>

<span data-ttu-id="6a2e5-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-137">t = h/2.</span></span>

<span data-ttu-id="6a2e5-138">Alle Parameter der D3DXMatrixOrthoOffCenterLH-Funktion sind Abstände im Kameraraum.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-138">All the parameters of the D3DXMatrixOrthoOffCenterLH function are distances in camera space.</span></span> <span data-ttu-id="6a2e5-139">Die Parameter beschreiben die Dimensionen des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="6a2e5-140">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6a2e5-141">Auf diese Weise kann die D3DXMatrixOrthoOffCenterLH-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-141">In this way, the D3DXMatrixOrthoOffCenterLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="6a2e5-142">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="6a2e5-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="6a2e5-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a2e5-143">Requirements</span></span>



| <span data-ttu-id="6a2e5-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a2e5-144">Requirement</span></span> | <span data-ttu-id="6a2e5-145">Wert</span><span class="sxs-lookup"><span data-stu-id="6a2e5-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a2e5-146">Header</span><span class="sxs-lookup"><span data-stu-id="6a2e5-146">Header</span></span><br/>  | <dl> <span data-ttu-id="6a2e5-147"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6a2e5-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6a2e5-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6a2e5-148">Library</span></span><br/> | <dl> <span data-ttu-id="6a2e5-149"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a2e5-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a2e5-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6a2e5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a2e5-151">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="6a2e5-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
