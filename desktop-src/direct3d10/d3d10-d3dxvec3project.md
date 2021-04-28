---
description: 'D3DXVec3Project-Funktion (D3DX10Math.h): Projiziert einen 3D-Vektor aus dem Objektbereich in den Bildschirmraum.'
ms.assetid: 6fc59788-c3f7-4f47-a345-9108105e820e
title: D3DXVec3Project-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: f4a2cffa77b2a66267daf0a67a59698ae3e3b8eb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108168"
---
# <a name="d3dxvec3project-function-d3dx10mathh"></a><span data-ttu-id="ebe21-103">D3DXVec3Project-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="ebe21-103">D3DXVec3Project function (D3DX10Math.h)</span></span>

<span data-ttu-id="ebe21-104">Projiziert einen 3D-Vektor aus dem Objektbereich in den Bildschirmbereich.</span><span class="sxs-lookup"><span data-stu-id="ebe21-104">Projects a 3D vector from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe21-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebe21-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="ebe21-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebe21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebe21-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ebe21-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebe21-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ebe21-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ebe21-109">Zeiger auf [**D3DXVECTOR3,**](d3d10-d3dxvector3.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="ebe21-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ebe21-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ebe21-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebe21-111">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ebe21-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ebe21-112">Zeiger auf die D3DXVECTOR3-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="ebe21-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="ebe21-113">*pViewport* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ebe21-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebe21-114">Typ: **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="ebe21-114">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="ebe21-115">Zeiger auf einen [**D3D10 \_ VIEWPORT,**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)der den Viewport darstellt.</span><span class="sxs-lookup"><span data-stu-id="ebe21-115">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="ebe21-116">*pProjection* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ebe21-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebe21-117">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ebe21-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ebe21-118">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die die Projektionsmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="ebe21-118">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="ebe21-119">*pView* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ebe21-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebe21-120">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ebe21-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ebe21-121">Zeiger auf eine D3DXMATRIX-Struktur, die die Ansichtsmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="ebe21-121">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="ebe21-122">*pWorld* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ebe21-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebe21-123">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ebe21-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ebe21-124">Zeiger auf eine D3DXMATRIX-Struktur, die die Weltmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="ebe21-124">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebe21-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebe21-125">Return value</span></span>

<span data-ttu-id="ebe21-126">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ebe21-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ebe21-127">Zeiger auf eine D3DXVECTOR3-Struktur, bei der es sich um den Vektor handelt, der vom Objektbereich in den Bildschirmbereich projiziert wird.</span><span class="sxs-lookup"><span data-stu-id="ebe21-127">Pointer to a D3DXVECTOR3 structure that is the vector projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebe21-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebe21-128">Remarks</span></span>

<span data-ttu-id="ebe21-129">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ebe21-129">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ebe21-130">Auf diese Weise kann die D3DXVec3Project-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ebe21-130">In this way, the D3DXVec3Project function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe21-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebe21-131">Requirements</span></span>



| <span data-ttu-id="ebe21-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebe21-132">Requirement</span></span> | <span data-ttu-id="ebe21-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ebe21-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe21-134">Header</span><span class="sxs-lookup"><span data-stu-id="ebe21-134">Header</span></span><br/> | <dl> <span data-ttu-id="ebe21-135"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ebe21-135"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe21-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ebe21-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe21-137">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ebe21-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
