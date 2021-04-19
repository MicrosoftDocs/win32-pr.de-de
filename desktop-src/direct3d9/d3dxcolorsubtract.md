---
description: Subtrahiert zwei Farbwerte, um einen neuen Farbwert zu erstellen.
ms.assetid: c21f8402-c1c2-4909-896f-2872ef518537
title: D3DXColorSubtract-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorSubtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 47f28ea3a3fb6d1556e699fed3820e228faf6604
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355201"
---
# <a name="d3dxcolorsubtract-function"></a><span data-ttu-id="c58c2-103">D3DXColorSubtract-Funktion</span><span class="sxs-lookup"><span data-stu-id="c58c2-103">D3DXColorSubtract function</span></span>

<span data-ttu-id="c58c2-104">Subtrahiert zwei Farbwerte, um einen neuen Farbwert zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c58c2-104">Subtracts two color values to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c58c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c58c2-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorSubtract(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="c58c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c58c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c58c2-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c58c2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c58c2-108">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="c58c2-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="c58c2-109">Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="c58c2-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c58c2-110">*pC1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c58c2-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c58c2-111">Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="c58c2-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="c58c2-112">Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c58c2-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c58c2-113">*pC2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c58c2-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c58c2-114">Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="c58c2-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="c58c2-115">Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c58c2-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c58c2-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c58c2-116">Return value</span></span>

<span data-ttu-id="c58c2-117">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="c58c2-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="c58c2-118">Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur zurück, die den Unterschied zwischen zwei Farbwerten ist.</span><span class="sxs-lookup"><span data-stu-id="c58c2-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the difference between two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c58c2-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c58c2-119">Remarks</span></span>

<span data-ttu-id="c58c2-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c58c2-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c58c2-121">Auf diese Weise kann die **D3DXColorSubtract** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c58c2-121">In this way, the **D3DXColorSubtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c58c2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c58c2-122">Requirements</span></span>



| <span data-ttu-id="c58c2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c58c2-123">Requirement</span></span> | <span data-ttu-id="c58c2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c58c2-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c58c2-125">Header</span><span class="sxs-lookup"><span data-stu-id="c58c2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c58c2-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c58c2-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c58c2-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c58c2-127">Library</span></span><br/> | <dl> <span data-ttu-id="c58c2-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c58c2-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c58c2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c58c2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c58c2-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c58c2-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c58c2-131">**D3DXColorAdd**</span><span class="sxs-lookup"><span data-stu-id="c58c2-131">**D3DXColorAdd**</span></span>](d3dxcoloradd.md)
</dt> </dl>

 

 




