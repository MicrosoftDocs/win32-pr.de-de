---
description: Sucht die Schnittmenge zwischen einer Ebene und einer Linie.
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: D3DXPlaneIntersectLine-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 00d25fcba9e5884cec10da96964ad0f5daa9ed14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357273"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a><span data-ttu-id="0e8f4-103">D3DXPlaneIntersectLine-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="0e8f4-103">D3DXPlaneIntersectLine function (D3DX10Math.h)</span></span>

<span data-ttu-id="0e8f4-104">Sucht die Schnittmenge zwischen einer Ebene und einer Linie.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e8f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e8f4-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="0e8f4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e8f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e8f4-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0e8f4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e8f4-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e8f4-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0e8f4-109">Zeiger auf ein [**D3DXVECTOR3**](d3d10-d3dxvector3.md)-Typ, der die Schnittmenge zwischen der angegebenen Ebene und der angegebenen Zeile identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="0e8f4-110">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e8f4-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e8f4-111">Typ: **Konstanten [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e8f4-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="0e8f4-112">Zeiger auf den Quell- [**D3DXPLANE**](d3d10-d3dxplane.md).</span><span class="sxs-lookup"><span data-stu-id="0e8f4-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e8f4-113">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e8f4-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e8f4-114">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e8f4-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0e8f4-115">Zeiger auf eine Quell-D3DXVECTOR3-Struktur, die einen Zeilen Startpunkt definiert.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-115">Pointer to a source D3DXVECTOR3 structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="0e8f4-116">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e8f4-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e8f4-117">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e8f4-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0e8f4-118">Zeiger auf eine Quell-D3DXVECTOR3-Struktur, die einen Zeilen Endpunkt definiert.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-118">Pointer to a source D3DXVECTOR3 structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e8f4-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e8f4-119">Return value</span></span>

<span data-ttu-id="0e8f4-120">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e8f4-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0e8f4-121">Zeiger auf eine D3DXVECTOR3-Struktur, die die Schnittmenge zwischen der angegebenen Ebene und der angegebenen Zeile ist.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-121">Pointer to a D3DXVECTOR3 structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e8f4-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e8f4-122">Remarks</span></span>

<span data-ttu-id="0e8f4-123">Wenn die Zeile parallel zur Ebene ist, wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="0e8f4-124">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0e8f4-125">Auf diese Weise kann die D3DXPlaneIntersectLine-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-125">In this way, the D3DXPlaneIntersectLine function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e8f4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e8f4-126">Requirements</span></span>



| <span data-ttu-id="0e8f4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e8f4-127">Requirement</span></span> | <span data-ttu-id="0e8f4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0e8f4-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e8f4-129">Header</span><span class="sxs-lookup"><span data-stu-id="0e8f4-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0e8f4-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e8f4-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="0e8f4-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e8f4-131">Library</span></span><br/> | <dl> <span data-ttu-id="0e8f4-132"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e8f4-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0e8f4-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e8f4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e8f4-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="0e8f4-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
