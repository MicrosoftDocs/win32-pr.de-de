---
title: Ambientattribute. clippingcolor
description: Das clippingcolor-Attribut gibt die Farbe an, die aus der clippingimage-Bitmap abgeschnitten werden soll, oder ruft diese ab.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- Ambientattribute. clippingcolor-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370748"
---
# <a name="ambientattributesclippingcolor"></a><span data-ttu-id="cb696-104">Ambientattribute. clippingcolor</span><span class="sxs-lookup"><span data-stu-id="cb696-104">AmbientAttributes.clippingColor</span></span>

<span data-ttu-id="cb696-105">Das **clippingcolor** -Attribut gibt die Farbe an, die aus der **clippingimage** -Bitmap abgeschnitten werden soll, oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="cb696-105">The **clippingColor** attribute specifies or retrieves the color to clip out from the **clippingImage** bitmap.</span></span>

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a><span data-ttu-id="cb696-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="cb696-106">Possible Values</span></span>

<span data-ttu-id="cb696-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="cb696-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="cb696-108">Wert</span><span class="sxs-lookup"><span data-stu-id="cb696-108">Value</span></span>                                       | <span data-ttu-id="cb696-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb696-109">Description</span></span>                                       |
|---------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="cb696-110">Auto</span><span class="sxs-lookup"><span data-stu-id="cb696-110">Auto</span></span>                                        | <span data-ttu-id="cb696-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="cb696-111">Default.</span></span> <span data-ttu-id="cb696-112">Die Farbe an Pixelposition 0, 0 wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb696-112">The color at pixel location 0,0 is used.</span></span> |
| <span data-ttu-id="cb696-113">Jeder Microsoft Internet Explorer-Farbwert</span><span class="sxs-lookup"><span data-stu-id="cb696-113">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="cb696-114">Die angegebene Internet Explorer-Farbe wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb696-114">The specified Internet Explorer color is used.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="cb696-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb696-115">Remarks</span></span>

<span data-ttu-id="cb696-116">Die clippingfarbe gibt die Bereiche von **clippingimage** (oder **BackgroundImage** für **Ansicht** oder **unter Ansicht**) an, die transparenten, nicht klickbaren Teilen des Steuer Elements entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cb696-116">The clipping color indicates the regions of the **clippingImage** (or **backgroundImage** for **VIEW** or **SUBVIEW**) that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="cb696-117">Die clippingfarbe kann angeben, dass mehrere Bereiche abgeschnitten werden sollen. Eine Warnung wird ausgegeben, wenn **clippingimage** ein JPG ist, um den Verlust von Farben in den JPGs zu warnen.</span><span class="sxs-lookup"><span data-stu-id="cb696-117">The clipping color can indicate multiple regions to be clipped out. A warning is issued if the **clippingImage** is a JPG to warn of loss of color in JPGs.</span></span>

<span data-ttu-id="cb696-118">Das **clippingcolor** -Attribut wird vom **Wiedergabe** Listenelement nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb696-118">The **clippingColor** attribute is not supported by the **PLAYLIST** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb696-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb696-119">Requirements</span></span>



| <span data-ttu-id="cb696-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb696-120">Requirement</span></span> | <span data-ttu-id="cb696-121">Wert</span><span class="sxs-lookup"><span data-stu-id="cb696-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cb696-122">Version</span><span class="sxs-lookup"><span data-stu-id="cb696-122">Version</span></span><br/> | <span data-ttu-id="cb696-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="cb696-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cb696-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb696-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb696-125">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="cb696-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="cb696-126">**Ambientattribute. clippingimage**</span><span class="sxs-lookup"><span data-stu-id="cb696-126">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> <dt>

[<span data-ttu-id="cb696-127">**Farb Verweis**</span><span class="sxs-lookup"><span data-stu-id="cb696-127">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





