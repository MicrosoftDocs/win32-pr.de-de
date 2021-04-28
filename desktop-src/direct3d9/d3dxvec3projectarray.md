---
description: 'D3DXVec3ProjectArray-Funktion (D3dx9math.h): Projiziert ein Array (x, y, z, 0) aus dem Objektbereich in den Bildschirmbereich.'
ms.assetid: cf022741-0bae-4c22-872f-bd94c3721aff
title: D3DXVec3ProjectArray-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 10f0e19ad5bdbff59d7386223c88ed867e8d0d88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097808"
---
# <a name="d3dxvec3projectarray-function-d3dx9mathh"></a><span data-ttu-id="58fb3-103">D3DXVec3ProjectArray-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="58fb3-103">D3DXVec3ProjectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="58fb3-104">Projektet ein Array (x, y, z, 0) aus dem Objektbereich in den Bildschirmbereich.</span><span class="sxs-lookup"><span data-stu-id="58fb3-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="58fb3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58fb3-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="58fb3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58fb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58fb3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="58fb3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="58fb3-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="58fb3-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="58fb3-109">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="58fb3-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="58fb3-110">*OutStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="58fb3-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fb3-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58fb3-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58fb3-112">Stride zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="58fb3-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="58fb3-113">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="58fb3-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fb3-114">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="58fb3-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="58fb3-115">Zeiger auf die [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="58fb3-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="58fb3-116">*VStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="58fb3-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fb3-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58fb3-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58fb3-118">Stride zwischen Vektoren im Eingabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="58fb3-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="58fb3-119">*pViewport* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="58fb3-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fb3-120">Typ: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="58fb3-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="58fb3-121">Zeiger auf eine [**D3DVIEWPORT9-Struktur,**](d3dviewport9.md) die den Viewport darstellt.</span><span class="sxs-lookup"><span data-stu-id="58fb3-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="58fb3-122">*pProjection* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="58fb3-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fb3-123">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="58fb3-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="58fb3-124">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Projektionsmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="58fb3-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="58fb3-125">*pView* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="58fb3-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fb3-126">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="58fb3-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="58fb3-127">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Ansichtsmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="58fb3-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="58fb3-128">*pWorld* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="58fb3-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fb3-129">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="58fb3-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="58fb3-130">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Weltmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="58fb3-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="58fb3-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58fb3-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fb3-132">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58fb3-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58fb3-133">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="58fb3-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58fb3-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58fb3-134">Return value</span></span>

<span data-ttu-id="58fb3-135">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="58fb3-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="58fb3-136">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) bei der es sich um das Array handelt, das vom Objektbereich in den Bildschirmbereich projiziert wird.</span><span class="sxs-lookup"><span data-stu-id="58fb3-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="58fb3-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58fb3-137">Remarks</span></span>

<span data-ttu-id="58fb3-138">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="58fb3-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="58fb3-139">Auf diese Weise kann die **D3DXVec3ProjectArray-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58fb3-139">In this way, the **D3DXVec3ProjectArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="58fb3-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58fb3-140">Requirements</span></span>



| <span data-ttu-id="58fb3-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58fb3-141">Requirement</span></span> | <span data-ttu-id="58fb3-142">Wert</span><span class="sxs-lookup"><span data-stu-id="58fb3-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58fb3-143">Header</span><span class="sxs-lookup"><span data-stu-id="58fb3-143">Header</span></span><br/>  | <dl> <span data-ttu-id="58fb3-144"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="58fb3-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="58fb3-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="58fb3-145">Library</span></span><br/> | <dl> <span data-ttu-id="58fb3-146"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="58fb3-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="58fb3-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="58fb3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58fb3-148">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="58fb3-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="58fb3-149">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="58fb3-149">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 
