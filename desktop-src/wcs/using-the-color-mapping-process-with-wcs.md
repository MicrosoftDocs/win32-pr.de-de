---
title: Verwenden des Farbzuordnungsprozesses mit WCS
description: Die WCS-Farbzuordnung basiert auf Geräte Profilen.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Windows Color System (WCS), Farbzuordnung
- WCS (Windows Color System), Farbzuordnung
- Bild Farbverwaltung, Farbzuordnung
- Farbverwaltung, Farbzuordnung
- Farben, Farbzuordnung
- Farbzuordnung
- Windows Color System (WCS), Geräteprofile
- WCS (Windows Color System), Geräteprofile
- Bild Farbverwaltung, Geräteprofile
- Farbverwaltung, Geräteprofile
- Farben, Geräteprofile
- Windows Color System (WCS), profile
- WCS (Windows Color System), profile
- Bildfarben Verwaltung, profile
- Farbverwaltung, profile
- Farben, profile
- Geräteprofile
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428b09749f3781def44e56ff6cea0539259d0464
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106351181"
---
# <a name="using-the-color-mapping-process-with-wcs"></a><span data-ttu-id="20e48-120">Verwenden des Farbzuordnungsprozesses mit WCS</span><span class="sxs-lookup"><span data-stu-id="20e48-120">Using The Color Mapping Process with WCS</span></span>

<span data-ttu-id="20e48-121">Die WCS-Farbzuordnung basiert auf [Geräte Profilen](d.md).</span><span class="sxs-lookup"><span data-stu-id="20e48-121">WCS color mapping is based on [device profiles](d.md).</span></span> <span data-ttu-id="20e48-122">Diese werden von Herstellern von Color-Hardware Geräten bereitgestellt und bei der Installation eines Geräts installiert.</span><span class="sxs-lookup"><span data-stu-id="20e48-122">These are supplied by vendors of color hardware devices and installed when a device is installed.</span></span> <span data-ttu-id="20e48-123">Wenn die Farbzuordnung von einem Anwendungsprogramm verwendet wird, greift WCS auf das Geräte Profil des Abbilds zu, um die Informationen zu erhalten, die zum Konvertieren des Abbilds auf den PCs erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="20e48-123">When color mapping is used by an application program, WCS accesses the device profile of the image to get the information needed to convert the image to the PCS.</span></span> <span data-ttu-id="20e48-124">Die Konvertierung erfolgt durch CMM.</span><span class="sxs-lookup"><span data-stu-id="20e48-124">The conversion is done by the CMM.</span></span>

<span data-ttu-id="20e48-125">Ein Geräte Profil kann in das Abbild selbst eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="20e48-125">A device profile can be embedded into the image itself.</span></span> <span data-ttu-id="20e48-126">Das Geräte Profil wird also auch über das Internet mit dem Image bewegt.</span><span class="sxs-lookup"><span data-stu-id="20e48-126">So the device profile travels with the image, even across the Internet.</span></span> <span data-ttu-id="20e48-127">Ein Benutzer benötigt das Quellgerät nicht, um eine exakte Farbzuordnung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="20e48-127">A user does not need the source device to get an accurate color mapping.</span></span> <span data-ttu-id="20e48-128">Wenn ein Image nicht über ein Geräte Profil verfügt, wird der sRGB-Speicherplatz als Standard verwendet.</span><span class="sxs-lookup"><span data-stu-id="20e48-128">If an image does not have a device profile, the sRGB space is used as a default.</span></span> <span data-ttu-id="20e48-129">Weitere Informationen finden Sie unter [Verwenden der Farbverwaltung im Internet](using-color-management-on-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="20e48-129">For more details, see [Using Color Management on the Internet](using-color-management-on-the-internet.md).</span></span>

<span data-ttu-id="20e48-130">Beachten Sie, dass Anwendungen, die WCS verwenden, das sRGB-Profil nie in ein Image einbetten sollten.</span><span class="sxs-lookup"><span data-stu-id="20e48-130">Note that applications which use WCS should never embed the sRGB profile into an image.</span></span> <span data-ttu-id="20e48-131">Der sRGB-Farbraum bietet einen standardisierten Farbraum, der auf allen Geräten portabel ist.</span><span class="sxs-lookup"><span data-stu-id="20e48-131">The sRGB color space provides a standardized color space that is portable across all devices.</span></span> <span data-ttu-id="20e48-132">Es ist automatisch für Benutzer von Windows 98 und höher sowie Windows 2000 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20e48-132">It is automatically available to users of Windows 98 and later as well as Windows 2000 and later.</span></span> <span data-ttu-id="20e48-133">Daher ist es nicht erforderlich, mit dem Image zu reisen.</span><span class="sxs-lookup"><span data-stu-id="20e48-133">Therefore, it does not need to travel with the image.</span></span>

<span data-ttu-id="20e48-134">Nachdem sich die Bildfarben auf den [PCs](p.md)befinden, greift WCS auf das Geräte Profil des Zielgeräts zu.</span><span class="sxs-lookup"><span data-stu-id="20e48-134">After the image colors are in the [PCS](p.md), WCS accesses the device profile of the destination device.</span></span> <span data-ttu-id="20e48-135">Der CMM-Dienst erhält die Umwandlung der Bildfarben von PCs in den Farbskala des Zielgeräts.</span><span class="sxs-lookup"><span data-stu-id="20e48-135">It gets the CMM to convert the image colors from PCS to the gamut of the destination device.</span></span>

<span data-ttu-id="20e48-136">Eine komplexere Farbzuordnung kann auch mit WCS durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="20e48-136">More complex color mapping can also be done with WCS.</span></span> <span data-ttu-id="20e48-137">Beispielsweise kann es verwendet werden, um eine Vorstellung davon zu erhalten, wie ein Bild, das in einer Videoanzeige erstellt wurde, auf einem hochauflösenden Laserdrucker gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="20e48-137">For example, it can be used to get an idea of what an image created on a video display would look like when printed on a high resolution laser printer.</span></span> <span data-ttu-id="20e48-138">Das Beispiel wird komplexer, wenn es nur einen Standard-Inkjet-Drucker gibt, in dem die Vorschau angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="20e48-138">The example gets more complex if there is only a standard inkjet printer on which to preview it.</span></span> <span data-ttu-id="20e48-139">Das Bild kann aus dem Spiel der Anzeige in den Spiel Schirm des Inkjet-Druckers konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="20e48-139">The image can be converted from the gamut of the display, into the gamut of the inkjet printer.</span></span> <span data-ttu-id="20e48-140">Von dort aus kann es in das Spiel des Laserdruckers konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="20e48-140">From there it can converted into the gamut of the laser printer.</span></span> <span data-ttu-id="20e48-141">Das resultierende Bild kann auf dem Inkjet-Drucker gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="20e48-141">The resulting image can be printed on the inkjet printer.</span></span> <span data-ttu-id="20e48-142">Natürlich wäre das Image bei der Ausgabe auf dem Color-Laser-Drucker eine höhere Auflösung.</span><span class="sxs-lookup"><span data-stu-id="20e48-142">Of course the image would be at a higher resolution when printed on the color laser printer.</span></span> <span data-ttu-id="20e48-143">Die Farben des auf dem Inkjet-Drucker gedruckten Druck Abbilds entsprechen jedoch der Farbe, die der Laserdrucker drucken würde.</span><span class="sxs-lookup"><span data-stu-id="20e48-143">However, the colors of the proofing image printed on the inkjet printer would be a close match to the colors that the laser printer would print.</span></span>

<span data-ttu-id="20e48-144">Die Konvertierungen im Beispiel werden durch die Konvertierung der Bildfarben aus dem Farbskala der Anzeige in die PCs konvertiert.</span><span class="sxs-lookup"><span data-stu-id="20e48-144">The way the conversions in the example are accomplished is to convert the image colors from the display's gamut into the PCS.</span></span> <span data-ttu-id="20e48-145">Nachdem die Bildfarben in die PCs konvertiert wurden, wird das Geräte Profil des Inkjet-Druckers verwendet, um Sie in die Fläche des Inkjet-Druckers umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="20e48-145">After the image colors are converted into the PCS, the device profile of the inkjet printer would be used to transform them into the gamut of the inkjet printer.</span></span> <span data-ttu-id="20e48-146">Im nächsten Schritt wird die Transformation für PCs zu PCs verwendet, um die Farben zurück auf die PCs zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="20e48-146">Next, the gamut to PCS transform would be used to move the colors back to the PCS.</span></span> <span data-ttu-id="20e48-147">Von dort aus wird das Geräte Profil des Laserdruckers zum Konvertieren der Farben von PCs in den Spiel-des Laserdruckers verwendet.</span><span class="sxs-lookup"><span data-stu-id="20e48-147">From there, the laser printer's device profile is used to convert the colors from PCS into the gamut of the laser printer.</span></span>

<span data-ttu-id="20e48-148">Durch die Möglichkeit, Farben von einem Geräte Spiel auf PCs und wieder zurück zu transformieren, können Bildfarben, die für ein Farbausgabe Gerät bestimmt sind, auf nahezu jedem anderen Gerät überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="20e48-148">The ability to easily transform colors from a device gamut to the PCS and back again enables image colors intended for one color output device to be proofed on almost any other.</span></span>

<span data-ttu-id="20e48-149">Im vorherigen Beispiel unterscheidet sich die Beschreibung von der eigentlichen Prozedur aus Gründen der Übersichtlichkeit.</span><span class="sxs-lookup"><span data-stu-id="20e48-149">In the preceding example, the description varies from the actual procedure somewhat for clarity.</span></span> <span data-ttu-id="20e48-150">In der Realität werden alle im vorangehenden Absatz erwähnten Transformationen in einer einzigen Transformation verkettet.</span><span class="sxs-lookup"><span data-stu-id="20e48-150">In reality, all of the transformations mentioned in the preceding paragraph would be concatenated into a single transformation.</span></span>

 

 




