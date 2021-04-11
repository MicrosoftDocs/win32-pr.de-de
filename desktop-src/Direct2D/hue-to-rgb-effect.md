---
title: Hue-zu-RGB-Effekt
description: Konvertiert ein Bild vom Typ HSL (Hue, Sättigung, Helligkeit) oder HSV (Farbton, Sättigung, Wert) in den RGB-Farbraum.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82064d01281ab0edf2327f00cf6e852a0bebae53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949808"
---
# <a name="hue-to-rgb-effect"></a><span data-ttu-id="14da7-103">Hue-zu-RGB-Effekt</span><span class="sxs-lookup"><span data-stu-id="14da7-103">Hue-to-RGB effect</span></span>

<span data-ttu-id="14da7-104">Konvertiert ein Bild vom Typ HSL (Hue, Sättigung, Helligkeit) oder HSV (Farbton, Sättigung, Wert) in den RGB-Farbraum.</span><span class="sxs-lookup"><span data-stu-id="14da7-104">Converts an HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) image to the RGB color space.</span></span>

<span data-ttu-id="14da7-105">HSL und HSV sind zwei verschiedene Modelle für die Darstellung einer RGB-Farbe in einem zylindrischen Farbraum.</span><span class="sxs-lookup"><span data-stu-id="14da7-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="14da7-106">Sie sind nützlich, da Sie eine Farbe mit intuitiveren Konzepten wie Hue und Intensität und Kombinieren von roten, grünen und blauen Werten haben können.</span><span class="sxs-lookup"><span data-stu-id="14da7-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="14da7-107">Dieser Effekt durchläuft alle eingegebenen Alpha Werte.</span><span class="sxs-lookup"><span data-stu-id="14da7-107">This effect passes through any input alpha values.</span></span>

<span data-ttu-id="14da7-108">Die CLSID für diesen Effekt ist CLSID \_ D2D1HueToRgb.</span><span class="sxs-lookup"><span data-stu-id="14da7-108">The CLSID for this effect is CLSID\_D2D1HueToRgb.</span></span>

<span data-ttu-id="14da7-109">Um das Verhalten dieses Effekts umzukehren, verwenden Sie den [RGB-Effekt](rgb-to-hue-effect.md).</span><span class="sxs-lookup"><span data-stu-id="14da7-109">To reverse the behavior of this effect, use the [RGB to Hue effect](rgb-to-hue-effect.md).</span></span>

-   [<span data-ttu-id="14da7-110">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="14da7-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="14da7-111">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14da7-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="14da7-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14da7-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="14da7-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="14da7-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="14da7-114">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="14da7-114">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="14da7-115">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14da7-115">Effect properties</span></span>

<span data-ttu-id="14da7-116">Die Eigenschaften für den Kontrast Effekt werden von der [**D2D1 \_ huetorgb- \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="14da7-116">The properties for the contrast effect are defined by the [**D2D1\_HUETORGB\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="14da7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14da7-117">Requirements</span></span>



| <span data-ttu-id="14da7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14da7-118">Requirement</span></span> | <span data-ttu-id="14da7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="14da7-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="14da7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14da7-120">Minimum supported client</span></span> | <span data-ttu-id="14da7-121">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14da7-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="14da7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14da7-122">Minimum supported server</span></span> | <span data-ttu-id="14da7-123">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14da7-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="14da7-124">Header</span><span class="sxs-lookup"><span data-stu-id="14da7-124">Header</span></span>                   | <span data-ttu-id="14da7-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="14da7-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="14da7-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="14da7-126">Library</span></span>                  | <span data-ttu-id="14da7-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="14da7-127">d2d1.lib, dxguid.lib</span></span>                              |



## <a name="related-topics"></a><span data-ttu-id="14da7-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="14da7-128">Related topics</span></span>

* [<span data-ttu-id="14da7-129">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="14da7-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
