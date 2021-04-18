---
title: Slider. ForegroundColor
description: Das ForegroundColor-Attribut gibt die Vordergrundfarbe des Schieberegler-Steuer Elements an oder ruft diese ab.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- Schieberegler. ForegroundColor-Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d334dff4d9b7d90582e44018bf8f56c04fa784a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365633"
---
# <a name="sliderforegroundcolor"></a><span data-ttu-id="837ff-104">Slider. ForegroundColor</span><span class="sxs-lookup"><span data-stu-id="837ff-104">SLIDER.foregroundColor</span></span>

<span data-ttu-id="837ff-105">Das **ForegroundColor** -Attribut gibt die Vordergrundfarbe des Schieberegler-Steuer Elements an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="837ff-105">The **foregroundColor** attribute specifies or retrieves the foreground color of the slider control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="837ff-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="837ff-106">Possible Values</span></span>

<span data-ttu-id="837ff-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** mit einem beliebigen Microsoft Internet Explorer-Farbwert.</span><span class="sxs-lookup"><span data-stu-id="837ff-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="837ff-108">Der Standardwert ist "White".</span><span class="sxs-lookup"><span data-stu-id="837ff-108">The default value is "white".</span></span>

## <a name="remarks"></a><span data-ttu-id="837ff-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="837ff-109">Remarks</span></span>

<span data-ttu-id="837ff-110">Ein grundlegendes Schieberegler-Steuerelement kann erstellt werden, indem eines von zwei Attributen von Attributen angegeben wird: **Background Color** und **ForegroundColor** oder **BackgroundImage** und **foregroundimage**.</span><span class="sxs-lookup"><span data-stu-id="837ff-110">A basic slider control can be constructed by specifying one of two pairs of attributes: the **backgroundColor** and **foregroundColor**, or the **backgroundImage** and **foregroundImage**.</span></span>

<span data-ttu-id="837ff-111">Wenn Sie mithilfe der Color-Attribute ein Schieberegler-Steuerelement erstellen, definieren die Abmessungen des Schieberegler-Steuer Elements den Bereich, der von der Hintergrundfarbe ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="837ff-111">When you construct a slider control using the color attributes, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="837ff-112">Die Vordergrundfarbe deckt die Hintergrundfarbe ab, wenn die Schiebereglerposition zunimmt.</span><span class="sxs-lookup"><span data-stu-id="837ff-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="837ff-113">Geben Sie die Attribute **backgroundendcolor** oder **foregroundendcolor** an, um eine Verlaufs Füllung in dem Bereich zu erstellen, der durch die Hintergrund-oder Vordergrundfarbe belegt ist.</span><span class="sxs-lookup"><span data-stu-id="837ff-113">To make a gradient fill in the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="837ff-114">Weitere Informationen finden Sie unter *customslider*. [positionImage](customslider-positionimage.md) -Attribut für ein Beispiel, das veranschaulicht, wie die Attribute des **Slider** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="837ff-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="837ff-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="837ff-115">Requirements</span></span>



| <span data-ttu-id="837ff-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="837ff-116">Requirement</span></span> | <span data-ttu-id="837ff-117">Wert</span><span class="sxs-lookup"><span data-stu-id="837ff-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="837ff-118">Version</span><span class="sxs-lookup"><span data-stu-id="837ff-118">Version</span></span><br/> | <span data-ttu-id="837ff-119">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="837ff-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="837ff-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="837ff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="837ff-121">**Farb Verweis**</span><span class="sxs-lookup"><span data-stu-id="837ff-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="837ff-122">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="837ff-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="837ff-123">**Slider. BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="837ff-123">**SLIDER.backgroundColor**</span></span>](slider-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="837ff-124">**Slider. backgroundendcolor**</span><span class="sxs-lookup"><span data-stu-id="837ff-124">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="837ff-125">**Slider. foregroundendcolor**</span><span class="sxs-lookup"><span data-stu-id="837ff-125">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="837ff-126">**Slider. foregroundimage**</span><span class="sxs-lookup"><span data-stu-id="837ff-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





