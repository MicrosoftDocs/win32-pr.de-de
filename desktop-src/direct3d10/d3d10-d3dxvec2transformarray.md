---
description: 'D3DXVec2TransformArray-Funktion (D3DX10Math.h): Transformiert ein Array (x, y, 0, 1) durch eine angegebene Matrix.'
ms.assetid: 66c8909c-6c20-4b32-9546-fcf2d0e824fa
title: D3DXVec2TransformArray-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cec42fcbe53d3a8aa160f6864af70cbf441a19ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108368"
---
# <a name="d3dxvec2transformarray-function-d3dx10mathh"></a><span data-ttu-id="c4ed2-103">D3DXVec2TransformArray-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="c4ed2-103">D3DXVec2TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="c4ed2-104">Transformiert ein Array (x, y, 0, 1) durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="c4ed2-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4ed2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4ed2-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="c4ed2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4ed2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4ed2-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c4ed2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ed2-108">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4ed2-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="c4ed2-109">Zeiger auf die [**D3DXVECTOR4-Struktur,**](d3d10-d3dxvector4.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="c4ed2-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c4ed2-110">*OutStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c4ed2-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ed2-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4ed2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4ed2-112">Schreitet zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="c4ed2-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="c4ed2-113">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c4ed2-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ed2-114">Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="c4ed2-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="c4ed2-115">Zeiger auf die [**D3DXVECTOR2-Quelle.**](d3d10-d3dxvector2.md)</span><span class="sxs-lookup"><span data-stu-id="c4ed2-115">Pointer to the source [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4ed2-116">*VStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c4ed2-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ed2-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4ed2-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4ed2-118">Schreitet zwischen Vektoren im Eingabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="c4ed2-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="c4ed2-119">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c4ed2-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ed2-120">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c4ed2-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c4ed2-121">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="c4ed2-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c4ed2-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4ed2-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ed2-123">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4ed2-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4ed2-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="c4ed2-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4ed2-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4ed2-125">Return value</span></span>

<span data-ttu-id="c4ed2-126">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4ed2-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="c4ed2-127">Zeiger auf eine D3DXVECTOR4-Struktur, die das transformierte Array ist.</span><span class="sxs-lookup"><span data-stu-id="c4ed2-127">Pointer to a D3DXVECTOR4 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4ed2-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4ed2-128">Remarks</span></span>

<span data-ttu-id="c4ed2-129">Diese Funktion transformiert den Array-pV (x, y, 0, 1) durch die Matrix pM.</span><span class="sxs-lookup"><span data-stu-id="c4ed2-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM.</span></span>

<span data-ttu-id="c4ed2-130">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4ed2-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c4ed2-131">Auf diese Weise kann die [**D3DXVec2Transform-Funktion**](d3d10-d3dxvec2transform.md) als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4ed2-131">In this way, the [**D3DXVec2Transform**](d3d10-d3dxvec2transform.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ed2-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4ed2-132">Requirements</span></span>



| <span data-ttu-id="c4ed2-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4ed2-133">Requirement</span></span> | <span data-ttu-id="c4ed2-134">Wert</span><span class="sxs-lookup"><span data-stu-id="c4ed2-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ed2-135">Header</span><span class="sxs-lookup"><span data-stu-id="c4ed2-135">Header</span></span><br/>  | <dl> <span data-ttu-id="c4ed2-136"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c4ed2-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c4ed2-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c4ed2-137">Library</span></span><br/> | <dl> <span data-ttu-id="c4ed2-138"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4ed2-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4ed2-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c4ed2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ed2-140">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c4ed2-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
