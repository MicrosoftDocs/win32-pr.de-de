---
description: Bestimmt das Kreuz Produkt in vier Dimensionen.
ms.assetid: 10b965c9-7ed7-450c-86a0-114f068c888f
title: D3DXVec4Cross-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 91e6e5662bff503ba96d96f135f98e60cf15c8fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219552"
---
# <a name="d3dxvec4cross-function-d3dx9mathh"></a><span data-ttu-id="fb2ef-103">D3DXVec4Cross-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fb2ef-103">D3DXVec4Cross function (D3dx9math.h)</span></span>

<span data-ttu-id="fb2ef-104">Bestimmt das Kreuz Produkt in vier Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="fb2ef-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb2ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb2ef-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="fb2ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb2ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb2ef-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fb2ef-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb2ef-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb2ef-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fb2ef-109">Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="fb2ef-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fb2ef-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb2ef-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb2ef-111">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="fb2ef-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fb2ef-112">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="fb2ef-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fb2ef-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb2ef-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb2ef-114">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="fb2ef-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fb2ef-115">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="fb2ef-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fb2ef-116">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb2ef-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb2ef-117">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="fb2ef-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fb2ef-118">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="fb2ef-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb2ef-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb2ef-119">Return value</span></span>

<span data-ttu-id="fb2ef-120">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb2ef-120">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fb2ef-121">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Kreuz Produkt ist.</span><span class="sxs-lookup"><span data-stu-id="fb2ef-121">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb2ef-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb2ef-122">Remarks</span></span>

<span data-ttu-id="fb2ef-123">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fb2ef-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fb2ef-124">Auf diese Weise kann die **D3DXVec4Cross** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb2ef-124">In this way, the **D3DXVec4Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb2ef-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb2ef-125">Requirements</span></span>



| <span data-ttu-id="fb2ef-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb2ef-126">Requirement</span></span> | <span data-ttu-id="fb2ef-127">Wert</span><span class="sxs-lookup"><span data-stu-id="fb2ef-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb2ef-128">Header</span><span class="sxs-lookup"><span data-stu-id="fb2ef-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fb2ef-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ef-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fb2ef-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb2ef-130">Library</span></span><br/> | <dl> <span data-ttu-id="fb2ef-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb2ef-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb2ef-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb2ef-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb2ef-133">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="fb2ef-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fb2ef-134">**D3DXVec4Dot**</span><span class="sxs-lookup"><span data-stu-id="fb2ef-134">**D3DXVec4Dot**</span></span>](d3dxvec4dot.md)
</dt> </dl>

 

 




