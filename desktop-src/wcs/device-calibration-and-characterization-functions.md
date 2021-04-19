---
title: Geräterkalibrierung und Charakterisierungsfunktionen
description: Die folgenden Funktionen sind nützlich für das Schreiben von geräterkalibrierung und-Charakterisierungs Tools, die für die Installation und das Kalibrieren von Farbanzeige Geräten wie Monitoren und Druckern erforderlich
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Windows Color System (WCS), Funktionen
- WCS (Windows Color System), Funktionen
- Bild Farbverwaltung, Funktionen
- Farbverwaltung, Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCs, Funktionen
- Windows Color System (WCS), Gerätekalibrierung
- WCS (Windows Color System), Gerätekalibrierung
- Bild Farbverwaltung, Gerätekalibrierung
- Farbverwaltung, Gerätekalibrierung
- Farben, Gerätekalibrierung
- WCS-Referenz, Gerätekalibrierung
- Referenz für WCs, Gerätekalibrierung
- Windows Color System (WCS), Charakterisierung
- WCS (Windows Color System), Charakterisierung
- Bild Farbverwaltung,-Charakterisierung
- Farbverwaltung, Charakterisierung
- Farben, Charakterisierung
- WCS-Referenz,-Charakterisierung
- Referenz für WCs, Charakterisierung
- Gerätekalibrierung
- Energie
- Charakterisierung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367bbc6385cc21c8dbff3a88bed685616fb3f29
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106361834"
---
# <a name="device-calibration-and-characterization-functions"></a><span data-ttu-id="cf9d6-127">Geräterkalibrierung und Charakterisierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="cf9d6-127">Device Calibration and Characterization Functions</span></span>

<span data-ttu-id="cf9d6-128">Die folgenden Funktionen sind nützlich für das Schreiben von geräterkalibrierung und-Charakterisierungs Tools, die für die Installation und das Kalibrieren von Farbanzeige Geräten wie Monitoren und Druckern erforderlich</span><span class="sxs-lookup"><span data-stu-id="cf9d6-128">The following functions are useful for writing device calibration and characterization tools needed for installing and calibrating color display devices such as monitors and printers.</span></span>



| <span data-ttu-id="cf9d6-129">Funktion</span><span class="sxs-lookup"><span data-stu-id="cf9d6-129">Function</span></span> | <span data-ttu-id="cf9d6-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf9d6-130">Description</span></span> |
|-|-|
| [<span data-ttu-id="cf9d6-131">**Closecolorprofile**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-131">**CloseColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-closecolorprofile) | <span data-ttu-id="cf9d6-132">Schließt ein geöffnetes Profil handle.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-132">Closes an open profile handle.</span></span> |
| [<span data-ttu-id="cf9d6-133">**"Kreatedevicelinkprofile"**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-133">**CreateDeviceLinkProfile**</span></span>](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | <span data-ttu-id="cf9d6-134">Erstellt unter Verwendung der angegebenen Intents ein International Color Consortium (ICC)-Geräte Verknüpfungs *Profil* aus einem Satz von Farbprofilen.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-134">Creates an International Color Consortium (ICC) *device link profile* from a set of color profiles, using the specified intents.</span></span> |
| [<span data-ttu-id="cf9d6-135">**Getcolorprofileelement**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-135">**GetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | <span data-ttu-id="cf9d6-136">Kopiert Daten aus einem angegebenen markierten Profil Element eines angegebenen Farbprofils in einen Puffer.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-136">Copies data from a specified tagged profile element of a specified color profile into a buffer.</span></span> |
| [<span data-ttu-id="cf9d6-137">**Getcolorprofileelementtag**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-137">**GetColorProfileElementTag**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | <span data-ttu-id="cf9d6-138">Ruft den von *dwIndex* angegebenen Tagnamen in der Tagtabelle eines bestimmten International Color Consortium (ICC)-Farbprofils ab, wobei *dwIndex* ein einbasierter Index in dieser Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-138">Retrieves the tag name specified by *dwIndex* in the tag table of a given International Color Consortium (ICC) color profile, where *dwIndex* is a one-based index into that table.</span></span> |
| [<span data-ttu-id="cf9d6-139">**Getcolorprofilefromhandle**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-139">**GetColorProfileFromHandle**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| <span data-ttu-id="cf9d6-140">Ruft den Farbprofil Inhalt ab, wenn ein Handle für ein geöffnetes Farbprofil angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-140">Retrieves the color profile contents given a handle to an open color profile.</span></span>     |
| [<span data-ttu-id="cf9d6-141">**Getcolorprofileheader**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-141">**GetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | <span data-ttu-id="cf9d6-142">Ruft die ICC-Header Struktur entweder aus dem ICC-Farbprofil oder dem WCS-XML-Profil ab oder leitet Sie</span><span class="sxs-lookup"><span data-stu-id="cf9d6-142">Retrieves or derives ICC header structure from either ICC color profile or WCS XML profile.</span></span> <span data-ttu-id="cf9d6-143">Treiber und Anwendungen sollten davon ausgehen, dass die Rückgabe von **true** nur bedeutet, dass ein ordnungsgemäß strukturierter Header zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="cf9d6-143">Drivers and applications should assume returning **TRUE** only indicates that a properly structured header is returned.</span></span> <span data-ttu-id="cf9d6-144">Jedes Tag muss mithilfe von Legacy-ICM2-APIs oder XML-Schema-APIs unabhängig überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-144">Each tag will still need to be validated independently using either legacy ICM2 APIs or XML schema APIs.</span></span> |
| [<span data-ttu-id="cf9d6-145">**Getcountrytcolorprofileelements**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-145">**GetCountColorProfileElements**</span></span>](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | <span data-ttu-id="cf9d6-146">Ruft die Anzahl der markierten Elemente in einem angegebenen Farbprofil ab.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-146">Retrieves the number of tagged elements in a given color profile.</span></span> |
| [<span data-ttu-id="cf9d6-147">**GetPS2ColorRenderingDictionary**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-147">**GetPS2ColorRenderingDictionary**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | <span data-ttu-id="cf9d6-148">Ruft das textrenderingwörterbuch der PostScript-Ebene 2 aus dem angegebenen "ICC"-Farbprofil</span><span class="sxs-lookup"><span data-stu-id="cf9d6-148">Retrieves the PostScript Level 2 color rendering dictionary from the specified ICC color profile.</span></span> |
| [<span data-ttu-id="cf9d6-149">**GetPS2ColorRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-149">**GetPS2ColorRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | <span data-ttu-id="cf9d6-150">Ruft die [textrenderingabsicht](r.md) der PostScript-Ebene 2 aus einem ICC-Farbprofil ab.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-150">Retrieves the PostScript Level 2 color [rendering intent](r.md) from an ICC color profile.</span></span> |
| [<span data-ttu-id="cf9d6-151">**GetPS2ColorSpaceArray**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-151">**GetPS2ColorSpaceArray**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | <span data-ttu-id="cf9d6-152">Ruft das Bytearray der [](c.md) PostScript-Ebene 2 aus einem ICC-Farbprofil ab.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-152">Retrieves the PostScript Level 2 [color space](c.md) array from an ICC color profile.</span></span> |
| [<span data-ttu-id="cf9d6-153">**Iscolorprofiletagpresent**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-153">**IsColorProfileTagPresent**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | <span data-ttu-id="cf9d6-154">Meldet, ob ein angegebenes International Color Consortium-Tag (ICC) im angegebenen Farbprofil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-154">Reports whether a specified International Color Consortium (ICC) tag is present in the specified color profile.</span></span> |
| [<span data-ttu-id="cf9d6-155">**Iscolorprofilevalid**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-155">**IsColorProfileValid**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | <span data-ttu-id="cf9d6-156">Hiermit können Sie bestimmen, ob es sich bei dem angegebenen Profil um ein gültiges International Color Consortium (ICC)-Profil oder ein gültiges Windows Color System (WCS)-Profil Handle handelt, das für die Farbverwaltung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-156">Allows you to determine whether the specified profile is a valid International Color Consortium (ICC) profile, or a valid Windows Color System (WCS) profile handle that can be used for color management.</span></span> |
| [<span data-ttu-id="cf9d6-157">**Opencolorprofilew**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-157">**OpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-opencolorprofilew) | <span data-ttu-id="cf9d6-158">Erstellt ein Handle für ein angegebenes Farbprofil.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-158">Creates a handle to a specified color profile.</span></span> <span data-ttu-id="cf9d6-159">Das Handle kann dann in anderen Profil Verwaltungsfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-159">The handle can then be used in other profile management functions.</span></span> |
| [<span data-ttu-id="cf9d6-160">**Setcolorprofileelement**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-160">**SetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | <span data-ttu-id="cf9d6-161">Legt die Elementdaten für ein getaggtes Profil Element in einem Datenprofil für den IStGH fest.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-161">Sets the element data for a tagged profile element in an ICC color profile.</span></span> |
| [<span data-ttu-id="cf9d6-162">**Setcolorprofileelementreference**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-162">**SetColorProfileElementReference**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | <span data-ttu-id="cf9d6-163">Erstellt in einem angegebenen ICC-Farbprofil ein neues Tag, das auf dieselben Daten wie ein vorhandenes Tag verweist.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-163">Creates in a specified ICC color profile a new tag that references the same data as an existing tag.</span></span> |
| [<span data-ttu-id="cf9d6-164">**Setcolorprofileelementsize**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-164">**SetColorProfileElementSize**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | <span data-ttu-id="cf9d6-165">Legt die Größe eines markierten Elements in einem poolfarbprofil fest.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-165">Sets the size of a tagged element in an ICC color profile.</span></span> |
| [<span data-ttu-id="cf9d6-166">**Setcolorprofileheader**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-166">**SetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | <span data-ttu-id="cf9d6-167">Legt die Header Daten in einem angegebenen ICC-Farbprofil fest.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-167">Sets the header data in a specified ICC color profile.</span></span> |
| [<span data-ttu-id="cf9d6-168">**Wcsgetcalibrationmanagementstate**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-168">**WcsGetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | <span data-ttu-id="cf9d6-169">Bestimmt, ob die Systemverwaltung des Anzeige-Kalibrierungs Zustands aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-169">Determines whether system management of the display calibration state is enabled.</span></span> |
| [<span data-ttu-id="cf9d6-170">**Wcssetcalibrationmanagementstate**</span><span class="sxs-lookup"><span data-stu-id="cf9d6-170">**WcsSetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | <span data-ttu-id="cf9d6-171">Bestimmt, ob die Systemverwaltung des Anzeige-Kalibrierungs Zustands aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cf9d6-171">Determines whether system management of the display calibration state is enabled.</span></span> |



 

 

 




