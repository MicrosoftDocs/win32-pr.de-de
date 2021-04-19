---
title: ButtonGroup. TransparencyColor
description: Das TransparencyColor-Attribut gibt die transparente Farbe der ButtonGroup-Bilder an oder ruft diese ab.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- ButtonGroup. TransparencyColor-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaf6fb70db7d2699a63eb7b4fd34009f7b8ba75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373693"
---
# <a name="buttongrouptransparencycolor"></a><span data-ttu-id="fa502-104">ButtonGroup. TransparencyColor</span><span class="sxs-lookup"><span data-stu-id="fa502-104">BUTTONGROUP.transparencyColor</span></span>

<span data-ttu-id="fa502-105">Das **TransparencyColor** -Attribut gibt die transparente Farbe der **ButtonGroup** -Bilder an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="fa502-105">The **transparencyColor** attribute specifies or retrieves the transparent color of the **BUTTONGROUP** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="fa502-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="fa502-106">Possible Values</span></span>

<span data-ttu-id="fa502-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** ohne Standardwert, der einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="fa502-107">This attribute is a read/write **String** with no default, containing one of the following values.</span></span>



| <span data-ttu-id="fa502-108">Wert</span><span class="sxs-lookup"><span data-stu-id="fa502-108">Value</span></span>                                       | <span data-ttu-id="fa502-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa502-109">Description</span></span>                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa502-110">Auto</span><span class="sxs-lookup"><span data-stu-id="fa502-110">Auto</span></span>                                        | <span data-ttu-id="fa502-111">Das Pixel an Position 0, 0 im Bild wird zur transparenten Farbe.</span><span class="sxs-lookup"><span data-stu-id="fa502-111">The pixel at location 0,0 in the image becomes the transparent color.</span></span>                              |
| <span data-ttu-id="fa502-112">Jeder Microsoft Internet Explorer-Farbwert</span><span class="sxs-lookup"><span data-stu-id="fa502-112">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="fa502-113">Ein Internet Explorer-Farbwert wird zur transparenten Farbe (z. b. "Red" oder " \# FF0000").</span><span class="sxs-lookup"><span data-stu-id="fa502-113">An Internet Explorer color value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="fa502-114">Keine</span><span class="sxs-lookup"><span data-stu-id="fa502-114">None</span></span>                                        | <span data-ttu-id="fa502-115">Standard.</span><span class="sxs-lookup"><span data-stu-id="fa502-115">Default.</span></span> <span data-ttu-id="fa502-116">Keine Transparenz.</span><span class="sxs-lookup"><span data-stu-id="fa502-116">No transparency.</span></span>                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="fa502-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa502-117">Remarks</span></span>

<span data-ttu-id="fa502-118">Eine transparente Farbe in einem Bild ermöglicht, dass alle hinter dem Bild liegenden Bereiche durch die Transparenz Bereiche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fa502-118">A transparent color in an image will allow whatever is behind the image to show through the areas of transparency.</span></span> <span data-ttu-id="fa502-119">Der transparente Bereich ist klickbar, es sei denn, er wurde durch das **clippingimage** -Tag abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="fa502-119">The transparent region is clickable unless clipped by the **clippingImage** tag.</span></span>

<span data-ttu-id="fa502-120">Die Farbe kann jeder beliebige Microsoft Internet Explorer-Farbwert sein.</span><span class="sxs-lookup"><span data-stu-id="fa502-120">The color can be any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="fa502-121">Wenn der Wert Auto ist, wird die Farbe des Pixels an Position 0, 0 im Bild verwendet.</span><span class="sxs-lookup"><span data-stu-id="fa502-121">If the value is Auto, then the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="fa502-122">Wenn es sich bei der angegebenen Farbe nicht um eine der gültigen Internet Explorer-Farben handelt, wird eine Warnung zurückgegeben, und der vorherige Wert wird beibehalten.</span><span class="sxs-lookup"><span data-stu-id="fa502-122">If the color specified is not one of the valid Internet Explorer colors, a warning is returned and the previous value is maintained.</span></span>

<span data-ttu-id="fa502-123">Da es sich bei den JPGs um Verlust Verluste handelt und daher unerwartete Farbänderungen unterliegen, werden Sie nicht empfohlen, wenn **transparendcolor** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa502-123">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa502-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa502-124">Requirements</span></span>



| <span data-ttu-id="fa502-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa502-125">Requirement</span></span> | <span data-ttu-id="fa502-126">Wert</span><span class="sxs-lookup"><span data-stu-id="fa502-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fa502-127">Version</span><span class="sxs-lookup"><span data-stu-id="fa502-127">Version</span></span><br/> | <span data-ttu-id="fa502-128">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fa502-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa502-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa502-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa502-130">**ButtonGroup-Element**</span><span class="sxs-lookup"><span data-stu-id="fa502-130">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="fa502-131">**Farb Verweis**</span><span class="sxs-lookup"><span data-stu-id="fa502-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





