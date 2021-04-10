---
description: Passt den Sättigungswert einer Farbe an.
ms.assetid: a7ca64b4-2198-4116-8e9f-79d6c922fd09
title: D3DXColorAdjustSaturation-Funktion (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6cfa4dd2af6e4a4ac3772af80ba11b8189405f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961704"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx10mathh"></a><span data-ttu-id="8eff7-103">D3DXColorAdjustSaturation-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="8eff7-103">D3DXColorAdjustSaturation function (D3DX10Math.h)</span></span>

<span data-ttu-id="8eff7-104">Passt den Sättigungswert einer Farbe an.</span><span class="sxs-lookup"><span data-stu-id="8eff7-104">Adjusts the saturation value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eff7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8eff7-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="8eff7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8eff7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eff7-107">*Pout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8eff7-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eff7-108">Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="8eff7-108">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="8eff7-109">Zeiger auf ein [**D3DXCOLOR**](d3d10-d3dxcolor.md) -Ergebnis, das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="8eff7-109">Pointer to a [**D3DXCOLOR**](d3d10-d3dxcolor.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8eff7-110">*PC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8eff7-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eff7-111">Typ: **Konstanten [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="8eff7-111">Type: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="8eff7-112">Zeiger auf eine Quell-D3DXCOLOR-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8eff7-112">Pointer to a source D3DXCOLOR structure.</span></span>

</dd> <dt>

<span data-ttu-id="8eff7-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8eff7-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eff7-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8eff7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8eff7-115">Sättigungswert.</span><span class="sxs-lookup"><span data-stu-id="8eff7-115">Saturation value.</span></span> <span data-ttu-id="8eff7-116">Dieser Parameter interpoliert eine lineare Interpolation zwischen der Farbe, die in Graustufen konvertiert wurde, und der ursprünglichen Farbe, dem PC.</span><span class="sxs-lookup"><span data-stu-id="8eff7-116">This parameter linearly interpolates between the color converted to grayscale and the original color, pC.</span></span> <span data-ttu-id="8eff7-117">Es gibt keine Einschränkungen für den Wert von s.</span><span class="sxs-lookup"><span data-stu-id="8eff7-117">There are no limits on the value of s.</span></span> <span data-ttu-id="8eff7-118">Wenn s 0 ist, ist die zurückgegebene Farbe die Graustufen Farbe.</span><span class="sxs-lookup"><span data-stu-id="8eff7-118">If s is 0, the returned color is the grayscale color.</span></span> <span data-ttu-id="8eff7-119">Wenn s den Wert 1 hat, ist die zurückgegebene Farbe die ursprüngliche Farbe.</span><span class="sxs-lookup"><span data-stu-id="8eff7-119">If s is 1, the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eff7-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8eff7-120">Return value</span></span>

<span data-ttu-id="8eff7-121">Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="8eff7-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="8eff7-122">Diese Funktion gibt einen Zeiger auf eine D3DXCOLOR-Struktur zurück, die das Ergebnis der Sättigungs Anpassung ist.</span><span class="sxs-lookup"><span data-stu-id="8eff7-122">This function returns a pointer to a D3DXCOLOR structure that is the result of the saturation adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eff7-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8eff7-123">Remarks</span></span>

<span data-ttu-id="8eff7-124">Der Alphakanal für die Eingabe wird unverändert in den Alpha-Ausgabekanal kopiert.</span><span class="sxs-lookup"><span data-stu-id="8eff7-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="8eff7-125">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8eff7-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8eff7-126">Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8eff7-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8eff7-127">Diese Funktion interpoliert die roten, grünen und blauen Farbkomponenten einer D3DXCOLOR-Struktur zwischen einer ungesättigten Farbe und einer Farbe, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8eff7-127">This function interpolates the red, green, and blue color components of a D3DXCOLOR structure between an unsaturated color and a color, as shown in the following example.</span></span>


```
//Approximate values for each component's contribution to luminance.
//Based upon the NTSC standard described in ITU-R Recommendation BT.709.
FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;

pOut->r = grey + s * (pC->r - grey);
```



<span data-ttu-id="8eff7-128">Wenn s größer als 0 und kleiner als 1 ist, wird die Sättigung verringert.</span><span class="sxs-lookup"><span data-stu-id="8eff7-128">If s is greater than 0 and less than 1, the saturation is decreased.</span></span> <span data-ttu-id="8eff7-129">Wenn s größer als 1 ist, wird die Sättigung angehoben.</span><span class="sxs-lookup"><span data-stu-id="8eff7-129">If s is greater than 1, the saturation is increased.</span></span>

<span data-ttu-id="8eff7-130">Die Graustufen Farbe wird wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="8eff7-130">The grayscale color is computed as:</span></span>


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b;
```



## <a name="requirements"></a><span data-ttu-id="8eff7-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8eff7-131">Requirements</span></span>



| <span data-ttu-id="8eff7-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8eff7-132">Requirement</span></span> | <span data-ttu-id="8eff7-133">Wert</span><span class="sxs-lookup"><span data-stu-id="8eff7-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8eff7-134">Header</span><span class="sxs-lookup"><span data-stu-id="8eff7-134">Header</span></span><br/>  | <dl> <span data-ttu-id="8eff7-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eff7-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8eff7-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8eff7-136">Library</span></span><br/> | <dl> <span data-ttu-id="8eff7-137"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8eff7-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8eff7-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8eff7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eff7-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="8eff7-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
