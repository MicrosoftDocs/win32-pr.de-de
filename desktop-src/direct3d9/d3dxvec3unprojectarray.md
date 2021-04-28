---
description: 'D3DXVec3UnprojectArray-Funktion (D3dx9math.h): Projiziert ein Array (x, y, z, 0) aus dem Bildschirmbereich in den Objektbereich.'
ms.assetid: fef2a76c-c2fe-48c5-a1bb-6669bcc76b9b
title: D3DXVec3UnprojectArray-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 67e42b30a8f8d44bb9b21668a515a202436b7631
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097718"
---
# <a name="d3dxvec3unprojectarray-function-d3dx9mathh"></a><span data-ttu-id="54ab7-103">D3DXVec3UnprojectArray-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="54ab7-103">D3DXVec3UnprojectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="54ab7-104">Projiziert ein Array (x, y, z, 0) aus dem Bildschirmbereich in den Objektbereich.</span><span class="sxs-lookup"><span data-stu-id="54ab7-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="54ab7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54ab7-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
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



## <a name="parameters"></a><span data-ttu-id="54ab7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54ab7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54ab7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="54ab7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54ab7-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="54ab7-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="54ab7-109">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="54ab7-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="54ab7-110">*OutStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="54ab7-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54ab7-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54ab7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54ab7-112">Schreitet zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="54ab7-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="54ab7-113">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="54ab7-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54ab7-114">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="54ab7-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="54ab7-115">Zeiger auf die [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="54ab7-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="54ab7-116">*VStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="54ab7-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54ab7-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54ab7-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54ab7-118">Schreitet zwischen Vektoren im Eingabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="54ab7-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="54ab7-119">*pViewport* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="54ab7-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54ab7-120">Typ: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="54ab7-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="54ab7-121">Zeiger auf eine [**D3DVIEWPORT9-Struktur,**](d3dviewport9.md) die den Viewport darstellt.</span><span class="sxs-lookup"><span data-stu-id="54ab7-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="54ab7-122">*pProjection* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="54ab7-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54ab7-123">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="54ab7-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="54ab7-124">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Projektionsmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="54ab7-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="54ab7-125">*pView* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="54ab7-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54ab7-126">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="54ab7-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="54ab7-127">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Ansichtsmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="54ab7-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="54ab7-128">*pWorld* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="54ab7-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54ab7-129">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="54ab7-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="54ab7-130">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Weltmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="54ab7-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="54ab7-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54ab7-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54ab7-132">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54ab7-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54ab7-133">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="54ab7-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54ab7-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54ab7-134">Return value</span></span>

<span data-ttu-id="54ab7-135">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="54ab7-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="54ab7-136">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) bei der es sich um das Array handelt, das vom Bildschirmbereich in den Objektraum projiziert wird.</span><span class="sxs-lookup"><span data-stu-id="54ab7-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="54ab7-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54ab7-137">Remarks</span></span>

<span data-ttu-id="54ab7-138">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="54ab7-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="54ab7-139">Auf diese Weise kann die [**D3DXVec3Unproject-Funktion**](d3dxvec3unproject.md) als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54ab7-139">In this way, the [**D3DXVec3Unproject**](d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="54ab7-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54ab7-140">Requirements</span></span>



| <span data-ttu-id="54ab7-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54ab7-141">Requirement</span></span> | <span data-ttu-id="54ab7-142">Wert</span><span class="sxs-lookup"><span data-stu-id="54ab7-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54ab7-143">Header</span><span class="sxs-lookup"><span data-stu-id="54ab7-143">Header</span></span><br/>  | <dl> <span data-ttu-id="54ab7-144"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="54ab7-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="54ab7-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="54ab7-145">Library</span></span><br/> | <dl> <span data-ttu-id="54ab7-146"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="54ab7-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54ab7-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="54ab7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54ab7-148">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="54ab7-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="54ab7-149">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="54ab7-149">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 
