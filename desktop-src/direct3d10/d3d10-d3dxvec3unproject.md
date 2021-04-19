---
description: Projiziert einen Vektor aus dem Bildschirmbereich in den Objektbereich.
ms.assetid: c96d732d-0594-42b4-bc54-458a313f153e
title: D3DXVec3Unproject-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 21916392c689bcac794d44ec2c42c3e0b39abb0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366657"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a><span data-ttu-id="81058-103">D3DXVec3Unproject-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="81058-103">D3DXVec3Unproject function (D3DX10Math.h)</span></span>

<span data-ttu-id="81058-104">Projiziert einen Vektor aus dem Bildschirmbereich in den Objektbereich.</span><span class="sxs-lookup"><span data-stu-id="81058-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="81058-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="81058-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="81058-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="81058-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81058-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="81058-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="81058-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="81058-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="81058-109">Zeiger auf das [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="81058-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="81058-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81058-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81058-111">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="81058-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="81058-112">Ein Zeiger auf die Quell-D3DXVECTOR3-Struktur.</span><span class="sxs-lookup"><span data-stu-id="81058-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="81058-113">*pviewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81058-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81058-114">Typ: **Konstanten [**d3d10 \_ Viewport**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="81058-114">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="81058-115">Zeiger auf einen [**d3d10 \_ Viewport**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), der den Viewport darstellt.</span><span class="sxs-lookup"><span data-stu-id="81058-115">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="81058-116">*pprojection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81058-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81058-117">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="81058-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="81058-118">Zeiger auf eine [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die die Projektions Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="81058-118">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="81058-119">*PView* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81058-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81058-120">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="81058-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="81058-121">Zeiger auf eine D3DXMATRIX-Struktur, die die Ansichts Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="81058-121">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="81058-122">*pworld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81058-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81058-123">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="81058-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="81058-124">Zeiger auf eine D3DXMATRIX-Struktur, die die Weltmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="81058-124">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81058-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81058-125">Return value</span></span>

<span data-ttu-id="81058-126">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="81058-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="81058-127">Zeiger auf eine D3DXVECTOR3-Struktur, bei der es sich um den Vektor handelt, der vom Bildschirmbereich zum Objekt Raum projiziert</span><span class="sxs-lookup"><span data-stu-id="81058-127">Pointer to a D3DXVECTOR3 structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="81058-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81058-128">Remarks</span></span>

<span data-ttu-id="81058-129">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="81058-129">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="81058-130">Auf diese Weise kann die D3DXVec3Unproject-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81058-130">In this way, the D3DXVec3Unproject function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="81058-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81058-131">Requirements</span></span>



| <span data-ttu-id="81058-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81058-132">Requirement</span></span> | <span data-ttu-id="81058-133">Wert</span><span class="sxs-lookup"><span data-stu-id="81058-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81058-134">Header</span><span class="sxs-lookup"><span data-stu-id="81058-134">Header</span></span><br/> | <dl> <span data-ttu-id="81058-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="81058-135"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81058-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81058-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81058-137">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="81058-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
