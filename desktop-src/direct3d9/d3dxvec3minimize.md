---
description: Gibt einen 3D-Vektor zurück, der aus den kleinsten Komponenten von zwei 3D-Vektoren besteht.
ms.assetid: f38164a5-d016-4a8a-a7fe-d7eb0a681107
title: D3DXVec3Minimize-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 532c3cfaddc63b0f358fa3ce88afeccc2f12e289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050940"
---
# <a name="d3dxvec3minimize-function"></a><span data-ttu-id="4481a-103">D3DXVec3Minimize-Funktion</span><span class="sxs-lookup"><span data-stu-id="4481a-103">D3DXVec3Minimize function</span></span>

<span data-ttu-id="4481a-104">Gibt einen 3D-Vektor zurück, der aus den kleinsten Komponenten von zwei 3D-Vektoren besteht.</span><span class="sxs-lookup"><span data-stu-id="4481a-104">Returns a 3D vector that is made up of the smallest components of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="4481a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4481a-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Minimize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="4481a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4481a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4481a-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4481a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4481a-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4481a-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4481a-109">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="4481a-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4481a-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4481a-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4481a-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4481a-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4481a-112">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4481a-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4481a-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4481a-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4481a-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4481a-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4481a-115">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4481a-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4481a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4481a-116">Return value</span></span>

<span data-ttu-id="4481a-117">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4481a-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4481a-118">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die aus den kleinsten Komponenten der beiden Vektoren besteht.</span><span class="sxs-lookup"><span data-stu-id="4481a-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is made up of the smallest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="4481a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4481a-119">Remarks</span></span>

<span data-ttu-id="4481a-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4481a-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4481a-121">Auf diese Weise kann die **D3DXVec3Minimize** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4481a-121">In this way, the **D3DXVec3Minimize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4481a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4481a-122">Requirements</span></span>



| <span data-ttu-id="4481a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4481a-123">Requirement</span></span> | <span data-ttu-id="4481a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4481a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4481a-125">Header</span><span class="sxs-lookup"><span data-stu-id="4481a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4481a-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4481a-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4481a-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4481a-127">Library</span></span><br/> | <dl> <span data-ttu-id="4481a-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4481a-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4481a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4481a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4481a-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="4481a-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4481a-131">**D3DXVec3Maximize**</span><span class="sxs-lookup"><span data-stu-id="4481a-131">**D3DXVec3Maximize**</span></span>](d3dxvec3maximize.md)
</dt> </dl>

 

 




