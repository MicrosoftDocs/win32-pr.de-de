---
title: Win32_TerminalServiceSetting-Klasse
description: Stellt die Konfiguration für einen Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server dar.
ms.assetid: 4cd047db-921f-4ccb-946b-d2c7b8d6beea
ms.tgt_platform: multiple
keywords:
- Win32_TerminalServiceSetting-Remotedesktopdienste
- Win32_TerminalServiceSetting klasse Remotedesktopdienste , beschrieben
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
ms.openlocfilehash: 5a4d7aefdd3f0a684c91fda3ab73d17de32327f34e8d20d5a7f844ea07e21906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769890"
---
# <a name="win32_terminalservicesetting-class"></a>Win32 \_ TerminalServiceSetting-Klasse

Die **WMI-Klasse \_ Win32 TerminalServiceSetting** stellt die Konfiguration für einen Remotedesktop-Sitzungshost(RD-Sitzungshost) Server dar. Einstellungen umfassen Funktionen wie RD-Sitzungshost Servermodus, Lizenzierung, Active Desktop, Berechtigungen, Löschen temporärer Ordner und temporäre Verzeichnisse für Sitzungen.

Die folgende Syntax wird von MOF-Code vereinfacht und enthält alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge. Referenzinformationen zu Methoden finden Sie in der Tabelle der Methoden weiter unten in diesem Thema.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **Win32 \_ TerminalServiceSetting-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ TerminalServiceSetting-Klasse** verfügt über diese Methoden.



| Methode                                                                                                                | Beschreibung                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDirectConnectLicenseServer**](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | Konfiguriert einen neuen Lizenzserver im Unternehmen.<br/>                                                                                                                  |
| [**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | Fügt den angegebenen Lizenzserver am Ende der Liste der angegebenen Lizenzserver hinzu.<br/>                                                                                  |
| [**CanAccessLicenseServer**](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | Bestimmt, ob der RD-Sitzungshost-Server Remotedesktopdienste Clientzugriffslizenzen (RDS CALs) von einem Remotedesktop anfordern darf.<br/> |
| [**ChangeMode**](win32-terminalservicesetting-changemode.md)                                                         | Legt den Lizenzierungstyp des Lizenzservers Remotedesktop fest.<br/>                                                                                                       |
| [**CreateWinstation**](createwinstation-win32-terminalservicesetting.md)                                             | Erstellt einen neuen Listenerstapel basierend auf der eindeutigen Kombination aus Listenername und NIC.<br/>                                                                              |
| [**DeleteDirectConnectLicenseServer**](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | Löscht den angegebenen Lizenzserver aus dem Unternehmen.<br/>                                                                                                           |
| [**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | Entfernt alle Lizenzserver aus der Liste der angegebenen Lizenzserver.<br/>                                                                                             |
| [**FindLicenseServers**](findlicenseservers-win32-terminalservicesetting.md)                                         | Enumeriert alle Remotedesktop Lizenzserver und die Ermittlungsmethode.<br/>                                                                                   |
| [**GetDomain**](getdomain-win32-terminalservicesetting.md)                                                           | Ruft den Namen der Domäne ab, zu der RD-Sitzungshost Server gehört.<br/>                                                                                    |
| [**GetGracePeriodDays**](getgraceperioddays-win32-terminalservicesetting.md)                                         | Ruft die Anzahl der Tage ab, die in der RD-Lizenzierungs-Toleranzperiode für einen RD-Sitzungshost bleiben.<br/>                                                     |
| [**GetRegisteredLicenseServerList**](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | Ruft die Liste der registrierten Lizenzserver ab.<br/>                                                                                                                        |
| [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Ruft die Liste der angegebenen Lizenzserver ab.<br/>                                                                                                                    |
| [**GetTSLanaIds**](gettslanaids-win32-terminalservicesetting.md)                                                     | Ruft die IDs und Beschreibungen Remotedesktopdienste Netzwerkadaptern ab.<br/>                                                                                          |
| [**GetTStoLSConnectivityStatus**](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | Bestimmt den Konnektivitätsstatus zwischen Remotedesktopdienste und einem Lizenzserver.<br/>                                                                            |
| [**GetWinstationDriverNames**](getwinstationdrivernames-win32-terminalservicesetting.md)                             | Ruft eine Liste der Winstation-Treibernamen ab.<br/>                                                                                                                        |
| [**PingLicenseServer**](pinglicenseserver-win32-terminalservicesetting.md)                                           | Pingt den Lizenzserver, um zu ermitteln, ob es sich um einen gültigen Lizenzserver handelt.<br/>                                                                                         |
| [**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | Entfernt den angegebenen Lizenzserver aus der Liste der angegebenen Lizenzserver.<br/>                                                                                        |
| [**SetAllowTSConnections**](win32-terminalservicesetting-setallowtsconnections.md)                                   | Legt die **AllowTSConnections-Eigenschaft** fest.<br/>                                                                                                                           |
| [**SetDisableForcibleLogoff**](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | Legt die **DisableForcibleLogoff-Eigenschaft** fest.<br/>                                                                                                                        |
| [**SetFallbackPrintDriverType**](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | Legt die **FallbackPrintDriverType-Eigenschaft** fest.<br/>                                                                                                                      |
| [**SetHomeDirectory**](win32-terminalservicesetting-sethomedirectory.md)                                             | Legt die **HomeDirectory-Eigenschaft** fest.<br/>                                                                                                                                |
| [**SetPolicyPropertyName**](win32-terminalservicesetting-setpolicypropertyname.md)                                   | Legt eine der folgenden Eigenschaften fest: **DeleteTempFolders** oder **UseTempFolders**.<br/>                                                                                  |
| [**SetPrimaryLicenseServer**](setprimarylicenseserver-win32-terminalservicesetting.md)                               | Legt den angegebenen Lizenzserver als ersten Eintrag in der Liste der angegebenen Lizenzserver fest.<br/>                                                                          |
| [**SetProfilePath**](win32-terminalservicesetting-setprofilepath.md)                                                 | Legt die **ProfilePath-Eigenschaft** fest.<br/>                                                                                                                                  |
| [**SetSingleSession**](win32-terminalservicesetting-setsinglesession.md)                                             | Legt die **SingleSession-Eigenschaft** fest.<br/>                                                                                                                                |
| [**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Aktualisiert die Liste der angegebenen Lizenzserver und ersetzt dabei alle vorhandenen angegebenen Lizenzserver.<br/>                                                                    |
| [**SetTimeZoneRedirection**](win32-terminalservicesetting-settimezoneredirection.md)                                 | Legt die **TimeZoneRedirection-Eigenschaft** fest.<br/>                                                                                                                          |
| [**UpdateDirectConnectLicenseServer**](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | Aktualisiert die Liste der Ermittlungslizenzserver.<br/>                                                                                                                      |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TerminalServiceSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ActiveDesktop**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, Active Desktop in jeder Benutzersitzung zulässig ist.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (0)


</dt> <dd>

Active Desktop ist nicht in jeder Benutzersitzung zulässig.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (1)


</dt> <dd>

Active Desktop ist in jeder Benutzersitzung zulässig.

</dd> </dl>

</dd> <dt>

**AllowTSConnections**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob neue Remotedesktopdienste verbindungen zulässig sind.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Neue Verbindungen sind nicht zulässig.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Neue Verbindungen sind zulässig.

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Beschreibung (einzeilenbasierte Zeichenfolge) des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**DeleteTempFolders**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob temporäre Verzeichnisse beim Beenden gelöscht werden.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Das Löschen temporärer Verzeichnisse ist deaktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Das Löschen temporärer Verzeichnisse ist aktiviert.

</dd> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**DirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **VERALTET**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft ist nicht verfügbar.

**Windows Server 2008:** Listet die Lizenzserver auf.

</dd> <dt>

**DisableForcibleLogoff**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bestimmt, ob ein Administrator, der bei der Konsole angemeldet ist, abgemeldet werden kann.

<dt>

0
</dt> <dd>

Der Administrator kann abgemeldet werden.

</dd> <dt>

1
</dt> <dd>

Der Administrator kann nicht abgemeldet werden.

</dd> </dl>

</dd> <dt>

**EnableAutomaticReconnection**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob Remotedesktop Verbindungsclients automatisch eine erneute Verbindung mit Sitzungen auf einem RD-Sitzungshost Server herstellen soll, wenn die Netzwerkverbindung vorübergehend unterbrochen wird.

<dt>

0 (0x0)
</dt> <dd>

Die automatische wiederherzustellende Verbindung ist deaktiviert.

</dd> <dt>

1 (0x1)
</dt> <dd>

Die automatische wiederherzustellende Verbindung ist aktiviert.

</dd> </dl>

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**EnableDFSS**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die dynamische Zeitplanung mit fairer Freigabe (DFSS) aktiviert oder deaktiviert ist. Dies kann einer der folgenden Werte sein.

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

<dt>

0
</dt> <dd>

DFSS ist deaktiviert.

</dd> <dt>

1
</dt> <dd>

DFSS ist aktiviert.

</dd> </dl>

</dd> <dt>

**EnableDiskFSS**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Zeitplanung für die teilungsfähige Datenträgerfreigabe aktiviert ist.

<dt>

0 (0x0)
</dt> <dd>

Die Zeitplanung für faire Freigaben auf Datenträgern ist deaktiviert.

</dd> <dt>

1 (0x1)
</dt> <dd>

Die Zeitplanung für die teilungsfähige Datenträgerfreigabe ist aktiviert.

</dd> </dl>

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**EnableNetworkFSS**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Zeitplanung für die faire Netzwerkfreigabe aktiviert ist.

<dt>

0 (0x0)
</dt> <dd>

Die Zeitplanung für eine angemessene Netzwerkfreigabe ist deaktiviert.

</dd> <dt>

1 (0x1)
</dt> <dd>

Die Zeitplanung für eine angemessene Netzwerkfreigabe ist aktiviert.

</dd> </dl>

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**EnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Remotedesktop MSI aktiviert oder deaktiviert ist.

<dt>

0 (0x0)
</dt> <dd>

Disabled

</dd> <dt>

1 (0x1)
</dt> <dd>

Aktiviert

</dd> </dl>

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**FallbackPrintDriverType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, auf welchen Druckertreiber ein Fallback stattfindet.

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**Kein Fallback-Dirvers=0** (0)


</dt> <dd>

Keine Fallbacktreiber.

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Best Guess=1** (1)


</dt> <dd>

Beste Schätzung.

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Beste Schätzung, wenn keine Übereinstimmung gefunden wird Fallback auf PCL=2** (2)


</dt> <dd>

Beste Schätzung. Wenn keine Übereinstimmung gefunden wird, wird ein Fallback auf Hewlett-Packard Printer Control Language (PCL) angezeigt.

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Best guess, if no match is found fallback to PS=3 (3) (Fallback auf PS=3 (3))**


</dt> <dd>

Beste Schätzung. Wenn keine Übereinstimmung gefunden wird, fallbacken Sie auf Postscript (PS).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Best guess, if no match is found both PCL and PS drivers=4 (4) (PCL- und PS-Treiber =4)**


</dt> <dd>

Beste Schätzung. Wenn keine Übereinstimmung gefunden wird, zeigen Sie sowohl PS- als auch PCL-Treiber an.

</dd> </dl>

</dd> <dt>

**GetCapabilitiesID**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Funktionen-ID für den Anbieter.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Stammverzeichnis für den Computer.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Das Datum, an dem das Objekt installiert wurde. Das Fehlen eines Werts gibt nicht an, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**LicensingDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des Lizenzierungsmodus.

</dd> <dt>

**LicensingName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Lizenzierungsmodus.

</dd> <dt>

**LicensingType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Lizenzierungstyp für den angegebenen Servermodus.

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Personal Terminal Server** (0)


</dt> <dd>

Persönlicher RD-Sitzungshost-Server.

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Remotedesktop für die Verwaltung** (1)


</dt> <dd>

Remotedesktop für die Verwaltung.

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Pro Gerät** (2)


</dt> <dd>

Pro Gerät. Gültig für Anwendungsserver.

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Pro Benutzer** (3)


</dt> <dd>

Pro Benutzer. Gültig für Anwendungsserver.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (4)


</dt> <dd>

Nicht konfiguriert.

</dd> </dl>

</dd> <dt>

**LimitedUserSessions**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob das Feature zum Begrenzen der Anzahl aktiver und inaktiver Sitzungen, die auf einem RD-Sitzungshost Server zulässig sind, aktiviert ist. Beispielsweise können Sie **LimitedUserSessions** festlegen, um die Lizenzkonformität für eine bestimmte Anwendung zu gewährleisten, die auf dem RD-Sitzungshost-Server installiert ist. Sie können auch die maximale Anzahl von Sitzungen auf einem RD-Sitzungshost Server in einer Farm mit Lastenausgleich begrenzen, damit der Server nicht überlastet wird, wenn ein anderer Server in der Farm ausfällt.

> [!Note]
>
> Die Sitzung, die zum Herstellen einer Verbindung mit dem Server zu Administrativen Zwecken verwendet wird, ist von **LimitedUserSessions** nicht betroffen.
>
> Wenn ein Benutzer in einer RD-Sitzungshost Serverfarm das Sitzungslimit überschreitet, wird die Sitzung durch den Lastenausgleich des RD-Verbindungsbrokers an einen anderen Server weitergeleitet. Wenn der Server ein eigenständiger Server ist, kann der Benutzer keine Verbindung herstellen.
>
> Aufgrund der Sitzung, die zum Herstellen einer Verbindung mit dem Server zu Administrativen Zwecken verwendet wird, und aufgrund des Zeitlichen Ablaufs der Erzwingung der Anzahl von Sitzungen während des Anmeldezyklus wird empfohlen, **LimitedUserSessions** auf einen Wert festzulegen, der etwas niedriger ist als der physische Grenzwert für die Anzahl der Sitzungen auf einem Server.
>
> Die **LimitedUserSessions-Eigenschaft** ist nur gültig, wenn der RD-Sitzungshost Rollendienst installiert ist.

 

<dt>

0
</dt> <dd>

Die Funktion ist deaktiviert.

</dd> <dt>

1 oder höher
</dt> <dd>

Der Wert mindestens stellt die maximale Anzahl von Sitzungen (sowohl aktiv als auch inaktiv) dar, die auf dem RD-Sitzungshost-Server zulässig sind.

</dd> </dl>

</dd> <dt>

**Anmeldungen**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob neue Sitzungen zulässig sind. Diese Einstellung wirkt sich nicht auf vorhandene Einstellungen aus.

<dt>

0
</dt> <dd>

Neue Sitzungen sind zulässig.

</dd> <dt>

1
</dt> <dd>

Neue Sitzungen sind nicht zulässig.

</dd> </dl>

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**NetworkFSSCatchAllWeight**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die Standardgewichtung der Netzwerk-Fair Share für den gesamten Netzwerkdatenverkehr an. Gültige Werte sind 1 bis 9.

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**NetworkFSSLocalSystemWeight**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die Standardgewichtung der Netzwerk-Fair Share für lokale Systemprozesse an. Gültige Werte sind 1 bis 9.

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**NetworkFSSUserSessionWeight**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die Standardgewichtung für die netzwerkeinheitliche Freigabe für eine Benutzersitzung an. Gültige Werte sind 1 bis 9.

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**PolicySourceAllowTSConnections**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **AllowTSConnections-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceConfiguredLicenseServers**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die von der [**GetSpecifiedLicenseServerList-Methode zurückgegebenen**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) Lizenzserver vom Server oder von der Gruppenrichtlinie konfiguriert werden.

**Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceDeleteTempFolders**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **DeleteTempFolders-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceDirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **VERALTET**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft ist nicht verfügbar.

**Windows Server 2008:** Gibt an, ob **die DirectConnectLicenseServers-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceDisableForcibleLogoff**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird nicht unterstützt.

**Windows Server 2008:** Bestimmt, ob **die DisableForcibleLogoff-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Gruppenrichtlinie:

</dd> </dl>

</dd> <dt>

**PolicySourceEnableAutomaticReconnection**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die EnableAutomaticReconnection-Eigenschaft** von der Server- oder Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**PolicySourceEnableDFSS**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die EnableDFSS-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**PolicySourceEnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die EnableRemoteDesktopMSI-Eigenschaft** von der Server- oder Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

**Windows Server 2008:** Diese Eigenschaft ist vor Windows Server 2008 R2 nicht verfügbar.

</dd> <dt>

**PolicySourceFallbackPrintDriverType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die FallbackPrintDriverType-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceHomeDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die HomeDirectory-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceLicensingType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die LicensingType-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceProfilePath**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die ProfilePath-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceRedirectSmartCards**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob **die RedirectSmartCards-Eigenschaft** von der Server- oder Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**PolicySourceSingleSession**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **SingleSession-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceTimeZoneRedirection**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **TimeZoneRedirection-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PolicySourceUseRD FootprintPrintDriver**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **UseRD FootprintPrintDriver-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**PolicySourceUseTempFolders**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **UseTempFolders-Eigenschaft** vom Server oder von der Gruppenrichtlinie konfiguriert wird.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Gruppenrichtlinie

</dd> </dl>

</dd> <dt>

**PossibleLicensingTypes**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("Personal Terminal Server", "Remotedesktop for Administration", "Per Device", "Per User", "Not Configured")
</dt> </dl>

Eine Bitmaske, die die verfügbaren Lizenzierungstypen angibt. Dies kann eine Kombination aus einem oder mehreren der folgenden Werte sein.

<dt>

1 (0x1)
</dt> <dd>

Persönliche RD-Sitzungshost Serverlizenzen werden unterstützt.

</dd> <dt>

2 (0x2)
</dt> <dd>

Remotedesktop Lizenzen werden unterstützt.

</dd> <dt>

4 (0x4)
</dt> <dd>

Pro Gerät werden Lizenzen unterstützt.

</dd> <dt>

8 (0x8)
</dt> <dd>

Lizenzen pro Benutzer werden unterstützt.

</dd> </dl>

</dd> <dt>

**ProfilePath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Profilpfad für den Computer.

</dd> <dt>

**RedirectSmartCards**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Umleitung von Smartcardgeräten in einer Remotesitzung zulässig ist.

<dt>

0 (0x0)
</dt> <dd>

Die Umleitung von Smartcardgeräten ist nicht zulässig.

</dd> <dt>

1 (0x1)
</dt> <dd>

Die Umleitung von Smartcardgeräten ist zulässig.

</dd> </dl>

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name des RD-Sitzungshost Servers, dessen Eigenschaften von Interesse sind.

</dd> <dt>

**SessionBrokerDrainMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Benutzeranmeldemodus des RD-Verbindungsbrokers.

<dt>

0
</dt> <dd>

Lassen Sie alle Verbindungen zu.

</dd> <dt>

1
</dt> <dd>

Lassen Sie erneute Verbindungen zu, verhindern Sie jedoch neue Anmeldungen, bis der Server neu gestartet wird.

</dd> <dt>

2
</dt> <dd>

Lassen Sie erneute Verbindungen zu, verhindern Sie jedoch neue Anmeldungen.

</dd> </dl>

</dd> <dt>

**SingleSession**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob eine oder mehrere Remotedesktopdienste Sitzungen pro Benutzer zulässig sind.

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)


</dt> <dd>

Pro Benutzer sind mehr als eine Sitzung zulässig.

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)


</dt> <dd>

Pro Benutzer ist nur eine Sitzung zulässig.

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs- und Nichtoperationsstatus definiert werden. Betriebsstatus: "OK", "Heruntergestuft" und "Pred Fail" (ein Element, z. B. ein SMART-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, sagt aber einen Fehler in naher Zukunft vorher). Nichtoperationale Status: "Error", "Starting", "Stopping" und "Service". Letzteres, "Dienst", kann während des Spiegelungsresilverings eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Verwaltungsaufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Fehler")


</dt> <dd></dd> <dt>



 ("Heruntergestuft")


</dt> <dd></dd> <dt>



 ("Unbekannt")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Wird gestartet")


</dt> <dd></dd> <dt>



 ("Wird beendet")


</dt> <dd></dd> <dt>



 ("Dienst")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalServerMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der RD-Sitzungshost Serverbetriebsmodus des Remotedesktopdienste-Diensts. Dieser Modus steuert die lizenzierungsrichtlinien, die anwendbar sind, sowie, ob Anwendungskompatibilitätsfeatures aktiviert sind.

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)


</dt> <dd>

Der Server fungiert als Anwendungsserver.

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)


</dt> <dd>

Die Sitzung wird remote verwaltet.

</dd> </dl>

</dd> <dt>

**TimeZoneRedirection**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Clientcomputer seine Zeitzoneneinstellungen an die Remotedesktopdienste Sitzung umleiten kann.

<dt>

0
</dt> <dd>

Die Umleitung ist deaktiviert.

</dd> <dt>

1
</dt> <dd>

Die Umleitung ist aktiviert.

</dd> </dl>

</dd> <dt>

**UseRD FootprintPrintDriver**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der Easy Print für Remotedesktop Druckertreiber zuerst verwendet wird, um alle Clientdrucker zu installieren.

<dt>

0
</dt> <dd>

Der RD-Sitzungshost-Server versucht, einen geeigneten Druckertreiber für die Installation des Clientdruckers zu finden. Wenn der RD-Sitzungshost Server nicht über einen Druckertreiber verfügt, der mit dem Clientdrucker übereinstimmt, versucht der Server, den Easy Print für Remotedesktop Treiber zum Installieren des Clientdruckers zu verwenden.

</dd> <dt>

1
</dt> <dd>

Der RD-Sitzungshost-Server versucht zunächst, den Easy Print für Remotedesktop Druckertreiber zu verwenden, um alle Clientdrucker zu installieren. Wenn der Easy Print für Remotedesktop Druckertreiber aus irgendeinem Grund nicht verwendet werden kann, wird ein Druckertreiber auf dem RD-Sitzungshost-Server verwendet, der dem Clientdrucker entspricht.

</dd> </dl>

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Userpermission**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob jede Benutzersitzung eine enge oder gelockerte Sicherheit hat.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Die Sicherheit ist streng.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Die Sicherheit ist gelockert.

</dd> </dl>

</dd> <dt>

**UseTempFolders**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob temporäre Verzeichnisse pro Sitzung erstellt und gelöscht werden.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Temporäre Verzeichnisse werden nicht für jede Sitzung erstellt und gelöscht. Eine wird für die erste Sitzung erstellt und nie gelöscht.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Temporäre Verzeichnisse werden für jede Sitzung erstellt und gelöscht.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

**Win32 \_ TerminalServiceSetting** ist [**Win32 \_ TerminalService**](win32-terminalservice.md) als **Einstellungseigenschaft** der [**Win32 \_ TerminalServiceToSetting-Zuordnung**](win32-terminalservicetosetting.md) zugeordnet.

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md) ist [**Win32 \_ Terminal**](win32-terminal.md) als **Einstellungseigenschaft** der [**Win32 \_ TerminalTerminalSetting-Zuordnung**](win32-terminalterminalsetting.md) zugeordnet.

Um eine Verbindung mit dem \\ Root CIMV2 \\ TerminalServices-Namespace herzustellen, muss die Authentifizierungsebene Paketdatenschutz enthalten. Bei C/C++-Aufrufen ist dies eine Authentifizierungsebene von **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Bei Visual Basic- und Skriptaufrufen ist dies eine Authentifizierungsebene von **WbemAuthenticationLevelPktPrivacy** oder "pktPrivacy" mit dem Wert sechs.

Das folgende Beispiel Visual Basic Scripting Edition (VBScript) zeigt, wie Sie eine Verbindung mit einem Remotecomputer mit Paketschutz herstellen.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Einstellung**](cim-setting.md)
</dt> <dt>

[**\_Win32-Terminal**](win32-terminal.md)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dt>

[**Win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md)
</dt> <dt>

[**\_CIM-Einstellung**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

