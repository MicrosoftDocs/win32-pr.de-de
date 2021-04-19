---
title: View. BackgroundImage
description: Das BackgroundImage-Attribut gibt das Hintergrundbild der Ansicht oder unter Ansicht an oder ruft es ab.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- Anzeigen von BackgroundImage-Windows-Media Player
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96f4a93882e02589d7f15b74ba5cb225f506d69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352891"
---
# <a name="viewbackgroundimage"></a><span data-ttu-id="75a95-104">View. BackgroundImage</span><span class="sxs-lookup"><span data-stu-id="75a95-104">VIEW.backgroundImage</span></span>

<span data-ttu-id="75a95-105">Das **BackgroundImage** -Attribut gibt das Hintergrundbild der **Ansicht** oder **unter Ansicht** an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="75a95-105">The **backgroundImage** attribute specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="75a95-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="75a95-106">Possible Values</span></span>

<span data-ttu-id="75a95-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="75a95-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="75a95-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75a95-108">Remarks</span></span>

<span data-ttu-id="75a95-109">Die unterstützten Formate sind BMP, JPG, GIF und PNG.</span><span class="sxs-lookup"><span data-stu-id="75a95-109">The supported formats are BMP, JPG, GIF, and PNG.</span></span> <span data-ttu-id="75a95-110">Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können seine Farbton-und Sättigungswerte mithilfe der **backgroundimagehueshift** -und **backgroundimagesationtribute** -Attribute dynamisch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="75a95-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **backgroundImageHueShift** and **backgroundImageSaturation** attributes.</span></span>

<span data-ttu-id="75a95-111">Wenn Sie in einem Windows Media-Download Paket das **BackgroundImage** -Attribut für ein **Ansichts** Element angeben, müssen Sie auch das **BackgroundColor** -Attribut für dieses Element angeben.</span><span class="sxs-lookup"><span data-stu-id="75a95-111">In a Windows Media Download package, if you specify the **backgroundImage** attribute for a **VIEW** element, then you must also specify the **backgroundColor** attribute for that element.</span></span>

## <a name="requirements"></a><span data-ttu-id="75a95-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75a95-112">Requirements</span></span>



| <span data-ttu-id="75a95-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75a95-113">Requirement</span></span> | <span data-ttu-id="75a95-114">Wert</span><span class="sxs-lookup"><span data-stu-id="75a95-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="75a95-115">Version</span><span class="sxs-lookup"><span data-stu-id="75a95-115">Version</span></span><br/> | <span data-ttu-id="75a95-116">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="75a95-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75a95-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75a95-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75a95-118">**View-Element**</span><span class="sxs-lookup"><span data-stu-id="75a95-118">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="75a95-119">**View. backgroundimagehueshift**</span><span class="sxs-lookup"><span data-stu-id="75a95-119">**VIEW.backgroundImageHueShift**</span></span>](view-backgroundimagehueshift.md)
</dt> <dt>

[<span data-ttu-id="75a95-120">**View. backgroundimagesationations**</span><span class="sxs-lookup"><span data-stu-id="75a95-120">**VIEW.backgroundImageSaturation**</span></span>](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





