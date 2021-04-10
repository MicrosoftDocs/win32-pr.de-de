---
description: Kombiniert zwei Farben.
ms.assetid: deff70c7-2359-48b2-ab40-8c418acf5a07
title: D3DXColorModulate-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorModulate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf9b202da786f6ec87ceca9816c2a4fc86776577
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219586"
---
# <a name="d3dxcolormodulate-function"></a><span data-ttu-id="2cecc-103">D3DXColorModulate-Funktion</span><span class="sxs-lookup"><span data-stu-id="2cecc-103">D3DXColorModulate function</span></span>

<span data-ttu-id="2cecc-104">Kombiniert zwei Farben.</span><span class="sxs-lookup"><span data-stu-id="2cecc-104">Blends two colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cecc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cecc-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorModulate(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="2cecc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cecc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cecc-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2cecc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cecc-108">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cecc-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="2cecc-109">Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="2cecc-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2cecc-110">*pC1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2cecc-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cecc-111">Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="2cecc-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="2cecc-112">Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2cecc-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2cecc-113">*pC2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2cecc-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cecc-114">Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="2cecc-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="2cecc-115">Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2cecc-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cecc-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2cecc-116">Return value</span></span>

<span data-ttu-id="2cecc-117">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cecc-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="2cecc-118">Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur zurück, die das Ergebnis des Mischungs Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="2cecc-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the blending operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cecc-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cecc-119">Remarks</span></span>

<span data-ttu-id="2cecc-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2cecc-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2cecc-121">Auf diese Weise kann die **D3DXColorModulate** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cecc-121">In this way, the **D3DXColorModulate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2cecc-122">Diese Funktion kombiniert zwei Farben, indem übereinstimmende Farbkomponenten multipliziert werden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2cecc-122">This function blends together two colors by multiplying matching color components, as shown in the following example.</span></span>


```
pOut->r = pC1->r * pC2->r;
```



## <a name="requirements"></a><span data-ttu-id="2cecc-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cecc-123">Requirements</span></span>



| <span data-ttu-id="2cecc-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cecc-124">Requirement</span></span> | <span data-ttu-id="2cecc-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2cecc-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cecc-126">Header</span><span class="sxs-lookup"><span data-stu-id="2cecc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2cecc-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cecc-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2cecc-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2cecc-128">Library</span></span><br/> | <dl> <span data-ttu-id="2cecc-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cecc-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2cecc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cecc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cecc-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2cecc-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2cecc-132">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="2cecc-132">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="2cecc-133">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="2cecc-133">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="2cecc-134">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="2cecc-134">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




