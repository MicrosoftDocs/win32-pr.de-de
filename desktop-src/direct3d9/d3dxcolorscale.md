---
description: Skaliert einen Farbwert.
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: D3DXColorScale-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74020f302a26162df1e42cb4c9f020af3f64e59c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351968"
---
# <a name="d3dxcolorscale-function"></a><span data-ttu-id="267e0-103">D3DXColorScale-Funktion</span><span class="sxs-lookup"><span data-stu-id="267e0-103">D3DXColorScale function</span></span>

<span data-ttu-id="267e0-104">Skaliert einen Farbwert.</span><span class="sxs-lookup"><span data-stu-id="267e0-104">Scales a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="267e0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="267e0-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorScale(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="267e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="267e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="267e0-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="267e0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="267e0-108">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="267e0-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="267e0-109">Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="267e0-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="267e0-110">*PC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="267e0-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="267e0-111">Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="267e0-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="267e0-112">Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="267e0-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="267e0-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="267e0-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="267e0-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="267e0-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="267e0-115">Skalierungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="267e0-115">Scale factor.</span></span> <span data-ttu-id="267e0-116">Die Farbe wird skaliert und wie ein 4D-Vektor behandelt.</span><span class="sxs-lookup"><span data-stu-id="267e0-116">It scales the color, treating it like a 4D vector.</span></span> <span data-ttu-id="267e0-117">Es gibt keine Einschränkungen für den Wert von s.</span><span class="sxs-lookup"><span data-stu-id="267e0-117">There are no limits on the value of s.</span></span> <span data-ttu-id="267e0-118">Wenn s den Wert 1 hat, ist die resultierende Farbe die ursprüngliche Farbe.</span><span class="sxs-lookup"><span data-stu-id="267e0-118">If s is 1, the resulting color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="267e0-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="267e0-119">Return value</span></span>

<span data-ttu-id="267e0-120">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="267e0-120">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="267e0-121">Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur zurück, die der skalierte Farbwert ist.</span><span class="sxs-lookup"><span data-stu-id="267e0-121">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the scaled color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="267e0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="267e0-122">Remarks</span></span>

<span data-ttu-id="267e0-123">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="267e0-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="267e0-124">Auf diese Weise kann die **D3DXColorScale** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="267e0-124">In this way, the **D3DXColorScale** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="267e0-125">Diese Funktion berechnet den skalierten Farbwert, indem die Farbkomponenten der [**D3DXCOLOR**](d3dxcolor.md) -Struktur mit dem angegebenen Skalierungsfaktor multipliziert werden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="267e0-125">This function computes the scaled color value by multiplying the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure by the specified scale factor, as shown in the following example.</span></span>


```
pOut->r = pC->r * s;
```



## <a name="requirements"></a><span data-ttu-id="267e0-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="267e0-126">Requirements</span></span>



| <span data-ttu-id="267e0-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="267e0-127">Requirement</span></span> | <span data-ttu-id="267e0-128">Wert</span><span class="sxs-lookup"><span data-stu-id="267e0-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="267e0-129">Header</span><span class="sxs-lookup"><span data-stu-id="267e0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="267e0-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="267e0-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="267e0-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="267e0-131">Library</span></span><br/> | <dl> <span data-ttu-id="267e0-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="267e0-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="267e0-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="267e0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="267e0-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="267e0-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="267e0-135">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="267e0-135">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="267e0-136">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="267e0-136">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="267e0-137">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="267e0-137">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> </dl>

 

 
