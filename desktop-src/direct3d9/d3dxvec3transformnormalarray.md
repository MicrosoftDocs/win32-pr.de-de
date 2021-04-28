---
description: 'D3DXVec3TransformNormalArray-Funktion (D3dx9math.h): Transformiert ein Array (x, y, z, 0) durch eine bestimmte Matrix.'
ms.assetid: c12fad52-d541-483f-a919-e6031aa4f761
title: D3DXVec3TransformNormalArray-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74da959002bfbd0c488e630f09c89e848708b1b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097728"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="a2def-103">D3DXVec3TransformNormalArray-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="a2def-103">D3DXVec3TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="a2def-104">Transformiert ein Array (x, y, z, 0) durch eine bestimmte Matrix.</span><span class="sxs-lookup"><span data-stu-id="a2def-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2def-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2def-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a2def-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2def-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2def-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a2def-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2def-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a2def-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a2def-109">Zeiger auf das [**D3DXVECTOR3-Array,**](d3dxvector3.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="a2def-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a2def-110">*OutStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a2def-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2def-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2def-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2def-112">Stride zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="a2def-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="a2def-113">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a2def-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2def-114">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a2def-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a2def-115">Zeiger auf das [**D3DXVECTOR3-Quellarray.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="a2def-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="a2def-116">*VStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a2def-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2def-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2def-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2def-118">Stride zwischen Vektoren im Eingabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="a2def-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="a2def-119">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a2def-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2def-120">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a2def-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a2def-121">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="a2def-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a2def-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2def-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2def-123">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2def-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2def-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="a2def-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2def-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2def-125">Return value</span></span>

<span data-ttu-id="a2def-126">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a2def-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a2def-127">Zeiger auf ein [**D3DXVECTOR3-Array,**](d3dxvector3.md) das das transformierte Array ist.</span><span class="sxs-lookup"><span data-stu-id="a2def-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2def-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2def-128">Remarks</span></span>

<span data-ttu-id="a2def-129">Diese Funktion transformiert den Vektor (*pV*->x, *pV*->y, *pV*->z, 0) durch die Matrix, auf die *pM* zeigt.</span><span class="sxs-lookup"><span data-stu-id="a2def-129">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="a2def-130">Wenn Sie einen normalen transformieren möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Transponieren der Umkehrung der Matrix sein, die Sie zum Transformieren eines Punkts verwenden würden.</span><span class="sxs-lookup"><span data-stu-id="a2def-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="a2def-131">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a2def-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a2def-132">Auf diese Weise kann die **D3DXVec3TransformNormalArray-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2def-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2def-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2def-133">Requirements</span></span>



| <span data-ttu-id="a2def-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2def-134">Requirement</span></span> | <span data-ttu-id="a2def-135">Wert</span><span class="sxs-lookup"><span data-stu-id="a2def-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2def-136">Header</span><span class="sxs-lookup"><span data-stu-id="a2def-136">Header</span></span><br/>  | <dl> <span data-ttu-id="a2def-137"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a2def-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a2def-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a2def-138">Library</span></span><br/> | <dl> <span data-ttu-id="a2def-139"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2def-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a2def-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a2def-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2def-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a2def-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
