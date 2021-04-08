---
title: Emboss-Effekt
description: Erstellt eine Graustufen Version des Bilds, das angezeigt wird, als ob es in Papier gestempelt wurde.
ms.assetid: 74f63875-35cd-f335-62cd-410a953e53ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dde087eb7f85fcd68615c39730bf6208024fc43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741536"
---
# <a name="emboss-effect"></a><span data-ttu-id="0d4de-103">Emboss-Effekt</span><span class="sxs-lookup"><span data-stu-id="0d4de-103">Emboss effect</span></span>

<span data-ttu-id="0d4de-104">Erstellt eine Graustufen Version des Bilds, das angezeigt wird, als ob es in Papier gestempelt wurde.</span><span class="sxs-lookup"><span data-stu-id="0d4de-104">Creates a grayscale version of the image that appears as though it has been stamped into paper.</span></span>

<span data-ttu-id="0d4de-105">Die CLSID für diesen Effekt ist CLSID \_ D2D1Emboss.</span><span class="sxs-lookup"><span data-stu-id="0d4de-105">The CLSID for this effect is CLSID\_D2D1Emboss.</span></span>

-   [<span data-ttu-id="0d4de-106">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="0d4de-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="0d4de-107">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="0d4de-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="0d4de-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0d4de-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="0d4de-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d4de-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0d4de-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d4de-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="0d4de-111">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="0d4de-111">Example image</span></span>

![Beispiel für Effekte Ausgabe](images/emboss-effect.png)

## <a name="sample-code"></a><span data-ttu-id="0d4de-113">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="0d4de-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> embossEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Emboss, &embossEffect);
 
embossEffect->SetInput(0, bitmap);
embossEffect->SetValue(D2D1_EMBOSS_PROP_HEIGHT, 1.0f);
embossEffect->SetValue(D2D1_EMBOSS_PROP_DIRECTION, 0.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(embossEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="0d4de-114">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0d4de-114">Effect properties</span></span>

<span data-ttu-id="0d4de-115">Die Eigenschaften des Prägung-Effekts werden von der [**D2D1 \_ Prägung- \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="0d4de-115">The properties for the emboss effect are defined by the [**D2D1\_EMBOSS\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d4de-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d4de-116">Requirements</span></span>



| <span data-ttu-id="0d4de-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d4de-117">Requirement</span></span> | <span data-ttu-id="0d4de-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0d4de-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="0d4de-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d4de-119">Minimum supported client</span></span> | <span data-ttu-id="0d4de-120">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d4de-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0d4de-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d4de-121">Minimum supported server</span></span> | <span data-ttu-id="0d4de-122">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d4de-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0d4de-123">Header</span><span class="sxs-lookup"><span data-stu-id="0d4de-123">Header</span></span>                   | <span data-ttu-id="0d4de-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="0d4de-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="0d4de-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0d4de-125">Library</span></span>                  | <span data-ttu-id="0d4de-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="0d4de-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="0d4de-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d4de-127">Related topics</span></span>

* [<span data-ttu-id="0d4de-128">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0d4de-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
