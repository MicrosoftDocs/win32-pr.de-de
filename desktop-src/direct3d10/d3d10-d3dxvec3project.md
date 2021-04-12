---
description: Projiziert einen 3D-Vektor aus dem Objekt Raum in den Bildschirmbereich.
ms.assetid: 6fc59788-c3f7-4f47-a345-9108105e820e
title: D3DXVec3Project-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: c8d86949f754afb7639a0c28ff6d8b14c0e40ff0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354976"
---
# <a name="d3dxvec3project-function-d3dx10mathh"></a><span data-ttu-id="a4ad8-103">D3DXVec3Project-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a4ad8-103">D3DXVec3Project function (D3DX10Math.h)</span></span>

<span data-ttu-id="a4ad8-104">Projiziert einen 3D-Vektor aus dem Objekt Raum in den Bildschirmbereich.</span><span class="sxs-lookup"><span data-stu-id="a4ad8-104">Projects a 3D vector from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4ad8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4ad8-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a4ad8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4ad8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4ad8-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a4ad8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4ad8-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4ad8-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a4ad8-109">Zeiger auf das [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="a4ad8-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a4ad8-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4ad8-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4ad8-111">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a4ad8-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a4ad8-112">Ein Zeiger auf die Quell-D3DXVECTOR3-Struktur.</span><span class="sxs-lookup"><span data-stu-id="a4ad8-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="a4ad8-113">*pviewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4ad8-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4ad8-114">Typ: **Konstanten [**d3d10 \_ Viewport**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="a4ad8-114">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="a4ad8-115">Zeiger auf einen [**d3d10 \_ Viewport**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), der den Viewport darstellt.</span><span class="sxs-lookup"><span data-stu-id="a4ad8-115">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="a4ad8-116">*pprojection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4ad8-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4ad8-117">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a4ad8-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a4ad8-118">Zeiger auf eine [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die die Projektions Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="a4ad8-118">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a4ad8-119">*PView* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4ad8-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4ad8-120">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a4ad8-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a4ad8-121">Zeiger auf eine D3DXMATRIX-Struktur, die die Ansichts Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="a4ad8-121">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="a4ad8-122">*pworld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4ad8-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4ad8-123">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a4ad8-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a4ad8-124">Zeiger auf eine D3DXMATRIX-Struktur, die die Weltmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="a4ad8-124">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4ad8-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4ad8-125">Return value</span></span>

<span data-ttu-id="a4ad8-126">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4ad8-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a4ad8-127">Zeiger auf eine D3DXVECTOR3-Struktur, bei der es sich um den Vektor handelt, der vom Objekt Raum zum Bildschirmbereich projiziert</span><span class="sxs-lookup"><span data-stu-id="a4ad8-127">Pointer to a D3DXVECTOR3 structure that is the vector projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4ad8-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4ad8-128">Remarks</span></span>

<span data-ttu-id="a4ad8-129">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a4ad8-129">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a4ad8-130">Auf diese Weise kann die D3DXVec3Project-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4ad8-130">In this way, the D3DXVec3Project function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4ad8-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4ad8-131">Requirements</span></span>



| <span data-ttu-id="a4ad8-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4ad8-132">Requirement</span></span> | <span data-ttu-id="a4ad8-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a4ad8-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4ad8-134">Header</span><span class="sxs-lookup"><span data-stu-id="a4ad8-134">Header</span></span><br/> | <dl> <span data-ttu-id="a4ad8-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4ad8-135"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4ad8-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4ad8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4ad8-137">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a4ad8-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
