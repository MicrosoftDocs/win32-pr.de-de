---
description: Transformiert ein Array (x, y, z, 1) durch eine angegebene Matrix.
ms.assetid: fd7ab674-5e42-4265-afad-ae5a00dabcdb
title: D3DXVec3TransformArray-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0b515c98be82aa47801b333c4b25680e0e464b2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354376"
---
# <a name="d3dxvec3transformarray-function-d3dx9mathh"></a><span data-ttu-id="07669-103">D3DXVec3TransformArray-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="07669-103">D3DXVec3TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="07669-104">Transformiert ein Array (x, y, z, 1) durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="07669-104">Transforms an array (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="07669-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07669-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="07669-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="07669-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07669-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="07669-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07669-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="07669-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="07669-109">Zeiger auf das [**D3DXVECTOR4**](d3dxvector4.md) -Array, das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="07669-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="07669-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07669-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07669-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07669-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07669-112">Schritt zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="07669-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="07669-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07669-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07669-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="07669-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="07669-115">Zeiger auf das Quell- [**D3DXVECTOR3**](d3dxvector3.md) Array.</span><span class="sxs-lookup"><span data-stu-id="07669-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="07669-116">*Vstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07669-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07669-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07669-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07669-118">Schritt zwischen Vektoren im Eingabedaten Strom.</span><span class="sxs-lookup"><span data-stu-id="07669-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="07669-119">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07669-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07669-120">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="07669-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="07669-121">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="07669-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="07669-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07669-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07669-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07669-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07669-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="07669-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07669-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07669-125">Return value</span></span>

<span data-ttu-id="07669-126">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="07669-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="07669-127">Zeiger auf ein [**D3DXVECTOR4**](d3dxvector4.md) transformiertes Array.</span><span class="sxs-lookup"><span data-stu-id="07669-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="07669-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07669-128">Remarks</span></span>

<span data-ttu-id="07669-129">Diese Funktion wandelt das Array *PV* (x, y, z, 1) durch die Matrix *pm* um.</span><span class="sxs-lookup"><span data-stu-id="07669-129">This function transforms the array *pV* (x, y, z, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="07669-130">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="07669-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="07669-131">Auf diese Weise kann die **D3DXVec3TransformArray** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07669-131">In this way, the **D3DXVec3TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="07669-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07669-132">Requirements</span></span>



| <span data-ttu-id="07669-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07669-133">Requirement</span></span> | <span data-ttu-id="07669-134">Wert</span><span class="sxs-lookup"><span data-stu-id="07669-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07669-135">Header</span><span class="sxs-lookup"><span data-stu-id="07669-135">Header</span></span><br/>  | <dl> <span data-ttu-id="07669-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="07669-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="07669-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07669-137">Library</span></span><br/> | <dl> <span data-ttu-id="07669-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07669-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07669-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07669-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07669-140">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="07669-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
