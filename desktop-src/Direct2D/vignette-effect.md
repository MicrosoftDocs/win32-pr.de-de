---
title: Vigffekt
description: Blendet das Eingabebild an den Rändern in eine Benutzer Satz Farbe aus.
ms.assetid: 34da221f-44a2-1d01-d88d-d7846b9770b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3fe9302a86a49b060aa05ecb856ce43122d946d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104936"
---
# <a name="vignette-effect"></a><span data-ttu-id="75b2c-103">Vigffekt</span><span class="sxs-lookup"><span data-stu-id="75b2c-103">Vignette effect</span></span>

<span data-ttu-id="75b2c-104">Blendet das Eingabebild an den Rändern in eine Benutzer Satz Farbe aus.</span><span class="sxs-lookup"><span data-stu-id="75b2c-104">Fades the input image at the edges to a user-set color.</span></span>

<span data-ttu-id="75b2c-105">Die CLSID für diesen Effekt ist CLSID \_ D2D1Vignette.</span><span class="sxs-lookup"><span data-stu-id="75b2c-105">The CLSID for this effect is CLSID\_D2D1Vignette.</span></span>

-   [<span data-ttu-id="75b2c-106">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="75b2c-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="75b2c-107">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="75b2c-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="75b2c-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="75b2c-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="75b2c-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75b2c-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="75b2c-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75b2c-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="75b2c-111">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="75b2c-111">Example image</span></span>

![Beispiel für Effekte Ausgabe](images/vignette-effect.png)

## <a name="sample-code"></a><span data-ttu-id="75b2c-113">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="75b2c-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> vignetteEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Vignette, &vignetteEffect);
 
vignetteEffect->SetInput(0, bitmap);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_COLOR, );
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_TRANSITION_SIZE, 0.1f);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_STRENGTH, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(vignetteEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="75b2c-114">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="75b2c-114">Effect properties</span></span>

<span data-ttu-id="75b2c-115">Die Eigenschaften für den vigaseeffekt werden durch die [**D2D1- \_ Vignette- \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="75b2c-115">The properties for the vignette effect are defined by the [**D2D1\_VIGNETTE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b2c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75b2c-116">Requirements</span></span>

| <span data-ttu-id="75b2c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75b2c-117">Requirement</span></span> | <span data-ttu-id="75b2c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="75b2c-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="75b2c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75b2c-119">Minimum supported client</span></span> | <span data-ttu-id="75b2c-120">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75b2c-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="75b2c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75b2c-121">Minimum supported server</span></span> | <span data-ttu-id="75b2c-122">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75b2c-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="75b2c-123">Header</span><span class="sxs-lookup"><span data-stu-id="75b2c-123">Header</span></span>                   | <span data-ttu-id="75b2c-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="75b2c-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="75b2c-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="75b2c-125">Library</span></span>                  | <span data-ttu-id="75b2c-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="75b2c-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="75b2c-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75b2c-127">Related topics</span></span>

* [<span data-ttu-id="75b2c-128">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="75b2c-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
