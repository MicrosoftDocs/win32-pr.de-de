---
description: Gibt die normalisierte Version eines 4D-Vektors zurück.
ms.assetid: e12d5dc7-b26f-41dd-b89d-1df9ba23077a
title: D3DXVec4Normalize-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 38d97f337711375d1d414eb78fb317672bc7c5cb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050949"
---
# <a name="d3dxvec4normalize-function-d3dx9mathh"></a><span data-ttu-id="412e6-103">D3DXVec4Normalize-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="412e6-103">D3DXVec4Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="412e6-104">Gibt die normalisierte Version eines 4D-Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="412e6-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="412e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="412e6-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="412e6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="412e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="412e6-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="412e6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="412e6-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="412e6-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="412e6-109">Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="412e6-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="412e6-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="412e6-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="412e6-111">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="412e6-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="412e6-112">Ein Zeiger auf die Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="412e6-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="412e6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="412e6-113">Return value</span></span>

<span data-ttu-id="412e6-114">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="412e6-114">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="412e6-115">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die die normalisierte Version des Vektors ist.</span><span class="sxs-lookup"><span data-stu-id="412e6-115">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="412e6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="412e6-116">Remarks</span></span>

<span data-ttu-id="412e6-117">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="412e6-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="412e6-118">Auf diese Weise kann die **D3DXVec4Normalize** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="412e6-118">In this way, the **D3DXVec4Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="412e6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="412e6-119">Requirements</span></span>



| <span data-ttu-id="412e6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="412e6-120">Requirement</span></span> | <span data-ttu-id="412e6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="412e6-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="412e6-122">Header</span><span class="sxs-lookup"><span data-stu-id="412e6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="412e6-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="412e6-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="412e6-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="412e6-124">Library</span></span><br/> | <dl> <span data-ttu-id="412e6-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="412e6-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="412e6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="412e6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="412e6-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="412e6-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




