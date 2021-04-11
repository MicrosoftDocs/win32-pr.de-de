---
description: Stellt ein Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: fdb9fe36-1b8a-4dfa-a1cd-55065017ba2a
ms.tgt_platform: multiple
title: Win32_ComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem
- Win32_ComputerSystem.SetPowerState
- Win32_ComputerSystem.AdminPasswordStatus
- Win32_ComputerSystem.AutomaticManagedPagefile
- Win32_ComputerSystem.AutomaticResetBootOption
- Win32_ComputerSystem.AutomaticResetCapability
- Win32_ComputerSystem.BootOptionOnLimit
- Win32_ComputerSystem.BootOptionOnWatchDog
- Win32_ComputerSystem.BootROMSupported
- Win32_ComputerSystem.BootupState
- Win32_ComputerSystem.BootStatus
- Win32_ComputerSystem.Caption
- Win32_ComputerSystem.ChassisBootupState
- Win32_ComputerSystem.ChassisSKUNumber
- Win32_ComputerSystem.CreationClassName
- Win32_ComputerSystem.CurrentTimeZone
- Win32_ComputerSystem.DaylightInEffect
- Win32_ComputerSystem.Description
- Win32_ComputerSystem.DNSHostName
- Win32_ComputerSystem.Domain
- Win32_ComputerSystem.DomainRole
- Win32_ComputerSystem.EnableDaylightSavingsTime
- Win32_ComputerSystem.FrontPanelResetStatus
- Win32_ComputerSystem.HypervisorPresent
- Win32_ComputerSystem.InfraredSupported
- Win32_ComputerSystem.InitialLoadInfo
- Win32_ComputerSystem.InstallDate
- Win32_ComputerSystem.KeyboardPasswordStatus
- Win32_ComputerSystem.LastLoadInfo
- Win32_ComputerSystem.Manufacturer
- Win32_ComputerSystem.Model
- Win32_ComputerSystem.Name
- Win32_ComputerSystem.NameFormat
- Win32_ComputerSystem.NetworkServerModeEnabled
- Win32_ComputerSystem.NumberOfLogicalProcessors
- Win32_ComputerSystem.NumberOfProcessors
- Win32_ComputerSystem.OEMLogoBitmap
- Win32_ComputerSystem.OEMStringArray
- Win32_ComputerSystem.PartOfDomain
- Win32_ComputerSystem.PauseAfterReset
- Win32_ComputerSystem.PCSystemType
- Win32_ComputerSystem.PCSystemTypeEx
- Win32_ComputerSystem.PowerManagementCapabilities
- Win32_ComputerSystem.PowerManagementSupported
- Win32_ComputerSystem.PowerOnPasswordStatus
- Win32_ComputerSystem.PowerState
- Win32_ComputerSystem.PowerSupplyState
- Win32_ComputerSystem.PrimaryOwnerContact
- Win32_ComputerSystem.PrimaryOwnerName
- Win32_ComputerSystem.ResetCapability
- Win32_ComputerSystem.ResetCount
- Win32_ComputerSystem.ResetLimit
- Win32_ComputerSystem.Roles
- Win32_ComputerSystem.Status
- Win32_ComputerSystem.SupportContactDescription
- Win32_ComputerSystem.SystemFamily
- Win32_ComputerSystem.SystemSKUNumber
- Win32_ComputerSystem.SystemStartupDelay
- Win32_ComputerSystem.SystemStartupOptions
- Win32_ComputerSystem.SystemStartupSetting
- Win32_ComputerSystem.SystemType
- Win32_ComputerSystem.ThermalState
- Win32_ComputerSystem.TotalPhysicalMemory
- Win32_ComputerSystem.UserName
- Win32_ComputerSystem.WakeUpType
- Win32_ComputerSystem.Workgroup
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e5282c854bfdb1ce4b80f61a202ebecac990576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126272"
---
# <a name="win32_computersystem-class"></a>Win32 \_ Computersystem-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ Computersystem** stellt ein Computersystem dar, auf dem Windows ausgeführt wird.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystem : CIM_UnitaryComputerSystem
{
  uint16   AdminPasswordStatus;
  boolean  AutomaticManagedPagefile;
  boolean  AutomaticResetBootOption;
  boolean  AutomaticResetCapability;
  uint16   BootOptionOnLimit;
  uint16   BootOptionOnWatchDog;
  boolean  BootROMSupported;
  string   BootupState;
  uint16   BootStatus[];
  string   Caption;
  uint16   ChassisBootupState;
  string   ChassisSKUNumber;
  string   CreationClassName;
  sint16   CurrentTimeZone;
  boolean  DaylightInEffect;
  string   Description;
  string   DNSHostName;
  string   Domain;
  uint16   DomainRole;
  boolean  EnableDaylightSavingsTime;
  uint16   FrontPanelResetStatus;
  boolean  HypervisorPresent;
  boolean  InfraredSupported;
  string   InitialLoadInfo[];
  datetime InstallDate;
  uint16   KeyboardPasswordStatus;
  string   LastLoadInfo;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   NameFormat;
  boolean  NetworkServerModeEnabled;
  uint32   NumberOfLogicalProcessors;
  uint32   NumberOfProcessors;
  uint8    OEMLogoBitmap[];
  string   OEMStringArray[];
  boolean  PartOfDomain;
  sint64   PauseAfterReset;
  uint16   PCSystemType;
  uint16   PCSystemTypeEx;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerOnPasswordStatus;
  uint16   PowerState;
  uint16   PowerSupplyState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  sint16   ResetCount;
  sint16   ResetLimit;
  string   Roles[];
  string   Status;
  string   SupportContactDescription[];
  string   SystemFamily;
  string   SystemSKUNumber;
  uint16   SystemStartupDelay;
  string   SystemStartupOptions[];
  uint8    SystemStartupSetting;
  string   SystemType;
  uint16   ThermalState;
  uint64   TotalPhysicalMemory;
  string   UserName;
  uint16   WakeUpType;
  string   Workgroup;
};
```

## <a name="members"></a>Member

Die **Win32- \_ Computersystem** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32- \_ Computersystem** -Klasse verfügt über diese Methoden.



| Methode                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**JoinDomainOrWorkgroup**](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | Fügt einer Domäne oder Arbeitsgruppe ein Computersystem hinzu.<br/>                                                                                                                                                                                   |
| [**Benen**](rename-method-in-class-win32-computersystem.md)                                   | Benennt einen lokalen Computer um.<br/>                                                                                                                                                                                                          |
| **SetPowerState**                                                                               | Nicht implementiert. Weitere Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md).<br/> |
| [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | Entfernt ein Computersystem aus einer Domäne oder Arbeitsgruppe.<br/>                                                                                                                                                                              |



 

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ Computersystem** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Adminpasswordstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 24 \| Hardware Sicherheitseinstellungen \| adminpasswordstatus")
</dt> </dl>

System Hardware-Sicherheitseinstellungen für den Status des Administrator Kennworts.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Nicht implementiert** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticManagedPagefile**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

**True** gibt an, dass das System die Auslagerungs Datei verwaltet.

</dd> <dt>

**Automatikresetbootoption**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| AutoReboot")
</dt> </dl>

**True** gibt an, dass die Startoption für automatisches Zurücksetzen aktiviert ist.

</dd> <dt>

**Automatikresetcapability**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

**True** gibt an, dass die automatische zurück Setzung aktiviert ist.

</dd> <dt>

**Bootoptiononlimit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 23 \| Capabilites \| Boot Option on Limit")
</dt> </dl>

Das Limit für die Startoption ist on. Identifiziert die System Aktion, wenn der **resetLimit** -Wert erreicht wird.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reserviert** (0)


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**Betriebssystem** (1)


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**System Dienstprogramme** (2)


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

**Nicht neu starten** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Bootoptiononwatchdog**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 23- \| Funktionen- \| Start Option")
</dt> </dl>

Der Typ der Neustart Aktion nach dem Zeitpunkt, an dem der Watchdog-Timer abgelaufen ist.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reserviert** (0)


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**Betriebssystem** (1)


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**System Dienstprogramme** (2)


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

**Nicht neu starten** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Bootrompeten unterstützt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

**True** gibt an, ob eine Start-ROM unterstützt wird.

</dd> <dt>

**Bootstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 32 \| System Startinformationen \| Start Status")
</dt> </dl>

Status und zusätzliche Datenfelder, die den Startstatus identifizieren.

Dieser Wert stammt vom **Start Status** Mitglied der **System Start Informations** Struktur in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.

</dd> <dt>

**BootupState**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ CleanBoot")
</dt> </dl>

Das System wurde gestartet. Der ausfallsichere Start umgeht die Benutzer Startdateien, die auch "SafeBoot" genannt werden.

Die folgende Liste enthält die erforderlichen Werte:

<dl> <dd>"Normaler Start"</dd> <dd>"Ausfallsicherer Start"</dd> <dd>"Ausfallsicherheit beim Netzwerkstart"</dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

**Normaler Start** (normaler Start)


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

**Ausfallsicherer Start** ("ausfallsicherer Start")


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

**Ausfallsicherheit mit dem Netzwerkstart** ("Ausfallsicherheit beim Netzwerkstart")


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**ChassisBootupState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 3 \| bootup State")
</dt> </dl>

Startstatus des Chassis.

Dieser Wert stammt aus dem **Status des Start Zustands** des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**Safe** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Warnung** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Kritisch** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

**Nicht wiederherstellbar** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**Chassisskunverber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 3 \| Chassis- \| SKU-Nummer")
</dt> </dl>

Die SKU-Nummer des Chassis oder Gehäuses als Zeichenfolge.

Dieser Wert stammt aus dem **SKU-Nummer** -Member des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Name der ersten konkreten Klasse in der Vererbungs Kette einer Instanz. Sie können diese Eigenschaft mit anderen Eigenschaften der-Klasse verwenden, um alle Instanzen der-Klasse und ihrer Unterklassen zu identifizieren.

Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.

</dd> <dt>

**CurrentTimeZone**
</dt> <dd> <dl> <dt>

Datentyp: **sint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Zeitstrukturen \| [**Zeit \_ Zonen \_ Informationen**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| Bias"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Minuten")
</dt> </dl>

Die Zeitspanne, für die das einheitliche Computersystem von der koordinierten Weltzeit (UTC) versetzt wird.

</dd> <dt>

**DaylightInEffect**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Time Functions \| [**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")
</dt> </dl>

Wenn der Wert **true** ist, ist der sommermodus auf on.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**DNSHostName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| GetComputerNameEx \| ComputerNameDnsHostname")
</dt> </dl>

Der Name des lokalen Computers gemäß dem DNS (Domain Nameserver).

</dd> <dt>

**Domäne**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**wksta \_ Info \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ LANGroup")
</dt> </dl>

Der Name der Domäne, zu der ein Computer gehört.

> [!Note]  
> Wenn der Computer nicht Teil einer Domäne ist, wird der Name der Arbeitsgruppe zurückgegeben.

 

</dd> <dt>

**DomainRole**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Directory Service (DS) Structures \| [**DsRole \_ Primary \_ Domain \_ Info \_ Basic**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**DsRole \_ Machine \_ Role**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| machinerole")
</dt> </dl>

Rolle eines Computers in einer zugewiesenen Domänen Arbeitsgruppe. Eine Domänen Arbeitsgruppe ist eine Sammlung von Computern im gleichen Netzwerk. Beispielsweise kann eine **DomainRole** -Eigenschaft anzeigen, dass ein Computer Mitglied einer Arbeitsstation ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

**Eigenständige Arbeits** Station (0)


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

**Mitglieds** Arbeitsstation (1)


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

**Eigenständiger Server** (2)


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

**Mitglieds Server** (3)


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

**Domänen Controller sichern** (4)


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

**Primärer Domänen Controller** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Enabledaylightsavingstime**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Aktiviert die Sommerzeit (DST) auf einem Computer. Der Wert **true** gibt an, dass sich die Systemzeit vor oder nach dem Start oder Ende des DST auf eine Stunde vor oder nach dem Ende ändert. Der Wert **false** gibt an, dass die Systemzeit nicht in eine Stunde vor oder hinter dem DST beginnt oder endet. Der Wert **null** gibt an, dass der DST-Status in einem System unbekannt ist.

</dd> <dt>

**FrontPanelResetStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 24 \| Hardware Sicherheitseinstellungen \| FrontPanelResetStatus")
</dt> </dl>

In der folgenden Tabelle sind die Hardware Sicherheitseinstellungen für die Schaltfläche Zurücksetzen auf einem Computer aufgeführt.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Nicht implementiert** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Hypervisorpresent**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

**True** gibt an, dass ein Hypervisor vorhanden ist.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 8 und Windows Server 2012 nicht unterstützt.

</dd> <dt>

**Nicht unterstützt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

**True** gibt an, dass ein Infrarot-Port (IR) auf einem Computersystem vorhanden ist.

</dd> <dt>

**Initizuadinfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Daten, die für die Suche nach dem anfänglichen Lade Gerät oder Start Dienst erforderlich sind, um den Start des Betriebssystems anzufordern.

Diese Eigenschaft wird von [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)geerbt.

**Windows Server 2008 R2:** Diese Eigenschaft ist verfügbar, aber leer.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")
</dt> </dl>

Das Objekt ist installiert. Ein Objekt benötigt keinen Wert, um anzugeben, dass es installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**KeyboardPasswordStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 24 \| Hardware Sicherheitseinstellungen \| KeyboardPasswordStatus")
</dt> </dl>

System Hardware-Sicherheitseinstellungen für den Status des Tastatur Kennworts.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Nicht implementiert** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Lastloadinfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array Eintrag der **initizuadinfo** -Eigenschaft, die die Daten zum Starten des geladenen Betriebssystems enthält.

Diese Eigenschaft wird von [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)geerbt.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| Manufacturer")
</dt> </dl>

Name eines Computerherstellers.

Beispiel: Adventure Works

</dd> <dt>

**Modell**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| Product Name")
</dt> </dl>

Produktname, den ein Hersteller an einen Computer übergibt. Diese Eigenschaft muss über einen Wert verfügen.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Schlüssel einer [**CIM- \_ System**](cim-system.md) Instanz in einer Unternehmensumgebung.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computer System **namens** , der automatisch generiert wird. Das [**CIM \_ Computersystem**](cim-computersystem.md) -Objekt und seine Ableitungen sind Objekte der obersten Ebene des Common Information Model (CIM). Sie stellen den Bereich für verschiedene Komponenten bereit. Es sind eindeutige [**CIM- \_ System**](cim-system.md) Schlüssel erforderlich, Sie können jedoch eine Heuristik definieren, um den Namen des **CIM- \_ Computer Systems** zu erstellen, der denselben Namen generiert, und unabhängig vom Discovery-Protokoll. Dies verhindert Inventur-und Verwaltungsprobleme, wenn das gleiche Asset oder die gleiche Entität mehrmals erkannt wird, aber nicht in ein Objekt aufgelöst werden kann. Die Verwendung einer heuristischen Empfehlung wird empfohlen, ist jedoch nicht erforderlich.

Die Heuristik wird in der Common Model-Spezifikation von CIM V2 beschrieben und geht davon aus, dass die dokumentierten Regeln zum bestimmen und Zuweisen eines Namens verwendet werden. Die Liste **NameFormat** -Werte definiert die Reihenfolge, in der ein Computersystem Name zugewiesen werden soll. Mehrere Regeln werden demselben Wert zugeordnet.

Der Wert des [**CIM \_ Computersystem-namens**](cim-computersystem.md) , der mithilfe der Heuristik berechnet wird, ist der Schlüsselwert des Systems. Verwenden Sie jedoch Aliase, um einen anderen Namen für **CIM \_ Computersystem** zuzuweisen, der für Ihr Unternehmen eindeutiger ist.

Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.

Folgende Werte sind gültig:

<dt>

<span id="IP"></span><span id="ip"></span>

**IP** ("IP")


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

**Dial** ("Dial")


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

**HID** ("HID")


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

**NWA** ("NWA")


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

**Hwa** ("Hwa")


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

**X25** ("x25")


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

**ISDN** ("ISDN")


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

**IPX** ("IPX")


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

**DCC** ("DCC")


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

**ICD** ("ICD")


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

**E. 164** ("e. 164")


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**SNA** ("SNA")


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

**OID/OSI** ("OID/OSI")


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** ("Sonstige")


</dt> <dd></dd> </dl>

</dd> <dt>

**Network Server modefähig**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**Server \_ Info \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ Type \| SV \_ Type \_ Server")
</dt> </dl>

**True** gibt an, dass der Netzwerk Server Modus aktiviert ist.

</dd> <dt>

**"Numoflogicalprocessor"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Anzahl der auf dem Computer verfügbaren logischen Prozessoren.

Mithilfe von " **numoflogicalprocessor** " und " **numofprocessor** " können Sie ermitteln, ob der Computer Hyperthreading ist. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Structures \| [**System \_ Info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| dwnumofprocessor")
</dt> </dl>

Anzahl der physischen Prozessoren, die zurzeit auf einem System verfügbar sind. Dies ist die Anzahl der aktivierten Prozessoren für ein System, das die deaktivierten Prozessoren nicht einschließt. Wenn ein Computersystem über zwei physische Prozessoren verfügt, die jeweils zwei logische Prozessoren enthalten, ist der Wert von " **numofprocessor** " 2, und " **numoflogicalprocessor** " ist 4. Dabei kann es sich um mehr Kern Prozessoren oder um Hyperthreading-Prozessoren handeln. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**Oemlogobitmap**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Liste der Daten für eine Bitmap, die der Originalgerätehersteller (OEM) erstellt.

</dd> <dt>

**Oemstringarray**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 11 \| OEM Strings")
</dt> </dl>

Liste der frei Form Zeichenfolgen, die von einem OEM definiert werden. Ein OEM definiert z. b. die Teilenummern für System Verweis Dokumente, Hersteller Kontaktinformationen usw.

</dd> <dt>

**"Element Domäne"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

**True** gibt an, dass der Computer Teil einer Domäne ist. Wenn der Wert **null** ist, befindet sich der Computer nicht in einer Domäne, oder der Status ist unbekannt. Wenn Sie den Computer aus einer Domäne entfernen, wird der Wert **false**.

</dd> <dt>

**Pausegafterreset**
</dt> <dd> <dl> <dt>

Datentyp: **sint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 23 \| Timeout"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")
</dt> </dl>

Zeitverzögerung vor dem Initiieren eines Neustarts in Millisekunden. Es wird nach einem System Energie-, System-oder Remote System-Reset und automatischer System Zurücksetzung verwendet. Der Wert 1 (minus 1) gibt an, dass der Pausen Wert unbekannt ist.

**Windows Vista:** Diese Eigenschaft gibt möglicherweise eine unbekannte Zahl zurück.

</dd> <dt>

**Pcsystemtype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Typ des verwendeten Computers, z. b. Laptop, Desktop oder Tablet.

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Nicht angegeben** (0)


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (1)


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Mobil** (2)


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Arbeits** Station (3)


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4)


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**Soho-Server** (5)


</dt> <dd>

Small Office-und Home Office-Server (Soho)

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**Appliance-PC** (6)


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Leistungs Server** (7)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**Pcsystemtypeex**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Typ des verwendeten Computers, z. b. Laptop, Desktop oder Tablet.

**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

**Nicht angegeben** (0)


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

**Desktop** (1)


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

**Mobil** (2)


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

**Arbeits** Station (3)


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

**Enterprise Server** (4)


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

**Soho-Server** (5)


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

**Appliance-PC** (6)


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

**Leistungs Server** (7)


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

**Slate** (8)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Maximum** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Powermanagementfunktionen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Energiesteuerung \| 001,2 ")
</dt> </dl>

Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.

Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)


</dt> <dd>

Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)


</dt> <dd>

Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)


</dt> <dd>

Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt. Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden. Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)


</dt> <dd>

Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)


</dt> <dd>

Zeitgesteuerte Power-On unterstützt

Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.

</dd> </dl>

</dd> <dt>

**Powermanagementsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass das Gerät Energie gesteuert werden kann, z. b. Wenn ein Gerät in den Unterbrechungs Modus versetzt werden kann usw. Diese Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen derzeit aktiviert sind, gibt jedoch an, dass das logische Gerät für die Energie Verwaltung geeignet ist.

Diese Eigenschaft wird von [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)geerbt.

</dd> <dt>

**PowerOnPasswordStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 24 \| Hardware Sicherheitseinstellungen \| PowerOnPasswordStatus")
</dt> </dl>

System Hardware-Sicherheitseinstellungen für Power-On Kenn Wort Status

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Nicht implementiert** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**PowerState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktueller Energiezustand eines Computers und des zugehörigen Betriebssystems. Die Energiespar Zustände weisen die folgenden Werte auf: Wert 4 (unbekannt) gibt an, dass sich das System bekanntermaßen in einem Energiesparmodus befindet, aber der genaue Status in diesem Modus ist unbekannt. 2 (niedriger Energie Modus) zeigt an, dass sich das System in einem Energiespar Zustand befindet, aber noch funktionsfähig ist und eine Beeinträchtigung der Leistung aufweisen kann. 3 (Standby) gibt an, dass das System nicht funktioniert, aber schnell in den vollständigen Energiesparmodus versetzt werden kann. und 7 (Warnung) gibt an, dass sich das Computersystem in einem Warnungs Status und in einem Energiesparmodus befindet.

Diese Eigenschaft wird von [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Vollstrom** (1)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (2)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (3)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (4)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (5)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (6)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (7)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Energiespar Speicher-** Ruhezustand (8)


</dt> <dd>

Energie sparen Sie den Ruhezustand.

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save-Soft Off** (9)


</dt> <dd>

Power Save Soft aus.

</dd> </dl>

</dd> <dt>

**PowerSupplyState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 3- \| System Gehäuse oder Gehäuse \| Stromversorgung-Status")
</dt> </dl>

Der Status der Stromversorgung oder der Bereitstellung beim letzten starten.

Dieser Wert stammt **aus dem** statusstatusmember des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.

In der folgenden Liste sind die Werte für diese Eigenschaft aufgeführt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Safe** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Nicht wiederherstellbar** (6)


</dt> <dd>

Nicht BEHEB barer

</dd> </dl>

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kontaktinformationen für den primären Systembesitzer, z. b. Telefonnummer, e-Mail-Adresse usw.

Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.

</dd> <dt>

**Primaryownername**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Der Name des primären System Besitzers.

Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.

</dd> <dt>

**Resetcapability**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| System Hardware Security \| 001,4 ")
</dt> </dl>

Wenn diese Option aktiviert ist, ist der Wert 4, und das einheitliche Computersystem kann mithilfe der Schaltflächen Strom und Zurücksetzen zurückgesetzt werden. Wenn diese Option deaktiviert ist, ist der Wert 3, und eine zurück Setzung ist nicht zulässig.

Diese Eigenschaft wird von [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (4)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Nicht implementiert** (5)


</dt> <dd>

Nicht BEHEB barer

</dd> </dl>

</dd> <dt>

**ResetCount**
</dt> <dd> <dl> <dt>

Datentyp: **sint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 23 \| Systemreset \| Reset count")
</dt> </dl>

Anzahl der automatischen zurück setzungen seit dem letzten Zurücksetzen. Der Wert 1 (minus 1) gibt an, dass die Anzahl unbekannt ist.

</dd> <dt>

**ResetLimit**
</dt> <dd> <dl> <dt>

Datentyp: **sint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 23 \| System Reset \| Reset Limit")
</dt> </dl>

Anzahl der aufeinander folgenden Versuche beim Zurücksetzen des Systems. Der Wert 1 (minus 1) gibt an, dass der Grenzwert unbekannt ist.

</dd> <dt>

**Rollen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Liste, in der die Rollen eines Systems in der Informationstechnologie Umgebung angegeben werden.

Diese Eigenschaft wird vom [**CIM- \_ System**](cim-system.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Aktueller Status eines Objekts.

Für Win32_ComputerSystem lautet der Status immer "OK".

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dl>

</dd> <dt>

**Supportcontactdescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \| Support Information")
</dt> </dl>

Liste der Kontaktinformationen des Supports für das Windows-Betriebssystem.

</dd> <dt>

**Systemfamilie**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| Family")
</dt> </dl>

Die Familie, zu der ein bestimmter Computer gehört. Eine Familie bezieht sich auf eine Gruppe von Computern, die einer Hardware-oder Software Sicht ähnlich, aber nicht identisch sind.

Dieser Wert stammt aus dem **Familien** Mitglied der **System Informations** Struktur in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.

</dd> <dt>

**SystemSKUNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| SKU Number")
</dt> </dl>

Identifiziert eine bestimmte Computerkonfiguration für den Verkauf. Manchmal auch als Produkt-ID oder Bestellnummer bezeichnet.

Dieser Wert stammt aus dem **SKU-Nummern** Element der **System Informations** Struktur in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.

</dd> <dt>

**SystemStartupDelay**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Berechtigungen**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sesystemumgebungsprivileg"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**getprivateprofileint**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| Boot Loader \| Timeout"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sekunden")
</dt> </dl>

**SystemStartupDelay** ist nicht mehr zur Verwendung verfügbar, da Boot.ini nicht zum Konfigurieren des Systemstarts verwendet wird. Verwenden Sie stattdessen die vom WMI-Anbieter für Startkonfigurationsdaten (BCD) oder den Befehl **Bcdedit** bereitgestellten [BCD-Klassen](/previous-versions/windows/desktop/bcd/bcd-classes) .

</dd> <dt>

**SystemStartupOptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Berechtigungen**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sesystemumgebungprivileg"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \| Operating Systems")
</dt> </dl>

**SystemStartupOptions** ist nicht mehr zur Verwendung verfügbar, da Boot.ini nicht zum Konfigurieren des Systemstarts verwendet wird. Verwenden Sie stattdessen die vom WMI-Anbieter für Startkonfigurationsdaten (BCD) oder den Befehl **Bcdedit** bereitgestellten [BCD-Klassen](/previous-versions/windows/desktop/bcd/bcd-classes) .

</dd> <dt>

**Systemstartupsetting**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Berechtigungen**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sesystemumgebtungprivilege"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

**Systemstartupsetting** ist nicht mehr zur Verwendung verfügbar, da Boot.ini nicht zum Konfigurieren des Systemstarts verwendet wird. Verwenden Sie stattdessen die vom WMI-Anbieter für Startkonfigurationsdaten (BCD) oder den Befehl **Bcdedit** bereitgestellten [BCD-Klassen](/previous-versions/windows/desktop/bcd/bcd-classes) .

</dd> <dt>

**System Type**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Structures \| [**System \_ Info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| wprocessorarchitecture")
</dt> </dl>

System, das auf dem Windows-basierten Computer ausgeführt wird. Diese Eigenschaft muss über einen Wert verfügen.

In der folgenden Liste sind einige der möglichen Werte für diese Eigenschaft aufgeführt.

<dl> <dd>"x64-basierter PC"</dd> <dd>"X86-basierter PC"</dd> <dd>"MIPS-basierter PC"</dd> <dd>"Alpha basierter PC"</dd> <dd>"Power PC"</dd> <dd>"Sh-x PC"</dd> <dd>"StrongARM-PC"</dd> <dd>"64-Bit-Intel-PC"</dd> <dd>"64-Bit-Alpha-PC"</dd> <dd>Unbekannter</dd> <dd>"X86-Nec98 PC"</dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

**X86-basierter PC** (x86-basierter PC)


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

**MIPS-basierter PC** ("MIPS-basierter PC")


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

**Alpha basierter PC** ("Alpha basierter PC")


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

**Power PC** ("Power PC")


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

**SH-x PC** ("sh-x PC")


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

**StrongARM-PC** ("StrongARM-PC")


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

**64-Bit-Intel-PC** ("64-Bit Intel PC")


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

**x64-basierter PC** ("x64-basierter PC")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("unbekannt")


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

**X86-Nec98 PC** ("x86-Nec98 PC")


</dt> <dd></dd> </dl>

</dd> <dt>

**Thermalzustand**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS- \| Typ 3- \| System Gehäuse oder Gehäuse- \| wärmezustand")
</dt> </dl>

Der thermische Zustand des Systems beim letzten starten.

Dieser Wert stammt aus dem **wärmestatusmember** des **System Gehäuses oder der Gehäuse** Struktur in den SMBIOS-Informationen.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**Safe** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Warnung** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Kritisch** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

**Nicht wiederherstellbar** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**TotalPhysicalMemory**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Memory Management Structures \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| dwTotalPhys"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")
</dt> </dl>

Gesamtgröße des physischen Speichers. Beachten Sie, dass diese Eigenschaft unter bestimmten Umständen keinen exakten Wert für den physischen Arbeitsspeicher zurückgibt. Beispielsweise ist es nicht korrekt, wenn das BIOS einen Teil des physischen Speichers verwendet. Verwenden Sie für einen exakten Wert stattdessen die **Capacity** -Eigenschaft im [**Win32- \_ PhysicalMemory**](win32-physicalmemory.md) .

Beispiel: 67108864

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Functions \| [**GetUsername**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")
</dt> </dl>

Der Name eines Benutzers, der zurzeit angemeldet ist. Diese Eigenschaft muss über einen Wert verfügen. In einer Terminaldienste-Sitzung gibt **username** den Namen des Benutzers zurück, der bei der Konsole nicht angemeldet ist, nicht den Benutzer, der während der Terminaldienst Sitzung angemeldet ist.

Beispiel: JeffSmith

</dd> <dt>

**Wakeuptype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information Reaktivierungs \| Type")
</dt> </dl>

Das Ereignis bewirkt, dass das System aufschlägt.

Dieser Wert stammt aus dem Reaktivierungs **-Typmember** der **System Informations** Struktur in den SMBIOS-Informationen.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reserviert** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="APM_Timer"></span><span id="apm_timer"></span><span id="APM_TIMER"></span>

**APM-Timer** (3)


</dt> <dd></dd> <dt>

<span id="Modem_Ring"></span><span id="modem_ring"></span><span id="MODEM_RING"></span>

**Modem Ring** (4)


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

**LAN-Remote** (5)


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

**Netzschalter** (6)


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

**PCI-PME \#** 19.00


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

**Stromversorgung wieder hergestellt** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**Arbeitsgruppe**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Der Name der Arbeitsgruppe für diesen Computer. Wenn der Wert der Eigenschaft " **Parser** " auf " **false**" festgelegt ist, wird der Name der Arbeitsgruppe zurückgegeben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die [**Win32 \_ computersystemprocessor**](win32-computersystemprocessor.md) Association-Klasse, um die Gesamtanzahl der Prozessor Instanzen zu ermitteln, die einem Computersystem Objekt zugeordnet sind.

Eine **Win32- \_ Computersystem** Instanz, der mehrere physische Prozessoren zugeordnet sind, sind mehrere [**Win32- \_ Prozessor**](win32-processor.md) Instanzen zugeordnet. Wenn der Wert von " **numoflogicalprocessor** " größer als der Wert von " **numofprocessor** " ist, handelt es sich bei dem Computersystem entweder um ein Multikernsystem oder um einen oder mehrere Prozessoren, die für Hyperthreading aktiviert sind. Weitere Informationen finden Sie im Abschnitt **zu den Eigenschaften** und Hinweisen im Abschnitt **"Eigenschaften und** Hinweise" im Win32- **\_ Prozessor**.

Die **Win32- \_ Computersystem** -Klasse wird von [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)abgeleitet.

## <a name="examples"></a>Beispiele

Im folgenden Skript Center- [Codebeispiel](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) wird das **Win32- \_ Computersystem** verwendet, um Informationen aus einer Reihe von Computersystemen abzurufen und in einer GUI anzuzeigen.

Ein Beispielskript, das Betriebssystem-und Prozessor Daten von **Win32 \_ Computersystem**, [**Win32 \_ Processor**](win32-processor.md)und [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) abruft, finden Sie in den Beispielen zu [**Win32- \_ Prozessor**](win32-processor.md) Themen.

Im folgenden VBScript-Beispiel wird beschrieben, wie der Domänen Name des lokalen Computers aus Instanzen von **Win32 \_ Computersystem** abgerufen wird.


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



Im folgenden Perl-Beispiel wird beschrieben, wie der lokale Computername aus den Instanzen von **Win32 \_ Computersystem** abgerufen wird.


```
use strict;
use Win32::OLE;

my ($SystemSet, $System);  
eval {$SystemSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("Win32_ComputerSystem") };
  
unless($@)
{
 foreach $System (in $SystemSet)
 {
  print "\n", $System->{Domain}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



Im folgenden Perl-Beispiel wird beschrieben, wie der DNS-Domänen Name des lokalen Computers aus Instanzen von **Win32 \_ Computersystem** abgerufen wird.


```
use strict;
use Win32::OLE;

close (STDERR);

my ($NICSet, $NIC);  
eval {$NICSet = Win32::OLE->GetObject("winmgmts:!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=true"); };
if (!$@ && defined $NICSet)
{
 foreach $NIC (in $NICSet)
 {
  if(defined $NIC->{DNSDomain})
  {
   print "\n", $NIC->{DNSDomain}, "\n";
  }
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[WMI-Tasks: Konten und Domänen](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[WMI-Tasks: Computer Hardware](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[WMI-Tasks: Desktop Verwaltung](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

