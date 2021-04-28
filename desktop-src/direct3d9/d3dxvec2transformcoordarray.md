---
description: 'D3DXVec2TransformCoordArray-Funktion (D3dx9math.h): Transformiert ein Array (x, y, 0, 1) durch eine bestimmte Matrix und probiert das Ergebnis zurück in w = 1.'
ms.assetid: 23c88bed-344b-4b3a-bb92-e50cbe96daf9
title: D3DXVec2TransformCoordArray-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 257cb77ba97396170f221cff1c512a73eb84179c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097938"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx9mathh"></a><span data-ttu-id="6bb2f-103">D3DXVec2TransformCoordArray-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="6bb2f-103">D3DXVec2TransformCoordArray function (D3dx9math.h)</span></span>

<span data-ttu-id="6bb2f-104">Transformiert ein Array (x, y, 0, 1) durch eine bestimmte Matrix und probiert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="6bb2f-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb2f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bb2f-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="6bb2f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bb2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bb2f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6bb2f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bb2f-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="6bb2f-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6bb2f-109">Zeiger auf die [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="6bb2f-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6bb2f-110">*OutStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6bb2f-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bb2f-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6bb2f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6bb2f-112">Stride zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="6bb2f-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="6bb2f-113">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6bb2f-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bb2f-114">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="6bb2f-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6bb2f-115">Zeiger auf das [**D3DXVECTOR2-Quellarray.**](d3dxvector2.md)</span><span class="sxs-lookup"><span data-stu-id="6bb2f-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="6bb2f-116">*VStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6bb2f-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bb2f-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6bb2f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6bb2f-118">Stride zwischen Vektoren im Eingabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="6bb2f-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="6bb2f-119">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6bb2f-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bb2f-120">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6bb2f-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6bb2f-121">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="6bb2f-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6bb2f-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6bb2f-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bb2f-123">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6bb2f-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6bb2f-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="6bb2f-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bb2f-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6bb2f-125">Return value</span></span>

<span data-ttu-id="6bb2f-126">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="6bb2f-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6bb2f-127">Zeiger auf ein transformiertes [**D3DXVECTOR4-Array.**](d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="6bb2f-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bb2f-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bb2f-128">Remarks</span></span>

<span data-ttu-id="6bb2f-129">Diese Funktion transformiert das Array *pV* (x, y, 0, 1) durch die Matrix *pM* und projiziert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="6bb2f-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*, projecting the result back into w = 1.</span></span>

<span data-ttu-id="6bb2f-130">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6bb2f-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6bb2f-131">Auf diese Weise kann die **D3DXVec2TransformCoordArray-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6bb2f-131">In this way, the **D3DXVec2TransformCoordArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb2f-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bb2f-132">Requirements</span></span>



| <span data-ttu-id="6bb2f-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bb2f-133">Requirement</span></span> | <span data-ttu-id="6bb2f-134">Wert</span><span class="sxs-lookup"><span data-stu-id="6bb2f-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb2f-135">Header</span><span class="sxs-lookup"><span data-stu-id="6bb2f-135">Header</span></span><br/>  | <dl> <span data-ttu-id="6bb2f-136"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6bb2f-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6bb2f-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6bb2f-137">Library</span></span><br/> | <dl> <span data-ttu-id="6bb2f-138"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bb2f-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6bb2f-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6bb2f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb2f-140">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="6bb2f-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
