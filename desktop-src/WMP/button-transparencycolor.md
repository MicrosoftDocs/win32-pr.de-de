---
title: Button. transparendcolor
description: Das TransparencyColor-Attribut gibt die Farbe an, die in den Schaltflächen Bildern transparent sein wird, oder ruft Sie ab.
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- Button. transparendcycolor-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361032"
---
# <a name="buttontransparencycolor"></a><span data-ttu-id="cae48-104">Button. transparendcolor</span><span class="sxs-lookup"><span data-stu-id="cae48-104">BUTTON.transparencyColor</span></span>

<span data-ttu-id="cae48-105">Das **TransparencyColor** -Attribut gibt die Farbe an, die in den **Schalt** Flächen Bildern transparent sein wird, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="cae48-105">The **transparencyColor** attribute specifies or retrieves the color that will be transparent in the **BUTTON** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="cae48-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="cae48-106">Possible Values</span></span>

<span data-ttu-id="cae48-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** ohne den Standardwert, der einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="cae48-107">This attribute is a read/write **String** with no default containing one of the following values.</span></span>



| <span data-ttu-id="cae48-108">Wert</span><span class="sxs-lookup"><span data-stu-id="cae48-108">Value</span></span>                                    | <span data-ttu-id="cae48-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cae48-109">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cae48-110">Auto</span><span class="sxs-lookup"><span data-stu-id="cae48-110">Auto</span></span>                                     | <span data-ttu-id="cae48-111">Die Farbe des Pixels an Position 0, 0 im Bild wird zur transparenten Farbe.</span><span class="sxs-lookup"><span data-stu-id="cae48-111">The color of the pixel at location 0,0 in the image becomes the transparent color.</span></span>                        |
| <span data-ttu-id="cae48-112">Ein beliebiger Internet Explorer-Farb Format Wert</span><span class="sxs-lookup"><span data-stu-id="cae48-112">Any Internet Explorer color format value</span></span> | <span data-ttu-id="cae48-113">Ein Wert für den Internet Explorer-Farb Format wird zur transparenten Farbe (z. b. "Red" oder " \# FF0000").</span><span class="sxs-lookup"><span data-stu-id="cae48-113">An Internet Explorer color format value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="cae48-114">Keine</span><span class="sxs-lookup"><span data-stu-id="cae48-114">None</span></span>                                     | <span data-ttu-id="cae48-115">Keine Transparenz.</span><span class="sxs-lookup"><span data-stu-id="cae48-115">No transparency.</span></span>                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="cae48-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cae48-116">Remarks</span></span>

<span data-ttu-id="cae48-117">Eine transparente Farbe in einem Bild ermöglicht das Anzeigen des Bilds, das über die transparenten Bereiche angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cae48-117">A transparent color in an image allows whatever is behind the image to show through the transparent areas.</span></span> <span data-ttu-id="cae48-118">Die **Schaltfläche** erhält weiterhin Klicks auf den Bereich transparent.</span><span class="sxs-lookup"><span data-stu-id="cae48-118">The **BUTTON** will still receive clicks on the transparent region.</span></span>

<span data-ttu-id="cae48-119">Die transparente Farbe kann ein beliebiger Internet Explorer-Farbwert sein.</span><span class="sxs-lookup"><span data-stu-id="cae48-119">The transparent color can be any Internet Explorer color value.</span></span> <span data-ttu-id="cae48-120">Wenn der Wert des **TransparencyColor** -Attributs auf "Auto" festgelegt ist, wird die Farbe des Pixels an Position 0, 0 im Bild verwendet.</span><span class="sxs-lookup"><span data-stu-id="cae48-120">If the value of the **transparencyColor** attribute is set to "Auto", the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="cae48-121">Wenn es sich bei der angegebenen Farbe nicht um eine der gültigen IE-Farben handelt, wird der vorherige Wert beibehalten.</span><span class="sxs-lookup"><span data-stu-id="cae48-121">If the color specified is not one of the valid IE colors, the previous value is maintained.</span></span>

<span data-ttu-id="cae48-122">Da es sich bei den JPGs um Verlust Verluste handelt und daher unerwartete Farbänderungen unterliegen, werden Sie nicht empfohlen, wenn **transparendcolor** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cae48-122">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cae48-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cae48-123">Requirements</span></span>



| <span data-ttu-id="cae48-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cae48-124">Requirement</span></span> | <span data-ttu-id="cae48-125">Wert</span><span class="sxs-lookup"><span data-stu-id="cae48-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cae48-126">Version</span><span class="sxs-lookup"><span data-stu-id="cae48-126">Version</span></span><br/> | <span data-ttu-id="cae48-127">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="cae48-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cae48-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cae48-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae48-129">**Button-Element**</span><span class="sxs-lookup"><span data-stu-id="cae48-129">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="cae48-130">**Button. Bild**</span><span class="sxs-lookup"><span data-stu-id="cae48-130">**BUTTON.image**</span></span>](button-image.md)
</dt> <dt>

[<span data-ttu-id="cae48-131">**Farb Verweis**</span><span class="sxs-lookup"><span data-stu-id="cae48-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





