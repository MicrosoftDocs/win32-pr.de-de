---
title: WCS-Registrierungsschlüssel
description: WCS verwendet Registrierungsschlüssel, um zu signalisieren, dass bestimmte Farbprofil Ereignisse aufgetreten sind. Apps sollten diese Registrierungsschlüssel für den aktualisierten Zustand des System Farbprofils Abfragen.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Color System (WCS), Registrierungsschlüssel
- WCS (Windows Color System), Registrierungsschlüssel
- Bild Farbverwaltung, Registrierungsschlüssel
- Farbverwaltung, Registrierungsschlüssel
- Farben, Registrierungsschlüssel
- WCS-Referenz, Registrierungsschlüssel
- Referenz für WCs, Registrierungsschlüssel
- Windows Color System (WCS), Registrierung
- WCS (Windows Color System), Registrierung
- Bild Farbverwaltung, Registrierung
- Farbverwaltung, Registrierung
- Farben, Registrierung
- WCS-Referenz, Registrierung
- Referenz für WCs, Registrierung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a1c0072d9a00fe0cff4a4dbe57af839f65731b
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106373403"
---
# <a name="wcs-registry-keys"></a><span data-ttu-id="b78f5-118">WCS-Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="b78f5-118">WCS Registry Keys</span></span>

<span data-ttu-id="b78f5-119">WCS verwendet Registrierungsschlüssel, um zu signalisieren, dass bestimmte Farbprofil Ereignisse aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="b78f5-119">WCS uses registry keys to signal that certain color profile events have occurred.</span></span> <span data-ttu-id="b78f5-120">Apps sollten diese Registrierungsschlüssel für den aktualisierten Zustand des System Farbprofils Abfragen.</span><span class="sxs-lookup"><span data-stu-id="b78f5-120">Apps should query these registry keys for updated system color profile state.</span></span>

## <a name="active-color-profile-changed"></a><span data-ttu-id="b78f5-121">Aktives Farbprofil geändert</span><span class="sxs-lookup"><span data-stu-id="b78f5-121">Active color profile changed</span></span>

<span data-ttu-id="b78f5-122">Apps können auf das Ändern von Farbprofilen für ein Überwachungsgerät reagieren. Dadurch wird sichergestellt, dass Sie immer über genaue Farbinformationen für Ihr Ziel verfügen, auch wenn der Benutzer oder eine andere APP das aktive Profil für das Gerät geändert hat.</span><span class="sxs-lookup"><span data-stu-id="b78f5-122">Apps may want to respond to color profile change events for a monitor device; this ensures that they always have accurate color information for their target, even if the user or another app has changed the active profile for the device.</span></span>

### <a name="desktop-applications"></a><span data-ttu-id="b78f5-123">Desktopanwendungen</span><span class="sxs-lookup"><span data-stu-id="b78f5-123">Desktop applications</span></span>

<span data-ttu-id="b78f5-124">Desktop-Apps sollten Änderungen an der Registrierung überwachen, um zu bestimmen, wann sich die Zuordnung von Farbprofil Zuordnungen mithilfe von [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue)geändert hat.</span><span class="sxs-lookup"><span data-stu-id="b78f5-124">Desktop apps should listen for changes to the registry to determine when a color profile associations has changed using [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span></span> <span data-ttu-id="b78f5-125">Eine APP sollte sich sowohl für Profil Zuordnungs Änderungen pro Benutzer als auch für systemweite Änderungen registrieren.</span><span class="sxs-lookup"><span data-stu-id="b78f5-125">An app should register both for per-user profile association changes, and for system-wide changes.</span></span>

<span data-ttu-id="b78f5-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) muss mit einem HKEY initialisiert werden, der von [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b78f5-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) should be initialized with an HKEY provided by [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span></span> <span data-ttu-id="b78f5-127">**RegOpenKeyEx** muss mithilfe der folgenden Registrierungs Struktur Speicherorte initialisiert werden:</span><span class="sxs-lookup"><span data-stu-id="b78f5-127">**RegOpenKeyEx** should be initialized using the following registry tree locations:</span></span>



|                                  |                                                                                                                                                    |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b78f5-128">Profil Zuordnungen pro Benutzer</span><span class="sxs-lookup"><span data-stu-id="b78f5-128">Per-user profile associations</span></span>    | <span data-ttu-id="b78f5-129">**HKEY \_ Current \_ User Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ICM \\ profileassociations \\ Display \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}**</span><span class="sxs-lookup"><span data-stu-id="b78f5-129">**HKEY\_CURRENT\_USER SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ProfileAssociations\\Display\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span> |
| <span data-ttu-id="b78f5-130">System weite Profil Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="b78f5-130">System-wide profile associations</span></span> | <span data-ttu-id="b78f5-131">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Class \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}**</span><span class="sxs-lookup"><span data-stu-id="b78f5-131">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Class\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span>                                        |



 

<span data-ttu-id="b78f5-132">Wenn die APP über eine Änderung des Registrierungsschlüssels benachrichtigt wird, sollte Sie zuerst Abfragen, ob Benutzer-oder systemweite Zuordnungen durch Aufrufen von [**wcsgetuseperuserprofiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b78f5-132">When the app is notified of a registry key change, it should first query whether per-user or system-wide associations are being used by calling [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span></span> <span data-ttu-id="b78f5-133">Dann sollte [**wcsgetdefaultcolorprofile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) mit dem richtigen Wert für den [**\_ \_ Verwaltungs \_ Bereich des WCS-Profils**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) aufgerufen werden, um das neue aktive Farbprofil für den Monitor zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b78f5-133">It should then call [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) with the right [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value to obtain the new active color profile for the monitor.</span></span> <span data-ttu-id="b78f5-134">Beachten Sie, dass nicht alle Änderungen des Registrierungsschlüssels einer tatsächlichen Änderung im momentan aktiven Farbprofil entsprechen. die APP Mush prüft, ob das von **wcsgetdefaultcolorprofile** zurückgegebene Profil tatsächlich geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="b78f5-134">Note that not all registry key changes will correspond to an actual change in the currently active color profile; the app mush check whether the profile returned by **WcsGetDefaultColorProfile** has actually changed.</span></span>

### <a name="universal-windows-uwp-apps"></a><span data-ttu-id="b78f5-135">Universelle Windows-Apps (UWP)</span><span class="sxs-lookup"><span data-stu-id="b78f5-135">Universal Windows (UWP) apps</span></span>

<span data-ttu-id="b78f5-136">Universelle Windows-apps haben keinen Zugriff auf die obigen Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="b78f5-136">Universal Windows Apps do not have access to the above registry keys.</span></span> <span data-ttu-id="b78f5-137">Stattdessen sollten Sie einen Handler für das [**Display Information. colorprofilechanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) -Ereignis registrieren.</span><span class="sxs-lookup"><span data-stu-id="b78f5-137">Instead, they should register a handler for the [**DisplayInformation.ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) event.</span></span> <span data-ttu-id="b78f5-138">Dieses Ereignis wird immer dann ausgelöst, wenn das aktive Farbprofil für den Monitor, auf dem die Anwendung ausgeführt wird, geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="b78f5-138">This event fires whenever the active color profile for the monitor on which the application is running has changed.</span></span> <span data-ttu-id="b78f5-139">Colorprofilechanged berücksichtigt, ob Benutzer-oder systemweite Profil Zuordnungen verwendet werden. Diese Informationen werden von UWP-apps abstrahiert.</span><span class="sxs-lookup"><span data-stu-id="b78f5-139">ColorProfileChanged takes into account whether per-user or system-wide profile associations are being used; this information is abstracted from UWP apps.</span></span>

<span data-ttu-id="b78f5-140">Wenn Sie auf das colorprofilechanged-Ereignis reagieren, sollte die APP das aktuell aktive Profil mithilfe von " [**Displayinformation. getcolorprofileasync**](/uwp/api/Windows.Graphics.Display.DisplayInformation)" Abfragen.</span><span class="sxs-lookup"><span data-stu-id="b78f5-140">When responding to the ColorProfileChanged event, the app should query the currently active profile using [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span></span>

 

 