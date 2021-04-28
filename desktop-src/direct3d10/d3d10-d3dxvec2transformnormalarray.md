---
description: 'D3DXVec2TransformNormalArray-Funktion (D3DX10Math.h): Transformiert ein Array (x, y, 0, 0) durch eine bestimmte Matrix.'
ms.assetid: a53f998a-f2a5-4e4b-bc1c-c1f46284d78b
title: D3DXVec2TransformNormalArray-Funktion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b4e18fc2bb8c62bb86947b9eab35daae9d0242ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108278"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx10mathh"></a><span data-ttu-id="71cda-103">D3DXVec2TransformNormalArray-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="71cda-103">D3DXVec2TransformNormalArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="71cda-104">Transformiert ein Array (x, y, 0, 0) durch eine bestimmte Matrix.</span><span class="sxs-lookup"><span data-stu-id="71cda-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="71cda-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="71cda-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="71cda-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="71cda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71cda-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="71cda-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="71cda-108">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="71cda-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="71cda-109">Zeiger auf den [**D3DXVECTOR2,**](d3d10-d3dxvector2.md) der das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="71cda-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="71cda-110">*OutStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="71cda-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71cda-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71cda-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71cda-112">Stride zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="71cda-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="71cda-113">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="71cda-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71cda-114">Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="71cda-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="71cda-115">Zeiger auf das D3DXVECTOR2-Quellarray.</span><span class="sxs-lookup"><span data-stu-id="71cda-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="71cda-116">*VStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="71cda-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71cda-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71cda-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71cda-118">Stride zwischen Vektoren im Eingabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="71cda-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="71cda-119">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="71cda-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71cda-120">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="71cda-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="71cda-121">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="71cda-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="71cda-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71cda-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71cda-123">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71cda-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71cda-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="71cda-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71cda-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71cda-125">Return value</span></span>

<span data-ttu-id="71cda-126">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="71cda-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="71cda-127">Zeiger auf eine D3DXVECTOR2-Struktur, die das transformierte Array ist.</span><span class="sxs-lookup"><span data-stu-id="71cda-127">Pointer to a D3DXVECTOR2 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="71cda-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71cda-128">Remarks</span></span>

<span data-ttu-id="71cda-129">Diese Funktion transformiert den Vektor (pV->x, pV->y, 0, 0) durch die Matrix, auf die pM zeigt.</span><span class="sxs-lookup"><span data-stu-id="71cda-129">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="71cda-130">Wenn Sie einen normalen transformieren möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Transponieren der Umkehrung der Matrix sein, die Sie zum Transformieren eines Punkts verwenden würden.</span><span class="sxs-lookup"><span data-stu-id="71cda-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="71cda-131">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="71cda-131">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="71cda-132">Auf diese Weise kann die **D3DXVec2TransformNormalArray-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71cda-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="71cda-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71cda-133">Requirements</span></span>



| <span data-ttu-id="71cda-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71cda-134">Requirement</span></span> | <span data-ttu-id="71cda-135">Wert</span><span class="sxs-lookup"><span data-stu-id="71cda-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71cda-136">Header</span><span class="sxs-lookup"><span data-stu-id="71cda-136">Header</span></span><br/>  | <dl> <span data-ttu-id="71cda-137"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="71cda-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="71cda-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71cda-138">Library</span></span><br/> | <dl> <span data-ttu-id="71cda-139"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="71cda-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="71cda-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="71cda-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71cda-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="71cda-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
