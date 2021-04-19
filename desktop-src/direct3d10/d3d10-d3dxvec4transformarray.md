---
description: Transformiert ein Array (x, y, z, w) durch eine angegebene Matrix.
ms.assetid: afd5cccb-e22f-4726-a84e-9eac1c1c277f
title: D3DXVec4TransformArray-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 5571fb19786e19a61c85741bcf6d4acb5231e977
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366672"
---
# <a name="d3dxvec4transformarray-function-d3dx10mathh"></a><span data-ttu-id="62fd7-103">D3DXVec4TransformArray-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="62fd7-103">D3DXVec4TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="62fd7-104">Transformiert ein Array (x, y, z, w) durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="62fd7-104">Transforms an array (x, y, z, w) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="62fd7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="62fd7-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR4 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="62fd7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="62fd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62fd7-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="62fd7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="62fd7-108">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="62fd7-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="62fd7-109">Zeiger auf das [**D3DXVECTOR4**](d3d10-d3dxvector4.md) -Array, das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="62fd7-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="62fd7-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62fd7-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fd7-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62fd7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62fd7-112">Schritt zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="62fd7-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="62fd7-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62fd7-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fd7-114">Typ: **Konstanten [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="62fd7-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="62fd7-115">Zeiger auf das Quell-D3DXVECTOR4 Array.</span><span class="sxs-lookup"><span data-stu-id="62fd7-115">Pointer to the source D3DXVECTOR4 array.</span></span>

</dd> <dt>

<span data-ttu-id="62fd7-116">*Vstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62fd7-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fd7-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62fd7-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62fd7-118">Schritt zwischen Vektoren im Eingabedaten Strom.</span><span class="sxs-lookup"><span data-stu-id="62fd7-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="62fd7-119">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62fd7-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fd7-120">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="62fd7-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="62fd7-121">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="62fd7-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="62fd7-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62fd7-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fd7-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="62fd7-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="62fd7-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="62fd7-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62fd7-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62fd7-125">Return value</span></span>

<span data-ttu-id="62fd7-126">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="62fd7-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="62fd7-127">Zeiger auf eine [**D3DXVECTOR4**](d3d10-d3dxvector4.md) -Struktur, die das transformierte Array ist.</span><span class="sxs-lookup"><span data-stu-id="62fd7-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="62fd7-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62fd7-128">Remarks</span></span>

<span data-ttu-id="62fd7-129">Diese Funktion wandelt das Array PV (x, y, z, w) durch die Matrix pm um.</span><span class="sxs-lookup"><span data-stu-id="62fd7-129">This function transforms the array pV (x, y, z, w) by the matrix pM.</span></span>

<span data-ttu-id="62fd7-130">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="62fd7-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="62fd7-131">Auf diese Weise kann die **D3DXVec4TransformArray** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62fd7-131">In this way, the **D3DXVec4TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="62fd7-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62fd7-132">Requirements</span></span>



| <span data-ttu-id="62fd7-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62fd7-133">Requirement</span></span> | <span data-ttu-id="62fd7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="62fd7-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62fd7-135">Header</span><span class="sxs-lookup"><span data-stu-id="62fd7-135">Header</span></span><br/> | <dl> <span data-ttu-id="62fd7-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="62fd7-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62fd7-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62fd7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62fd7-138">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="62fd7-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
