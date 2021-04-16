---
title: Highlights und Schatteneffekte
description: Passt die Highlights und Schatten des Bilds an.
ms.assetid: ebbb7d99-9144-ffff-af73-d89e7d269924
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d595a5b82a2df0b0b0bab14c03e6a807511ed61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104562388"
---
# <a name="highlights-and-shadows-effect"></a><span data-ttu-id="b3eb7-103">Highlights und Schatteneffekte</span><span class="sxs-lookup"><span data-stu-id="b3eb7-103">Highlights and shadows effect</span></span>

<span data-ttu-id="b3eb7-104">Passt die Highlights und Schatten des Bilds an.</span><span class="sxs-lookup"><span data-stu-id="b3eb7-104">Adjusts the highlights and shadows of the image.</span></span>

<span data-ttu-id="b3eb7-105">Die CLSID für diesen Effekt ist CLSID \_ D2D1HighlightsShadows.</span><span class="sxs-lookup"><span data-stu-id="b3eb7-105">The CLSID for this effect is CLSID\_D2D1HighlightsShadows.</span></span>

-   [<span data-ttu-id="b3eb7-106">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="b3eb7-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="b3eb7-107">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="b3eb7-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="b3eb7-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3eb7-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="b3eb7-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3eb7-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b3eb7-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3eb7-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="b3eb7-111">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="b3eb7-111">Example image</span></span>

![Beispiel für Effekte Ausgabe](images/highlights-and-shadows-effect.png)

## <a name="sample-code"></a><span data-ttu-id="b3eb7-113">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="b3eb7-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> highlightsAndShadowsEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HighlightsShadows, &highlightsAndShadowsEffect);
 
highlightsAndShadowsEffect->SetInput(0, bitmap);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS, 0.0f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS, 0.5f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY, 0.2f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA, D2D1_HIGHLIGHTSANDSHADOWS_INPUT_GAMMA_LINEAR);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="b3eb7-114">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3eb7-114">Effect properties</span></span>

<span data-ttu-id="b3eb7-115">Die Eigenschaften für den Hervorhebungen und den Schatteneffekt werden von der [**D2D1 \_ highlighnerandshadows- \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="b3eb7-115">The properties for the highlights and shadows effect are defined by the [**D2D1\_HIGHLIGHTSANDSHADOWS\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3eb7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3eb7-116">Requirements</span></span>

| <span data-ttu-id="b3eb7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3eb7-117">Requirement</span></span> | <span data-ttu-id="b3eb7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b3eb7-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="b3eb7-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3eb7-119">Minimum supported client</span></span> | <span data-ttu-id="b3eb7-120">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3eb7-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b3eb7-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3eb7-121">Minimum supported server</span></span> | <span data-ttu-id="b3eb7-122">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3eb7-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b3eb7-123">Header</span><span class="sxs-lookup"><span data-stu-id="b3eb7-123">Header</span></span>                   | <span data-ttu-id="b3eb7-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="b3eb7-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="b3eb7-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b3eb7-125">Library</span></span>                  | <span data-ttu-id="b3eb7-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b3eb7-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="b3eb7-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3eb7-127">Related topics</span></span>

* [<span data-ttu-id="b3eb7-128">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b3eb7-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
