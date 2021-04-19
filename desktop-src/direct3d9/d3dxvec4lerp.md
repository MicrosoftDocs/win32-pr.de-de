---
description: Führt eine lineare interpolung zwischen zwei 4D-Vektoren aus.
ms.assetid: a068a626-17cd-4df9-8f41-9b417bfda1d1
title: D3DXVec4Lerp-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8df6f7b4be5a39335532dc86096f989727230942
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370435"
---
# <a name="d3dxvec4lerp-function"></a><span data-ttu-id="6b9e3-103">D3DXVec4Lerp-Funktion</span><span class="sxs-lookup"><span data-stu-id="6b9e3-103">D3DXVec4Lerp function</span></span>

<span data-ttu-id="6b9e3-104">Führt eine lineare interpolung zwischen zwei 4D-Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="6b9e3-104">Performs a linear interpolation between two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b9e3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b9e3-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Lerp(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="6b9e3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b9e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b9e3-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6b9e3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b9e3-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b9e3-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6b9e3-109">Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="6b9e3-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6b9e3-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b9e3-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b9e3-111">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="6b9e3-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6b9e3-112">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6b9e3-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6b9e3-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b9e3-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b9e3-114">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="6b9e3-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6b9e3-115">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6b9e3-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6b9e3-116">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b9e3-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b9e3-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b9e3-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b9e3-118">Der Parameter, der linear zwischen den Vektoren interpoliert.</span><span class="sxs-lookup"><span data-stu-id="6b9e3-118">Parameter that linearly interpolates between the vectors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b9e3-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b9e3-119">Return value</span></span>

<span data-ttu-id="6b9e3-120">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b9e3-120">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6b9e3-121">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis der linearen interpolung ist.</span><span class="sxs-lookup"><span data-stu-id="6b9e3-121">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b9e3-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b9e3-122">Remarks</span></span>

<span data-ttu-id="6b9e3-123">Diese Funktion führt die lineare interpolung basierend auf der folgenden Formel aus: v1 + s (V2-V1).</span><span class="sxs-lookup"><span data-stu-id="6b9e3-123">This function performs the linear interpolation based on the following formula: V1 + s(V2-V1).</span></span>

<span data-ttu-id="6b9e3-124">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6b9e3-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6b9e3-125">Auf diese Weise kann die **D3DXVec4Lerp** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b9e3-125">In this way, the **D3DXVec4Lerp** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b9e3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b9e3-126">Requirements</span></span>



| <span data-ttu-id="6b9e3-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b9e3-127">Requirement</span></span> | <span data-ttu-id="6b9e3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6b9e3-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b9e3-129">Header</span><span class="sxs-lookup"><span data-stu-id="6b9e3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6b9e3-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b9e3-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6b9e3-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b9e3-131">Library</span></span><br/> | <dl> <span data-ttu-id="6b9e3-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b9e3-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6b9e3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b9e3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b9e3-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="6b9e3-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
