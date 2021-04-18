---
title: Auswirkung
description: Rotiert und skaliert optional ein Bild.
ms.assetid: aa37cdf1-bbb6-db4e-45a7-67c7cc16b7b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8e521ca4c0c452301c0f8031c94ba8c22efe80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104561351"
---
# <a name="straighten-effect"></a><span data-ttu-id="f217a-103">Auswirkung</span><span class="sxs-lookup"><span data-stu-id="f217a-103">Straighten effect</span></span>

<span data-ttu-id="f217a-104">Rotiert und skaliert optional ein Bild.</span><span class="sxs-lookup"><span data-stu-id="f217a-104">Rotates and optionally scales an image.</span></span>

<span data-ttu-id="f217a-105">Die CLSID für diesen Effekt ist CLSID \_ D2D1Straighten.</span><span class="sxs-lookup"><span data-stu-id="f217a-105">The CLSID for this effect is CLSID\_D2D1Straighten.</span></span>

-   [<span data-ttu-id="f217a-106">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="f217a-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="f217a-107">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="f217a-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="f217a-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f217a-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="f217a-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f217a-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f217a-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f217a-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="f217a-111">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="f217a-111">Example image</span></span>

![Beispiel für Effekte Ausgabe](images/straighten-effect.png)

## <a name="sample-code"></a><span data-ttu-id="f217a-113">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="f217a-113">Sample code</span></span>


```cpp
ComPtr<ID2D1Effect> straightenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Straighten, &straightenEffect);
 
straightenEffect->SetInput(0, bitmap);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_ANGLE, 12.0f);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE, true);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_SCALE_MODE, D2D1_STRAIGHTEN_SCALE_MODE_LINEAR);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(straightenEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="f217a-114">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f217a-114">Effect properties</span></span>

<span data-ttu-id="f217a-115">Die Eigenschaften für den geraden Effekt werden durch die D2D1- [**\_ \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="f217a-115">The properties for the straighten effect are defined by the [**D2D1\_STRAIGHTEN\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="f217a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f217a-116">Requirements</span></span>



| <span data-ttu-id="f217a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f217a-117">Requirement</span></span> | <span data-ttu-id="f217a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f217a-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="f217a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f217a-119">Minimum supported client</span></span> | <span data-ttu-id="f217a-120">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f217a-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f217a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f217a-121">Minimum supported server</span></span> | <span data-ttu-id="f217a-122">Windows 10 \[ Desktop Apps- \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f217a-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f217a-123">Header</span><span class="sxs-lookup"><span data-stu-id="f217a-123">Header</span></span>                   | <span data-ttu-id="f217a-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="f217a-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="f217a-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f217a-125">Library</span></span>                  | <span data-ttu-id="f217a-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="f217a-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="f217a-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f217a-127">Related topics</span></span>

* [<span data-ttu-id="f217a-128">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f217a-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

