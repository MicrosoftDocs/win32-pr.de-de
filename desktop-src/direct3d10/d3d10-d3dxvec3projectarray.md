---
description: Projiziert ein Array (x, y, z, 0) aus dem Objekt Raum in den Bildschirmbereich.
ms.assetid: 33f0f65a-c027-4a31-83a7-f5f6b2a2f72f
title: D3DXVec3ProjectArray-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: bdbda9201d23a6c525dc054c53874c71d548e65e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355386"
---
# <a name="d3dxvec3projectarray-function-d3dx10mathh"></a><span data-ttu-id="99e0b-103">D3DXVec3ProjectArray-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="99e0b-103">D3DXVec3ProjectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="99e0b-104">Projiziert ein Array (x, y, z, 0) aus dem Objekt Raum in den Bildschirmbereich.</span><span class="sxs-lookup"><span data-stu-id="99e0b-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e0b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99e0b-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
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



## <a name="parameters"></a><span data-ttu-id="99e0b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99e0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99e0b-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="99e0b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99e0b-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="99e0b-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="99e0b-109">Zeiger auf das [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="99e0b-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="99e0b-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99e0b-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e0b-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99e0b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99e0b-112">Schritt zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="99e0b-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="99e0b-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99e0b-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e0b-114">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="99e0b-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="99e0b-115">Ein Zeiger auf die Quell-D3DXVECTOR3-Struktur.</span><span class="sxs-lookup"><span data-stu-id="99e0b-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="99e0b-116">*Vstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99e0b-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e0b-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99e0b-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99e0b-118">Schritt zwischen Vektoren im Eingabedaten Strom.</span><span class="sxs-lookup"><span data-stu-id="99e0b-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="99e0b-119">*pviewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99e0b-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e0b-120">Typ: **Konstanten [**d3d10 \_ Viewport**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="99e0b-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="99e0b-121">Zeiger auf einen [**d3d10 \_ Viewport**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), der den Viewport darstellt.</span><span class="sxs-lookup"><span data-stu-id="99e0b-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="99e0b-122">*pprojection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99e0b-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e0b-123">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="99e0b-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="99e0b-124">Zeiger auf eine [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die die Projektions Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="99e0b-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="99e0b-125">*PView* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99e0b-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e0b-126">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="99e0b-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="99e0b-127">Zeiger auf eine D3DXMATRIX-Struktur, die die Ansichts Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="99e0b-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="99e0b-128">*pworld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99e0b-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e0b-129">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="99e0b-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="99e0b-130">Zeiger auf eine D3DXMATRIX-Struktur, die die Weltmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="99e0b-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="99e0b-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99e0b-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e0b-132">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99e0b-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99e0b-133">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="99e0b-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99e0b-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99e0b-134">Return value</span></span>

<span data-ttu-id="99e0b-135">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="99e0b-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="99e0b-136">Zeiger auf eine D3DXVECTOR3-Struktur, bei der es sich um das Array handelt, das vom Objekt Raum auf den Bildschirmbereich</span><span class="sxs-lookup"><span data-stu-id="99e0b-136">Pointer to a D3DXVECTOR3 structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="99e0b-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99e0b-137">Remarks</span></span>

<span data-ttu-id="99e0b-138">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="99e0b-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="99e0b-139">Auf diese Weise kann die D3DXVec3ProjectArray-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99e0b-139">In this way, the D3DXVec3ProjectArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="99e0b-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99e0b-140">Requirements</span></span>



| <span data-ttu-id="99e0b-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99e0b-141">Requirement</span></span> | <span data-ttu-id="99e0b-142">Wert</span><span class="sxs-lookup"><span data-stu-id="99e0b-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99e0b-143">Header</span><span class="sxs-lookup"><span data-stu-id="99e0b-143">Header</span></span><br/> | <dl> <span data-ttu-id="99e0b-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="99e0b-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99e0b-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99e0b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99e0b-146">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="99e0b-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
