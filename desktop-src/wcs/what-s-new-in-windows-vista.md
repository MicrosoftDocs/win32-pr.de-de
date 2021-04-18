---
title: Neuerungen in Windows Vista
description: Version 1,0 der Abbild Farbverwaltung (Image Color Management, ICM) wurde in Microsoft Windows 95 bereitgestellt und stellt grundlegende Farb Verwaltungsfunktionen innerhalb von Windows-Geräte Kontexten bereit.
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- Windows Color System (WCS), Windows Vista
- WCS (Windows Color System), Windows Vista
- Bildfarben Verwaltung, Windows Vista
- Farbverwaltung, Windows Vista
- Farben, Windows Vista
- Windows Color System (WCS), Betriebssysteme
- WCS (Windows Color System), Betriebssysteme
- Abbild Farben Verwaltung, Betriebssysteme
- Farbverwaltung, Betriebssysteme
- Farben, Betriebssysteme
- Farbverwaltung (Image Color Management; ICM)
- ICM (Bildfarben Verwaltung)
- Windows Vista-Farbverwaltung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b889dd0ba3b044f0d0f158bd2364f5c3216ec39
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106354887"
---
# <a name="whats-new-in-windows-vista"></a><span data-ttu-id="41891-116">Neuerungen in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41891-116">What's New in Windows Vista</span></span>

<span data-ttu-id="41891-117">Version 1,0 der Abbild Farbverwaltung (Image Color Management, ICM) wurde in Microsoft Windows 95 bereitgestellt und stellt grundlegende Farb Verwaltungsfunktionen innerhalb von Windows-Geräte Kontexten bereit.</span><span class="sxs-lookup"><span data-stu-id="41891-117">Version 1.0 of Image Color Management (ICM) was delivered in Microsoft Windows 95, and provides basic color management capabilities within Windows device contexts.</span></span>

<span data-ttu-id="41891-118">Die ICM-Version 2,0 wurde in Windows 98, Windows Millennium Edition, Windows 2000 und Windows XP bereitgestellt und enthielt eine Reihe von neuen Funktionen, die die Farbverwaltung außerhalb der Geräte Kontexte implementierten.</span><span class="sxs-lookup"><span data-stu-id="41891-118">ICM version 2.0 was delivered in Windows 98, Windows Millennium Edition, Windows 2000, and WindowsXP and included a variety of new functions that implemented color management outside of device contexts.</span></span> <span data-ttu-id="41891-119">Diese neuen Funktionen waren für anspruchsvollere Anforderungen an die Farbverwaltung geeignet und lieferten Anwendungen eine bessere Kontrolle über den Farb Verwaltungsprozess.</span><span class="sxs-lookup"><span data-stu-id="41891-119">These new functions were suitable for more demanding color management requirements, and gave applications greater control over the color-management process.</span></span>

<span data-ttu-id="41891-120">Mit der Veröffentlichung von Windows Vista ist ICM 2,0 jetzt in Windows Color System (WCS) 1,0 enthalten. Dadurch werden weitere Funktionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="41891-120">With the release of Windows Vista, ICM 2.0 is now included in Windows Color System (WCS) 1.0, which adds more functionality.</span></span> <span data-ttu-id="41891-121">In der folgenden Tabelle werden neue Anwendungs Programmierschnittstellen (API) aufgelistet, die in Windows Vista ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="41891-121">The following table lists new application programming interfaces (API) that ship in Windows Vista.</span></span>

## <a name="new-api-shipping-in-windows-vista"></a><span data-ttu-id="41891-122">Neuer API-Versand in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41891-122">New API Shipping in Windows Vista</span></span>



<span data-ttu-id="41891-123">Enumerationen</span><span class="sxs-lookup"><span data-stu-id="41891-123">Enumerations</span></span>

<span data-ttu-id="41891-124">API-Name</span><span class="sxs-lookup"><span data-stu-id="41891-124">API Name</span></span>

<span data-ttu-id="41891-125">Header</span><span class="sxs-lookup"><span data-stu-id="41891-125">Header</span></span>

<span data-ttu-id="41891-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="41891-126">Library</span></span>

[<span data-ttu-id="41891-127">**Colordatatype**</span><span class="sxs-lookup"><span data-stu-id="41891-127">**COLORDATATYPE**</span></span>](/windows/win32/api/icm/ne-icm-colordatatype)

<span data-ttu-id="41891-128">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-128">icm.h</span></span>

<span data-ttu-id="41891-129">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-129">mscms.lib</span></span>

[<span data-ttu-id="41891-130">**Colorprofilesubtype**</span><span class="sxs-lookup"><span data-stu-id="41891-130">**COLORPROFILESUBTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

<span data-ttu-id="41891-131">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-131">icm.h</span></span>

<span data-ttu-id="41891-132">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-132">mscms.lib</span></span>

[<span data-ttu-id="41891-133">**Colorprofiletype**</span><span class="sxs-lookup"><span data-stu-id="41891-133">**COLORPROFILETYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofiletype)

<span data-ttu-id="41891-134">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-134">icm.h</span></span>

<span data-ttu-id="41891-135">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-135">mscms.lib</span></span>

[<span data-ttu-id="41891-136">**WCS- \_ Profil \_ Verwaltungs \_ Bereich**</span><span class="sxs-lookup"><span data-stu-id="41891-136">**WCS\_PROFILE\_MANAGEMENT\_SCOPE**</span></span>](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

<span data-ttu-id="41891-137">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-137">icm.h</span></span>

<span data-ttu-id="41891-138">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-138">mscms.lib</span></span>



 



<span data-ttu-id="41891-139">Functions</span><span class="sxs-lookup"><span data-stu-id="41891-139">Functions</span></span>

<span data-ttu-id="41891-140">API-Name</span><span class="sxs-lookup"><span data-stu-id="41891-140">API Name</span></span>

<span data-ttu-id="41891-141">Header</span><span class="sxs-lookup"><span data-stu-id="41891-141">Header</span></span>

<span data-ttu-id="41891-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="41891-142">Library</span></span>

[<span data-ttu-id="41891-143">**Wcsassociatecolorprofilewithdevice**</span><span class="sxs-lookup"><span data-stu-id="41891-143">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="41891-144">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-144">icm.h</span></span>

<span data-ttu-id="41891-145">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-145">mscms.lib</span></span>

[<span data-ttu-id="41891-146">**Wcscheckcolors**</span><span class="sxs-lookup"><span data-stu-id="41891-146">**WcsCheckColors**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="41891-147">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-147">icm.h</span></span>

<span data-ttu-id="41891-148">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-148">mscms.lib</span></span>

[<span data-ttu-id="41891-149">**Wcscreateiccprofile**</span><span class="sxs-lookup"><span data-stu-id="41891-149">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

<span data-ttu-id="41891-150">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-150">icm.h</span></span>

<span data-ttu-id="41891-151">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-151">mscms.lib</span></span>

[<span data-ttu-id="41891-152">**Wcsdisassociatecolorprofilefromdevice**</span><span class="sxs-lookup"><span data-stu-id="41891-152">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

<span data-ttu-id="41891-153">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-153">icm.h</span></span>

<span data-ttu-id="41891-154">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-154">mscms.lib</span></span>

[<span data-ttu-id="41891-155">**Wcsenaufcolorprofiles**</span><span class="sxs-lookup"><span data-stu-id="41891-155">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

<span data-ttu-id="41891-156">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-156">icm.h</span></span>

<span data-ttu-id="41891-157">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-157">mscms.lib</span></span>

[<span data-ttu-id="41891-158">**Wcsenaufcolorprofilessize**</span><span class="sxs-lookup"><span data-stu-id="41891-158">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

<span data-ttu-id="41891-159">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-159">icm.h</span></span>

<span data-ttu-id="41891-160">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-160">mscms.lib</span></span>

[<span data-ttu-id="41891-161">**Wcsgetdefaultcolorprofile**</span><span class="sxs-lookup"><span data-stu-id="41891-161">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

<span data-ttu-id="41891-162">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-162">icm.h</span></span>

<span data-ttu-id="41891-163">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-163">mscms.lib</span></span>

[<span data-ttu-id="41891-164">**Wcsgetdefaultcolorprofilesize**</span><span class="sxs-lookup"><span data-stu-id="41891-164">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

<span data-ttu-id="41891-165">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-165">icm.h</span></span>

<span data-ttu-id="41891-166">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-166">mscms.lib</span></span>

[<span data-ttu-id="41891-167">**Wcsgetdefaultrenderingintent**</span><span class="sxs-lookup"><span data-stu-id="41891-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="41891-168">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-168">icm.h</span></span>

<span data-ttu-id="41891-169">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-169">mscms.lib</span></span>

[<span data-ttu-id="41891-170">**Wcsgetuseperuserprofiles**</span><span class="sxs-lookup"><span data-stu-id="41891-170">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="41891-171">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-171">icm.h</span></span>

<span data-ttu-id="41891-172">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-172">mscms.lib</span></span>

[<span data-ttu-id="41891-173">**Wcsopeincolorprofilew**</span><span class="sxs-lookup"><span data-stu-id="41891-173">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

<span data-ttu-id="41891-174">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-174">icm.h</span></span>

<span data-ttu-id="41891-175">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-175">mscms.lib</span></span>

[<span data-ttu-id="41891-176">**Wcssetdefaultcolorprofile**</span><span class="sxs-lookup"><span data-stu-id="41891-176">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

<span data-ttu-id="41891-177">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-177">icm.h</span></span>

<span data-ttu-id="41891-178">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-178">mscms.lib</span></span>

[<span data-ttu-id="41891-179">**Wcssetdefaultrenderingintent**</span><span class="sxs-lookup"><span data-stu-id="41891-179">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

<span data-ttu-id="41891-180">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-180">icm.h</span></span>

<span data-ttu-id="41891-181">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-181">mscms.lib</span></span>

[<span data-ttu-id="41891-182">**Wcssetuseperuserprofiles**</span><span class="sxs-lookup"><span data-stu-id="41891-182">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

<span data-ttu-id="41891-183">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-183">icm.h</span></span>

<span data-ttu-id="41891-184">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-184">mscms.lib</span></span>

[<span data-ttu-id="41891-185">**Wcstranslatecolors**</span><span class="sxs-lookup"><span data-stu-id="41891-185">**WcsTranslateColors**</span></span>](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

<span data-ttu-id="41891-186">ICM. h</span><span class="sxs-lookup"><span data-stu-id="41891-186">icm.h</span></span>

<span data-ttu-id="41891-187">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="41891-187">mscms.lib</span></span>



 



<span data-ttu-id="41891-188">Schnittstellen und ihre Funktionen</span><span class="sxs-lookup"><span data-stu-id="41891-188">Interfaces and Their Functions</span></span>

<span data-ttu-id="41891-189">API-Name</span><span class="sxs-lookup"><span data-stu-id="41891-189">API Name</span></span>

<span data-ttu-id="41891-190">Header</span><span class="sxs-lookup"><span data-stu-id="41891-190">Header</span></span>

<span data-ttu-id="41891-191">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="41891-191">Library</span></span>

[<span data-ttu-id="41891-192">**Idevicemodelplugin**</span><span class="sxs-lookup"><span data-stu-id="41891-192">**IDeviceModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

<span data-ttu-id="41891-193">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-193">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-194">–</span><span class="sxs-lookup"><span data-stu-id="41891-194">N/A</span></span>

[<span data-ttu-id="41891-195">**Idevicemodelplugin:: colormetrictodevicecolors**</span><span class="sxs-lookup"><span data-stu-id="41891-195">**IDeviceModelPlugin::ColorimetricToDeviceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

<span data-ttu-id="41891-196">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-196">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-197">–</span><span class="sxs-lookup"><span data-stu-id="41891-197">N/A</span></span>

[<span data-ttu-id="41891-198">**Idevicemodelplugin:: colormetrictodevicecolorswithblack**</span><span class="sxs-lookup"><span data-stu-id="41891-198">**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

<span data-ttu-id="41891-199">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-199">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-200">–</span><span class="sxs-lookup"><span data-stu-id="41891-200">N/A</span></span>

[<span data-ttu-id="41891-201">**Idevicemodelplugin::D evicetocolormetriccolors**</span><span class="sxs-lookup"><span data-stu-id="41891-201">**IDeviceModelPlugin::DeviceToColorimetricColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

<span data-ttu-id="41891-202">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-202">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-203">–</span><span class="sxs-lookup"><span data-stu-id="41891-203">N/A</span></span>

[<span data-ttu-id="41891-204">**Idevicemodelplugin:: getgamutboundarymesh**</span><span class="sxs-lookup"><span data-stu-id="41891-204">**IDeviceModelPlugin::GetGamutBoundaryMesh**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

<span data-ttu-id="41891-205">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-205">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-206">–</span><span class="sxs-lookup"><span data-stu-id="41891-206">N/A</span></span>

[<span data-ttu-id="41891-207">**Idevicemodelplugin:: getgamutboundarymeschsize**</span><span class="sxs-lookup"><span data-stu-id="41891-207">**IDeviceModelPlugin::GetGamutBoundaryMeshSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

<span data-ttu-id="41891-208">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-208">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-209">–</span><span class="sxs-lookup"><span data-stu-id="41891-209">N/A</span></span>

[<span data-ttu-id="41891-210">**Idevicemodelplugin:: getneutralaxis**</span><span class="sxs-lookup"><span data-stu-id="41891-210">**IDeviceModelPlugin::GetNeutralAxis**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

<span data-ttu-id="41891-211">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-211">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-212">–</span><span class="sxs-lookup"><span data-stu-id="41891-212">N/A</span></span>

[<span data-ttu-id="41891-213">**Idevicemodelplugin:: getneutralaxissize**</span><span class="sxs-lookup"><span data-stu-id="41891-213">**IDeviceModelPlugin::GetNeutralAxisSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

<span data-ttu-id="41891-214">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-214">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-215">–</span><span class="sxs-lookup"><span data-stu-id="41891-215">N/A</span></span>

[<span data-ttu-id="41891-216">**Idevicemodelplugin:: getnumchannels**</span><span class="sxs-lookup"><span data-stu-id="41891-216">**IDeviceModelPlugin::GetNumChannels**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

<span data-ttu-id="41891-217">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-217">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-218">–</span><span class="sxs-lookup"><span data-stu-id="41891-218">N/A</span></span>

[<span data-ttu-id="41891-219">**Idevicemodelplugin:: getprimarysamples**</span><span class="sxs-lookup"><span data-stu-id="41891-219">**IDeviceModelPlugin::GetPrimarySamples**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

<span data-ttu-id="41891-220">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-220">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-221">–</span><span class="sxs-lookup"><span data-stu-id="41891-221">N/A</span></span>

[<span data-ttu-id="41891-222">**Idevicemodelplugin:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="41891-222">**IDeviceModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

<span data-ttu-id="41891-223">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-223">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-224">–</span><span class="sxs-lookup"><span data-stu-id="41891-224">N/A</span></span>

[<span data-ttu-id="41891-225">**Idevicemodelplugin:: settransformdevicemodelinfo**</span><span class="sxs-lookup"><span data-stu-id="41891-225">**IDeviceModelPlugin::SetTransformDeviceModelInfo**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

<span data-ttu-id="41891-226">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-226">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-227">–</span><span class="sxs-lookup"><span data-stu-id="41891-227">N/A</span></span>

[<span data-ttu-id="41891-228">**Igamutmapmodelplugin**</span><span class="sxs-lookup"><span data-stu-id="41891-228">**IGamutMapModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

<span data-ttu-id="41891-229">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-229">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-230">–</span><span class="sxs-lookup"><span data-stu-id="41891-230">N/A</span></span>

[<span data-ttu-id="41891-231">**Igamutmapmodelplugin:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="41891-231">**IGamutMapModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

<span data-ttu-id="41891-232">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-232">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-233">–</span><span class="sxs-lookup"><span data-stu-id="41891-233">N/A</span></span>

[<span data-ttu-id="41891-234">**Igamutmapmodelplugin:: sourceesdestinationdestinancecolors**</span><span class="sxs-lookup"><span data-stu-id="41891-234">**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

<span data-ttu-id="41891-235">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-235">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-236">–</span><span class="sxs-lookup"><span data-stu-id="41891-236">N/A</span></span>



 



<span data-ttu-id="41891-237">Strukturen</span><span class="sxs-lookup"><span data-stu-id="41891-237">Structures</span></span>

<span data-ttu-id="41891-238">API-Name</span><span class="sxs-lookup"><span data-stu-id="41891-238">API Name</span></span>

<span data-ttu-id="41891-239">Header</span><span class="sxs-lookup"><span data-stu-id="41891-239">Header</span></span>

<span data-ttu-id="41891-240">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="41891-240">Library</span></span>

[<span data-ttu-id="41891-241">**Blackinformation**</span><span class="sxs-lookup"><span data-stu-id="41891-241">**BlackInformation**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

<span data-ttu-id="41891-242">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-242">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-243">–</span><span class="sxs-lookup"><span data-stu-id="41891-243">N/A</span></span>

[<span data-ttu-id="41891-244">**Gamutboundarydescription**</span><span class="sxs-lookup"><span data-stu-id="41891-244">**GamutBoundaryDescription**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

<span data-ttu-id="41891-245">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-245">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-246">–</span><span class="sxs-lookup"><span data-stu-id="41891-246">N/A</span></span>

[<span data-ttu-id="41891-247">**Xyzcolorf**</span><span class="sxs-lookup"><span data-stu-id="41891-247">**XYZColorF**</span></span>](https://www.bing.com/search?q=**XYZColorF**)

<span data-ttu-id="41891-248">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-248">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-249">–</span><span class="sxs-lookup"><span data-stu-id="41891-249">N/A</span></span>

[<span data-ttu-id="41891-250">**Jchcolorf**</span><span class="sxs-lookup"><span data-stu-id="41891-250">**JChColorF**</span></span>](https://www.bing.com/search?q=**JChColorF**)

<span data-ttu-id="41891-251">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-251">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-252">–</span><span class="sxs-lookup"><span data-stu-id="41891-252">N/A</span></span>

[<span data-ttu-id="41891-253">**Jabcolorf**</span><span class="sxs-lookup"><span data-stu-id="41891-253">**JabColorF**</span></span>](https://www.bing.com/search?q=**JabColorF**)

<span data-ttu-id="41891-254">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-254">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-255">–</span><span class="sxs-lookup"><span data-stu-id="41891-255">N/A</span></span>

[<span data-ttu-id="41891-256">**Gamutshell**</span><span class="sxs-lookup"><span data-stu-id="41891-256">**GamutShell**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

<span data-ttu-id="41891-257">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-257">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-258">–</span><span class="sxs-lookup"><span data-stu-id="41891-258">N/A</span></span>

[<span data-ttu-id="41891-259">**Gamutshelldreieck**</span><span class="sxs-lookup"><span data-stu-id="41891-259">**GamutShellTriangle**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

<span data-ttu-id="41891-260">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-260">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-261">–</span><span class="sxs-lookup"><span data-stu-id="41891-261">N/A</span></span>

[<span data-ttu-id="41891-262">**Primaryjabcolors**</span><span class="sxs-lookup"><span data-stu-id="41891-262">**PrimaryJabColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

<span data-ttu-id="41891-263">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-263">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-264">–</span><span class="sxs-lookup"><span data-stu-id="41891-264">N/A</span></span>

[<span data-ttu-id="41891-265">**Primaryxyzcolors**</span><span class="sxs-lookup"><span data-stu-id="41891-265">**PrimaryXYZColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

<span data-ttu-id="41891-266">Wcsplugin. h</span><span class="sxs-lookup"><span data-stu-id="41891-266">WcsPlugIn.h</span></span>

<span data-ttu-id="41891-267">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="41891-267">N/A</span></span>



 

 

 