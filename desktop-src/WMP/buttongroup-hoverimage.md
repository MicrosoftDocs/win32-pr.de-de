---
title: ButtonGroup. hoverimage
description: Das hoverimage-Attribut gibt den Namen des Bilds an, das den Hover-Zustand einer Schaltfläche in der ButtonGroup darstellt, oder ruft ihn ab. Der Hover-Zustand tritt auf, wenn sich die Schaltfläche im Zustand "up" befindet und der Benutzer mit der Maus darauf zeigt.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- ButtonGroup. hoverimage-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702a7aa73f5800628fdf14deb0dbfe142cd80dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360256"
---
# <a name="buttongrouphoverimage"></a><span data-ttu-id="404c8-105">ButtonGroup. hoverimage</span><span class="sxs-lookup"><span data-stu-id="404c8-105">BUTTONGROUP.hoverImage</span></span>

<span data-ttu-id="404c8-106">Das **hoverimage** -Attribut gibt den Namen des Bilds an, das den Hover-Zustand einer Schaltfläche in der **ButtonGroup** darstellt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="404c8-106">The **hoverImage** attribute specifies or retrieves the name of the image representing the hover state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="404c8-107">Der Hover-Zustand tritt auf, wenn sich die Schaltfläche im Zustand "up" befindet und der Benutzer mit der Maus darauf zeigt.</span><span class="sxs-lookup"><span data-stu-id="404c8-107">The hover state occurs when the button is in the up state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="404c8-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="404c8-108">Possible Values</span></span>

<span data-ttu-id="404c8-109">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="404c8-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="404c8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="404c8-110">Remarks</span></span>

<span data-ttu-id="404c8-111">Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.</span><span class="sxs-lookup"><span data-stu-id="404c8-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="404c8-112">Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können seine Farbton-und Sättigungswerte mithilfe der Attribute **hueshift** und **Sättigung** dynamisch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="404c8-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="404c8-113">Das Standardbild ist das im **Image** -Attribut angegebene oder sein Standardbild.</span><span class="sxs-lookup"><span data-stu-id="404c8-113">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="404c8-114">Wenn das Hover-Bild größer als der definierte Bereich ist, wird das Hover-Bild beschnitten.</span><span class="sxs-lookup"><span data-stu-id="404c8-114">If the hover image is larger than the defined region, the hover image will be cropped.</span></span>

<span data-ttu-id="404c8-115">Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="404c8-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="404c8-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="404c8-116">Examples</span></span>

<span data-ttu-id="404c8-117">Siehe *ButtonElement*. [mappingColor](buttonelement-mappingcolor.md) -Attribut für ein Beispiel, das die Verwendung dieses Attributs veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="404c8-117">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="404c8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="404c8-118">Requirements</span></span>



| <span data-ttu-id="404c8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="404c8-119">Requirement</span></span> | <span data-ttu-id="404c8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="404c8-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="404c8-121">Version</span><span class="sxs-lookup"><span data-stu-id="404c8-121">Version</span></span><br/> | <span data-ttu-id="404c8-122">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="404c8-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="404c8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="404c8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="404c8-124">**ButtonGroup-Element**</span><span class="sxs-lookup"><span data-stu-id="404c8-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="404c8-125">**ButtonGroup. hueshift**</span><span class="sxs-lookup"><span data-stu-id="404c8-125">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="404c8-126">**ButtonGroup. Image**</span><span class="sxs-lookup"><span data-stu-id="404c8-126">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="404c8-127">**ButtonGroup. Sättigung**</span><span class="sxs-lookup"><span data-stu-id="404c8-127">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





