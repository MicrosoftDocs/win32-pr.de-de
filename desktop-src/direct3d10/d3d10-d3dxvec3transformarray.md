---
description: Transformiert ein Array (x, y, z, 1) durch eine angegebene Matrix.
ms.assetid: f64c55df-ea93-4c93-be89-eee650e6ecf0
title: D3DXVec3TransformArray-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 9ae223d4e1b8c424230ba12719f25258dae18548
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050902"
---
# <a name="d3dxvec3transformarray-function-d3dx10mathh"></a><span data-ttu-id="87392-103">D3DXVec3TransformArray-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="87392-103">D3DXVec3TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="87392-104">Transformiert ein Array (x, y, z, 1) durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="87392-104">Transforms an array (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="87392-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87392-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="87392-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87392-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87392-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="87392-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="87392-108">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="87392-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="87392-109">Zeiger auf das [**D3DXVECTOR4**](d3d10-d3dxvector4.md) -Array, das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="87392-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="87392-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87392-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87392-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87392-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87392-112">Schritt zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="87392-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="87392-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87392-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87392-114">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="87392-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="87392-115">Zeiger auf das Quell- [**D3DXVECTOR3**](d3d10-d3dxvector3.md) Array.</span><span class="sxs-lookup"><span data-stu-id="87392-115">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="87392-116">*Vstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87392-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87392-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87392-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87392-118">Schritt zwischen Vektoren im Eingabedaten Strom.</span><span class="sxs-lookup"><span data-stu-id="87392-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="87392-119">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87392-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87392-120">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="87392-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="87392-121">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="87392-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="87392-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87392-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87392-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87392-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87392-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="87392-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87392-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87392-125">Return value</span></span>

<span data-ttu-id="87392-126">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="87392-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="87392-127">Zeiger auf ein [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformiertes Array.</span><span class="sxs-lookup"><span data-stu-id="87392-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="87392-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87392-128">Remarks</span></span>

<span data-ttu-id="87392-129">Diese Funktion wandelt das Array PV (x, y, z, 1) durch die Matrix pm um.</span><span class="sxs-lookup"><span data-stu-id="87392-129">This function transforms the array pV (x, y, z, 1) by the matrix pM.</span></span>

<span data-ttu-id="87392-130">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="87392-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="87392-131">Auf diese Weise kann die D3DXVec3TransformArray-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87392-131">In this way, the D3DXVec3TransformArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="87392-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87392-132">Requirements</span></span>



| <span data-ttu-id="87392-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87392-133">Requirement</span></span> | <span data-ttu-id="87392-134">Wert</span><span class="sxs-lookup"><span data-stu-id="87392-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87392-135">Header</span><span class="sxs-lookup"><span data-stu-id="87392-135">Header</span></span><br/> | <dl> <span data-ttu-id="87392-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="87392-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87392-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87392-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87392-138">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="87392-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
