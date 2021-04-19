---
title: Grundlegende Funktionen zur Verwendung innerhalb eines Gerätekontexts
description: Die folgenden WCS-Funktionen bieten grundlegende Funktionen zur Farbzuordnung innerhalb von Geräte Kontexten. Sie sind für alle Anwendungen nützlich, die die Farbverwaltung mit geringem mehr Aufwand und minimalem Benutzereingriff implementieren müssen.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Windows Color System (WCS), Funktionen
- WCS (Windows Color System), Funktionen
- Bild Farbverwaltung, Funktionen
- Farbverwaltung, Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCs, Funktionen
- Windows Color System (WCS), Geräte Kontexte
- WCS (Windows Color System), Geräte Kontexte
- Bild Farbverwaltung, Geräte Kontexte
- Farbverwaltung, Geräte Kontexte
- Farben, Geräte Kontexte
- WCS-Referenz, Geräte Kontexte
- Referenz für WCs, Geräte Kontexte
- Gerätekontexte
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde99ed077af108ddc20c73f86e17bedfe1d4a8c
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "106357135"
---
# <a name="basic-functions-for-use-within-a-device-context"></a><span data-ttu-id="1da83-119">Grundlegende Funktionen zur Verwendung innerhalb eines Gerätekontexts</span><span class="sxs-lookup"><span data-stu-id="1da83-119">Basic Functions for Use Within a Device Context</span></span>

<span data-ttu-id="1da83-120">Die folgenden WCS-Funktionen bieten grundlegende Funktionen zur [Farbzuordnung](c.md) innerhalb von Geräte Kontexten.</span><span class="sxs-lookup"><span data-stu-id="1da83-120">The following WCS functions deliver basic [color mapping](c.md) capabilities within device contexts.</span></span> <span data-ttu-id="1da83-121">Sie sind für alle Anwendungen nützlich, die die Farbverwaltung mit geringem mehr Aufwand und minimalem Benutzereingriff implementieren müssen.</span><span class="sxs-lookup"><span data-stu-id="1da83-121">They are useful to all applications that need to implement color management with low overhead and minimal user intervention.</span></span>



| <span data-ttu-id="1da83-122">Funktion</span><span class="sxs-lookup"><span data-stu-id="1da83-122">Function</span></span>                                                           | <span data-ttu-id="1da83-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1da83-123">Description</span></span>                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1da83-124">**Checkcolorsingamut**</span><span class="sxs-lookup"><span data-stu-id="1da83-124">**CheckColorsInGamut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | <span data-ttu-id="1da83-125">Überprüft, ob die angegebenen Farben sich im Gamut eines Geräts befinden.</span><span class="sxs-lookup"><span data-stu-id="1da83-125">Checks if given colors are in a device's gamut.</span></span>                                                                                                     |
| [<span data-ttu-id="1da83-126">**Colorcorrectpalette**</span><span class="sxs-lookup"><span data-stu-id="1da83-126">**ColorCorrectPalette**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | <span data-ttu-id="1da83-127">Korrigiert die Einträge in einer Palette für einen Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="1da83-127">Corrects the entries in a palette for a device context.</span></span>                                                                                             |
| [<span data-ttu-id="1da83-128">**Colormatchdetarget**</span><span class="sxs-lookup"><span data-stu-id="1da83-128">**ColorMatchToTarget**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | <span data-ttu-id="1da83-129">Führt eine Farbzuordnung für Vorschau Zwecke aus.</span><span class="sxs-lookup"><span data-stu-id="1da83-129">Performs color mapping for preview purposes.</span></span>                                                                                                        |
| [<span data-ttu-id="1da83-130">**"Kreatecolorspace"**</span><span class="sxs-lookup"><span data-stu-id="1da83-130">**CreateColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | <span data-ttu-id="1da83-131">Erstellt einen Farbraum.</span><span class="sxs-lookup"><span data-stu-id="1da83-131">Creates a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="1da83-132">**Deletecolorspace**</span><span class="sxs-lookup"><span data-stu-id="1da83-132">**DeleteColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | <span data-ttu-id="1da83-133">Löscht einen Farbraum.</span><span class="sxs-lookup"><span data-stu-id="1da83-133">Deletes a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="1da83-134">**"Umumicmprofiles"**</span><span class="sxs-lookup"><span data-stu-id="1da83-134">**EnumICMProfiles**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | <span data-ttu-id="1da83-135">Listet Ausgabe Farbprofile auf, die für einen bestimmten Gerätekontext verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1da83-135">Enumerates output color profiles available for a given device context.</span></span>                                                                              |
| [<span data-ttu-id="1da83-136">**"Umumicmprofilesproccallback"**</span><span class="sxs-lookup"><span data-stu-id="1da83-136">**EnumICMProfilesProcCallback**</span></span>](/windows/desktop/api/Wingdi/) | <span data-ttu-id="1da83-137">Anwendungs definierte Rückruffunktion für [**enumicmprofiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).</span><span class="sxs-lookup"><span data-stu-id="1da83-137">Application-defined callback function for [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).</span></span> <span data-ttu-id="1da83-138">Der Name dieser Funktion wird auch von der Anwendung definiert.</span><span class="sxs-lookup"><span data-stu-id="1da83-138">The name of this function is also defined by the application.</span></span> |
| [<span data-ttu-id="1da83-139">**GetColorSpace**</span><span class="sxs-lookup"><span data-stu-id="1da83-139">**GetColorSpace**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | <span data-ttu-id="1da83-140">Ruft den aktuellen Eingabe Farbraum in einem Gerätekontext ab.</span><span class="sxs-lookup"><span data-stu-id="1da83-140">Gets the current input color space in a device context.</span></span> |
| [<span data-ttu-id="1da83-141">**Geticmprofile**</span><span class="sxs-lookup"><span data-stu-id="1da83-141">**GetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | <span data-ttu-id="1da83-142">Ruft das aktuelle Ausgabe Farbprofil eines Geräte Kontexts ab.</span><span class="sxs-lookup"><span data-stu-id="1da83-142">Gets the current output color profile of a device context.</span></span>                                                                                          |
| [<span data-ttu-id="1da83-143">**Getlogcolorspace**</span><span class="sxs-lookup"><span data-stu-id="1da83-143">**GetLogColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | <span data-ttu-id="1da83-144">Ruft die [**logcolorspace**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) -Struktur eines Geräte Kontexts ab.</span><span class="sxs-lookup"><span data-stu-id="1da83-144">Gets the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure of a device context.</span></span>                                                                      |
| [<span data-ttu-id="1da83-145">**Setcolorspace**</span><span class="sxs-lookup"><span data-stu-id="1da83-145">**SetColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | <span data-ttu-id="1da83-146">Legt den Eingabe Farbraum eines Geräte Kontexts fest.</span><span class="sxs-lookup"><span data-stu-id="1da83-146">Sets a device context's input color space.</span></span>                                                                                                          |
| [<span data-ttu-id="1da83-147">**-Modus**</span><span class="sxs-lookup"><span data-stu-id="1da83-147">**SetICMMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | <span data-ttu-id="1da83-148">Schaltet die Farbverwaltung in einem Gerätekontext ein bzw. aus.</span><span class="sxs-lookup"><span data-stu-id="1da83-148">Turns color management on or off in a device context.</span></span>                                                                                               |
| [<span data-ttu-id="1da83-149">**"Abbild profile"**</span><span class="sxs-lookup"><span data-stu-id="1da83-149">**SetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | <span data-ttu-id="1da83-150">Legt das Ausgabe Farbprofil für einen angegebenen Gerätekontext fest.</span><span class="sxs-lookup"><span data-stu-id="1da83-150">Sets the output color profile for a given device context.</span></span>                                                                                           |
| [<span data-ttu-id="1da83-151">**Wcsenaufcolorprofiles**</span><span class="sxs-lookup"><span data-stu-id="1da83-151">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | <span data-ttu-id="1da83-152">Listet alle Farbprofile auf, die die enumerationskriterien im angegebenen Profil Verwaltungsbereich erfüllen.</span><span class="sxs-lookup"><span data-stu-id="1da83-152">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                      |



 

 

 




