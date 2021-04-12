---
description: Gibt einen 4D-Vektor zurück, der aus den größten Komponenten von zwei 4D-Vektoren besteht.
ms.assetid: a08ceba0-938c-42af-8f32-b1fd8c12d926
title: D3DXVec4Maximize-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c145094deec5bdfdca123e6e494b18bbee01ce5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219723"
---
# <a name="d3dxvec4maximize-function"></a><span data-ttu-id="2aa6f-103">D3DXVec4Maximize-Funktion</span><span class="sxs-lookup"><span data-stu-id="2aa6f-103">D3DXVec4Maximize function</span></span>

<span data-ttu-id="2aa6f-104">Gibt einen 4D-Vektor zurück, der aus den größten Komponenten von zwei 4D-Vektoren besteht.</span><span class="sxs-lookup"><span data-stu-id="2aa6f-104">Returns a 4D vector that is made up of the largest components of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aa6f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2aa6f-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Maximize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="2aa6f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2aa6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aa6f-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2aa6f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa6f-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2aa6f-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2aa6f-109">Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="2aa6f-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2aa6f-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aa6f-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa6f-111">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2aa6f-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2aa6f-112">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2aa6f-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2aa6f-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aa6f-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa6f-114">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2aa6f-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2aa6f-115">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2aa6f-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aa6f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2aa6f-116">Return value</span></span>

<span data-ttu-id="2aa6f-117">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2aa6f-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2aa6f-118">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die aus den größten Komponenten der beiden Vektoren besteht.</span><span class="sxs-lookup"><span data-stu-id="2aa6f-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aa6f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2aa6f-119">Remarks</span></span>

<span data-ttu-id="2aa6f-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2aa6f-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2aa6f-121">Auf diese Weise kann die **D3DXVec4Maximize** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2aa6f-121">In this way, the **D3DXVec4Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2aa6f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2aa6f-122">Requirements</span></span>



| <span data-ttu-id="2aa6f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2aa6f-123">Requirement</span></span> | <span data-ttu-id="2aa6f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2aa6f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa6f-125">Header</span><span class="sxs-lookup"><span data-stu-id="2aa6f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2aa6f-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2aa6f-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2aa6f-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2aa6f-127">Library</span></span><br/> | <dl> <span data-ttu-id="2aa6f-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2aa6f-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2aa6f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2aa6f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aa6f-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2aa6f-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2aa6f-131">**D3DXVec4Minimize**</span><span class="sxs-lookup"><span data-stu-id="2aa6f-131">**D3DXVec4Minimize**</span></span>](d3dxvec4minimize.md)
</dt> </dl>

 

 




