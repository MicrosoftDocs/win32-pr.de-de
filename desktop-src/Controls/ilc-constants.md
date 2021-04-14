---
title: Abbild Listen-erstellungsflags (shlobj. h)
description: Der Satz von Bitflags, der den Typ der zu erstellenden Bildliste angibt. Dieser Parameter kann eine Kombination der folgenden Werte sein, kann jedoch nur einen der ILC- \_ Farbwerte enthalten. Wird von ImageList \_ Create und IImageList2 Initialize verwendet.
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27f9a83c119b8e201ba41c002bf7c166ba3e4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476317"
---
# <a name="image-list-creation-flags"></a><span data-ttu-id="8708c-105">Abbild Listen-Erstellungs Flags</span><span class="sxs-lookup"><span data-stu-id="8708c-105">Image List Creation Flags</span></span>

<span data-ttu-id="8708c-106">Der Satz von Bitflags, der den Typ der zu erstellenden Bildliste angibt.</span><span class="sxs-lookup"><span data-stu-id="8708c-106">The set of bit flags that specifies the type of image list to create.</span></span> <span data-ttu-id="8708c-107">Dieser Parameter kann eine Kombination der folgenden Werte sein, kann jedoch nur einen der ILC- \_ Farbwerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="8708c-107">This parameter can be a combination of the following values, but it can include only one of the ILC\_COLOR values.</span></span> <span data-ttu-id="8708c-108">Wird von [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) und [**IImageList2:: Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize)verwendet.</span><span class="sxs-lookup"><span data-stu-id="8708c-108">Used by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) and [**IImageList2::Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).</span></span>



| <span data-ttu-id="8708c-109">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="8708c-109">Constant/value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="8708c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8708c-110">Description</span></span>                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <span data-ttu-id="8708c-111"><dt>**ILC \_ Maske**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-111"><dt>**ILC\_MASK**</dt> <dt>0x00000001</dt></span></span> </dl>                                     | <span data-ttu-id="8708c-112">Verwenden Sie eine Maske.</span><span class="sxs-lookup"><span data-stu-id="8708c-112">Use a mask.</span></span> <span data-ttu-id="8708c-113">Die Bildliste enthält zwei Bitmaps, von denen eine eine monochrome Bitmap ist, die als Maske verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8708c-113">The image list contains two bitmaps, one of which is a monochrome bitmap used as a mask.</span></span> <span data-ttu-id="8708c-114">Wenn dieser Wert nicht eingeschlossen ist, enthält die Bildliste nur eine Bitmap.</span><span class="sxs-lookup"><span data-stu-id="8708c-114">If this value is not included, the image list contains only one bitmap.</span></span><br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <span data-ttu-id="8708c-115"><dt>**ILC \_ Farbe**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-115"><dt>**ILC\_COLOR**</dt> <dt>0x00000000</dt></span></span> </dl>                                  | <span data-ttu-id="8708c-116">Verwenden Sie das Standardverhalten, wenn keines der anderen ILC \_ ColorX-Flags angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8708c-116">Use the default behavior if none of the other ILC\_COLORx flags is specified.</span></span> <span data-ttu-id="8708c-117">In der Regel ist der Standardwert ILC \_ COLOR4, aber für ältere Anzeigetreiber lautet der Standardwert ILC \_ colorddb.</span><span class="sxs-lookup"><span data-stu-id="8708c-117">Typically, the default is ILC\_COLOR4, but for older display drivers, the default is ILC\_COLORDDB.</span></span><br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <span data-ttu-id="8708c-118"><dt>**ILC \_ Colorddb**</dt> <dt>0x000000FE</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-118"><dt>**ILC\_COLORDDB**</dt> <dt>0x000000FE</dt></span></span> </dl>                         | <span data-ttu-id="8708c-119">Verwenden Sie eine Geräte abhängige Bitmap.</span><span class="sxs-lookup"><span data-stu-id="8708c-119">Use a device-dependent bitmap.</span></span><br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <span data-ttu-id="8708c-120"><dt>**ILC \_ COLOR4**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-120"><dt>**ILC\_COLOR4**</dt> <dt>0x00000004</dt></span></span> </dl>                               | <span data-ttu-id="8708c-121">Verwenden Sie einen 4-Bit-Abschnitt (16-farbig) geräteunabhängige Bitmap (DIB) als Bitmap für die Bildliste.</span><span class="sxs-lookup"><span data-stu-id="8708c-121">Use a 4-bit (16-color) device-independent bitmap (DIB) section as the bitmap for the image list.</span></span><br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <span data-ttu-id="8708c-122"><dt>**ILC \_ COLOR8**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-122"><dt>**ILC\_COLOR8**</dt> <dt>0x00000008</dt></span></span> </dl>                               | <span data-ttu-id="8708c-123">Verwenden Sie einen 8-Bit-DIB-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="8708c-123">Use an 8-bit DIB section.</span></span> <span data-ttu-id="8708c-124">Die Farben, die für die Farbtabelle verwendet werden, entsprechen den Farben der halbftone-Palette.</span><span class="sxs-lookup"><span data-stu-id="8708c-124">The colors used for the color table are the same colors as the halftone palette.</span></span><br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <span data-ttu-id="8708c-125"><dt>**ILC \_ COLOR16**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-125"><dt>**ILC\_COLOR16**</dt> <dt>0x00000010</dt></span></span> </dl>                            | <span data-ttu-id="8708c-126">Verwenden Sie einen 16-Bit-DIB-Abschnitt (32/64K-Color).</span><span class="sxs-lookup"><span data-stu-id="8708c-126">Use a 16-bit (32/64k-color) DIB section.</span></span><br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <span data-ttu-id="8708c-127"><dt>**ILC \_ COLOR24**</dt> <dt>0x00000018</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-127"><dt>**ILC\_COLOR24**</dt> <dt>0x00000018</dt></span></span> </dl>                            | <span data-ttu-id="8708c-128">Verwenden Sie einen 24-Bit-DIB-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="8708c-128">Use a 24-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <span data-ttu-id="8708c-129"><dt>**ILC \_ COLOR32**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-129"><dt>**ILC\_COLOR32**</dt> <dt>0x00000020</dt></span></span> </dl>                            | <span data-ttu-id="8708c-130">Verwenden Sie einen 32-Bit-DIB-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="8708c-130">Use a 32-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <span data-ttu-id="8708c-131"><dt>**ILC \_ Palette**</dt> <dt>0x00000800</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-131"><dt>**ILC\_PALETTE**</dt> <dt>0x00000800</dt></span></span> </dl>                            | <span data-ttu-id="8708c-132">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8708c-132">Not implemented.</span></span><br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <span data-ttu-id="8708c-133"><dt>**ILC \_ Spiegelung**</dt> <dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-133"><dt>**ILC\_MIRROR**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="8708c-134">Spiegelung der enthaltenen Symbole, wenn der Prozess gespiegelt wird</span><span class="sxs-lookup"><span data-stu-id="8708c-134">Mirror the icons contained, if the process is mirrored</span></span><br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <span data-ttu-id="8708c-135"><dt>**ILC \_ Peritemmirror**</dt> <dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-135"><dt>**ILC\_PERITEMMIRROR**</dt> <dt>0x00008000</dt></span></span> </dl>          | <span data-ttu-id="8708c-136">Bewirkt, dass der Spiegelungs Code jedes Element Spiegelung, wenn ein Satz von Bildern eingefügt wird, im Vergleich zum gesamten Strip.</span><span class="sxs-lookup"><span data-stu-id="8708c-136">Causes the mirroring code to mirror each item when inserting a set of images, versus the whole strip.</span></span><br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <span data-ttu-id="8708c-137"><dt>**ILC \_ OriginalSize**</dt> <dt>0x00010000 bis</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-137"><dt>**ILC\_ORIGINALSIZE**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="8708c-138">**Windows Vista und höher.**</span><span class="sxs-lookup"><span data-stu-id="8708c-138">**Windows Vista and later.**</span></span> <span data-ttu-id="8708c-139">ImageList sollte kleiner als festgelegte Images annehmen und die ursprüngliche Größe basierend auf dem hinzugefügten Image anwenden.</span><span class="sxs-lookup"><span data-stu-id="8708c-139">Imagelist should accept smaller than set images and apply original size based on image added.</span></span><br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <span data-ttu-id="8708c-140"><dt>**ILC \_ Highqualityscale**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-140"><dt>**ILC\_HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="8708c-141">**Windows Vista und höher.**</span><span class="sxs-lookup"><span data-stu-id="8708c-141">**Windows Vista and later.**</span></span> <span data-ttu-id="8708c-142">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="8708c-142">Reserved.</span></span><br/>                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="8708c-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8708c-143">Requirements</span></span>



| <span data-ttu-id="8708c-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8708c-144">Requirement</span></span> | <span data-ttu-id="8708c-145">Wert</span><span class="sxs-lookup"><span data-stu-id="8708c-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8708c-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8708c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8708c-147">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8708c-147">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8708c-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8708c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8708c-149">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8708c-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8708c-150">Header</span><span class="sxs-lookup"><span data-stu-id="8708c-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="8708c-151"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="8708c-151"><dt>Shlobj.h</dt></span></span> </dl> |



 

 





