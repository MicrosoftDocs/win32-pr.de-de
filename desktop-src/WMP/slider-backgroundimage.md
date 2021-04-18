---
title: Slider. BackgroundImage
description: Das BackgroundImage-Attribut gibt das Hintergrundbild des Schiebereglers an oder ruft es ab.
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- Slider. BackgroundImage-Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1188756c16b13bef69dfd0bcd9a5b66560856f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358252"
---
# <a name="sliderbackgroundimage"></a><span data-ttu-id="c736a-104">Slider. BackgroundImage</span><span class="sxs-lookup"><span data-stu-id="c736a-104">SLIDER.backgroundImage</span></span>

<span data-ttu-id="c736a-105">Das **BackgroundImage** -Attribut gibt das Hintergrundbild des Schiebereglers an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="c736a-105">The **backgroundImage** attribute specifies or retrieves the background image of the slider.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="c736a-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="c736a-106">Possible Values</span></span>

<span data-ttu-id="c736a-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.</span><span class="sxs-lookup"><span data-stu-id="c736a-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="c736a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c736a-108">Remarks</span></span>

<span data-ttu-id="c736a-109">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="c736a-109">This attribute is optional.</span></span> <span data-ttu-id="c736a-110">Wenn Sie Bilder zum Erstellen eines Schiebereglers verwenden, wird **BackgroundImage** für den hauptschiebe Regler verwendet.</span><span class="sxs-lookup"><span data-stu-id="c736a-110">When using images to construct a slider, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="c736a-111">" **Thumbimage** " stellt den tatsächlichen Schieberegler dar und kann mit der Maus verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="c736a-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="c736a-112">Im Schieberegler " **thumbimage** " gibt es eine unsichtbare Zeile, in der das Hintergrundbild auf einer Seite der Zeile angezeigt wird, und das Vordergrundbild wird auf der anderen Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c736a-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="c736a-113">Wenn der Schieberegler " **thumbimage** " mit der Maus bewegt wird und " **Folie** " auf "true" festgelegt ist, wird das Vordergrundbild so bewegt, als ob es vom Schieberegler abgerufen wird, um das Hintergrundbild abzudecken.</span><span class="sxs-lookup"><span data-stu-id="c736a-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="c736a-114">Wenn **Folie** auf false festgelegt ist, wird das Vordergrundbild nicht verschoben, sondern direkt angezeigt, als ob der Schieberegler das Hintergrundbild aus dem Vordergrundbild verschiebt.</span><span class="sxs-lookup"><span data-stu-id="c736a-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="c736a-115">Wenn das **Kachel** Attribut auf "true" festgelegt ist und das Hintergrundbild kleiner als das Schieberegler-Steuerelement ist, wird das Bild abhängig vom **Direction** -Attribut entweder horizontal oder vertikal gekachelt.</span><span class="sxs-lookup"><span data-stu-id="c736a-115">If the **tiled** attribute is set to true and the background image is smaller than the slider control, the image will be tiled either horizontally or vertically depending on the **direction** attribute.</span></span> <span data-ttu-id="c736a-116">Wenn das **BorderSize** -Attribut auf einen Wert größer als 0 (null) festgelegt ist, ist die angegebene Zahl die Anzahl der Pixel von links nach rechts oder oben und unten im Bild (abhängig vom **Direction** -Attribut), die für die Rahmen des Schieberegler-Steuer Elements reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="c736a-116">If the **borderSize** attribute is set to a value greater than zero, the number specified will be the number of pixels from the left and right or top and bottom of the image (again, depending on the **direction** attribute) that will be reserved for the borders of the slider control.</span></span> <span data-ttu-id="c736a-117">In diesem Fall wird nur der zentrale Teil des Bilds zum Durchsuchen des restlichen Steuer Elements verwendet.</span><span class="sxs-lookup"><span data-stu-id="c736a-117">In this case, only the central portion of the image is used for tiling the remainder of the control.</span></span>

<span data-ttu-id="c736a-118">Die unterstützten Formate sind BMP, JPG, PNG und GIF (keine animierten GIFs).</span><span class="sxs-lookup"><span data-stu-id="c736a-118">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="c736a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c736a-119">Requirements</span></span>



| <span data-ttu-id="c736a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c736a-120">Requirement</span></span> | <span data-ttu-id="c736a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c736a-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c736a-122">Version</span><span class="sxs-lookup"><span data-stu-id="c736a-122">Version</span></span><br/> | <span data-ttu-id="c736a-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c736a-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c736a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c736a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c736a-125">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="c736a-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="c736a-126">**Slider. foregroundimage**</span><span class="sxs-lookup"><span data-stu-id="c736a-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="c736a-127">**Schieberegler. Folie**</span><span class="sxs-lookup"><span data-stu-id="c736a-127">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="c736a-128">**Slider. thumbimage**</span><span class="sxs-lookup"><span data-stu-id="c736a-128">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> </dl>

 

 





