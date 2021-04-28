---
description: 'D3DXColorAdjustSaturation-Funktion (D3DX10Math.h): Passt den Sättigungswert einer Farbe an.'
ms.assetid: a7ca64b4-2198-4116-8e9f-79d6c922fd09
title: D3DXColorAdjustSaturation-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 9e9ae91f5c898dae8ff922616bc02846732c760a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103538"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx10mathh"></a><span data-ttu-id="5c241-103">D3DXColorAdjustSaturation-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="5c241-103">D3DXColorAdjustSaturation function (D3DX10Math.h)</span></span>

<span data-ttu-id="5c241-104">Passt den Sättigungswert einer Farbe an.</span><span class="sxs-lookup"><span data-stu-id="5c241-104">Adjusts the saturation value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c241-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c241-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="5c241-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c241-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c241-107">*pOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5c241-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c241-108">Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="5c241-108">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="5c241-109">Zeiger auf eine [**D3DXCOLOR,**](d3d10-d3dxcolor.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="5c241-109">Pointer to a [**D3DXCOLOR**](d3d10-d3dxcolor.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5c241-110">*pC* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5c241-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c241-111">Typ: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="5c241-111">Type: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="5c241-112">Zeiger auf eine D3DXCOLOR-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="5c241-112">Pointer to a source D3DXCOLOR structure.</span></span>

</dd> <dt>

<span data-ttu-id="5c241-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c241-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c241-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c241-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c241-115">Sättigungswert.</span><span class="sxs-lookup"><span data-stu-id="5c241-115">Saturation value.</span></span> <span data-ttu-id="5c241-116">Dieser Parameter interpoliert linear zwischen der in Graustufen konvertierten Farbe und der ursprünglichen Farbe pC.</span><span class="sxs-lookup"><span data-stu-id="5c241-116">This parameter linearly interpolates between the color converted to grayscale and the original color, pC.</span></span> <span data-ttu-id="5c241-117">Es gibt keine Grenzwerte für den Wert von s.</span><span class="sxs-lookup"><span data-stu-id="5c241-117">There are no limits on the value of s.</span></span> <span data-ttu-id="5c241-118">Wenn s 0 ist, ist die zurückgegebene Farbe die Graustufenfarbe.</span><span class="sxs-lookup"><span data-stu-id="5c241-118">If s is 0, the returned color is the grayscale color.</span></span> <span data-ttu-id="5c241-119">Wenn s 1 ist, ist die zurückgegebene Farbe die ursprüngliche Farbe.</span><span class="sxs-lookup"><span data-stu-id="5c241-119">If s is 1, the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c241-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c241-120">Return value</span></span>

<span data-ttu-id="5c241-121">Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="5c241-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="5c241-122">Diese Funktion gibt einen Zeiger auf eine D3DXCOLOR-Struktur zurück, die das Ergebnis der Anpassung der Sättigung ist.</span><span class="sxs-lookup"><span data-stu-id="5c241-122">This function returns a pointer to a D3DXCOLOR structure that is the result of the saturation adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c241-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c241-123">Remarks</span></span>

<span data-ttu-id="5c241-124">Der Alpha-Eingabekanal wird unverändert in den Alphaausgabekanal kopiert.</span><span class="sxs-lookup"><span data-stu-id="5c241-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="5c241-125">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5c241-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5c241-126">Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c241-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="5c241-127">Diese Funktion interpoliert die Rot-, Grün- und Blau-Farbkomponenten einer D3DXCOLOR-Struktur zwischen einer nicht überlasteten Farbe und einer Farbe, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c241-127">This function interpolates the red, green, and blue color components of a D3DXCOLOR structure between an unsaturated color and a color, as shown in the following example.</span></span>


```
//Approximate values for each component's contribution to luminance.
//Based upon the NTSC standard described in ITU-R Recommendation BT.709.
FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;

pOut->r = grey + s * (pC->r - grey);
```



<span data-ttu-id="5c241-128">Wenn s größer als 0 und kleiner als 1 ist, wird die Sättigung verringert.</span><span class="sxs-lookup"><span data-stu-id="5c241-128">If s is greater than 0 and less than 1, the saturation is decreased.</span></span> <span data-ttu-id="5c241-129">Wenn s größer als 1 ist, wird die Sättigung erhöht.</span><span class="sxs-lookup"><span data-stu-id="5c241-129">If s is greater than 1, the saturation is increased.</span></span>

<span data-ttu-id="5c241-130">Die Graustufenfarbe wird wie die folgende berechnet:</span><span class="sxs-lookup"><span data-stu-id="5c241-130">The grayscale color is computed as:</span></span>


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b;
```



## <a name="requirements"></a><span data-ttu-id="5c241-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c241-131">Requirements</span></span>



| <span data-ttu-id="5c241-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c241-132">Requirement</span></span> | <span data-ttu-id="5c241-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5c241-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c241-134">Header</span><span class="sxs-lookup"><span data-stu-id="5c241-134">Header</span></span><br/>  | <dl> <span data-ttu-id="5c241-135"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5c241-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5c241-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5c241-136">Library</span></span><br/> | <dl> <span data-ttu-id="5c241-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c241-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5c241-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5c241-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c241-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5c241-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
