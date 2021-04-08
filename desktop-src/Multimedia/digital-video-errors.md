---
title: Digital-Video Fehler
description: Digital-Video Fehler
ms.assetid: 177436fc-543f-4692-8281-1555c1fa21b0
keywords:
- Mcierr-Rückgabewerte, Digital-Video-Fehler
- Multimedia-Referenz, Digital-Video-Fehler
- Referenz für Multimedia-, Digital-Video-Fehler
- Media Control Interface (MCI), Digital-Video-Fehler
- MCI (Media Control Interface), Digital-Video-Fehler
- Referenz für MCI, Digital-Video-Fehler
- MCI-Referenz, Digital-Video-Fehler
- Media Control Interface (MCI), Fehler
- MCI (Medien Steuerungs Schnittstelle), Fehler
- Referenz für MCI, Fehler
- MCI-Referenz, Fehler
- Digital-Video-Fehler
- MCI Digital-Video-Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6938330d15777ed867bf7d151a9d626e60b28646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713224"
---
# <a name="digital-video-errors"></a><span data-ttu-id="9f63a-116">Digital-Video Fehler</span><span class="sxs-lookup"><span data-stu-id="9f63a-116">Digital-Video Errors</span></span>

<span data-ttu-id="9f63a-117">Die folgenden zusätzlichen Rückgabewerte werden für Digital Video-Geräte definiert:</span><span class="sxs-lookup"><span data-stu-id="9f63a-117">The following additional return values are defined for digital-video devices:</span></span>



| <span data-ttu-id="9f63a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9f63a-118">Value</span></span>                           | <span data-ttu-id="9f63a-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9f63a-119">Meaning</span></span>                                                         |
|---------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="9f63a-120">MCIAVI \_ ProductName</span><span class="sxs-lookup"><span data-stu-id="9f63a-120">MCIAVI\_PRODUCTNAME</span></span>             | <span data-ttu-id="9f63a-121">Video</span><span class="sxs-lookup"><span data-stu-id="9f63a-121">Video</span></span>                                                           |
| <span data-ttu-id="9f63a-122">mcierr \_ AVI \_ audioerror</span><span class="sxs-lookup"><span data-stu-id="9f63a-122">MCIERR\_AVI\_AUDIOERROR</span></span>         | <span data-ttu-id="9f63a-123">Unbekannter Fehler beim Versuch, Audioinhalte wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="9f63a-123">Unknown error while attempting to play audio.</span></span>                   |
| <span data-ttu-id="9f63a-124">mcierr \_ AVI \_ badpalette</span><span class="sxs-lookup"><span data-stu-id="9f63a-124">MCIERR\_AVI\_BADPALETTE</span></span>         | <span data-ttu-id="9f63a-125">Wechsel zur neuen Palette nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="9f63a-125">Unable to switch to new palette.</span></span>                                |
| <span data-ttu-id="9f63a-126">mcierr \_ AVI \_ cantplayfullscreen</span><span class="sxs-lookup"><span data-stu-id="9f63a-126">MCIERR\_AVI\_CANTPLAYFULLSCREEN</span></span> | <span data-ttu-id="9f63a-127">Diese AVI-Datei kann nicht im Vollbildmodus abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="9f63a-127">This AVI file cannot be played in full screen mode.</span></span>             |
| <span data-ttu-id="9f63a-128">mcierr \_ AVI \_ displayerror</span><span class="sxs-lookup"><span data-stu-id="9f63a-128">MCIERR\_AVI\_DISPLAYERROR</span></span>       | <span data-ttu-id="9f63a-129">Unbekannter Fehler beim Versuch, Video anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9f63a-129">Unknown error while attempting to display video.</span></span>                |
| <span data-ttu-id="9f63a-130">mcierr \_ AVI \_ nokompressor</span><span class="sxs-lookup"><span data-stu-id="9f63a-130">MCIERR\_AVI\_NOCOMPRESSOR</span></span>       | <span data-ttu-id="9f63a-131">Der installierbare Kompressor, der zum Abspielen dieser Datei erforderlich ist, kann</span><span class="sxs-lookup"><span data-stu-id="9f63a-131">Can't locate installable compressor needed to play this file.</span></span>   |
| <span data-ttu-id="9f63a-132">mcierr \_ AVI \_ nodispdib</span><span class="sxs-lookup"><span data-stu-id="9f63a-132">MCIERR\_AVI\_NODISPDIB</span></span>          | <span data-ttu-id="9f63a-133">256 Farben-VGA-Modus nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9f63a-133">256 color VGA mode not available.</span></span>                               |
| <span data-ttu-id="9f63a-134">mcierr \_ AVI \_ notinterleaved</span><span class="sxs-lookup"><span data-stu-id="9f63a-134">MCIERR\_AVI\_NOTINTERLEAVED</span></span>     | <span data-ttu-id="9f63a-135">Diese AVI-Datei ist nicht verschachtelt.</span><span class="sxs-lookup"><span data-stu-id="9f63a-135">This AVI file is not interleaved.</span></span>                               |
| <span data-ttu-id="9f63a-136">mcierr \_ AVI \_ oldaviformat</span><span class="sxs-lookup"><span data-stu-id="9f63a-136">MCIERR\_AVI\_OLDAVIFORMAT</span></span>       | <span data-ttu-id="9f63a-137">Diese AVI-Datei hat ein veraltetes Format.</span><span class="sxs-lookup"><span data-stu-id="9f63a-137">This AVI file is of an obsolete format.</span></span>                         |
| <span data-ttu-id="9f63a-138">mcierr \_ AVI \_ toobigforvga</span><span class="sxs-lookup"><span data-stu-id="9f63a-138">MCIERR\_AVI\_TOOBIGFORVGA</span></span>       | <span data-ttu-id="9f63a-139">Diese AVI-Datei ist zu groß, um im ausgewählten VGA-Modus wiedergegeben zu werden.</span><span class="sxs-lookup"><span data-stu-id="9f63a-139">This AVI file is too big to be played in the selected VGA mode.</span></span> |



 

 

 




