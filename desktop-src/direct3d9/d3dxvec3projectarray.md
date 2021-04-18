---
description: Projiziert ein Array (x, y, z, 0) aus dem Objekt Raum in den Bildschirmbereich.
ms.assetid: cf022741-0bae-4c22-872f-bd94c3721aff
title: D3DXVec3ProjectArray-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f802d8ab564f2cbfe1cc60ad6aed13959bef9383
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354412"
---
# <a name="d3dxvec3projectarray-function-d3dx9mathh"></a><span data-ttu-id="a3d1a-103">D3DXVec3ProjectArray-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a3d1a-103">D3DXVec3ProjectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="a3d1a-104">Projiziert ein Array (x, y, z, 0) aus dem Objekt Raum in den Bildschirmbereich.</span><span class="sxs-lookup"><span data-stu-id="a3d1a-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d1a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3d1a-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a><span data-ttu-id="a3d1a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3d1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3d1a-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a3d1a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d1a-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3d1a-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3d1a-109">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="a3d1a-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a3d1a-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d1a-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d1a-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3d1a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3d1a-112">Schritt zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="a3d1a-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="a3d1a-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d1a-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d1a-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3d1a-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3d1a-115">Ein Zeiger auf die Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a3d1a-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a3d1a-116">*Vstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d1a-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d1a-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3d1a-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3d1a-118">Schritt zwischen Vektoren im Eingabedaten Strom.</span><span class="sxs-lookup"><span data-stu-id="a3d1a-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="a3d1a-119">*pviewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d1a-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d1a-120">Typ: **Konstanten [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3d1a-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="a3d1a-121">Zeiger auf eine [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur, die den Viewport darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3d1a-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="a3d1a-122">*pprojection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d1a-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d1a-123">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3d1a-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a3d1a-124">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Projektions Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3d1a-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a3d1a-125">*PView* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d1a-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d1a-126">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3d1a-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a3d1a-127">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Ansichts Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3d1a-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a3d1a-128">*pworld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d1a-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d1a-129">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3d1a-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a3d1a-130">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Weltmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3d1a-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a3d1a-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d1a-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d1a-132">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3d1a-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3d1a-133">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="a3d1a-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3d1a-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3d1a-134">Return value</span></span>

<span data-ttu-id="a3d1a-135">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3d1a-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3d1a-136">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, bei der es sich um das Array handelt, das vom Objekt Raum auf den Bildschirmbereich</span><span class="sxs-lookup"><span data-stu-id="a3d1a-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3d1a-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3d1a-137">Remarks</span></span>

<span data-ttu-id="a3d1a-138">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a3d1a-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a3d1a-139">Auf diese Weise kann die **D3DXVec3ProjectArray** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3d1a-139">In this way, the **D3DXVec3ProjectArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d1a-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3d1a-140">Requirements</span></span>



| <span data-ttu-id="a3d1a-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3d1a-141">Requirement</span></span> | <span data-ttu-id="a3d1a-142">Wert</span><span class="sxs-lookup"><span data-stu-id="a3d1a-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3d1a-143">Header</span><span class="sxs-lookup"><span data-stu-id="a3d1a-143">Header</span></span><br/>  | <dl> <span data-ttu-id="a3d1a-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3d1a-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a3d1a-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3d1a-145">Library</span></span><br/> | <dl> <span data-ttu-id="a3d1a-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3d1a-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a3d1a-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3d1a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3d1a-148">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a3d1a-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a3d1a-149">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="a3d1a-149">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 
