---
description: Transformiert ein Array (x, y, 0, 1) durch eine angegebene Matrix und projiziert das Ergebnis zurück in w = 1.
ms.assetid: dba68678-2ab4-4f64-9975-5e9f2a20f66a
title: D3DXVec2TransformCoordArray-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: aa57d96b0497fea572e580cfe6d1af2a0184f09d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355040"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="b75b6-103">D3DXVec2TransformCoordArray-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b75b6-103">D3DXVec2TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="b75b6-104">Transformiert ein Array (x, y, 0, 1) durch eine angegebene Matrix und projiziert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="b75b6-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="b75b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b75b6-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b75b6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b75b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b75b6-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b75b6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b75b6-108">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="b75b6-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="b75b6-109">Zeiger auf das [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="b75b6-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b75b6-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b75b6-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b75b6-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b75b6-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b75b6-112">Schritt zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="b75b6-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="b75b6-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b75b6-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b75b6-114">Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="b75b6-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="b75b6-115">Zeiger auf das Quell-D3DXVECTOR2 Array.</span><span class="sxs-lookup"><span data-stu-id="b75b6-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="b75b6-116">*Vstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b75b6-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b75b6-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b75b6-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b75b6-118">Schritt zwischen Vektoren im Eingabedaten Strom.</span><span class="sxs-lookup"><span data-stu-id="b75b6-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="b75b6-119">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b75b6-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b75b6-120">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b75b6-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b75b6-121">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b75b6-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b75b6-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b75b6-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b75b6-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b75b6-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b75b6-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="b75b6-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b75b6-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b75b6-125">Return value</span></span>

<span data-ttu-id="b75b6-126">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="b75b6-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="b75b6-127">Zeiger auf ein [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformiertes Array.</span><span class="sxs-lookup"><span data-stu-id="b75b6-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="b75b6-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b75b6-128">Remarks</span></span>

<span data-ttu-id="b75b6-129">Diese Funktion wandelt das Array PV (x, y, 0, 1) durch die Matrix pm um und projiziert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="b75b6-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="b75b6-130">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b75b6-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b75b6-131">Auf diese Weise kann die D3DXVec2TransformCoordArray-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b75b6-131">In this way, the D3DXVec2TransformCoordArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b75b6-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b75b6-132">Requirements</span></span>



| <span data-ttu-id="b75b6-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b75b6-133">Requirement</span></span> | <span data-ttu-id="b75b6-134">Wert</span><span class="sxs-lookup"><span data-stu-id="b75b6-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b75b6-135">Header</span><span class="sxs-lookup"><span data-stu-id="b75b6-135">Header</span></span><br/>  | <dl> <span data-ttu-id="b75b6-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b75b6-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b75b6-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b75b6-137">Library</span></span><br/> | <dl> <span data-ttu-id="b75b6-138"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b75b6-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b75b6-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b75b6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b75b6-140">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="b75b6-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
