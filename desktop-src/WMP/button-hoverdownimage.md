---
title: Button. hoverdownimage
description: Das hoverdownimage-Attribut gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die Schaltfläche im Zustand "gedrückt" befindet und der Benutzer mit dem Mauszeiger darüber bewegt wird.
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- Button. hoverdownimage-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bc8221875656c38a35eb6539dce25f58133984f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372258"
---
# <a name="buttonhoverdownimage"></a><span data-ttu-id="461bb-104">Button. hoverdownimage</span><span class="sxs-lookup"><span data-stu-id="461bb-104">BUTTON.hoverDownImage</span></span>

<span data-ttu-id="461bb-105">Das **hoverdownimage** -Attribut gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die **Schaltfläche** im Zustand "gedrückt" befindet und der Benutzer mit dem Mauszeiger darüber bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="461bb-105">The **hoverDownImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the down state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="461bb-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="461bb-106">Possible Values</span></span>

<span data-ttu-id="461bb-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen der Bilddatei enthält</span><span class="sxs-lookup"><span data-stu-id="461bb-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="461bb-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="461bb-108">Remarks</span></span>

<span data-ttu-id="461bb-109">Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.</span><span class="sxs-lookup"><span data-stu-id="461bb-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="461bb-110">Das Standard Image ist das im " **downImage** "-Attribut angegebene Standard Image oder der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="461bb-110">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="461bb-111">Wenn das Hover-Bild größer als der definierte Bereich im Ambient-Attribut ist, wird das Bild mit dem Mauszeiger abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="461bb-111">If the hover-down image is larger than the defined region in the ambient attribute, the hover-down image will be cropped.</span></span>

<span data-ttu-id="461bb-112">Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="461bb-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="461bb-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="461bb-113">Requirements</span></span>



| <span data-ttu-id="461bb-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="461bb-114">Requirement</span></span> | <span data-ttu-id="461bb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="461bb-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="461bb-116">Version</span><span class="sxs-lookup"><span data-stu-id="461bb-116">Version</span></span><br/> | <span data-ttu-id="461bb-117">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="461bb-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="461bb-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="461bb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="461bb-119">**Button-Element**</span><span class="sxs-lookup"><span data-stu-id="461bb-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="461bb-120">**Button. downImage**</span><span class="sxs-lookup"><span data-stu-id="461bb-120">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





