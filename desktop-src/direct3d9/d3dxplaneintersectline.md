---
description: Sucht die Schnittmenge zwischen einer Ebene und einer Linie.
ms.assetid: 2723cd3e-fdc3-4aab-a089-0089e5b14e3e
title: D3DXPlaneIntersectLine-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4a91a4592d039510e11147ffb680c880c43ccec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219433"
---
# <a name="d3dxplaneintersectline-function-d3dx9mathh"></a><span data-ttu-id="b24cc-103">D3DXPlaneIntersectLine-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b24cc-103">D3DXPlaneIntersectLine function (D3dx9math.h)</span></span>

<span data-ttu-id="b24cc-104">Sucht die Schnittmenge zwischen einer Ebene und einer Linie.</span><span class="sxs-lookup"><span data-stu-id="b24cc-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="b24cc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b24cc-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="b24cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b24cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b24cc-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b24cc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b24cc-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b24cc-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b24cc-109">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Schnittmenge zwischen der angegebenen Ebene und der angegebenen Zeile identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b24cc-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="b24cc-110">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b24cc-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b24cc-111">Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="b24cc-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="b24cc-112">Ein Zeiger auf die Quell- [**D3DXPLANE**](d3dxplane.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b24cc-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b24cc-113">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b24cc-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b24cc-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b24cc-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b24cc-115">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die einen Zeilen Startpunkt definiert.</span><span class="sxs-lookup"><span data-stu-id="b24cc-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="b24cc-116">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b24cc-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b24cc-117">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b24cc-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b24cc-118">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die einen Zeilen Endpunkt definiert.</span><span class="sxs-lookup"><span data-stu-id="b24cc-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b24cc-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b24cc-119">Return value</span></span>

<span data-ttu-id="b24cc-120">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b24cc-120">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b24cc-121">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Schnittmenge zwischen der angegebenen Ebene und der angegebenen Zeile ist.</span><span class="sxs-lookup"><span data-stu-id="b24cc-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="b24cc-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b24cc-122">Remarks</span></span>

<span data-ttu-id="b24cc-123">Wenn die Zeile parallel zur Ebene ist, wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b24cc-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="b24cc-124">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b24cc-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b24cc-125">Auf diese Weise kann die **D3DXPlaneIntersectLine** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b24cc-125">In this way, the **D3DXPlaneIntersectLine** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b24cc-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b24cc-126">Requirements</span></span>



| <span data-ttu-id="b24cc-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b24cc-127">Requirement</span></span> | <span data-ttu-id="b24cc-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b24cc-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b24cc-129">Header</span><span class="sxs-lookup"><span data-stu-id="b24cc-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b24cc-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b24cc-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b24cc-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b24cc-131">Library</span></span><br/> | <dl> <span data-ttu-id="b24cc-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b24cc-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b24cc-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b24cc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b24cc-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="b24cc-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




