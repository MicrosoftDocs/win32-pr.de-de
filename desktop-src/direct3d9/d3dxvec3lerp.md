---
description: Führt eine lineare interpolung zwischen zwei 3D-Vektoren aus.
ms.assetid: f3f06f1b-8824-47f0-b2ed-c212fa4c3225
title: D3DXVec3Lerp-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed6905cc0b13908a4e60e221737e9b5dc5a627f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365351"
---
# <a name="d3dxvec3lerp-function"></a><span data-ttu-id="cc89c-103">D3DXVec3Lerp-Funktion</span><span class="sxs-lookup"><span data-stu-id="cc89c-103">D3DXVec3Lerp function</span></span>

<span data-ttu-id="cc89c-104">Führt eine lineare interpolung zwischen zwei 3D-Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="cc89c-104">Performs a linear interpolation between two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc89c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc89c-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Lerp(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="cc89c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc89c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc89c-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cc89c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc89c-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc89c-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cc89c-109">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="cc89c-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cc89c-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc89c-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc89c-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc89c-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cc89c-112">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="cc89c-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cc89c-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc89c-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc89c-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc89c-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cc89c-115">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="cc89c-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cc89c-116">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc89c-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc89c-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc89c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc89c-118">Der Parameter, der linear zwischen den Vektoren interpoliert.</span><span class="sxs-lookup"><span data-stu-id="cc89c-118">Parameter that linearly interpolates between the vectors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc89c-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc89c-119">Return value</span></span>

<span data-ttu-id="cc89c-120">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc89c-120">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cc89c-121">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis der linearen interpolung ist.</span><span class="sxs-lookup"><span data-stu-id="cc89c-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc89c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc89c-122">Remarks</span></span>

<span data-ttu-id="cc89c-123">Diese Funktion führt die lineare interpolung basierend auf der folgenden Formel aus: v1 + s (V2-V1).</span><span class="sxs-lookup"><span data-stu-id="cc89c-123">This function performs the linear interpolation based on the following formula: V1 + s(V2-V1).</span></span>

<span data-ttu-id="cc89c-124">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc89c-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="cc89c-125">Auf diese Weise kann die **D3DXVec3Lerp** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc89c-125">In this way, the **D3DXVec3Lerp** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc89c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc89c-126">Requirements</span></span>



| <span data-ttu-id="cc89c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc89c-127">Requirement</span></span> | <span data-ttu-id="cc89c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="cc89c-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc89c-129">Header</span><span class="sxs-lookup"><span data-stu-id="cc89c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cc89c-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc89c-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="cc89c-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cc89c-131">Library</span></span><br/> | <dl> <span data-ttu-id="cc89c-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc89c-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cc89c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc89c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc89c-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="cc89c-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
