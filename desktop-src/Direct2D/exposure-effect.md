---
title: Expositions Effekt
description: Vergrößern oder verringern Sie die Darstellung des Bilds.
ms.assetid: d384f539-5c19-53c7-e52b-bf833e221449
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6f5bda52fecc0b5e3896515b04a6560f17da49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956853"
---
# <a name="exposure-effect"></a><span data-ttu-id="2c7fb-103">Expositions Effekt</span><span class="sxs-lookup"><span data-stu-id="2c7fb-103">Exposure effect</span></span>

<span data-ttu-id="2c7fb-104">Vergrößern oder verringern Sie die Darstellung des Bilds.</span><span class="sxs-lookup"><span data-stu-id="2c7fb-104">Increase or decreases the exposure of the image.</span></span>

<span data-ttu-id="2c7fb-105">Die CLSID für diesen Effekt ist CLSID \_ D2D1Exposure.</span><span class="sxs-lookup"><span data-stu-id="2c7fb-105">The CLSID for this effect is CLSID\_D2D1Exposure.</span></span>

-   [<span data-ttu-id="2c7fb-106">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="2c7fb-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="2c7fb-107">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="2c7fb-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="2c7fb-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c7fb-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="2c7fb-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c7fb-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2c7fb-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2c7fb-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="2c7fb-111">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="2c7fb-111">Example image</span></span>

![Beispiel für Effekte Ausgabe](images/exposure-effect.png)

## <a name="sample-code"></a><span data-ttu-id="2c7fb-113">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="2c7fb-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> exposureEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Exposure, &exposureEffect);
 
exposureEffect->SetInput(0, bitmap);
exposureEffect->SetValue(D2D1_EXPOSURE_PROP_EXPOSURE_VALUE, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(exposureEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="2c7fb-114">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c7fb-114">Effect properties</span></span>

<span data-ttu-id="2c7fb-115">Die Eigenschaften für den Expositions Effekt werden durch die [**D2D1 \_ Exposure \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="2c7fb-115">The properties for the exposure effect are defined by the [**D2D1\_EXPOSURE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c7fb-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c7fb-116">Requirements</span></span>



| <span data-ttu-id="2c7fb-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c7fb-117">Requirement</span></span> | <span data-ttu-id="2c7fb-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2c7fb-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="2c7fb-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c7fb-119">Minimum supported client</span></span> | <span data-ttu-id="2c7fb-120">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c7fb-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2c7fb-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c7fb-121">Minimum supported server</span></span> | <span data-ttu-id="2c7fb-122">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c7fb-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2c7fb-123">Header</span><span class="sxs-lookup"><span data-stu-id="2c7fb-123">Header</span></span>                   | <span data-ttu-id="2c7fb-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="2c7fb-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="2c7fb-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2c7fb-125">Library</span></span>                  | <span data-ttu-id="2c7fb-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="2c7fb-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="2c7fb-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2c7fb-127">Related topics</span></span>

* [<span data-ttu-id="2c7fb-128">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2c7fb-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




