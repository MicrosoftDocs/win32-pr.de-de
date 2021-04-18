---
title: Slider. thumbimage
description: Das Attribut "thumbimage" gibt das Bild an, das zum Darstellen der aktuellen Position des Schiebereglers verwendet wird, oder ruft es ab.
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- Slider. thumbimage-Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b798dfbae24fe2cef3669d2fb372966e47254026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371702"
---
# <a name="sliderthumbimage"></a><span data-ttu-id="8df86-104">Slider. thumbimage</span><span class="sxs-lookup"><span data-stu-id="8df86-104">SLIDER.thumbImage</span></span>

<span data-ttu-id="8df86-105">Das Attribut " **thumbimage** " gibt das Bild an, das zum Darstellen der aktuellen Position des Schiebereglers verwendet wird, oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="8df86-105">The **thumbImage** attribute specifies or retrieves the image that will be used to represent the current position of the slider.</span></span>

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a><span data-ttu-id="8df86-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="8df86-106">Possible Values</span></span>

<span data-ttu-id="8df86-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.</span><span class="sxs-lookup"><span data-stu-id="8df86-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="8df86-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8df86-108">Remarks</span></span>

<span data-ttu-id="8df86-109">Das **thumbimage** gibt das Bild an, das verwendet wird, um die aktuelle Position darzustellen, und zeigt an, dass der Benutzer mit dem Steuerelement Aktionen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="8df86-109">The **thumbImage** specifies the image that will be used to represent current position, as well as indicate that the user can take action with the control.</span></span> <span data-ttu-id="8df86-110">Wenn kein Thumb-Bild angegeben wird, ist der Schieberegler nicht interaktiv.</span><span class="sxs-lookup"><span data-stu-id="8df86-110">If no thumb image is specified, the slider is non-interactive.</span></span>

<span data-ttu-id="8df86-111">Das Thumb-Bild wird in der schmalen Dimension des Schieberegler-Steuer Elements zentriert.</span><span class="sxs-lookup"><span data-stu-id="8df86-111">The thumb image is centered in the narrow dimension of the slider control.</span></span> <span data-ttu-id="8df86-112">Wenn das Thumb-Bild schmaler ist als das-Steuerelement, wird das Bild in der Mitte des Hintergrunds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8df86-112">If the thumb image is narrower than the control, the image appears in the middle of the background.</span></span> <span data-ttu-id="8df86-113">Wenn das Thumb-Bild größer als das-Steuerelement ist, werden die Enden des Bilds abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="8df86-113">If the thumb image is larger than the control, the ends of the image are cut off.</span></span>

<span data-ttu-id="8df86-114">Die Position des Schiebereglers wird durch die Mitte des Thumb-Bilds angegeben.</span><span class="sxs-lookup"><span data-stu-id="8df86-114">The position of the slider is specified by the center of the thumb image.</span></span> <span data-ttu-id="8df86-115">Wenn **BorderSize** gleich 0 (null) ist, wird nur die Hälfte des Thumb-Bilds am Anfang und am Ende des Schiebereglers sichtbar.</span><span class="sxs-lookup"><span data-stu-id="8df86-115">If **borderSize** is zero, only half the thumb image will be visible at the beginning and end slider positions.</span></span> <span data-ttu-id="8df86-116">Um dies zu verhindern, legen Sie **BorderSize** auf einen Wert fest, der größer oder gleich der Hälfte der Breite des Thumb-Bilds ist (oder die halbe Höhe, wenn die **Richtung** auf "vertikal" festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="8df86-116">To prevent this, set **borderSize** to a value greater than or equal to half the width of the thumb image (or half the height if **direction** is set to "vertical").</span></span>

<span data-ttu-id="8df86-117">Die unterstützten Formate sind BMP, JPG, PNG und GIF (keine animierten GIFs).</span><span class="sxs-lookup"><span data-stu-id="8df86-117">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

<span data-ttu-id="8df86-118">Weitere Informationen finden Sie unter **customslider**. [positionImage](customslider-positionimage.md) -Attribut für ein Beispiel, das veranschaulicht, wie die Attribute des **Slider** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8df86-118">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8df86-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8df86-119">Requirements</span></span>



| <span data-ttu-id="8df86-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8df86-120">Requirement</span></span> | <span data-ttu-id="8df86-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8df86-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8df86-122">Version</span><span class="sxs-lookup"><span data-stu-id="8df86-122">Version</span></span><br/> | <span data-ttu-id="8df86-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="8df86-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8df86-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8df86-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df86-125">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="8df86-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="8df86-126">**Slider. BorderSize**</span><span class="sxs-lookup"><span data-stu-id="8df86-126">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="8df86-127">**Schieberegler. Richtung**</span><span class="sxs-lookup"><span data-stu-id="8df86-127">**SLIDER.direction**</span></span>](slider-direction.md)
</dt> </dl>

 

 





