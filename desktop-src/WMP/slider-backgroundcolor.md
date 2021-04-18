---
title: Slider. BackgroundColor
description: Das BackgroundColor-Attribut gibt die Hintergrundfarbe des Schieberegler-Steuer Elements an oder ruft diese ab.
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- Schieberegler. BackgroundColor-Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06cc595af13b28541fcc570e130da4e804fdeafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365939"
---
# <a name="sliderbackgroundcolor"></a><span data-ttu-id="72561-104">Slider. BackgroundColor</span><span class="sxs-lookup"><span data-stu-id="72561-104">SLIDER.backgroundColor</span></span>

<span data-ttu-id="72561-105">Das **BackgroundColor** -Attribut gibt die Hintergrundfarbe des Schieberegler-Steuer Elements an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="72561-105">The **backgroundColor** attribute specifies or retrieves the background color of the slider control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="72561-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="72561-106">Possible Values</span></span>

<span data-ttu-id="72561-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** mit einem beliebigen Microsoft Internet Explorer-Farbwert.</span><span class="sxs-lookup"><span data-stu-id="72561-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="72561-108">Er besitzt keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="72561-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72561-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72561-109">Remarks</span></span>

<span data-ttu-id="72561-110">Ein grundlegendes Schieberegler-Steuerelement kann erstellt werden, indem **Background Color** oder **BackgroundImage** und **ForegroundColor** oder **foregroundimage** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="72561-110">A basic slider control can be constructed by specifying **backgroundColor** or **backgroundImage**, and **foregroundColor** or **foregroundImage**.</span></span>

<span data-ttu-id="72561-111">Wenn die Farben verwendet werden, definieren die Abmessungen des Schieberegler-Steuer Elements den Bereich, der von der Hintergrundfarbe ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="72561-111">When using the colors, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="72561-112">Die Vordergrundfarbe deckt die Hintergrundfarbe ab, wenn die Schiebereglerposition zunimmt.</span><span class="sxs-lookup"><span data-stu-id="72561-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="72561-113">Geben Sie die **backgroundendcolor** -oder **foregroundendcolor** -Attribute an, um eine Verlaufs Füllung des Bereichs zu erstellen, der durch die Hintergrund-oder Vordergrundfarbe belegt ist.</span><span class="sxs-lookup"><span data-stu-id="72561-113">To make a gradient fill of the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="72561-114">Weitere Informationen finden Sie unter *customslider*. [positionImage](customslider-positionimage.md) -Attribut für ein Beispiel, das veranschaulicht, wie die Attribute des **Slider** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72561-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="72561-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72561-115">Requirements</span></span>



| <span data-ttu-id="72561-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72561-116">Requirement</span></span> | <span data-ttu-id="72561-117">Wert</span><span class="sxs-lookup"><span data-stu-id="72561-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="72561-118">Version</span><span class="sxs-lookup"><span data-stu-id="72561-118">Version</span></span><br/> | <span data-ttu-id="72561-119">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="72561-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72561-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72561-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72561-121">**Farb Verweis**</span><span class="sxs-lookup"><span data-stu-id="72561-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="72561-122">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="72561-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="72561-123">**Slider. backgroundendcolor**</span><span class="sxs-lookup"><span data-stu-id="72561-123">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="72561-124">**Slider. BackgroundImage**</span><span class="sxs-lookup"><span data-stu-id="72561-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="72561-125">**Slider. ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="72561-125">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="72561-126">**Slider. foregroundendcolor**</span><span class="sxs-lookup"><span data-stu-id="72561-126">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="72561-127">**Slider. foregroundimage**</span><span class="sxs-lookup"><span data-stu-id="72561-127">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





