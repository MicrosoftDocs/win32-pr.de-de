---
description: 'D3DXVec3TransformCoordArray-Funktion (D3DX10Math.h): Transformiert ein Array (x, y, z, 1) durch eine angegebene Matrix und projiziert das Ergebnis zurück in w = 1.'
ms.assetid: 259a885d-89be-4fea-a579-dac3dd76878f
title: D3DXVec3TransformCoordArray-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: c4a1edfd89b127d0782d3bab23c2390775422c69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103108"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="00be4-103">D3DXVec3TransformCoordArray-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="00be4-103">D3DXVec3TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="00be4-104">Transformiert ein Array (x, y, z, 1) durch eine bestimmte Matrix und projiziert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="00be4-104">Transforms an array (x, y, z, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="00be4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00be4-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="00be4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00be4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00be4-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="00be4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="00be4-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="00be4-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="00be4-109">Zeiger auf [**D3DXVECTOR3,**](d3d10-d3dxvector3.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="00be4-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="00be4-110">*OutStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="00be4-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00be4-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00be4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00be4-112">Schreitet zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="00be4-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="00be4-113">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="00be4-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00be4-114">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="00be4-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="00be4-115">Zeiger auf das D3DXVECTOR3-Quellarray.</span><span class="sxs-lookup"><span data-stu-id="00be4-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="00be4-116">*VStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="00be4-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00be4-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00be4-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00be4-118">Schreitet zwischen Vektoren im Eingabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="00be4-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="00be4-119">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="00be4-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00be4-120">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="00be4-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="00be4-121">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="00be4-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="00be4-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00be4-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00be4-123">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00be4-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00be4-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="00be4-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00be4-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00be4-125">Return value</span></span>

<span data-ttu-id="00be4-126">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="00be4-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="00be4-127">Zeiger auf eine D3DXVECTOR3-Struktur, die das transformierte Array ist.</span><span class="sxs-lookup"><span data-stu-id="00be4-127">Pointer to a D3DXVECTOR3 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="00be4-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00be4-128">Remarks</span></span>

<span data-ttu-id="00be4-129">Diese Funktion transformiert das Array pV (x, y, z, 1) durch die Matrix pM und projektiert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="00be4-129">This function transforms the array pV (x, y, z, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="00be4-130">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="00be4-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="00be4-131">Auf diese Weise kann die [**D3DXVec3TransformCoord-Funktion**](d3d10-d3dxvec3transformcoord.md) als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00be4-131">In this way, the [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="00be4-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00be4-132">Requirements</span></span>



| <span data-ttu-id="00be4-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00be4-133">Requirement</span></span> | <span data-ttu-id="00be4-134">Wert</span><span class="sxs-lookup"><span data-stu-id="00be4-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00be4-135">Header</span><span class="sxs-lookup"><span data-stu-id="00be4-135">Header</span></span><br/> | <dl> <span data-ttu-id="00be4-136"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="00be4-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00be4-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="00be4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00be4-138">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="00be4-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
