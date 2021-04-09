---
title: Edge-Erkennungs Effekt
description: Filtert den Inhalt eines Bilds heraus und verlässt die Zeilen an den Rändern der kontrastreichen Abschnitte des Bilds.
ms.assetid: d22868cf-95fe-690e-66ac-268d7e116aee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47239bede77dc5d32582c6e83c8101e5c9bbf2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041009"
---
# <a name="edge-detection-effect"></a><span data-ttu-id="56be9-103">Edge-Erkennungs Effekt</span><span class="sxs-lookup"><span data-stu-id="56be9-103">Edge-detection effect</span></span>

<span data-ttu-id="56be9-104">Filtert den Inhalt eines Bilds heraus und verlässt die Zeilen an den Rändern der kontrastreichen Abschnitte des Bilds.</span><span class="sxs-lookup"><span data-stu-id="56be9-104">Filters out the content of an image, leaving lines at the edges of contrasting sections of the image.</span></span>

<span data-ttu-id="56be9-105">Die CLSID für diesen Effekt ist CLSID \_ D2D1EdgeDetection.</span><span class="sxs-lookup"><span data-stu-id="56be9-105">The CLSID for this effect is CLSID\_D2D1EdgeDetection.</span></span>

-   [<span data-ttu-id="56be9-106">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="56be9-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="56be9-107">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="56be9-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="56be9-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="56be9-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="56be9-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56be9-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="56be9-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56be9-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="56be9-111">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="56be9-111">Example image</span></span>

![Beispiel für Effekte Ausgabe](images/edge-detection-effect.png)

## <a name="sample-code"></a><span data-ttu-id="56be9-113">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="56be9-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> edgeDetectionEffect;
m_d2dContext->CreateEffect(CLSID_D2D1EdgeDetection, &edgeDetectionEffect);
 
edgeDetectionEffect->SetInput(0, bitmap);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_STRENGTH, 0.5f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_BLUR_RADIUS, 0.0f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_MODE, D2D1_EDGEDETECTION_MODE_SOBEL);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES, false);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(edgeDetectionEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="56be9-114">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="56be9-114">Effect properties</span></span>

<span data-ttu-id="56be9-115">Die Eigenschaften für den Edge-Erkennungs Effekt werden von der [**D2D1 \_ edgeerkennungs- \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="56be9-115">The properties for the edge detection effect are defined by the [**D2D1\_EDGEDETECTION\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="56be9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56be9-116">Requirements</span></span>



| <span data-ttu-id="56be9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56be9-117">Requirement</span></span> | <span data-ttu-id="56be9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="56be9-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="56be9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56be9-119">Minimum supported client</span></span> | <span data-ttu-id="56be9-120">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56be9-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="56be9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56be9-121">Minimum supported server</span></span> | <span data-ttu-id="56be9-122">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56be9-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="56be9-123">Header</span><span class="sxs-lookup"><span data-stu-id="56be9-123">Header</span></span>                   | <span data-ttu-id="56be9-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="56be9-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="56be9-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56be9-125">Library</span></span>                  | <span data-ttu-id="56be9-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="56be9-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="56be9-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56be9-127">Related topics</span></span>

* [<span data-ttu-id="56be9-128">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="56be9-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
