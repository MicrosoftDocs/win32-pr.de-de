---
title: WCS-Registrierungsschlüssel
description: WCS verwendet Registrierungsschlüssel, um zu signalisieren, dass bestimmte Farbprofilereignisse aufgetreten sind. Apps sollten diese Registrierungsschlüssel auf den aktualisierten Zustand des Systemfarbprofils abfragen.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Color System (WCS), Registrierungsschlüssel
- WCS (Windows Color System), Registrierungsschlüssel
- Bildfarbverwaltung, Registrierungsschlüssel
- Farbverwaltung, Registrierungsschlüssel
- Farben, Registrierungsschlüssel
- WCS-Referenz, Registrierungsschlüssel
- Referenz für WCS, Registrierungsschlüssel
- Windows Color System (WCS),Registrierung
- WCS (Windows-Farbsystem),Registrierung
- Bildfarbverwaltung,Registrierung
- Farbverwaltung,Registrierung
- Farben, Registrierung
- WCS-Referenz,Registrierung
- Referenz für WCS, Registrierung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058ec839b226e96542604f151f06e2654a4180d5
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444671"
---
# <a name="wcs-registry-keys"></a><span data-ttu-id="ec6ca-118">WCS-Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="ec6ca-118">WCS Registry Keys</span></span>

<span data-ttu-id="ec6ca-119">WCS verwendet Registrierungsschlüssel, um zu signalisieren, dass bestimmte Farbprofilereignisse aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-119">WCS uses registry keys to signal that certain color profile events have occurred.</span></span> <span data-ttu-id="ec6ca-120">Apps sollten diese Registrierungsschlüssel auf den aktualisierten Zustand des Systemfarbprofils abfragen.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-120">Apps should query these registry keys for updated system color profile state.</span></span>

## <a name="active-color-profile-changed"></a><span data-ttu-id="ec6ca-121">Aktives Farbprofil geändert</span><span class="sxs-lookup"><span data-stu-id="ec6ca-121">Active color profile changed</span></span>

<span data-ttu-id="ec6ca-122">Apps möchten möglicherweise auf Farbprofiländerungsereignisse für ein Überwachungsgerät reagieren. Dadurch wird sichergestellt, dass sie immer über genaue Farbinformationen für ihr Ziel verfügen, auch wenn der Benutzer oder eine andere App das aktive Profil für das Gerät geändert hat.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-122">Apps may want to respond to color profile change events for a monitor device; this ensures that they always have accurate color information for their target, even if the user or another app has changed the active profile for the device.</span></span>

### <a name="desktop-applications"></a><span data-ttu-id="ec6ca-123">Desktopanwendungen</span><span class="sxs-lookup"><span data-stu-id="ec6ca-123">Desktop applications</span></span>

<span data-ttu-id="ec6ca-124">Desktop-Apps sollten mithilfe von [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue)auf Änderungen an der Registrierung lauschen, um zu bestimmen, wann sich eine Farbprofilzuordnung geändert hat.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-124">Desktop apps should listen for changes to the registry to determine when a color profile associations has changed using [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span></span> <span data-ttu-id="ec6ca-125">Eine App sollte sowohl für Benutzerprofilzuordnungsänderungen als auch für systemweite Änderungen registriert werden.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-125">An app should register both for per-user profile association changes, and for system-wide changes.</span></span>

<span data-ttu-id="ec6ca-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) sollte mit einem von [**RegOpenKeyEx bereitgestellten**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)HKEY initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) should be initialized with an HKEY provided by [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span></span> <span data-ttu-id="ec6ca-127">**RegOpenKeyEx** sollte mit den folgenden Registrierungsstrukturspeicherorten initialisiert werden:</span><span class="sxs-lookup"><span data-stu-id="ec6ca-127">**RegOpenKeyEx** should be initialized using the following registry tree locations:</span></span>



|    &nbsp;  |  &nbsp;      | 
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec6ca-128">Benutzerspezifische Profilzuordnungen</span><span class="sxs-lookup"><span data-stu-id="ec6ca-128">Per-user profile associations</span></span>    | <span data-ttu-id="ec6ca-129">**HKEY \_ CURRENT USER SOFTWARE Microsoft Windows NT \_ \\ \\ \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ Display \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**</span><span class="sxs-lookup"><span data-stu-id="ec6ca-129">**HKEY\_CURRENT\_USER SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ProfileAssociations\\Display\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span> |
| <span data-ttu-id="ec6ca-130">Systemweite Profilzuordnungen</span><span class="sxs-lookup"><span data-stu-id="ec6ca-130">System-wide profile associations</span></span> | <span data-ttu-id="ec6ca-131">**HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Class \\ \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**</span><span class="sxs-lookup"><span data-stu-id="ec6ca-131">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Class\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span>                                        |



 

<span data-ttu-id="ec6ca-132">Wenn die App über eine Änderung des Registrierungsschlüssels benachrichtigt wird, sollte sie zuerst abfragen, ob benutzer- oder systemweite Zuordnungen durch Aufrufen von [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-132">When the app is notified of a registry key change, it should first query whether per-user or system-wide associations are being used by calling [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span></span> <span data-ttu-id="ec6ca-133">Anschließend sollte [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) mit dem richtigen [**WCS \_ PROFILE MANAGEMENT \_ \_ SCOPE-Wert**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) aufgerufen werden, um das neue aktive Farbprofil für den Monitor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-133">It should then call [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) with the right [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value to obtain the new active color profile for the monitor.</span></span> <span data-ttu-id="ec6ca-134">Beachten Sie, dass nicht alle Änderungen des Registrierungsschlüssels einer tatsächlichen Änderung im derzeit aktiven Farbprofil entsprechen. Die App überprüft, ob sich das von **WcsGetDefaultColorProfile** zurückgegebene Profil tatsächlich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-134">Note that not all registry key changes will correspond to an actual change in the currently active color profile; the app mush check whether the profile returned by **WcsGetDefaultColorProfile** has actually changed.</span></span>

### <a name="universal-windows-uwp-apps"></a><span data-ttu-id="ec6ca-135">Universelle Windows-Apps (UWP)</span><span class="sxs-lookup"><span data-stu-id="ec6ca-135">Universal Windows (UWP) apps</span></span>

<span data-ttu-id="ec6ca-136">Universelle Windows-Apps haben keinen Zugriff auf die oben genannten Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-136">Universal Windows Apps do not have access to the above registry keys.</span></span> <span data-ttu-id="ec6ca-137">Stattdessen sollten sie einen Handler für das [**DisplayInformation.ColorProfileChanged-Ereignis**](/uwp/api/Windows.Graphics.Display.DisplayInformation) registrieren.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-137">Instead, they should register a handler for the [**DisplayInformation.ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) event.</span></span> <span data-ttu-id="ec6ca-138">Dieses Ereignis wird immer dann ausgelöst, wenn sich das aktive Farbprofil für den Monitor, auf dem die Anwendung ausgeführt wird, geändert hat.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-138">This event fires whenever the active color profile for the monitor on which the application is running has changed.</span></span> <span data-ttu-id="ec6ca-139">ColorProfileChanged berücksichtigt, ob benutzer- oder systemweite Profilzuordnungen verwendet werden. Diese Informationen werden von UWP-Apps abstrahiert.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-139">ColorProfileChanged takes into account whether per-user or system-wide profile associations are being used; this information is abstracted from UWP apps.</span></span>

<span data-ttu-id="ec6ca-140">Wenn sie auf das ColorProfileChanged-Ereignis reagiert, sollte die App das derzeit aktive Profil mit [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation)abfragen.</span><span class="sxs-lookup"><span data-stu-id="ec6ca-140">When responding to the ColorProfileChanged event, the app should query the currently active profile using [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span></span>

 

 