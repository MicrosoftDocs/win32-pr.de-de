---
title: Text. Scroll
description: Mit dem Scroll-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob der Text durch einen Bildlauf
ms.assetid: 1cd5cb4e-673f-4273-91ff-50165c2b08fa
keywords:
- Text. Scrollfenster Media Player
topic_type:
- apiref
api_name:
- TEXT.scrolling
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fdbb80b2033d542da4894172d58451ed5da224f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368555"
---
# <a name="textscrolling"></a><span data-ttu-id="2acd4-104">Text. Scroll</span><span class="sxs-lookup"><span data-stu-id="2acd4-104">TEXT.scrolling</span></span>

<span data-ttu-id="2acd4-105">Mit dem **Scroll** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob der Text durch einen Bildlauf</span><span class="sxs-lookup"><span data-stu-id="2acd4-105">The **scrolling** attribute specifies or retrieves a value indicating whether the text scrolls.</span></span>

``` syntax
        elementID.scrolling
```

## <a name="possible-values"></a><span data-ttu-id="2acd4-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="2acd4-106">Possible Values</span></span>

<span data-ttu-id="2acd4-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2acd4-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="2acd4-108">Wert</span><span class="sxs-lookup"><span data-stu-id="2acd4-108">Value</span></span> | <span data-ttu-id="2acd4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2acd4-109">Description</span></span>                     |
|-------|---------------------------------|
| <span data-ttu-id="2acd4-110">true</span><span class="sxs-lookup"><span data-stu-id="2acd4-110">true</span></span>  | <span data-ttu-id="2acd4-111">Scrollen ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2acd4-111">Scrolling is enabled.</span></span>           |
| <span data-ttu-id="2acd4-112">false</span><span class="sxs-lookup"><span data-stu-id="2acd4-112">false</span></span> | <span data-ttu-id="2acd4-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="2acd4-113">Default.</span></span> <span data-ttu-id="2acd4-114">Der Bildlauf ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2acd4-114">Scrolling is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2acd4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2acd4-115">Remarks</span></span>

<span data-ttu-id="2acd4-116">Die Scrollfunktion stellt einen Puffer mit zwei Leerzeichen zwischen dem Ende des Texts und dem Anfang der wiederholten Zeile bereit.</span><span class="sxs-lookup"><span data-stu-id="2acd4-116">The scrolling feature provides a two-space buffer between the end of the text and the beginning of the repeated line.</span></span>

<span data-ttu-id="2acd4-117">Das Attribut " **Begründung** " gibt an, wo der Text zuerst vor dem Scrollen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2acd4-117">The **justification** attribute specifies where the text first appears before the scrolling begins.</span></span>

<span data-ttu-id="2acd4-118">Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2acd4-118">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2acd4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2acd4-119">Requirements</span></span>



| <span data-ttu-id="2acd4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2acd4-120">Requirement</span></span> | <span data-ttu-id="2acd4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2acd4-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2acd4-122">Version</span><span class="sxs-lookup"><span data-stu-id="2acd4-122">Version</span></span><br/> | <span data-ttu-id="2acd4-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="2acd4-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2acd4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2acd4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2acd4-125">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="2acd4-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="2acd4-126">**Text. Begründung**</span><span class="sxs-lookup"><span data-stu-id="2acd4-126">**TEXT.justification**</span></span>](text-justification.md)
</dt> <dt>

[<span data-ttu-id="2acd4-127">**Text. scrollingamount**</span><span class="sxs-lookup"><span data-stu-id="2acd4-127">**TEXT.scrollingAmount**</span></span>](text-scrollingamount.md)
</dt> <dt>

[<span data-ttu-id="2acd4-128">**Text. scrollingdelay**</span><span class="sxs-lookup"><span data-stu-id="2acd4-128">**TEXT.scrollingDelay**</span></span>](text-scrollingdelay.md)
</dt> <dt>

[<span data-ttu-id="2acd4-129">**Text. scrollingdirection**</span><span class="sxs-lookup"><span data-stu-id="2acd4-129">**TEXT.scrollingDirection**</span></span>](text-scrollingdirection.md)
</dt> </dl>

 

 





