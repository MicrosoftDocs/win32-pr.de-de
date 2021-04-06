---
title: Chroma-Schlüssel Effekt
description: Konvertiert eine angegebene Farbe plus oder minus eine Toleranz in alpha. Beispielsweise kann Chroma-Key den Hintergrund eines Bilds für einen Überlagerungs Effekt mit grünes Bildschirm entfernen.
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a13d5558d103d6f937ed6638d0debbeddaf71dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858812"
---
# <a name="chroma-key-effect"></a><span data-ttu-id="5359b-104">Chroma-Schlüssel Effekt</span><span class="sxs-lookup"><span data-stu-id="5359b-104">Chroma-key effect</span></span>

<span data-ttu-id="5359b-105">Konvertiert eine angegebene Farbe plus oder minus eine Toleranz in alpha.</span><span class="sxs-lookup"><span data-stu-id="5359b-105">Converts a given color plus or minus a tolerance to alpha.</span></span> <span data-ttu-id="5359b-106">Beispielsweise kann Chroma-Key den Hintergrund eines Bilds für einen Überlagerungs Effekt mit grünes Bildschirm entfernen.</span><span class="sxs-lookup"><span data-stu-id="5359b-106">For example, chroma-key can remove the background of an image for a green-screen overlay effect.</span></span>

<span data-ttu-id="5359b-107">Die CLSID für diesen Effekt ist CLSID \_ D2D1ChromaKey.</span><span class="sxs-lookup"><span data-stu-id="5359b-107">The CLSID for this effect is CLSID\_D2D1ChromaKey.</span></span>

-   [<span data-ttu-id="5359b-108">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="5359b-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="5359b-109">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="5359b-109">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="5359b-110">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5359b-110">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="5359b-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5359b-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5359b-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5359b-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="5359b-113">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="5359b-113">Example image</span></span>

![Beispiel für Effekte Ausgabe](images/chromakey-effect.png)

> [!Note]  
> <span data-ttu-id="5359b-115">In diesem Beispiel ist die Ausgabe des Chroma-Key-Effekts das zweite Bild mit dem transparenten Hintergrund des checkboards.</span><span class="sxs-lookup"><span data-stu-id="5359b-115">In this example, the output of the chroma-key effect is the second image with the checkerboard transparent background.</span></span> <span data-ttu-id="5359b-116">Das dritte Bild kombiniert dies mit einem Hintergrundbild für den abschließenden grünen Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="5359b-116">The third image combines this with a background image for the final green-screen overlay.</span></span>

## <a name="sample-code"></a><span data-ttu-id="5359b-117">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="5359b-117">Sample code</span></span>

```cppcx
ComPtr<ID2D1Effect> chromakeyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ChromaKey, &chromakeyEffect);
 
chromakeyEffect->SetInput(0, bitmap);
chromaKeyEffect->SetValue(D2D1_CHROMAKEY_PROP_COLOR, {0.0f, 1.0f, 0.0f, 0.0f});
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_TOLERANCE, 0.2f);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_INVERT_ALPHA, false);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_FEATHER, false);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(chromakeyEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="5359b-118">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5359b-118">Effect properties</span></span>

<span data-ttu-id="5359b-119">Die Eigenschaften des Chroma-Key-Effekts werden von der [**D2D1 \_ Chromakey- \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="5359b-119">The properties for the chroma-key effect are defined by the [**D2D1\_CHROMAKEY\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="5359b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5359b-120">Requirements</span></span>

| <span data-ttu-id="5359b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5359b-121">Requirement</span></span> | <span data-ttu-id="5359b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5359b-122">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="5359b-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5359b-123">Minimum supported client</span></span> | <span data-ttu-id="5359b-124">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5359b-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5359b-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5359b-125">Minimum supported server</span></span> | <span data-ttu-id="5359b-126">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5359b-126">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5359b-127">Header</span><span class="sxs-lookup"><span data-stu-id="5359b-127">Header</span></span>                   | <span data-ttu-id="5359b-128">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="5359b-128">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="5359b-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5359b-129">Library</span></span>                  | <span data-ttu-id="5359b-130">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="5359b-130">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="5359b-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5359b-131">Related topics</span></span>

* [<span data-ttu-id="5359b-132">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5359b-132">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
