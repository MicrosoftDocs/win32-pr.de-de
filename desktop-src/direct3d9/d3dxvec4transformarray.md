---
description: Transformiert ein Array (x, y, 0, 1) durch eine angegebene Matrix.
ms.assetid: 11d69f65-2aef-46f4-b274-e173a11382a8
title: D3DXVec4TransformArray-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3102d1766ba43525829e045503c1838a19d4b0e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354419"
---
# <a name="d3dxvec4transformarray-function-d3dx9mathh"></a><span data-ttu-id="eb72c-103">D3DXVec4TransformArray-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="eb72c-103">D3DXVec4TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="eb72c-104">Transformiert ein Array (x, y, 0, 1) durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="eb72c-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb72c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb72c-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="eb72c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb72c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb72c-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eb72c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb72c-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb72c-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="eb72c-109">Zeiger auf das [**D3DXVECTOR4**](d3dxvector4.md) -Array, das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="eb72c-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eb72c-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb72c-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb72c-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb72c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb72c-112">Schritt zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="eb72c-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="eb72c-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb72c-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb72c-114">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb72c-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="eb72c-115">Zeiger auf das Quell- [**D3DXVECTOR4**](d3dxvector4.md) Array.</span><span class="sxs-lookup"><span data-stu-id="eb72c-115">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="eb72c-116">*Vstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb72c-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb72c-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb72c-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb72c-118">Schritt zwischen Vektoren im Eingabedaten Strom.</span><span class="sxs-lookup"><span data-stu-id="eb72c-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="eb72c-119">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb72c-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb72c-120">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb72c-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eb72c-121">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="eb72c-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="eb72c-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb72c-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb72c-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb72c-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb72c-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="eb72c-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb72c-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb72c-125">Return value</span></span>

<span data-ttu-id="eb72c-126">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb72c-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="eb72c-127">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das transformierte Array ist.</span><span class="sxs-lookup"><span data-stu-id="eb72c-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb72c-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb72c-128">Remarks</span></span>

<span data-ttu-id="eb72c-129">Diese Funktion wandelt das Array *PV* (x, y, 0, 1) durch die Matrix *pm* um.</span><span class="sxs-lookup"><span data-stu-id="eb72c-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="eb72c-130">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eb72c-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="eb72c-131">Auf diese Weise kann die **D3DXVec4TransformArray** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb72c-131">In this way, the **D3DXVec4TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb72c-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb72c-132">Requirements</span></span>



| <span data-ttu-id="eb72c-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb72c-133">Requirement</span></span> | <span data-ttu-id="eb72c-134">Wert</span><span class="sxs-lookup"><span data-stu-id="eb72c-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb72c-135">Header</span><span class="sxs-lookup"><span data-stu-id="eb72c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="eb72c-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb72c-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="eb72c-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eb72c-137">Library</span></span><br/> | <dl> <span data-ttu-id="eb72c-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb72c-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eb72c-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb72c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb72c-140">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="eb72c-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
