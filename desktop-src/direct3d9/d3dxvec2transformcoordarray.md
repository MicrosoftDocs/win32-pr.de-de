---
description: Transformiert ein Array (x, y, 0, 1) durch eine angegebene Matrix und projiziert das Ergebnis zurück in w = 1.
ms.assetid: 23c88bed-344b-4b3a-bb92-e50cbe96daf9
title: D3DXVec2TransformCoordArray-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoordArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e924f9c008efe76490f9f51903a1c31f254e0001
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355200"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx9mathh"></a><span data-ttu-id="13255-103">D3DXVec2TransformCoordArray-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="13255-103">D3DXVec2TransformCoordArray function (D3dx9math.h)</span></span>

<span data-ttu-id="13255-104">Transformiert ein Array (x, y, 0, 1) durch eine angegebene Matrix und projiziert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="13255-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="13255-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13255-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoordArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="13255-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13255-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13255-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="13255-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="13255-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="13255-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="13255-109">Ein Zeiger auf die [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="13255-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="13255-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13255-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13255-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13255-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13255-112">Schritt zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="13255-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="13255-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13255-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13255-114">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="13255-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="13255-115">Zeiger auf das Quell- [**D3DXVECTOR2**](d3dxvector2.md) Array.</span><span class="sxs-lookup"><span data-stu-id="13255-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="13255-116">*Vstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13255-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13255-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13255-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13255-118">Schritt zwischen Vektoren im Eingabedaten Strom.</span><span class="sxs-lookup"><span data-stu-id="13255-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="13255-119">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13255-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13255-120">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="13255-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="13255-121">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="13255-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="13255-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13255-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13255-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13255-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13255-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="13255-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13255-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13255-125">Return value</span></span>

<span data-ttu-id="13255-126">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="13255-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="13255-127">Zeiger auf ein [**D3DXVECTOR4**](d3dxvector4.md) transformiertes Array.</span><span class="sxs-lookup"><span data-stu-id="13255-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="13255-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13255-128">Remarks</span></span>

<span data-ttu-id="13255-129">Diese Funktion wandelt das Array *PV* (x, y, 0, 1) durch die Matrix *pm* um und projiziert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="13255-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*, projecting the result back into w = 1.</span></span>

<span data-ttu-id="13255-130">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13255-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="13255-131">Auf diese Weise kann die **D3DXVec2TransformCoordArray** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13255-131">In this way, the **D3DXVec2TransformCoordArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="13255-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13255-132">Requirements</span></span>



| <span data-ttu-id="13255-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13255-133">Requirement</span></span> | <span data-ttu-id="13255-134">Wert</span><span class="sxs-lookup"><span data-stu-id="13255-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13255-135">Header</span><span class="sxs-lookup"><span data-stu-id="13255-135">Header</span></span><br/>  | <dl> <span data-ttu-id="13255-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="13255-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="13255-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="13255-137">Library</span></span><br/> | <dl> <span data-ttu-id="13255-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13255-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="13255-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13255-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13255-140">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="13255-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
