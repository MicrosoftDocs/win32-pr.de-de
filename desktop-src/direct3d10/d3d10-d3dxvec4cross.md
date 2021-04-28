---
description: 'D3DXVec4Cross-Funktion (D3DX10Math.h): Bestimmt das Kreuzprodukt in vier Dimensionen.'
ms.assetid: 4f728fbd-cf5a-4d2e-ba4f-487616d83f6d
title: D3DXVec4Cross-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: e52cc1adb1e48f65599b1bf7179f7953823f1e1c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102948"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a><span data-ttu-id="a4c51-103">D3DXVec4Cross-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="a4c51-103">D3DXVec4Cross function (D3DX10Math.h)</span></span>

<span data-ttu-id="a4c51-104">Bestimmt das Kreuzprodukt in vier Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="a4c51-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c51-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4c51-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="a4c51-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4c51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4c51-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a4c51-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c51-108">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4c51-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a4c51-109">Zeiger auf [**D3DXVECTOR4,**](d3d10-d3dxvector4.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="a4c51-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a4c51-110">*pV1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a4c51-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c51-111">Typ: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a4c51-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a4c51-112">Zeiger auf eine D3DXVECTOR4-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="a4c51-112">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="a4c51-113">*pV2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a4c51-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c51-114">Typ: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a4c51-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a4c51-115">Zeiger auf eine D3DXVECTOR4-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="a4c51-115">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="a4c51-116">*pV3* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a4c51-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c51-117">Typ: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a4c51-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a4c51-118">Zeiger auf eine D3DXVECTOR4-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="a4c51-118">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4c51-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4c51-119">Return value</span></span>

<span data-ttu-id="a4c51-120">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4c51-120">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a4c51-121">Zeiger auf eine D3DXVECTOR4-Struktur, die das Kreuzprodukt ist.</span><span class="sxs-lookup"><span data-stu-id="a4c51-121">Pointer to a D3DXVECTOR4 structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4c51-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4c51-122">Remarks</span></span>

<span data-ttu-id="a4c51-123">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a4c51-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a4c51-124">Auf diese Weise kann die D3DXVec4Cross-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4c51-124">In this way, the D3DXVec4Cross function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4c51-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4c51-125">Requirements</span></span>



| <span data-ttu-id="a4c51-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4c51-126">Requirement</span></span> | <span data-ttu-id="a4c51-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a4c51-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c51-128">Header</span><span class="sxs-lookup"><span data-stu-id="a4c51-128">Header</span></span><br/> | <dl> <span data-ttu-id="a4c51-129"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a4c51-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4c51-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a4c51-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c51-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a4c51-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
