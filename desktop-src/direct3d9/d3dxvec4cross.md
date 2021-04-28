---
description: 'D3DXVec4Cross-Funktion (D3dx9math.h): Bestimmt das Kreuzprodukt in vier Dimensionen.'
ms.assetid: 10b965c9-7ed7-450c-86a0-114f068c888f
title: D3DXVec4Cross-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3630a486f6c8fcd456373445bd931d878fdc38e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097688"
---
# <a name="d3dxvec4cross-function-d3dx9mathh"></a><span data-ttu-id="06c7f-103">D3DXVec4Cross-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="06c7f-103">D3DXVec4Cross function (D3dx9math.h)</span></span>

<span data-ttu-id="06c7f-104">Bestimmt das Kreuzprodukt in vier Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="06c7f-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c7f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06c7f-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="06c7f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06c7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c7f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="06c7f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="06c7f-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="06c7f-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="06c7f-109">Zeiger auf die [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="06c7f-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="06c7f-110">*pV1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="06c7f-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c7f-111">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="06c7f-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="06c7f-112">Zeiger auf eine [**D3DXVECTOR4-Quellstruktur.**](d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="06c7f-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="06c7f-113">*pV2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="06c7f-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c7f-114">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="06c7f-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="06c7f-115">Zeiger auf eine [**D3DXVECTOR4-Quellstruktur.**](d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="06c7f-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="06c7f-116">*pV3* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="06c7f-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c7f-117">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="06c7f-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="06c7f-118">Zeiger auf eine [**D3DXVECTOR4-Quellstruktur.**](d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="06c7f-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c7f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06c7f-119">Return value</span></span>

<span data-ttu-id="06c7f-120">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="06c7f-120">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="06c7f-121">Zeiger auf eine [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Kreuzprodukt ist.</span><span class="sxs-lookup"><span data-stu-id="06c7f-121">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="06c7f-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06c7f-122">Remarks</span></span>

<span data-ttu-id="06c7f-123">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="06c7f-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="06c7f-124">Auf diese Weise kann die **D3DXVec4Cross-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06c7f-124">In this way, the **D3DXVec4Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c7f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06c7f-125">Requirements</span></span>



| <span data-ttu-id="06c7f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06c7f-126">Requirement</span></span> | <span data-ttu-id="06c7f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="06c7f-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06c7f-128">Header</span><span class="sxs-lookup"><span data-stu-id="06c7f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="06c7f-129"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="06c7f-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="06c7f-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="06c7f-130">Library</span></span><br/> | <dl> <span data-ttu-id="06c7f-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="06c7f-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06c7f-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="06c7f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c7f-133">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="06c7f-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="06c7f-134">**D3DXVec4Dot**</span><span class="sxs-lookup"><span data-stu-id="06c7f-134">**D3DXVec4Dot**</span></span>](d3dxvec4dot.md)
</dt> </dl>

 

 




