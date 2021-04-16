---
description: Gibt einen 3D-Vektor zurück, der aus den größten Komponenten von zwei 3D-Vektoren besteht.
ms.assetid: 8d3a5310-bee9-4dbd-bef3-8a0e1586f365
title: D3DXVec3Maximize-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d86f3e54a6399693e37cc0c8970439558d82c9c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530872"
---
# <a name="d3dxvec3maximize-function"></a><span data-ttu-id="6dc42-103">D3DXVec3Maximize-Funktion</span><span class="sxs-lookup"><span data-stu-id="6dc42-103">D3DXVec3Maximize function</span></span>

<span data-ttu-id="6dc42-104">Gibt einen 3D-Vektor zurück, der aus den größten Komponenten von zwei 3D-Vektoren besteht.</span><span class="sxs-lookup"><span data-stu-id="6dc42-104">Returns a 3D vector that is made up of the largest components of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dc42-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dc42-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Maximize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="6dc42-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dc42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dc42-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6dc42-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dc42-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6dc42-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6dc42-109">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="6dc42-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6dc42-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6dc42-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dc42-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6dc42-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6dc42-112">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6dc42-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6dc42-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6dc42-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dc42-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6dc42-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6dc42-115">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6dc42-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dc42-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6dc42-116">Return value</span></span>

<span data-ttu-id="6dc42-117">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6dc42-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6dc42-118">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die aus den größten Komponenten der beiden Vektoren besteht.</span><span class="sxs-lookup"><span data-stu-id="6dc42-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dc42-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6dc42-119">Remarks</span></span>

<span data-ttu-id="6dc42-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6dc42-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6dc42-121">Auf diese Weise kann die **D3DXVec3Maximize** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6dc42-121">In this way, the **D3DXVec3Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dc42-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dc42-122">Requirements</span></span>



| <span data-ttu-id="6dc42-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6dc42-123">Requirement</span></span> | <span data-ttu-id="6dc42-124">Wert</span><span class="sxs-lookup"><span data-stu-id="6dc42-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc42-125">Header</span><span class="sxs-lookup"><span data-stu-id="6dc42-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6dc42-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dc42-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6dc42-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6dc42-127">Library</span></span><br/> | <dl> <span data-ttu-id="6dc42-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6dc42-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6dc42-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dc42-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dc42-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="6dc42-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6dc42-131">**D3DXVec3Minimize**</span><span class="sxs-lookup"><span data-stu-id="6dc42-131">**D3DXVec3Minimize**</span></span>](d3dxvec3minimize.md)
</dt> </dl>

 

 




