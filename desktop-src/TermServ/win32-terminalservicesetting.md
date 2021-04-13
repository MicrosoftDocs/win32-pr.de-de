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
# <a name="win32_terminalservicesetting-class"></a>Win32 \_ terminalservicesetts-Klasse

Die **Win32 \_ terminalserviceseten** -WMI-Klasse stellt die Konfiguration für einen Remotedesktop-Sitzungshost Server (RD-Sitzungshost) dar. Zu den Einstellungen gehören Funktionen wie RD-Sitzungshost Server Modus, Lizenzierung, aktiver Desktop, Berechtigungen, Löschen temporärer Ordner und temporäre Verzeichnisse für Sitzungen.

Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge. Referenzinformationen zu-Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.

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

Die **Win32 \_ terminalservicesetts** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ terminalservicesetts** -Klasse verfügt über diese Methoden.



| Methode                                                                                                                | BESCHREIBUNG                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Adddirectconnectlicenseserver**](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | Konfiguriert einen neuen Lizenzserver im Unternehmen.<br/>                                                                                                                  |
| [**Addlstospecifiedlicenseserverlist**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | Fügt den angegebenen Lizenzserver am Ende der Liste der angegebenen Lizenzserver hinzu.<br/>                                                                                  |
| [**Canaccesslicenseserver**](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | Bestimmt, ob auf dem RD-Sitzungshost Server Remotedesktopdienste Client Zugriffs Lizenzen (RDS-CALs) von einem Remotedesktop Lizenzserver angefordert werden können.<br/> |
| [**ChangeMode**](win32-terminalservicesetting-changemode.md)                                                         | Legt den Lizenztyp des Remotedesktop Lizenzservers fest.<br/>                                                                                                       |
| [**"Kreatewinstation"**](createwinstation-win32-terminalservicesetting.md)                                             | Erstellt einen neuen listenerstapel auf der Grundlage der eindeutigen Kombination aus Listenername und NIC.<br/>                                                                              |
| [**Deletedirectconnectlicenseserver**](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | Löscht den angegebenen Lizenzserver aus dem Unternehmen.<br/>                                                                                                           |
| [**Emptyspecifiedlicenseserverlist**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | Entfernt alle Lizenzserver aus der Liste der angegebenen Lizenzserver.<br/>                                                                                             |
| [**Findlicenseservers**](findlicenseservers-win32-terminalservicesetting.md)                                         | Listet alle Remotedesktop Lizenzserver und die Ermittlungsmethode auf.<br/>                                                                                   |
| [**GetDomain**](getdomain-win32-terminalservicesetting.md)                                                           | Ruft den Namen der Domäne ab, der der RD-Sitzungshost Server angehört.<br/>                                                                                    |
| [**Getgraceperioddays**](getgraceperioddays-win32-terminalservicesetting.md)                                         | Ruft die Anzahl der Tage ab, die in der RD-Lizenzierung Toleranz Periode für einen RD-Sitzungshost Server verbleiben.<br/>                                                     |
| [**Getregisteredlicenseserverlist**](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | Ruft die Liste der registrierten Lizenzserver ab.<br/>                                                                                                                        |
| [**Getspecifiedlicenseserverlist**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Ruft die Liste der angegebenen Lizenzserver ab.<br/>                                                                                                                    |
| [**Gettslanaids**](gettslanaids-win32-terminalservicesetting.md)                                                     | Ruft die IDs und Beschreibungen Remotedesktopdienste Netzwerkadapter ab.<br/>                                                                                          |
| [**Gettstolsconnectivitystatus**](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | Bestimmt den Konnektivitätsstatus zwischen Remotedesktopdienste und einem Lizenzserver.<br/>                                                                            |
| [**Getwinstationdrivernames**](getwinstationdrivernames-win32-terminalservicesetting.md)                             | Ruft eine Liste der Namen von WinStation-Treibern ab.<br/>                                                                                                                        |
| [**Pinglicenseserver**](pinglicenseserver-win32-terminalservicesetting.md)                                           | Pings an den Lizenzserver, um zu bestimmen, ob es sich um einen gültigen Lizenzserver handelt.<br/>                                                                                         |
| [**Removelsfromspecifiedlicenseserverlist**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | Entfernt den angegebenen Lizenzserver aus der Liste der angegebenen Lizenzserver.<br/>                                                                                        |
| [**"Aballow-Connections"**](win32-terminalservicesetting-setallowtsconnections.md)                                   | Legt die **allowtconnections** -Eigenschaft fest.<br/>                                                                                                                           |
| [**Setdisableforciblelogoff**](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | Legt die **disablezwangs blelogoff** -Eigenschaft fest.<br/>                                                                                                                        |
| [**Setfallbackprintdrivertype**](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | Legt die **fallbackprintdrivertype** -Eigenschaft fest.<br/>                                                                                                                      |
| [**Verzeichnis ""**](win32-terminalservicesetting-sethomedirectory.md)                                             | Legt die **Homedirectory** -Eigenschaft fest.<br/>                                                                                                                                |
| [**Setpolicypropertyname**](win32-terminalservicesetting-setpolicypropertyname.md)                                   | Legt eine der folgenden Eigenschaften fest: **deletetempfolders** oder **usetempfolders**.<br/>                                                                                  |
| [**Setprimarylicenseserver**](setprimarylicenseserver-win32-terminalservicesetting.md)                               | Legt den angegebenen Lizenzserver als ersten Eintrag in der Liste der angegebenen Lizenzserver fest.<br/>                                                                          |
| [**Setprofilepath**](win32-terminalservicesetting-setprofilepath.md)                                                 | Legt die **ProfilePath** -Eigenschaft fest.<br/>                                                                                                                                  |
| [**Setsinglesession**](win32-terminalservicesetting-setsinglesession.md)                                             | Legt die **SingleSession** -Eigenschaft fest.<br/>                                                                                                                                |
| [**Setspecifiedlicenseserverlist**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Aktualisiert die Liste der angegebenen Lizenzserver, wobei alle vorhandenen angegebenen Lizenzserver ersetzt werden.<br/>                                                                    |
| [**Settimezoneredirection**](win32-terminalservicesetting-settimezoneredirection.md)                                 | Legt die **timezoneredirection** -Eigenschaft fest.<br/>                                                                                                                          |
| [**Updatedirectconnectlicenseserver**](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | Aktualisiert die Liste der Discovery-Lizenzserver.<br/>                                                                                                                      |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ terminalservicesetts** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Activedesktop**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob Active Desktop in jeder Benutzersitzung zulässig ist.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (0)


</dt> <dd>

Active Desktop ist in jeder Benutzersitzung nicht zulässig.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (1)


</dt> <dd>

Aktiver Desktop ist in jeder Benutzersitzung zulässig.

</dd> </dl>

</dd> <dt>

**Allow-connections**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob neue Remotedesktopdienste Verbindungen zulässig sind.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Neue Verbindungen sind nicht zulässig.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


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

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Deletetempfolders**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob temporäre Verzeichnisse beim Beenden gelöscht werden.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Das Löschen temporärer Verzeichnisse ist deaktiviert.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Das Löschen temporärer Verzeichnisse ist aktiviert.

</dd> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**DirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft ist nicht verfügbar.

**Windows Server 2008:** Listet die Lizenzserver auf.

</dd> <dt>

**Disableforciblelogoff**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bestimmt, ob ein Administrator, der bei der Konsole angemeldet ist, erzwungen werden kann.

<dt>

0
</dt> <dd>

Der Administrator kann erzwungen werden.

</dd> <dt>

1
</dt> <dd>

Der Administrator kann nicht erzwungen werden.

</dd> </dl>

</dd> <dt>

**Enableautomatikreconnection**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob Remotedesktop Verbindungs Clients die automatische erneute Verbindung mit Sitzungen auf einem RD-Sitzungshost Server zulassen, wenn die Netzwerkverbindung vorübergehend unterbrochen wird.

<dt>

0 (0x0)
</dt> <dd>

Das automatische erneute Herstellen der Verbindung ist deaktiviert.

</dd> <dt>

1 (0x1)
</dt> <dd>

Die automatische erneute Verbindungs Herstellung ist aktiviert.

</dd> </dl>

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Enabledfss**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob Dynamic Fair-Share Scheduling (DfSS) aktiviert oder deaktiviert ist. Dies kann einer der folgenden Werte sein:

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

**Enablediskf**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Zeitplanung für die gleichmäßige Datenträger-

<dt>

0 (0x0)
</dt> <dd>

Die Datenträger-planmäßige Freigabe Planung ist deaktiviert.

</dd> <dt>

1 (0x1)
</dt> <dd>

Die gemeinsame Nutzung von Datenträger Plänen ist aktiviert.

</dd> </dl>

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Enablenetworkf**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Planung der Netzwerk gerechten Freigabe aktiviert ist.

<dt>

0 (0x0)
</dt> <dd>

Die Planung der Netzwerk gerechten Freigabe ist deaktiviert.

</dd> <dt>

1 (0x1)
</dt> <dd>

Die Planung der Netzwerk gerechten Freigabe ist aktiviert.

</dd> </dl>

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Enableremotedesktopmsi**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Remotedesktop-MSI aktiviert oder deaktiviert ist.

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

**Fallbackprintdrivertype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, auf welchen Druckertreiber ein Fall Back durch ein Fall Back

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**Keine Fall Back-dirvers = 0** (0)


</dt> <dd>

Keine Fall Back Treiber.

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Beste Vermutung = 1** (1)


</dt> <dd>

Beste Schätzung.

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Beste Schätzung, wenn keine Entsprechung für die PCL gefunden wird = 2** (2)


</dt> <dd>

Beste Schätzung. Wenn keine Entsprechung gefunden wird, Fall Back auf Hewlett-Packard-druckersteuerungsprache (PCL).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Beste Schätzung, wenn keine Entsprechung gefunden wird, Fall Back auf PS = 3** (3)


</dt> <dd>

Beste Schätzung. Wenn keine Entsprechung gefunden wird, Fall Back auf PostScript (PS).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Wenn keine Entsprechung gefunden wird, wird empfohlen, sowohl PCL-als auch PS-Treiber = 4** (4) anzuzeigen.


</dt> <dd>

Beste Schätzung. Wenn keine Entsprechung gefunden wird, zeigen Sie sowohl PS-als auch PCL-Treiber an.

</dd> </dl>

</dd> <dt>

**Getcapabilitiesid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Funktions-ID für den Anbieter.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Stammverzeichnis für den Computer.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Das Datum, an dem das Objekt installiert wurde. Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Licensingdescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des Lizenzierungs Modus.

</dd> <dt>

**Licensingname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Lizenzierungs Modus.

</dd> <dt>

**LicensingType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Lizenzierungstyp für den angegebenen Server Modus.

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Persönlicher Terminal Server** (0)


</dt> <dd>

Persönlicher RD-Sitzungshost Server.

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

**Limitedusersessions**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Funktion zum Begrenzen der Anzahl aktiver und inaktiver Sitzungen, die auf einem RD-Sitzungshost Server zulässig sind, aktiviert ist. Beispielsweise können Sie " **limitedusersessions** " festlegen, um die Lizenz Konformität für eine bestimmte Anwendung zu gewährleisten, die auf dem RD-Sitzungshost Server installiert ist. Möglicherweise möchten Sie die maximale Anzahl von Sitzungen auf einem RD-Sitzungshost Server in einer Farm mit Lastenausgleich einschränken, damit der Server nicht überladen wird, wenn ein anderer Server in der Farm ausfällt.

> [!Note]
>
> Die Sitzung, die zum Herstellen einer Verbindung mit dem Server zu Verwaltungszwecken verwendet wird, wird von " **limitedusersessions**" nicht beeinträchtigt.
>
> Wenn ein Benutzer in einer RD-Sitzungshost Serverfarm das Sitzungs Limit überschreitet, wird die Sitzung durch RD-Verbindungsbroker Lastenausgleich an einen anderen Server weitergeleitet. Wenn es sich bei dem Server um einen eigenständigen Server handelt, ist der Benutzer nicht in der Lage, eine Verbindung herzustellen.
>
> Aufgrund der Sitzung, die zum Herstellen einer Verbindung mit dem Server zu Verwaltungszwecken verwendet wird, und der zeitlichen Steuerung der Anzahl der Sitzungen während des Anmeldevorgangs wird empfohlen, dass Sie " **limitedusersessions** " auf einen Wert festlegen, der den physischen Grenzwert für die Anzahl der Sitzungen auf einem Server etwas niedriger ist.
>
> Die **limitedusersessions** -Eigenschaft ist nur gültig, wenn der RD-Sitzungshost-Rollen Dienst installiert ist.

 

<dt>

0
</dt> <dd>

Die Funktion ist deaktiviert.

</dd> <dt>

1 oder höher
</dt> <dd>

Der Wert 1 oder höher stellt die maximale Anzahl von Sitzungen (sowohl aktive als auch inaktive) dar, die auf dem RD-Sitzungshost Server zulässig sind.

</dd> </dl>

</dd> <dt>

**Anmeldungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
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

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Networkf-Klasse**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die standardmäßige Netzwerk Last für den gesamten Netzwerk Datenverkehr an. Gültige Werte sind 1 bis 9.

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Networkf-localsystemweight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die standardmäßige Netzwerk Last für lokale System Prozesse an. Gültige Werte sind 1 bis 9.

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Networksssusersessionweight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die standardmäßige Netzwerk Last für eine Benutzersitzung an. Gültige Werte sind 1 bis 9.

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Policysourceallow-Connections**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **allowtconnections** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourceconfiguredlicenseservers**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die von der [**getspecifiedlicenseserverlist**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) -Methode zurückgegebenen Lizenzserver vom Server oder von der Gruppenrichtlinie konfiguriert werden.

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

**Policysourcedeletetempfolders**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **deletetempfolders** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft ist nicht verfügbar.

**Windows Server 2008:** Gibt an, ob die **DirectConnectLicenseServers** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourcedisableforciblelogoff**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird nicht unterstützt.

**Windows Server 2008:** Bestimmt, ob die **disableforciblelogoff** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourceenableautomatikreconnection**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **enableautomatikreconnection** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourceenabledfss**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **enabledfss** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourceenableremotedesktopmsi**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **enableremotedesktopmsi** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourcefallbackprintdrivertype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **fallbackprintdrivertype** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourcehomedirectory**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **Homedirectory** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **LicensingType** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **ProfilePath** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourceredirec\martcards**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **redirectmartcards** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **SingleSession** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourcetimezoneredirection**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **timezoneredirection** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourceuserdecoasyprintdriver**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **userenasyprintdriver** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Policysourceu-tempfolders**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die **usetempfolders** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.

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

**Possiblelicensingtypes**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("persönlicher Terminal Server", "Remotedesktop für die Verwaltung", "pro Gerät", "pro Benutzer", "nicht konfiguriert")
</dt> </dl>

Eine Bitmaske, die die verfügbaren Lizenzierungs Typen angibt. Dies kann eine Kombination aus einem oder mehreren der folgenden Werte sein.

<dt>

1 (0x1)
</dt> <dd>

Persönliche RD-Sitzungshost Server-Lizenzen werden unterstützt.

</dd> <dt>

2 (0x2)
</dt> <dd>

Remotedesktop Lizenzen werden unterstützt.

</dd> <dt>

4 (0x4)
</dt> <dd>

Pro-Gerät-Lizenzen werden unterstützt.

</dd> <dt>

8 (0x8)
</dt> <dd>

Pro-Benutzer-Lizenzen werden unterstützt.

</dd> </dl>

</dd> <dt>

**Profilpfad**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Profilpfad für den Computer.

</dd> <dt>

**Redirecrichmartcards**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Umleitung von smartcardgeräten in einer Remote Sitzung zulässig ist.

<dt>

0 (0x0)
</dt> <dd>

Eine Smartcard-Geräte Umleitung ist nicht zulässig.

</dd> <dt>

1 (0x1)
</dt> <dd>

Eine Smartcard-Geräte Umleitung ist zulässig.

</dd> </dl>

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Name des RD-Sitzungshost Servers, dessen Eigenschaften von Interesse sind.

</dd> <dt>

**Sessionbrokerdrainmode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der RD-Verbindungsbroker Benutzer Anmeldemodus.

<dt>

0
</dt> <dd>

Lässt alle Verbindungen zu.

</dd> <dt>

1
</dt> <dd>

Zulassen von erneuten Verbindungen, aber verhindern von neuen Anmeldungen, bis der Server neu gestartet wird.

</dd> <dt>

2
</dt> <dd>

Lässt erneute Verbindungen zu, verhindert jedoch neue Anmeldungen.

</dd> </dl>

</dd> <dt>

**SingleSession**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob pro Benutzer eine oder mehrere Remotedesktopdienste Sitzungen zulässig sind.

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)


</dt> <dd>

Pro Benutzer ist mehr als eine Sitzung zulässig.

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)


</dt> <dd>

Pro Benutzer ist nur eine Sitzung zulässig.

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen). Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service". Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

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

**Terminalservermode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der RD-Sitzungshost Server-Betriebsmodus des Remotedesktopdienste Dienstanbieter. Dieser Modus steuert die anwendbaren Lizenzierungsrichtlinien und ob die Anwendungs Kompatibilitäts Features aktiviert sind.

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**Appserver** (1)


</dt> <dd>

Der Server fungiert als Anwendungsserver.

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)


</dt> <dd>

Die Sitzung wird Remote verwaltet.

</dd> </dl>

</dd> <dt>

**Timezoneredirection**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Client Computer seine Zeitzoneneinstellungen an die Remotedesktopdienste Sitzung umleiten kann.

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

**Userdebug PrintDriver**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der Easy Print für Remotedesktop Druckertreiber zuerst zum Installieren aller Client Drucker verwendet wird.

<dt>

0
</dt> <dd>

Der RD-Sitzungshost Server versucht, einen geeigneten Druckertreiber zu finden, um den Client Drucker zu installieren. Wenn der RD-Sitzungshost Server keinen Druckertreiber hat, der mit dem Client Drucker übereinstimmt, versucht der Server, den-Easy Print für Remotedesktop Treiber zu verwenden, um den Client Drucker zu installieren.

</dd> <dt>

1
</dt> <dd>

Der RD-Sitzungshost Server versucht zunächst, den Easy Print für Remotedesktop Druckertreiber zu verwenden, um alle Client Drucker zu installieren. Wenn der Easy Print für Remotedesktop Druckertreiber nicht verwendet werden kann, wird ein Druckertreiber auf dem RD-Sitzungshost Server verwendet, der mit dem Client Drucker übereinstimmt.

</dd> </dl>

**Windows Server 2008 R2 und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.

</dd> <dt>

**Userberechtigung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob jede Benutzersitzung eine strenge oder gelockerte Sicherheit aufweist.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Sicherheit ist sehr streng.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Sicherheit ist gelockert.

</dd> </dl>

</dd> <dt>

**Usetempfolders**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob temporäre Verzeichnisse pro Sitzung erstellt und gelöscht werden.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Temporäre Verzeichnisse werden für jede Sitzung nicht erstellt und gelöscht. Eine wird für die erste Sitzung erstellt und nie gelöscht.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Temporäre Verzeichnisse werden für jede Sitzung erstellt und gelöscht.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**Win32 \_ Terminalservicesete** ist [**Win32 \_ Terminalservice**](win32-terminalservice.md) als **Einstellungs** Eigenschaft der [**Win32 \_ terminalservicedesetting**](win32-terminalservicetosetting.md) -Zuordnung zugeordnet.

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md) ist dem [**Win32- \_ Terminal**](win32-terminal.md) als **Setting** -Eigenschaft der [**Win32 \_ terminalterminalsetting**](win32-terminalterminalsetting.md) -Zuordnung zugeordnet.

Zum Herstellen einer Verbindung mit dem root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten. Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**. Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von sechs.

Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> <dt>

[**Win32- \_ Terminal**](win32-terminal.md)
</dt> <dt>

[**Win32 \_ Terminalservice**](win32-terminalservice.md)
</dt> <dt>

[**Win32 \_ terminalservicede Setting**](win32-terminalservicetosetting.md)
</dt> <dt>

[**Win32 \_ terminalterminalsetting**](win32-terminalterminalsetting.md)
</dt> <dt>

[**CIM- \_ Einstellung**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

