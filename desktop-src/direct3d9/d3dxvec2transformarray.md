---
description: 'D3DXVec2TransformArray-Funktion (D3dx9math.h): Transformiert ein Array (x, y, 0, 1) durch eine angegebene Matrix.'
ms.assetid: ba8c1983-bd65-4249-9451-69d813e4a3a4
title: D3DXVec2TransformArray-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 38e60c6bb8084e7f8e1c0ee71379af552e73c09d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097928"
---
# <a name="d3dxvec2transformarray-function-d3dx9mathh"></a><span data-ttu-id="6787d-103">D3DXVec2TransformArray-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="6787d-103">D3DXVec2TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="6787d-104">Transformiert ein Array (x, y, 0, 1) durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="6787d-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6787d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6787d-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="6787d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6787d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6787d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6787d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6787d-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6787d-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6787d-109">Zeiger auf die [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="6787d-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6787d-110">*OutStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6787d-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6787d-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6787d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6787d-112">Schreitet zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="6787d-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="6787d-113">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6787d-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6787d-114">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="6787d-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6787d-115">Zeiger auf die [**D3DXVECTOR2-Quellstruktur.**](d3dxvector2.md)</span><span class="sxs-lookup"><span data-stu-id="6787d-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6787d-116">*VStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6787d-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6787d-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6787d-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6787d-118">Schreitet zwischen Vektoren im Eingabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="6787d-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="6787d-119">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6787d-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6787d-120">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6787d-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6787d-121">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="6787d-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6787d-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6787d-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6787d-123">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6787d-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6787d-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="6787d-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6787d-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6787d-125">Return value</span></span>

<span data-ttu-id="6787d-126">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6787d-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6787d-127">Zeiger auf eine [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das transformierte Array ist.</span><span class="sxs-lookup"><span data-stu-id="6787d-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="6787d-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6787d-128">Remarks</span></span>

<span data-ttu-id="6787d-129">Diese Funktion transformiert das *Array pV* (x, y, 0, 1) durch die *Matrix pM*.</span><span class="sxs-lookup"><span data-stu-id="6787d-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="6787d-130">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="6787d-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6787d-131">Auf diese Weise kann die [**D3DXVec2Transform-Funktion**](d3dxvec2transform.md) als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6787d-131">In this way, the [**D3DXVec2Transform**](d3dxvec2transform.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6787d-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6787d-132">Requirements</span></span>



| <span data-ttu-id="6787d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6787d-133">Requirement</span></span> | <span data-ttu-id="6787d-134">Wert</span><span class="sxs-lookup"><span data-stu-id="6787d-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6787d-135">Header</span><span class="sxs-lookup"><span data-stu-id="6787d-135">Header</span></span><br/>  | <dl> <span data-ttu-id="6787d-136"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6787d-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6787d-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6787d-137">Library</span></span><br/> | <dl> <span data-ttu-id="6787d-138"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6787d-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6787d-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6787d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6787d-140">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="6787d-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6787d-141">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="6787d-141">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> <dt>

[<span data-ttu-id="6787d-142">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="6787d-142">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 
