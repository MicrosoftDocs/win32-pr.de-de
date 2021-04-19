---
title: Slider. BorderSize
description: Das BorderSize-Attribut gibt die Rahmenbreite in Pixel an oder ruft Sie ab.
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- Schieberegler. BorderSize-Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c3ebc95e3ecf04ae78fa78c4b46f38fdd910004
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372598"
---
# <a name="sliderbordersize"></a><span data-ttu-id="7d914-104">Slider. BorderSize</span><span class="sxs-lookup"><span data-stu-id="7d914-104">SLIDER.borderSize</span></span>

<span data-ttu-id="7d914-105">Das **BorderSize** -Attribut gibt die Rahmenbreite in Pixel an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="7d914-105">The **borderSize** attribute specifies or retrieves the border width in pixels.</span></span>

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a><span data-ttu-id="7d914-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="7d914-106">Possible Values</span></span>

<span data-ttu-id="7d914-107">Dieses Attribut ist eine Lese-/schreibzahl (**Long**), die die Breite des Rahmens in Pixel darstellt. </span><span class="sxs-lookup"><span data-stu-id="7d914-107">This attribute is a read/write **Number** (**long**) representing the border width in pixels.</span></span> <span data-ttu-id="7d914-108">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7d914-108">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d914-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d914-109">Remarks</span></span>

<span data-ttu-id="7d914-110">Dieses Attribut definiert einen Offset vom Anfang und Ende des Schieberegler-Steuer Elements, von links nach rechts, wenn das **Direction** -Attribut auf "horizontal" festgelegt ist, und von oben nach unten, wenn es auf "vertikal" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7d914-110">This attribute defines an offset from the beginning and end of the slider control that is, from the left and right if the **direction** attribute is set to "horizontal", and from the top and bottom if it is set to "vertical".</span></span> <span data-ttu-id="7d914-111">Diese Offset Positionen legen die minimalen und maximalen Positionen des Schieberegler-Zieh Punkts fest, über den die Vordergrundfarbe oder das Bild nicht angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d914-111">These offset positions dictate the minimum and maximum positions of the slider thumb, beyond which the foreground color or image will not be applied.</span></span>

<span data-ttu-id="7d914-112">Wenn ein Hintergrundbild mit dem auf true festgelegten **Kachel** Attribut verwendet wird, wird der Offset auf das Bild angewendet, wobei die Größe des Bilds (entweder von links nach rechts oder von oben nach unten) für den Anfangs-und Endrahmen des Schieberegler-Steuer Elements festgelegt wird, wobei der zentrale Teil des Bilds im gesamten Rest gekachelt wird.</span><span class="sxs-lookup"><span data-stu-id="7d914-112">If a background image is used with the **tiled** attribute set to true, the offset is applied to the image, dictating the amount of the image (either from the left and right or from the top and bottom) to be used for the beginning and end borders of the slider control, with the central portion of the image being tiled throughout the remainder.</span></span> <span data-ttu-id="7d914-113">Auf diese Weise kann ein kleines Hintergrundbild verwendet werden, um die vollständige Länge eines größeren Schieberegler-Steuer Elements abzudecken.</span><span class="sxs-lookup"><span data-stu-id="7d914-113">In this way, a small background image can be used to cover the full length of a larger slider control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d914-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d914-114">Requirements</span></span>



| <span data-ttu-id="7d914-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d914-115">Requirement</span></span> | <span data-ttu-id="7d914-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7d914-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7d914-117">Version</span><span class="sxs-lookup"><span data-stu-id="7d914-117">Version</span></span><br/> | <span data-ttu-id="7d914-118">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="7d914-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d914-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d914-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d914-120">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="7d914-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="7d914-121">**Slider. ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="7d914-121">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="7d914-122">**Slider. foregroundimage**</span><span class="sxs-lookup"><span data-stu-id="7d914-122">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="7d914-123">**Slider. thumbimage**</span><span class="sxs-lookup"><span data-stu-id="7d914-123">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="7d914-124">**Schieberegler. Kachel**</span><span class="sxs-lookup"><span data-stu-id="7d914-124">**SLIDER.tiled**</span></span>](slider-tiled.md)
</dt> </dl>

 

 





