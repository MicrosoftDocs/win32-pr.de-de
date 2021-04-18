---
title: ButtonGroup. Image
description: Das Image-Attribut gibt den Namen des Bilds an, das die Schaltflächen einer ButtonGroup darstellt, oder ruft ihn ab.
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- ButtonGroup. Image-Windows-Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa395edc149671ad05a38a5ff7c77053b6e3d82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361677"
---
# <a name="buttongroupimage"></a><span data-ttu-id="02eb0-104">ButtonGroup. Image</span><span class="sxs-lookup"><span data-stu-id="02eb0-104">BUTTONGROUP.image</span></span>

<span data-ttu-id="02eb0-105">Das **Image** -Attribut gibt den Namen des Bilds an, das die Schaltflächen einer **ButtonGroup** darstellt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="02eb0-105">The **image** attribute specifies or retrieves the name of the image representing the buttons of a **BUTTONGROUP**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="02eb0-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="02eb0-106">Possible Values</span></span>

<span data-ttu-id="02eb0-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="02eb0-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="02eb0-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02eb0-108">Remarks</span></span>

<span data-ttu-id="02eb0-109">Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.</span><span class="sxs-lookup"><span data-stu-id="02eb0-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="02eb0-110">Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können seine Farbton-und Sättigungswerte mithilfe der Attribute **hueshift** und **Sättigung** dynamisch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="02eb0-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="02eb0-111">Wenn das Bild des Steuer Elements größer als der definierte Bereich ist, wird das Bild beschnitten.</span><span class="sxs-lookup"><span data-stu-id="02eb0-111">If the image of the control is larger than the defined region, the image will be cropped.</span></span>

<span data-ttu-id="02eb0-112">Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="02eb0-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="02eb0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02eb0-113">Requirements</span></span>



| <span data-ttu-id="02eb0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02eb0-114">Requirement</span></span> | <span data-ttu-id="02eb0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="02eb0-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="02eb0-116">Version</span><span class="sxs-lookup"><span data-stu-id="02eb0-116">Version</span></span><br/> | <span data-ttu-id="02eb0-117">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="02eb0-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02eb0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02eb0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02eb0-119">**ButtonGroup-Element**</span><span class="sxs-lookup"><span data-stu-id="02eb0-119">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="02eb0-120">**ButtonGroup. hueshift**</span><span class="sxs-lookup"><span data-stu-id="02eb0-120">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="02eb0-121">**ButtonGroup. Sättigung**</span><span class="sxs-lookup"><span data-stu-id="02eb0-121">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





