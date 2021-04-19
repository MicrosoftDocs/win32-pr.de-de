---
description: Addiert zwei 4D-Vektoren.
ms.assetid: da807dc0-6a31-4315-a32d-a42062c22199
title: D3DXVec4Add-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 62747cec15c4a9916dfb42572006cbb9fc908b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370459"
---
# <a name="d3dxvec4add-function"></a><span data-ttu-id="13562-103">D3DXVec4Add-Funktion</span><span class="sxs-lookup"><span data-stu-id="13562-103">D3DXVec4Add function</span></span>

<span data-ttu-id="13562-104">Addiert zwei 4D-Vektoren.</span><span class="sxs-lookup"><span data-stu-id="13562-104">Adds two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="13562-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13562-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Add(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="13562-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13562-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13562-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="13562-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="13562-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="13562-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="13562-109">Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="13562-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="13562-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13562-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13562-111">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="13562-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="13562-112">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="13562-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="13562-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13562-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13562-114">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="13562-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="13562-115">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="13562-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13562-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13562-116">Return value</span></span>

<span data-ttu-id="13562-117">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="13562-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="13562-118">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die die Summe der beiden Vektoren ist.</span><span class="sxs-lookup"><span data-stu-id="13562-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the sum of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="13562-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13562-119">Remarks</span></span>

<span data-ttu-id="13562-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13562-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="13562-121">Auf diese Weise kann die **D3DXVec4Add** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13562-121">In this way, the **D3DXVec4Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="13562-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13562-122">Requirements</span></span>



| <span data-ttu-id="13562-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13562-123">Requirement</span></span> | <span data-ttu-id="13562-124">Wert</span><span class="sxs-lookup"><span data-stu-id="13562-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13562-125">Header</span><span class="sxs-lookup"><span data-stu-id="13562-125">Header</span></span><br/>  | <dl> <span data-ttu-id="13562-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="13562-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="13562-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="13562-127">Library</span></span><br/> | <dl> <span data-ttu-id="13562-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13562-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="13562-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13562-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13562-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="13562-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="13562-131">**D3DXVec4Subtract**</span><span class="sxs-lookup"><span data-stu-id="13562-131">**D3DXVec4Subtract**</span></span>](d3dxvec4subtract.md)
</dt> <dt>

[<span data-ttu-id="13562-132">**D3DXVec4Scale**</span><span class="sxs-lookup"><span data-stu-id="13562-132">**D3DXVec4Scale**</span></span>](d3dxvec4scale.md)
</dt> </dl>

 

 




