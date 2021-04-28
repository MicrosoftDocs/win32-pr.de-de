---
description: 'D3DXVec2TransformNormalArray-Funktion (D3dx9math.h): Transformiert ein Array (x, y, 0, 0) durch eine bestimmte Matrix.'
ms.assetid: 9f5d8fdc-f3e1-41dc-be4e-9ffc6be1947f
title: D3DXVec2TransformNormalArray-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71706551e73ed9bd52b41aae127625cd09b6d7f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097891"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="b62a8-103">D3DXVec2TransformNormalArray-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="b62a8-103">D3DXVec2TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="b62a8-104">Transformiert ein Array (x, y, 0, 0) durch eine bestimmte Matrix.</span><span class="sxs-lookup"><span data-stu-id="b62a8-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b62a8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b62a8-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="b62a8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b62a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b62a8-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b62a8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b62a8-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="b62a8-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="b62a8-109">Zeiger auf die [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="b62a8-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b62a8-110">*OutStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b62a8-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b62a8-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b62a8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b62a8-112">Stride zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="b62a8-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="b62a8-113">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b62a8-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b62a8-114">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="b62a8-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="b62a8-115">Zeiger auf das [**D3DXVECTOR2-Quellarray.**](d3dxvector2.md)</span><span class="sxs-lookup"><span data-stu-id="b62a8-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="b62a8-116">*VStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b62a8-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b62a8-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b62a8-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b62a8-118">Stride zwischen Vektoren im Eingabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="b62a8-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="b62a8-119">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b62a8-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b62a8-120">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b62a8-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b62a8-121">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="b62a8-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b62a8-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b62a8-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b62a8-123">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b62a8-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b62a8-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="b62a8-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b62a8-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b62a8-125">Return value</span></span>

<span data-ttu-id="b62a8-126">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="b62a8-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="b62a8-127">Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die das transformierte Array ist.</span><span class="sxs-lookup"><span data-stu-id="b62a8-127">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="b62a8-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b62a8-128">Remarks</span></span>

<span data-ttu-id="b62a8-129">Diese Funktion transformiert den Vektor (*pV-*>x, *pV-*>y, 0, 0) durch die Matrix, auf die *pM zeigt.*</span><span class="sxs-lookup"><span data-stu-id="b62a8-129">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM.*</span></span>

<span data-ttu-id="b62a8-130">Wenn Sie einen normalen transformieren möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Transponieren der Umkehrung der Matrix sein, die Sie zum Transformieren eines Punkts verwenden würden.</span><span class="sxs-lookup"><span data-stu-id="b62a8-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="b62a8-131">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b62a8-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b62a8-132">Auf diese Weise kann die **D3DXVec2TransformNormalArray-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b62a8-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b62a8-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b62a8-133">Requirements</span></span>



| <span data-ttu-id="b62a8-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b62a8-134">Requirement</span></span> | <span data-ttu-id="b62a8-135">Wert</span><span class="sxs-lookup"><span data-stu-id="b62a8-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b62a8-136">Header</span><span class="sxs-lookup"><span data-stu-id="b62a8-136">Header</span></span><br/>  | <dl> <span data-ttu-id="b62a8-137"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="b62a8-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b62a8-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b62a8-138">Library</span></span><br/> | <dl> <span data-ttu-id="b62a8-139"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b62a8-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b62a8-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b62a8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b62a8-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="b62a8-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
