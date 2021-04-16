---
description: Gibt einen 2D-Vektor zurück, der aus den größten Komponenten zweier 2D-Vektoren besteht.
ms.assetid: 5eb5141b-d611-4c6b-a3e3-c7ad8f223657
title: D3DXVec2Maximize-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffd5fbc98e653a6bbaffa7d3cec16b13695365b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394113"
---
# <a name="d3dxvec2maximize-function"></a><span data-ttu-id="70edc-103">D3DXVec2Maximize-Funktion</span><span class="sxs-lookup"><span data-stu-id="70edc-103">D3DXVec2Maximize function</span></span>

<span data-ttu-id="70edc-104">Gibt einen 2D-Vektor zurück, der aus den größten Komponenten zweier 2D-Vektoren besteht.</span><span class="sxs-lookup"><span data-stu-id="70edc-104">Returns a 2D vector that is made up of the largest components of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="70edc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="70edc-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Maximize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="70edc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="70edc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70edc-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="70edc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="70edc-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="70edc-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="70edc-109">Ein Zeiger auf die [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="70edc-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="70edc-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70edc-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70edc-111">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="70edc-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="70edc-112">Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="70edc-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="70edc-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70edc-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70edc-114">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="70edc-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="70edc-115">Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="70edc-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70edc-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70edc-116">Return value</span></span>

<span data-ttu-id="70edc-117">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="70edc-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="70edc-118">Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die aus den größten Komponenten der beiden Vektoren besteht.</span><span class="sxs-lookup"><span data-stu-id="70edc-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="70edc-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70edc-119">Remarks</span></span>

<span data-ttu-id="70edc-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="70edc-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="70edc-121">Auf diese Weise kann die **D3DXVec2Maximize** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70edc-121">In this way, the **D3DXVec2Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="70edc-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70edc-122">Requirements</span></span>



| <span data-ttu-id="70edc-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70edc-123">Requirement</span></span> | <span data-ttu-id="70edc-124">Wert</span><span class="sxs-lookup"><span data-stu-id="70edc-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70edc-125">Header</span><span class="sxs-lookup"><span data-stu-id="70edc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="70edc-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="70edc-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="70edc-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="70edc-127">Library</span></span><br/> | <dl> <span data-ttu-id="70edc-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70edc-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70edc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70edc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70edc-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="70edc-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="70edc-131">**D3DXVec2Minimize**</span><span class="sxs-lookup"><span data-stu-id="70edc-131">**D3DXVec2Minimize**</span></span>](d3dxvec2minimize.md)
</dt> </dl>

 

 




