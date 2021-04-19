---
description: Erstellt den negativen Farbwert eines Farbwerts.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: D3DXColorNegative-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6d4d8559e64580897aec5261c450dc739496e75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355018"
---
# <a name="d3dxcolornegative-function"></a><span data-ttu-id="0fb27-103">D3DXColorNegative-Funktion</span><span class="sxs-lookup"><span data-stu-id="0fb27-103">D3DXColorNegative function</span></span>

<span data-ttu-id="0fb27-104">Erstellt den negativen Farbwert eines Farbwerts.</span><span class="sxs-lookup"><span data-stu-id="0fb27-104">Creates the negative color value of a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fb27-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fb27-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
);
```



## <a name="parameters"></a><span data-ttu-id="0fb27-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fb27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fb27-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0fb27-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb27-108">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="0fb27-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="0fb27-109">Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="0fb27-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0fb27-110">*PC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0fb27-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb27-111">Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="0fb27-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="0fb27-112">Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0fb27-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fb27-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fb27-113">Return value</span></span>

<span data-ttu-id="0fb27-114">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="0fb27-114">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="0fb27-115">Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur zurück, die der negative Farbwert des Farbwerts ist.</span><span class="sxs-lookup"><span data-stu-id="0fb27-115">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the negative color value of the color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fb27-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fb27-116">Remarks</span></span>

<span data-ttu-id="0fb27-117">Der Alphakanal für die Eingabe wird unverändert in den Alpha-Ausgabekanal kopiert.</span><span class="sxs-lookup"><span data-stu-id="0fb27-117">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="0fb27-118">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0fb27-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0fb27-119">Auf diese Weise kann die **D3DXColorNegative** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb27-119">In this way, the **D3DXColorNegative** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0fb27-120">Diese Funktion gibt den negativen Farbwert zurück, indem Sie 1,0 von den Farbkomponenten der [**D3DXCOLOR**](d3dxcolor.md) -Struktur subtrahieren, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0fb27-120">This function returns the negative color value by subtracting 1.0 from the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure, as shown in the following example.</span></span>


```
pOut->r = 1.0f - pC->r;
```



## <a name="requirements"></a><span data-ttu-id="0fb27-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fb27-121">Requirements</span></span>



| <span data-ttu-id="0fb27-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fb27-122">Requirement</span></span> | <span data-ttu-id="0fb27-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0fb27-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb27-124">Header</span><span class="sxs-lookup"><span data-stu-id="0fb27-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0fb27-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fb27-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0fb27-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0fb27-126">Library</span></span><br/> | <dl> <span data-ttu-id="0fb27-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fb27-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0fb27-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fb27-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fb27-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="0fb27-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0fb27-130">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="0fb27-130">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="0fb27-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="0fb27-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="0fb27-132">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="0fb27-132">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




