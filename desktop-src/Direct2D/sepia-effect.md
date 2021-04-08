---
title: '* Pia-Effekt'
description: Konvertiert ein Bild in Sepiatöne.
ms.assetid: fe321be9-6ade-bd0c-1c66-cc8042e5a5e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6ead1d439e86cbd35be14d1f0ae32923de408d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949760"
---
# <a name="sepia-effect"></a><span data-ttu-id="74837-103">\* Pia-Effekt</span><span class="sxs-lookup"><span data-stu-id="74837-103">Sepia effect</span></span>

<span data-ttu-id="74837-104">Konvertiert ein Bild in Sepiatöne.</span><span class="sxs-lookup"><span data-stu-id="74837-104">Converts an image to sepia tones.</span></span>

<span data-ttu-id="74837-105">Die CLSID für diesen Effekt ist CLSID \_ D2D1Sepia.</span><span class="sxs-lookup"><span data-stu-id="74837-105">The CLSID for this effect is CLSID\_D2D1Sepia.</span></span>

-   [<span data-ttu-id="74837-106">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="74837-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="74837-107">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="74837-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="74837-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74837-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="74837-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74837-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="74837-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="74837-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="74837-111">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="74837-111">Example image</span></span>

![Beispiel für Effekte Ausgabe](images/sepia-effect.png)

## <a name="sample-code"></a><span data-ttu-id="74837-113">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="74837-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sepiaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sepia, &sepiaEffect);
 
sepiaEffect->SetInput(0, bitmap);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_INTENSITY, 0.75f);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(sepiaEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="74837-114">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74837-114">Effect properties</span></span>

<span data-ttu-id="74837-115">Die Eigenschaften für den "\*"-Effekt werden durch [**die \_ \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) -Enumeration "D2D1" definiert.</span><span class="sxs-lookup"><span data-stu-id="74837-115">The properties for the sepia effect are defined by the [**D2D1\_SEPIA\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="74837-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74837-116">Requirements</span></span>



| <span data-ttu-id="74837-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74837-117">Requirement</span></span> | <span data-ttu-id="74837-118">Wert</span><span class="sxs-lookup"><span data-stu-id="74837-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="74837-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74837-119">Minimum supported client</span></span> | <span data-ttu-id="74837-120">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74837-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="74837-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74837-121">Minimum supported server</span></span> | <span data-ttu-id="74837-122">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74837-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="74837-123">Header</span><span class="sxs-lookup"><span data-stu-id="74837-123">Header</span></span>                   | <span data-ttu-id="74837-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="74837-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="74837-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="74837-125">Library</span></span>                  | <span data-ttu-id="74837-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="74837-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="74837-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="74837-127">Related topics</span></span>

* [<span data-ttu-id="74837-128">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="74837-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




