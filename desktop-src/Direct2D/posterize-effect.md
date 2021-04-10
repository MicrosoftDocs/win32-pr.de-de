---
title: Auswirkung auf die Folge
description: Der folgeeffekt reduziert die Anzahl der eindeutigen Farben in einem Bild.
ms.assetid: e6686998-1246-b3b7-6f4f-212568c3191c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c98c55154300f7b29c23c24e97570335c6e930f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040781"
---
# <a name="posterize-effect"></a><span data-ttu-id="da117-103">Auswirkung auf die Folge</span><span class="sxs-lookup"><span data-stu-id="da117-103">Posterize effect</span></span>

<span data-ttu-id="da117-104">Der folgeeffekt reduziert die Anzahl der eindeutigen Farben in einem Bild.</span><span class="sxs-lookup"><span data-stu-id="da117-104">The posterize effect reduces the number of unique colors in an image.</span></span>

<span data-ttu-id="da117-105">Die CLSID für diesen Effekt ist CLSID \_ D2D1Posterize.</span><span class="sxs-lookup"><span data-stu-id="da117-105">The CLSID for this effect is CLSID\_D2D1Posterize.</span></span>

-   [<span data-ttu-id="da117-106">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="da117-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="da117-107">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="da117-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="da117-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da117-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="da117-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da117-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="da117-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="da117-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="da117-111">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="da117-111">Example image</span></span>

![Beispiel für Effekte Ausgabe](images/posterize-effect.png)

## <a name="sample-code"></a><span data-ttu-id="da117-113">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="da117-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> posterizeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Posterize, &posterizeEffect);
 
posterizeEffect->SetInput(0, bitmap);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_RED_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT, 4);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(posterizeEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="da117-114">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da117-114">Effect properties</span></span>

<span data-ttu-id="da117-115">Die Eigenschaften für den folgeeffekt werden durch die D2D1- [**unter \_ Stützung der \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="da117-115">The properties for the posterize effect are defined by the [**D2D1\_POSTERIZE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="da117-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da117-116">Requirements</span></span>



| <span data-ttu-id="da117-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da117-117">Requirement</span></span> | <span data-ttu-id="da117-118">Wert</span><span class="sxs-lookup"><span data-stu-id="da117-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="da117-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da117-119">Minimum supported client</span></span> | <span data-ttu-id="da117-120">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da117-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="da117-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da117-121">Minimum supported server</span></span> | <span data-ttu-id="da117-122">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da117-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="da117-123">Header</span><span class="sxs-lookup"><span data-stu-id="da117-123">Header</span></span>                   | <span data-ttu-id="da117-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="da117-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="da117-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="da117-125">Library</span></span>                  | <span data-ttu-id="da117-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="da117-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="da117-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="da117-127">Related topics</span></span>

* [<span data-ttu-id="da117-128">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="da117-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)


