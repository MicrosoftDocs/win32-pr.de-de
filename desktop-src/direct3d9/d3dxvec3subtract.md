---
description: Subtrahiert zwei 3D-Vektoren.
ms.assetid: 09e2cede-a0a3-4a5e-a7e1-e7a98cdc433b
title: D3DXVec3Subtract-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 17f41f2fd133db1064e2ba2778eacc139bab01ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219703"
---
# <a name="d3dxvec3subtract-function"></a><span data-ttu-id="2f8c8-103">D3DXVec3Subtract-Funktion</span><span class="sxs-lookup"><span data-stu-id="2f8c8-103">D3DXVec3Subtract function</span></span>

<span data-ttu-id="2f8c8-104">Subtrahiert zwei 3D-Vektoren.</span><span class="sxs-lookup"><span data-stu-id="2f8c8-104">Subtracts two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f8c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f8c8-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Subtract(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="2f8c8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f8c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f8c8-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2f8c8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f8c8-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f8c8-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f8c8-109">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="2f8c8-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2f8c8-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f8c8-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f8c8-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f8c8-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f8c8-112">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2f8c8-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2f8c8-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f8c8-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f8c8-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f8c8-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f8c8-115">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2f8c8-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f8c8-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f8c8-116">Return value</span></span>

<span data-ttu-id="2f8c8-117">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f8c8-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f8c8-118">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Differenz zweier Vektoren ist.</span><span class="sxs-lookup"><span data-stu-id="2f8c8-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the difference of two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f8c8-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f8c8-119">Remarks</span></span>

<span data-ttu-id="2f8c8-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2f8c8-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2f8c8-121">Auf diese Weise kann die **D3DXVec3Subtract** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f8c8-121">In this way, the **D3DXVec3Subtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f8c8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f8c8-122">Requirements</span></span>



| <span data-ttu-id="2f8c8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f8c8-123">Requirement</span></span> | <span data-ttu-id="2f8c8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2f8c8-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f8c8-125">Header</span><span class="sxs-lookup"><span data-stu-id="2f8c8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2f8c8-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f8c8-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2f8c8-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2f8c8-127">Library</span></span><br/> | <dl> <span data-ttu-id="2f8c8-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f8c8-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f8c8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f8c8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f8c8-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2f8c8-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2f8c8-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="2f8c8-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="2f8c8-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="2f8c8-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




