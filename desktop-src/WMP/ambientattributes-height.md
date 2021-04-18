---
title: Ambientattribute. Height
description: Das Height-Attribut gibt die Höhe des Steuer Elements an oder ruft diese ab.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- Ambientattribute. Height-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662268bfeaf00b3185d531ff10d8dd17c9127a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358706"
---
# <a name="ambientattributesheight"></a><span data-ttu-id="03086-104">Ambientattribute. Height</span><span class="sxs-lookup"><span data-stu-id="03086-104">AmbientAttributes.height</span></span>

<span data-ttu-id="03086-105">Das **height** -Attribut gibt die Höhe des Steuer Elements an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="03086-105">The **height** attribute specifies or retrieves the height of the control.</span></span>

``` syntax
        elementID.height
```

## <a name="possible-values"></a><span data-ttu-id="03086-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="03086-106">Possible Values</span></span>

<span data-ttu-id="03086-107">Dieses Attribut ist eine Lese-/schreibzahl (**Long**), die die Höhe des Steuer Elements in Pixel darstellt. </span><span class="sxs-lookup"><span data-stu-id="03086-107">This attribute is a read/write **Number** (**long**) representing the height of the control in pixels.</span></span> <span data-ttu-id="03086-108">Der Standardwert ist 0 (null) oder die Höhe des Bilds, das im **Image** -Attribut des Steuer Elements angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="03086-108">The default value is zero or the height of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="03086-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03086-109">Remarks</span></span>

<span data-ttu-id="03086-110">Wenn die angegebene Höhe kleiner als die Höhe des angegebenen Bilds ist, wird das Bild abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="03086-110">If the height specified is smaller than the height of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="03086-111">Wenn die Höhe größer als die Höhe des Bilds ist, geht der Klick Bereich über die Bild Begrenzung hinaus.</span><span class="sxs-lookup"><span data-stu-id="03086-111">If the height is larger than the height of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="03086-112">Unabhängig davon, welcher Wert diesem Attribut zugewiesen wird, kann das Bild nicht über seine übergeordnete **Ansicht** oder **unter Ansicht** hinaus wachsen.</span><span class="sxs-lookup"><span data-stu-id="03086-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="03086-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03086-113">Requirements</span></span>



| <span data-ttu-id="03086-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03086-114">Requirement</span></span> | <span data-ttu-id="03086-115">Wert</span><span class="sxs-lookup"><span data-stu-id="03086-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="03086-116">Version</span><span class="sxs-lookup"><span data-stu-id="03086-116">Version</span></span><br/> | <span data-ttu-id="03086-117">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="03086-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="03086-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03086-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03086-119">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="03086-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





