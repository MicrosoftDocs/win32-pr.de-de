---
title: Profilverwaltungsfunktionen
description: Profilverwaltungsfunktionen
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Windows Color System (WCS), Funktionen
- WCS (Windows Color System), Funktionen
- Bild Farbverwaltung, Funktionen
- Farbverwaltung, Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCs, Funktionen
- Windows Color System (WCS), profile
- WCS (Windows Color System), profile
- Bildfarben Verwaltung, profile
- Farbverwaltung, profile
- Farben, profile
- WCS-Referenz, profile
- Referenz für WCs, profile
- Profilverwaltung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0e80e300532b20148eef6d9dc362438b6714a3
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106371802"
---
# <a name="profile-management-functions"></a><span data-ttu-id="0239a-118">Profilverwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="0239a-118">Profile Management Functions</span></span>

## <a name="profile-management-functions"></a><span data-ttu-id="0239a-119">Profilverwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="0239a-119">Profile Management Functions</span></span>

<span data-ttu-id="0239a-120">Die folgenden API-Funktionen sind für die Profilverwaltung nützlich.</span><span class="sxs-lookup"><span data-stu-id="0239a-120">The following API functions are useful in profile management.</span></span>



| <span data-ttu-id="0239a-121">Funktion</span><span class="sxs-lookup"><span data-stu-id="0239a-121">Function</span></span>                                                                               | <span data-ttu-id="0239a-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0239a-122">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0239a-123">**Associatecolorprofilewithdevicew**</span><span class="sxs-lookup"><span data-stu-id="0239a-123">**AssociateColorProfileWithDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | <span data-ttu-id="0239a-124">Ordnet ein angegebenes Farbprofil einem angegebenen Gerät zu.</span><span class="sxs-lookup"><span data-stu-id="0239a-124">Associates a specified color profile with a specified device.</span></span>                                                              |
| <span data-ttu-id="0239a-125">[**Erkreateprofilefromlogcolorspacew**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)</span><span class="sxs-lookup"><span data-stu-id="0239a-125">[**CreateProfileFromLogColorSpaceW**]((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)</span></span> | <span data-ttu-id="0239a-126">Konvertiert einen logischen [Farbraum](c.md) in ein [Geräte Profil](d.md).</span><span class="sxs-lookup"><span data-stu-id="0239a-126">Converts a logical [color space](c.md) to a [device profile](d.md).</span></span> |
| [<span data-ttu-id="0239a-127">**Disassociatecolorprofilefromdevicew**</span><span class="sxs-lookup"><span data-stu-id="0239a-127">**DisassociateColorProfileFromDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | <span data-ttu-id="0239a-128">Trennt ein angegebenes Farbprofil einem angegebenen Gerät auf einem angegebenen Computer.</span><span class="sxs-lookup"><span data-stu-id="0239a-128">Disassociates a specified color profile with a specified device on a specified computer.</span></span> |
| [<span data-ttu-id="0239a-129">**Enumcolorprofilesw**</span><span class="sxs-lookup"><span data-stu-id="0239a-129">**EnumColorProfilesW**</span></span>](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | <span data-ttu-id="0239a-130">Listet alle Profile auf, die die angegebenen enumerationskriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="0239a-130">Enumerates all the profiles satisfying the given enumeration criteria.</span></span> |
| [<span data-ttu-id="0239a-131">**Getcolordirector**</span><span class="sxs-lookup"><span data-stu-id="0239a-131">**GetColorDirectoryW**</span></span>](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | <span data-ttu-id="0239a-132">Ruft den Pfad des Windows-Farb Verzeichnisses auf einem angegebenen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="0239a-132">Retrieves the path of the Windows COLOR directory on a specified machine.</span></span> |
| [<span data-ttu-id="0239a-133">**Getde vicegammaramp**</span><span class="sxs-lookup"><span data-stu-id="0239a-133">**GetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | <span data-ttu-id="0239a-134">Ruft die Gamma-Rampe von der direkten Farbanzeige Boards ab.</span><span class="sxs-lookup"><span data-stu-id="0239a-134">Gets the gamma ramp from direct color display boards.</span></span>                                                                                                |
| [<span data-ttu-id="0239a-135">**Getstandardcolorspaceprofilew**</span><span class="sxs-lookup"><span data-stu-id="0239a-135">**GetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | <span data-ttu-id="0239a-136">Ruft das Farbprofil ab, das für den angegebenen Standard [Farbraum](c.md)registriert ist.</span><span class="sxs-lookup"><span data-stu-id="0239a-136">Retrieves the color profile registered for the specified standard [color space](c.md).</span></span> |
| [<span data-ttu-id="0239a-137">**Installcolorprofilew**</span><span class="sxs-lookup"><span data-stu-id="0239a-137">**InstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-installcolorprofilew) | <span data-ttu-id="0239a-138">Installiert ein bestimmtes Profil für die Verwendung auf einem angegebenen Computer.</span><span class="sxs-lookup"><span data-stu-id="0239a-138">Installs a given profile for use on a specified machine.</span></span> <span data-ttu-id="0239a-139">Das Profil wird auch in das Farb Verzeichnis kopiert.</span><span class="sxs-lookup"><span data-stu-id="0239a-139">The profile is also copied to the COLOR directory.</span></span> |
| [<span data-ttu-id="0239a-140">**Registercmmw**</span><span class="sxs-lookup"><span data-stu-id="0239a-140">**RegisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-registercmmw) | <span data-ttu-id="0239a-141">Ordnet einen angegebenen Identifikations Wert der angegebenen CMM-dll (Dynamic Link Library) des Farb Verwaltungs Moduls zu.</span><span class="sxs-lookup"><span data-stu-id="0239a-141">Associates a specified identification value with the specified color management module dynamic link library (CMM DLL).</span></span> <span data-ttu-id="0239a-142">Wenn diese ID in einem Farbprofil angezeigt wird, kann Windows den entsprechenden CMM-Code suchen, um eine Transformation zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0239a-142">When this ID appears in a color profile, Windows can then locate the corresponding CMM so as to create a transform.</span></span> |
| [<span data-ttu-id="0239a-143">**Setde vicegammaramp**</span><span class="sxs-lookup"><span data-stu-id="0239a-143">**SetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | <span data-ttu-id="0239a-144">Legt die Gamma-Rampe für die Anzeige Boards der direkten Farbe fest.</span><span class="sxs-lookup"><span data-stu-id="0239a-144">Sets the gamma ramp on direct color display boards.</span></span>                                                                                                  |
| [<span data-ttu-id="0239a-145">**Setstandardcolorspaceprofilew**</span><span class="sxs-lookup"><span data-stu-id="0239a-145">**SetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | <span data-ttu-id="0239a-146">Registriert ein angegebenes Profil für einen angegebenen Standard [Farbraum](c.md).</span><span class="sxs-lookup"><span data-stu-id="0239a-146">Registers a specified profile for a given standard [color space](c.md).</span></span> <span data-ttu-id="0239a-147">Das Profil kann mithilfe von [getstandardcolorspaceprofilew](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew)abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-147">The profile can be queried using [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew).</span></span> |
| [<span data-ttu-id="0239a-148">**Uninstallcolorprofilew**</span><span class="sxs-lookup"><span data-stu-id="0239a-148">**UninstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | <span data-ttu-id="0239a-149">Entfernt ein angegebenes Farbprofil von einem angegebenen Computer.</span><span class="sxs-lookup"><span data-stu-id="0239a-149">Removes a specified color profile from a specified computer.</span></span> <span data-ttu-id="0239a-150">Zugehörige Dateien werden optional aus dem System gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0239a-150">Associated files are optionally deleted from the system.</span></span> |
| [<span data-ttu-id="0239a-151">**Unregistercmmw**</span><span class="sxs-lookup"><span data-stu-id="0239a-151">**UnregisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-unregistercmmw) | <span data-ttu-id="0239a-152">Trennt einen angegebenen ID-Wert aus einer angegebenen Dynamic Link Library (CMM-dll) des Farb Verwaltungs Moduls.</span><span class="sxs-lookup"><span data-stu-id="0239a-152">Dissociates a specified ID value from a given color management module dynamic-link library (CMM DLL).</span></span> |
| [<span data-ttu-id="0239a-153">**Wcsassociatecolorprofilewithdevice**</span><span class="sxs-lookup"><span data-stu-id="0239a-153">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | <span data-ttu-id="0239a-154">Ordnet ein angegebenes WCS-Farbprofil einem angegebenen Gerät zu.</span><span class="sxs-lookup"><span data-stu-id="0239a-154">Associates a specified WCS color profile with a specified device.</span></span>                                                                                    |
| [<span data-ttu-id="0239a-155">**Wcscreateiccprofile**</span><span class="sxs-lookup"><span data-stu-id="0239a-155">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | <span data-ttu-id="0239a-156">Konvertiert ein WCS-Profil in ein-ICC-Profil.</span><span class="sxs-lookup"><span data-stu-id="0239a-156">Converts a WCS profile into an ICC profile.</span></span>                                                                                                          |
| [<span data-ttu-id="0239a-157">**Wcsdisassociatecolorprofilefromdevice**</span><span class="sxs-lookup"><span data-stu-id="0239a-157">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | <span data-ttu-id="0239a-158">Trennt ein angegebenes WCS-Farbprofil einem angegebenen Gerät auf einem angegebenen Computer.</span><span class="sxs-lookup"><span data-stu-id="0239a-158">Disassociates a specified WCS color profile with a specified device on a specified computer.</span></span>                                                         |
| [<span data-ttu-id="0239a-159">**Wcsenaufcolorprofiles**</span><span class="sxs-lookup"><span data-stu-id="0239a-159">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | <span data-ttu-id="0239a-160">Listet alle Farbprofile auf, die die enumerationskriterien im angegebenen Profil Verwaltungsbereich erfüllen.</span><span class="sxs-lookup"><span data-stu-id="0239a-160">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                       |
| [<span data-ttu-id="0239a-161">**Wcsenaufcolorprofilessize**</span><span class="sxs-lookup"><span data-stu-id="0239a-161">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | <span data-ttu-id="0239a-162">Gibt die Größe (in Bytes) des Puffers zurück, der von der Funktion [**wcsenumcolorprofiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) zum Auflisten von Farbprofilen benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="0239a-162">Returns the size, in bytes, of the buffer required by the [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) function to enumerate color profiles.</span></span> |
| [<span data-ttu-id="0239a-163">**Wcsgetdefaultcolorprofile**</span><span class="sxs-lookup"><span data-stu-id="0239a-163">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | <span data-ttu-id="0239a-164">Ruft das Standard Farbprofil für ein Gerät oder den geräteunabhängigen Standardwert ab, wenn das Gerät nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0239a-164">Retrieves the default color profile for a device, or the device-independent default if the device is not specified.</span></span>                                  |
| [<span data-ttu-id="0239a-165">**Wcsgetdefaultcolorprofilesize**</span><span class="sxs-lookup"><span data-stu-id="0239a-165">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | <span data-ttu-id="0239a-166">Gibt die Größe (in Bytes) des standardmäßigen Farbprofil namens für ein Gerät zurück, einschließlich des **null** -Terminator.</span><span class="sxs-lookup"><span data-stu-id="0239a-166">Returns the size, in bytes, of the default color profile name for a device, including the **NULL** terminator.</span></span>                                       |
| [<span data-ttu-id="0239a-167">**Wcsgetdefaultrenderingintent**</span><span class="sxs-lookup"><span data-stu-id="0239a-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="0239a-168">Ruft die standardmäßige renderabsicht im angegebenen Profil Verwaltungsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="0239a-168">Retrieves the default rendering intent in the specified profile management scope.</span></span>                                                                    |
| [<span data-ttu-id="0239a-169">**Wcsgetuseperuserprofiles**</span><span class="sxs-lookup"><span data-stu-id="0239a-169">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="0239a-170">Bestimmt, ob der Benutzer eine benutzerspezifische Profil Zuordnungs Liste für das angegebene Gerät verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="0239a-170">Determines whether the user has chosen to use a per-user profile association list for the specified device.</span></span>                                          |
| [<span data-ttu-id="0239a-171">**Wcsopeincolorprofilew**</span><span class="sxs-lookup"><span data-stu-id="0239a-171">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | <span data-ttu-id="0239a-172">Erstellt ein Handle für ein angegebenes Farbprofil.</span><span class="sxs-lookup"><span data-stu-id="0239a-172">Creates a handle to a specified color profile.</span></span>                                                                                                       |
| [<span data-ttu-id="0239a-173">**Wcssetdefaultcolorprofile**</span><span class="sxs-lookup"><span data-stu-id="0239a-173">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | <span data-ttu-id="0239a-174">Legt den Standardnamen des Farbprofils für den angegebenen Profiltyp im angegebenen Profil Verwaltungsbereich fest.</span><span class="sxs-lookup"><span data-stu-id="0239a-174">Sets the default color profile name of the specified profile type in the specified profile management scope.</span></span>                                         |
| [<span data-ttu-id="0239a-175">**Wcssetdefaultrenderingintent**</span><span class="sxs-lookup"><span data-stu-id="0239a-175">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | <span data-ttu-id="0239a-176">Legt die Standard-renderabsicht im angegebenen Profil Verwaltungsbereich fest.</span><span class="sxs-lookup"><span data-stu-id="0239a-176">Sets the default rendering intent in the specified profile management scope.</span></span>                                                                         |
| [<span data-ttu-id="0239a-177">**Wcssetuseperuserprofiles**</span><span class="sxs-lookup"><span data-stu-id="0239a-177">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | <span data-ttu-id="0239a-178">Ermöglicht es dem Benutzer anzugeben, ob eine Profil Zuordnungs Liste pro Benutzer für das angegebene Gerät verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0239a-178">Allows the user to specify whether to use a per-user profile association list for the specified device.</span></span>                                              |



 

## <a name="profile-consumption-functions"></a><span data-ttu-id="0239a-179">Profil Nutzungs Funktionen</span><span class="sxs-lookup"><span data-stu-id="0239a-179">Profile Consumption Functions</span></span>

<span data-ttu-id="0239a-180">Bei den APIs für die Profil Nutzung handelt es sich um APIs in ICM2, die die XML-Profile, Profil Handles oder renderingintents von ICC oder WCS als Parameter und eine Reihe neuer APIs für die WCS-Profil Unterstützung für den Anwendungs Farb Verwaltungs Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="0239a-180">The profile consumption APIs are those APIs in ICM2 that take ICC or WCS XML profiles, profile handles, or rendering intents as parameters, and a set of new APIs for WCS profile support for application color management code.</span></span>

 

## <a name="profiles-and-profile-management-functions"></a><span data-ttu-id="0239a-181">Profile und Profil Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="0239a-181">Profiles and Profile Management Functions</span></span>

<span data-ttu-id="0239a-182">Der Profil Verwaltungs Workflow basiert auf vorhandenen ICM2-APIs, die erweitert werden, um zusätzliche Funktionen zum Überarbeiten von Anwendungscode bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0239a-182">The profile management workflow is based on existing ICM2 APIs that are augmented to provide additional functionality for revising application code.</span></span>

<span data-ttu-id="0239a-183">Profile enthalten Informationen, die von Farb Verarbeitungsalgorithmen verwendet werden, um die Farbe zwischen verschiedenen Farbräumen zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="0239a-183">Profiles contain information used by color processing algorithms to translate color between different color spaces.</span></span> <span data-ttu-id="0239a-184">Mit der Profilverwaltung können Sie Abfragen und angeben, welche Profile in verschiedenen Phasen vom Farb Verarbeitungsmodell verwendet werden, um die Farbausgabe verschiedener Peripheriegeräte mit unterschiedlichen Farb Merkmalen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="0239a-184">Profile management provides a way to query and specify which profiles get used at different stages by the color processing model to manage color output of various peripheral devices with diverse color characteristics.</span></span>

<span data-ttu-id="0239a-185">Die Profilverwaltung bietet die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="0239a-185">Profile management provides the following set of functionalities:</span></span>

 

1. <span data-ttu-id="0239a-186">Installieren von Farbprofilen für die Verwendung im System.</span><span class="sxs-lookup"><span data-stu-id="0239a-186">Installing color profiles for use in the system.</span></span>

 

2. <span data-ttu-id="0239a-187">Zuordnen eines oder mehrerer installierter Farbprofile zu einem bestimmten Gerät.</span><span class="sxs-lookup"><span data-stu-id="0239a-187">Associating one or more installed color profiles with any particular device.</span></span>

 

3. <span data-ttu-id="0239a-188">Auswählen eines Standard Farbprofils eines bestimmten Typs in den Profilen, die in einer bestimmten Phase der Farbverarbeitung zur Verwendung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="0239a-188">Choosing a default color profile of a particular type among the profiles available for use in a particular stage of color processing.</span></span> <span data-ttu-id="0239a-189">Dies kann für ein Gerät in den zugeordneten Profilen oder zwischen den Profilen, die im System installiert sind, und nicht für gerätespezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="0239a-189">This could be for a device among the profiles associated with it, or among the profiles installed in the system and not device specific.</span></span>

 

4. <span data-ttu-id="0239a-190">Auflisten von Farbprofilen, die bestimmte Kriterien zwischen den im System installierten Profilen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="0239a-190">Enumerating color profiles that satisfy particular criteria among the profiles installed in the system.</span></span>

<span data-ttu-id="0239a-191">Die Dateinamen Erweiterungen für WCS-Profile sind ". CDMP" für DMPs, ". Camp" für CAMPs und ". GMMP" für gmmps.</span><span class="sxs-lookup"><span data-stu-id="0239a-191">The WCS profile filename extensions are ".cdmp" for DMPs, ".camp" for CAMPs, and ".gmmp" for GMMPs.</span></span>

 

<span data-ttu-id="0239a-192">**Profilverwaltung pro Benutzer und Aktivierung der Ausführung im Lua-Kontext**</span><span class="sxs-lookup"><span data-stu-id="0239a-192">**Per-user profile management and enabling execution in LUA context**</span></span>

<span data-ttu-id="0239a-193">Das Ziel des im aktuellen Dokument beschriebenen Entwurfs ist Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0239a-193">The goal of the design described in the current document is as follows:</span></span>

 

1. <span data-ttu-id="0239a-194">Die Legacy-ICM2-Implementierung bietet keine Unterstützung für die Profilverwaltung pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0239a-194">Legacy ICM2 implementation does not provide support for per-user profile management.</span></span> <span data-ttu-id="0239a-195">Verschiedene Benutzer können nicht über eigene Profileinstellungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="0239a-195">Different users cannot have their own profile settings.</span></span> <span data-ttu-id="0239a-196">In Vista ermöglicht die WCS-Profil Verwaltungsinfrastruktur Benutzern, individuelle Profileinstellungen für die meisten Funktionen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0239a-196">In Vista, the WCS profile management infrastructure enables users to configure individual profile settings for most functionalities.</span></span>

 

2. <span data-ttu-id="0239a-197">Alle veralteten ICM2-Profilverwaltungs-APIs ändern systemweite Einstellungen und erfordern Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="0239a-197">All legacy ICM2 profile management APIs modify settings system-wide and require administrative privileges.</span></span> <span data-ttu-id="0239a-198">In Windows Vista führen alle Benutzer in den meisten Fällen die Einstellungen mit den geringsten Berechtigungen für Benutzerkonten (LUA) aus, und Administratoren können die Berechtigung selektiv erhöhen, um Anwendungen auszuführen, die systemweite Einstellungen ändern.</span><span class="sxs-lookup"><span data-stu-id="0239a-198">In Windows Vista, all users run in Least-privileged User Account (LUA) settings most of the time, and administrators can elevate privilege selectively to run applications that modify system-wide settings.</span></span> <span data-ttu-id="0239a-199">In der WCS-Profilverwaltung können alle Profileinstellungen pro Benutzer im Lua-Kontext konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-199">In WCS profile management, all per-user profile settings are configurable in LUA context.</span></span> <span data-ttu-id="0239a-200">Profil Verwaltungs Anwendungen können als Lua-Einstellungen ausgeführt werden, wodurch der Verwendungs Umfang erhöht und sichergestellt wird, dass die Sicherheit des Systems nicht beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="0239a-200">Profile management applications can run as LUA settings, increasing their scope of use and ensuring that security of the system is not compromised.</span></span>

<span data-ttu-id="0239a-201">Die Profilverwaltung in Vista bietet die folgenden Verbesserungen gegenüber der Legacy-ICM2-Infrastruktur:</span><span class="sxs-lookup"><span data-stu-id="0239a-201">Profile management in Vista provides the following enhancements over legacy ICM2 infrastructure:</span></span>

 

1. <span data-ttu-id="0239a-202">Sie ermöglicht die Zuordnung von Profilen zu Geräten, Standardprofil Einstellungen und die Enumeration von Profilen sowohl im Benutzer-als auch im systemweiten Bereich.</span><span class="sxs-lookup"><span data-stu-id="0239a-202">It enables profile association with devices, default profile settings, and enumeration of profiles in both per-user and system-wide scope.</span></span>

 

2. <span data-ttu-id="0239a-203">Die Installation eines Profils bleibt systemweit und erfordert Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="0239a-203">Installing a profile remains system wide and requires administrator privileges.</span></span> <span data-ttu-id="0239a-204">Dies ist mit der Profil Installation während der Geräteinstallation konsistent, da die Geräteinstallation systemweit ist und Administratorrechte erfordert.</span><span class="sxs-lookup"><span data-stu-id="0239a-204">This is consistent with profile installation during device installation because device installation is system wide and requires administrative privileges.</span></span>

 

<span data-ttu-id="0239a-205">Ob Geräte aus dem Lua-Kontext installiert werden können, ist besonders für die unterstützte Geräteklasse von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="0239a-205">Whether devices can be installed from LUA context is particular to what is supported for that class of device.</span></span> <span data-ttu-id="0239a-206">In Vista ist es beispielsweise möglich, die Drucker Installation aus dem Lua-Kontext durchzuführen, wenn dem Benutzer die Berechtigung erteilt wurde, Dateien von einem Domänen Administrator mithilfe von Treiber Speicher Richtlinien in den Treiber Speicher zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="0239a-206">For example, in Vista, it is possible to do printer installation from LUA context if the user has been granted rights to copy files into the driver store by a domain administrator using driver store policies.</span></span> <span data-ttu-id="0239a-207">Die Infrastruktur für die Farbprofilverwaltung muss in diesem Zusammenhang nichts Besonderes tun, da die Installation im spoolerkontext erfolgt.</span><span class="sxs-lookup"><span data-stu-id="0239a-207">Color profile management infrastructure doesn't need to do anything special in this regard since the installation happens in spooler context.</span></span>

 

3. <span data-ttu-id="0239a-208">Das Ändern von Profileinstellungen im Benutzer bezogenen Bereich kann im Lua-Kontext erfolgen. systemweite Änderungen erforderten Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="0239a-208">Modifying profile settings in per-user scope can be done in LUA context; system-wide modifications required administrative privileges.</span></span> <span data-ttu-id="0239a-209">Profil Verwaltungsvorgänge, die das Lesen von Konfigurationsinformationen erfordern, können im Lua-Kontext sowohl für benutzerspezifische als auch für systemweite Einstellungen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-209">Profile management operations that require reading configuration information can be done in LUA context for both per-user and system-wide settings.</span></span>

<span data-ttu-id="0239a-210">Profil Verwaltungsbereich gibt den Umfang der durchgeführten Vorgänge an. entweder pro Benutzer oder systemweit.</span><span class="sxs-lookup"><span data-stu-id="0239a-210">Profile management scope indicates the scope of the operations performed; either per-user or system wide.</span></span>

<span data-ttu-id="0239a-211">Für jeden Vorgang wird angegeben, ob Sie über den Lua-Kontext ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0239a-211">For each operation, it is indicated whether it can be done from LUA context.</span></span> <span data-ttu-id="0239a-212">Wenn ein Vorgang im Lua-Kontext nicht ausgeführt werden kann, gibt die entsprechende Profilverwaltungs-API einen Fehler mit dem Zugriff verweigert zurück.</span><span class="sxs-lookup"><span data-stu-id="0239a-212">If an operation cannot be performed in LUA context, the corresponding profile management API returns failure with access denied.</span></span> <span data-ttu-id="0239a-213">Anwendungen, die die API verwenden, z. b. die System Steuerungs Option "Farbverwaltung", können es Benutzern ermöglichen, die Rechte auf den administrativen Kontext zu erhöhen (mithilfe von OTS oder der Zustimmungs Benutzeroberfläche), und dann die API aus dem erweiterten Kontext aufzurufen, damit der Vorgang erfolgreich</span><span class="sxs-lookup"><span data-stu-id="0239a-213">Applications using the API, such as Color Management Control Panel, can enable the user to elevate to administrative context (using OTS or Consent UI), and then call the API from the elevated context so that the operation will succeed.</span></span>



<span data-ttu-id="0239a-214">Vorgang</span><span class="sxs-lookup"><span data-stu-id="0239a-214">Operation</span></span>

<span data-ttu-id="0239a-215">Profil Verwaltungsbereich</span><span class="sxs-lookup"><span data-stu-id="0239a-215">Profile Management Scope</span></span>

<span data-ttu-id="0239a-216">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="0239a-216">Pre-condition</span></span>

<span data-ttu-id="0239a-217">Nach Bedingung</span><span class="sxs-lookup"><span data-stu-id="0239a-217">Post-condition</span></span>

<span data-ttu-id="0239a-218">Ausführbare Datei im Lua-Kontext</span><span class="sxs-lookup"><span data-stu-id="0239a-218">Executable in LUA context</span></span>

<span data-ttu-id="0239a-219">$ {ROWSPAN2} $install Profil $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="0239a-219">${ROWSPAN2}$Install profile${REMOVE}$</span></span>  

<span data-ttu-id="0239a-220">System weit</span><span class="sxs-lookup"><span data-stu-id="0239a-220">System wide</span></span>

<span data-ttu-id="0239a-221">Das Profil wurde kopiert, im System installiert und ist zur Verwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0239a-221">Profile copied, installed into the system, and available for use.</span></span> <span data-ttu-id="0239a-222">Das Profil kann im systemweiten und aktuellen Benutzerbereich für alle Benutzer aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-222">Profile is enumerable in system-wide and current-user scope for all users.</span></span>

<span data-ttu-id="0239a-223">Bei der Installation des Gerätetreibers unterliegen Richtlinien für die Treiberinstallation.</span><span class="sxs-lookup"><span data-stu-id="0239a-223">During device driver installation, governed by driver installation policies.</span></span> <span data-ttu-id="0239a-224">Andernfalls nein.</span><span class="sxs-lookup"><span data-stu-id="0239a-224">No, otherwise.</span></span>

<span data-ttu-id="0239a-225">Aktueller Benutzer</span><span class="sxs-lookup"><span data-stu-id="0239a-225">Current user</span></span>

<span data-ttu-id="0239a-226">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0239a-226">Not supported</span></span>

<span data-ttu-id="0239a-227">$ {ROWSPAN2} $Uninstall Profil $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="0239a-227">${ROWSPAN2}$Uninstall profile${REMOVE}$</span></span>  

<span data-ttu-id="0239a-228">System weit</span><span class="sxs-lookup"><span data-stu-id="0239a-228">System wide</span></span>

<span data-ttu-id="0239a-229">Das Profil ist im System installiert.</span><span class="sxs-lookup"><span data-stu-id="0239a-229">Profile is installed in the system</span></span>

<span data-ttu-id="0239a-230">Das Profil wurde vom System deinstalliert und optional aus dem Profil Speicher gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0239a-230">Profile uninstalled from the system and optionally deleted from the profile store.</span></span> <span data-ttu-id="0239a-231">Das Profil ist nicht mehr zur Verwendung verfügbar und kann in keinem Bereich aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-231">Profile is no longer available for use and is not enumerable in any scope.</span></span>

<span data-ttu-id="0239a-232">Nein</span><span class="sxs-lookup"><span data-stu-id="0239a-232">No</span></span>

<span data-ttu-id="0239a-233">Aktueller Benutzer</span><span class="sxs-lookup"><span data-stu-id="0239a-233">Current user</span></span>

<span data-ttu-id="0239a-234">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0239a-234">Not supported</span></span>

<span data-ttu-id="0239a-235">$ {ROWSPAN2} $Associate Profil mit Gerät $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="0239a-235">${ROWSPAN2}$Associate profile with device${REMOVE}$</span></span>  

<span data-ttu-id="0239a-236">System weit</span><span class="sxs-lookup"><span data-stu-id="0239a-236">System wide</span></span>

<span data-ttu-id="0239a-237">Profil ist installiert und hat den Typ "ICC" oder "CDMP".</span><span class="sxs-lookup"><span data-stu-id="0239a-237">Profile is installed and is of type ICC or CDMP</span></span>

<span data-ttu-id="0239a-238">Das Profil ist für die Verwendung mit dem Gerät durch alle Benutzer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0239a-238">Profile is available for use with the device by all users.</span></span> <span data-ttu-id="0239a-239">Sie ist für alle Benutzer, die dem Gerät zugeordnet sind, im systemweiten Bereich und auch im Gültigkeitsbereich des aktuellen Benutzers Aufzähl Bar.</span><span class="sxs-lookup"><span data-stu-id="0239a-239">It is enumerable, in system-wide scope and also current-user scope for all users, as associated with the device.</span></span>

<span data-ttu-id="0239a-240">Nein</span><span class="sxs-lookup"><span data-stu-id="0239a-240">No</span></span>

<span data-ttu-id="0239a-241">Aktueller Benutzer</span><span class="sxs-lookup"><span data-stu-id="0239a-241">Current user</span></span>

<span data-ttu-id="0239a-242">Das Profil ist installiert.</span><span class="sxs-lookup"><span data-stu-id="0239a-242">Profile is installed.</span></span> <span data-ttu-id="0239a-243">Es spielt keine Rolle, ob das Profil bereits dem Gerät im systemweiten Gültigkeitsbereich zugeordnet ist und den Typ "ICC" oder "CDMP" hat.</span><span class="sxs-lookup"><span data-stu-id="0239a-243">It does not matter whether the profile is already associated to the device in system-wide scope and is of type ICC or CDMP.</span></span>

<span data-ttu-id="0239a-244">Das Profil ist für die Verwendung mit dem Gerät durch den aktuellen Benutzer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0239a-244">Profile is available for use with the device by current user.</span></span> <span data-ttu-id="0239a-245">Es ist nur im Gültigkeitsbereich des aktuellen Benutzers Aufzähl Bar (es sei denn, es gibt auch eine systemweite Zuordnung), die dem Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0239a-245">It is enumerable only in current-user scope (unless there is a system-wide association as well) as associated with the device.</span></span>

<span data-ttu-id="0239a-246">Ja</span><span class="sxs-lookup"><span data-stu-id="0239a-246">Yes</span></span>

<span data-ttu-id="0239a-247">$ {ROWSPAN2} $Disassociate Profil von Gerät $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="0239a-247">${ROWSPAN2}$Disassociate profile from device${REMOVE}$</span></span>  

<span data-ttu-id="0239a-248">System weit</span><span class="sxs-lookup"><span data-stu-id="0239a-248">System wide</span></span>

<span data-ttu-id="0239a-249">Das Profil ist dem Gerät im systemweiten Gültigkeitsbereich zugeordnet und hat den Typ "ICC" oder "CDMP".</span><span class="sxs-lookup"><span data-stu-id="0239a-249">Profile is associated with the device in system-wide scope and is of type ICC or CDMP</span></span>

<span data-ttu-id="0239a-250">Das Profil ist nicht mehr zur Verwendung verfügbar (mit Ausnahme von Benutzern, die diese Zuordnung in Ihrem aktuellen Benutzerbereich aufweisen).</span><span class="sxs-lookup"><span data-stu-id="0239a-250">Profile is no longer available for use (except for users who have this association in their current-user scope as well).</span></span> <span data-ttu-id="0239a-251">Sie kann nicht im systemweiten Gültigkeitsbereich aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-251">It is not enumerable in system-wide scope.</span></span> <span data-ttu-id="0239a-252">Sie kann jedoch im Gültigkeitsbereich des aktuellen Benutzers aufgeführt werden, für einen Benutzer, der diese Zuordnung im Gültigkeitsbereich hat.</span><span class="sxs-lookup"><span data-stu-id="0239a-252">It could be enumerable in current-user scope though, for a user who has this association in its scope.</span></span>

<span data-ttu-id="0239a-253">Nein</span><span class="sxs-lookup"><span data-stu-id="0239a-253">No</span></span>

<span data-ttu-id="0239a-254">Aktueller Benutzer</span><span class="sxs-lookup"><span data-stu-id="0239a-254">Current user</span></span>

<span data-ttu-id="0239a-255">Das Profil ist dem Gerät im Gültigkeitsbereich des aktuellen Benutzers zugeordnet (unabhängig davon, ob es im systemweiten Gültigkeitsbereich zugeordnet ist) und hat den Typ "ICC" oder "CDMP".</span><span class="sxs-lookup"><span data-stu-id="0239a-255">Profile is associated with the device in current-user scope (irrespective of whether it is associated in system-wide scope) and is of type ICC or CDMP.</span></span>

<span data-ttu-id="0239a-256">Das Profil kann nicht mehr verwendet werden, oder es kann vom aktuellen Benutzer als dem Gerät zugeordnetes Element nicht mehr verwendet werden (es sei denn, es ist auch im systemweiten Gültigkeitsbereich des Geräts zugeordnet).</span><span class="sxs-lookup"><span data-stu-id="0239a-256">Profile is no longer available for use, or enumerable as associated to the device, by current user (unless it is also associated in system-wide scope to the device).</span></span>

<span data-ttu-id="0239a-257">Ja</span><span class="sxs-lookup"><span data-stu-id="0239a-257">Yes</span></span>

<span data-ttu-id="0239a-258">$ {ROWSPAN2} $Set Profil für einen Typ (DMP oder ICC) als Standardwert für ein Gerät $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="0239a-258">${ROWSPAN2}$Set profile for a type (DMP or ICC) as default for a device${REMOVE}$</span></span>  

<span data-ttu-id="0239a-259">System weit</span><span class="sxs-lookup"><span data-stu-id="0239a-259">System wide</span></span>

<span data-ttu-id="0239a-260">Profil ist vom Typ "ICC" oder "CDMP"</span><span class="sxs-lookup"><span data-stu-id="0239a-260">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="0239a-261">Das Profil wird standardmäßig für den jeweiligen Typ mit dem Gerät für alle Benutzer verwendet, mit Ausnahme derjenigen, die diese Einstellung im aktuellen Benutzerbereich überschrieben haben.</span><span class="sxs-lookup"><span data-stu-id="0239a-261">The profile is used by default, for the particular type with the device, for all users except for those who have overridden this setting in their current-user scope.</span></span> <span data-ttu-id="0239a-262">(Das Profil wird installiert und dem Gerätesystem breit zugeordnet, wenn dies nicht bereits der Fall ist.)</span><span class="sxs-lookup"><span data-stu-id="0239a-262">(The profile is installed and associated to the device system wide, if that is not already the case.)</span></span>

<span data-ttu-id="0239a-263">Nein</span><span class="sxs-lookup"><span data-stu-id="0239a-263">No</span></span>

<span data-ttu-id="0239a-264">Aktueller Benutzer</span><span class="sxs-lookup"><span data-stu-id="0239a-264">Current user</span></span>

<span data-ttu-id="0239a-265">Profil ist vom Typ "ICC" oder "CDMP"</span><span class="sxs-lookup"><span data-stu-id="0239a-265">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="0239a-266">Das Profil wird standardmäßig für den jeweiligen Typ mit dem Gerät im Falle des aktuellen Benutzers verwendet, und zwar unabhängig vom systemweiten Standardwert für diesen.</span><span class="sxs-lookup"><span data-stu-id="0239a-266">The profile is used by default for the particular type with the device in case of current user, irrespective of the system-wide default for this.</span></span> <span data-ttu-id="0239a-267">(Das Profil wird installiert und dem Gerät für den aktuellen Benutzer zugeordnet, wenn dies nicht bereits der Fall ist.)</span><span class="sxs-lookup"><span data-stu-id="0239a-267">(The profile is installed and associated to the device for current user, if that is not already the case.)</span></span>

<span data-ttu-id="0239a-268">Ja, wenn das Profil bereits installiert ist</span><span class="sxs-lookup"><span data-stu-id="0239a-268">Yes, if the profile is already installed</span></span>

<span data-ttu-id="0239a-269">$ {ROWSPAN2} $Set Profil für einen Typ ("ICC", "DMP", "Camp", "GMMP") und eine Untertyp Kombination als globaler Standardwert $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="0239a-269">${ROWSPAN2}$Set profile for a type (ICC, DMP, CAMP, GMMP) and subtype combination as global default${REMOVE}$</span></span>  

<span data-ttu-id="0239a-270">System weit</span><span class="sxs-lookup"><span data-stu-id="0239a-270">System wide</span></span>

<span data-ttu-id="0239a-271">Geräte können nur die "ICC"-und "CDMP"-Profile zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-271">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="0239a-272">Das Profil wird standardmäßig für den jeweiligen Typ verwendet.</span><span class="sxs-lookup"><span data-stu-id="0239a-272">The profile is used by default for the particular type.</span></span> <span data-ttu-id="0239a-273">Benutzer können diese Einstellung im Gültigkeitsbereich des aktuellen Benutzers außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="0239a-273">Users can override this setting in the current-user scope.</span></span> <span data-ttu-id="0239a-274">(Das Profil ist installiert, wenn dies nicht bereits der Fall ist.)</span><span class="sxs-lookup"><span data-stu-id="0239a-274">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="0239a-275">Nein</span><span class="sxs-lookup"><span data-stu-id="0239a-275">No</span></span>

<span data-ttu-id="0239a-276">Aktueller Benutzer</span><span class="sxs-lookup"><span data-stu-id="0239a-276">Current user</span></span>

<span data-ttu-id="0239a-277">Geräte können nur die "ICC"-und "CDMP"-Profile zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-277">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="0239a-278">Das Profil wird standardmäßig für den jeweiligen Typ des aktuellen Benutzers verwendet.</span><span class="sxs-lookup"><span data-stu-id="0239a-278">The profile is used by default for the particular type for current user.</span></span> <span data-ttu-id="0239a-279">(Das Profil ist installiert, wenn dies nicht bereits der Fall ist.)</span><span class="sxs-lookup"><span data-stu-id="0239a-279">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="0239a-280">Ja, wenn das Profil bereits installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0239a-280">Yes, if the profile is already installed.</span></span>

<span data-ttu-id="0239a-281">$ {ROWSPAN2} $Erase die Überschreibung des aktuellen Benutzers für eine bestimmte Standardprofil Einstellung, sodass der System Standard immer als Fallback für den aktuellen Benutzerbereich verwendet wird. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="0239a-281">${ROWSPAN2}$Erase the current-user override for a particular default profile setting, so that the system default always gets used (as fallback) even for current-user scope.${REMOVE}$</span></span>  

<span data-ttu-id="0239a-282">System weit</span><span class="sxs-lookup"><span data-stu-id="0239a-282">System wide</span></span>

<span data-ttu-id="0239a-283">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="0239a-283">Not applicable</span></span>

<span data-ttu-id="0239a-284">Aktueller Benutzer</span><span class="sxs-lookup"><span data-stu-id="0239a-284">Current user</span></span>

<span data-ttu-id="0239a-285">Auch für aktuelle Benutzer Abfragen von Standardprofil Einstellungen werden systemweite Einstellungen zur Verwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0239a-285">Even for current-user queries on default profile settings, system-wide settings are returned for use.</span></span>

<span data-ttu-id="0239a-286">Ja</span><span class="sxs-lookup"><span data-stu-id="0239a-286">Yes</span></span>

<span data-ttu-id="0239a-287">$ {ROWSPAN2} $Enumerate installierte Profile, die bestimmte Kriterien erfüllen (z. b. Geräteklasse, Profilklasse usw.) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="0239a-287">${ROWSPAN2}$Enumerate installed profiles satisfying particular criteria (like device class, profile class, etc.)${REMOVE}$</span></span>  

<span data-ttu-id="0239a-288">System weit</span><span class="sxs-lookup"><span data-stu-id="0239a-288">System wide</span></span>

<span data-ttu-id="0239a-289">Nur die "ICC"-und "CDMP"-Profile können für Geräte zugeordnet und aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-289">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="0239a-290">Profile, die installiert sind und die angegebenen Kriterien im systemweiten Gültigkeitsbereich erfüllen, werden aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="0239a-290">Profiles that are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="0239a-291">Ja</span><span class="sxs-lookup"><span data-stu-id="0239a-291">Yes</span></span>

<span data-ttu-id="0239a-292">Aktueller Benutzer</span><span class="sxs-lookup"><span data-stu-id="0239a-292">Current user</span></span>

<span data-ttu-id="0239a-293">Den Geräten können nur die-und-CDMP-Profile zugeordnet und somit für Geräte aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-293">Only ICC and CDMP profiles can be associated with devices and thus enumerated for devices.</span></span>

<span data-ttu-id="0239a-294">Profile, die installiert sind und die angegebenen Kriterien im systemweiten Gültigkeitsbereich erfüllen, werden aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="0239a-294">Profiles which are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="0239a-295">Ja</span><span class="sxs-lookup"><span data-stu-id="0239a-295">Yes</span></span>

<span data-ttu-id="0239a-296">$ {ROWSPAN2} $Enumerate Profile, die einem bestimmten Gerät zugeordnet sind, das bestimmte Kriterien erfüllt, z. b. Geräteklasse und Profilklasse $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="0239a-296">${ROWSPAN2}$Enumerate profiles associated with a particular device satisfying particular criteria, such as device class, and profile class${REMOVE}$</span></span>  

<span data-ttu-id="0239a-297">System weit</span><span class="sxs-lookup"><span data-stu-id="0239a-297">System wide</span></span>

<span data-ttu-id="0239a-298">Nur die "ICC"-und "CDMP"-Profile können für Geräte zugeordnet und aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-298">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="0239a-299">Profile, die dem Gerät im systemweiten Gültigkeitsbereich zugeordnet sind und die angegebenen Kriterien im systemweiten Gültigkeitsbereich erfüllen, werden aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="0239a-299">Profiles that are associated with the device in system-wide scope and satisfies the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="0239a-300">Ja</span><span class="sxs-lookup"><span data-stu-id="0239a-300">Yes</span></span>

<span data-ttu-id="0239a-301">Aktueller Benutzer</span><span class="sxs-lookup"><span data-stu-id="0239a-301">Current user</span></span>

<span data-ttu-id="0239a-302">Nur die "ICC"-und "CDMP"-Profile können für Geräte zugeordnet und aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-302">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="0239a-303">Profile, die dem Gerät im Gültigkeitsbereich des aktuellen Benutzers zugeordnet sind, einschließlich der systemweiten Zuordnungen, die die angegebenen Kriterien im aktuellen Benutzerbereich erfüllen, werden aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="0239a-303">Profiles that are available as associated with the device in current-user scope, which includes the system-wide associations and satisfies the specified criteria in current-user scope are enumerated.</span></span>

<span data-ttu-id="0239a-304">Ja</span><span class="sxs-lookup"><span data-stu-id="0239a-304">Yes</span></span>



 

<span data-ttu-id="0239a-305">Die gültigen Farbprofil Typen werden von der colorprofiletype-Enumeration bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="0239a-305">The valid color profile types are provided by the COLORPROFILETYPE enumeration.</span></span>

<span data-ttu-id="0239a-306">Die gültigen Farbprofil-Untertypen werden von der colorprofilesubtype-Enumeration bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="0239a-306">The valid color profile subtypes are provided by the COLORPROFILESUBTYPE enumeration.</span></span>

<span data-ttu-id="0239a-307">In der folgenden Tabelle sind die gültigen Profiltyp-/Untertyp Kombinationen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0239a-307">The valid profile type/subtype combinations are shown in the following table.</span></span>



<span data-ttu-id="0239a-308">COLORPROFILETYPE </span><span class="sxs-lookup"><span data-stu-id="0239a-308">COLORPROFILETYPE</span></span>

<span data-ttu-id="0239a-309">Gültiger colorprofilesubtype</span><span class="sxs-lookup"><span data-stu-id="0239a-309">Valid COLORPROFILESUBTYPE</span></span>

<span data-ttu-id="0239a-310">Notizen</span><span class="sxs-lookup"><span data-stu-id="0239a-310">Notes</span></span>

<span data-ttu-id="0239a-311">Gerätestandard</span><span class="sxs-lookup"><span data-stu-id="0239a-311">Device Default</span></span>

<span data-ttu-id="0239a-312">Globaler Standardwert</span><span class="sxs-lookup"><span data-stu-id="0239a-312">Global Default</span></span>

<span data-ttu-id="0239a-313">Beabsichtigte Verwendung</span><span class="sxs-lookup"><span data-stu-id="0239a-313">Intended Use</span></span>

<span data-ttu-id="0239a-314">Beabsichtigte Verwendung</span><span class="sxs-lookup"><span data-stu-id="0239a-314">Intended Use</span></span>

<span data-ttu-id="0239a-315">CPT- \_ ICC</span><span class="sxs-lookup"><span data-stu-id="0239a-315">CPT\_ICC</span></span>

<span data-ttu-id="0239a-316">CPST \_ None</span><span class="sxs-lookup"><span data-stu-id="0239a-316">CPST\_NONE</span></span>

<span data-ttu-id="0239a-317">Mit einem Gerät verknüpften Standard-ICC-Profil erhalten/festlegen</span><span class="sxs-lookup"><span data-stu-id="0239a-317">Get/Set default ICC profile associated with a device</span></span>

<span data-ttu-id="0239a-318">CPST \_ rgbworkingspace oder CPST \_ customworkingspace</span><span class="sxs-lookup"><span data-stu-id="0239a-318">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="0239a-319">Sie sollten das ICC-Profil als globales RGB-oder benutzerdefiniertes Arbeitsplatz Profil festlegen.</span><span class="sxs-lookup"><span data-stu-id="0239a-319">Get/Set ICC profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="0239a-320">Siehe Hinweis.</span><span class="sxs-lookup"><span data-stu-id="0239a-320">See Note.</span></span>

<span data-ttu-id="0239a-321">Der colorprofiletype CPT \_ -ICC und der CPT- \_ DMP schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="0239a-321">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="0239a-322">Das Standard Farbprofil, das Sie für einen bestimmten Arbeitsbereich festlegen (RGB oder Custom), kann entweder ein ICC-Profil oder ein DMP-Profil sein, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="0239a-322">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>

<span data-ttu-id="0239a-323">CPT- \_ DMP</span><span class="sxs-lookup"><span data-stu-id="0239a-323">CPT\_DMP</span></span>

<span data-ttu-id="0239a-324">CPST \_ None</span><span class="sxs-lookup"><span data-stu-id="0239a-324">CPST\_NONE</span></span>

<span data-ttu-id="0239a-325">Standard-DMP-Profil, das einem Gerät zugeordnet ist, erhalten/festlegen</span><span class="sxs-lookup"><span data-stu-id="0239a-325">Get/Set default DMP profile associated with a device</span></span>

<span data-ttu-id="0239a-326">CPST \_ rgbworkingspace oder CPST \_ customworkingspace</span><span class="sxs-lookup"><span data-stu-id="0239a-326">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="0239a-327">Legen Sie das DMP-Profil als globales RGB-oder benutzerdefiniertes Arbeitsplatz Profil fest.</span><span class="sxs-lookup"><span data-stu-id="0239a-327">Get/Set DMP profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="0239a-328">Siehe Hinweis.</span><span class="sxs-lookup"><span data-stu-id="0239a-328">See Note.</span></span>

<span data-ttu-id="0239a-329">Der colorprofiletype CPT \_ -ICC und der CPT- \_ DMP schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="0239a-329">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="0239a-330">Das Standard Farbprofil, das Sie für einen bestimmten Arbeitsbereich festlegen (RGB oder Custom), kann entweder ein ICC-Profil oder ein DMP-Profil sein, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="0239a-330">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>



 

> [!Note]  
> <span data-ttu-id="0239a-331">Wenn wcssetdefaultcolorprofile aufgerufen wird, um ein DMP-Profil als Standardprofil für den RGB-Arbeitsbereich oder einen benutzerdefinierten Arbeitsbereich festzulegen, ist nur ein DMP-Profil vom Typ rgbvirtualdevice, LCD oder CRT gültig.</span><span class="sxs-lookup"><span data-stu-id="0239a-331">When WcsSetDefaultColorProfile is called to set a DMP profile as the default profile for the RGB working space or a custom working space, only a DMP profile that is of type RGBVirtualDevice, LCD, or CRT is valid.</span></span>
>
>  
>
> <span data-ttu-id="0239a-332">Wenn wcssetdefaultcolorprofile aufgerufen wird, um ein ICC-Profil als Standardprofil für den RGB-Arbeitsbereich oder einen benutzerdefinierten Arbeitsbereich festzulegen, ist nur ein ICC-Profil, dessen Klasse "SPAC" oder "DISP" ist und dessen Farbraum "RGB" ist, gültig.</span><span class="sxs-lookup"><span data-stu-id="0239a-332">When WcsSetDefaultColorProfile is called to set an ICC profile as the default profile for the RGB working space or a custom working space, only an ICC profile whose class is "spac" or "disp," and whose color space is "RGB" is valid.</span></span>

 

<span data-ttu-id="0239a-333">Die Architektur basiert auf den Anforderungen der Vorgänge, die in den obigen Enumerationen und Tabellen erwähnt wurden.</span><span class="sxs-lookup"><span data-stu-id="0239a-333">The architecture is designed according to the requirements of the operations as mentioned in the enumerations and tables above.</span></span>

### <a name="profile-management-public-api-layer"></a><span data-ttu-id="0239a-334">Ebene der öffentlichen API der Profilverwaltung</span><span class="sxs-lookup"><span data-stu-id="0239a-334">Profile management public API layer</span></span>

<span data-ttu-id="0239a-335">Da der Profil Verwaltungsbereich von Legacy-ICM2-APIs nicht unterstützt wird, ist ein neuer Satz von WCS-Profilverwaltungs-APIs erforderlich, der den Profil Verwaltungsbereich als systemweit oder aktueller Benutzer definiert.</span><span class="sxs-lookup"><span data-stu-id="0239a-335">Because profile management scope is not supported by legacy ICM2 APIs, a new set of WCS profile management APIs is required that defines profile management scope as system wide or current user.</span></span> <span data-ttu-id="0239a-336">?</span><span class="sxs-lookup"><span data-stu-id="0239a-336">?</span></span> <span data-ttu-id="0239a-337">Ältere ICM2-APIs werden weiterhin aus Gründen der Abwärtskompatibilität unterstützt und arbeiten im Profil Verwaltungsbereich, der für den-Befehl implizit ist.</span><span class="sxs-lookup"><span data-stu-id="0239a-337">Legacy ICM2 APIs continue to be supported for backward compatibility, and work on profile management scope that is implicit for the call.</span></span> <span data-ttu-id="0239a-338">o ICM2-APIs, die im Gültigkeitsbereich des aktuellen Benutzers funktionieren?</span><span class="sxs-lookup"><span data-stu-id="0239a-338">o ICM2 APIs that work on current-user scope ?</span></span> <span data-ttu-id="0239a-339">Dies gilt für Vorgänge, die für den systemweiten und aktuellen Benutzerbereich in der WCS-Profilverwaltung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-339">This is for operations that are supported for both system wide and current-user scope in WCS profile management.</span></span> <span data-ttu-id="0239a-340">Ältere ICM2-APIs werden für neue WCS-APIs mit Profil Verwaltungsbereich als aktueller Benutzer aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0239a-340">Legacy ICM2 APIs call on new WCS APIs with profile management scope as current user.</span></span> <span data-ttu-id="0239a-341">Dies ergibt sich aus der Sicht des Benutzers, da dies benutzerspezifische Einstellungen von Legacy Anwendungen und die meisten Vorgänge im Lua-Kontext ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="0239a-341">This makes sense from user perspective because this enables per-user settings from legacy applications and also executing most of the operations in LUA context.</span></span> <span data-ttu-id="0239a-342">o ICM2-APIs, die im systemweiten Bereich funktionieren?</span><span class="sxs-lookup"><span data-stu-id="0239a-342">o ICM2 APIs that work on system-wide scope ?</span></span> <span data-ttu-id="0239a-343">Dies gilt für Vorgänge (Installations Profile und Deinstallations Profile), die nur den systemweiten Bereich unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0239a-343">This is for operations (install profiles and uninstall profiles) that support only system-wide scope.</span></span> <span data-ttu-id="0239a-344">Es werden keine neuen APIs für die WCS-Profilverwaltung erstellt, und vorhandene APIs können nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-344">No new WCS profile management APIs are created and existing APIs can be modified.</span></span>

<span data-ttu-id="0239a-345">Die zugrunde liegenden Implementierungen der Profil Verwaltungsvorgänge funktionieren in den folgenden Konfigurationsdaten Entitäten, um den Kontext für farbverarbeitungs Algorithmen zum Bereitstellen von Farb Verwaltungsfunktionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0239a-345">The underlying implementations of the profile management operations work on the following configuration data entities to create the context for color processing algorithms to provide color management functionalities.</span></span> <span data-ttu-id="0239a-346">Sie sind entweder gerätespezifische oder globale (geräteunabhängige) Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="0239a-346">They are either device specific or global (device independent) settings.</span></span> <span data-ttu-id="0239a-347">gerätespezifische Konfigurationsdaten:?</span><span class="sxs-lookup"><span data-stu-id="0239a-347">o Device specific configuration data: ?</span></span> <span data-ttu-id="0239a-348">Liste der Profile, die einem bestimmten Gerät zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0239a-348">List of profiles associated with a particular device.</span></span> <span data-ttu-id="0239a-349">?</span><span class="sxs-lookup"><span data-stu-id="0239a-349">?</span></span> <span data-ttu-id="0239a-350">Standardprofil für verschiedene Profiltypen, die einem Gerät zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0239a-350">Default profile for different profile types associated with a device.</span></span> <span data-ttu-id="0239a-351">?</span><span class="sxs-lookup"><span data-stu-id="0239a-351">?</span></span> <span data-ttu-id="0239a-352">Abgleichsmodus für die Enumeration.</span><span class="sxs-lookup"><span data-stu-id="0239a-352">Matching mode of profiles used for enumeration.</span></span> <span data-ttu-id="0239a-353">Globale Konfigurationsdaten:?</span><span class="sxs-lookup"><span data-stu-id="0239a-353">o Global configuration data: ?</span></span> <span data-ttu-id="0239a-354">Liste der im System installierten Profile.</span><span class="sxs-lookup"><span data-stu-id="0239a-354">List of profiles installed in the system.</span></span> <span data-ttu-id="0239a-355">?</span><span class="sxs-lookup"><span data-stu-id="0239a-355">?</span></span> <span data-ttu-id="0239a-356">Globales Standardprofil für verschiedene Profiltypen.</span><span class="sxs-lookup"><span data-stu-id="0239a-356">Global default profile for different profile types.</span></span> <span data-ttu-id="0239a-357">?</span><span class="sxs-lookup"><span data-stu-id="0239a-357">?</span></span> <span data-ttu-id="0239a-358">Die zugrunde liegenden Implementierungen der Konfigurationsdaten Speicherung übernehmen den Speicherbereich für Konfigurationsdaten (entweder Geräte unabhängig oder gerätespezifisch), bei denen es sich entweder um systemweite oder den aktuellen Benutzer handeln kann.</span><span class="sxs-lookup"><span data-stu-id="0239a-358">The underlying implementations of configuration data storage take in storage scope for configuration data (either device independent or device specific), which can be either system wide or current user.</span></span> <span data-ttu-id="0239a-359">Dies unterscheidet sich vom Profil Verwaltungsbereich.</span><span class="sxs-lookup"><span data-stu-id="0239a-359">This is different from profile management scope.</span></span> <span data-ttu-id="0239a-360">Ein Vorgang mit dem Profil Verwaltungsbereich aktueller Benutzer kann einen Lesevorgang aus einem systemweiten Speicherbereich bewirken, wenn die aktuelle Benutzereinstellung für diesen Vorgang nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0239a-360">An operation with current-user profile management scope can cause a read from a system-wide storage scope if the current-user setting for that operation is not present.</span></span> <span data-ttu-id="0239a-361">?</span><span class="sxs-lookup"><span data-stu-id="0239a-361">?</span></span> <span data-ttu-id="0239a-362">Die ICM2/WCS-API-Schicht ruft in dieser Speicher Ebene auf, um Daten mit dem entsprechenden Speicherbereich zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0239a-362">The ICM2/WCS API layer calls in this storage layer for getting and setting data with appropriate storage scope.</span></span> <span data-ttu-id="0239a-363">Die Speicher Ebene ist für den Profil Verwaltungsbereich transparent.</span><span class="sxs-lookup"><span data-stu-id="0239a-363">The storage layer is transparent to profile management scope.</span></span> <span data-ttu-id="0239a-364">Die Logik für das Kombinieren von Daten aus aktuellen Benutzer-und systemweiten Speicherbereichen zum Erstellen oder Aktualisieren einer Konfiguration gemäß dem Profil Verwaltungsbereich, der vom API-Aufrufer festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="0239a-364">The logic for combining data from current-user and system-wide storage scopes to create or update a configuration according to the profile management scope specified by the API caller.</span></span> <span data-ttu-id="0239a-365">Diese Logik ist in der ICM2/WCS-API-Ebene vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0239a-365">This logic is present in the ICM2/WCS API layer.</span></span>

### <a name="device-specific-storage-layer"></a><span data-ttu-id="0239a-366">Gerätespezifische Speicher Ebene</span><span class="sxs-lookup"><span data-stu-id="0239a-366">Device-specific storage layer</span></span>

<span data-ttu-id="0239a-367">Der Speicher für verschiedene Klassen von Geräten, wie z. b. Print, Capture oder Display, kann sich voneinander unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="0239a-367">The storage for different classes of devices like print, capture or display could be different from each other.</span></span> <span data-ttu-id="0239a-368">Beispielsweise müssen Konfigurationsdaten für ein Druck Gerät mithilfe von standardmäßigen Druck-APIs, wie z. b. setprinterdataex und getprinterdataex, gespeichert werden, damit die Profile kopiert werden können und Einstellungen während der Point-and-Print-Verbindung an einen Client Computer übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-368">For example, configuration data for a print device must be stored using standard print APIs, such as SetPrinterDataEx and GetPrinterDataEx, to enable the profiles to be copied and settings to be transferred to a client machine during Point-and-Print connection.</span></span> <span data-ttu-id="0239a-369">?</span><span class="sxs-lookup"><span data-stu-id="0239a-369">?</span></span> <span data-ttu-id="0239a-370">Diese Schicht exportiert Funktionen zum Öffnen von speichern, Abrufen von Daten, Festlegen von Daten und Schließen des Speichers mithilfe allgemeiner vordefinierter Schnittstellen, sodass die Speicher Ebene der Profil Verwaltungs Konfiguration aufgerufen werden kann, während Sie transparent ist, wie die Daten für das Gerät gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0239a-370">This layer exports functionality to open store, get data, set data and close store using common pre-defined interfaces so that the profile management configuration storage layer can call into them while being transparent to the way the data gets stored for that device.</span></span>

<span data-ttu-id="0239a-371">Diese Architektur wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="0239a-371">The following diagram illustrates this architecture.</span></span>



<span data-ttu-id="0239a-372">Ebene der öffentlichen API der Profilverwaltung</span><span class="sxs-lookup"><span data-stu-id="0239a-372">Profile Management Public API Layer</span></span>

<span data-ttu-id="0239a-373">$ {ROWSPAN2} $Legacy ICM2-APIs für Vorgänge, die nur den systemweiten Profil Verwaltungsbereich in Vista unterstützen (installieren, deinstallieren und das Farb Verzeichnis erhalten).</span><span class="sxs-lookup"><span data-stu-id="0239a-373">${ROWSPAN2}$Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista (install, uninstall, and get color directory).</span></span> <span data-ttu-id="0239a-374">Die Konfigurations Speicher Ebene wird mit dem entsprechenden Speicherbereich aufgerufen. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="0239a-374">They call the configuration storage layer with appropriate storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="0239a-375">Ältere ICM2-API für Vorgänge, die sowohl den systemweiten als auch den aktuellen Profil Verwaltungsbereich in Vista unterstützen (alle Vorgänge außer "Install", "Uninstall" und "Get Color Directory").</span><span class="sxs-lookup"><span data-stu-id="0239a-375">Legacy ICM2 API for operations that support both system-wide and current-user profile management scope in Vista (all operations other than install, uninstall, and get color directory).</span></span> <span data-ttu-id="0239a-376">Sie arbeiten implizit mit dem aktuellen Benutzerbereich und wenden eine neue WCS-API mit Profil Verwaltungsbereich als aktueller Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="0239a-376">They implicitly work on current-user scope, and call into new WCS API with profile management scope as current user.</span></span>

<span data-ttu-id="0239a-377">Neue WCS-API mit Unterstützung für systemweite und aktuelle Profil Verwaltungsbereiche.</span><span class="sxs-lookup"><span data-stu-id="0239a-377">New WCS API with system-wide and current-user profile management scope support.</span></span> <span data-ttu-id="0239a-378">Sie bezeichnen die Konfigurations Speicher Ebene mit dem entsprechenden Speicherbereich.</span><span class="sxs-lookup"><span data-stu-id="0239a-378">They call the configuration storage layer with appropriate storage scope.</span></span>



 



<span data-ttu-id="0239a-379">Speicher Ebene für die Profil Verwaltungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="0239a-379">Profile Management Configuration Storage Layer</span></span>

<span data-ttu-id="0239a-380">Geräteunabhängige globale Konfigurations Routinen</span><span class="sxs-lookup"><span data-stu-id="0239a-380">Device-independent global configuration routines</span></span>

<span data-ttu-id="0239a-381">Gerätespezifische Konfigurations Routinen</span><span class="sxs-lookup"><span data-stu-id="0239a-381">Device-specific configuration routines</span></span>

<span data-ttu-id="0239a-382">$ {ROWSPAN3} $profile Installation und geräteunabhängige Standardprofil Einstellungen-Verwaltung, unterstützt im systemweiten und aktuellen Benutzerspeicher Bereich. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="0239a-382">${ROWSPAN3}$Profile installation and device-independent default profile settings management, supported in system-wide and current-user storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="0239a-383">Geräte Zuordnung und gerätespezifische Standardprofil Einstellungen-Verwaltung, unterstützt im systemweiten und aktuellen Benutzerspeicher Bereich.</span><span class="sxs-lookup"><span data-stu-id="0239a-383">Device association and device-specific default profile settings management, supported in system-wide and current-user storage scope.</span></span>

<span data-ttu-id="0239a-384">Device-Specific-Speicher Ebene</span><span class="sxs-lookup"><span data-stu-id="0239a-384">Device-Specific Storage layer</span></span>

<span data-ttu-id="0239a-385">Drucken eines bestimmten Speichers</span><span class="sxs-lookup"><span data-stu-id="0239a-385">Print specific storage</span></span>

<span data-ttu-id="0239a-386">Anzeigen eines bestimmten Speichers</span><span class="sxs-lookup"><span data-stu-id="0239a-386">Display specific storage</span></span>

<span data-ttu-id="0239a-387">Erfassen eines bestimmten Speichers</span><span class="sxs-lookup"><span data-stu-id="0239a-387">Capture specific storage</span></span>



 

<span data-ttu-id="0239a-388">Ältere ICM2-APIs für Vorgänge, die nur den systemweiten Profil Verwaltungsbereich in Vista unterstützen, weisen keine Verhaltensänderungen auf.</span><span class="sxs-lookup"><span data-stu-id="0239a-388">Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista have no changes in behavior.</span></span> <span data-ttu-id="0239a-389">Installations-und Deinstallations Vorgänge fallen in diese Kategorie.</span><span class="sxs-lookup"><span data-stu-id="0239a-389">Install and uninstall operations fall in this category.</span></span>

<span data-ttu-id="0239a-390">Ältere ICM2-APIs für Vorgänge, die sowohl den systemweiten als auch den aktuellen Profil Verwaltungsbereich unterstützen, haben das Verhalten geändert, um die aktuellen Benutzereinstellungen abzufragen und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0239a-390">Legacy ICM2 APIs for operations that support both system-wide and current-user profile management scope have their behavior changed to query and configure current-user settings.</span></span> <span data-ttu-id="0239a-391">Alle Vorgänge außer Installation und Deinstallation fallen in diese Kategorie.</span><span class="sxs-lookup"><span data-stu-id="0239a-391">All operations other than install and uninstall fall in this category.</span></span>

 

 




