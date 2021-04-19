---
title: Schieberegler. Kachel
description: Mit dem gekachelten Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Schieberegler-Bild angezeigt wird.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- Schieberegler. gekachelte Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1448f496ee45d6c8b01356499b9628c745d69f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369707"
---
# <a name="slidertiled"></a><span data-ttu-id="829f6-104">Schieberegler. Kachel</span><span class="sxs-lookup"><span data-stu-id="829f6-104">SLIDER.tiled</span></span>

<span data-ttu-id="829f6-105">Mit dem **gekachelten** Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Schieberegler-Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="829f6-105">The **tiled** attribute specifies or retrieves a value indicating whether the slider image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="829f6-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="829f6-106">Possible Values</span></span>

<span data-ttu-id="829f6-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="829f6-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="829f6-108">Wert</span><span class="sxs-lookup"><span data-stu-id="829f6-108">Value</span></span> | <span data-ttu-id="829f6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="829f6-109">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="829f6-110">true</span><span class="sxs-lookup"><span data-stu-id="829f6-110">true</span></span>  | <span data-ttu-id="829f6-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="829f6-111">Default.</span></span> <span data-ttu-id="829f6-112">Die Bild Bitmap wird wiederholt, bis Sie den gesamten Bereich des Steuer Elements füllt.</span><span class="sxs-lookup"><span data-stu-id="829f6-112">The image bitmap will be repeated until it fills the entire region of the control.</span></span> |
| <span data-ttu-id="829f6-113">false</span><span class="sxs-lookup"><span data-stu-id="829f6-113">false</span></span> | <span data-ttu-id="829f6-114">Das Bild wird nicht gekachelt.</span><span class="sxs-lookup"><span data-stu-id="829f6-114">The image will not be tiled.</span></span>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="829f6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="829f6-115">Remarks</span></span>

<span data-ttu-id="829f6-116">Dieses Attribut gilt nur, wenn Sie Vordergrund-und Hintergrundbilder zum Definieren eines Schieberegler-Steuer Elements verwenden.</span><span class="sxs-lookup"><span data-stu-id="829f6-116">This attribute applies only if you are using foreground and background images to define a slider control.</span></span> <span data-ttu-id="829f6-117">Wenn die Bilder kleiner als der definierte Bereich des Schiebereglers sind und das **Kachel** Attribut auf true festgelegt ist, werden die Bilder so lange wiederholt, bis Sie die gesamte Länge des Steuer Elements auffüllen.</span><span class="sxs-lookup"><span data-stu-id="829f6-117">If the images are smaller than the defined area of the slider, and the **tiled** attribute is set to true, the images will be repeated until they fill the entire length of the control.</span></span>

<span data-ttu-id="829f6-118">Möglicherweise möchten Sie dieses Attribut zusammen mit dem **BorderSize** -Attribut verwenden.</span><span class="sxs-lookup"><span data-stu-id="829f6-118">You may wish to use this attribute in conjunction with the **borderSize** attribute.</span></span> <span data-ttu-id="829f6-119">Das **BorderSize** -Attribut ermöglicht es Ihnen, einen Rahmen zu definieren, der während der tiult nicht wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="829f6-119">The **borderSize** attribute allows you to define a border that is not repeated during tiling.</span></span>

## <a name="requirements"></a><span data-ttu-id="829f6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="829f6-120">Requirements</span></span>



| <span data-ttu-id="829f6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="829f6-121">Requirement</span></span> | <span data-ttu-id="829f6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="829f6-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="829f6-123">Version</span><span class="sxs-lookup"><span data-stu-id="829f6-123">Version</span></span><br/> | <span data-ttu-id="829f6-124">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="829f6-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="829f6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="829f6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="829f6-126">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="829f6-126">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="829f6-127">**Slider. BackgroundImage**</span><span class="sxs-lookup"><span data-stu-id="829f6-127">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="829f6-128">**Slider. BorderSize**</span><span class="sxs-lookup"><span data-stu-id="829f6-128">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="829f6-129">**Slider. foregroundimage**</span><span class="sxs-lookup"><span data-stu-id="829f6-129">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





