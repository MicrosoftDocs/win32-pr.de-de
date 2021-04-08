---
title: Schärfe Effekt
description: Zeichnet das Bild mit einem Sharding.
ms.assetid: 1eb12d1e-83c1-ba13-33be-df2078f3ccb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54203cfeb786204500c905e2ff4cfc83bf9719e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741177"
---
# <a name="sharpen-effect"></a><span data-ttu-id="23a15-103">Schärfe Effekt</span><span class="sxs-lookup"><span data-stu-id="23a15-103">Sharpen effect</span></span>

<span data-ttu-id="23a15-104">Zeichnet das Bild mit einem Sharding.</span><span class="sxs-lookup"><span data-stu-id="23a15-104">Sharpens the image.</span></span>

<span data-ttu-id="23a15-105">Die CLSID für diesen Effekt ist CLSID \_ D2D1Sharpen.</span><span class="sxs-lookup"><span data-stu-id="23a15-105">The CLSID for this effect is CLSID\_D2D1Sharpen.</span></span>

-   [<span data-ttu-id="23a15-106">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="23a15-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="23a15-107">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="23a15-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="23a15-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23a15-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="23a15-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23a15-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="23a15-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23a15-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="23a15-111">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="23a15-111">Example image</span></span>

![Beispiel für Effekte Ausgabe](images/sharpen-effect.png)

## <a name="sample-code"></a><span data-ttu-id="23a15-113">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="23a15-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sharpenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sharpen, &sharpenEffect);
 
sharpenEffect->SetInput(0, bitmap);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_SHARPNESS, 1.0f);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_THRESHOLD, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="23a15-114">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23a15-114">Effect properties</span></span>

<span data-ttu-id="23a15-115">Die Eigenschaften für den schärfeffekt werden von der [**D2D1 \_ Sharpen \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="23a15-115">The properties for the sharpen effect are defined by the [**D2D1\_SHARPEN\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="23a15-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23a15-116">Requirements</span></span>



| <span data-ttu-id="23a15-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23a15-117">Requirement</span></span> | <span data-ttu-id="23a15-118">Wert</span><span class="sxs-lookup"><span data-stu-id="23a15-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="23a15-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23a15-119">Minimum supported client</span></span> | <span data-ttu-id="23a15-120">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23a15-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="23a15-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23a15-121">Minimum supported server</span></span> | <span data-ttu-id="23a15-122">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23a15-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="23a15-123">Header</span><span class="sxs-lookup"><span data-stu-id="23a15-123">Header</span></span>                   | <span data-ttu-id="23a15-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="23a15-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="23a15-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="23a15-125">Library</span></span>                  | <span data-ttu-id="23a15-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="23a15-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="23a15-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23a15-127">Related topics</span></span>

* [<span data-ttu-id="23a15-128">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="23a15-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)



