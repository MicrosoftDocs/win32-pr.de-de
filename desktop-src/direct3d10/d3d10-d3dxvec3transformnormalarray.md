---
description: Transformiert ein Array (x, y, z, 0) durch eine angegebene Matrix.
ms.assetid: 7f0a41ce-bd3a-4e35-9a5d-8178a4e7bd44
title: D3DXVec3TransformNormalArray-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: facb5591becd27d3fff283e8d531118ca433d5d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366446"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx10mathh"></a><span data-ttu-id="5cc43-103">D3DXVec3TransformNormalArray-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="5cc43-103">D3DXVec3TransformNormalArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="5cc43-104">Transformiert ein Array (x, y, z, 0) durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="5cc43-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cc43-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cc43-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="5cc43-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cc43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cc43-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5cc43-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5cc43-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5cc43-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5cc43-109">Zeiger auf das [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Array, das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="5cc43-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5cc43-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5cc43-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cc43-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5cc43-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5cc43-112">Schritt zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="5cc43-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="5cc43-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5cc43-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cc43-114">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5cc43-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5cc43-115">Zeiger auf das Quell-D3DXVECTOR3 Array.</span><span class="sxs-lookup"><span data-stu-id="5cc43-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="5cc43-116">*Vstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5cc43-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cc43-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5cc43-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5cc43-118">Schritt zwischen Vektoren im Eingabedaten Strom.</span><span class="sxs-lookup"><span data-stu-id="5cc43-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="5cc43-119">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5cc43-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cc43-120">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5cc43-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5cc43-121">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5cc43-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5cc43-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5cc43-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cc43-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5cc43-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5cc43-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="5cc43-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cc43-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5cc43-125">Return value</span></span>

<span data-ttu-id="5cc43-126">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5cc43-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5cc43-127">Zeiger auf ein D3DXVECTOR3-Array, das das transformierte Array ist.</span><span class="sxs-lookup"><span data-stu-id="5cc43-127">Pointer to a D3DXVECTOR3 array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cc43-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5cc43-128">Remarks</span></span>

<span data-ttu-id="5cc43-129">Diese Funktion transformiert den Vektor (PV->x, PV->y, PV->z, 0) durch die Matrix, auf die von pm gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5cc43-129">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="5cc43-130">Wenn Sie eine normale Transformation durchführen möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Umwandlung der Umkehrung der Matrix sein, die zum Transformieren eines Punkts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5cc43-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="5cc43-131">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5cc43-131">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5cc43-132">Auf diese Weise kann die **D3DXVec3TransformNormalArray** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5cc43-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cc43-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5cc43-133">Requirements</span></span>



| <span data-ttu-id="5cc43-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5cc43-134">Requirement</span></span> | <span data-ttu-id="5cc43-135">Wert</span><span class="sxs-lookup"><span data-stu-id="5cc43-135">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cc43-136">Header</span><span class="sxs-lookup"><span data-stu-id="5cc43-136">Header</span></span><br/> | <dl> <span data-ttu-id="5cc43-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cc43-137"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cc43-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cc43-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cc43-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5cc43-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
