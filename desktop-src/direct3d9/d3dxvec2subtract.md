---
description: Subtrahiert zwei 2D-Vektoren.
ms.assetid: e5a693e9-b143-41d5-923d-3f3f71461a42
title: D3DXVec2Subtract-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c12f41da7594f3eff9743eed7a1b0780f36c5fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530884"
---
# <a name="d3dxvec2subtract-function"></a><span data-ttu-id="3f41b-103">D3DXVec2Subtract-Funktion</span><span class="sxs-lookup"><span data-stu-id="3f41b-103">D3DXVec2Subtract function</span></span>

<span data-ttu-id="3f41b-104">Subtrahiert zwei 2D-Vektoren.</span><span class="sxs-lookup"><span data-stu-id="3f41b-104">Subtracts two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f41b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f41b-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Subtract(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="3f41b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f41b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f41b-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3f41b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f41b-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f41b-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="3f41b-109">Ein Zeiger auf die [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="3f41b-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3f41b-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f41b-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f41b-111">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="3f41b-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="3f41b-112">Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3f41b-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3f41b-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f41b-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f41b-114">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="3f41b-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="3f41b-115">Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3f41b-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f41b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f41b-116">Return value</span></span>

<span data-ttu-id="3f41b-117">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f41b-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="3f41b-118">Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die die Differenz zweier Vektoren ist.</span><span class="sxs-lookup"><span data-stu-id="3f41b-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the difference of two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f41b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f41b-119">Remarks</span></span>

<span data-ttu-id="3f41b-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f41b-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="3f41b-121">Auf diese Weise kann die **D3DXVec2Subtract** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f41b-121">In this way, the **D3DXVec2Subtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f41b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f41b-122">Requirements</span></span>



| <span data-ttu-id="3f41b-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f41b-123">Requirement</span></span> | <span data-ttu-id="3f41b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="3f41b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f41b-125">Header</span><span class="sxs-lookup"><span data-stu-id="3f41b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3f41b-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f41b-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3f41b-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3f41b-127">Library</span></span><br/> | <dl> <span data-ttu-id="3f41b-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f41b-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3f41b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f41b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f41b-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="3f41b-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3f41b-131">**D3DXVec2Add**</span><span class="sxs-lookup"><span data-stu-id="3f41b-131">**D3DXVec2Add**</span></span>](d3dxvec2add.md)
</dt> <dt>

[<span data-ttu-id="3f41b-132">**D3DXVec2Scale**</span><span class="sxs-lookup"><span data-stu-id="3f41b-132">**D3DXVec2Scale**</span></span>](d3dxvec2scale.md)
</dt> </dl>

 

 




