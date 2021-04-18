---
title: Button. hoverimage
description: Das hoverimage-Attribut gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die Schaltfläche im Zustand "up" befindet, und der Benutzer mit dem Mauszeiger darauf zeigt.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- Button. hoverimage-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80b17a461ffde4b9f6777f3ce360c6b3f1747235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364833"
---
# <a name="buttonhoverimage"></a><span data-ttu-id="c1e8a-104">Button. hoverimage</span><span class="sxs-lookup"><span data-stu-id="c1e8a-104">BUTTON.hoverImage</span></span>

<span data-ttu-id="c1e8a-105">Das **hoverimage** -Attribut gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die **Schaltfläche** im Zustand "up" befindet, und der Benutzer mit dem Mauszeiger darauf zeigt.</span><span class="sxs-lookup"><span data-stu-id="c1e8a-105">The **hoverImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the up state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="c1e8a-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="c1e8a-106">Possible Values</span></span>

<span data-ttu-id="c1e8a-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen der Bilddatei enthält</span><span class="sxs-lookup"><span data-stu-id="c1e8a-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1e8a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1e8a-108">Remarks</span></span>

<span data-ttu-id="c1e8a-109">Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.</span><span class="sxs-lookup"><span data-stu-id="c1e8a-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="c1e8a-110">Das Standardbild ist das im **Image** -Attribut angegebene oder sein Standardbild.</span><span class="sxs-lookup"><span data-stu-id="c1e8a-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="c1e8a-111">Wenn das Hover-Bild größer als der definierte Bereich im Ambient-Attribut ist, wird das Hover-Bild beschnitten.</span><span class="sxs-lookup"><span data-stu-id="c1e8a-111">If the hover image is larger than the defined region in the ambient attribute, the hover image will be cropped.</span></span>

<span data-ttu-id="c1e8a-112">Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1e8a-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1e8a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1e8a-113">Requirements</span></span>



| <span data-ttu-id="c1e8a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1e8a-114">Requirement</span></span> | <span data-ttu-id="c1e8a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c1e8a-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c1e8a-116">Version</span><span class="sxs-lookup"><span data-stu-id="c1e8a-116">Version</span></span><br/> | <span data-ttu-id="c1e8a-117">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c1e8a-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1e8a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1e8a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1e8a-119">**Button-Element**</span><span class="sxs-lookup"><span data-stu-id="c1e8a-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="c1e8a-120">**Button. Bild**</span><span class="sxs-lookup"><span data-stu-id="c1e8a-120">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





