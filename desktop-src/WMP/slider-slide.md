---
title: Schieberegler. Folie
description: Mit dem Folie-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Vordergrundbild über das Hintergrundbild bewegt wird oder in einer statischen Position über das Hintergrundbild angezeigt wird.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- Schieberegler. Folien Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9f79b5016b323380c5a4d06c8af7ab5fb0b8a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367717"
---
# <a name="sliderslide"></a><span data-ttu-id="6511d-104">Schieberegler. Folie</span><span class="sxs-lookup"><span data-stu-id="6511d-104">SLIDER.slide</span></span>

<span data-ttu-id="6511d-105">Mit dem **Folie** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Vordergrundbild über das Hintergrundbild bewegt wird oder in einer statischen Position über das Hintergrundbild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6511d-105">The **slide** attribute specifies or retrieves a value indicating whether the foreground image slides over the background image or is gradually revealed in a static position over the background image.</span></span>

``` syntax
        elementID.slide
```

## <a name="possible-values"></a><span data-ttu-id="6511d-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="6511d-106">Possible Values</span></span>

<span data-ttu-id="6511d-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6511d-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="6511d-108">Wert</span><span class="sxs-lookup"><span data-stu-id="6511d-108">Value</span></span> | <span data-ttu-id="6511d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6511d-109">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="6511d-110">true</span><span class="sxs-lookup"><span data-stu-id="6511d-110">true</span></span>  | <span data-ttu-id="6511d-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="6511d-111">Default.</span></span> <span data-ttu-id="6511d-112">Das Vordergrundbild bewegt sich über das Hintergrundbild.</span><span class="sxs-lookup"><span data-stu-id="6511d-112">The foreground image slides over the background image.</span></span>      |
| <span data-ttu-id="6511d-113">false</span><span class="sxs-lookup"><span data-stu-id="6511d-113">false</span></span> | <span data-ttu-id="6511d-114">Das Vordergrundbild wird direkt über das Hintergrundbild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6511d-114">The foreground image is revealed in place over the background image.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6511d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6511d-115">Remarks</span></span>

<span data-ttu-id="6511d-116">Wenn der Schieberegler " **thumbimage** " mit der Maus bewegt wird und " **Folie** " auf "true" festgelegt ist, wird das Vordergrundbild so bewegt, als ob es vom Schieberegler abgerufen wird, um das Hintergrundbild abzudecken.</span><span class="sxs-lookup"><span data-stu-id="6511d-116">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="6511d-117">Wenn **Folie** auf false festgelegt ist, wird das Vordergrundbild nicht verschoben, sondern direkt angezeigt, als ob der Schieberegler das Hintergrundbild aus dem Vordergrundbild verschiebt.</span><span class="sxs-lookup"><span data-stu-id="6511d-117">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

## <a name="requirements"></a><span data-ttu-id="6511d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6511d-118">Requirements</span></span>



| <span data-ttu-id="6511d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6511d-119">Requirement</span></span> | <span data-ttu-id="6511d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6511d-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6511d-121">Version</span><span class="sxs-lookup"><span data-stu-id="6511d-121">Version</span></span><br/> | <span data-ttu-id="6511d-122">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="6511d-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6511d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6511d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6511d-124">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="6511d-124">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="6511d-125">**Slider. BackgroundImage**</span><span class="sxs-lookup"><span data-stu-id="6511d-125">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="6511d-126">**Slider. foregroundimage**</span><span class="sxs-lookup"><span data-stu-id="6511d-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





