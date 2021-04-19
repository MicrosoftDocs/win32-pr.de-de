---
description: Gibt einen 2D-Vektor zurück, der aus den kleinsten Komponenten zweier 2D-Vektoren besteht.
ms.assetid: 6944523e-33dd-456e-9cc2-17760d76c548
title: D3DXVec2Minimize-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1914ae9317d686e369f1cb2c7eb36ab54a29845f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355172"
---
# <a name="d3dxvec2minimize-function"></a><span data-ttu-id="e4e6e-103">D3DXVec2Minimize-Funktion</span><span class="sxs-lookup"><span data-stu-id="e4e6e-103">D3DXVec2Minimize function</span></span>

<span data-ttu-id="e4e6e-104">Gibt einen 2D-Vektor zurück, der aus den kleinsten Komponenten zweier 2D-Vektoren besteht.</span><span class="sxs-lookup"><span data-stu-id="e4e6e-104">Returns a 2D vector that is made up of the smallest components of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4e6e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4e6e-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Minimize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="e4e6e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4e6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4e6e-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e4e6e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e6e-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4e6e-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e4e6e-109">Ein Zeiger auf die [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="e4e6e-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e4e6e-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4e6e-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e6e-111">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4e6e-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e4e6e-112">Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e4e6e-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e4e6e-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4e6e-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e6e-114">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4e6e-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e4e6e-115">Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e4e6e-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4e6e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4e6e-116">Return value</span></span>

<span data-ttu-id="e4e6e-117">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4e6e-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e4e6e-118">Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die aus den kleinsten Komponenten der beiden Vektoren besteht.</span><span class="sxs-lookup"><span data-stu-id="e4e6e-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is made up of the smallest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4e6e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4e6e-119">Remarks</span></span>

<span data-ttu-id="e4e6e-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e4e6e-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e4e6e-121">Auf diese Weise kann die **D3DXVec2Minimize** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4e6e-121">In this way, the **D3DXVec2Minimize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e6e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4e6e-122">Requirements</span></span>



| <span data-ttu-id="e4e6e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4e6e-123">Requirement</span></span> | <span data-ttu-id="e4e6e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e4e6e-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e6e-125">Header</span><span class="sxs-lookup"><span data-stu-id="e4e6e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e4e6e-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4e6e-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e4e6e-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4e6e-127">Library</span></span><br/> | <dl> <span data-ttu-id="e4e6e-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4e6e-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4e6e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4e6e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4e6e-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="e4e6e-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e4e6e-131">**D3DXVec2Maximize**</span><span class="sxs-lookup"><span data-stu-id="e4e6e-131">**D3DXVec2Maximize**</span></span>](d3dxvec2maximize.md)
</dt> </dl>

 

 




