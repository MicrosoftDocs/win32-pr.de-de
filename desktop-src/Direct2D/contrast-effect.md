---
title: Kontrast Effekt
description: Erhöht oder verringert den Kontrast eines Bilds.
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040716"
---
# <a name="contrast-effect"></a><span data-ttu-id="e7328-103">Kontrast Effekt</span><span class="sxs-lookup"><span data-stu-id="e7328-103">Contrast effect</span></span>

<span data-ttu-id="e7328-104">Erhöht oder verringert den Kontrast eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="e7328-104">Increases or decreases the contrast of an image.</span></span>

<span data-ttu-id="e7328-105">Die CLSID für diesen Effekt ist CLSID \_ D2D1Contrast.</span><span class="sxs-lookup"><span data-stu-id="e7328-105">The CLSID for this effect is CLSID\_D2D1Contrast.</span></span>

<span data-ttu-id="e7328-106">Die Funktion "Kontrast" ändert jeden farbchannelwert mithilfe von zwei, schrittweisen, quadratischen Polynomen, die mit der Neigungs Kontinuität am Punkt (0,5, 0,5) übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7328-106">The contrast function modifies each color channel value using two, piecewise quadratic polynomials that meet with slope continuity at the point (0.5, 0.5).</span></span>

![schrittweise quadratische Polynomen, die mit der Neigungs Kontinuität an der Stelle (0,5, 0,5) erfüllen](images/contrast-effect-slope.png)

-   [<span data-ttu-id="e7328-108">Beispiel Bilder</span><span class="sxs-lookup"><span data-stu-id="e7328-108">Example Images</span></span>](#example-images)
-   [<span data-ttu-id="e7328-109">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="e7328-109">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="e7328-110">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7328-110">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="e7328-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7328-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e7328-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e7328-112">Related topics</span></span>](#related-topics)

## <a name="example-images"></a><span data-ttu-id="e7328-113">Beispiel Bilder</span><span class="sxs-lookup"><span data-stu-id="e7328-113">Example images</span></span>

<span data-ttu-id="e7328-114">Dieses Beispiel zeigt die Ausgabe des Effekts mit angewendetem maximalem Kontrast (Kontrast = 1,0).</span><span class="sxs-lookup"><span data-stu-id="e7328-114">This example shows the output of the effect with maximum contrast applied (Contrast = 1.0).</span></span>

<span data-ttu-id="e7328-115">Vorher</span><span class="sxs-lookup"><span data-stu-id="e7328-115">Before</span></span>

![Bild vor Auswirkung wird angewendet](images/contrast-effect-before.png)

<span data-ttu-id="e7328-117">Nach</span><span class="sxs-lookup"><span data-stu-id="e7328-117">After</span></span>

![Bild nach dem Anwenden der Auswirkung](images/contrast-effect-after.png)

## <a name="sample-code"></a><span data-ttu-id="e7328-119">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="e7328-119">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> contrastEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Contrast, &contrastEffect);
 
contrastEffect->SetInput(0, bitmap);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CONTRAST, 0.5f);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CLAMP_INPUT, TRUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(contrastEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="e7328-120">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7328-120">Effect properties</span></span>

<span data-ttu-id="e7328-121">Die Eigenschaften für den Kontrast Effekt werden durch die [**\_ \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) -Enumeration D2D1 Kontraste definiert.</span><span class="sxs-lookup"><span data-stu-id="e7328-121">The properties for the contrast effect are defined by the [**D2D1\_CONTRAST\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7328-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7328-122">Requirements</span></span>

| <span data-ttu-id="e7328-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7328-123">Requirement</span></span> | <span data-ttu-id="e7328-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e7328-124">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="e7328-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7328-125">Minimum supported client</span></span> | <span data-ttu-id="e7328-126">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7328-126">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e7328-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7328-127">Minimum supported server</span></span> | <span data-ttu-id="e7328-128">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7328-128">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e7328-129">Header</span><span class="sxs-lookup"><span data-stu-id="e7328-129">Header</span></span>                   | <span data-ttu-id="e7328-130">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="e7328-130">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="e7328-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7328-131">Library</span></span>                  | <span data-ttu-id="e7328-132">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="e7328-132">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="e7328-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e7328-133">Related topics</span></span>

* [<span data-ttu-id="e7328-134">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e7328-134">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
