---
description: Fügt zwei 2D-Vektoren hinzu.
ms.assetid: 82b2fdf6-1b1f-4768-8c0b-ac8faa77d7ed
title: D3DXVec2Add-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5087177448b01763bd94acb9b50c27c6cdf38815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961582"
---
# <a name="d3dxvec2add-function"></a><span data-ttu-id="5adc3-103">D3DXVec2Add-Funktion</span><span class="sxs-lookup"><span data-stu-id="5adc3-103">D3DXVec2Add function</span></span>

<span data-ttu-id="5adc3-104">Fügt zwei 2D-Vektoren hinzu.</span><span class="sxs-lookup"><span data-stu-id="5adc3-104">Adds two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="5adc3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5adc3-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Add(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="5adc3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5adc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5adc3-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5adc3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5adc3-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="5adc3-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5adc3-109">Ein Zeiger auf die [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="5adc3-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5adc3-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5adc3-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5adc3-111">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="5adc3-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5adc3-112">Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5adc3-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5adc3-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5adc3-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5adc3-114">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="5adc3-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5adc3-115">Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5adc3-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5adc3-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5adc3-116">Return value</span></span>

<span data-ttu-id="5adc3-117">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="5adc3-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5adc3-118">Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die die Summe der beiden Vektoren ist.</span><span class="sxs-lookup"><span data-stu-id="5adc3-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the sum of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="5adc3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5adc3-119">Remarks</span></span>

<span data-ttu-id="5adc3-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5adc3-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5adc3-121">Auf diese Weise kann die **D3DXVec2Add** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5adc3-121">In this way, the **D3DXVec2Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5adc3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5adc3-122">Requirements</span></span>



| <span data-ttu-id="5adc3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5adc3-123">Requirement</span></span> | <span data-ttu-id="5adc3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5adc3-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5adc3-125">Header</span><span class="sxs-lookup"><span data-stu-id="5adc3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5adc3-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5adc3-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5adc3-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5adc3-127">Library</span></span><br/> | <dl> <span data-ttu-id="5adc3-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5adc3-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5adc3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5adc3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5adc3-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5adc3-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5adc3-131">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="5adc3-131">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
</dt> <dt>

[<span data-ttu-id="5adc3-132">**D3DXVec2Scale**</span><span class="sxs-lookup"><span data-stu-id="5adc3-132">**D3DXVec2Scale**</span></span>](d3dxvec2scale.md)
</dt> </dl>

 

 




