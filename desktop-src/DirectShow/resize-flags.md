---
description: Diese Flags geben an, wie eine Videoquelle gerendert wird, wenn ihre Größe nicht den Ausgabe Dimensionen entspricht.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Größenänderung von Flags ("qedit. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RESIZEF_STRETCH
- RESIZEF_CROP
- RESIZEF_PRESERVEASPECTRATIO
- RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 9e2ef2766f7f54fea4fad16fc26242a8c2ee08db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371243"
---
# <a name="resize-flags"></a><span data-ttu-id="3a178-103">Größenänderung von Flags</span><span class="sxs-lookup"><span data-stu-id="3a178-103">Resize Flags</span></span>

<span data-ttu-id="3a178-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3a178-104">\[Deprecated.</span></span> <span data-ttu-id="3a178-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="3a178-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="3a178-106">Diese Flags geben an, wie eine Videoquelle gerendert wird, wenn ihre Größe nicht den Ausgabe Dimensionen entspricht.</span><span class="sxs-lookup"><span data-stu-id="3a178-106">These flags specify how a video source is rendered if its size does not match the output dimensions.</span></span>



| <span data-ttu-id="3a178-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="3a178-107">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="3a178-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a178-108">Description</span></span>                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <span data-ttu-id="3a178-109"><dt>**Resizef \_ Stretch**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3a178-109"><dt>**RESIZEF\_STRETCH**</dt> <dt>0</dt></span></span> </dl>                                                                          | <span data-ttu-id="3a178-110">Das Bild wird so gestreckt, dass es der Zielframe Größe in beiden Dimensionen entspricht, ohne das Seitenverhältnis beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="3a178-110">The image is stretched to fit the target frame size in both dimensions, without preserving the aspect ratio.</span></span><br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <span data-ttu-id="3a178-111"><dt>**Resizef \_ Ernte**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3a178-111"><dt>**RESIZEF\_CROP**</dt> <dt>1</dt></span></span> </dl>                                                                                   | <span data-ttu-id="3a178-112">Die Größe des Bilds wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="3a178-112">The image is not resized.</span></span> <span data-ttu-id="3a178-113">Wenn das Bild kleiner als der Zielframe ist, ist der umgebende Bereich schwarz.</span><span class="sxs-lookup"><span data-stu-id="3a178-113">If the image is smaller than the target frame, the surrounding area is black.</span></span> <span data-ttu-id="3a178-114">Wenn das Bild größer als der Zielframe ist, wird das Bild abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="3a178-114">If the image is larger than the target frame, the image is cropped.</span></span><br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <span data-ttu-id="3a178-115"><dt>**Resizef \_ Preserveaspectratio**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3a178-115"><dt>**RESIZEF\_PRESERVEASPECTRATIO**</dt> <dt>2</dt></span></span> </dl>                                      | <span data-ttu-id="3a178-116">Die Größe des Bilds wird so angepasst, dass es an den Zielframe entlang einer Dimension angepasst wird, wobei das Seitenverhältnis beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="3a178-116">The image is resized to fit the target frame along one dimension, while preserving the aspect ratio.</span></span> <span data-ttu-id="3a178-117">Wenn das Verhältnis zwischen Breite und Höhe im Bild nicht mit dem Verhältnis im Zielframe identisch ist, wird ein Letterbox-Wert erstellt.</span><span class="sxs-lookup"><span data-stu-id="3a178-117">If the ratio of width to height in the image does not match the ratio in the target frame, it creates a letterbox.</span></span><br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <span data-ttu-id="3a178-118"><dt>**Resizef \_ Preserveaspectratio \_ noletterbox**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3a178-118"><dt>**RESIZEF\_PRESERVEASPECTRATIO\_NOLETTERBOX**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="3a178-119">Die Größe des Bilds wird geändert, um den gesamten Zielframe auszufüllen und gleichzeitig das Seitenverhältnis beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="3a178-119">The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span> <span data-ttu-id="3a178-120">Anstatt ein Letterbox-Feld zu erstellen, erstellt dieser Modus das Bild entweder entlang der Seite oder über den oberen und unteren Rand.</span><span class="sxs-lookup"><span data-stu-id="3a178-120">Rather than create a letterbox, this mode crops the image, either along the sides or across the top and bottom.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="3a178-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a178-121">Remarks</span></span>

<span data-ttu-id="3a178-122">Die folgenden Abbildungen zeigen die Auswirkungen dieser Flags.</span><span class="sxs-lookup"><span data-stu-id="3a178-122">The following images show the effects of these flags.</span></span>

![Größenänderung von Flags](images/stretch14.png)

## <a name="requirements"></a><span data-ttu-id="3a178-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a178-124">Requirements</span></span>



| <span data-ttu-id="3a178-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a178-125">Requirement</span></span> | <span data-ttu-id="3a178-126">Wert</span><span class="sxs-lookup"><span data-stu-id="3a178-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a178-127">Header</span><span class="sxs-lookup"><span data-stu-id="3a178-127">Header</span></span><br/> | <dl> <span data-ttu-id="3a178-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3a178-128"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a178-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a178-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a178-130">**Iamtimelinesrc:: getstretchmode**</span><span class="sxs-lookup"><span data-stu-id="3a178-130">**IAMTimelineSrc::GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[<span data-ttu-id="3a178-131">**Iamtimelinesrc:: setstretchmode**</span><span class="sxs-lookup"><span data-stu-id="3a178-131">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




