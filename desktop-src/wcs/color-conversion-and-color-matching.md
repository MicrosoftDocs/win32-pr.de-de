---
title: Farbkonvertierung und Farbübereinstimmung
description: Der Prozess der Konvertierung von Farben von einem Farb Raum in einen anderen wird als Farbkonvertierung bezeichnet.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Windows Color System (WCS), Farbkonvertierung
- WCS (Windows Color System), Farbkonvertierung
- Bild Farbverwaltung, Farbkonvertierung
- Farbverwaltung, Farbkonvertierung
- Farben, Farbkonvertierung
- Farbkonvertierung
- Windows Color System (WCS), Farbabgleich
- WCS (Windows Color System), Farbabgleich
- Bild Farbverwaltung, Farbabgleich
- Farbverwaltung, Farb Übereinstimmung
- Farben, Farb Übereinstimmung
- Farb Übereinstimmung
- Windows Color System (WCS), Farbzuordnung
- WCS (Windows Color System), Farbzuordnung
- Bild Farbverwaltung, Farbzuordnung
- Farbverwaltung, Farbzuordnung
- Farben, Farbzuordnung
- Farbzuordnung
- weißer Punkt
- Colorants
- Gammakorrektur
- Farbskala
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74de95238472f58d49c5033a601c6d5458773c8
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106355086"
---
# <a name="color-conversion-and-color-matching"></a><span data-ttu-id="8df66-125">Farbkonvertierung und Farbübereinstimmung</span><span class="sxs-lookup"><span data-stu-id="8df66-125">Color Conversion and Color Matching</span></span>

<span data-ttu-id="8df66-126">Der Prozess der Konvertierung von Farben von einem [Farb Raum](c.md) in einen anderen wird als *Farbkonvertierung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8df66-126">The process of converting colors from one [color space](c.md) to another is called *color conversion*.</span></span> <span data-ttu-id="8df66-127">Alle Farben in einem Farbraum werden relativ zum [weißen Punkt](w.md)des Farb Raums korrigiert.</span><span class="sxs-lookup"><span data-stu-id="8df66-127">All colors in a color space are fixed relative to the color space's [white point](w.md).</span></span> <span data-ttu-id="8df66-128">Da der weiße Punkt eines Farbraum von Gerät zu Gerät abweicht, muss eine konvertierte Farbe dann mit der visuellen Farbe im Ziel Farbraum übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="8df66-128">Since the white point of a color space varies from device to device, a converted color must then be matched to its visually closest color in the destination color space.</span></span> <span data-ttu-id="8df66-129">Dieser Vorgang wird als *Farbzuordnung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8df66-129">This process is called *color mapping*.</span></span>

<span data-ttu-id="8df66-130">Wenn Sie z. b. über ein digitales Image verfügen, das Sie in der Anzeige erstellt haben, befindet es sich möglicherweise in einem geräteabhängigen RGB-Farbraum.</span><span class="sxs-lookup"><span data-stu-id="8df66-130">For example, if you have a digital image that you created on your display, it may be in a device-dependent RGB color space.</span></span> <span data-ttu-id="8df66-131">Wenn Sie die Datei auf einem Drucker drucken möchten, muss Sie in den Farbraum der Drucker konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="8df66-131">If you want to print it on a printer, it must be converted to the printer's color space.</span></span> <span data-ttu-id="8df66-132">Da der Drucker wahrscheinlich einen geräteabhängigen CMYK-Farbraum verwendet, müssen alle RGB-Werte in CYMK konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="8df66-132">Since the printer probably uses a device-dependent CMYK color space, all RGB values must be converted to CYMK.</span></span> <span data-ttu-id="8df66-133">Dies ist eine [Farbkonvertierung](c.md).</span><span class="sxs-lookup"><span data-stu-id="8df66-133">This is [color conversion](c.md).</span></span> <span data-ttu-id="8df66-134">Nachdem die Werte im Hinblick auf den CYMK-Bereich angegeben wurden, müssen Sie mit der nächstgelegenen Farbe übereinstimmen, die der Drucker liefern kann.</span><span class="sxs-lookup"><span data-stu-id="8df66-134">Once the values are specified in terms of the CYMK space, they need to be matched to the closest color that the printer can produce.</span></span> <span data-ttu-id="8df66-135">Dies wird als Farbzuordnung oder [Farb](c.md)Vergleich bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8df66-135">This is called color mapping or [color matching](c.md).</span></span>

<span data-ttu-id="8df66-136">Sowohl bei der Farbkonvertierung als auch bei der Farbzuordnung müssen verschiedene gerätespezifische Faktoren berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="8df66-136">Both color conversion and color mapping must take into account a number of device-specific factors.</span></span> <span data-ttu-id="8df66-137">Beispielsweise sind die Bausteine von Bildschirmbildern Pixel.</span><span class="sxs-lookup"><span data-stu-id="8df66-137">For instance, the building blocks of screen images are pixels.</span></span> <span data-ttu-id="8df66-138">Jedes Pixel verfügt über eine festgelegte Anzahl von Bits zum Speichern des Farb-oder Farb Index Werts.</span><span class="sxs-lookup"><span data-stu-id="8df66-138">Each pixel has a set number of bits to store its color or color index value.</span></span> <span data-ttu-id="8df66-139">Die Anzahl der Bits pro Pixel ist abhängig vom Typ der verwendeten Anzeige und dem angezeigten Anzeige Adapter und vom Modus, in dem der Adapter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8df66-139">The number of bits per pixel depends on the type of display and display adapter being used, and the mode to which that the adapter is set.</span></span> <span data-ttu-id="8df66-140">Die meisten Druckertypen verwenden verschiedene [Colorants](c.md) und Drucke bei bestimmten Auflösungen.</span><span class="sxs-lookup"><span data-stu-id="8df66-140">Most every printer type uses different [colorants](c.md) and prints at particular resolutions.</span></span>

<span data-ttu-id="8df66-141">Außerdem unterscheiden sich die physischen farbiges Merkmale eines Geräts häufig auf verschiedenen Geräten.</span><span class="sxs-lookup"><span data-stu-id="8df66-141">In addition, the physical tone characteristics of a device are often different on different devices.</span></span> <span data-ttu-id="8df66-142">Wenn beispielsweise Farben von Computermonitoren erstellt werden, können Sie anders erscheinen als bei der Erstellung auf einem Druck Press.</span><span class="sxs-lookup"><span data-stu-id="8df66-142">For instance, when colors are produced by computer monitors, they can appear different than they would if they were produced on a printing press.</span></span> <span data-ttu-id="8df66-143">Ein Korrekturfaktor, der als *Gammakorrektur* bezeichnet wird, wird häufig verwendet, um derartige Unterschiede auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="8df66-143">A correction factor, called *gamma correction*, is frequently used to compensate for such differences.</span></span>

<span data-ttu-id="8df66-144">Das Ergebnis dieser geräteabhängigen Faktoren besteht darin, dass jedes Farbgerät über einen bestimmten Satz von Farben verfügt, die es ergeben kann.</span><span class="sxs-lookup"><span data-stu-id="8df66-144">The result of these device-dependent factors is that each color device has a particular set of colors that it can produce.</span></span> <span data-ttu-id="8df66-145">Dieser Farbsatz wird *als seine Spiel* Farbe bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8df66-145">This color set is known as its *gamut*.</span></span> <span data-ttu-id="8df66-146">Zum Durchführen der Farbkonvertierung und der Farbzuordnung müssen die Farben in einem Bild aus dem Farbraum und dem Bereich des Quell Geräts in den Farbraum des Zielgeräts konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="8df66-146">To perform color conversion and color mapping, the colors in an image must be converted from the color space and gamut of the source device into the color space of the destination device.</span></span> <span data-ttu-id="8df66-147">Sie werden dann mit dem Spiel des Zielgeräts abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="8df66-147">They are then matched into the gamut of the destination device.</span></span>

 

 




