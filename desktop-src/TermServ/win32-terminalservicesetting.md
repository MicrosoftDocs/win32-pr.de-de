---
title: Win32_TerminalServiceSetting-Klasse
description: Stellt die Konfiguration für einen Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) dar.
ms.assetid: 4cd047db-921f-4ccb-946b-d2c7b8d6beea
ms.tgt_platform: multiple
keywords:
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste
- Win32_TerminalServiceSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting.Caption
- Win32_TerminalServiceSetting.Description
- Win32_TerminalServiceSetting.InstallDate
- Win32_TerminalServiceSetting.Name
- Win32_TerminalServiceSetting.Status
- Win32_TerminalServiceSetting.ServerName
- Win32_TerminalServiceSetting.TerminalServerMode
- Win32_TerminalServiceSetting.GetCapabilitiesID
- Win32_TerminalServiceSetting.LicensingType
- Win32_TerminalServiceSetting.PolicySourceLicensingType
- Win32_TerminalServiceSetting.PossibleLicensingTypes
- Win32_TerminalServiceSetting.LicensingName
- Win32_TerminalServiceSetting.LicensingDescription
- Win32_TerminalServiceSetting.ActiveDesktop
- Win32_TerminalServiceSetting.UserPermission
- Win32_TerminalServiceSetting.DeleteTempFolders
- Win32_TerminalServiceSetting.PolicySourceDeleteTempFolders
- Win32_TerminalServiceSetting.UseTempFolders
- Win32_TerminalServiceSetting.PolicySourceUseTempFolders
- Win32_TerminalServiceSetting.AllowTSConnections
- Win32_TerminalServiceSetting.PolicySourceAllowTSConnections
- Win32_TerminalServiceSetting.SingleSession
- Win32_TerminalServiceSetting.PolicySourceSingleSession
- Win32_TerminalServiceSetting.ProfilePath
- Win32_TerminalServiceSetting.PolicySourceProfilePath
- Win32_TerminalServiceSetting.HomeDirectory
- Win32_TerminalServiceSetting.PolicySourceHomeDirectory
- Win32_TerminalServiceSetting.TimeZoneRedirection
- Win32_TerminalServiceSetting.PolicySourceTimeZoneRedirection
- Win32_TerminalServiceSetting.Logons
- Win32_TerminalServiceSetting.DirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceDirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceConfiguredLicenseServers
- Win32_TerminalServiceSetting.DisableForcibleLogoff
- Win32_TerminalServiceSetting.PolicySourceDisableForcibleLogoff
- Win32_TerminalServiceSetting.FallbackPrintDriverType
- Win32_TerminalServiceSetting.PolicySourceFallbackPrintDriverType
- Win32_TerminalServiceSetting.SessionBrokerDrainMode
- Win32_TerminalServiceSetting.LimitedUserSessions
- Win32_TerminalServiceSetting.EnableDFSS
- Win32_TerminalServiceSetting.PolicySourceEnableDFSS
- Win32_TerminalServiceSetting.EnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.PolicySourceEnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.EnableAutomaticReconnection
- Win32_TerminalServiceSetting.PolicySourceEnableAutomaticReconnection
- Win32_TerminalServiceSetting.UseRDEasyPrintDriver
- Win32_TerminalServiceSetting.PolicySourceUseRDEasyPrintDriver
- Win32_TerminalServiceSetting.RedirectSmartCards
- Win32_TerminalServiceSetting.PolicySourceRedirectSmartCards
- Win32_TerminalServiceSetting.EnableDiskFSS
- Win32_TerminalServiceSetting.EnableNetworkFSS
- Win32_TerminalServiceSetting.NetworkFSSUserSessionWeight
- Win32_TerminalServiceSetting.NetworkFSSLocalSystemWeight
- Win32_TerminalServiceSetting.NetworkFSSCatchAllWeight
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f02028a331a3688152a1ce8c57ada7269d07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341117"
---
# <a name="win32_terminalservicesetting-class"></a><span data-ttu-id="ab1de-105">Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="ab1de-105">Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="ab1de-106">Die **Win32 \_ terminalserviceseten** -WMI-Klasse stellt die Konfiguration für einen Remotedesktop-Sitzungshost Server (RD-Sitzungshost) dar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-106">The **Win32\_TerminalServiceSetting** WMI class represents the configuration for a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="ab1de-107">Zu den Einstellungen gehören Funktionen wie RD-Sitzungshost Server Modus, Lizenzierung, aktiver Desktop, Berechtigungen, Löschen temporärer Ordner und temporäre Verzeichnisse für Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="ab1de-107">Settings include capabilities such as RD Session Host server mode, licensing, Active Desktop, permissions, deletion of temporary folders, and temporary directories for sessions.</span></span>

<span data-ttu-id="ab1de-108">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="ab1de-108">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="ab1de-109">Referenzinformationen zu-Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="ab1de-109">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab1de-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab1de-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICESETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   ServerName;
  uint32   TerminalServerMode;
  uint32   GetCapabilitiesID;
  uint32   LicensingType;
  uint32   PolicySourceLicensingType;
  uint32   PossibleLicensingTypes;
  string   LicensingName;
  string   LicensingDescription;
  uint32   ActiveDesktop;
  uint32   UserPermission;
  uint32   DeleteTempFolders;
  uint32   PolicySourceDeleteTempFolders;
  uint32   UseTempFolders;
  uint32   PolicySourceUseTempFolders;
  uint32   AllowTSConnections;
  uint32   PolicySourceAllowTSConnections;
  uint32   SingleSession;
  uint32   PolicySourceSingleSession;
  string   ProfilePath;
  uint32   PolicySourceProfilePath;
  string   HomeDirectory;
  uint32   PolicySourceHomeDirectory;
  uint32   TimeZoneRedirection;
  uint32   PolicySourceTimeZoneRedirection;
  string   Logons;
  string   DirectConnectLicenseServers;
  uint32   PolicySourceDirectConnectLicenseServers;
  uint32   PolicySourceConfiguredLicenseServers;
  uint32   DisableForcibleLogoff;
  uint32   PolicySourceDisableForcibleLogoff;
  uint32   FallbackPrintDriverType;
  uint32   PolicySourceFallbackPrintDriverType;
  uint32   SessionBrokerDrainMode;
  uint32   LimitedUserSessions;
  uint32   EnableDFSS;
  uint32   PolicySourceEnableDFSS;
  uint32   EnableRemoteDesktopMSI;
  uint32   PolicySourceEnableRemoteDesktopMSI;
  uint32   EnableAutomaticReconnection;
  uint32   PolicySourceEnableAutomaticReconnection;
  uint32   UseRDEasyPrintDriver;
  uint32   PolicySourceUseRDEasyPrintDriver;
  uint32   RedirectSmartCards;
  uint32   PolicySourceRedirectSmartCards;
  uint32   EnableDiskFSS;
  uint32   EnableNetworkFSS;
  uint32   NetworkFSSUserSessionWeight;
  uint32   NetworkFSSLocalSystemWeight;
  uint32   NetworkFSSCatchAllWeight;
};
```

## <a name="members"></a><span data-ttu-id="ab1de-111">Member</span><span class="sxs-lookup"><span data-stu-id="ab1de-111">Members</span></span>

<span data-ttu-id="ab1de-112">Die **Win32 \_ terminalservicesetts** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ab1de-112">The **Win32\_TerminalServiceSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="ab1de-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="ab1de-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="ab1de-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab1de-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ab1de-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="ab1de-115">Methods</span></span>

<span data-ttu-id="ab1de-116">Die **Win32 \_ terminalservicesetts** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ab1de-116">The **Win32\_TerminalServiceSetting** class has these methods.</span></span>



| <span data-ttu-id="ab1de-117">Methode</span><span class="sxs-lookup"><span data-stu-id="ab1de-117">Method</span></span>                                                                                                                | <span data-ttu-id="ab1de-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab1de-118">Description</span></span>                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab1de-119">**Adddirectconnectlicenseserver**</span><span class="sxs-lookup"><span data-stu-id="ab1de-119">**AddDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | <span data-ttu-id="ab1de-120">Konfiguriert einen neuen Lizenzserver im Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="ab1de-120">Configures a new license server in the enterprise.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="ab1de-121">**Addlstospecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="ab1de-121">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | <span data-ttu-id="ab1de-122">Fügt den angegebenen Lizenzserver am Ende der Liste der angegebenen Lizenzserver hinzu.</span><span class="sxs-lookup"><span data-stu-id="ab1de-122">Adds the given license server to the end of the list of specified license servers.</span></span><br/>                                                                                  |
| [<span data-ttu-id="ab1de-123">**Canaccesslicenseserver**</span><span class="sxs-lookup"><span data-stu-id="ab1de-123">**CanAccessLicenseServer**</span></span>](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | <span data-ttu-id="ab1de-124">Bestimmt, ob auf dem RD-Sitzungshost Server Remotedesktopdienste Client Zugriffs Lizenzen (RDS-CALs) von einem Remotedesktop Lizenzserver angefordert werden können.</span><span class="sxs-lookup"><span data-stu-id="ab1de-124">Determines whether the RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="ab1de-125">**ChangeMode**</span><span class="sxs-lookup"><span data-stu-id="ab1de-125">**ChangeMode**</span></span>](win32-terminalservicesetting-changemode.md)                                                         | <span data-ttu-id="ab1de-126">Legt den Lizenztyp des Remotedesktop Lizenzservers fest.</span><span class="sxs-lookup"><span data-stu-id="ab1de-126">Sets the licensing type of the Remote Desktop license server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="ab1de-127">**"Kreatewinstation"**</span><span class="sxs-lookup"><span data-stu-id="ab1de-127">**CreateWinstation**</span></span>](createwinstation-win32-terminalservicesetting.md)                                             | <span data-ttu-id="ab1de-128">Erstellt einen neuen listenerstapel auf der Grundlage der eindeutigen Kombination aus Listenername und NIC.</span><span class="sxs-lookup"><span data-stu-id="ab1de-128">Creates a new listener stack based on the unique combination of listener name and NIC.</span></span><br/>                                                                              |
| [<span data-ttu-id="ab1de-129">**Deletedirectconnectlicenseserver**</span><span class="sxs-lookup"><span data-stu-id="ab1de-129">**DeleteDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | <span data-ttu-id="ab1de-130">Löscht den angegebenen Lizenzserver aus dem Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="ab1de-130">Deletes the specified license server from the enterprise.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="ab1de-131">**Emptyspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="ab1de-131">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | <span data-ttu-id="ab1de-132">Entfernt alle Lizenzserver aus der Liste der angegebenen Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="ab1de-132">Removes all license servers from the list of specified license servers.</span></span><br/>                                                                                             |
| [<span data-ttu-id="ab1de-133">**Findlicenseservers**</span><span class="sxs-lookup"><span data-stu-id="ab1de-133">**FindLicenseServers**</span></span>](findlicenseservers-win32-terminalservicesetting.md)                                         | <span data-ttu-id="ab1de-134">Listet alle Remotedesktop Lizenzserver und die Ermittlungsmethode auf.</span><span class="sxs-lookup"><span data-stu-id="ab1de-134">Enumerates all of the Remote Desktop license servers and the method of discovery.</span></span><br/>                                                                                   |
| [<span data-ttu-id="ab1de-135">**GetDomain**</span><span class="sxs-lookup"><span data-stu-id="ab1de-135">**GetDomain**</span></span>](getdomain-win32-terminalservicesetting.md)                                                           | <span data-ttu-id="ab1de-136">Ruft den Namen der Domäne ab, der der RD-Sitzungshost Server angehört.</span><span class="sxs-lookup"><span data-stu-id="ab1de-136">Retrieves the name of the domain that the RD Session Host server is a member of.</span></span><br/>                                                                                    |
| [<span data-ttu-id="ab1de-137">**Getgraceperioddays**</span><span class="sxs-lookup"><span data-stu-id="ab1de-137">**GetGracePeriodDays**</span></span>](getgraceperioddays-win32-terminalservicesetting.md)                                         | <span data-ttu-id="ab1de-138">Ruft die Anzahl der Tage ab, die in der RD-Lizenzierung Toleranz Periode für einen RD-Sitzungshost Server verbleiben.</span><span class="sxs-lookup"><span data-stu-id="ab1de-138">Retrieves the number of days that are remaining in the RD Licensing grace period for an RD Session Host server.</span></span><br/>                                                     |
| [<span data-ttu-id="ab1de-139">**Getregisteredlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="ab1de-139">**GetRegisteredLicenseServerList**</span></span>](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | <span data-ttu-id="ab1de-140">Ruft die Liste der registrierten Lizenzserver ab.</span><span class="sxs-lookup"><span data-stu-id="ab1de-140">Gets the list of registered license servers.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="ab1de-141">**Getspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="ab1de-141">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="ab1de-142">Ruft die Liste der angegebenen Lizenzserver ab.</span><span class="sxs-lookup"><span data-stu-id="ab1de-142">Retrieves the list of specified license servers.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="ab1de-143">**Gettslanaids**</span><span class="sxs-lookup"><span data-stu-id="ab1de-143">**GetTSLanaIds**</span></span>](gettslanaids-win32-terminalservicesetting.md)                                                     | <span data-ttu-id="ab1de-144">Ruft die IDs und Beschreibungen Remotedesktopdienste Netzwerkadapter ab.</span><span class="sxs-lookup"><span data-stu-id="ab1de-144">Gets the IDs and descriptions of Remote Desktop Services network adapters.</span></span><br/>                                                                                          |
| [<span data-ttu-id="ab1de-145">**Gettstolsconnectivitystatus**</span><span class="sxs-lookup"><span data-stu-id="ab1de-145">**GetTStoLSConnectivityStatus**</span></span>](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | <span data-ttu-id="ab1de-146">Bestimmt den Konnektivitätsstatus zwischen Remotedesktopdienste und einem Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="ab1de-146">Determines the connectivity status between Remote Desktop Services and a license server.</span></span><br/>                                                                            |
| [<span data-ttu-id="ab1de-147">**Getwinstationdrivernames**</span><span class="sxs-lookup"><span data-stu-id="ab1de-147">**GetWinstationDriverNames**</span></span>](getwinstationdrivernames-win32-terminalservicesetting.md)                             | <span data-ttu-id="ab1de-148">Ruft eine Liste der Namen von WinStation-Treibern ab.</span><span class="sxs-lookup"><span data-stu-id="ab1de-148">Retrieves a list of Winstation driver names.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="ab1de-149">**Pinglicenseserver**</span><span class="sxs-lookup"><span data-stu-id="ab1de-149">**PingLicenseServer**</span></span>](pinglicenseserver-win32-terminalservicesetting.md)                                           | <span data-ttu-id="ab1de-150">Pings an den Lizenzserver, um zu bestimmen, ob es sich um einen gültigen Lizenzserver handelt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-150">Pings the license server to determine whether it is a valid license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="ab1de-151">**Removelsfromspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="ab1de-151">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | <span data-ttu-id="ab1de-152">Entfernt den angegebenen Lizenzserver aus der Liste der angegebenen Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="ab1de-152">Removes the given license server from the list of specified license servers.</span></span><br/>                                                                                        |
| [<span data-ttu-id="ab1de-153">**"Aballow-Connections"**</span><span class="sxs-lookup"><span data-stu-id="ab1de-153">**SetAllowTSConnections**</span></span>](win32-terminalservicesetting-setallowtsconnections.md)                                   | <span data-ttu-id="ab1de-154">Legt die **allowtconnections** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="ab1de-154">Sets the **AllowTSConnections** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="ab1de-155">**Setdisableforciblelogoff**</span><span class="sxs-lookup"><span data-stu-id="ab1de-155">**SetDisableForcibleLogoff**</span></span>](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | <span data-ttu-id="ab1de-156">Legt die **disablezwangs blelogoff** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="ab1de-156">Sets the **DisableForcibleLogoff** property.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="ab1de-157">**Setfallbackprintdrivertype**</span><span class="sxs-lookup"><span data-stu-id="ab1de-157">**SetFallbackPrintDriverType**</span></span>](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | <span data-ttu-id="ab1de-158">Legt die **fallbackprintdrivertype** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="ab1de-158">Sets the **FallbackPrintDriverType** property.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="ab1de-159">**Verzeichnis ""**</span><span class="sxs-lookup"><span data-stu-id="ab1de-159">**SetHomeDirectory**</span></span>](win32-terminalservicesetting-sethomedirectory.md)                                             | <span data-ttu-id="ab1de-160">Legt die **Homedirectory** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="ab1de-160">Sets the **HomeDirectory** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="ab1de-161">**Setpolicypropertyname**</span><span class="sxs-lookup"><span data-stu-id="ab1de-161">**SetPolicyPropertyName**</span></span>](win32-terminalservicesetting-setpolicypropertyname.md)                                   | <span data-ttu-id="ab1de-162">Legt eine der folgenden Eigenschaften fest: **deletetempfolders** oder **usetempfolders**.</span><span class="sxs-lookup"><span data-stu-id="ab1de-162">Sets one of the following properties: **DeleteTempFolders** or **UseTempFolders**.</span></span><br/>                                                                                  |
| [<span data-ttu-id="ab1de-163">**Setprimarylicenseserver**</span><span class="sxs-lookup"><span data-stu-id="ab1de-163">**SetPrimaryLicenseServer**</span></span>](setprimarylicenseserver-win32-terminalservicesetting.md)                               | <span data-ttu-id="ab1de-164">Legt den angegebenen Lizenzserver als ersten Eintrag in der Liste der angegebenen Lizenzserver fest.</span><span class="sxs-lookup"><span data-stu-id="ab1de-164">Sets the given license server as the first entry in the list of specified license servers.</span></span><br/>                                                                          |
| [<span data-ttu-id="ab1de-165">**Setprofilepath**</span><span class="sxs-lookup"><span data-stu-id="ab1de-165">**SetProfilePath**</span></span>](win32-terminalservicesetting-setprofilepath.md)                                                 | <span data-ttu-id="ab1de-166">Legt die **ProfilePath** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="ab1de-166">Sets the **ProfilePath** property.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="ab1de-167">**Setsinglesession**</span><span class="sxs-lookup"><span data-stu-id="ab1de-167">**SetSingleSession**</span></span>](win32-terminalservicesetting-setsinglesession.md)                                             | <span data-ttu-id="ab1de-168">Legt die **SingleSession** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="ab1de-168">Sets the **SingleSession** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="ab1de-169">**Setspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="ab1de-169">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="ab1de-170">Aktualisiert die Liste der angegebenen Lizenzserver, wobei alle vorhandenen angegebenen Lizenzserver ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="ab1de-170">Updates the list of specified license servers, replacing any existing specified license servers.</span></span><br/>                                                                    |
| [<span data-ttu-id="ab1de-171">**Settimezoneredirection**</span><span class="sxs-lookup"><span data-stu-id="ab1de-171">**SetTimeZoneRedirection**</span></span>](win32-terminalservicesetting-settimezoneredirection.md)                                 | <span data-ttu-id="ab1de-172">Legt die **timezoneredirection** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="ab1de-172">Sets the **TimeZoneRedirection** property.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="ab1de-173">**Updatedirectconnectlicenseserver**</span><span class="sxs-lookup"><span data-stu-id="ab1de-173">**UpdateDirectConnectLicenseServer**</span></span>](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | <span data-ttu-id="ab1de-174">Aktualisiert die Liste der Discovery-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="ab1de-174">Updates the list of discovery license servers.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="ab1de-175">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab1de-175">Properties</span></span>

<span data-ttu-id="ab1de-176">Die **Win32 \_ terminalservicesetts** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ab1de-176">The **Win32\_TerminalServiceSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab1de-177">**Activedesktop**</span><span class="sxs-lookup"><span data-stu-id="ab1de-177">**ActiveDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-178">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-179">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-180">Gibt an, ob Active Desktop in jeder Benutzersitzung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="ab1de-180">Specifies whether Active Desktop is allowed in each user session.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ab1de-181"><span id="TRUE"></span><span id="true"></span>**True** (0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-181"><span id="TRUE"></span><span id="true"></span>**TRUE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-182">Active Desktop ist in jeder Benutzersitzung nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ab1de-182">Active Desktop is not allowed in each user session.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ab1de-183"><span id="FALSE"></span><span id="false"></span>**False** (1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-183"><span id="FALSE"></span><span id="false"></span>**FALSE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-184">Aktiver Desktop ist in jeder Benutzersitzung zulässig.</span><span class="sxs-lookup"><span data-stu-id="ab1de-184">Active Desktop is allowed in each user session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-185">**Allow-connections**</span><span class="sxs-lookup"><span data-stu-id="ab1de-185">**AllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-186">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-188">Gibt an, ob neue Remotedesktopdienste Verbindungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ab1de-188">Specifies whether new Remote Desktop Services connections are allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ab1de-189"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-189"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-190">Neue Verbindungen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ab1de-190">New connections are not allowed.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ab1de-191"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-191"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-192">Neue Verbindungen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="ab1de-192">New connections are allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-193">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ab1de-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab1de-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-196">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ab1de-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-197">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ab1de-197">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="ab1de-198">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-199">**Deletetempfolders**</span><span class="sxs-lookup"><span data-stu-id="ab1de-199">**DeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-200">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-202">Gibt an, ob temporäre Verzeichnisse beim Beenden gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="ab1de-202">Specifies whether temporary directories are deleted on exit.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ab1de-203"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-204">Das Löschen temporärer Verzeichnisse ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-204">Deletion of temporary directories is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ab1de-205"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-206">Das Löschen temporärer Verzeichnisse ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-206">Deletion of temporary directories is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-207">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab1de-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab1de-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-210">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ab1de-210">Description of the object.</span></span>

<span data-ttu-id="ab1de-211">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-211">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-212">**DirectConnectLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="ab1de-212">**DirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab1de-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-215">Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ab1de-215">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-216">Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-216">This property is not available.</span></span>

<span data-ttu-id="ab1de-217">**Windows Server 2008:** Listet die Lizenzserver auf.</span><span class="sxs-lookup"><span data-stu-id="ab1de-217">**Windows Server 2008:** Enumerates the list of license servers.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-218">**Disableforciblelogoff**</span><span class="sxs-lookup"><span data-stu-id="ab1de-218">**DisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-219">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-219">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-221">Bestimmt, ob ein Administrator, der bei der Konsole angemeldet ist, erzwungen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ab1de-221">Determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span data-ttu-id="ab1de-222">0</span><span class="sxs-lookup"><span data-stu-id="ab1de-222">0</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-223">Der Administrator kann erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="ab1de-223">Administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-224">1</span><span class="sxs-lookup"><span data-stu-id="ab1de-224">1</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-225">Der Administrator kann nicht erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="ab1de-225">Administrator cannot be forcibly logged off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-226">**Enableautomatikreconnection**</span><span class="sxs-lookup"><span data-stu-id="ab1de-226">**EnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-227">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-228">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-229">Gibt an, ob Remotedesktop Verbindungs Clients die automatische erneute Verbindung mit Sitzungen auf einem RD-Sitzungshost Server zulassen, wenn die Netzwerkverbindung vorübergehend unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-229">Specifies whether to allow Remote Desktop connection clients to automatically reconnect to sessions on an RD Session Host server if the network link is temporarily lost.</span></span>

<dt>

<span data-ttu-id="ab1de-230">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-230">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-231">Das automatische erneute Herstellen der Verbindung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-231">Automatic reconnection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-232">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-232">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-233">Die automatische erneute Verbindungs Herstellung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-233">Automatic reconnection is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="ab1de-234">**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-234">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-235">**Enabledfss**</span><span class="sxs-lookup"><span data-stu-id="ab1de-235">**EnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-236">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-237">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-238">Gibt an, ob Dynamic Fair-Share Scheduling (DfSS) aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ab1de-238">Indicates whether dynamic fair-share scheduling (DFSS) is enabled or disabled.</span></span> <span data-ttu-id="ab1de-239">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="ab1de-239">This can be one of the following values.</span></span>

<span data-ttu-id="ab1de-240">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-240">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="ab1de-241">0</span><span class="sxs-lookup"><span data-stu-id="ab1de-241">0</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-242">DFSS ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-242">DFSS is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-243">1</span><span class="sxs-lookup"><span data-stu-id="ab1de-243">1</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-244">DFSS ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-244">DFSS is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-245">**Enablediskf**</span><span class="sxs-lookup"><span data-stu-id="ab1de-245">**EnableDiskFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-246">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-247">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-247">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-248">Gibt an, ob die Zeitplanung für die gleichmäßige Datenträger-</span><span class="sxs-lookup"><span data-stu-id="ab1de-248">Specifies if disk fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="ab1de-249">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-249">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-250">Die Datenträger-planmäßige Freigabe Planung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-250">Disk fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-251">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-251">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-252">Die gemeinsame Nutzung von Datenträger Plänen ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-252">Disk fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="ab1de-253">**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-253">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-254">**Enablenetworkf**</span><span class="sxs-lookup"><span data-stu-id="ab1de-254">**EnableNetworkFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-255">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-256">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-256">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-257">Gibt an, ob die Planung der Netzwerk gerechten Freigabe aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ab1de-257">Specifies if network fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="ab1de-258">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-258">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-259">Die Planung der Netzwerk gerechten Freigabe ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-259">Network fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-260">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-260">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-261">Die Planung der Netzwerk gerechten Freigabe ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-261">Network fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="ab1de-262">**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-262">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-263">**Enableremotedesktopmsi**</span><span class="sxs-lookup"><span data-stu-id="ab1de-263">**EnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-264">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-265">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-266">Gibt an, ob die Remotedesktop-MSI aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ab1de-266">Indicates whether the Remote Desktop MSI is enabled or disabled.</span></span>

<dt>

<span data-ttu-id="ab1de-267">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-267">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-268">Disabled</span><span class="sxs-lookup"><span data-stu-id="ab1de-268">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-269">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-269">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-270">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="ab1de-270">Enabled</span></span>

</dd> </dl>

<span data-ttu-id="ab1de-271">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-271">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-272">**Fallbackprintdrivertype**</span><span class="sxs-lookup"><span data-stu-id="ab1de-272">**FallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-273">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-275">Gibt an, auf welchen Druckertreiber ein Fall Back durch ein Fall Back</span><span class="sxs-lookup"><span data-stu-id="ab1de-275">Specifies which printer driver to fallback to.</span></span>

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span data-ttu-id="ab1de-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**Keine Fall Back-dirvers = 0** (0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**No fallback dirvers=0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-277">Keine Fall Back Treiber.</span><span class="sxs-lookup"><span data-stu-id="ab1de-277">No fallback drivers.</span></span>

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span data-ttu-id="ab1de-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Beste Vermutung = 1** (1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Best guess=1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-279">Beste Schätzung.</span><span class="sxs-lookup"><span data-stu-id="ab1de-279">Best guess.</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span data-ttu-id="ab1de-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Beste Schätzung, wenn keine Entsprechung für die PCL gefunden wird = 2** (2)</span><span class="sxs-lookup"><span data-stu-id="ab1de-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Best guess, if no match is found fallback to PCL=2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-281">Beste Schätzung.</span><span class="sxs-lookup"><span data-stu-id="ab1de-281">Best guess.</span></span> <span data-ttu-id="ab1de-282">Wenn keine Entsprechung gefunden wird, Fall Back auf Hewlett-Packard-druckersteuerungsprache (PCL).</span><span class="sxs-lookup"><span data-stu-id="ab1de-282">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span data-ttu-id="ab1de-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Beste Schätzung, wenn keine Entsprechung gefunden wird, Fall Back auf PS = 3** (3)</span><span class="sxs-lookup"><span data-stu-id="ab1de-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Best guess, if no match is found fallback to PS=3** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-284">Beste Schätzung.</span><span class="sxs-lookup"><span data-stu-id="ab1de-284">Best guess.</span></span> <span data-ttu-id="ab1de-285">Wenn keine Entsprechung gefunden wird, Fall Back auf PostScript (PS).</span><span class="sxs-lookup"><span data-stu-id="ab1de-285">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span data-ttu-id="ab1de-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Wenn keine Entsprechung gefunden wird, wird empfohlen, sowohl PCL-als auch PS-Treiber = 4** (4) anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ab1de-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Best guess, if no match is found show both PCL and PS drivers=4** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-287">Beste Schätzung.</span><span class="sxs-lookup"><span data-stu-id="ab1de-287">Best guess.</span></span> <span data-ttu-id="ab1de-288">Wenn keine Entsprechung gefunden wird, zeigen Sie sowohl PS-als auch PCL-Treiber an.</span><span class="sxs-lookup"><span data-stu-id="ab1de-288">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-289">**Getcapabilitiesid**</span><span class="sxs-lookup"><span data-stu-id="ab1de-289">**GetCapabilitiesID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-290">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-292">Die Funktions-ID für den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="ab1de-292">Capabilities ID for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-293">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="ab1de-293">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-294">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab1de-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-296">Das Stammverzeichnis für den Computer.</span><span class="sxs-lookup"><span data-stu-id="ab1de-296">The root directory for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ab1de-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-298">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ab1de-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-300">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="ab1de-300">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-301">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ab1de-301">The date the object was installed.</span></span> <span data-ttu-id="ab1de-302">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab1de-302">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ab1de-303">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-304">**Licensingdescription**</span><span class="sxs-lookup"><span data-stu-id="ab1de-304">**LicensingDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-305">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab1de-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-307">Eine kurze Beschreibung des Lizenzierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="ab1de-307">A brief description of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-308">**Licensingname**</span><span class="sxs-lookup"><span data-stu-id="ab1de-308">**LicensingName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-309">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab1de-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-311">Der Name des Lizenzierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="ab1de-311">The name of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-312">**LicensingType**</span><span class="sxs-lookup"><span data-stu-id="ab1de-312">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-313">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-315">Der Lizenzierungstyp für den angegebenen Server Modus.</span><span class="sxs-lookup"><span data-stu-id="ab1de-315">The licensing type for the specified server mode.</span></span>

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span data-ttu-id="ab1de-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Persönlicher Terminal Server** (0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Personal Terminal Server** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-317">Persönlicher RD-Sitzungshost Server.</span><span class="sxs-lookup"><span data-stu-id="ab1de-317">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span data-ttu-id="ab1de-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Remotedesktop für die Verwaltung** (1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Remote Desktop for Administration** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-319">Remotedesktop für die Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="ab1de-319">Remote Desktop for Administration.</span></span>

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="ab1de-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Pro Gerät** (2)</span><span class="sxs-lookup"><span data-stu-id="ab1de-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Per Device** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-321">Pro Gerät.</span><span class="sxs-lookup"><span data-stu-id="ab1de-321">Per Device.</span></span> <span data-ttu-id="ab1de-322">Gültig für Anwendungsserver.</span><span class="sxs-lookup"><span data-stu-id="ab1de-322">Valid for application servers.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="ab1de-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Pro Benutzer** (3)</span><span class="sxs-lookup"><span data-stu-id="ab1de-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-324">Pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="ab1de-324">Per User.</span></span> <span data-ttu-id="ab1de-325">Gültig für Anwendungsserver.</span><span class="sxs-lookup"><span data-stu-id="ab1de-325">Valid for application servers.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ab1de-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (4)</span><span class="sxs-lookup"><span data-stu-id="ab1de-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-327">Nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-327">Not Configured.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-328">**Limitedusersessions**</span><span class="sxs-lookup"><span data-stu-id="ab1de-328">**LimitedUserSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-329">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-330">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-330">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-331">Gibt an, ob die Funktion zum Begrenzen der Anzahl aktiver und inaktiver Sitzungen, die auf einem RD-Sitzungshost Server zulässig sind, aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ab1de-331">Indicates whether the feature to limit the number of both active and inactive sessions that are allowed on an RD Session Host server is enabled.</span></span> <span data-ttu-id="ab1de-332">Beispielsweise können Sie " **limitedusersessions** " festlegen, um die Lizenz Konformität für eine bestimmte Anwendung zu gewährleisten, die auf dem RD-Sitzungshost Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab1de-332">For example, you may want to set **LimitedUserSessions** to guarantee license compliance for a particular application that is installed on the RD Session Host server.</span></span> <span data-ttu-id="ab1de-333">Möglicherweise möchten Sie die maximale Anzahl von Sitzungen auf einem RD-Sitzungshost Server in einer Farm mit Lastenausgleich einschränken, damit der Server nicht überladen wird, wenn ein anderer Server in der Farm ausfällt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-333">Or, you may want to limit the maximum number of sessions on an RD Session Host server in a load-balanced farm so that the server will not be overloaded if another server in the farm fails.</span></span>

> [!Note]
>
> <span data-ttu-id="ab1de-334">Die Sitzung, die zum Herstellen einer Verbindung mit dem Server zu Verwaltungszwecken verwendet wird, wird von " **limitedusersessions**" nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-334">The session that is used to connect to the server for administrative purposes is not affected by **LimitedUserSessions**.</span></span>
>
> <span data-ttu-id="ab1de-335">Wenn ein Benutzer in einer RD-Sitzungshost Serverfarm das Sitzungs Limit überschreitet, wird die Sitzung durch RD-Verbindungsbroker Lastenausgleich an einen anderen Server weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="ab1de-335">In an RD Session Host server farm, if a user exceeds the session limit, the session will be directed to another server by RD Connection Broker load balancing.</span></span> <span data-ttu-id="ab1de-336">Wenn es sich bei dem Server um einen eigenständigen Server handelt, ist der Benutzer nicht in der Lage, eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="ab1de-336">If the server is a stand-alone server, the user will not be able to connect.</span></span>
>
> <span data-ttu-id="ab1de-337">Aufgrund der Sitzung, die zum Herstellen einer Verbindung mit dem Server zu Verwaltungszwecken verwendet wird, und der zeitlichen Steuerung der Anzahl der Sitzungen während des Anmeldevorgangs wird empfohlen, dass Sie " **limitedusersessions** " auf einen Wert festlegen, der den physischen Grenzwert für die Anzahl der Sitzungen auf einem Server etwas niedriger ist.</span><span class="sxs-lookup"><span data-stu-id="ab1de-337">Because of the session that is used to connect to the server for administrative purposes, and the timing of the enforcement of the number of sessions during the logon cycle, it is recommended that you set **LimitedUserSessions** to a value that is slightly lower that the physical limit for the number of sessions on a server.</span></span>
>
> <span data-ttu-id="ab1de-338">Die **limitedusersessions** -Eigenschaft ist nur gültig, wenn der RD-Sitzungshost-Rollen Dienst installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab1de-338">The **LimitedUserSessions** property is only valid if the RD Session Host role service is installed.</span></span>

 

<dt>

<span data-ttu-id="ab1de-339">0</span><span class="sxs-lookup"><span data-stu-id="ab1de-339">0</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-340">Die Funktion ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-340">The feature is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-341">1 oder höher</span><span class="sxs-lookup"><span data-stu-id="ab1de-341">1 or greater</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-342">Der Wert 1 oder höher stellt die maximale Anzahl von Sitzungen (sowohl aktive als auch inaktive) dar, die auf dem RD-Sitzungshost Server zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ab1de-342">A value of one or greater represents the maximum number of sessions (both active and inactive) that are allowed on the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-343">**Anmeldungen**</span><span class="sxs-lookup"><span data-stu-id="ab1de-343">**Logons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-344">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab1de-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-345">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-345">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-346">Gibt an, ob neue Sitzungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ab1de-346">Specifies whether new sessions are allowed.</span></span> <span data-ttu-id="ab1de-347">Diese Einstellung wirkt sich nicht auf vorhandene Einstellungen aus.</span><span class="sxs-lookup"><span data-stu-id="ab1de-347">This setting does not affect existing settings.</span></span>

<dt>

<span data-ttu-id="ab1de-348">0</span><span class="sxs-lookup"><span data-stu-id="ab1de-348">0</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-349">Neue Sitzungen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="ab1de-349">New sessions are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-350">1</span><span class="sxs-lookup"><span data-stu-id="ab1de-350">1</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-351">Neue Sitzungen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ab1de-351">New sessions are not allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-352">**Name**</span><span class="sxs-lookup"><span data-stu-id="ab1de-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-353">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab1de-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-355">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ab1de-355">The name of the object.</span></span>

<span data-ttu-id="ab1de-356">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-357">**Networkf-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ab1de-357">**NetworkFSSCatchAllWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-358">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-359">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-359">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-360">Gibt die standardmäßige Netzwerk Last für den gesamten Netzwerk Datenverkehr an.</span><span class="sxs-lookup"><span data-stu-id="ab1de-360">Specifies the default network fair share weight for catch-all network traffic.</span></span> <span data-ttu-id="ab1de-361">Gültige Werte sind 1 bis 9.</span><span class="sxs-lookup"><span data-stu-id="ab1de-361">Valid values are 1 to 9.</span></span>

<span data-ttu-id="ab1de-362">**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-362">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-363">**Networkf-localsystemweight**</span><span class="sxs-lookup"><span data-stu-id="ab1de-363">**NetworkFSSLocalSystemWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-364">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-365">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-365">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-366">Gibt die standardmäßige Netzwerk Last für lokale System Prozesse an.</span><span class="sxs-lookup"><span data-stu-id="ab1de-366">Specifies the default network fair share weight for a local system processes.</span></span> <span data-ttu-id="ab1de-367">Gültige Werte sind 1 bis 9.</span><span class="sxs-lookup"><span data-stu-id="ab1de-367">Valid values are 1 to 9.</span></span>

<span data-ttu-id="ab1de-368">**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-368">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-369">**Networksssusersessionweight**</span><span class="sxs-lookup"><span data-stu-id="ab1de-369">**NetworkFSSUserSessionWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-370">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-371">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-371">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-372">Gibt die standardmäßige Netzwerk Last für eine Benutzersitzung an.</span><span class="sxs-lookup"><span data-stu-id="ab1de-372">Specifies the default network fair share weight for a user session.</span></span> <span data-ttu-id="ab1de-373">Gültige Werte sind 1 bis 9.</span><span class="sxs-lookup"><span data-stu-id="ab1de-373">Valid values are 1 to 9.</span></span>

<span data-ttu-id="ab1de-374">**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-374">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-375">**Policysourceallow-Connections**</span><span class="sxs-lookup"><span data-stu-id="ab1de-375">**PolicySourceAllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-376">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-378">Gibt an, ob die **allowtconnections** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-378">Indicates whether the **AllowTSConnections** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-379">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-379">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-380">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-380">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-381">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-381">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-382">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-382">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-383">**Policysourceconfiguredlicenseservers**</span><span class="sxs-lookup"><span data-stu-id="ab1de-383">**PolicySourceConfiguredLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-384">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-384">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-385">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-386">Gibt an, ob die von der [**getspecifiedlicenseserverlist**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) -Methode zurückgegebenen Lizenzserver vom Server oder von der Gruppenrichtlinie konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ab1de-386">Indicates whether the license servers returned by the [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) method are configured by the server or by group policy.</span></span>

<span data-ttu-id="ab1de-387">**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-387">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="ab1de-388">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-388">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-389">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-389">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-390">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-390">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-391">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-391">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-392">**Policysourcedeletetempfolders**</span><span class="sxs-lookup"><span data-stu-id="ab1de-392">**PolicySourceDeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-393">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-395">Gibt an, ob die **deletetempfolders** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-395">Indicates whether the **DeleteTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-396">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-396">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-397">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-397">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-398">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-398">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-399">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-399">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-400">**PolicySourceDirectConnectLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="ab1de-400">**PolicySourceDirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-401">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-401">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-403">Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ab1de-403">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-404">Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-404">This property is not available.</span></span>

<span data-ttu-id="ab1de-405">**Windows Server 2008:** Gibt an, ob die **DirectConnectLicenseServers** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-405">**Windows Server 2008:** Indicates whether the **DirectConnectLicenseServers** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-406">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-406">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-407">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-407">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-408">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-408">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-409">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-409">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-410">**Policysourcedisableforciblelogoff**</span><span class="sxs-lookup"><span data-stu-id="ab1de-410">**PolicySourceDisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-411">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-412">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-413">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-413">This property is not supported.</span></span>

<span data-ttu-id="ab1de-414">**Windows Server 2008:** Bestimmt, ob die **disableforciblelogoff** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-414">**Windows Server 2008:** Determines whether the **DisableForcibleLogoff** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-415">0</span><span class="sxs-lookup"><span data-stu-id="ab1de-415">0</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-416">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-416">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-417">1</span><span class="sxs-lookup"><span data-stu-id="ab1de-417">1</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-418">Gruppenrichtlinie:</span><span class="sxs-lookup"><span data-stu-id="ab1de-418">Group Policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-419">**Policysourceenableautomatikreconnection**</span><span class="sxs-lookup"><span data-stu-id="ab1de-419">**PolicySourceEnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-420">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-422">Gibt an, ob die **enableautomatikreconnection** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-422">Indicates whether the **EnableAutomaticReconnection** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-423">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-424">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-425">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-426">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-426">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="ab1de-427">**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-427">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-428">**Policysourceenabledfss**</span><span class="sxs-lookup"><span data-stu-id="ab1de-428">**PolicySourceEnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-429">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-431">Gibt an, ob die **enabledfss** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-431">Indicates whether the **EnableDFSS** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-432">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-432">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-433">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-433">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-434">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-434">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-435">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-435">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="ab1de-436">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-436">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-437">**Policysourceenableremotedesktopmsi**</span><span class="sxs-lookup"><span data-stu-id="ab1de-437">**PolicySourceEnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-438">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-439">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-440">Gibt an, ob die **enableremotedesktopmsi** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-440">Indicates whether the **EnableRemoteDesktopMSI** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-441">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-441">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-442">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-442">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-443">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-443">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-444">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-444">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="ab1de-445">**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-445">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-446">**Policysourcefallbackprintdrivertype**</span><span class="sxs-lookup"><span data-stu-id="ab1de-446">**PolicySourceFallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-447">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-447">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-448">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-449">Gibt an, ob die **fallbackprintdrivertype** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-449">Indicates whether the **FallbackPrintDriverType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-450">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-450">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-451">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-451">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-452">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-452">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-453">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-453">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-454">**Policysourcehomedirectory**</span><span class="sxs-lookup"><span data-stu-id="ab1de-454">**PolicySourceHomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-455">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-455">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-456">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-457">Gibt an, ob die **Homedirectory** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-457">Indicates whether the **HomeDirectory** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-458">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-458">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-459">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-459">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-460">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-460">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-461">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-461">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-462">**PolicySourceLicensingType**</span><span class="sxs-lookup"><span data-stu-id="ab1de-462">**PolicySourceLicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-463">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-464">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-465">Gibt an, ob die **LicensingType** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-465">Indicates whether the **LicensingType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-466">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-466">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-467">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-467">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-468">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-468">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-469">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-469">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-470">**PolicySourceProfilePath**</span><span class="sxs-lookup"><span data-stu-id="ab1de-470">**PolicySourceProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-471">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-473">Gibt an, ob die **ProfilePath** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-473">Indicates whether the **ProfilePath** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-474">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-474">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-475">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-475">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-476">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-476">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-477">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-477">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-478">**Policysourceredirec\martcards**</span><span class="sxs-lookup"><span data-stu-id="ab1de-478">**PolicySourceRedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-479">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-479">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-480">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-481">Gibt an, ob die **redirectmartcards** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-481">Indicates whether the **RedirectSmartCards** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-482">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-482">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-483">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-483">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-484">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-484">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-485">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-485">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="ab1de-486">**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-486">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-487">**PolicySourceSingleSession**</span><span class="sxs-lookup"><span data-stu-id="ab1de-487">**PolicySourceSingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-488">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-489">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-490">Gibt an, ob die **SingleSession** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-490">Indicates whether the property **SingleSession** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-491">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-491">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-492">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-492">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-493">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-493">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-494">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-494">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-495">**Policysourcetimezoneredirection**</span><span class="sxs-lookup"><span data-stu-id="ab1de-495">**PolicySourceTimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-496">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-497">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-498">Gibt an, ob die **timezoneredirection** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-498">Indicates whether the property **TimeZoneRedirection** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-499">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-499">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-500">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-500">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-501">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-501">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-502">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-502">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-503">**Policysourceuserdecoasyprintdriver**</span><span class="sxs-lookup"><span data-stu-id="ab1de-503">**PolicySourceUseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-504">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-505">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-506">Gibt an, ob die **userenasyprintdriver** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-506">Indicates whether the **UseRDEasyPrintDriver** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-507">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-507">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-508">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-508">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-509">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-509">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-510">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-510">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="ab1de-511">**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-511">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-512">**Policysourceu-tempfolders**</span><span class="sxs-lookup"><span data-stu-id="ab1de-512">**PolicySourceUseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-513">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-513">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-514">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-515">Gibt an, ob die **usetempfolders** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-515">Indicates whether the **UseTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="ab1de-516">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-516">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-517">Server</span><span class="sxs-lookup"><span data-stu-id="ab1de-517">Server</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-518">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-518">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-519">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="ab1de-519">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-520">**Possiblelicensingtypes**</span><span class="sxs-lookup"><span data-stu-id="ab1de-520">**PossibleLicensingTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-521">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-522">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-523">Qualifizierer: [**Bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("persönlicher Terminal Server", "Remotedesktop für die Verwaltung", "pro Gerät", "pro Benutzer", "nicht konfiguriert")</span><span class="sxs-lookup"><span data-stu-id="ab1de-523">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("Personal Terminal Server", "Remote Desktop for Administration", "Per Device", "Per User", "Not Configured")</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-524">Eine Bitmaske, die die verfügbaren Lizenzierungs Typen angibt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-524">A bitmask that specifies the licensing types that are available.</span></span> <span data-ttu-id="ab1de-525">Dies kann eine Kombination aus einem oder mehreren der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="ab1de-525">This can be a combination of one or more of the following values.</span></span>

<dt>

<span data-ttu-id="ab1de-526">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-526">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-527">Persönliche RD-Sitzungshost Server-Lizenzen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-527">Personal RD Session Host server licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-528">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ab1de-528">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-529">Remotedesktop Lizenzen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-529">Remote Desktop licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-530">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="ab1de-530">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-531">Pro-Gerät-Lizenzen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-531">Per device licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-532">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="ab1de-532">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-533">Pro-Benutzer-Lizenzen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-533">Per user licenses are supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-534">**Profilpfad**</span><span class="sxs-lookup"><span data-stu-id="ab1de-534">**ProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-535">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab1de-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-536">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-537">Profilpfad für den Computer.</span><span class="sxs-lookup"><span data-stu-id="ab1de-537">Profile path for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-538">**Redirecrichmartcards**</span><span class="sxs-lookup"><span data-stu-id="ab1de-538">**RedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-539">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-540">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-540">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-541">Gibt an, ob die Umleitung von smartcardgeräten in einer Remote Sitzung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="ab1de-541">Specifies if redirection of smart card devices is allowed in a remote session.</span></span>

<dt>

<span data-ttu-id="ab1de-542">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-542">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-543">Eine Smartcard-Geräte Umleitung ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ab1de-543">Smart card device redirection is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-544">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-544">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-545">Eine Smartcard-Geräte Umleitung ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="ab1de-545">Smart card device redirection is allowed.</span></span>

</dd> </dl>

<span data-ttu-id="ab1de-546">**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-546">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-547">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="ab1de-547">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-548">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab1de-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-549">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-550">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ab1de-550">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-551">Der Name des RD-Sitzungshost Servers, dessen Eigenschaften von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="ab1de-551">Name of the RD Session Host server whose properties are of interest.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-552">**Sessionbrokerdrainmode**</span><span class="sxs-lookup"><span data-stu-id="ab1de-552">**SessionBrokerDrainMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-553">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-553">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-554">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-555">Der RD-Verbindungsbroker Benutzer Anmeldemodus.</span><span class="sxs-lookup"><span data-stu-id="ab1de-555">The RD Connection Broker user logon mode.</span></span>

<dt>

<span data-ttu-id="ab1de-556">0</span><span class="sxs-lookup"><span data-stu-id="ab1de-556">0</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-557">Lässt alle Verbindungen zu.</span><span class="sxs-lookup"><span data-stu-id="ab1de-557">Allow all connections.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-558">1</span><span class="sxs-lookup"><span data-stu-id="ab1de-558">1</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-559">Zulassen von erneuten Verbindungen, aber verhindern von neuen Anmeldungen, bis der Server neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-559">Allow reconnections, but prevent new logons until the server is restarted.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-560">2</span><span class="sxs-lookup"><span data-stu-id="ab1de-560">2</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-561">Lässt erneute Verbindungen zu, verhindert jedoch neue Anmeldungen.</span><span class="sxs-lookup"><span data-stu-id="ab1de-561">Allow reconnections, but prevent new logons.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-562">**SingleSession**</span><span class="sxs-lookup"><span data-stu-id="ab1de-562">**SingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-563">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-564">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-565">Gibt an, ob pro Benutzer eine oder mehrere Remotedesktopdienste Sitzungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ab1de-565">Specifies whether one or more Remote Desktop Services sessions are allowed per user.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="ab1de-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-567">Pro Benutzer ist mehr als eine Sitzung zulässig.</span><span class="sxs-lookup"><span data-stu-id="ab1de-567">More than one session is allowed per user.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="ab1de-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-569">Pro Benutzer ist nur eine Sitzung zulässig.</span><span class="sxs-lookup"><span data-stu-id="ab1de-569">Only one session is allowed per user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-570">**Status**</span><span class="sxs-lookup"><span data-stu-id="ab1de-570">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-571">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab1de-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-572">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-573">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="ab1de-573">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-574">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ab1de-574">Current status of the object.</span></span> <span data-ttu-id="ab1de-575">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ab1de-575">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ab1de-576">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="ab1de-576">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ab1de-577">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="ab1de-577">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ab1de-578">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab1de-578">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ab1de-579">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="ab1de-579">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ab1de-580">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-580">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="ab1de-581">("OK")</span><span class="sxs-lookup"><span data-stu-id="ab1de-581">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ab1de-582">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="ab1de-582">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ab1de-583">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="ab1de-583">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ab1de-584">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="ab1de-584">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ab1de-585">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ab1de-585">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ab1de-586">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="ab1de-586">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ab1de-587">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="ab1de-587">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ab1de-588">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="ab1de-588">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-589">**Terminalservermode**</span><span class="sxs-lookup"><span data-stu-id="ab1de-589">**TerminalServerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-590">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-591">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-592">Der RD-Sitzungshost Server-Betriebsmodus des Remotedesktopdienste Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="ab1de-592">The RD Session Host server operating mode of the Remote Desktop Services service.</span></span> <span data-ttu-id="ab1de-593">Dieser Modus steuert die anwendbaren Lizenzierungsrichtlinien und ob die Anwendungs Kompatibilitäts Features aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="ab1de-593">This mode controls the licensing policies that are applicable as well as whether application-compatibility features are enabled.</span></span>

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span data-ttu-id="ab1de-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**Appserver** (1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-595">Der Server fungiert als Anwendungsserver.</span><span class="sxs-lookup"><span data-stu-id="ab1de-595">The server operates as an application server.</span></span>

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span data-ttu-id="ab1de-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-597">Die Sitzung wird Remote verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ab1de-597">The session is administered remotely.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-598">**Timezoneredirection**</span><span class="sxs-lookup"><span data-stu-id="ab1de-598">**TimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-599">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-599">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-600">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-600">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-601">Gibt an, ob der Client Computer seine Zeitzoneneinstellungen an die Remotedesktopdienste Sitzung umleiten kann.</span><span class="sxs-lookup"><span data-stu-id="ab1de-601">Specifies whether the client computer can redirect its time zone settings to the Remote Desktop Services session.</span></span>

<dt>

<span data-ttu-id="ab1de-602">0</span><span class="sxs-lookup"><span data-stu-id="ab1de-602">0</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-603">Die Umleitung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-603">Redirection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-604">1</span><span class="sxs-lookup"><span data-stu-id="ab1de-604">1</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-605">Die Umleitung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-605">Redirection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-606">**Userdebug PrintDriver**</span><span class="sxs-lookup"><span data-stu-id="ab1de-606">**UseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-607">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-607">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-608">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-608">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-609">Gibt an, ob der Easy Print für Remotedesktop Druckertreiber zuerst zum Installieren aller Client Drucker verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-609">Specifies whether the Remote Desktop Easy Print printer driver is used first to install all client printers.</span></span>

<dt>

<span data-ttu-id="ab1de-610">0</span><span class="sxs-lookup"><span data-stu-id="ab1de-610">0</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-611">Der RD-Sitzungshost Server versucht, einen geeigneten Druckertreiber zu finden, um den Client Drucker zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ab1de-611">The RD Session Host server tries to find a suitable printer driver to install the client printer.</span></span> <span data-ttu-id="ab1de-612">Wenn der RD-Sitzungshost Server keinen Druckertreiber hat, der mit dem Client Drucker übereinstimmt, versucht der Server, den-Easy Print für Remotedesktop Treiber zu verwenden, um den Client Drucker zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ab1de-612">If the RD Session Host server does not have a printer driver that matches the client printer, the server tries to use the Remote Desktop Easy Print driver to install the client printer.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-613">1</span><span class="sxs-lookup"><span data-stu-id="ab1de-613">1</span></span>
</dt> <dd>

<span data-ttu-id="ab1de-614">Der RD-Sitzungshost Server versucht zunächst, den Easy Print für Remotedesktop Druckertreiber zu verwenden, um alle Client Drucker zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ab1de-614">The RD Session Host server first tries to use the Remote Desktop Easy Print printer driver to install all client printers.</span></span> <span data-ttu-id="ab1de-615">Wenn der Easy Print für Remotedesktop Druckertreiber nicht verwendet werden kann, wird ein Druckertreiber auf dem RD-Sitzungshost Server verwendet, der mit dem Client Drucker übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="ab1de-615">If for any reason the Remote Desktop Easy Print printer driver cannot be used, a printer driver on the RD Session Host server that matches the client printer is used.</span></span>

</dd> </dl>

<span data-ttu-id="ab1de-616">**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab1de-616">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="ab1de-617">**Userberechtigung**</span><span class="sxs-lookup"><span data-stu-id="ab1de-617">**UserPermission**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-618">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-618">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-619">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab1de-619">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-620">Gibt an, ob jede Benutzersitzung eine strenge oder gelockerte Sicherheit aufweist.</span><span class="sxs-lookup"><span data-stu-id="ab1de-620">Specifies if each user session has tight or relaxed security.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ab1de-621"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-621"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-622">Sicherheit ist sehr streng.</span><span class="sxs-lookup"><span data-stu-id="ab1de-622">Security is tight.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ab1de-623"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-623"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-624">Sicherheit ist gelockert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-624">Security is relaxed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ab1de-625">**Usetempfolders**</span><span class="sxs-lookup"><span data-stu-id="ab1de-625">**UseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab1de-626">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab1de-626">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab1de-627">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-627">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab1de-628">Gibt an, ob temporäre Verzeichnisse pro Sitzung erstellt und gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="ab1de-628">Specifies whether temporary directories are created and deleted on a per-session basis.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ab1de-629"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ab1de-629"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-630">Temporäre Verzeichnisse werden für jede Sitzung nicht erstellt und gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ab1de-630">Temporary directories are not created and deleted for each session.</span></span> <span data-ttu-id="ab1de-631">Eine wird für die erste Sitzung erstellt und nie gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ab1de-631">One is created for the first session and never deleted.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ab1de-632"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ab1de-632"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ab1de-633">Temporäre Verzeichnisse werden für jede Sitzung erstellt und gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ab1de-633">Temporary directories are created and deleted for each session.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab1de-634">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab1de-634">Remarks</span></span>

<span data-ttu-id="ab1de-635">**Win32 \_ Terminalservicesete** ist [**Win32 \_ Terminalservice**](win32-terminalservice.md) als **Einstellungs** Eigenschaft der [**Win32 \_ terminalservicedesetting**](win32-terminalservicetosetting.md) -Zuordnung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ab1de-635">**Win32\_TerminalServiceSetting** is associated to [**Win32\_TerminalService**](win32-terminalservice.md) as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="ab1de-636">[**Win32 \_ TerminalSetting**](win32-terminalsetting.md) ist dem [**Win32- \_ Terminal**](win32-terminal.md) als **Setting** -Eigenschaft der [**Win32 \_ terminalterminalsetting**](win32-terminalterminalsetting.md) -Zuordnung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ab1de-636">[**Win32\_TerminalSetting**](win32-terminalsetting.md) is associated to [**Win32\_Terminal**](win32-terminal.md) as the **Setting** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="ab1de-637">Zum Herstellen einer Verbindung mit dem root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="ab1de-637">To connect to the Root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="ab1de-638">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="ab1de-638">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="ab1de-639">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von sechs.</span><span class="sxs-lookup"><span data-stu-id="ab1de-639">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="ab1de-640">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ab1de-640">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="ab1de-641">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="ab1de-641">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ab1de-642">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="ab1de-642">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ab1de-643">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ab1de-643">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ab1de-644">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ab1de-644">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab1de-645">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab1de-645">Requirements</span></span>



| <span data-ttu-id="ab1de-646">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab1de-646">Requirement</span></span> | <span data-ttu-id="ab1de-647">Wert</span><span class="sxs-lookup"><span data-stu-id="ab1de-647">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1de-648">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab1de-648">Minimum supported client</span></span><br/> | <span data-ttu-id="ab1de-649">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ab1de-649">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ab1de-650">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab1de-650">Minimum supported server</span></span><br/> | <span data-ttu-id="ab1de-651">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab1de-651">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab1de-652">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab1de-652">Namespace</span></span><br/>                | <span data-ttu-id="ab1de-653">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ab1de-653">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ab1de-654">MOF</span><span class="sxs-lookup"><span data-stu-id="ab1de-654">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab1de-655"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ab1de-655"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab1de-656">DLL</span><span class="sxs-lookup"><span data-stu-id="ab1de-656">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab1de-657"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab1de-657"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab1de-658">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab1de-658">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab1de-659">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="ab1de-659">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="ab1de-660">**Win32- \_ Terminal**</span><span class="sxs-lookup"><span data-stu-id="ab1de-660">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="ab1de-661">**Win32 \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="ab1de-661">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="ab1de-662">**Win32 \_ terminalservicede Setting**</span><span class="sxs-lookup"><span data-stu-id="ab1de-662">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="ab1de-663">**Win32 \_ terminalterminalsetting**</span><span class="sxs-lookup"><span data-stu-id="ab1de-663">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> <dt>

[<span data-ttu-id="ab1de-664">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="ab1de-664">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

