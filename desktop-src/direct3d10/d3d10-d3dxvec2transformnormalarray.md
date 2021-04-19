---
description: Transformiert ein Array (x, y, 0, 0) durch eine angegebene Matrix.
ms.assetid: a53f998a-f2a5-4e4b-bc1c-c1f46284d78b
title: D3DXVec2TransformNormalArray-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 4850961560ae810b9a21f58fbefa9b6b07227c77
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357260"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx10mathh"></a><span data-ttu-id="30d1d-103">D3DXVec2TransformNormalArray-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="30d1d-103">D3DXVec2TransformNormalArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="30d1d-104">Transformiert ein Array (x, y, 0, 0) durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="30d1d-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="30d1d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="30d1d-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="30d1d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30d1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30d1d-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="30d1d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30d1d-108">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="30d1d-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="30d1d-109">Zeiger auf das [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="30d1d-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="30d1d-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30d1d-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30d1d-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30d1d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30d1d-112">Schritt zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="30d1d-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="30d1d-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30d1d-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30d1d-114">Typ: **Konstanten [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="30d1d-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="30d1d-115">Zeiger auf das Quell-D3DXVECTOR2 Array.</span><span class="sxs-lookup"><span data-stu-id="30d1d-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="30d1d-116">*Vstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30d1d-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30d1d-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30d1d-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30d1d-118">Schritt zwischen Vektoren im Eingabedaten Strom.</span><span class="sxs-lookup"><span data-stu-id="30d1d-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="30d1d-119">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30d1d-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30d1d-120">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="30d1d-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="30d1d-121">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="30d1d-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="30d1d-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30d1d-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30d1d-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30d1d-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30d1d-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="30d1d-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30d1d-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30d1d-125">Return value</span></span>

<span data-ttu-id="30d1d-126">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="30d1d-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="30d1d-127">Zeiger auf eine D3DXVECTOR2-Struktur, die das transformierte Array ist.</span><span class="sxs-lookup"><span data-stu-id="30d1d-127">Pointer to a D3DXVECTOR2 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="30d1d-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30d1d-128">Remarks</span></span>

<span data-ttu-id="30d1d-129">Diese Funktion transformiert den Vektor (PV->x, PV->y, 0, 0) durch die Matrix, auf die von pm gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="30d1d-129">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="30d1d-130">Wenn Sie eine normale Transformation durchführen möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Umwandlung der Umkehrung der Matrix sein, die zum Transformieren eines Punkts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="30d1d-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="30d1d-131">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="30d1d-131">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="30d1d-132">Auf diese Weise kann die **D3DXVec2TransformNormalArray** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="30d1d-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="30d1d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30d1d-133">Requirements</span></span>



| <span data-ttu-id="30d1d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30d1d-134">Requirement</span></span> | <span data-ttu-id="30d1d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="30d1d-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30d1d-136">Header</span><span class="sxs-lookup"><span data-stu-id="30d1d-136">Header</span></span><br/>  | <dl> <span data-ttu-id="30d1d-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="30d1d-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="30d1d-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30d1d-138">Library</span></span><br/> | <dl> <span data-ttu-id="30d1d-139"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30d1d-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="30d1d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30d1d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30d1d-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="30d1d-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
