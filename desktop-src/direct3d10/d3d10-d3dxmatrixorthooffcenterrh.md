---
description: 'D3DXMatrixOrthoOffCenterRH-Funktion (D3DX10Math.h): Erstellt eine benutzerdefinierte, rechtshändige orthografische Projektionsmatrix.'
ms.assetid: 01d4d61e-de7b-4431-a168-68a50b1d6021
title: D3DXMatrixOrthoOffCenterRH-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 0b41038021cc34cb02961cb9894415995955404c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113078"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="bc7be-103">D3DXMatrixOrthoOffCenterRH-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="bc7be-103">D3DXMatrixOrthoOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="bc7be-104">Erstellt eine angepasste, rechtshändige orthografische Projektionsmatrix.</span><span class="sxs-lookup"><span data-stu-id="bc7be-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc7be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc7be-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="bc7be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc7be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc7be-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bc7be-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc7be-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc7be-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bc7be-109">Zeiger auf die resultierende [**D3DXMATRIX.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="bc7be-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc7be-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc7be-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc7be-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc7be-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc7be-112">Minimaler x-Wert des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="bc7be-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="bc7be-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc7be-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc7be-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc7be-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc7be-115">Maximaler x-Wert des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="bc7be-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="bc7be-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc7be-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc7be-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc7be-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc7be-118">Minimaler y-Wert des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="bc7be-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="bc7be-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc7be-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc7be-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc7be-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc7be-121">Maximaler y-Wert des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="bc7be-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="bc7be-122">*zn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bc7be-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc7be-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc7be-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc7be-124">Minimaler Z-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="bc7be-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="bc7be-125">*NSD* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bc7be-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc7be-126">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc7be-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc7be-127">Maximaler Z-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="bc7be-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc7be-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc7be-128">Return value</span></span>

<span data-ttu-id="bc7be-129">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc7be-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bc7be-130">Zeiger auf die resultierende [**D3DXMATRIX.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="bc7be-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bc7be-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc7be-131">Remarks</span></span>

<span data-ttu-id="bc7be-132">Die [**D3DXMatrixOrthoRH-Funktion**](d3d10-d3dxmatrixorthorh.md) ist ein Sonderfall der D3DXMatrixOrthoOffCenterRH-Funktion.</span><span class="sxs-lookup"><span data-stu-id="bc7be-132">The [**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) function is a special case of the D3DXMatrixOrthoOffCenterRH function.</span></span> <span data-ttu-id="bc7be-133">Verwenden Sie die folgenden Werte, um dieselbe Projektion mit D3DXMatrixOrthoOffCenterRH zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="bc7be-133">To create the same projection using D3DXMatrixOrthoOffCenterRH, use the following values:</span></span>

<span data-ttu-id="bc7be-134">l = -w/2,</span><span class="sxs-lookup"><span data-stu-id="bc7be-134">l = -w/2,</span></span>

<span data-ttu-id="bc7be-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="bc7be-135">r = w/2,</span></span>

<span data-ttu-id="bc7be-136">b = -h/2 und</span><span class="sxs-lookup"><span data-stu-id="bc7be-136">b = -h/2, and</span></span>

<span data-ttu-id="bc7be-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="bc7be-137">t = h/2.</span></span>

<span data-ttu-id="bc7be-138">Alle Parameter der D3DXMatrixOrthoOffCenterRH-Funktion sind Entfernungen im Kameraraum.</span><span class="sxs-lookup"><span data-stu-id="bc7be-138">All the parameters of the D3DXMatrixOrthoOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="bc7be-139">Die Parameter beschreiben die Dimensionen des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="bc7be-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="bc7be-140">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bc7be-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="bc7be-141">Auf diese Weise kann die D3DXMatrixOrthoOffCenterRH-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc7be-141">In this way, the D3DXMatrixOrthoOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="bc7be-142">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="bc7be-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="bc7be-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc7be-143">Requirements</span></span>



| <span data-ttu-id="bc7be-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc7be-144">Requirement</span></span> | <span data-ttu-id="bc7be-145">Wert</span><span class="sxs-lookup"><span data-stu-id="bc7be-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc7be-146">Header</span><span class="sxs-lookup"><span data-stu-id="bc7be-146">Header</span></span><br/>  | <dl> <span data-ttu-id="bc7be-147"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="bc7be-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bc7be-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bc7be-148">Library</span></span><br/> | <dl> <span data-ttu-id="bc7be-149"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc7be-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc7be-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bc7be-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc7be-151">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="bc7be-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
