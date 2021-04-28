---
description: 'D3DXColorAdjustSaturation-Funktion (D3dx9math.h): Passt den Sättigungswert einer Farbe an.'
ms.assetid: 1f66c3b4-2f02-4993-80c6-c484180c2459
title: D3DXColorAdjustSaturation-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 878cdd83a04f594da3133eda314486af96ac3d56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115868"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx9mathh"></a><span data-ttu-id="0c2a9-103">D3DXColorAdjustSaturation-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="0c2a9-103">D3DXColorAdjustSaturation function (D3dx9math.h)</span></span>

<span data-ttu-id="0c2a9-104">Passt den Sättigungswert einer Farbe an.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-104">Adjusts the saturation value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c2a9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c2a9-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="0c2a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c2a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c2a9-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0c2a9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c2a9-108">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c2a9-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="0c2a9-109">Zeiger auf eine [**D3DXCOLOR-Struktur,**](d3dxcolor.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0c2a9-110">*pC* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0c2a9-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c2a9-111">Typ: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="0c2a9-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="0c2a9-112">Zeiger auf eine [**D3DXCOLOR-Quellstruktur.**](d3dxcolor.md)</span><span class="sxs-lookup"><span data-stu-id="0c2a9-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0c2a9-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c2a9-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c2a9-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c2a9-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c2a9-115">Sättigungswert.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-115">Saturation value.</span></span> <span data-ttu-id="0c2a9-116">Dieser Parameter interpoliert linear zwischen der in Graustufen konvertierten Farbe und der ursprünglichen Farbe pC.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-116">This parameter linearly interpolates between the color converted to grayscale and the original color, pC.</span></span> <span data-ttu-id="0c2a9-117">Es gibt keine Grenzwerte für den Wert von s.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-117">There are no limits on the value of s.</span></span> <span data-ttu-id="0c2a9-118">Wenn s 0 ist, ist die zurückgegebene Farbe die Graustufenfarbe.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-118">If s is 0, the returned color is the grayscale color.</span></span> <span data-ttu-id="0c2a9-119">Wenn s 1 ist, ist die zurückgegebene Farbe die ursprüngliche Farbe.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-119">If s is 1, the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c2a9-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c2a9-120">Return value</span></span>

<span data-ttu-id="0c2a9-121">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c2a9-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="0c2a9-122">Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR-Struktur**](d3dxcolor.md) zurück, die das Ergebnis der Anpassung der Sättigung ist.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the saturation adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c2a9-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c2a9-123">Remarks</span></span>

<span data-ttu-id="0c2a9-124">Der Alpha-Eingabekanal wird unverändert in den Alphaausgabekanal kopiert.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="0c2a9-125">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0c2a9-126">Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0c2a9-127">Diese Funktion interpoliert die Rot-, Grün- und Blaufarbkomponenten einer [**D3DXCOLOR-Struktur**](d3dxcolor.md) zwischen einer nicht überschäumten Farbe und einer Farbe, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-127">This function interpolates the red, green, and blue color components of a [**D3DXCOLOR**](d3dxcolor.md) structure between an unsaturated color and a color, as shown in the following example.</span></span>


```
    // Approximate values for each component's contribution to luminance.
    // Based upon the NTSC standard described in ITU-R Recommendation BT.709.
    FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;
    
    pOut->r = grey + s * (pC->r - grey);
```



<span data-ttu-id="0c2a9-128">Wenn s größer als 0 und kleiner als 1 ist, wird die Sättigung verringert.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-128">If s is greater than 0 and less than 1, the saturation is decreased.</span></span> <span data-ttu-id="0c2a9-129">Wenn s größer als 1 ist, wird die Sättigung erhöht.</span><span class="sxs-lookup"><span data-stu-id="0c2a9-129">If s is greater than 1, the saturation is increased.</span></span>

<span data-ttu-id="0c2a9-130">Die Graustufenfarbe wird wie die folgenden berechnet:</span><span class="sxs-lookup"><span data-stu-id="0c2a9-130">The grayscale color is computed as:</span></span>


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b
```



## <a name="requirements"></a><span data-ttu-id="0c2a9-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c2a9-131">Requirements</span></span>



| <span data-ttu-id="0c2a9-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c2a9-132">Requirement</span></span> | <span data-ttu-id="0c2a9-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0c2a9-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c2a9-134">Header</span><span class="sxs-lookup"><span data-stu-id="0c2a9-134">Header</span></span><br/>  | <dl> <span data-ttu-id="0c2a9-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0c2a9-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0c2a9-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c2a9-136">Library</span></span><br/> | <dl> <span data-ttu-id="0c2a9-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c2a9-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0c2a9-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0c2a9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c2a9-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="0c2a9-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0c2a9-140">**D3DXColorAdjustContrast**</span><span class="sxs-lookup"><span data-stu-id="0c2a9-140">**D3DXColorAdjustContrast**</span></span>](d3dxcoloradjustcontrast.md)
</dt> </dl>

 

 
