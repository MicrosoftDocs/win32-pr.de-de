---
description: 'D3DXMatrixOrthoRH-Funktion (D3DX10Math.h): Erstellt eine rechtshändige orthografische Projektionsmatrix.'
ms.assetid: e6673ff4-06a2-4a16-b72e-5ca69ddf2438
title: D3DXMatrixOrthoRH-Funktion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f1ab6069890bdffdedbd3e36caed1a93984fc2c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109148"
---
# <a name="d3dxmatrixorthorh-function-d3dx10mathh"></a><span data-ttu-id="9b932-103">D3DXMatrixOrthoRH-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="9b932-103">D3DXMatrixOrthoRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="9b932-104">Erstellt eine rechtshändige orthografische Projektionsmatrix.</span><span class="sxs-lookup"><span data-stu-id="9b932-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b932-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b932-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="9b932-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b932-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b932-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9b932-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b932-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b932-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9b932-109">Zeiger auf die resultierende [**D3DXMATRIX.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="9b932-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b932-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b932-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b932-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b932-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b932-112">Breite des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="9b932-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="9b932-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b932-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b932-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b932-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b932-115">Höhe des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="9b932-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="9b932-116">*zn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9b932-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b932-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b932-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b932-118">Minimaler Z-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="9b932-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="9b932-119">*NSD* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9b932-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b932-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b932-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b932-121">Maximaler Z-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="9b932-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b932-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b932-122">Return value</span></span>

<span data-ttu-id="9b932-123">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b932-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9b932-124">Zeiger auf die resultierende [**D3DXMATRIX.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="9b932-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b932-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b932-125">Remarks</span></span>

<span data-ttu-id="9b932-126">Alle Parameter der D3DXMatrixOrthoRH-Funktion sind Abstände im Kameraraum.</span><span class="sxs-lookup"><span data-stu-id="9b932-126">All the parameters of the D3DXMatrixOrthoRH function are distances in camera space.</span></span> <span data-ttu-id="9b932-127">Die Parameter beschreiben die Dimensionen des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="9b932-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="9b932-128">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b932-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9b932-129">Auf diese Weise kann die D3DXMatrixOrthoRH-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b932-129">In this way, the D3DXMatrixOrthoRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9b932-130">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="9b932-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="9b932-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b932-131">Requirements</span></span>



| <span data-ttu-id="9b932-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b932-132">Requirement</span></span> | <span data-ttu-id="9b932-133">Wert</span><span class="sxs-lookup"><span data-stu-id="9b932-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b932-134">Header</span><span class="sxs-lookup"><span data-stu-id="9b932-134">Header</span></span><br/>  | <dl> <span data-ttu-id="9b932-135"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="9b932-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9b932-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9b932-136">Library</span></span><br/> | <dl> <span data-ttu-id="9b932-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b932-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9b932-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9b932-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b932-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="9b932-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
