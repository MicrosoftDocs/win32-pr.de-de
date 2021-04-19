---
description: Bestimmt das Kreuz Produkt von zwei 3D-Vektoren.
ms.assetid: c9623f35-c8fc-4fbe-87b6-0e5bb8ebd5e8
title: D3DXVec3Cross-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ba0d8a80690f43d5f8e9f6df55aa3b2e0db23dc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353361"
---
# <a name="d3dxvec3cross-function"></a><span data-ttu-id="e5406-103">D3DXVec3Cross-Funktion</span><span class="sxs-lookup"><span data-stu-id="e5406-103">D3DXVec3Cross function</span></span>

<span data-ttu-id="e5406-104">Bestimmt das Kreuz Produkt von zwei 3D-Vektoren.</span><span class="sxs-lookup"><span data-stu-id="e5406-104">Determines the cross-product of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5406-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5406-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Cross(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="e5406-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5406-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5406-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e5406-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5406-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5406-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e5406-109">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="e5406-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e5406-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5406-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5406-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e5406-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e5406-112">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e5406-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e5406-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5406-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5406-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e5406-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e5406-115">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e5406-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5406-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5406-116">Return value</span></span>

<span data-ttu-id="e5406-117">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5406-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e5406-118">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Kreuz Produkt von zwei 3D-Vektoren ist.</span><span class="sxs-lookup"><span data-stu-id="e5406-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the cross product of two 3D vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5406-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5406-119">Remarks</span></span>

<span data-ttu-id="e5406-120">Diese Funktion bestimmt das Kreuz Produkt mit dem folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="e5406-120">This function determines the cross-product with the following code.</span></span>


```
D3DXVECTOR3 v;
    
v.x = pV1->y * pV2->z - pV1->z * pV2->y;
v.y = pV1->z * pV2->x - pV1->x * pV2->z;
v.z = pV1->x * pV2->y - pV1->y * pV2->x;
    
*pOut = v;
```



<span data-ttu-id="e5406-121">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e5406-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e5406-122">Auf diese Weise kann die **D3DXVec3Cross** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5406-122">In this way, the **D3DXVec3Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5406-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5406-123">Requirements</span></span>



| <span data-ttu-id="e5406-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5406-124">Requirement</span></span> | <span data-ttu-id="e5406-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e5406-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5406-126">Header</span><span class="sxs-lookup"><span data-stu-id="e5406-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e5406-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5406-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e5406-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e5406-128">Library</span></span><br/> | <dl> <span data-ttu-id="e5406-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5406-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e5406-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5406-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5406-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="e5406-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e5406-132">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="e5406-132">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
</dt> </dl>

 

 




