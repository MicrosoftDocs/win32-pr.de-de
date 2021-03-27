---
description: Ab Windows Vista erhalten in Windows enthaltene System Steuerungselemente einen kanonischen Namen, der in einem API-Befehl oder in einer Befehlszeilen Anweisung zum programmgesteuerten Starten dieses Elements verwendet werden kann.
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: Kanonische Namen von System Steuerungselementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55fc360b0d3db0f85a057977d1898c59d09d5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958773"
---
# <a name="canonical-names-of-control-panel-items"></a><span data-ttu-id="d15cf-103">Kanonische Namen von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="d15cf-103">Canonical Names of Control Panel Items</span></span>

<span data-ttu-id="d15cf-104">Ab Windows Vista erhalten in Windows enthaltene System Steuerungselemente einen kanonischen Namen, der in einem [API-Befehl oder in einer Befehlszeilen Anweisung](executing-control-panel-items.md) zum programmgesteuerten Starten dieses Elements verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d15cf-104">As of Windows Vista, Control Panel items included with Windows are given a canonical name that can be used in an [API call or a command-line instruction](executing-control-panel-items.md) to programmatically launch that item.</span></span> <span data-ttu-id="d15cf-105">Ab Windows 7 und Windows Server 2008 R2 können kanonische Namen in einer Gruppenrichtlinie verwendet werden, um bestimmte System Steuerungselemente auszublenden.</span><span class="sxs-lookup"><span data-stu-id="d15cf-105">As of Windows 7 and Windows Server 2008 R2, canonical names can be used in a group policy to hide specific Control Panel items.</span></span> <span data-ttu-id="d15cf-106">Dieses Thema enthält Details zu den einzelnen System Steuerungselementen: kanonischer Name, Guid, Modulname und Betriebssystemversionen, die den kanonischen Namen erkennen.</span><span class="sxs-lookup"><span data-stu-id="d15cf-106">This topic provides details for each Control Panel item: canonical name, GUID, module name, and the operating system versions that recognize the canonical name.</span></span>

> [!Note]  
> <span data-ttu-id="d15cf-107">Kanonische Namen für System Steuerungselemente werden vor Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d15cf-107">Canonical names for Control Panel items are not supported prior to Windows Vista.</span></span>

 

-   [<span data-ttu-id="d15cf-108">Kanonische Namen der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="d15cf-108">Control Panel Canonical Names</span></span>](#control-panel-canonical-names)
-   [<span data-ttu-id="d15cf-109">Als veraltet markierte kanonische Name der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="d15cf-109">Deprecated Control Panel Canonical Names</span></span>](#deprecated-control-panel-canonical-names)
-   [<span data-ttu-id="d15cf-110">Verwenden von kanonischen Namen in Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d15cf-110">Using Canonical Names in Group Policy</span></span>](#using-canonical-names-in-local-group-policy)
-   [<span data-ttu-id="d15cf-111">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-111">Remarks</span></span>](#remarks)

## <a name="control-panel-canonical-names"></a><span data-ttu-id="d15cf-112">Kanonische Namen der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="d15cf-112">Control Panel Canonical Names</span></span>

<span data-ttu-id="d15cf-113">Beachten Sie beim Arbeiten mit diesen Werten Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d15cf-113">Points to remember when working with these values:</span></span>

-   <span data-ttu-id="d15cf-114">In der Definition werden kanonische Namen nicht auf der Grundlage der Systemsprache geändert. Sie sind immer in englischer Sprache, auch wenn die Sprache des Systems nicht ist.</span><span class="sxs-lookup"><span data-stu-id="d15cf-114">By definition, canonical names do not change based on the system language; they're always in English, even if the system's language is not.</span></span>
-   <span data-ttu-id="d15cf-115">Nicht alle System Steuerungselemente sind in allen Arten von Fenstern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d15cf-115">Not all Control Panel items are present in all varieties of Windows.</span></span>
-   <span data-ttu-id="d15cf-116">Einige System Steuerungselemente werden nur angezeigt, wenn auf dem System die richtige Hardware erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="d15cf-116">Some Control Panel items only appear if the right hardware is detected on the system.</span></span>
-   <span data-ttu-id="d15cf-117">Drittanbieter können auch System Steuerungselemente hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d15cf-117">Third parties can also add Control Panel items.</span></span> <span data-ttu-id="d15cf-118">Die hier aufgeführten kanonischen Namen gelten nur für System Steuerungselemente, die in Windows enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d15cf-118">The canonical names listed here are only for Control Panel items that are included with Windows.</span></span>

<span data-ttu-id="d15cf-119">Im folgenden finden Sie die System Steuerungselemente, die in Windows 8.1 verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="d15cf-119">The following are the Control Panel items available in Windows 8.1:</span></span>

-   [<span data-ttu-id="d15cf-120">Info-Center</span><span class="sxs-lookup"><span data-stu-id="d15cf-120">Action Center</span></span>](#action-center)
-   [<span data-ttu-id="d15cf-121">Verwaltungs Tools</span><span class="sxs-lookup"><span data-stu-id="d15cf-121">Administrative Tools</span></span>](#administrative-tools)
-   [<span data-ttu-id="d15cf-122">Automatische Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="d15cf-122">AutoPlay</span></span>](#autoplay)
-   [<span data-ttu-id="d15cf-123">Biometrische Geräte</span><span class="sxs-lookup"><span data-stu-id="d15cf-123">Biometric Devices</span></span>](#biometric-devices)
-   [<span data-ttu-id="d15cf-124">BitLocker-Laufwerkverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="d15cf-124">BitLocker Drive Encryption</span></span>](#bitlocker-drive-encryption)
-   [<span data-ttu-id="d15cf-125">Farbverwaltung</span><span class="sxs-lookup"><span data-stu-id="d15cf-125">Color Management</span></span>](#color-management)
-   [<span data-ttu-id="d15cf-126">Anmeldeinformationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="d15cf-126">Credential Manager</span></span>](#credential-manager)
-   [<span data-ttu-id="d15cf-127">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="d15cf-127">Date and Time</span></span>](#date-and-time)
-   [<span data-ttu-id="d15cf-128">Standardprogramme</span><span class="sxs-lookup"><span data-stu-id="d15cf-128">Default Programs</span></span>](#default-programs)
-   [<span data-ttu-id="d15cf-129">Geräte-Manager</span><span class="sxs-lookup"><span data-stu-id="d15cf-129">Device Manager</span></span>](#device-manager)
-   [<span data-ttu-id="d15cf-130">Geräte und Drucker</span><span class="sxs-lookup"><span data-stu-id="d15cf-130">Devices and Printers</span></span>](#devices-and-printers)
-   [<span data-ttu-id="d15cf-131">Anzeige</span><span class="sxs-lookup"><span data-stu-id="d15cf-131">Display</span></span>](#display)
-   [<span data-ttu-id="d15cf-132">Center für erleichterte Bedienung</span><span class="sxs-lookup"><span data-stu-id="d15cf-132">Ease of Access Center</span></span>](#ease-of-access-center)
-   [<span data-ttu-id="d15cf-133">Family Safety</span><span class="sxs-lookup"><span data-stu-id="d15cf-133">Family Safety</span></span>](#family-safety)
-   [<span data-ttu-id="d15cf-134">Dateiversionsverlauf</span><span class="sxs-lookup"><span data-stu-id="d15cf-134">File History</span></span>](#file-history)
-   [<span data-ttu-id="d15cf-135">Ordneroptionen</span><span class="sxs-lookup"><span data-stu-id="d15cf-135">Folder Options</span></span>](#folder-options)
-   [<span data-ttu-id="d15cf-136">Schriftarten</span><span class="sxs-lookup"><span data-stu-id="d15cf-136">Fonts</span></span>](#fonts)
-   [<span data-ttu-id="d15cf-137">Heimnetzgruppe</span><span class="sxs-lookup"><span data-stu-id="d15cf-137">HomeGroup</span></span>](#homegroup)
-   [<span data-ttu-id="d15cf-138">Indizierungs Optionen</span><span class="sxs-lookup"><span data-stu-id="d15cf-138">Indexing Options</span></span>](#indexing-options)
-   [<span data-ttu-id="d15cf-139">Infrarot</span><span class="sxs-lookup"><span data-stu-id="d15cf-139">Infrared</span></span>](#infrared)
-   [<span data-ttu-id="d15cf-140">Internetoptionen</span><span class="sxs-lookup"><span data-stu-id="d15cf-140">Internet Options</span></span>](#internet-options)
-   [<span data-ttu-id="d15cf-141">iSCSI-Initiator</span><span class="sxs-lookup"><span data-stu-id="d15cf-141">iSCSI Initiator</span></span>](#iscsi-initiator)
-   [<span data-ttu-id="d15cf-142">iSNS-Server</span><span class="sxs-lookup"><span data-stu-id="d15cf-142">iSNS Server</span></span>](#isns-server)
-   [<span data-ttu-id="d15cf-143">Tastatur</span><span class="sxs-lookup"><span data-stu-id="d15cf-143">Keyboard</span></span>](#keyboard)
-   [<span data-ttu-id="d15cf-144">Standorteinstellungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-144">Location Settings</span></span>](#location-settings)
-   [<span data-ttu-id="d15cf-145">Maus</span><span class="sxs-lookup"><span data-stu-id="d15cf-145">Mouse</span></span>](#mouse)
-   [<span data-ttu-id="d15cf-146">Mpioconfiguration</span><span class="sxs-lookup"><span data-stu-id="d15cf-146">MPIOConfiguration</span></span>](#mpioconfiguration)
-   [<span data-ttu-id="d15cf-147">Netzwerk- und Freigabecenter</span><span class="sxs-lookup"><span data-stu-id="d15cf-147">Network and Sharing Center</span></span>](#network-and-sharing-center)
-   [<span data-ttu-id="d15cf-148">Benachrichtigungs Bereichs Symbole</span><span class="sxs-lookup"><span data-stu-id="d15cf-148">Notification Area Icons</span></span>](#notification-area-icons)
-   [<span data-ttu-id="d15cf-149">Stift und berühren</span><span class="sxs-lookup"><span data-stu-id="d15cf-149">Pen and Touch</span></span>](#pen-and-touch)
-   [<span data-ttu-id="d15cf-150">Personalisierung</span><span class="sxs-lookup"><span data-stu-id="d15cf-150">Personalization</span></span>](#personalization)
-   [<span data-ttu-id="d15cf-151">Telefon und Modem</span><span class="sxs-lookup"><span data-stu-id="d15cf-151">Phone and Modem</span></span>](#phone-and-modem)
-   [<span data-ttu-id="d15cf-152">Energieoptionen</span><span class="sxs-lookup"><span data-stu-id="d15cf-152">Power Options</span></span>](#power-options)
-   [<span data-ttu-id="d15cf-153">Programme und Funktionen</span><span class="sxs-lookup"><span data-stu-id="d15cf-153">Programs and Features</span></span>](#programs-and-features)
-   [<span data-ttu-id="d15cf-154">Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="d15cf-154">Recovery</span></span>](#recovery)
-   [<span data-ttu-id="d15cf-155">Region</span><span class="sxs-lookup"><span data-stu-id="d15cf-155">Region</span></span>](#region)
-   [<span data-ttu-id="d15cf-156">RemoteApp- und Desktopverbindungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-156">RemoteApp and Desktop Connections</span></span>](#remoteapp-and-desktop-connections)
-   [<span data-ttu-id="d15cf-157">Sound</span><span class="sxs-lookup"><span data-stu-id="d15cf-157">Sound</span></span>](#sound)
-   [<span data-ttu-id="d15cf-158">Spracherkennung</span><span class="sxs-lookup"><span data-stu-id="d15cf-158">Speech Recognition</span></span>](#speech-recognition)
-   [<span data-ttu-id="d15cf-159">Speicherplätze</span><span class="sxs-lookup"><span data-stu-id="d15cf-159">Storage Spaces</span></span>](#storage-spaces)
-   [<span data-ttu-id="d15cf-160">Synchronisierungscenter</span><span class="sxs-lookup"><span data-stu-id="d15cf-160">Sync Center</span></span>](#sync-center)
-   [<span data-ttu-id="d15cf-161">System</span><span class="sxs-lookup"><span data-stu-id="d15cf-161">System</span></span>](#system)
-   [<span data-ttu-id="d15cf-162">Tablet PC-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-162">Tablet PC Settings</span></span>](#tablet-pc-settings)
-   [<span data-ttu-id="d15cf-163">Taskleiste und Navigation</span><span class="sxs-lookup"><span data-stu-id="d15cf-163">Taskbar and Navigation</span></span>](#taskbar-and-navigation)
-   [<span data-ttu-id="d15cf-164">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="d15cf-164">Troubleshooting</span></span>](#troubleshooting)
-   [<span data-ttu-id="d15cf-165">"T AppInstall"</span><span class="sxs-lookup"><span data-stu-id="d15cf-165">TSAppInstall</span></span>](#tsappinstall)
-   [<span data-ttu-id="d15cf-166">User Accounts (Benutzerkonten)</span><span class="sxs-lookup"><span data-stu-id="d15cf-166">User Accounts</span></span>](#user-accounts)
-   [<span data-ttu-id="d15cf-167">Windows Anytime Upgrade</span><span class="sxs-lookup"><span data-stu-id="d15cf-167">Windows Anytime Upgrade</span></span>](#windows-anytime-upgrade)
-   [<span data-ttu-id="d15cf-168">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="d15cf-168">Windows Defender</span></span>](#windows-defender)
-   [<span data-ttu-id="d15cf-169">Windows-Firewall</span><span class="sxs-lookup"><span data-stu-id="d15cf-169">Windows Firewall</span></span>](#windows-firewall)
-   [<span data-ttu-id="d15cf-170">Windows-Mobilitätscenter</span><span class="sxs-lookup"><span data-stu-id="d15cf-170">Windows Mobility Center</span></span>](#windows-mobility-center)
-   [<span data-ttu-id="d15cf-171">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="d15cf-171">Windows To Go</span></span>](#windows-to-go)
-   [<span data-ttu-id="d15cf-172">Windows Update</span><span class="sxs-lookup"><span data-stu-id="d15cf-172">Windows Update</span></span>](#windows-update)
-   [<span data-ttu-id="d15cf-173">Arbeitsordner</span><span class="sxs-lookup"><span data-stu-id="d15cf-173">Work Folders</span></span>](#work-folders)

### <a name="action-center"></a><span data-ttu-id="d15cf-174">Info-Center</span><span class="sxs-lookup"><span data-stu-id="d15cf-174">Action Center</span></span>

-   <span data-ttu-id="d15cf-175">**Kanonischer Name**: Microsoft. Aktions Center</span><span class="sxs-lookup"><span data-stu-id="d15cf-175">**Canonical name**: Microsoft.ActionCenter</span></span>
-   <span data-ttu-id="d15cf-176">**GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span><span class="sxs-lookup"><span data-stu-id="d15cf-176">**GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span></span>
-   <span data-ttu-id="d15cf-177">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-177">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-178">**Modulname**: @% systemroot% \\ system32 \\ActionCenterCPL.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-178">**Module name**: @%SystemRoot%\\System32\\ActionCenterCPL.dll,-1</span></span>
-   <span data-ttu-id="d15cf-179">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-179">**Pages**</span></span>

    | <span data-ttu-id="d15cf-180">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-180">Page Name</span></span>           | <span data-ttu-id="d15cf-181">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-181">Opens</span></span>                      |
    |---------------------|----------------------------|
    | <span data-ttu-id="d15cf-182">Maintenancesettings</span><span class="sxs-lookup"><span data-stu-id="d15cf-182">MaintenanceSettings</span></span> | <span data-ttu-id="d15cf-183">Automatische Wartung</span><span class="sxs-lookup"><span data-stu-id="d15cf-183">Automatic Maintenance</span></span>      |
    | <span data-ttu-id="d15cf-184">pageproblems</span><span class="sxs-lookup"><span data-stu-id="d15cf-184">pageProblems</span></span>        | <span data-ttu-id="d15cf-185">Problemberichte</span><span class="sxs-lookup"><span data-stu-id="d15cf-185">Problem Reports</span></span>            |
    | <span data-ttu-id="d15cf-186">pageReliabilityView</span><span class="sxs-lookup"><span data-stu-id="d15cf-186">pageReliabilityView</span></span> | <span data-ttu-id="d15cf-187">Zuverlässigkeits Monitor</span><span class="sxs-lookup"><span data-stu-id="d15cf-187">Reliability Monitor</span></span>        |
    | <span data-ttu-id="d15cf-188">pageResponseArchive</span><span class="sxs-lookup"><span data-stu-id="d15cf-188">pageResponseArchive</span></span> | <span data-ttu-id="d15cf-189">Archivierte Nachrichten</span><span class="sxs-lookup"><span data-stu-id="d15cf-189">Archived Messages</span></span>          |
    | <span data-ttu-id="d15cf-190">pgesettings</span><span class="sxs-lookup"><span data-stu-id="d15cf-190">pageSettings</span></span>        | <span data-ttu-id="d15cf-191">Problem Berichterstattungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-191">Problem Reporting Settings</span></span> |

    

     

### <a name="administrative-tools"></a><span data-ttu-id="d15cf-192">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d15cf-192">Administrative Tools</span></span>

-   <span data-ttu-id="d15cf-193">**Kanonischer Name**: Microsoft. AdministrativeTools</span><span class="sxs-lookup"><span data-stu-id="d15cf-193">**Canonical name**: Microsoft.AdministrativeTools</span></span>
-   <span data-ttu-id="d15cf-194">**GUID**: {D20EA4E1-3957-11d2-A40B-0C5020524153}</span><span class="sxs-lookup"><span data-stu-id="d15cf-194">**GUID**: {D20EA4E1-3957-11d2-A40B-0C5020524153}</span></span>
-   <span data-ttu-id="d15cf-195">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-195">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-196">**Modulname**: @% systemroot% \\ system32 \\shell32.dll,-22982</span><span class="sxs-lookup"><span data-stu-id="d15cf-196">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22982</span></span>

### <a name="autoplay"></a><span data-ttu-id="d15cf-197">Automatische Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="d15cf-197">AutoPlay</span></span>

-   <span data-ttu-id="d15cf-198">**Kanonischer Name**: Microsoft. AutoPlay</span><span class="sxs-lookup"><span data-stu-id="d15cf-198">**Canonical name**: Microsoft.AutoPlay</span></span>
-   <span data-ttu-id="d15cf-199">**GUID**: {9c60de1e-e5fc-40b4-a487-460851a8d915}</span><span class="sxs-lookup"><span data-stu-id="d15cf-199">**GUID**: {9C60DE1E-E5FC-40f4-A487-460851A8D915}</span></span>
-   <span data-ttu-id="d15cf-200">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-200">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-201">**Modulname**: @% systemroot% \\ system32 \\autoplay.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-201">**Module name**: @%SystemRoot%\\System32\\autoplay.dll,-1</span></span>

### <a name="biometric-devices"></a><span data-ttu-id="d15cf-202">Biometrische Geräte</span><span class="sxs-lookup"><span data-stu-id="d15cf-202">Biometric Devices</span></span>

-   <span data-ttu-id="d15cf-203">**Kanonischer Name**: Microsoft. biometricdevices</span><span class="sxs-lookup"><span data-stu-id="d15cf-203">**Canonical name**: Microsoft.BiometricDevices</span></span>
-   <span data-ttu-id="d15cf-204">**GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span><span class="sxs-lookup"><span data-stu-id="d15cf-204">**GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span></span>
-   <span data-ttu-id="d15cf-205">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-205">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-206">**Modulname**: @% systemroot% \\ system32 \\biocpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-206">**Module name**: @%SystemRoot%\\System32\\biocpl.dll,-1</span></span>

### <a name="bitlocker-drive-encryption"></a><span data-ttu-id="d15cf-207">BitLocker-Laufwerkverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="d15cf-207">BitLocker Drive Encryption</span></span>

-   <span data-ttu-id="d15cf-208">**Kanonischer Name**: Microsoft. bitlockerdriveencryption</span><span class="sxs-lookup"><span data-stu-id="d15cf-208">**Canonical name**: Microsoft.BitLockerDriveEncryption</span></span>
-   <span data-ttu-id="d15cf-209">**GUID**: {D9EF8727-CAC2-4e60-809E-86F80A666C91}</span><span class="sxs-lookup"><span data-stu-id="d15cf-209">**GUID**: {D9EF8727-CAC2-4e60-809E-86F80A666C91}</span></span>
-   <span data-ttu-id="d15cf-210">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-210">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-211">**Modulname**: @% systemroot% \\ system32 \\fvecpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-211">**Module name**: @%SystemRoot%\\System32\\fvecpl.dll,-1</span></span>

### <a name="color-management"></a><span data-ttu-id="d15cf-212">Farbverwaltung</span><span class="sxs-lookup"><span data-stu-id="d15cf-212">Color Management</span></span>

-   <span data-ttu-id="d15cf-213">**Kanonischer Name**: Microsoft. Colormanagement</span><span class="sxs-lookup"><span data-stu-id="d15cf-213">**Canonical name**: Microsoft.ColorManagement</span></span>
-   <span data-ttu-id="d15cf-214">**GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}</span><span class="sxs-lookup"><span data-stu-id="d15cf-214">**GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}</span></span>
-   <span data-ttu-id="d15cf-215">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-215">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-216">**Modulname**: @% systemroot% \\ system32 \\colorcpl.exe,-6</span><span class="sxs-lookup"><span data-stu-id="d15cf-216">**Module name**: @%systemroot%\\system32\\colorcpl.exe,-6</span></span>

### <a name="credential-manager"></a><span data-ttu-id="d15cf-217">Anmeldeinformationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="d15cf-217">Credential Manager</span></span>

-   <span data-ttu-id="d15cf-218">**Kanonischer Name**: Microsoft. kredentialmanager</span><span class="sxs-lookup"><span data-stu-id="d15cf-218">**Canonical name**: Microsoft.CredentialManager</span></span>
-   <span data-ttu-id="d15cf-219">**GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}</span><span class="sxs-lookup"><span data-stu-id="d15cf-219">**GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}</span></span>
-   <span data-ttu-id="d15cf-220">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-220">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-221">**Modulname**: @% systemroot% \\ system32 \\Vault.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-221">**Module name**: @%SystemRoot%\\system32\\Vault.dll,-1</span></span>
-   <span data-ttu-id="d15cf-222">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-222">**Pages**</span></span>

    | <span data-ttu-id="d15cf-223">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-223">Page Name</span></span>                   | <span data-ttu-id="d15cf-224">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-224">Opens</span></span>               |
    |-----------------------------|---------------------|
    | <span data-ttu-id="d15cf-225">? Selectedvault = "kredmanvault"</span><span class="sxs-lookup"><span data-stu-id="d15cf-225">?SelectedVault=CredmanVault</span></span> | <span data-ttu-id="d15cf-226">Windows-Anmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="d15cf-226">Windows Credentials</span></span> |

    

     

### <a name="date-and-time"></a><span data-ttu-id="d15cf-227">Datum und Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="d15cf-227">Date and Time</span></span>

-   <span data-ttu-id="d15cf-228">**Kanonischer Name**: Microsoft. DateAndTime</span><span class="sxs-lookup"><span data-stu-id="d15cf-228">**Canonical name**: Microsoft.DateAndTime</span></span>
-   <span data-ttu-id="d15cf-229">**GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}</span><span class="sxs-lookup"><span data-stu-id="d15cf-229">**GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}</span></span>
-   <span data-ttu-id="d15cf-230">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-230">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-231">**Modulname**: @% systemroot% \\ system32 \\timedate.cpl,-51</span><span class="sxs-lookup"><span data-stu-id="d15cf-231">**Module name**: @%SystemRoot%\\System32\\timedate.cpl,-51</span></span>
-   <span data-ttu-id="d15cf-232">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-232">**Pages**</span></span>

    | <span data-ttu-id="d15cf-233">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-233">Page Name</span></span> | <span data-ttu-id="d15cf-234">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-234">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="d15cf-235">1</span><span class="sxs-lookup"><span data-stu-id="d15cf-235">1</span></span>         | <span data-ttu-id="d15cf-236">Weitere Uhren</span><span class="sxs-lookup"><span data-stu-id="d15cf-236">Additional Clocks</span></span> |

    

     

### <a name="default-programs"></a><span data-ttu-id="d15cf-237">Standardprogramme</span><span class="sxs-lookup"><span data-stu-id="d15cf-237">Default Programs</span></span>

-   <span data-ttu-id="d15cf-238">**Kanonischer Name**: Microsoft. defaultprograms</span><span class="sxs-lookup"><span data-stu-id="d15cf-238">**Canonical name**: Microsoft.DefaultPrograms</span></span>
-   <span data-ttu-id="d15cf-239">**GUID**: {17cd9488-1228-4b2f -88ce-4298e93e0966}</span><span class="sxs-lookup"><span data-stu-id="d15cf-239">**GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}</span></span>
-   <span data-ttu-id="d15cf-240">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-240">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-241">**Modulname**: @% systemroot% \\ system32 \\sud.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-241">**Module name**: @%SystemRoot%\\System32\\sud.dll,-1</span></span>
-   <span data-ttu-id="d15cf-242">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-242">**Pages**</span></span>

    | <span data-ttu-id="d15cf-243">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-243">Page Name</span></span>          | <span data-ttu-id="d15cf-244">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-244">Opens</span></span>                |
    |--------------------|----------------------|
    | <span data-ttu-id="d15cf-245">pagedefaultprogram</span><span class="sxs-lookup"><span data-stu-id="d15cf-245">pageDefaultProgram</span></span> | <span data-ttu-id="d15cf-246">Standardprogramme festlegen</span><span class="sxs-lookup"><span data-stu-id="d15cf-246">Set Default Programs</span></span> |
    | <span data-ttu-id="d15cf-247">pagefileassoc</span><span class="sxs-lookup"><span data-stu-id="d15cf-247">pageFileAssoc</span></span>      | <span data-ttu-id="d15cf-248">Zuordnungen festlegen</span><span class="sxs-lookup"><span data-stu-id="d15cf-248">Set Associations</span></span>     |

    

     

### <a name="device-manager"></a><span data-ttu-id="d15cf-249">Geräte-Manager</span><span class="sxs-lookup"><span data-stu-id="d15cf-249">Device Manager</span></span>

-   <span data-ttu-id="d15cf-250">**Kanonischer Name**: Microsoft. Debug Manager</span><span class="sxs-lookup"><span data-stu-id="d15cf-250">**Canonical name**: Microsoft.DeviceManager</span></span>
-   <span data-ttu-id="d15cf-251">**GUID**: {74246bfc-4c96-11D0-ABEF -0020af6b0b7a}</span><span class="sxs-lookup"><span data-stu-id="d15cf-251">**GUID**: {74246bfc-4c96-11d0-abef-0020af6b0b7a}</span></span>
-   <span data-ttu-id="d15cf-252">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-252">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-253">**Modulname**: @% systemroot% \\ system32 \\devmgr.dll,-4</span><span class="sxs-lookup"><span data-stu-id="d15cf-253">**Module name**: @%SystemRoot%\\System32\\devmgr.dll,-4</span></span>

### <a name="devices-and-printers"></a><span data-ttu-id="d15cf-254">Geräte und Drucker</span><span class="sxs-lookup"><span data-stu-id="d15cf-254">Devices and Printers</span></span>

-   <span data-ttu-id="d15cf-255">**Kanonischer Name**: Microsoft. Geräte Handler</span><span class="sxs-lookup"><span data-stu-id="d15cf-255">**Canonical name**: Microsoft.DevicesAndPrinters</span></span>
-   <span data-ttu-id="d15cf-256">**GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span><span class="sxs-lookup"><span data-stu-id="d15cf-256">**GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span></span>
-   <span data-ttu-id="d15cf-257">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-257">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-258">**Modulname**: @% systemroot% \\ system32 \\DeviceCenter.dll,-1000</span><span class="sxs-lookup"><span data-stu-id="d15cf-258">**Module name**: @%systemroot%\\system32\\DeviceCenter.dll,-1000</span></span>

### <a name="display"></a><span data-ttu-id="d15cf-259">Anzeige</span><span class="sxs-lookup"><span data-stu-id="d15cf-259">Display</span></span>

-   <span data-ttu-id="d15cf-260">**Kanonischer Name**: Microsoft. Display</span><span class="sxs-lookup"><span data-stu-id="d15cf-260">**Canonical name**: Microsoft.Display</span></span>
-   <span data-ttu-id="d15cf-261">**GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span><span class="sxs-lookup"><span data-stu-id="d15cf-261">**GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span></span>
-   <span data-ttu-id="d15cf-262">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-262">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-263">**Modulname**: @% systemroot% \\ system32 \\Display.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-263">**Module name**: @%SystemRoot%\\System32\\Display.dll,-1</span></span>
-   <span data-ttu-id="d15cf-264">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-264">**Pages**</span></span>

    | <span data-ttu-id="d15cf-265">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-265">Page Name</span></span> | <span data-ttu-id="d15cf-266">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-266">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="d15cf-267">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-267">Settings</span></span>  | <span data-ttu-id="d15cf-268">Bildschirmauflösung</span><span class="sxs-lookup"><span data-stu-id="d15cf-268">Screen Resolution</span></span> |

    

     

### <a name="ease-of-access-center"></a><span data-ttu-id="d15cf-269">Center für erleichterte Bedienung</span><span class="sxs-lookup"><span data-stu-id="d15cf-269">Ease of Access Center</span></span>

-   <span data-ttu-id="d15cf-270">**Kanonischer Name**: Microsoft. easeofakcescenters</span><span class="sxs-lookup"><span data-stu-id="d15cf-270">**Canonical name**: Microsoft.EaseOfAccessCenter</span></span>
-   <span data-ttu-id="d15cf-271">**GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span><span class="sxs-lookup"><span data-stu-id="d15cf-271">**GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span></span>
-   <span data-ttu-id="d15cf-272">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-272">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-273">**Modulname**: @% systemroot% \\ system32 \\accessibilitycpl.dll,-10</span><span class="sxs-lookup"><span data-stu-id="d15cf-273">**Module name**: @%SystemRoot%\\System32\\accessibilitycpl.dll,-10</span></span>
-   <span data-ttu-id="d15cf-274">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-274">**Pages**</span></span>

    | <span data-ttu-id="d15cf-275">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-275">Page Name</span></span>               | <span data-ttu-id="d15cf-276">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-276">Opens</span></span>                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | <span data-ttu-id="d15cf-277">pageeasierper Click</span><span class="sxs-lookup"><span data-stu-id="d15cf-277">pageEasierToClick</span></span>       | <span data-ttu-id="d15cf-278">Vereinfachen Sie die Verwendung der Maus</span><span class="sxs-lookup"><span data-stu-id="d15cf-278">Make the mouse easier to use</span></span>                                        |
    | <span data-ttu-id="d15cf-279">pageeasiergesee</span><span class="sxs-lookup"><span data-stu-id="d15cf-279">pageEasierToSee</span></span>         | <span data-ttu-id="d15cf-280">Machen Sie den Computer leichter zu erkennen</span><span class="sxs-lookup"><span data-stu-id="d15cf-280">Make the computer easier to see</span></span>                                     |
    | <span data-ttu-id="d15cf-281">pageeasierwithsounds</span><span class="sxs-lookup"><span data-stu-id="d15cf-281">pageEasierWithSounds</span></span>    | <span data-ttu-id="d15cf-282">Verwenden von Text oder visuellen Alternativen für Sounds</span><span class="sxs-lookup"><span data-stu-id="d15cf-282">Use text or visual alternatives for sounds</span></span>                          |
    | <span data-ttu-id="d15cf-283">"pgefilterkeyssettings"</span><span class="sxs-lookup"><span data-stu-id="d15cf-283">pageFilterKeysSettings</span></span>  | <span data-ttu-id="d15cf-284">Einrichten von Filter Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="d15cf-284">Set up Filter Keys</span></span>                                                  |
    | <span data-ttu-id="d15cf-285">pagekeyboardebug</span><span class="sxs-lookup"><span data-stu-id="d15cf-285">pageKeyboardEasierToUse</span></span> | <span data-ttu-id="d15cf-286">Vereinfachen der Verwendung der Tastatur</span><span class="sxs-lookup"><span data-stu-id="d15cf-286">Make the keyboard easier to use</span></span>                                     |
    | <span data-ttu-id="d15cf-287">pagenomouonorkeyboard</span><span class="sxs-lookup"><span data-stu-id="d15cf-287">pageNoMouseOrKeyboard</span></span>   | <span data-ttu-id="d15cf-288">Computer ohne Maus oder Tastatur verwenden</span><span class="sxs-lookup"><span data-stu-id="d15cf-288">Use the computer without a mouse or keyboard</span></span>                        |
    | <span data-ttu-id="d15cf-289">pagenovisual</span><span class="sxs-lookup"><span data-stu-id="d15cf-289">pageNoVisual</span></span>            | <span data-ttu-id="d15cf-290">Verwenden des Computers ohne Anzeige</span><span class="sxs-lookup"><span data-stu-id="d15cf-290">Use the computer without a display</span></span>                                  |
    | <span data-ttu-id="d15cf-291">pagefrag scognitive</span><span class="sxs-lookup"><span data-stu-id="d15cf-291">pageQuestionsCognitive</span></span>  | <span data-ttu-id="d15cf-292">Empfehlungen zur einfacheren Verwendung Ihres Computers erhalten (Cognitive)</span><span class="sxs-lookup"><span data-stu-id="d15cf-292">Get recommendations to make your computer easier to use (cognitive)</span></span> |
    | <span data-ttu-id="d15cf-293">pagefrag \ yesight</span><span class="sxs-lookup"><span data-stu-id="d15cf-293">pageQuestionsEyesight</span></span>   | <span data-ttu-id="d15cf-294">Empfehlungen zur einfacheren Verwendung Ihres Computers (eyesight)</span><span class="sxs-lookup"><span data-stu-id="d15cf-294">Get recommendations to make your computer easier to use (eyesight)</span></span>  |

    

     

### <a name="family-safety"></a><span data-ttu-id="d15cf-295">Family Safety</span><span class="sxs-lookup"><span data-stu-id="d15cf-295">Family Safety</span></span>

-   <span data-ttu-id="d15cf-296">**Kanonischer Name**: Microsoft. Parser Controls</span><span class="sxs-lookup"><span data-stu-id="d15cf-296">**Canonical name**: Microsoft.ParentalControls</span></span>
-   <span data-ttu-id="d15cf-297">**GUID**: {96ae8d84-A250-4520-95a5-a47a7e3c548b}</span><span class="sxs-lookup"><span data-stu-id="d15cf-297">**GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}</span></span>
-   <span data-ttu-id="d15cf-298">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-298">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-299">**Modulname**: @% systemroot% \\ system32 \\wpccpl.dll,-100</span><span class="sxs-lookup"><span data-stu-id="d15cf-299">**Module name**: @%SystemRoot%\\System32\\wpccpl.dll,-100</span></span>
-   <span data-ttu-id="d15cf-300">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-300">**Pages**</span></span>

    | <span data-ttu-id="d15cf-301">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-301">Page Name</span></span>   | <span data-ttu-id="d15cf-302">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-302">Opens</span></span>                                  |
    |-------------|----------------------------------------|
    | <span data-ttu-id="d15cf-303">pageuserhub</span><span class="sxs-lookup"><span data-stu-id="d15cf-303">pageUserHub</span></span> | <span data-ttu-id="d15cf-304">Auswählen eines Benutzers und Einrichten der Familien Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d15cf-304">Choose a user and set up Family Safety</span></span> |

    

     

### <a name="file-history"></a><span data-ttu-id="d15cf-305">Dateiversionsverlauf</span><span class="sxs-lookup"><span data-stu-id="d15cf-305">File History</span></span>

-   <span data-ttu-id="d15cf-306">**Kanonischer Name**: Microsoft. File History</span><span class="sxs-lookup"><span data-stu-id="d15cf-306">**Canonical name**: Microsoft.FileHistory</span></span>
-   <span data-ttu-id="d15cf-307">**GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span><span class="sxs-lookup"><span data-stu-id="d15cf-307">**GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span></span>
-   <span data-ttu-id="d15cf-308">**Unterstütztes Betriebssystem**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-308">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-309">**Modulname**: @% systemroot% \\ system32 \\fhcpl.dll,-52</span><span class="sxs-lookup"><span data-stu-id="d15cf-309">**Module name**: @%SystemRoot%\\System32\\fhcpl.dll,-52</span></span>
-   <span data-ttu-id="d15cf-310">Der Datei Versionsverlauf enthält eine neuere Version des Sicherungs-und Wiederherstellungs Elements, aber der kanonische Name des älteren Elements wird nicht dem Datei Versionsverlauf zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-310">File History includes a newer version of the Backup and Restore item, but that older item's canonical name does not remap to File History.</span></span>

### <a name="folder-options"></a><span data-ttu-id="d15cf-311">Ordneroptionen</span><span class="sxs-lookup"><span data-stu-id="d15cf-311">Folder Options</span></span>

-   <span data-ttu-id="d15cf-312">**Kanonischer Name**: Microsoft. folderoptions</span><span class="sxs-lookup"><span data-stu-id="d15cf-312">**Canonical name**: Microsoft.FolderOptions</span></span>
-   <span data-ttu-id="d15cf-313">**GUID**: {6dfd7c5c-2451-11d3-A299-00c04r8ef6af}</span><span class="sxs-lookup"><span data-stu-id="d15cf-313">**GUID**: {6DFD7C5C-2451-11d3-A299-00C04F8EF6AF}</span></span>
-   <span data-ttu-id="d15cf-314">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-314">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-315">**Modulname**: @% systemroot% \\ system32 \\shell32.dll,-22985</span><span class="sxs-lookup"><span data-stu-id="d15cf-315">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22985</span></span>

### <a name="fonts"></a><span data-ttu-id="d15cf-316">Schriftarten</span><span class="sxs-lookup"><span data-stu-id="d15cf-316">Fonts</span></span>

-   <span data-ttu-id="d15cf-317">**Kanonischer Name**: Microsoft. Fonts</span><span class="sxs-lookup"><span data-stu-id="d15cf-317">**Canonical name**: Microsoft.Fonts</span></span>
-   <span data-ttu-id="d15cf-318">**GUID**: {93412589-74d4-4e4e-ad0e-e0cb621440fd}</span><span class="sxs-lookup"><span data-stu-id="d15cf-318">**GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}</span></span>
-   <span data-ttu-id="d15cf-319">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-319">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-320">**Modulname**: @% systemroot% \\ system32 \\FontExt.dll,-8007</span><span class="sxs-lookup"><span data-stu-id="d15cf-320">**Module name**: @%SystemRoot%\\System32\\FontExt.dll,-8007</span></span>

### <a name="homegroup"></a><span data-ttu-id="d15cf-321">Heimnetzgruppe</span><span class="sxs-lookup"><span data-stu-id="d15cf-321">HomeGroup</span></span>

-   <span data-ttu-id="d15cf-322">**Kanonischer Name**: Microsoft. HomeGroup</span><span class="sxs-lookup"><span data-stu-id="d15cf-322">**Canonical name**: Microsoft.HomeGroup</span></span>
-   <span data-ttu-id="d15cf-323">**GUID**: {67ca7650-96e6-4fdd-BB43-a8e774f73a57}</span><span class="sxs-lookup"><span data-stu-id="d15cf-323">**GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}</span></span>
-   <span data-ttu-id="d15cf-324">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-324">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-325">**Modulname**: @% systemroot% \\ system32 \\hgcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-325">**Module name**: @%SystemRoot%\\System32\\hgcpl.dll,-1</span></span>

### <a name="indexing-options"></a><span data-ttu-id="d15cf-326">Indizierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="d15cf-326">Indexing Options</span></span>

-   <span data-ttu-id="d15cf-327">**Kanonischer Name**: Microsoft. indexingoptions</span><span class="sxs-lookup"><span data-stu-id="d15cf-327">**Canonical name**: Microsoft.IndexingOptions</span></span>
-   <span data-ttu-id="d15cf-328">**GUID**: {87d66a43-7b11-4a28-9811-c86ee395acb7}</span><span class="sxs-lookup"><span data-stu-id="d15cf-328">**GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}</span></span>
-   <span data-ttu-id="d15cf-329">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-329">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-330">**Modulname**: @% systemroot% \\ system32 \\srchadmin.dll,-601</span><span class="sxs-lookup"><span data-stu-id="d15cf-330">**Module name**: @%SystemRoot%\\System32\\srchadmin.dll,-601</span></span>

### <a name="infrared"></a><span data-ttu-id="d15cf-331">Infrarot</span><span class="sxs-lookup"><span data-stu-id="d15cf-331">Infrared</span></span>

-   <span data-ttu-id="d15cf-332">**Kanonischer Name**: Microsoft. Infrarot</span><span class="sxs-lookup"><span data-stu-id="d15cf-332">**Canonical name**: Microsoft.Infrared</span></span>
-   <span data-ttu-id="d15cf-333">**GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="d15cf-333">**GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span>
-   <span data-ttu-id="d15cf-334">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-334">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-335">**Modulname**: @% systemroot% \\ system32 \\irprops.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-335">**Module name**: @%SystemRoot%\\System32\\irprops.cpl,-1</span></span>

### <a name="internet-options"></a><span data-ttu-id="d15cf-336">Internetoptionen</span><span class="sxs-lookup"><span data-stu-id="d15cf-336">Internet Options</span></span>

-   <span data-ttu-id="d15cf-337">**Kanonischer Name**: Microsoft. internetoptions</span><span class="sxs-lookup"><span data-stu-id="d15cf-337">**Canonical name**: Microsoft.InternetOptions</span></span>
-   <span data-ttu-id="d15cf-338">**GUID**: {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}</span><span class="sxs-lookup"><span data-stu-id="d15cf-338">**GUID**: {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}</span></span>
-   <span data-ttu-id="d15cf-339">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-339">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-340">**Modulname**: @C: \\ Windows \\ system32 \\inetcpl.cpl,-4312</span><span class="sxs-lookup"><span data-stu-id="d15cf-340">**Module name**: @C:\\Windows\\System32\\inetcpl.cpl,-4312</span></span>
-   <span data-ttu-id="d15cf-341">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-341">**Pages**</span></span>

    | <span data-ttu-id="d15cf-342">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-342">Page Name</span></span> | <span data-ttu-id="d15cf-343">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-343">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="d15cf-344">1</span><span class="sxs-lookup"><span data-stu-id="d15cf-344">1</span></span>         | <span data-ttu-id="d15cf-345">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d15cf-345">Security</span></span>    |
    | <span data-ttu-id="d15cf-346">2</span><span class="sxs-lookup"><span data-stu-id="d15cf-346">2</span></span>         | <span data-ttu-id="d15cf-347">Datenschutz</span><span class="sxs-lookup"><span data-stu-id="d15cf-347">Privacy</span></span>     |
    | <span data-ttu-id="d15cf-348">3</span><span class="sxs-lookup"><span data-stu-id="d15cf-348">3</span></span>         | <span data-ttu-id="d15cf-349">Inhalt</span><span class="sxs-lookup"><span data-stu-id="d15cf-349">Content</span></span>     |
    | <span data-ttu-id="d15cf-350">4</span><span class="sxs-lookup"><span data-stu-id="d15cf-350">4</span></span>         | <span data-ttu-id="d15cf-351">Verbindungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-351">Connections</span></span> |
    | <span data-ttu-id="d15cf-352">5</span><span class="sxs-lookup"><span data-stu-id="d15cf-352">5</span></span>         | <span data-ttu-id="d15cf-353">Programs</span><span class="sxs-lookup"><span data-stu-id="d15cf-353">Programs</span></span>    |
    | <span data-ttu-id="d15cf-354">6</span><span class="sxs-lookup"><span data-stu-id="d15cf-354">6</span></span>         | <span data-ttu-id="d15cf-355">Erweitert</span><span class="sxs-lookup"><span data-stu-id="d15cf-355">Advanced</span></span>    |

    

     

### <a name="iscsi-initiator"></a><span data-ttu-id="d15cf-356">iSCSI-Initiator</span><span class="sxs-lookup"><span data-stu-id="d15cf-356">iSCSI Initiator</span></span>

-   <span data-ttu-id="d15cf-357">**Kanonischer Name**: Microsoft. iscsiinitiator</span><span class="sxs-lookup"><span data-stu-id="d15cf-357">**Canonical name**: Microsoft.iSCSIInitiator</span></span>
-   <span data-ttu-id="d15cf-358">**GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span><span class="sxs-lookup"><span data-stu-id="d15cf-358">**GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span></span>
-   <span data-ttu-id="d15cf-359">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-359">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-360">**Modulname**: @% systemroot% \\ system32 \\iscsicpl.dll,-5001</span><span class="sxs-lookup"><span data-stu-id="d15cf-360">**Module name**: @%SystemRoot%\\System32\\iscsicpl.dll,-5001</span></span>

### <a name="isns-server"></a><span data-ttu-id="d15cf-361">iSNS-Server</span><span class="sxs-lookup"><span data-stu-id="d15cf-361">iSNS Server</span></span>

-   <span data-ttu-id="d15cf-362">**Kanonischer Name**: Microsoft. isnsserver</span><span class="sxs-lookup"><span data-stu-id="d15cf-362">**Canonical name**: Microsoft.iSNSServer</span></span>
-   <span data-ttu-id="d15cf-363">**GUID**: {0d2a3442-5181-4e3a-9bd4-83bd10af3d76}</span><span class="sxs-lookup"><span data-stu-id="d15cf-363">**GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}</span></span>
-   <span data-ttu-id="d15cf-364">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-364">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-365">**Modulname**: @% systemroot% \\ system32 \\isnssrv.dll,-5005</span><span class="sxs-lookup"><span data-stu-id="d15cf-365">**Module name**: @%SystemRoot%\\System32\\isnssrv.dll,-5005</span></span>
-   <span data-ttu-id="d15cf-366">Dieses System Steuerungselement wird nur in Serverversionen von Windows angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d15cf-366">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="keyboard"></a><span data-ttu-id="d15cf-367">Tastatur</span><span class="sxs-lookup"><span data-stu-id="d15cf-367">Keyboard</span></span>

-   <span data-ttu-id="d15cf-368">**Kanonischer Name**: Microsoft. Keyboard</span><span class="sxs-lookup"><span data-stu-id="d15cf-368">**Canonical name**: Microsoft.Keyboard</span></span>
-   <span data-ttu-id="d15cf-369">**GUID**: {725be8b7-668e-4c7b-8F 90-46bdb0936430}</span><span class="sxs-lookup"><span data-stu-id="d15cf-369">**GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}</span></span>
-   <span data-ttu-id="d15cf-370">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-370">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-371">**Modulname**: @% systemroot% \\ system32 \\main.cpl,-102</span><span class="sxs-lookup"><span data-stu-id="d15cf-371">**Module name**: @%SystemRoot%\\System32\\main.cpl,-102</span></span>

### <a name="location-settings"></a><span data-ttu-id="d15cf-372">Standorteinstellungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-372">Location Settings</span></span>

-   <span data-ttu-id="d15cf-373">**Kanonischer Name**: Microsoft. locationsettings</span><span class="sxs-lookup"><span data-stu-id="d15cf-373">**Canonical name**: Microsoft.LocationSettings</span></span>
-   <span data-ttu-id="d15cf-374">**GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="d15cf-374">**GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}</span></span>
-   <span data-ttu-id="d15cf-375">**Unterstütztes Betriebssystem**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-375">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-376">**Modulname**: @% systemroot% \\ system32 \\SensorsCpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-376">**Module name**: @%SystemRoot%\\System32\\SensorsCpl.dll,-1</span></span>

### <a name="mouse"></a><span data-ttu-id="d15cf-377">Maus</span><span class="sxs-lookup"><span data-stu-id="d15cf-377">Mouse</span></span>

-   <span data-ttu-id="d15cf-378">**Kanonischer Name**: Microsoft. Mouse</span><span class="sxs-lookup"><span data-stu-id="d15cf-378">**Canonical name**: Microsoft.Mouse</span></span>
-   <span data-ttu-id="d15cf-379">**GUID**: {6c8eec18-8d75-41b2-a177-8831d59d2d50}</span><span class="sxs-lookup"><span data-stu-id="d15cf-379">**GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}</span></span>
-   <span data-ttu-id="d15cf-380">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-380">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-381">**Modulname**: @% systemroot% \\ system32 \\main.cpl,-100</span><span class="sxs-lookup"><span data-stu-id="d15cf-381">**Module name**: @%SystemRoot%\\System32\\main.cpl,-100</span></span>
-   <span data-ttu-id="d15cf-382">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-382">**Pages**</span></span>

    | <span data-ttu-id="d15cf-383">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-383">Page Name</span></span> | <span data-ttu-id="d15cf-384">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-384">Opens</span></span>           |
    |-----------|-----------------|
    | <span data-ttu-id="d15cf-385">1</span><span class="sxs-lookup"><span data-stu-id="d15cf-385">1</span></span>         | <span data-ttu-id="d15cf-386">Zeiger</span><span class="sxs-lookup"><span data-stu-id="d15cf-386">Pointers</span></span>        |
    | <span data-ttu-id="d15cf-387">2</span><span class="sxs-lookup"><span data-stu-id="d15cf-387">2</span></span>         | <span data-ttu-id="d15cf-388">Zeiger Optionen</span><span class="sxs-lookup"><span data-stu-id="d15cf-388">Pointer Options</span></span> |
    | <span data-ttu-id="d15cf-389">3</span><span class="sxs-lookup"><span data-stu-id="d15cf-389">3</span></span>         | <span data-ttu-id="d15cf-390">Wheel</span><span class="sxs-lookup"><span data-stu-id="d15cf-390">Wheel</span></span>           |
    | <span data-ttu-id="d15cf-391">4</span><span class="sxs-lookup"><span data-stu-id="d15cf-391">4</span></span>         | <span data-ttu-id="d15cf-392">Hardware</span><span class="sxs-lookup"><span data-stu-id="d15cf-392">Hardware</span></span>        |

    

     

### <a name="mpioconfiguration"></a><span data-ttu-id="d15cf-393">Mpioconfiguration</span><span class="sxs-lookup"><span data-stu-id="d15cf-393">MPIOConfiguration</span></span>

-   <span data-ttu-id="d15cf-394">**Kanonischer Name**: Microsoft. mpioconfiguration</span><span class="sxs-lookup"><span data-stu-id="d15cf-394">**Canonical name**: Microsoft.MPIOConfiguration</span></span>
-   <span data-ttu-id="d15cf-395">**GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}</span><span class="sxs-lookup"><span data-stu-id="d15cf-395">**GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}</span></span>
-   <span data-ttu-id="d15cf-396">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-396">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-397">**Modulname**: @% systemroot% \\ system32 \\mpiocpl.dll,-1000</span><span class="sxs-lookup"><span data-stu-id="d15cf-397">**Module name**: @%SystemRoot%\\System32\\mpiocpl.dll,-1000</span></span>
-   <span data-ttu-id="d15cf-398">Dieses System Steuerungselement wird nur in Serverversionen von Windows angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d15cf-398">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="network-and-sharing-center"></a><span data-ttu-id="d15cf-399">Netzwerk- und Freigabecenter</span><span class="sxs-lookup"><span data-stu-id="d15cf-399">Network and Sharing Center</span></span>

-   <span data-ttu-id="d15cf-400">**Kanonischer Name**: Microsoft. networkandsharingcenter</span><span class="sxs-lookup"><span data-stu-id="d15cf-400">**Canonical name**: Microsoft.NetworkAndSharingCenter</span></span>
-   <span data-ttu-id="d15cf-401">**GUID**: {8e908fc9-becc-40f 6-915b-f 4ca0e70d03d}</span><span class="sxs-lookup"><span data-stu-id="d15cf-401">**GUID**: {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}</span></span>
-   <span data-ttu-id="d15cf-402">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-402">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-403">**Modulname**: @% systemroot% \\ system32 \\netcenter.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-403">**Module name**: @%SystemRoot%\\System32\\netcenter.dll,-1</span></span>
-   <span data-ttu-id="d15cf-404">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-404">**Pages**</span></span>

    | <span data-ttu-id="d15cf-405">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-405">Page Name</span></span>  | <span data-ttu-id="d15cf-406">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-406">Opens</span></span>                     |
    |------------|---------------------------|
    | <span data-ttu-id="d15cf-407">Erweitert</span><span class="sxs-lookup"><span data-stu-id="d15cf-407">Advanced</span></span>   | <span data-ttu-id="d15cf-408">Erweiterte Freigabe Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-408">Advanced sharing settings</span></span> |
    | <span data-ttu-id="d15cf-409">Share Media</span><span class="sxs-lookup"><span data-stu-id="d15cf-409">ShareMedia</span></span> | <span data-ttu-id="d15cf-410">Optionen für Medien Streaming</span><span class="sxs-lookup"><span data-stu-id="d15cf-410">Media streaming options</span></span>   |

    

     

### <a name="notification-area-icons"></a><span data-ttu-id="d15cf-411">Benachrichtigungs Bereichs Symbole</span><span class="sxs-lookup"><span data-stu-id="d15cf-411">Notification Area Icons</span></span>

-   <span data-ttu-id="d15cf-412">**Kanonischer Name**: Microsoft. notificationareaicons</span><span class="sxs-lookup"><span data-stu-id="d15cf-412">**Canonical name**: Microsoft.NotificationAreaIcons</span></span>
-   <span data-ttu-id="d15cf-413">**GUID**: {05d7b0f 4-2121-4eff-BB. b-ed3g69b894d9}</span><span class="sxs-lookup"><span data-stu-id="d15cf-413">**GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}</span></span>
-   <span data-ttu-id="d15cf-414">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-414">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-415">**Modulname**: @% systemroot% \\ system32 \\taskbarcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-415">**Module name**: @%SystemRoot%\\System32\\taskbarcpl.dll,-1</span></span>

### <a name="pen-and-touch"></a><span data-ttu-id="d15cf-416">Stift und berühren</span><span class="sxs-lookup"><span data-stu-id="d15cf-416">Pen and Touch</span></span>

-   <span data-ttu-id="d15cf-417">**Kanonischer Name**: Microsoft. pandtouchscreen</span><span class="sxs-lookup"><span data-stu-id="d15cf-417">**Canonical name**: Microsoft.PenAndTouch</span></span>
-   <span data-ttu-id="d15cf-418">**GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="d15cf-418">**GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span>
-   <span data-ttu-id="d15cf-419">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-419">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-420">**Modulname**: @% systemroot% \\ system32 \\tabletpc.cpl,-10103</span><span class="sxs-lookup"><span data-stu-id="d15cf-420">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10103</span></span>
-   <span data-ttu-id="d15cf-421">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-421">**Pages**</span></span>

    | <span data-ttu-id="d15cf-422">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-422">Page Name</span></span> | <span data-ttu-id="d15cf-423">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-423">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="d15cf-424">1</span><span class="sxs-lookup"><span data-stu-id="d15cf-424">1</span></span>         | <span data-ttu-id="d15cf-425">Schnelle Stift Bewegungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-425">Flicks</span></span>      |
    | <span data-ttu-id="d15cf-426">2</span><span class="sxs-lookup"><span data-stu-id="d15cf-426">2</span></span>         | <span data-ttu-id="d15cf-427">Handwriting</span><span class="sxs-lookup"><span data-stu-id="d15cf-427">Handwriting</span></span> |

    

     

### <a name="personalization"></a><span data-ttu-id="d15cf-428">Personalization</span><span class="sxs-lookup"><span data-stu-id="d15cf-428">Personalization</span></span>

-   <span data-ttu-id="d15cf-429">**Kanonischer Name**: Microsoft. Personalization</span><span class="sxs-lookup"><span data-stu-id="d15cf-429">**Canonical name**: Microsoft.Personalization</span></span>
-   <span data-ttu-id="d15cf-430">**GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span><span class="sxs-lookup"><span data-stu-id="d15cf-430">**GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span></span>
-   <span data-ttu-id="d15cf-431">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-431">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-432">**Modulname**: @% systemroot% \\ system32 \\themecpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-432">**Module name**: @%SystemRoot%\\System32\\themecpl.dll,-1</span></span>
-   <span data-ttu-id="d15cf-433">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-433">**Pages**</span></span>

    | <span data-ttu-id="d15cf-434">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-434">Page Name</span></span>        | <span data-ttu-id="d15cf-435">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-435">Opens</span></span>                |
    |------------------|----------------------|
    | <span data-ttu-id="d15cf-436">pagecolorzation</span><span class="sxs-lookup"><span data-stu-id="d15cf-436">pageColorization</span></span> | <span data-ttu-id="d15cf-437">Farbe und Darstellung</span><span class="sxs-lookup"><span data-stu-id="d15cf-437">Color and Appearance</span></span> |
    | <span data-ttu-id="d15cf-438">"paarblatt"</span><span class="sxs-lookup"><span data-stu-id="d15cf-438">pageWallpaper</span></span>    | <span data-ttu-id="d15cf-439">Desktop Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d15cf-439">Desktop Background</span></span>   |

    

     

### <a name="phone-and-modem"></a><span data-ttu-id="d15cf-440">Telefon und Modem</span><span class="sxs-lookup"><span data-stu-id="d15cf-440">Phone and Modem</span></span>

-   <span data-ttu-id="d15cf-441">**Kanonischer Name**: Microsoft. phoneandmodem</span><span class="sxs-lookup"><span data-stu-id="d15cf-441">**Canonical name**: Microsoft.PhoneAndModem</span></span>
-   <span data-ttu-id="d15cf-442">**GUID**: {40419485-C444-4567-851a-2dd7bfa1684d}</span><span class="sxs-lookup"><span data-stu-id="d15cf-442">**GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}</span></span>
-   <span data-ttu-id="d15cf-443">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-443">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-444">**Modulname**: @% systemroot% \\ system32 \\telephon.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-444">**Module name**: @%SystemRoot%\\System32\\telephon.cpl,-1</span></span>
-   <span data-ttu-id="d15cf-445">Das Fenster, in dem dieser Wert gestartet wird, wird in Windows-Versionen vor Windows 8 als "Standortinformationen" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d15cf-445">The window that this value launches is titled "Location Information" in versions of Windows prior to Windows 8.</span></span> <span data-ttu-id="d15cf-446">Die Benutzeroberfläche des Elements ändert sich ab Windows 8 erheblich.</span><span class="sxs-lookup"><span data-stu-id="d15cf-446">The item's UI is considerably changed as of Windows 8.</span></span>

### <a name="power-options"></a><span data-ttu-id="d15cf-447">Energieoptionen</span><span class="sxs-lookup"><span data-stu-id="d15cf-447">Power Options</span></span>

-   <span data-ttu-id="d15cf-448">**Kanonischer Name**: Microsoft. poweroptions</span><span class="sxs-lookup"><span data-stu-id="d15cf-448">**Canonical name**: Microsoft.PowerOptions</span></span>
-   <span data-ttu-id="d15cf-449">**GUID**: {025a5937-A6BE-4686-A844-36fe4bec8b6d}</span><span class="sxs-lookup"><span data-stu-id="d15cf-449">**GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}</span></span>
-   <span data-ttu-id="d15cf-450">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-450">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-451">**Modulname**: @% systemroot% \\ system32 \\powercpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-451">**Module name**: @%SystemRoot%\\System32\\powercpl.dll,-1</span></span>
-   <span data-ttu-id="d15cf-452">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-452">**Pages**</span></span>

    | <span data-ttu-id="d15cf-453">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-453">Page Name</span></span>          | <span data-ttu-id="d15cf-454">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-454">Opens</span></span>              |
    |--------------------|--------------------|
    | <span data-ttu-id="d15cf-455">pageglobalsettings</span><span class="sxs-lookup"><span data-stu-id="d15cf-455">pageGlobalSettings</span></span> | <span data-ttu-id="d15cf-456">Systemeinstellungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-456">System Settings</span></span>    |
    | <span data-ttu-id="d15cf-457">pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="d15cf-457">pagePlanSettings</span></span>   | <span data-ttu-id="d15cf-458">Plan Einstellungen bearbeiten</span><span class="sxs-lookup"><span data-stu-id="d15cf-458">Edit Plan Settings</span></span> |

    

     

### <a name="programs-and-features"></a><span data-ttu-id="d15cf-459">Programme und Funktionen</span><span class="sxs-lookup"><span data-stu-id="d15cf-459">Programs and Features</span></span>

-   <span data-ttu-id="d15cf-460">**Kanonischer Name**: Microsoft. Program Sand Features</span><span class="sxs-lookup"><span data-stu-id="d15cf-460">**Canonical name**: Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="d15cf-461">**GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}</span><span class="sxs-lookup"><span data-stu-id="d15cf-461">**GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}</span></span>
-   <span data-ttu-id="d15cf-462">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-462">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-463">**Modulname**: @% systemroot% \\ system32 \\appwiz.cpl,-159</span><span class="sxs-lookup"><span data-stu-id="d15cf-463">**Module name**: @%systemroot%\\system32\\appwiz.cpl,-159</span></span>
-   <span data-ttu-id="d15cf-464">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-464">**Pages**</span></span>

    | <span data-ttu-id="d15cf-465">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-465">Page Name</span></span>                                | <span data-ttu-id="d15cf-466">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-466">Opens</span></span>             |
    |------------------------------------------|-------------------|
    | <span data-ttu-id="d15cf-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span><span class="sxs-lookup"><span data-stu-id="d15cf-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span></span> | <span data-ttu-id="d15cf-468">Installierte Updates</span><span class="sxs-lookup"><span data-stu-id="d15cf-468">Installed Updates</span></span> |

    

     

### <a name="recovery"></a><span data-ttu-id="d15cf-469">Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="d15cf-469">Recovery</span></span>

-   <span data-ttu-id="d15cf-470">**Kanonischer Name**: Microsoft. Recovery</span><span class="sxs-lookup"><span data-stu-id="d15cf-470">**Canonical name**: Microsoft.Recovery</span></span>
-   <span data-ttu-id="d15cf-471">**GUID**: {9fe63afd-59cf-4419-9775-ABCC3849F861}</span><span class="sxs-lookup"><span data-stu-id="d15cf-471">**GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}</span></span>
-   <span data-ttu-id="d15cf-472">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-472">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-473">**Modulname**: @% systemroot% \\ system32 \\recovery.dll,-101</span><span class="sxs-lookup"><span data-stu-id="d15cf-473">**Module name**: @%SystemRoot%\\System32\\recovery.dll,-101</span></span>

### <a name="region"></a><span data-ttu-id="d15cf-474">Region</span><span class="sxs-lookup"><span data-stu-id="d15cf-474">Region</span></span>

-   <span data-ttu-id="d15cf-475">**Kanonischer Name**: Microsoft. regionandlanguage</span><span class="sxs-lookup"><span data-stu-id="d15cf-475">**Canonical name**: Microsoft.RegionAndLanguage</span></span>
-   <span data-ttu-id="d15cf-476">**GUID**: {62d8ed13-C9D0-4ce8-a914-47dd628bb1b0}</span><span class="sxs-lookup"><span data-stu-id="d15cf-476">**GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span>
-   <span data-ttu-id="d15cf-477">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-477">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-478">**Modulname**: @% systemroot% \\ system32 \\intl.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-478">**Module name**: @%SystemRoot%\\System32\\intl.cpl,-1</span></span>
-   <span data-ttu-id="d15cf-479">Das in Windows 7 gefundene Regions-und sprach Element war von Windows 8 getrennt.</span><span class="sxs-lookup"><span data-stu-id="d15cf-479">The Region and Language item found in Windows 7 was split as of Windows 8.</span></span> <span data-ttu-id="d15cf-480">Microsoft. regionandlanguage öffnet nun das Regions Element.</span><span class="sxs-lookup"><span data-stu-id="d15cf-480">Microsoft.RegionAndLanguage now launches the Region item.</span></span> <span data-ttu-id="d15cf-481">Verwenden Sie [Microsoft. Language](#location-settings), um das sprach Element zu starten.</span><span class="sxs-lookup"><span data-stu-id="d15cf-481">To launch the Language item, use [Microsoft.Language](#location-settings).</span></span>
-   <span data-ttu-id="d15cf-482">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-482">**Pages**</span></span>

    | <span data-ttu-id="d15cf-483">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-483">Page Name</span></span> | <span data-ttu-id="d15cf-484">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-484">Opens</span></span>          |
    |-----------|----------------|
    | <span data-ttu-id="d15cf-485">1</span><span class="sxs-lookup"><span data-stu-id="d15cf-485">1</span></span>         | <span data-ttu-id="d15cf-486">Standort</span><span class="sxs-lookup"><span data-stu-id="d15cf-486">Location</span></span>       |
    | <span data-ttu-id="d15cf-487">2</span><span class="sxs-lookup"><span data-stu-id="d15cf-487">2</span></span>         | <span data-ttu-id="d15cf-488">Administrative</span><span class="sxs-lookup"><span data-stu-id="d15cf-488">Administrative</span></span> |

    

     

### <a name="remoteapp-and-desktop-connections"></a><span data-ttu-id="d15cf-489">RemoteApp- und Desktopverbindungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-489">RemoteApp and Desktop Connections</span></span>

-   <span data-ttu-id="d15cf-490">**Kanonischer Name**: Microsoft. remoteappanddesktopconnections</span><span class="sxs-lookup"><span data-stu-id="d15cf-490">**Canonical name**: Microsoft.RemoteAppAndDesktopConnections</span></span>
-   <span data-ttu-id="d15cf-491">**GUID**: {241d7c96-s8bf -4s85-b01t-e2b043341a4b}</span><span class="sxs-lookup"><span data-stu-id="d15cf-491">**GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}</span></span>
-   <span data-ttu-id="d15cf-492">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-492">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-493">**Modulname**: @% systemroot% \\ system32 \\tsworkspace.dll,-15300</span><span class="sxs-lookup"><span data-stu-id="d15cf-493">**Module name**: @%SystemRoot%\\System32\\tsworkspace.dll,-15300</span></span>

### <a name="sound"></a><span data-ttu-id="d15cf-494">Sound</span><span class="sxs-lookup"><span data-stu-id="d15cf-494">Sound</span></span>

-   <span data-ttu-id="d15cf-495">**Kanonischer Name**: Microsoft. Sound</span><span class="sxs-lookup"><span data-stu-id="d15cf-495">**Canonical name**: Microsoft.Sound</span></span>
-   <span data-ttu-id="d15cf-496">**GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="d15cf-496">**GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span>
-   <span data-ttu-id="d15cf-497">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-497">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-498">**Modulname**: @% systemroot% \\ system32 \\mmsys.cpl,-300</span><span class="sxs-lookup"><span data-stu-id="d15cf-498">**Module name**: @%SystemRoot%\\System32\\mmsys.cpl,-300</span></span>

### <a name="speech-recognition"></a><span data-ttu-id="d15cf-499">Spracherkennung</span><span class="sxs-lookup"><span data-stu-id="d15cf-499">Speech Recognition</span></span>

-   <span data-ttu-id="d15cf-500">**Kanonischer Name**: Microsoft. Sprech Erkennung</span><span class="sxs-lookup"><span data-stu-id="d15cf-500">**Canonical name**: Microsoft.SpeechRecognition</span></span>
-   <span data-ttu-id="d15cf-501">**GUID**: {58e3c745-D971-4081-9034-86e34b30836a}</span><span class="sxs-lookup"><span data-stu-id="d15cf-501">**GUID**: {58E3C745-D971-4081-9034-86E34B30836A}</span></span>
-   <span data-ttu-id="d15cf-502">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-502">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-503">**Modulname**: @% systemroot% \\ system32 \\ Speech Speech \\ UX \\speechuxcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-503">**Module name**: @%SystemRoot%\\System32\\Speech\\SpeechUX\\speechuxcpl.dll,-1</span></span>

### <a name="storage-spaces"></a><span data-ttu-id="d15cf-504">Speicherplätze</span><span class="sxs-lookup"><span data-stu-id="d15cf-504">Storage Spaces</span></span>

-   <span data-ttu-id="d15cf-505">**Kanonischer Name**: Microsoft. storagespaces</span><span class="sxs-lookup"><span data-stu-id="d15cf-505">**Canonical name**: Microsoft.StorageSpaces</span></span>
-   <span data-ttu-id="d15cf-506">**GUID**: {F942C606-0914-47AB-BE56-1321B8035096}</span><span class="sxs-lookup"><span data-stu-id="d15cf-506">**GUID**: {F942C606-0914-47AB-BE56-1321B8035096}</span></span>
-   <span data-ttu-id="d15cf-507">**Unterstütztes Betriebssystem**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-507">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-508">**Modulname**: @C: \\ Windows \\ system32 \\SpaceControl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-508">**Module name**: @C:\\Windows\\System32\\SpaceControl.dll,-1</span></span>

### <a name="sync-center"></a><span data-ttu-id="d15cf-509">Synchronisierungscenter</span><span class="sxs-lookup"><span data-stu-id="d15cf-509">Sync Center</span></span>

-   <span data-ttu-id="d15cf-510">**Kanonischer Name**: Microsoft. synccenter</span><span class="sxs-lookup"><span data-stu-id="d15cf-510">**Canonical name**: Microsoft.SyncCenter</span></span>
-   <span data-ttu-id="d15cf-511">**GUID**: {9c73f 5e5-7 AE7-4e32-a8e8-8d23b85255bf}</span><span class="sxs-lookup"><span data-stu-id="d15cf-511">**GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}</span></span>
-   <span data-ttu-id="d15cf-512">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-512">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-513">**Modulname**: @% systemroot% \\ system32 \\SyncCenter.dll,-3000</span><span class="sxs-lookup"><span data-stu-id="d15cf-513">**Module name**: @%SystemRoot%\\System32\\SyncCenter.dll,-3000</span></span>

### <a name="system"></a><span data-ttu-id="d15cf-514">System</span><span class="sxs-lookup"><span data-stu-id="d15cf-514">System</span></span>

-   <span data-ttu-id="d15cf-515">**Kanonischer Name**: Microsoft.System</span><span class="sxs-lookup"><span data-stu-id="d15cf-515">**Canonical name**: Microsoft.System</span></span>
-   <span data-ttu-id="d15cf-516">**GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span><span class="sxs-lookup"><span data-stu-id="d15cf-516">**GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span></span>
-   <span data-ttu-id="d15cf-517">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-517">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-518">**Modulname**: @% systemroot% \\ system32 \\systemcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-518">**Module name**: @%SystemRoot%\\System32\\systemcpl.dll,-1</span></span>

### <a name="tablet-pc-settings"></a><span data-ttu-id="d15cf-519">Tablet PC-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-519">Tablet PC Settings</span></span>

-   <span data-ttu-id="d15cf-520">**Kanonischer Name**: Microsoft. tabletpcsettings</span><span class="sxs-lookup"><span data-stu-id="d15cf-520">**Canonical name**: Microsoft.TabletPCSettings</span></span>
-   <span data-ttu-id="d15cf-521">**GUID**: {80F 5-FECA-45b3-BC32-752c152e456e}</span><span class="sxs-lookup"><span data-stu-id="d15cf-521">**GUID**: {80F3F1D5-FECA-45F3-BC32-752C152E456E}</span></span>
-   <span data-ttu-id="d15cf-522">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-522">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-523">**Modulname**: @% systemroot% \\ system32 \\tabletpc.cpl,-10100</span><span class="sxs-lookup"><span data-stu-id="d15cf-523">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10100</span></span>

### <a name="taskbar-and-navigation"></a><span data-ttu-id="d15cf-524">Taskleiste und Navigation</span><span class="sxs-lookup"><span data-stu-id="d15cf-524">Taskbar and Navigation</span></span>

-   <span data-ttu-id="d15cf-525">**Kanonischer Name**: Microsoft. Taskleiste</span><span class="sxs-lookup"><span data-stu-id="d15cf-525">**Canonical name**: Microsoft.Taskbar</span></span>
-   <span data-ttu-id="d15cf-526">**GUID**: {0df44eaa-ff21-4412-828e-260a8728e7f1}</span><span class="sxs-lookup"><span data-stu-id="d15cf-526">**GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span>
-   <span data-ttu-id="d15cf-527">**Unterstütztes Betriebssystem**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-527">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-528">**Modulname**: @% systemroot% \\ system32 \\shell32.dll,-32517</span><span class="sxs-lookup"><span data-stu-id="d15cf-528">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-32517</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="d15cf-529">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="d15cf-529">Troubleshooting</span></span>

-   <span data-ttu-id="d15cf-530">**Kanonischer Name**: Microsoft. Troubleshooting</span><span class="sxs-lookup"><span data-stu-id="d15cf-530">**Canonical name**: Microsoft.Troubleshooting</span></span>
-   <span data-ttu-id="d15cf-531">**GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span><span class="sxs-lookup"><span data-stu-id="d15cf-531">**GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span></span>
-   <span data-ttu-id="d15cf-532">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-532">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-533">**Modulname**: @% systemroot% \\ system32 \\DiagCpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-533">**Module name**: @%SystemRoot%\\System32\\DiagCpl.dll,-1</span></span>
-   <span data-ttu-id="d15cf-534">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-534">**Pages**</span></span>

    | <span data-ttu-id="d15cf-535">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-535">Page Name</span></span>   | <span data-ttu-id="d15cf-536">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-536">Opens</span></span>   |
    |-------------|---------|
    | <span data-ttu-id="d15cf-537">Historypage</span><span class="sxs-lookup"><span data-stu-id="d15cf-537">HistoryPage</span></span> | <span data-ttu-id="d15cf-538">Verlauf</span><span class="sxs-lookup"><span data-stu-id="d15cf-538">History</span></span> |

    

     

### <a name="tsappinstall"></a><span data-ttu-id="d15cf-539">"T AppInstall"</span><span class="sxs-lookup"><span data-stu-id="d15cf-539">TSAppInstall</span></span>

-   <span data-ttu-id="d15cf-540">**Kanonischer Name**: Microsoft. tappinstall</span><span class="sxs-lookup"><span data-stu-id="d15cf-540">**Canonical name**: Microsoft.TSAppInstall</span></span>
-   <span data-ttu-id="d15cf-541">**GUID**: {BAA884F4-3432-48b8-aa72-9BF20EEF31D5}</span><span class="sxs-lookup"><span data-stu-id="d15cf-541">**GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}</span></span>
-   <span data-ttu-id="d15cf-542">**Unterstütztes Betriebssystem**: Windows 7, Windows 8 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-542">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-543">**Modulname**: @% systemroot% \\ system32 \\tsappinstall.exe,-2001</span><span class="sxs-lookup"><span data-stu-id="d15cf-543">**Module name**: @%systemroot%\\system32\\tsappinstall.exe,-2001</span></span>

### <a name="user-accounts"></a><span data-ttu-id="d15cf-544">Benutzerkonten</span><span class="sxs-lookup"><span data-stu-id="d15cf-544">User Accounts</span></span>

-   <span data-ttu-id="d15cf-545">**Kanonischer Name**: Microsoft. UserAccounts</span><span class="sxs-lookup"><span data-stu-id="d15cf-545">**Canonical name**: Microsoft.UserAccounts</span></span>
-   <span data-ttu-id="d15cf-546">**GUID**: {60632754-C523-4b62-b45c-4172da012619}</span><span class="sxs-lookup"><span data-stu-id="d15cf-546">**GUID**: {60632754-c523-4b62-b45c-4172da012619}</span></span>
-   <span data-ttu-id="d15cf-547">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-547">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-548">**Modulname**: @% systemroot% \\ system32 \\usercpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-548">**Module name**: @%SystemRoot%\\System32\\usercpl.dll,-1</span></span>

### <a name="windows-anytime-upgrade"></a><span data-ttu-id="d15cf-549">Windows Anytime Upgrade</span><span class="sxs-lookup"><span data-stu-id="d15cf-549">Windows Anytime Upgrade</span></span>

-   <span data-ttu-id="d15cf-550">**Kanonischer Name**: Microsoft. windowsanytimeupgrade</span><span class="sxs-lookup"><span data-stu-id="d15cf-550">**Canonical name**: Microsoft.WindowsAnytimeUpgrade</span></span>
-   <span data-ttu-id="d15cf-551">**GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}</span><span class="sxs-lookup"><span data-stu-id="d15cf-551">**GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}</span></span>
-   <span data-ttu-id="d15cf-552">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-552">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-553">**Modulname**: @ $ (resourcestring). \_ SYS \_ mod \_ -Pfad),-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-553">**Module name**: @$(resourceString.\_SYS\_MOD\_PATH),-1</span></span>

### <a name="windows-defender"></a><span data-ttu-id="d15cf-554">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="d15cf-554">Windows Defender</span></span>

-   <span data-ttu-id="d15cf-555">**Kanonischer Name**: Microsoft. windowsdefender</span><span class="sxs-lookup"><span data-stu-id="d15cf-555">**Canonical name**: Microsoft.WindowsDefender</span></span>
-   <span data-ttu-id="d15cf-556">**GUID**: {D8559EB9-20C0-410E-Beda-7ED416AECC2A}</span><span class="sxs-lookup"><span data-stu-id="d15cf-556">**GUID**: {D8559EB9-20C0-410E-BEDA-7ED416AECC2A}</span></span>
-   <span data-ttu-id="d15cf-557">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-557">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-558">**Modulname**: @% Program Files% \\ Windows Defender \\MsMpRes.dll,-104</span><span class="sxs-lookup"><span data-stu-id="d15cf-558">**Module name**: @%ProgramFiles%\\Windows Defender\\MsMpRes.dll,-104</span></span>

### <a name="windows-firewall"></a><span data-ttu-id="d15cf-559">Windows-Firewall</span><span class="sxs-lookup"><span data-stu-id="d15cf-559">Windows Firewall</span></span>

-   <span data-ttu-id="d15cf-560">**Kanonischer Name**: Microsoft. WindowsFirewall</span><span class="sxs-lookup"><span data-stu-id="d15cf-560">**Canonical name**: Microsoft.WindowsFirewall</span></span>
-   <span data-ttu-id="d15cf-561">**GUID**: {4026492f -2F 69-46b8-b9bf -5654fc07e423}</span><span class="sxs-lookup"><span data-stu-id="d15cf-561">**GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}</span></span>
-   <span data-ttu-id="d15cf-562">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-562">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-563">**Modulname**: @C: \\ Windows \\ system32 \\FirewallControlPanel.dll,-12122</span><span class="sxs-lookup"><span data-stu-id="d15cf-563">**Module name**: @C:\\Windows\\system32\\FirewallControlPanel.dll,-12122</span></span>
-   <span data-ttu-id="d15cf-564">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-564">**Pages**</span></span>

    | <span data-ttu-id="d15cf-565">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-565">Page Name</span></span>         | <span data-ttu-id="d15cf-566">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-566">Opens</span></span>        |
    |-------------------|--------------|
    | <span data-ttu-id="d15cf-567">pagekonfigurireapps</span><span class="sxs-lookup"><span data-stu-id="d15cf-567">pageConfigureApps</span></span> | <span data-ttu-id="d15cf-568">Zulässige Apps</span><span class="sxs-lookup"><span data-stu-id="d15cf-568">Allowed apps</span></span> |

    

     

### <a name="windows-mobility-center"></a><span data-ttu-id="d15cf-569">Windows-Mobilitätscenter</span><span class="sxs-lookup"><span data-stu-id="d15cf-569">Windows Mobility Center</span></span>

-   <span data-ttu-id="d15cf-570">**Kanonischer Name**: Microsoft. MobilityCenter</span><span class="sxs-lookup"><span data-stu-id="d15cf-570">**Canonical name**: Microsoft.MobilityCenter</span></span>
-   <span data-ttu-id="d15cf-571">**GUID**: {5ea4f 148-308c-46d7-98a9-49041b1dd468}</span><span class="sxs-lookup"><span data-stu-id="d15cf-571">**GUID**: {5ea4f148-308c-46d7-98a9-49041b1dd468}</span></span>
-   <span data-ttu-id="d15cf-572">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-572">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-573">**Modulname**: @% systemroot% \\ system32 \\mblctr.exe,-1002</span><span class="sxs-lookup"><span data-stu-id="d15cf-573">**Module name**: @%SystemRoot%\\system32\\mblctr.exe,-1002</span></span>

### <a name="windows-to-go"></a><span data-ttu-id="d15cf-574">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="d15cf-574">Windows To Go</span></span>

-   <span data-ttu-id="d15cf-575">**Kanonischer Name**: Microsoft. portableworkspacecreator</span><span class="sxs-lookup"><span data-stu-id="d15cf-575">**Canonical name**: Microsoft.PortableWorkspaceCreator</span></span>
-   <span data-ttu-id="d15cf-576">**GUID**: {8e0c279d-0bd1-43c3-9ebd-31c3dc5b8a77}</span><span class="sxs-lookup"><span data-stu-id="d15cf-576">**GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}</span></span>
-   <span data-ttu-id="d15cf-577">**Unterstütztes Betriebssystem**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-577">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-578">**Modulname**: @% systemroot% \\ system32 \\pwcreator.exe,-151</span><span class="sxs-lookup"><span data-stu-id="d15cf-578">**Module name**: @%SystemRoot%\\System32\\pwcreator.exe,-151</span></span>

### <a name="windows-update"></a><span data-ttu-id="d15cf-579">Windows-Update</span><span class="sxs-lookup"><span data-stu-id="d15cf-579">Windows Update</span></span>

-   <span data-ttu-id="d15cf-580">**Kanonischer Name**: Microsoft. windowsupdate</span><span class="sxs-lookup"><span data-stu-id="d15cf-580">**Canonical name**: Microsoft.WindowsUpdate</span></span>
-   <span data-ttu-id="d15cf-581">**GUID**: {36eef7db-88ad-4e81-AD49-0e313f 0c35f}</span><span class="sxs-lookup"><span data-stu-id="d15cf-581">**GUID**: {36eef7db-88ad-4e81-ad49-0e313f0c35f8}</span></span>
-   <span data-ttu-id="d15cf-582">**Unterstütztes Betriebssystem**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-582">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-583">**Modulname**: @% systemroot% \\ system32 \\wucltux.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-583">**Module name**: @%SystemRoot%\\system32\\wucltux.dll,-1</span></span>
-   <span data-ttu-id="d15cf-584">**Seiten**</span><span class="sxs-lookup"><span data-stu-id="d15cf-584">**Pages**</span></span>

    | <span data-ttu-id="d15cf-585">Seitenname</span><span class="sxs-lookup"><span data-stu-id="d15cf-585">Page Name</span></span>         | <span data-ttu-id="d15cf-586">Opens</span><span class="sxs-lookup"><span data-stu-id="d15cf-586">Opens</span></span>               |
    |-------------------|---------------------|
    | <span data-ttu-id="d15cf-587">pgesettings</span><span class="sxs-lookup"><span data-stu-id="d15cf-587">pageSettings</span></span>      | <span data-ttu-id="d15cf-588">Änderung der Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-588">Change settings</span></span>     |
    | <span data-ttu-id="d15cf-589">pageupdatehistory</span><span class="sxs-lookup"><span data-stu-id="d15cf-589">pageUpdateHistory</span></span> | <span data-ttu-id="d15cf-590">Aktualisierungs Verlauf anzeigen</span><span class="sxs-lookup"><span data-stu-id="d15cf-590">View update history</span></span> |

    

     

### <a name="work-folders"></a><span data-ttu-id="d15cf-591">Arbeitsordner</span><span class="sxs-lookup"><span data-stu-id="d15cf-591">Work Folders</span></span>

-   <span data-ttu-id="d15cf-592">**Kanonischer Name**: Microsoft. workfolders</span><span class="sxs-lookup"><span data-stu-id="d15cf-592">**Canonical name**: Microsoft.WorkFolders</span></span>
-   <span data-ttu-id="d15cf-593">**GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}</span><span class="sxs-lookup"><span data-stu-id="d15cf-593">**GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}</span></span>
-   <span data-ttu-id="d15cf-594">**Unterstütztes Betriebssystem**: Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d15cf-594">**Supported OS**: Windows 8.1</span></span>
-   <span data-ttu-id="d15cf-595">**Modulname**: @C: \\ Windows \\ system32 \\WorkfoldersControl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="d15cf-595">**Module name**: @C:\\Windows\\System32\\WorkfoldersControl.dll,-1</span></span>

## <a name="deprecated-control-panel-canonical-names"></a><span data-ttu-id="d15cf-596">Als veraltet markierte kanonische Name der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="d15cf-596">Deprecated Control Panel Canonical Names</span></span>

<span data-ttu-id="d15cf-597">Im folgenden werden kanonische Namen verwendet, die nicht mehr ab Windows 8.1 oder höher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d15cf-597">The following are canonical names that are no longer in use as of Windows 8.1 or later.</span></span> <span data-ttu-id="d15cf-598">Einige wurden vollständig entfernt.</span><span class="sxs-lookup"><span data-stu-id="d15cf-598">Some have been removed altogether.</span></span> <span data-ttu-id="d15cf-599">Andere wurden in folgenden Situationen neu zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="d15cf-599">Others have been remapped in these situations:</span></span>

-   <span data-ttu-id="d15cf-600">Ein System Steuerungselement wurde umbenannt.</span><span class="sxs-lookup"><span data-stu-id="d15cf-600">A Control Panel item is renamed.</span></span> <span data-ttu-id="d15cf-601">Das umbenannte Element erhält einen neuen kanonischen Namen, behält aber dieselbe GUID bei.</span><span class="sxs-lookup"><span data-stu-id="d15cf-601">The renamed item is given a new canonical name but keeps the same GUID.</span></span> <span data-ttu-id="d15cf-602">In diesem Fall wird mit dem alten kanonischen Namen das umbenannte System Steuerungselement gestartet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-602">In this case, the old canonical name launches the renamed Control Panel item.</span></span> <span data-ttu-id="d15cf-603">Beachten Sie, dass das Element, das gestartet wird, möglicherweise nicht die gleiche Benutzeroberfläche wie die ältere Version dieses Elements verwendet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-603">Be aware that the item that's launched might not use the same UI as that item's older version.</span></span>
-   <span data-ttu-id="d15cf-604">Die Funktionalität eines oder mehrerer System Steuerungselemente wird in ein neues Element verschoben oder konsolidiert.</span><span class="sxs-lookup"><span data-stu-id="d15cf-604">The functionality of one or more Control Panel items is moved or consolidated into a new item.</span></span> <span data-ttu-id="d15cf-605">In diesem Fall wird der alte kanonische Name dem geeignetsten neuen System Steuerungselement zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-605">In this case, the old canonical name maps to the most appropriate new Control Panel item.</span></span>

> [!Note]  
> <span data-ttu-id="d15cf-606">Neuzuordnungen sind aus Gründen der Abwärtskompatibilität vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d15cf-606">Remappings exist for backward compatibility.</span></span> <span data-ttu-id="d15cf-607">Als veraltet markierte Werte sollten nicht in neuem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d15cf-607">You should not use deprecated values in new code.</span></span>

 



| <span data-ttu-id="d15cf-608">Der als veraltet markierte kanonische Name</span><span class="sxs-lookup"><span data-stu-id="d15cf-608">Deprecated canonical name</span></span>                                   | <span data-ttu-id="d15cf-609">System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="d15cf-609">Control Panel Item</span></span>                | <span data-ttu-id="d15cf-610">GUID</span><span class="sxs-lookup"><span data-stu-id="d15cf-610">GUID</span></span>                                   | <span data-ttu-id="d15cf-611">Notizen</span><span class="sxs-lookup"><span data-stu-id="d15cf-611">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d15cf-612">Microsoft. addhardware</span><span class="sxs-lookup"><span data-stu-id="d15cf-612">Microsoft.AddHardware</span></span>                                       | <span data-ttu-id="d15cf-613">Hardware hinzufügen</span><span class="sxs-lookup"><span data-stu-id="d15cf-613">Add Hardware</span></span>                      | <span data-ttu-id="d15cf-614">{7a979262-40ce-46ff-Aeee-7884ac3b6136}</span><span class="sxs-lookup"><span data-stu-id="d15cf-614">{7A979262-40CE-46ff-AEEE-7884AC3B6136}</span></span> | <span data-ttu-id="d15cf-615">Wird [Microsoft. devicesandprinters](#devices-and-printers) ab Windows 7 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-615">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d15cf-616">Microsoft. audiodebug-Themen</span><span class="sxs-lookup"><span data-stu-id="d15cf-616">Microsoft.AudioDevicesAndSoundThemes</span></span>                        | <span data-ttu-id="d15cf-617">Sound</span><span class="sxs-lookup"><span data-stu-id="d15cf-617">Sound</span></span>                             | <span data-ttu-id="d15cf-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="d15cf-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span> | <span data-ttu-id="d15cf-619">Wird [Microsoft. Sound](#sound) ab Windows 7 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-619">Maps to [Microsoft.Sound](#sound) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d15cf-620">Microsoft. backupandrestorecenter/Microsoft. backupandrestore</span><span class="sxs-lookup"><span data-stu-id="d15cf-620">Microsoft.BackupAndRestoreCenter/Microsoft.BackupAndRestore</span></span> | <span data-ttu-id="d15cf-621">Sicherungs-und Wiederherstellungs Center</span><span class="sxs-lookup"><span data-stu-id="d15cf-621">Backup and Restore Center</span></span>         | <span data-ttu-id="d15cf-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span><span class="sxs-lookup"><span data-stu-id="d15cf-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span></span> | <span data-ttu-id="d15cf-623">Microsoft. backupandrestorecenter ist in Windows 7 Microsoft. backupandrestore zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-623">Microsoft.BackupAndRestoreCenter maps to Microsoft.BackupAndRestore in Windows 7.</span></span> <span data-ttu-id="d15cf-624">Beide werden ab Windows 8 entfernt. Verwenden Sie stattdessen [Microsoft. File History](#file-history) .</span><span class="sxs-lookup"><span data-stu-id="d15cf-624">Both are removed as of Windows 8; use [Microsoft.FileHistory](#file-history) instead.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="d15cf-625">Microsoft. CardSpace</span><span class="sxs-lookup"><span data-stu-id="d15cf-625">Microsoft.CardSpace</span></span>                                         | <span data-ttu-id="d15cf-626">Windows CardSpace</span><span class="sxs-lookup"><span data-stu-id="d15cf-626">Windows CardSpace</span></span>                 | <span data-ttu-id="d15cf-627">{78cb147 a-98ea-4aa6-b0df-c8681f 69341c}</span><span class="sxs-lookup"><span data-stu-id="d15cf-627">{78CB147A-98EA-4AA6-B0DF-C8681F69341C}</span></span> | <span data-ttu-id="d15cf-628">Entfernt ab Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d15cf-628">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d15cf-629">Microsoft. Desktopgadgets</span><span class="sxs-lookup"><span data-stu-id="d15cf-629">Microsoft.DesktopGadgets</span></span>                                    | <span data-ttu-id="d15cf-630">Desktop Gadgets</span><span class="sxs-lookup"><span data-stu-id="d15cf-630">Desktop Gadgets</span></span>                   | <span data-ttu-id="d15cf-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="d15cf-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="d15cf-632">Entfernt ab Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d15cf-632">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d15cf-633">Microsoft. getprogramsonline</span><span class="sxs-lookup"><span data-stu-id="d15cf-633">Microsoft.GetProgramsOnline</span></span>                                 | <span data-ttu-id="d15cf-634">Windows Marketplace</span><span class="sxs-lookup"><span data-stu-id="d15cf-634">Windows Marketplace</span></span>               | <span data-ttu-id="d15cf-635">{3e7efb4c-laf1-453d-89eb-56026875ef90}</span><span class="sxs-lookup"><span data-stu-id="d15cf-635">{3e7efb4c-faf1-453d-89eb-56026875ef90}</span></span> | <span data-ttu-id="d15cf-636">Entfernt ab Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d15cf-636">Removed as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d15cf-637">Microsoft. infraredoptions</span><span class="sxs-lookup"><span data-stu-id="d15cf-637">Microsoft.InfraredOptions</span></span>                                   | <span data-ttu-id="d15cf-638">Infrarot</span><span class="sxs-lookup"><span data-stu-id="d15cf-638">Infrared</span></span>                          | <span data-ttu-id="d15cf-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="d15cf-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span> | <span data-ttu-id="d15cf-640">Wird [Microsoft. INFRAS](#infrared) von Windows 7 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-640">Maps to [Microsoft.Infrared](#infrared) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d15cf-641">Microsoft. Language</span><span class="sxs-lookup"><span data-stu-id="d15cf-641">Microsoft.Language</span></span>                                          | <span data-ttu-id="d15cf-642">Sprache</span><span class="sxs-lookup"><span data-stu-id="d15cf-642">Language</span></span>                          | <span data-ttu-id="d15cf-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span><span class="sxs-lookup"><span data-stu-id="d15cf-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span></span> | <span data-ttu-id="d15cf-644">Entfernt ab Windows 10, Version 1803</span><span class="sxs-lookup"><span data-stu-id="d15cf-644">Removed as of Windows 10, version 1803</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="d15cf-645">Microsoft. locationandothersensors</span><span class="sxs-lookup"><span data-stu-id="d15cf-645">Microsoft.LocationAndOtherSensors</span></span>                           | <span data-ttu-id="d15cf-646">Speicherort und andere Sensoren</span><span class="sxs-lookup"><span data-stu-id="d15cf-646">Location and Other Sensors</span></span>        | <span data-ttu-id="d15cf-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="d15cf-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span></span> | <span data-ttu-id="d15cf-648">Wird [Microsoft. locationsettings](#infrared) ab Windows 8 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-648">Maps to [Microsoft.LocationSettings](#infrared) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d15cf-649">Microsoft. pandinputdevices</span><span class="sxs-lookup"><span data-stu-id="d15cf-649">Microsoft.PenAndInputDevices</span></span>                                | <span data-ttu-id="d15cf-650">Stift-und Eingabegeräte</span><span class="sxs-lookup"><span data-stu-id="d15cf-650">Pen and Input Devices</span></span>             | <span data-ttu-id="d15cf-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="d15cf-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span> | <span data-ttu-id="d15cf-652">Wird [Microsoft. pandtouchscreen](#pen-and-touch) ab Windows 7 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-652">Maps to [Microsoft.PenAndTouch](#pen-and-touch) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d15cf-653">Microsoft. PeopleNearMe</span><span class="sxs-lookup"><span data-stu-id="d15cf-653">Microsoft.PeopleNearMe</span></span>                                      | <span data-ttu-id="d15cf-654">Personen in meiner Umgebung</span><span class="sxs-lookup"><span data-stu-id="d15cf-654">People Near Me</span></span>                    | <span data-ttu-id="d15cf-655">{5224f 545-a443-4859-ba23-7b5a95bdc8ef}</span><span class="sxs-lookup"><span data-stu-id="d15cf-655">{5224F545-A443-4859-BA23-7B5A95BDC8EF}</span></span> | <span data-ttu-id="d15cf-656">Entfernt ab Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d15cf-656">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d15cf-657">Microsoft. performanceingeformationandtools</span><span class="sxs-lookup"><span data-stu-id="d15cf-657">Microsoft.PerformanceInformationAndTools</span></span>                    | <span data-ttu-id="d15cf-658">Leistungsinformationen und-Tools</span><span class="sxs-lookup"><span data-stu-id="d15cf-658">Performance Information and Tools</span></span> | <span data-ttu-id="d15cf-659">{78f 3955e-3b90-4184-bd14-5397c15f 1efc}</span><span class="sxs-lookup"><span data-stu-id="d15cf-659">{78F3955E-3B90-4184-BD14-5397C15F1EFC}</span></span> | <span data-ttu-id="d15cf-660">Entfernt ab Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="d15cf-660">Removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="d15cf-661">Microsoft. phoneandmudeoptions</span><span class="sxs-lookup"><span data-stu-id="d15cf-661">Microsoft.PhoneAndModemOptions</span></span>                              | <span data-ttu-id="d15cf-662">Telefon und Modem</span><span class="sxs-lookup"><span data-stu-id="d15cf-662">Phone and Modem</span></span>                   | <span data-ttu-id="d15cf-663">{40419485-C444-4567-851a-2dd7bfa1684d}</span><span class="sxs-lookup"><span data-stu-id="d15cf-663">{40419485-C444-4567-851A-2DD7BFA1684D}</span></span> | <span data-ttu-id="d15cf-664">Wird [Microsoft. phoneandmodem](#phone-and-modem) ab Windows 7 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-664">Maps to [Microsoft.PhoneAndModem](#phone-and-modem) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d15cf-665">Microsoft. Printers</span><span class="sxs-lookup"><span data-stu-id="d15cf-665">Microsoft.Printers</span></span>                                          | <span data-ttu-id="d15cf-666">Drucker</span><span class="sxs-lookup"><span data-stu-id="d15cf-666">Printers</span></span>                          | <span data-ttu-id="d15cf-667">{2227a280-3aea-1069-A2DE-08002b30309d}</span><span class="sxs-lookup"><span data-stu-id="d15cf-667">{2227A280-3AEA-1069-A2DE-08002B30309D}</span></span> | <span data-ttu-id="d15cf-668">Wird [Microsoft. devicesandprinters](#devices-and-printers) ab Windows 7 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-668">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d15cf-669">Microsoft. problemreportsandsolutions</span><span class="sxs-lookup"><span data-stu-id="d15cf-669">Microsoft.ProblemReportsAndSolutions</span></span>                        | <span data-ttu-id="d15cf-670">Problemberichte und -lösungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-670">Problem Reports and Solutions</span></span>     | <span data-ttu-id="d15cf-671">{Fcfeecae-EE1B-4849-AE50-685dcf7717ec}</span><span class="sxs-lookup"><span data-stu-id="d15cf-671">{FCFEECAE-EE1B-4849-AE50-685DCF7717EC}</span></span> | <span data-ttu-id="d15cf-672">Wird [Microsoft. aktioncenter](#action-center) ab Windows 7 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-672">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d15cf-673">Microsoft. regionandlanguageoptions</span><span class="sxs-lookup"><span data-stu-id="d15cf-673">Microsoft.RegionalAndLanguageOptions</span></span>                        | <span data-ttu-id="d15cf-674">Regions- und Sprachoptionen</span><span class="sxs-lookup"><span data-stu-id="d15cf-674">Regional and Language Options</span></span>     | <span data-ttu-id="d15cf-675">{62d8ed13-C9D0-4ce8-a914-47dd628bb1b0}</span><span class="sxs-lookup"><span data-stu-id="d15cf-675">{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span> | <span data-ttu-id="d15cf-676">Wird [Microsoft. regionandlanguage](#region) von Windows 7 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-676">Maps to [Microsoft.RegionAndLanguage](#region) as of Windows 7.</span></span> <span data-ttu-id="d15cf-677">Beachten Sie, dass für die Region und die Sprache ab Windows 8 jeweils ein eigenes System Steuerungselement angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d15cf-677">Note that as of Windows 8, Region and Language were each given their own Control Panel item.</span></span> <span data-ttu-id="d15cf-678">Sowohl Microsoft. regionandlanguageoptions als auch Microsoft. regionandlanguage öffnen das Regions Element zurzeit.</span><span class="sxs-lookup"><span data-stu-id="d15cf-678">Both Microsoft.RegionalAndLanguageOptions and Microsoft.RegionAndLanguage currently open the Region item.</span></span> <span data-ttu-id="d15cf-679">Für den Zugriff auf das sprach Element müssen Sie [Microsoft. Language](#location-settings) verwenden.</span><span class="sxs-lookup"><span data-stu-id="d15cf-679">You must use [Microsoft.Language](#location-settings) to access the Language item.</span></span> |
| <span data-ttu-id="d15cf-680">Microsoft. SecurityCenter</span><span class="sxs-lookup"><span data-stu-id="d15cf-680">Microsoft.SecurityCenter</span></span>                                    | <span data-ttu-id="d15cf-681">Windows-Security Center</span><span class="sxs-lookup"><span data-stu-id="d15cf-681">Windows Security Center</span></span>           | <span data-ttu-id="d15cf-682">{087da31b-0dd3-4537-8e23-64a18591b88b}</span><span class="sxs-lookup"><span data-stu-id="d15cf-682">{087DA31B-0DD3-4537-8E23-64A18591F88B}</span></span> | <span data-ttu-id="d15cf-683">Wird [Microsoft. aktioncenter](#action-center) ab Windows 7 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-683">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d15cf-684">Microsoft. Sprech Erkennungs Optionen</span><span class="sxs-lookup"><span data-stu-id="d15cf-684">Microsoft.SpeechRecognitionOptions</span></span>                          | <span data-ttu-id="d15cf-685">Optionen für die Spracherkennung</span><span class="sxs-lookup"><span data-stu-id="d15cf-685">Speech Recognition Options</span></span>        | <span data-ttu-id="d15cf-686">{58e3c745-D971-4081-9034-86e34b30836a}</span><span class="sxs-lookup"><span data-stu-id="d15cf-686">{58E3C745-D971-4081-9034-86E34B30836A}</span></span> | <span data-ttu-id="d15cf-687">Wird [Microsoft. Sprech Erkennung](#speech-recognition) ab Windows 7 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-687">Maps to [Microsoft.SpeechRecognition](#speech-recognition) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d15cf-688">Microsoft. taskbarandstartmenu</span><span class="sxs-lookup"><span data-stu-id="d15cf-688">Microsoft.TaskbarAndStartMenu</span></span>                               | <span data-ttu-id="d15cf-689">Taskleiste und Startmenü</span><span class="sxs-lookup"><span data-stu-id="d15cf-689">Taskbar and Start Menu</span></span>            | <span data-ttu-id="d15cf-690">{0df44eaa-ff21-4412-828e-260a8728e7f1}</span><span class="sxs-lookup"><span data-stu-id="d15cf-690">{0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span> | <span data-ttu-id="d15cf-691">Wird [Microsoft. Taskbar](#speech-recognition) ab Windows 8 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-691">Maps to [Microsoft.Taskbar](#speech-recognition) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d15cf-692">Microsoft. welcomecenter</span><span class="sxs-lookup"><span data-stu-id="d15cf-692">Microsoft.WelcomeCenter</span></span>                                     | <span data-ttu-id="d15cf-693">Willkommens Center</span><span class="sxs-lookup"><span data-stu-id="d15cf-693">Welcome Center</span></span>                    | <span data-ttu-id="d15cf-694">{CB1B7F8C-C50A-4176-B604-9e24dee8d4d1}</span><span class="sxs-lookup"><span data-stu-id="d15cf-694">{CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1}</span></span> | <span data-ttu-id="d15cf-695">Wird Microsoft. GettingStarted in Windows 7 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-695">Maps to Microsoft.GettingStarted in Windows 7.</span></span> <span data-ttu-id="d15cf-696">Starten der System Steuerungs-Startseite ab Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d15cf-696">Launches the Control Panel home page as of Windows 8.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d15cf-697">Microsoft. windowssidebug Properties</span><span class="sxs-lookup"><span data-stu-id="d15cf-697">Microsoft.WindowsSidebarProperties</span></span>                          | <span data-ttu-id="d15cf-698">Windows-Sidebar-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d15cf-698">Windows Sidebar Properties</span></span>        | <span data-ttu-id="d15cf-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="d15cf-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="d15cf-700">Wird Microsoft. Desktopgadgets in Windows 7 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-700">Maps to Microsoft.DesktopGadgets in Windows 7.</span></span> <span data-ttu-id="d15cf-701">Entfernt ab Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d15cf-701">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="d15cf-702">Microsoft. windowsside Show</span><span class="sxs-lookup"><span data-stu-id="d15cf-702">Microsoft.WindowsSideShow</span></span>                                   | <span data-ttu-id="d15cf-703">Windows SideShow</span><span class="sxs-lookup"><span data-stu-id="d15cf-703">Windows SideShow</span></span>                  | <span data-ttu-id="d15cf-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span><span class="sxs-lookup"><span data-stu-id="d15cf-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span></span> | <span data-ttu-id="d15cf-705">Das in Windows 8 veraltete Feature, das ab Windows 8.1 entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="d15cf-705">Feature deprecated in Windows 8, removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a><span data-ttu-id="d15cf-706">Verwenden von kanonischen Namen in lokalen Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d15cf-706">Using Canonical Names in Local Group Policy</span></span>

<span data-ttu-id="d15cf-707">Ab Windows 7 können Sie kanonische Namen verwenden, um den Zugriff auf einzelne System Steuerungselemente mithilfe von Gruppenrichtlinien einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="d15cf-707">As of Windows 7, you can use canonical names to restrict access to individual Control Panel items through group policy.</span></span> <span data-ttu-id="d15cf-708">Diese Prozedur kann in Windows Vista verwendet werden, aber Sie müssen den Modulnamen anstelle des kanonischen Namens verwenden.</span><span class="sxs-lookup"><span data-stu-id="d15cf-708">This same procedure can be used in Windows Vista, but you have to use the module name instead of the canonical name.</span></span>

### <a name="hiding-individual-control-panel-items"></a><span data-ttu-id="d15cf-709">Ausblenden einzelner System Steuerungselemente</span><span class="sxs-lookup"><span data-stu-id="d15cf-709">Hiding individual Control Panel items</span></span>

<span data-ttu-id="d15cf-710">Verwenden Sie diese Methode, wenn Sie mehr System Steuerungselemente anzeigen möchten, als Sie ausblenden möchten.</span><span class="sxs-lookup"><span data-stu-id="d15cf-710">Use this method if you want to show more Control Panel items than you want to hide.</span></span>

1.  <span data-ttu-id="d15cf-711">Führen Sie die Datei "gpeer dit. msc" aus, um die Editor für lokale Gruppenrichtlinien zu starten.</span><span class="sxs-lookup"><span data-stu-id="d15cf-711">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="d15cf-712">Sie können auch "Gruppenrichtlinie" auf dem Windows 8.1 Start Bildschirm eingeben und dann in den Suchergebnissen die Option **Gruppenrichtlinie bearbeiten** auswählen.</span><span class="sxs-lookup"><span data-stu-id="d15cf-712">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="d15cf-713">Wählen Sie die Option **Benutzerkonfiguration**  >  **Administrative Vorlagen**  >  **Systemsteuerung** aus.</span><span class="sxs-lookup"><span data-stu-id="d15cf-713">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="d15cf-714">Wählen Sie **angegebene System Steuerungselemente ausblenden** aus.</span><span class="sxs-lookup"><span data-stu-id="d15cf-714">Select **Hide specified Control Panel items**.</span></span>
4.  <span data-ttu-id="d15cf-715">Klicken Sie im Fenster **angegebene System Steuerungselemente ausblenden** auf **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="d15cf-715">In the **Hide Specified Control Panel Items** window that opens, click **Enabled**.</span></span>
5.  <span data-ttu-id="d15cf-716">Klicken Sie im Options Panel auf die Schaltfläche **anzeigen** , um die Liste der unzulässigen System Steuerungselemente anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d15cf-716">Click the **Show** button in the Options panel to show the list of disallowed Control Panel items.</span></span>
6.  <span data-ttu-id="d15cf-717">Geben Sie im geöffneten Fenster **Inhalt anzeigen** einen kanonischen Namen in die Spalte **Wert** ein.</span><span class="sxs-lookup"><span data-stu-id="d15cf-717">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="d15cf-718">Wiederholen Sie dies bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d15cf-718">Repeat as necessary.</span></span>
7.  <span data-ttu-id="d15cf-719">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d15cf-719">Click **OK**.</span></span>

### <a name="showing-individual-control-panel-items"></a><span data-ttu-id="d15cf-720">Einzelne System Steuerungselemente werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d15cf-720">Showing individual Control Panel items</span></span>

<span data-ttu-id="d15cf-721">Verwenden Sie diese Methode, wenn Sie mehr System Steuerungselemente ausblenden möchten, als Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="d15cf-721">Use this method if you want to hide more Control Panel items than you want to show.</span></span>

1.  <span data-ttu-id="d15cf-722">Führen Sie die Datei "gpeer dit. msc" aus, um die Editor für lokale Gruppenrichtlinien zu starten.</span><span class="sxs-lookup"><span data-stu-id="d15cf-722">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="d15cf-723">Sie können auch "Gruppenrichtlinie" auf dem Windows 8.1 Start Bildschirm eingeben und dann in den Suchergebnissen die Option **Gruppenrichtlinie bearbeiten** auswählen.</span><span class="sxs-lookup"><span data-stu-id="d15cf-723">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="d15cf-724">Wählen Sie die Option **Benutzerkonfiguration**  >  **Administrative Vorlagen**  >  **Systemsteuerung** aus.</span><span class="sxs-lookup"><span data-stu-id="d15cf-724">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="d15cf-725">Wählen Sie **nur angegebene System Steuerungselemente anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="d15cf-725">Select **Show only specified Control Panel items**.</span></span>
4.  <span data-ttu-id="d15cf-726">Klicken Sie im Fenster **nur angegebene System Steuerungselemente anzeigen** , das geöffnet wird, auf **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="d15cf-726">In the **Show Only Specified Control Panel Items** window that opens, click **Enabled**.</span></span> <span data-ttu-id="d15cf-727">Dadurch wird alles in der Systemsteuerung ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="d15cf-727">This hides everything in the Control Panel.</span></span>
5.  <span data-ttu-id="d15cf-728">Klicken Sie im Options Panel auf die Schaltfläche **anzeigen** , um die Liste der zulässigen System Steuerungselemente anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d15cf-728">Click the **Show** button in the Options panel to show the list of allowed Control Panel items.</span></span>
6.  <span data-ttu-id="d15cf-729">Geben Sie im geöffneten Fenster **Inhalt anzeigen** einen kanonischen Namen in die Spalte **Wert** ein.</span><span class="sxs-lookup"><span data-stu-id="d15cf-729">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="d15cf-730">Wiederholen Sie dies bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d15cf-730">Repeat as necessary.</span></span>
7.  <span data-ttu-id="d15cf-731">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d15cf-731">Click **OK**.</span></span>

<span data-ttu-id="d15cf-732">Wenn Sie alle Einträge entfernen möchten, die Sie der Liste System Steuerungselemente anzeigen oder ausblenden hinzugefügt haben, kehren Sie zum Bildschirm in Schritt 4 zurück, und wählen Sie **nicht konfiguriert** aus, um die Liste zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d15cf-732">If you want to remove all of the entries that you've added to a Show or Hide Control Panel items list, return to the screen in step 4 and select **Not Configured** to clear the list.</span></span> <span data-ttu-id="d15cf-733">Wenn Sie Ihre Einträge beibehalten, aber die Einschränkungen unterbrechen möchten, wählen Sie **deaktiviert** aus.</span><span class="sxs-lookup"><span data-stu-id="d15cf-733">If you want to retain your entries but suspend the restrictions, select **Disabled**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d15cf-734">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d15cf-734">Remarks</span></span>

<span data-ttu-id="d15cf-735">In der Systemsteuerung werden möglicherweise Elemente angezeigt, die hier nicht aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d15cf-735">You might see items in your Control Panel that are not listed here.</span></span> <span data-ttu-id="d15cf-736">Diese Elemente sind nicht Teil von Windows, sondern werden stattdessen bei der Installation verschiedener Software und Hardware, wie Microsoft Office oder einer Grafikkarte, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d15cf-736">Those items are not part of Windows, but instead are added during the installation of various software and hardware, such as Microsoft Office or a video card.</span></span> <span data-ttu-id="d15cf-737">Nicht-Windows-System Steuerungselemente haben möglicherweise einen kanonischen Namen.</span><span class="sxs-lookup"><span data-stu-id="d15cf-737">Non-Windows Control Panel items may or may not have a canonical name.</span></span> <span data-ttu-id="d15cf-738">Wenn Sie den kanonischen Namen eines System Steuerungs Elements suchen möchten, das hier nicht aufgelistet ist, suchen Sie in der Registrierung unter den folgenden Pfaden:</span><span class="sxs-lookup"><span data-stu-id="d15cf-738">To find the canonical name of a Control Panel item not listed here, look in the registry under these paths:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

<span data-ttu-id="d15cf-739">Weitere Informationen, die Ihnen helfen können, die erforderlichen CLSIDs zu ermitteln, finden Sie unter [Registrieren von ausführbaren System Steuerungselementen](how-to-register-an-executable-control-panel-item-registration-.md) und [Registrieren von dll-System Steuerungselementen](how-to-register-dll-control-panel-item-registration-.md).</span><span class="sxs-lookup"><span data-stu-id="d15cf-739">For more information that can help you discover the necessary CLSIDs, see [How to Register Executable Control Panel Items](how-to-register-an-executable-control-panel-item-registration-.md) and [How to Register DLL Control Panel Items](how-to-register-dll-control-panel-item-registration-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d15cf-740">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d15cf-740">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d15cf-741">Ausführen von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="d15cf-741">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="d15cf-742">**Iopencontrolpanel**</span><span class="sxs-lookup"><span data-stu-id="d15cf-742">**IOpenControlPanel**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



