---
description: Subtrahiert zwei 4D-Vektoren.
ms.assetid: 3bc55b38-818e-40eb-859e-495ee28fc4ae
title: D3DXVec4Subtract-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1110930d8e37cf04f7de5129c2a72db4ecc4ac8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356136"
---
# <a name="d3dxvec4subtract-function"></a><span data-ttu-id="5b80d-103">D3DXVec4Subtract-Funktion</span><span class="sxs-lookup"><span data-stu-id="5b80d-103">D3DXVec4Subtract function</span></span>

<span data-ttu-id="5b80d-104">Subtrahiert zwei 4D-Vektoren.</span><span class="sxs-lookup"><span data-stu-id="5b80d-104">Subtracts two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b80d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b80d-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Subtract(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="5b80d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b80d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b80d-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5b80d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b80d-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="5b80d-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="5b80d-109">Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="5b80d-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5b80d-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b80d-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b80d-111">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="5b80d-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="5b80d-112">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5b80d-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5b80d-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b80d-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b80d-114">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="5b80d-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="5b80d-115">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5b80d-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b80d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b80d-116">Return value</span></span>

<span data-ttu-id="5b80d-117">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="5b80d-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="5b80d-118">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die die Differenz zweier Vektoren ist.</span><span class="sxs-lookup"><span data-stu-id="5b80d-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the difference of two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b80d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b80d-119">Remarks</span></span>

<span data-ttu-id="5b80d-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5b80d-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5b80d-121">Auf diese Weise kann die **D3DXVec4Subtract** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b80d-121">In this way, the **D3DXVec4Subtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b80d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b80d-122">Requirements</span></span>



| <span data-ttu-id="5b80d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b80d-123">Requirement</span></span> | <span data-ttu-id="5b80d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5b80d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b80d-125">Header</span><span class="sxs-lookup"><span data-stu-id="5b80d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5b80d-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b80d-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5b80d-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5b80d-127">Library</span></span><br/> | <dl> <span data-ttu-id="5b80d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b80d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5b80d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b80d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b80d-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5b80d-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5b80d-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="5b80d-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="5b80d-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="5b80d-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




