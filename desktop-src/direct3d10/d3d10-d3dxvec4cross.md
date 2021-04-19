---
description: Bestimmt das Kreuz Produkt in vier Dimensionen.
ms.assetid: 4f728fbd-cf5a-4d2e-ba4f-487616d83f6d
title: D3DXVec4Cross-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 8e3e2a612740a207ea4dc44243ce24ebbab7fc08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363163"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a><span data-ttu-id="3d4ff-103">D3DXVec4Cross-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="3d4ff-103">D3DXVec4Cross function (D3DX10Math.h)</span></span>

<span data-ttu-id="3d4ff-104">Bestimmt das Kreuz Produkt in vier Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="3d4ff-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d4ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d4ff-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="3d4ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d4ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d4ff-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3d4ff-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d4ff-108">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d4ff-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="3d4ff-109">Zeiger auf das [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="3d4ff-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3d4ff-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d4ff-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d4ff-111">Typ: **Konstanten [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d4ff-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="3d4ff-112">Zeiger auf eine Quell-D3DXVECTOR4-Struktur.</span><span class="sxs-lookup"><span data-stu-id="3d4ff-112">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="3d4ff-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d4ff-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d4ff-114">Typ: **Konstanten [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d4ff-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="3d4ff-115">Zeiger auf eine Quell-D3DXVECTOR4-Struktur.</span><span class="sxs-lookup"><span data-stu-id="3d4ff-115">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="3d4ff-116">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d4ff-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d4ff-117">Typ: **Konstanten [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d4ff-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="3d4ff-118">Zeiger auf eine Quell-D3DXVECTOR4-Struktur.</span><span class="sxs-lookup"><span data-stu-id="3d4ff-118">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d4ff-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d4ff-119">Return value</span></span>

<span data-ttu-id="3d4ff-120">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d4ff-120">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="3d4ff-121">Zeiger auf eine D3DXVECTOR4-Struktur, die das Kreuz Produkt ist.</span><span class="sxs-lookup"><span data-stu-id="3d4ff-121">Pointer to a D3DXVECTOR4 structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d4ff-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d4ff-122">Remarks</span></span>

<span data-ttu-id="3d4ff-123">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3d4ff-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="3d4ff-124">Auf diese Weise kann die D3DXVec4Cross-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d4ff-124">In this way, the D3DXVec4Cross function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d4ff-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d4ff-125">Requirements</span></span>



| <span data-ttu-id="3d4ff-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d4ff-126">Requirement</span></span> | <span data-ttu-id="3d4ff-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3d4ff-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d4ff-128">Header</span><span class="sxs-lookup"><span data-stu-id="3d4ff-128">Header</span></span><br/> | <dl> <span data-ttu-id="3d4ff-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d4ff-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d4ff-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d4ff-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d4ff-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="3d4ff-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
