---
description: 'D3DXVec3TransformArray-Funktion (D3dx9math.h): Transformiert ein Array (x, y, z, 1) durch eine bestimmte Matrix.'
ms.assetid: fd7ab674-5e42-4265-afad-ae5a00dabcdb
title: D3DXVec3TransformArray-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 440869f42769d5c20e26083acf3fad1203e20a22
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097768"
---
# <a name="d3dxvec3transformarray-function-d3dx9mathh"></a><span data-ttu-id="fd8ed-103">D3DXVec3TransformArray-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="fd8ed-103">D3DXVec3TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="fd8ed-104">Transformiert ein Array (x, y, z, 1) durch eine bestimmte Matrix.</span><span class="sxs-lookup"><span data-stu-id="fd8ed-104">Transforms an array (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd8ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd8ed-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="fd8ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd8ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd8ed-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fd8ed-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8ed-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd8ed-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fd8ed-109">Zeiger auf das [**D3DXVECTOR4-Array,**](d3dxvector4.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="fd8ed-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fd8ed-110">*OutStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fd8ed-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8ed-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd8ed-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd8ed-112">Stride zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="fd8ed-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="fd8ed-113">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fd8ed-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8ed-114">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd8ed-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fd8ed-115">Zeiger auf das [**D3DXVECTOR3-Quellarray.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="fd8ed-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="fd8ed-116">*VStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fd8ed-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8ed-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd8ed-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd8ed-118">Stride zwischen Vektoren im Eingabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="fd8ed-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="fd8ed-119">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fd8ed-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8ed-120">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd8ed-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fd8ed-121">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="fd8ed-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fd8ed-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd8ed-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8ed-123">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd8ed-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd8ed-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="fd8ed-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd8ed-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd8ed-125">Return value</span></span>

<span data-ttu-id="fd8ed-126">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd8ed-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fd8ed-127">Zeiger auf ein transformiertes [**D3DXVECTOR4-Array.**](d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="fd8ed-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd8ed-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd8ed-128">Remarks</span></span>

<span data-ttu-id="fd8ed-129">Diese Funktion transformiert das Array *pV* (x, y, z, 1) durch die Matrix *pM.*</span><span class="sxs-lookup"><span data-stu-id="fd8ed-129">This function transforms the array *pV* (x, y, z, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="fd8ed-130">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd8ed-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fd8ed-131">Auf diese Weise kann die **D3DXVec3TransformArray-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd8ed-131">In this way, the **D3DXVec3TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd8ed-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd8ed-132">Requirements</span></span>



| <span data-ttu-id="fd8ed-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd8ed-133">Requirement</span></span> | <span data-ttu-id="fd8ed-134">Wert</span><span class="sxs-lookup"><span data-stu-id="fd8ed-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd8ed-135">Header</span><span class="sxs-lookup"><span data-stu-id="fd8ed-135">Header</span></span><br/>  | <dl> <span data-ttu-id="fd8ed-136"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="fd8ed-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fd8ed-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fd8ed-137">Library</span></span><br/> | <dl> <span data-ttu-id="fd8ed-138"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd8ed-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd8ed-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fd8ed-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd8ed-140">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="fd8ed-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
