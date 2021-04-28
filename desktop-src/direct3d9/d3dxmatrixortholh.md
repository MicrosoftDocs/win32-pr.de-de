---
description: 'D3DXMatrixOrthoLH-Funktion (D3dx9math.h): Erstellt eine linkshändige orthografische Projektionsmatrix.'
ms.assetid: e42151bd-2302-491b-a211-7d5a4b8e437f
title: D3DXMatrixOrthoLH-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5492a6caba87025d83562c0327ac0e1f5a76f269
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107498"
---
# <a name="d3dxmatrixortholh-function-d3dx9mathh"></a><span data-ttu-id="03ca5-103">D3DXMatrixOrthoLH-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="03ca5-103">D3DXMatrixOrthoLH function (D3dx9math.h)</span></span>

<span data-ttu-id="03ca5-104">Erstellt eine linkshändige orthografische Projektionsmatrix.</span><span class="sxs-lookup"><span data-stu-id="03ca5-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ca5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03ca5-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="03ca5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03ca5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03ca5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="03ca5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="03ca5-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="03ca5-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="03ca5-109">Zeiger auf die resultierende [**D3DXMATRIX.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="03ca5-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="03ca5-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03ca5-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ca5-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03ca5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="03ca5-112">Breite des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="03ca5-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="03ca5-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03ca5-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ca5-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03ca5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="03ca5-115">Höhe des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="03ca5-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="03ca5-116">*zn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="03ca5-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ca5-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03ca5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="03ca5-118">Der minimale Z-Wert des Ansichtsvolumes, der als z-near bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="03ca5-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="03ca5-119">*NSD* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="03ca5-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ca5-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03ca5-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="03ca5-121">Maximaler Z-Wert des Ansichtsvolumes, der als z-far bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="03ca5-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03ca5-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03ca5-122">Return value</span></span>

<span data-ttu-id="03ca5-123">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="03ca5-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="03ca5-124">Zeiger auf die resultierende [**D3DXMATRIX.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="03ca5-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="03ca5-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03ca5-125">Remarks</span></span>

<span data-ttu-id="03ca5-126">Alle Parameter der **D3DXMatrixOrthoLH-Funktion** sind Abstände im Kameraraum.</span><span class="sxs-lookup"><span data-stu-id="03ca5-126">All the parameters of the **D3DXMatrixOrthoLH** function are distances in camera space.</span></span> <span data-ttu-id="03ca5-127">Die Parameter beschreiben die Dimensionen des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="03ca5-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="03ca5-128">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="03ca5-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="03ca5-129">Auf diese Weise kann die **D3DXMatrixOrthoLH-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03ca5-129">In this way, the **D3DXMatrixOrthoLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="03ca5-130">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="03ca5-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0   -zn/(zf-zn)  1
```



## <a name="requirements"></a><span data-ttu-id="03ca5-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03ca5-131">Requirements</span></span>



| <span data-ttu-id="03ca5-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03ca5-132">Requirement</span></span> | <span data-ttu-id="03ca5-133">Wert</span><span class="sxs-lookup"><span data-stu-id="03ca5-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03ca5-134">Header</span><span class="sxs-lookup"><span data-stu-id="03ca5-134">Header</span></span><br/>  | <dl> <span data-ttu-id="03ca5-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="03ca5-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="03ca5-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="03ca5-136">Library</span></span><br/> | <dl> <span data-ttu-id="03ca5-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="03ca5-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="03ca5-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="03ca5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ca5-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="03ca5-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="03ca5-140">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="03ca5-140">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="03ca5-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="03ca5-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="03ca5-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="03ca5-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
