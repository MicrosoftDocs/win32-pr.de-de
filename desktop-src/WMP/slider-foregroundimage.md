---
title: Slider. foregroundimage
description: Das foregroundimage-Attribut gibt das Vordergrundbild des Schiebereglers an oder ruft es ab.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- Slider. foregroundimage-Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a286d3b73a2647160a0bd23357703f4fcb88d267
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371510"
---
# <a name="sliderforegroundimage"></a><span data-ttu-id="98ea9-104">Slider. foregroundimage</span><span class="sxs-lookup"><span data-stu-id="98ea9-104">SLIDER.foregroundImage</span></span>

<span data-ttu-id="98ea9-105">Das **foregroundimage** -Attribut gibt das Vordergrundbild des Schiebereglers an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="98ea9-105">The **foregroundImage** attribute specifies or retrieves the foreground image of the slider.</span></span>

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a><span data-ttu-id="98ea9-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="98ea9-106">Possible Values</span></span>

<span data-ttu-id="98ea9-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.</span><span class="sxs-lookup"><span data-stu-id="98ea9-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="98ea9-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98ea9-108">Remarks</span></span>

<span data-ttu-id="98ea9-109">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="98ea9-109">This attribute is optional.</span></span> <span data-ttu-id="98ea9-110">Wenn Sie Bilder zum Erstellen eines Schieberegler-Steuer Elements verwenden, wird **BackgroundImage** für den hauptschiebe Regler verwendet.</span><span class="sxs-lookup"><span data-stu-id="98ea9-110">When using images to construct a slider control, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="98ea9-111">" **Thumbimage** " stellt den tatsächlichen Schieberegler dar und kann mit der Maus verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="98ea9-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="98ea9-112">Im Schieberegler " **thumbimage** " gibt es eine unsichtbare Zeile, in der das Hintergrundbild auf einer Seite der Zeile angezeigt wird, und das Vordergrundbild wird auf der anderen Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="98ea9-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="98ea9-113">Wenn der Schieberegler " **thumbimage** " mit der Maus bewegt wird und " **Folie** " auf "true" festgelegt ist, wird das Vordergrundbild so bewegt, als ob es vom Schieberegler abgerufen wird, um das Hintergrundbild abzudecken.</span><span class="sxs-lookup"><span data-stu-id="98ea9-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="98ea9-114">Wenn **Folie** auf false festgelegt ist, wird das Vordergrundbild nicht verschoben, sondern direkt angezeigt, als ob der Schieberegler das Hintergrundbild aus dem Vordergrundbild verschiebt.</span><span class="sxs-lookup"><span data-stu-id="98ea9-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="98ea9-115">Wenn das **Kachel** Attribut auf "true" festgelegt ist und das Vordergrundbild kleiner als der Vordergrund Bereich des Schieberegler-Steuer Elements ist, wird das Bild entweder horizontal oder vertikal gekachelt, abhängig vom **Direction** -Attribut, um den verfügbaren Platz auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="98ea9-115">If the **tiled** attribute is set to true and the foreground image is smaller than the foreground area of the slider control, the image will be tiled either horizontally or vertically, depending on the **direction** attribute, to fill the available space.</span></span>

<span data-ttu-id="98ea9-116">Die unterstützten Formate sind BMP, JPG, PNG und GIF (keine animierten GIFs).</span><span class="sxs-lookup"><span data-stu-id="98ea9-116">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="98ea9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98ea9-117">Requirements</span></span>



| <span data-ttu-id="98ea9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98ea9-118">Requirement</span></span> | <span data-ttu-id="98ea9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="98ea9-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="98ea9-120">Version</span><span class="sxs-lookup"><span data-stu-id="98ea9-120">Version</span></span><br/> | <span data-ttu-id="98ea9-121">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="98ea9-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98ea9-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98ea9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ea9-123">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="98ea9-123">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="98ea9-124">**Slider. BackgroundImage**</span><span class="sxs-lookup"><span data-stu-id="98ea9-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="98ea9-125">**Schieberegler. Folie**</span><span class="sxs-lookup"><span data-stu-id="98ea9-125">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="98ea9-126">**Slider. thumbimage**</span><span class="sxs-lookup"><span data-stu-id="98ea9-126">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="98ea9-127">**Slider. Wert**</span><span class="sxs-lookup"><span data-stu-id="98ea9-127">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





