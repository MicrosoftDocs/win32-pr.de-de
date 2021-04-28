---
description: 'D3DXMatrixOrthoRH-Funktion (D3dx9math.h): Erstellt eine rechtshändige orthografische Projektionsmatrix.'
ms.assetid: 6b9b50d5-0307-4fc7-a28d-8f42d2a21bf0
title: D3DXMatrixOrthoRH-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d34a8379851d80ae8734c7f32cc0dc5977af2088
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107438"
---
# <a name="d3dxmatrixorthorh-function-d3dx9mathh"></a><span data-ttu-id="a0ac0-103">D3DXMatrixOrthoRH-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="a0ac0-103">D3DXMatrixOrthoRH function (D3dx9math.h)</span></span>

<span data-ttu-id="a0ac0-104">Erstellt eine rechtshändige orthografische Projektionsmatrix.</span><span class="sxs-lookup"><span data-stu-id="a0ac0-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0ac0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0ac0-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="a0ac0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0ac0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0ac0-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a0ac0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ac0-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0ac0-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a0ac0-109">Zeiger auf die resultierende [**D3DXMATRIX.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="a0ac0-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0ac0-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0ac0-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ac0-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0ac0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0ac0-112">Breite des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="a0ac0-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="a0ac0-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0ac0-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ac0-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0ac0-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0ac0-115">Höhe des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="a0ac0-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="a0ac0-116">*zn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a0ac0-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ac0-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0ac0-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0ac0-118">Minimaler Z-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="a0ac0-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="a0ac0-119">*NSD* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a0ac0-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ac0-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0ac0-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0ac0-121">Maximaler Z-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="a0ac0-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0ac0-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0ac0-122">Return value</span></span>

<span data-ttu-id="a0ac0-123">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0ac0-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a0ac0-124">Zeiger auf die resultierende [**D3DXMATRIX.**](../direct3d10/d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="a0ac0-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0ac0-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0ac0-125">Remarks</span></span>

<span data-ttu-id="a0ac0-126">Alle Parameter der **D3DXMatrixOrthoRH-Funktion** sind Entfernungen im Kameraraum.</span><span class="sxs-lookup"><span data-stu-id="a0ac0-126">All the parameters of the **D3DXMatrixOrthoRH** function are distances in camera space.</span></span> <span data-ttu-id="a0ac0-127">Die Parameter beschreiben die Dimensionen des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="a0ac0-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="a0ac0-128">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a0ac0-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a0ac0-129">Auf diese Weise kann die **D3DXMatrixOrthoRH-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0ac0-129">In this way, the **D3DXMatrixOrthoRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a0ac0-130">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="a0ac0-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="a0ac0-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0ac0-131">Requirements</span></span>



| <span data-ttu-id="a0ac0-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0ac0-132">Requirement</span></span> | <span data-ttu-id="a0ac0-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ac0-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ac0-134">Header</span><span class="sxs-lookup"><span data-stu-id="a0ac0-134">Header</span></span><br/>  | <dl> <span data-ttu-id="a0ac0-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a0ac0-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a0ac0-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a0ac0-136">Library</span></span><br/> | <dl> <span data-ttu-id="a0ac0-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0ac0-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0ac0-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a0ac0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0ac0-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a0ac0-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a0ac0-140">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="a0ac0-140">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="a0ac0-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="a0ac0-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="a0ac0-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="a0ac0-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
