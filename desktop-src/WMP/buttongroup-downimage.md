---
title: ButtonGroup. downImage
description: Das downImage-Attribut gibt den Namen des Bilds an oder Ruft den Namen des Bilds ab, das den Zustand der ButtonGroup darstellt.
ms.assetid: 022e77e7-d3c0-41b5-984a-84d016a5a25a
keywords:
- ButtonGroup. downImage-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b8a1d5bc2f4c68894a3bba1ad8ce9f2b3aa28a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352961"
---
# <a name="buttongroupdownimage"></a><span data-ttu-id="f78f5-104">ButtonGroup. downImage</span><span class="sxs-lookup"><span data-stu-id="f78f5-104">BUTTONGROUP.downImage</span></span>

<span data-ttu-id="f78f5-105">Das **downImage** -Attribut gibt den Namen des Bilds an oder Ruft den Namen des Bilds ab, das den Zustand der **ButtonGroup** darstellt.</span><span class="sxs-lookup"><span data-stu-id="f78f5-105">The **downImage** attribute specifies or retrieves the name of the image representing the down state of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="f78f5-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f78f5-106">Possible Values</span></span>

<span data-ttu-id="f78f5-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="f78f5-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f78f5-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f78f5-108">Remarks</span></span>

<span data-ttu-id="f78f5-109">Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.</span><span class="sxs-lookup"><span data-stu-id="f78f5-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="f78f5-110">Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können seine Farbton-und Sättigungswerte mithilfe der Attribute **hueshift** und **Sättigung** dynamisch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f78f5-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="f78f5-111">Das Standard Image ist das im **Image** -Attribut angegebene.</span><span class="sxs-lookup"><span data-stu-id="f78f5-111">The default image is the one specified in the **image** attribute.</span></span>

<span data-ttu-id="f78f5-112">Wenn das Abbild größer als der definierte Bereich ist, wird das Bild mit dem Bild abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="f78f5-112">If the down image is larger than the defined region, the down image will be cropped.</span></span>

<span data-ttu-id="f78f5-113">Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f78f5-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f78f5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f78f5-114">Requirements</span></span>



| <span data-ttu-id="f78f5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f78f5-115">Requirement</span></span> | <span data-ttu-id="f78f5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f78f5-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f78f5-117">Version</span><span class="sxs-lookup"><span data-stu-id="f78f5-117">Version</span></span><br/> | <span data-ttu-id="f78f5-118">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="f78f5-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f78f5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f78f5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f78f5-120">**ButtonGroup-Element**</span><span class="sxs-lookup"><span data-stu-id="f78f5-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="f78f5-121">**ButtonGroup. hueshift**</span><span class="sxs-lookup"><span data-stu-id="f78f5-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="f78f5-122">**ButtonGroup. Image**</span><span class="sxs-lookup"><span data-stu-id="f78f5-122">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="f78f5-123">**ButtonGroup. Sättigung**</span><span class="sxs-lookup"><span data-stu-id="f78f5-123">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





