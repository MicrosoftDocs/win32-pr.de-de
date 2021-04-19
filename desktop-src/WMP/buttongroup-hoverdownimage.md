---
title: ButtonGroup. hoverdownimage
description: Das hoverdownimage-Attribut gibt den Namen des Bilds an oder Ruft den Namen des Bilds ab, das den Hover-Down-Zustand einer Schaltfläche in der ButtonGroup darstellt. Der Hover-Down-Zustand tritt auf, wenn sich die Schaltfläche im Zustand "gedrückt" befindet und der Benutzer mit der Maus darauf zeigt.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- ButtonGroup. hoverdownimage-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a40788fafffd6eb4626bc834a941f7330c988fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353789"
---
# <a name="buttongrouphoverdownimage"></a><span data-ttu-id="611ee-105">ButtonGroup. hoverdownimage</span><span class="sxs-lookup"><span data-stu-id="611ee-105">BUTTONGROUP.hoverDownImage</span></span>

<span data-ttu-id="611ee-106">Das **hoverdownimage** -Attribut gibt den Namen des Bilds an oder Ruft den Namen des Bilds ab, das den Hover-Down-Zustand einer Schaltfläche in der **ButtonGroup** darstellt.</span><span class="sxs-lookup"><span data-stu-id="611ee-106">The **hoverDownImage** attribute specifies or retrieves the name of the image representing the hover-down state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="611ee-107">Der Hover-Down-Zustand tritt auf, wenn sich die Schaltfläche im Zustand "gedrückt" befindet und der Benutzer mit der Maus darauf zeigt.</span><span class="sxs-lookup"><span data-stu-id="611ee-107">The hover-down state occurs when the button is in the down state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="611ee-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="611ee-108">Possible Values</span></span>

<span data-ttu-id="611ee-109">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="611ee-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="611ee-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="611ee-110">Remarks</span></span>

<span data-ttu-id="611ee-111">Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.</span><span class="sxs-lookup"><span data-stu-id="611ee-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="611ee-112">Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können seine Farbton-und Sättigungswerte mithilfe der Attribute **hueshift** und **Sättigung** dynamisch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="611ee-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="611ee-113">Das Standard Image ist das im " **downImage** "-Attribut angegebene Standard Image oder der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="611ee-113">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="611ee-114">Wenn das Bild mit dem Mauszeiger größer als der definierte Bereich ist, wird das Bild mit dem Mauszeiger abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="611ee-114">If the hover-down image is larger than the defined region, the hover-down image will be cropped.</span></span>

<span data-ttu-id="611ee-115">Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="611ee-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="611ee-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="611ee-116">Requirements</span></span>



| <span data-ttu-id="611ee-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="611ee-117">Requirement</span></span> | <span data-ttu-id="611ee-118">Wert</span><span class="sxs-lookup"><span data-stu-id="611ee-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="611ee-119">Version</span><span class="sxs-lookup"><span data-stu-id="611ee-119">Version</span></span><br/> | <span data-ttu-id="611ee-120">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="611ee-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="611ee-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="611ee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="611ee-122">**ButtonGroup-Element**</span><span class="sxs-lookup"><span data-stu-id="611ee-122">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="611ee-123">**ButtonGroup. downImage**</span><span class="sxs-lookup"><span data-stu-id="611ee-123">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> <dt>

[<span data-ttu-id="611ee-124">**ButtonGroup. hueshift**</span><span class="sxs-lookup"><span data-stu-id="611ee-124">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="611ee-125">**ButtonGroup. Sättigung**</span><span class="sxs-lookup"><span data-stu-id="611ee-125">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





