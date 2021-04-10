---
description: Transformiert ein Array (x, y, z, 1) durch eine angegebene Matrix und projiziert das Ergebnis zurück in w = 1.
ms.assetid: 259a885d-89be-4fea-a579-dac3dd76878f
title: D3DXVec3TransformCoordArray-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoordArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: b0b7ca3c2898e07dc8b5e9ced0117e642bfdfb41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961634"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="d6dd8-103">D3DXVec3TransformCoordArray-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d6dd8-103">D3DXVec3TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="d6dd8-104">Transformiert ein Array (x, y, z, 1) durch eine angegebene Matrix und projiziert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-104">Transforms an array (x, y, z, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6dd8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6dd8-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoordArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="d6dd8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6dd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6dd8-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d6dd8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6dd8-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6dd8-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6dd8-109">Zeiger auf das [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d6dd8-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6dd8-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6dd8-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6dd8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6dd8-112">Schritt zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d6dd8-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6dd8-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6dd8-114">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6dd8-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6dd8-115">Zeiger auf das Quell-D3DXVECTOR3 Array.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="d6dd8-116">*Vstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6dd8-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6dd8-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6dd8-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6dd8-118">Schritt zwischen Vektoren im Eingabedaten Strom.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d6dd8-119">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6dd8-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6dd8-120">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6dd8-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d6dd8-121">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6dd8-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6dd8-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6dd8-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6dd8-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6dd8-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6dd8-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6dd8-125">Return value</span></span>

<span data-ttu-id="d6dd8-126">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6dd8-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6dd8-127">Zeiger auf eine D3DXVECTOR3-Struktur, die das transformierte Array ist.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-127">Pointer to a D3DXVECTOR3 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6dd8-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6dd8-128">Remarks</span></span>

<span data-ttu-id="d6dd8-129">Diese Funktion wandelt das Array PV (x, y, z, 1) durch die Matrix pm um und projiziert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-129">This function transforms the array pV (x, y, z, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="d6dd8-130">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d6dd8-131">Auf diese Weise kann die [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-131">In this way, the [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6dd8-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6dd8-132">Requirements</span></span>



| <span data-ttu-id="d6dd8-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6dd8-133">Requirement</span></span> | <span data-ttu-id="d6dd8-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d6dd8-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dd8-135">Header</span><span class="sxs-lookup"><span data-stu-id="d6dd8-135">Header</span></span><br/> | <dl> <span data-ttu-id="d6dd8-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6dd8-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6dd8-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6dd8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6dd8-138">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="d6dd8-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
