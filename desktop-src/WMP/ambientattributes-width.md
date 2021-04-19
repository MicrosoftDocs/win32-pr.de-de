---
title: Ambientattribute. Width
description: Das width-Attribut gibt die Breite des-Steuer Elements an oder ruft diese ab.
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- Ambientattribute. Width-Windows-Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3f91ee47277dc511d54747197edfa44e80e251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369981"
---
# <a name="ambientattributeswidth"></a><span data-ttu-id="23e62-104">Ambientattribute. Width</span><span class="sxs-lookup"><span data-stu-id="23e62-104">AmbientAttributes.width</span></span>

<span data-ttu-id="23e62-105">Das **Width** -Attribut gibt die Breite des-Steuer Elements an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="23e62-105">The **width** attribute specifies or retrieves the width of the control.</span></span>

``` syntax
        elementID.width
```

## <a name="possible-values"></a><span data-ttu-id="23e62-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="23e62-106">Possible Values</span></span>

<span data-ttu-id="23e62-107">Dieses Attribut ist eine 16-Bit- **Ganzzahl** mit Lese-/Schreibzugriff (0 bis 32.767), die die Breite des Steuer Elements in Pixel darstellt.</span><span class="sxs-lookup"><span data-stu-id="23e62-107">This attribute is a read/write 16-bit **Integer** (0 to 32,767) representing the width of the control in pixels.</span></span> <span data-ttu-id="23e62-108">Der Standardwert ist 0 (null) oder die Breite des Bilds, das im **Image** -Attribut des Steuer Elements angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="23e62-108">The default value is zero or the width of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="23e62-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23e62-109">Remarks</span></span>

<span data-ttu-id="23e62-110">Wenn die angegebene Breite schmaler als die Breite des bereitgestellten Bilds ist, wird das Bild abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="23e62-110">If the width specified is narrower than the width of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="23e62-111">Wenn die Breite größer als die Breite des Bilds ist, geht der Klick Bereich über die Bild Begrenzung hinaus.</span><span class="sxs-lookup"><span data-stu-id="23e62-111">If the width is wider than the width of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="23e62-112">Unabhängig davon, welcher Wert diesem Attribut zugewiesen wird, kann das Bild nicht über seine übergeordnete **Ansicht** oder **unter Ansicht** hinaus wachsen.</span><span class="sxs-lookup"><span data-stu-id="23e62-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="23e62-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23e62-113">Requirements</span></span>



| <span data-ttu-id="23e62-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23e62-114">Requirement</span></span> | <span data-ttu-id="23e62-115">Wert</span><span class="sxs-lookup"><span data-stu-id="23e62-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="23e62-116">Version</span><span class="sxs-lookup"><span data-stu-id="23e62-116">Version</span></span><br/> | <span data-ttu-id="23e62-117">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="23e62-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23e62-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23e62-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e62-119">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="23e62-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





