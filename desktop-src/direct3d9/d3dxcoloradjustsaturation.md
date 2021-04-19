---
description: Passt den Sättigungswert einer Farbe an.
ms.assetid: 1f66c3b4-2f02-4993-80c6-c484180c2459
title: D3DXColorAdjustSaturation-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d9a801a8355c1a9399f9864f9b1753bbecc17b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364368"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx9mathh"></a><span data-ttu-id="34774-103">D3DXColorAdjustSaturation-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="34774-103">D3DXColorAdjustSaturation function (D3dx9math.h)</span></span>

<span data-ttu-id="34774-104">Passt den Sättigungswert einer Farbe an.</span><span class="sxs-lookup"><span data-stu-id="34774-104">Adjusts the saturation value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="34774-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34774-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="34774-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34774-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34774-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="34774-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="34774-108">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="34774-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="34774-109">Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="34774-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="34774-110">*PC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34774-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34774-111">Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="34774-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="34774-112">Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="34774-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="34774-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34774-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34774-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34774-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34774-115">Sättigungswert.</span><span class="sxs-lookup"><span data-stu-id="34774-115">Saturation value.</span></span> <span data-ttu-id="34774-116">Dieser Parameter interpoliert eine lineare Interpolation zwischen der Farbe, die in Graustufen konvertiert wurde, und der ursprünglichen Farbe, dem PC.</span><span class="sxs-lookup"><span data-stu-id="34774-116">This parameter linearly interpolates between the color converted to grayscale and the original color, pC.</span></span> <span data-ttu-id="34774-117">Es gibt keine Einschränkungen für den Wert von s.</span><span class="sxs-lookup"><span data-stu-id="34774-117">There are no limits on the value of s.</span></span> <span data-ttu-id="34774-118">Wenn s 0 ist, ist die zurückgegebene Farbe die Graustufen Farbe.</span><span class="sxs-lookup"><span data-stu-id="34774-118">If s is 0, the returned color is the grayscale color.</span></span> <span data-ttu-id="34774-119">Wenn s den Wert 1 hat, ist die zurückgegebene Farbe die ursprüngliche Farbe.</span><span class="sxs-lookup"><span data-stu-id="34774-119">If s is 1, the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34774-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34774-120">Return value</span></span>

<span data-ttu-id="34774-121">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="34774-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="34774-122">Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur zurück, die das Ergebnis der Sättigungs Anpassung ist.</span><span class="sxs-lookup"><span data-stu-id="34774-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the saturation adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="34774-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34774-123">Remarks</span></span>

<span data-ttu-id="34774-124">Der Alphakanal für die Eingabe wird unverändert in den Alpha-Ausgabekanal kopiert.</span><span class="sxs-lookup"><span data-stu-id="34774-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="34774-125">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="34774-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="34774-126">Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34774-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="34774-127">Diese Funktion interpoliert die roten, grünen und blauen Farbkomponenten einer [**D3DXCOLOR**](d3dxcolor.md) -Struktur zwischen einer ungesättigten Farbe und einer Farbe, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="34774-127">This function interpolates the red, green, and blue color components of a [**D3DXCOLOR**](d3dxcolor.md) structure between an unsaturated color and a color, as shown in the following example.</span></span>


```
    // Approximate values for each component's contribution to luminance.
    // Based upon the NTSC standard described in ITU-R Recommendation BT.709.
    FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;
    
    pOut->r = grey + s * (pC->r - grey);
```



<span data-ttu-id="34774-128">Wenn s größer als 0 und kleiner als 1 ist, wird die Sättigung verringert.</span><span class="sxs-lookup"><span data-stu-id="34774-128">If s is greater than 0 and less than 1, the saturation is decreased.</span></span> <span data-ttu-id="34774-129">Wenn s größer als 1 ist, wird die Sättigung angehoben.</span><span class="sxs-lookup"><span data-stu-id="34774-129">If s is greater than 1, the saturation is increased.</span></span>

<span data-ttu-id="34774-130">Die Graustufen Farbe wird wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="34774-130">The grayscale color is computed as:</span></span>


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b
```



## <a name="requirements"></a><span data-ttu-id="34774-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34774-131">Requirements</span></span>



| <span data-ttu-id="34774-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34774-132">Requirement</span></span> | <span data-ttu-id="34774-133">Wert</span><span class="sxs-lookup"><span data-stu-id="34774-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34774-134">Header</span><span class="sxs-lookup"><span data-stu-id="34774-134">Header</span></span><br/>  | <dl> <span data-ttu-id="34774-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="34774-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="34774-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34774-136">Library</span></span><br/> | <dl> <span data-ttu-id="34774-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34774-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="34774-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34774-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34774-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="34774-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="34774-140">**D3DXColorAdjustContrast**</span><span class="sxs-lookup"><span data-stu-id="34774-140">**D3DXColorAdjustContrast**</span></span>](d3dxcoloradjustcontrast.md)
</dt> </dl>

 

 
