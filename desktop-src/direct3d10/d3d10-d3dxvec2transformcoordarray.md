---
description: 'D3DXVec2TransformCoordArray-Funktion (D3DX10Math.h): Transformiert ein Array (x, y, 0, 1) durch eine bestimmte Matrix und probiert das Ergebnis zurück in w = 1.'
ms.assetid: dba68678-2ab4-4f64-9975-5e9f2a20f66a
title: D3DXVec2TransformCoordArray-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoordArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f36b5fb5a5263f83c42ac66cc5f606fa1c4b75ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108328"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="2ada5-103">D3DXVec2TransformCoordArray-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="2ada5-103">D3DXVec2TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="2ada5-104">Transformiert ein Array (x, y, 0, 1) durch eine bestimmte Matrix und probiert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="2ada5-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ada5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ada5-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoordArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="2ada5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ada5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ada5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2ada5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ada5-108">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ada5-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="2ada5-109">Zeiger auf den [**D3DXVECTOR2,**](d3d10-d3dxvector2.md) der das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="2ada5-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2ada5-110">*OutStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ada5-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ada5-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ada5-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ada5-112">Stride zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="2ada5-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="2ada5-113">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ada5-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ada5-114">Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ada5-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="2ada5-115">Zeiger auf das D3DXVECTOR2-Quellarray.</span><span class="sxs-lookup"><span data-stu-id="2ada5-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="2ada5-116">*VStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ada5-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ada5-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ada5-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ada5-118">Stride zwischen Vektoren im Eingabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="2ada5-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="2ada5-119">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2ada5-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ada5-120">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ada5-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ada5-121">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="2ada5-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2ada5-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ada5-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ada5-123">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ada5-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ada5-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="2ada5-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ada5-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ada5-125">Return value</span></span>

<span data-ttu-id="2ada5-126">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ada5-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="2ada5-127">Zeiger auf ein transformiertes [**D3DXVECTOR4-Array.**](d3d10-d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="2ada5-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ada5-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ada5-128">Remarks</span></span>

<span data-ttu-id="2ada5-129">Diese Funktion transformiert das Array pV (x, y, 0, 1) durch die Matrix-pM und projiziert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="2ada5-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="2ada5-130">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ada5-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2ada5-131">Auf diese Weise kann die D3DXVec2TransformCoordArray-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ada5-131">In this way, the D3DXVec2TransformCoordArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ada5-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ada5-132">Requirements</span></span>



| <span data-ttu-id="2ada5-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ada5-133">Requirement</span></span> | <span data-ttu-id="2ada5-134">Wert</span><span class="sxs-lookup"><span data-stu-id="2ada5-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ada5-135">Header</span><span class="sxs-lookup"><span data-stu-id="2ada5-135">Header</span></span><br/>  | <dl> <span data-ttu-id="2ada5-136"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2ada5-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2ada5-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ada5-137">Library</span></span><br/> | <dl> <span data-ttu-id="2ada5-138"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ada5-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2ada5-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2ada5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ada5-140">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2ada5-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
