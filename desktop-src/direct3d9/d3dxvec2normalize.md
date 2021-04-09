---
description: Gibt die normalisierte Version eines 2D-Vektors zurück.
ms.assetid: 2796a5d1-cb1c-4093-87f2-a2ad43279d91
title: D3DXVec2Normalize-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce3152c622c9083438d35c73b20e05ca2523efc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050849"
---
# <a name="d3dxvec2normalize-function-d3dx9mathh"></a><span data-ttu-id="e55a3-103">D3DXVec2Normalize-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e55a3-103">D3DXVec2Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="e55a3-104">Gibt die normalisierte Version eines 2D-Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="e55a3-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="e55a3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e55a3-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="e55a3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e55a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e55a3-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e55a3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e55a3-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="e55a3-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e55a3-109">Ein Zeiger auf die [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="e55a3-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e55a3-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e55a3-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e55a3-111">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="e55a3-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e55a3-112">Ein Zeiger auf die Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e55a3-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e55a3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e55a3-113">Return value</span></span>

<span data-ttu-id="e55a3-114">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="e55a3-114">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e55a3-115">Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die die normalisierte Version des Vektors ist.</span><span class="sxs-lookup"><span data-stu-id="e55a3-115">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="e55a3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e55a3-116">Remarks</span></span>

<span data-ttu-id="e55a3-117">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e55a3-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e55a3-118">Auf diese Weise kann die **D3DXVec2Normalize** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e55a3-118">In this way, the **D3DXVec2Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e55a3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e55a3-119">Requirements</span></span>



| <span data-ttu-id="e55a3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e55a3-120">Requirement</span></span> | <span data-ttu-id="e55a3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e55a3-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e55a3-122">Header</span><span class="sxs-lookup"><span data-stu-id="e55a3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e55a3-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e55a3-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e55a3-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e55a3-124">Library</span></span><br/> | <dl> <span data-ttu-id="e55a3-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e55a3-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e55a3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e55a3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e55a3-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="e55a3-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




