---
title: Customslider. hoverimage
description: Das hoverimage-Attribut gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die Maus über dem benutzerdefinierten Schieberegler befindet
ms.assetid: b5d10289-280c-4578-83e8-6259249ff448
keywords:
- Windows-Media Player "customslider. hoverimage"
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 361f7d903b6231e92f331ab38a3a9f51bc3ec679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354722"
---
# <a name="customsliderhoverimage"></a><span data-ttu-id="daca2-104">Customslider. hoverimage</span><span class="sxs-lookup"><span data-stu-id="daca2-104">CUSTOMSLIDER.hoverImage</span></span>

<span data-ttu-id="daca2-105">Das **hoverimage** -Attribut gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die Maus über dem benutzerdefinierten Schieberegler befindet</span><span class="sxs-lookup"><span data-stu-id="daca2-105">The **hoverImage** attribute specifies or retrieves the image that appears when the mouse is over the custom slider.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="daca2-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="daca2-106">Possible Values</span></span>

<span data-ttu-id="daca2-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.</span><span class="sxs-lookup"><span data-stu-id="daca2-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="daca2-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="daca2-108">Remarks</span></span>

<span data-ttu-id="daca2-109">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="daca2-109">This attribute is optional.</span></span> <span data-ttu-id="daca2-110">Wenn kein Wert angegeben ist, wird die im **Image** -Attribut angegebene Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="daca2-110">If it not specified, the file specified in the **image** attribute will be used.</span></span>

<span data-ttu-id="daca2-111">Das **hoverimage** stellt den Hover-Zustand des customslider-Steuer Elements dar. Das heißt, der Status, der angezeigt wird, wenn der Mauszeiger darüber bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="daca2-111">The **hoverImage** represents the hover state of the CUSTOMSLIDER control; that is, the state that is shown when the mouse cursor hovers over it.</span></span> <span data-ttu-id="daca2-112">Dabei kann es sich um ein einzelnes Bild oder eine Reihe von Bildern handeln, die die verschiedenen Zustände des Schiebereglers darstellen.</span><span class="sxs-lookup"><span data-stu-id="daca2-112">It can be a single image or a series of images representing the various states of the slider.</span></span> <span data-ttu-id="daca2-113">Wenn mehrere Images verwendet werden, werden Sie auf die gleiche Weise wie die **Bilddatei** angeordnet.</span><span class="sxs-lookup"><span data-stu-id="daca2-113">If multiple images are used, they are arranged in the same way as the **image** file</span></span>

<span data-ttu-id="daca2-114">Die unterstützten Bild Dateitypen sind BMP, JPG, PNG und GIF (keine animierten GIFs).</span><span class="sxs-lookup"><span data-stu-id="daca2-114">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="daca2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="daca2-115">Requirements</span></span>



| <span data-ttu-id="daca2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="daca2-116">Requirement</span></span> | <span data-ttu-id="daca2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="daca2-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="daca2-118">Version</span><span class="sxs-lookup"><span data-stu-id="daca2-118">Version</span></span><br/> | <span data-ttu-id="daca2-119">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="daca2-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="daca2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="daca2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daca2-121">**Customslider-Element**</span><span class="sxs-lookup"><span data-stu-id="daca2-121">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="daca2-122">**Customslider. Image**</span><span class="sxs-lookup"><span data-stu-id="daca2-122">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





