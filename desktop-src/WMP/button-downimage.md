---
title: Button. downImage
description: Das downImage-Attribut gibt das Bild an, das den Zustand der Schaltfläche darstellt, oder ruft es ab.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- Button. Fenster Media Player Windows-
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7a405a5df20a04ae9d093f2b28ee4c68cab67d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365183"
---
# <a name="buttondownimage"></a><span data-ttu-id="e6672-104">Button. downImage</span><span class="sxs-lookup"><span data-stu-id="e6672-104">BUTTON.downImage</span></span>

<span data-ttu-id="e6672-105">Das **downImage** -Attribut gibt das Bild an, das den Zustand der **Schaltfläche** darstellt, oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="e6672-105">The **downImage** attribute specifies or retrieves the image representing the down state of the **BUTTON**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="e6672-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="e6672-106">Possible Values</span></span>

<span data-ttu-id="e6672-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen der Bilddatei enthält</span><span class="sxs-lookup"><span data-stu-id="e6672-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6672-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6672-108">Remarks</span></span>

<span data-ttu-id="e6672-109">Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.</span><span class="sxs-lookup"><span data-stu-id="e6672-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="e6672-110">Das Standardbild ist das im **Image** -Attribut angegebene oder sein Standardbild.</span><span class="sxs-lookup"><span data-stu-id="e6672-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="e6672-111">Wenn das nach-unten-Bild größer als der definierte Bereich im Ambient-Attribut ist, wird das Bild mit dem Bild abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="e6672-111">If the down image is larger than the defined region in the ambient attribute, the down image will be cropped.</span></span>

<span data-ttu-id="e6672-112">Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6672-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6672-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6672-113">Requirements</span></span>



| <span data-ttu-id="e6672-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6672-114">Requirement</span></span> | <span data-ttu-id="e6672-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e6672-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e6672-116">Version</span><span class="sxs-lookup"><span data-stu-id="e6672-116">Version</span></span><br/> | <span data-ttu-id="e6672-117">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e6672-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6672-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6672-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6672-119">**Button-Element**</span><span class="sxs-lookup"><span data-stu-id="e6672-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="e6672-120">**Schaltfläche. nach unten**</span><span class="sxs-lookup"><span data-stu-id="e6672-120">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="e6672-121">**Button. Bild**</span><span class="sxs-lookup"><span data-stu-id="e6672-121">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





