---
description: 'D3DXVec3UnprojectArray-Funktion (D3DX10Math.h): Projiziert ein Array (x, y, z, 0) aus dem Bildschirmbereich in den Objektbereich.'
ms.assetid: 02db5b32-7fa3-4cde-bd63-0d8b3dfc31e7
title: D3DXVec3UnprojectArray-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 727744445e952fa0135feff944c768aaba1aba36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103008"
---
# <a name="d3dxvec3unprojectarray-function-d3dx10mathh"></a><span data-ttu-id="d6df2-103">D3DXVec3UnprojectArray-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="d6df2-103">D3DXVec3UnprojectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="d6df2-104">Projiziert ein Array (x, y, z, 0) aus dem Bildschirmbereich in den Objektbereich.</span><span class="sxs-lookup"><span data-stu-id="d6df2-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6df2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6df2-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_          UINT           OutStride,
  _In_    const D3DXVECTOR3    *pV,
  _In_          UINT           VStride,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld,
  _In_          UINT           n
);
```



## <a name="parameters"></a><span data-ttu-id="d6df2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6df2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6df2-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d6df2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6df2-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6df2-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6df2-109">Zeiger auf [**D3DXVECTOR3,**](d3d10-d3dxvector3.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="d6df2-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d6df2-110">*OutStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d6df2-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6df2-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6df2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6df2-112">Schreitet zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="d6df2-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d6df2-113">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d6df2-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6df2-114">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6df2-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6df2-115">Zeiger auf die D3DXVECTOR3-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="d6df2-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6df2-116">*VStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d6df2-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6df2-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6df2-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6df2-118">Schreitet zwischen Vektoren im Eingabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="d6df2-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d6df2-119">*pViewport* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d6df2-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6df2-120">Typ: **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="d6df2-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="d6df2-121">Zeiger auf einen [**D3D10 \_ VIEWPORT,**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)der den Viewport darstellt.</span><span class="sxs-lookup"><span data-stu-id="d6df2-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="d6df2-122">*pProjection* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d6df2-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6df2-123">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6df2-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d6df2-124">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die die Projektionsmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="d6df2-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="d6df2-125">*pView* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d6df2-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6df2-126">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6df2-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d6df2-127">Zeiger auf eine D3DXMATRIX-Struktur, die die Ansichtsmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="d6df2-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="d6df2-128">*pWorld* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d6df2-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6df2-129">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6df2-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d6df2-130">Zeiger auf eine D3DXMATRIX-Struktur, die die Weltmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="d6df2-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="d6df2-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6df2-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6df2-132">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6df2-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6df2-133">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="d6df2-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6df2-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6df2-134">Return value</span></span>

<span data-ttu-id="d6df2-135">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6df2-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6df2-136">Zeiger auf eine D3DXVECTOR3-Struktur, bei der es sich um das Array handelt, das vom Bildschirmbereich in den Objektbereich projiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d6df2-136">Pointer to a D3DXVECTOR3 structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6df2-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6df2-137">Remarks</span></span>

<span data-ttu-id="d6df2-138">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d6df2-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d6df2-139">Auf diese Weise kann die [**D3DXVec3Unproject-Funktion**](d3d10-d3dxvec3unproject.md) als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6df2-139">In this way, the [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6df2-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6df2-140">Requirements</span></span>



| <span data-ttu-id="d6df2-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6df2-141">Requirement</span></span> | <span data-ttu-id="d6df2-142">Wert</span><span class="sxs-lookup"><span data-stu-id="d6df2-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6df2-143">Header</span><span class="sxs-lookup"><span data-stu-id="d6df2-143">Header</span></span><br/> | <dl> <span data-ttu-id="d6df2-144"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d6df2-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6df2-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d6df2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6df2-146">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="d6df2-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
