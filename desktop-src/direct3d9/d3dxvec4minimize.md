---
description: Gibt einen 4D-Vektor zurück, der aus den kleinsten Komponenten von zwei 4D-Vektoren besteht.
ms.assetid: ae3819a3-a5b6-47c2-b789-3e3f07db9f03
title: D3DXVec4Minimize-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ccd4806bfa368fafa481500d3bd28e0ff55b7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361871"
---
# <a name="d3dxvec4minimize-function"></a><span data-ttu-id="3251c-103">D3DXVec4Minimize-Funktion</span><span class="sxs-lookup"><span data-stu-id="3251c-103">D3DXVec4Minimize function</span></span>

<span data-ttu-id="3251c-104">Gibt einen 4D-Vektor zurück, der aus den kleinsten Komponenten von zwei 4D-Vektoren besteht.</span><span class="sxs-lookup"><span data-stu-id="3251c-104">Returns a 4D vector that is made up of the smallest components of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="3251c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3251c-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Minimize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="3251c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3251c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3251c-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3251c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3251c-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3251c-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3251c-109">Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="3251c-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3251c-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3251c-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3251c-111">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="3251c-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3251c-112">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3251c-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3251c-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3251c-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3251c-114">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="3251c-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3251c-115">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3251c-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3251c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3251c-116">Return value</span></span>

<span data-ttu-id="3251c-117">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3251c-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="3251c-118">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die aus den kleinsten Komponenten der beiden Vektoren besteht.</span><span class="sxs-lookup"><span data-stu-id="3251c-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is made up of the smallest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="3251c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3251c-119">Remarks</span></span>

<span data-ttu-id="3251c-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3251c-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="3251c-121">Auf diese Weise kann die **D3DXVec4Minimize** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3251c-121">In this way, the **D3DXVec4Minimize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3251c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3251c-122">Requirements</span></span>



| <span data-ttu-id="3251c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3251c-123">Requirement</span></span> | <span data-ttu-id="3251c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="3251c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3251c-125">Header</span><span class="sxs-lookup"><span data-stu-id="3251c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3251c-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3251c-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3251c-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3251c-127">Library</span></span><br/> | <dl> <span data-ttu-id="3251c-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3251c-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3251c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3251c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3251c-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="3251c-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3251c-131">**D3DXVec4Maximize**</span><span class="sxs-lookup"><span data-stu-id="3251c-131">**D3DXVec4Maximize**</span></span>](d3dxvec4maximize.md)
</dt> </dl>

 

 




