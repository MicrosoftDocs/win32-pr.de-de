---
title: Button. Bild
description: Das Image-Attribut gibt das Standardbild der Schaltfläche an oder ruft es ab.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- Button. Bild-Windows-Media Player
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27363383d72110ebe7b3e94187013ab701a6a3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367763"
---
# <a name="buttonimage"></a><span data-ttu-id="f9b3c-104">Button. Bild</span><span class="sxs-lookup"><span data-stu-id="f9b3c-104">BUTTON.image</span></span>

<span data-ttu-id="f9b3c-105">Das **Image** -Attribut gibt das Standardbild der **Schaltfläche** an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="f9b3c-105">The **image** attribute specifies or retrieves the default image of the **BUTTON**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="f9b3c-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f9b3c-106">Possible Values</span></span>

<span data-ttu-id="f9b3c-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen der Bilddatei enthält</span><span class="sxs-lookup"><span data-stu-id="f9b3c-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9b3c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9b3c-108">Remarks</span></span>

<span data-ttu-id="f9b3c-109">Die unterstützten Bildformate sind BMP, JPG, PNG und GIF (einschließlich animierter Gifs).</span><span class="sxs-lookup"><span data-stu-id="f9b3c-109">The supported image formats are BMP, JPG, PNG, and GIF (including animated GIFs).</span></span>

<span data-ttu-id="f9b3c-110">Wenn das **Schalt** Flächen Bild größer als der durch die **Width** -und **height** -Attribute definierte Bereich ist, wird das Bild beschnitten.</span><span class="sxs-lookup"><span data-stu-id="f9b3c-110">If the **BUTTON** image is larger than the region defined by the **width** and **height** attributes, the image will be cropped.</span></span>

<span data-ttu-id="f9b3c-111">Wenn das Bild nicht angegeben wird, aber **Höhe** und **Breite** sind, wird das Bild direkt hinter diesem Steuerelement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f9b3c-111">If the image is not specified but the **height** and **width** are, then the image directly behind this control is displayed.</span></span> <span data-ttu-id="f9b3c-112">Dies kann das Zeichnen des Bilds auf der **Ansicht** selbst vereinfachen, wodurch die Anzahl der erforderlichen getrennten Bilddateien reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="f9b3c-112">This can facilitate drawing the image on the **VIEW** itself, reducing the number of separate image files needed.</span></span>

<span data-ttu-id="f9b3c-113">Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f9b3c-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9b3c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9b3c-114">Requirements</span></span>



| <span data-ttu-id="f9b3c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9b3c-115">Requirement</span></span> | <span data-ttu-id="f9b3c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f9b3c-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f9b3c-117">Version</span><span class="sxs-lookup"><span data-stu-id="f9b3c-117">Version</span></span><br/> | <span data-ttu-id="f9b3c-118">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="f9b3c-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9b3c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9b3c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b3c-120">**Button-Element**</span><span class="sxs-lookup"><span data-stu-id="f9b3c-120">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





