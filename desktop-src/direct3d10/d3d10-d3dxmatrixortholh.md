---
description: Erstellt eine linke orthografische Projektions Matrix.
ms.assetid: 67bec4a3-2126-4f5a-9301-97faa6dc6e84
title: D3DXMatrixOrthoLH-Funktion (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0b49e6008b52f7060075688730c72f5f5d3f725a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219663"
---
# <a name="d3dxmatrixortholh-function-d3dx10mathh"></a><span data-ttu-id="1cccd-103">D3DXMatrixOrthoLH-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1cccd-103">D3DXMatrixOrthoLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="1cccd-104">Erstellt eine linke orthografische Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="1cccd-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cccd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cccd-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="1cccd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cccd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cccd-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1cccd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cccd-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1cccd-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1cccd-109">Zeiger auf das resultierende [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="1cccd-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cccd-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cccd-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cccd-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cccd-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cccd-112">Breite des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="1cccd-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="1cccd-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cccd-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cccd-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cccd-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cccd-115">Höhe des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="1cccd-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="1cccd-116">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cccd-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cccd-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cccd-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cccd-118">Der minimale z-Wert des Ansichts Volumes, das als z-near bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1cccd-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="1cccd-119">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cccd-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cccd-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cccd-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cccd-121">Maximaler z-Wert des Ansichts Volumes, das als "z-weit" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1cccd-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cccd-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1cccd-122">Return value</span></span>

<span data-ttu-id="1cccd-123">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1cccd-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1cccd-124">Zeiger auf das resultierende [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="1cccd-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1cccd-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cccd-125">Remarks</span></span>

<span data-ttu-id="1cccd-126">Alle Parameter der D3DXMatrixOrthoLH-Funktion sind Abstände im Kamerabereich.</span><span class="sxs-lookup"><span data-stu-id="1cccd-126">All the parameters of the D3DXMatrixOrthoLH function are distances in camera space.</span></span> <span data-ttu-id="1cccd-127">Die Parameter beschreiben die Dimensionen des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="1cccd-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="1cccd-128">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1cccd-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1cccd-129">Auf diese Weise kann die D3DXMatrixOrthoLH-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1cccd-129">In this way, the D3DXMatrixOrthoLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1cccd-130">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="1cccd-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="1cccd-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1cccd-131">Requirements</span></span>



| <span data-ttu-id="1cccd-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1cccd-132">Requirement</span></span> | <span data-ttu-id="1cccd-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1cccd-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cccd-134">Header</span><span class="sxs-lookup"><span data-stu-id="1cccd-134">Header</span></span><br/>  | <dl> <span data-ttu-id="1cccd-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cccd-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1cccd-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1cccd-136">Library</span></span><br/> | <dl> <span data-ttu-id="1cccd-137"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cccd-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1cccd-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cccd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cccd-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1cccd-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
