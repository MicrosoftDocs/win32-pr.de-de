---
title: RGB-zu-Hue-Effekt
description: Konvertiert ein RGB-Bild in die Farbbereiche HSL (Hue, Sättigung, Helligkeit) oder HSV (Farbton, Sättigung, Wert).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ccb4d3f67d116426d7a3497c04c4e8fb115b74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391828"
---
# <a name="rgb-to-hue-effect"></a><span data-ttu-id="0a734-103">RGB-zu-Hue-Effekt</span><span class="sxs-lookup"><span data-stu-id="0a734-103">RGB-to-hue effect</span></span>

<span data-ttu-id="0a734-104">Konvertiert ein RGB-Bild in die Farbbereiche HSL (Hue, Sättigung, Helligkeit) oder HSV (Farbton, Sättigung, Wert).</span><span class="sxs-lookup"><span data-stu-id="0a734-104">Converts an RGB image to either the HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) color spaces.</span></span>

<span data-ttu-id="0a734-105">HSL und HSV sind zwei verschiedene Modelle für die Darstellung einer RGB-Farbe in einem zylindrischen Farbraum.</span><span class="sxs-lookup"><span data-stu-id="0a734-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="0a734-106">Sie sind nützlich, da Sie eine Farbe mit intuitiveren Konzepten wie Hue und Intensität und Kombinieren von roten, grünen und blauen Werten haben können.</span><span class="sxs-lookup"><span data-stu-id="0a734-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="0a734-107">Dieser Effekt normalisiert die Ausgabedaten (Hue, Sättigungswert für HSV, Hue, Sättigung, Helligkeit für HSL) in den Bereich \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="0a734-107">This effect normalizes the output data (hue, saturation value for HSV or hue, saturation, lightness for HSL) to the range \[0, 1\].</span></span>

<span data-ttu-id="0a734-108">Die CLSID für diesen Effekt ist CLSID \_ D2D1RgbToHue.</span><span class="sxs-lookup"><span data-stu-id="0a734-108">The CLSID for this effect is CLSID\_D2D1RgbToHue.</span></span>

<span data-ttu-id="0a734-109">Um das Verhalten dieses Effekts umzukehren, verwenden Sie den [Effekt Hue in RGB](hue-to-rgb-effect.md).</span><span class="sxs-lookup"><span data-stu-id="0a734-109">To reverse the behavior of this effect, use the [Hue to RGB effect](hue-to-rgb-effect.md).</span></span>

-   [<span data-ttu-id="0a734-110">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="0a734-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="0a734-111">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a734-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="0a734-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a734-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0a734-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0a734-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="0a734-114">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="0a734-114">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a><span data-ttu-id="0a734-115">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a734-115">Effect properties</span></span>

<span data-ttu-id="0a734-116">Die Eigenschaften für den Kontrast Effekt werden durch die [**D2D1 \_ rgbflhue \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="0a734-116">The properties for the contrast effect are defined by the [**D2D1\_RGBTOHUE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a734-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a734-117">Requirements</span></span>



| <span data-ttu-id="0a734-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a734-118">Requirement</span></span> | <span data-ttu-id="0a734-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0a734-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="0a734-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a734-120">Minimum supported client</span></span> | <span data-ttu-id="0a734-121">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a734-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0a734-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a734-122">Minimum supported server</span></span> | <span data-ttu-id="0a734-123">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a734-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0a734-124">Header</span><span class="sxs-lookup"><span data-stu-id="0a734-124">Header</span></span>                   | <span data-ttu-id="0a734-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="0a734-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="0a734-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0a734-126">Library</span></span>                  | <span data-ttu-id="0a734-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="0a734-127">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="0a734-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0a734-128">Related topics</span></span>

* [<span data-ttu-id="0a734-129">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0a734-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
