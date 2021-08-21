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
ms.openlocfilehash: 6c6a2d965a764be8925fda55958302d815b62ad6180ce4d3abb48d399fc2e817
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119700000"
---
# <a name="win32_computersystem-class"></a>Win32 \_ ComputerSystem-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ ComputerSystem** stellt ein Computersystem dar, auf dem Windows ausgeführt wird.

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

Die **Win32 \_ ComputerSystem-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ ComputerSystem-Klasse** verfügt über diese Methoden.



| Methode                                                                                          | Beschreibung                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**JoinDomainOrWorkgroup**](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | Fügt einer Domäne oder Arbeitsgruppe ein Computersystem hinzu.<br/>                                                                                                                                                                                   |
| [**Umbenennen**](rename-method-in-class-win32-computersystem.md)                                   | Benennt einen lokalen Computer um.<br/>                                                                                                                                                                                                          |
| **SetPowerState**                                                                               | Nicht implementiert. Weitere Informationen zum Implementieren dieser Methode finden Sie unter der [**SetPowerState-Methode**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).<br/> |
| [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | Entfernt ein Computersystem aus einer Domäne oder Arbeitsgruppe.<br/>                                                                                                                                                                              |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ ComputerSystem-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AdminPasswordStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| Hardware Security Einstellungen \| AdminPasswordStatus")
</dt> </dl>

Systemhardware-Sicherheitseinstellungen für den Administratorkennwortstatus.

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

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

**True** gibt an, dass das System die Seitendatei verwaltet.

</dd> <dt>

**AutomaticResetBootOption**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE \_ SYSTEM \\ \\ \\ \\ CurrentControlSet Control \\ \\ \\ \\ CrashControl \| AutoReboot")
</dt> </dl>

**True** gibt an, dass die Startoption für automatisches Zurücksetzen aktiviert ist.

</dd> <dt>

**AutomaticResetCapability**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

**True** gibt an, dass die automatische Zurücksetzung aktiviert ist.

</dd> <dt>

**BootOptionOnLimit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) \| ("SMBIOS Type 23 \| Capabilites \| Boot Option on Limit")
</dt> </dl>

Startoptionslimit ist ON. Identifiziert die Systemaktion, wenn der **ResetLimit-Wert** erreicht wird.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reserviert** (0)


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**Betriebssystem** (1)


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**Systemprogramme** (2)


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

**Nicht neu starten** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**BootOptionOnWatchDog**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) \| ("SMBIOS Type 23 \| Capabilities \| Boot Option")
</dt> </dl>

Typ der Neustartaktion, nachdem die Zeit auf dem Watchdog-Timer verstrichen ist.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reserviert** (0)


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**Betriebssystem** (1)


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**Systemprogramme** (2)


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

**Nicht neu starten** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**BootROMSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

**True** gibt an, ob ein Start-ROM unterstützt wird.

</dd> <dt>

**BootStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) \| ("SMBIOS Type 32 \| System Boot Information Boot \| Status")
</dt> </dl>

Die Felder Status und Zusätzliche Daten, die den Startstatus identifizieren.

Dieser Wert stammt aus dem **Boot Status-Member** der **System Boot Information-Struktur** in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.

</dd> <dt>

**BootupState**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ CLEANBOOT")
</dt> </dl>

Das System wird gestartet. Bei einem ausfallsicheren Start werden die Benutzerstartdateien umgangen, die auch als SafeBoot bezeichnet werden.

Die folgende Liste enthält die erforderlichen Werte:

<dl> <dd>"Normaler Start"</dd> <dd>"Ausfallsicherer Start"</dd> <dd>"Ausfallsicherheit beim Netzwerkstart"</dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

**Normaler Start** ("Normaler Start")


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

**Ausfallsicherer Start** ("Ausfallsicherer Start")


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

**Ausfallsicherheit beim Netzwerkstart** ("Ausfallsicher beim Netzwerkstart")


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Kurze Beschreibung des Objekts, eine einzeilige Zeichenfolge.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**ChassisBootupState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 3 \| Bootup State")
</dt> </dl>

Startzustand des Gehäuses.

Dieser Wert stammt aus dem **Startstatus-Member** der **Systemgehäuse-** oder Gehäusestruktur in den SMBIOS-Informationen.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**Tresor** (3)


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

**ChassisSKUNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 3 \| Chassis \| SKU Number")
</dt> </dl>

Die Gehäuse- oder Gehäuse-SKU-Nummer als Zeichenfolge.

Dieser Wert stammt aus dem **SKU-Nummer-Member** der **Systemgehäuse-** oder Gehäusestruktur in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird nicht unterstützt, bevor Windows 10 und Windows Server 2016.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **\_ CIM-Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Name der ersten konkreten Klasse in der Vererbungskette einer Instanz. Sie können diese Eigenschaft mit anderen Eigenschaften der -Klasse verwenden, um alle Instanzen der -Klasse und deren Unterklassen zu identifizieren.

Diese Eigenschaft wird vom [**\_ CIM-System geerbt.**](cim-system.md)

</dd> <dt>

**CurrentTimeZone**
</dt> <dd> <dl> <dt>

Datentyp: **sint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Time Structures TIME ZONE \| [**\_ \_ INFORMATION**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| Bias"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")
</dt> </dl>

Die Zeit, für die das unitäre Computersystem von koordinierte Weltzeit (UTC) versetzt wird.

</dd> <dt>

**DaylightInEffect**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Time Functions \| [**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")
</dt> </dl>

True **gibt an,** dass der Sommerzeitmodus aktiviert ist.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Dnshostname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| GetComputerNameEx \| ComputerNameDnsHostname")
</dt> </dl>

Name des lokalen Computers gemäß dem Domänennamenserver (DNS).

</dd> <dt>

**Domain**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Netzwerkverwaltungsstrukturen \| \| [**WKSTA \_ INFO \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ langroup")
</dt> </dl>

Name der Domäne, zu der ein Computer gehört.

> [!Note]  
> Wenn der Computer nicht Teil einer Domäne ist, wird der Name der Arbeitsgruppe zurückgegeben.

 

</dd> <dt>

**DomainRole**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Directory Service (Ds) Structures \| [**DSROLE \_ PRIMARY DOMAIN INFO \_ \_ \_ BASIC**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**DSROLE \_ MACHINE \_ ROLE**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| MachineRole")
</dt> </dl>

Rolle eines Computers in einer zugewiesenen Domänenarbeitsgruppe. Eine Domänenarbeitsgruppe ist eine Sammlung von Computern im gleichen Netzwerk. Beispielsweise kann eine **DomainRole-Eigenschaft** anzeigen, dass ein Computer eine Mitgliedsarbeitsstation ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

**Eigenständige Arbeitsstation** (0)


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

**Mitgliedsarbeitsstation** (1)


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

**Eigenständiger Server** (2)


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

**Mitgliedsserver** (3)


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

**Sicherungsdomänencontroller** (4)


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

**Primärer Domänencontroller** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**EnableDaylightSavingsTime**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Aktiviert die Sommerzeit (DST) auf einem Computer. Der Wert **True gibt an,** dass sich die Systemzeit in eine Stunde vor oder hinter dem Start oder Ende des DST ändert. Der Wert **False gibt an,** dass sich die Systemzeit nicht in eine Stunde vor oder hinter ändert, wenn DST beginnt oder endet. Der Wert **NULL gibt an,** dass der DST-Status auf einem System unbekannt ist.

</dd> <dt>

**FrontPanelResetStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| Hardware Security Einstellungen \| FrontPanelResetStatus")
</dt> </dl>

In der folgenden Tabelle sind die Hardwaresicherheitseinstellungen für die Zurücksetzungsschaltfläche auf einem Computer aufgeführt.

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

**HypervisorPresent**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

True **gibt an,** dass ein Hypervisor vorhanden ist.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird nicht unterstützt, bevor Windows 8 und Windows Server 2012.

</dd> <dt>

**Supported (2017)**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

True **gibt an,** dass auf einem Computersystem ein Ir-Port vorhanden ist.

</dd> <dt>

**InitialLoadInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Daten, die zum Suchen des anfänglichen Ladegeräts oder Startdiensts erforderlich sind, um die Betriebssystemstartanforderung zu erhalten.

Diese Eigenschaft wird von [**CIM \_ UnitaryComputerSystem geerbt.**](cim-unitarycomputersystem.md)

**Windows Server 2008 R2:** Diese Eigenschaft ist verfügbar, aber leer.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installation date")
</dt> </dl>

Das Objekt ist installiert. Ein Objekt benötigt keinen Wert, um anzugeben, dass es installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**KeyboardPasswordStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| Hardware Security Einstellungen \| KeyboardPasswordStatus")
</dt> </dl>

Systemhardwaresicherheitseinstellungen für Tastaturkennwortstatus.

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

**LastLoadInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Arrayeintrag der **InitialLoadInfo-Eigenschaft,** die die Daten zum Starten des geladenen Betriebssystems enthält.

Diese Eigenschaft wird von [**CIM \_ UnitaryComputerSystem geerbt.**](cim-unitarycomputersystem.md)

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| Systeminformationen \| Manufacturer")
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

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| Systeminformationen Product \| Name")
</dt> </dl>

Der Produktname, den ein Hersteller einem Computer gibt. Diese Eigenschaft muss einen -Wert haben.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Schlüssel einer [**\_ CIM-Systeminstanz**](cim-system.md) in einer Unternehmensumgebung.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name des **Computersystems,** der automatisch generiert wird. Das [**\_ CIM-ComputerSystem-Objekt**](cim-computersystem.md) und seine Ableitungen sind Objekte der obersten Ebene des Common Information Model (CIM). Sie stellen den Bereich für mehrere Komponenten zur Verfügung. Eindeutige [**\_ CIM-Systemschlüssel**](cim-system.md) sind erforderlich, aber Sie können eine Heuristik definieren, um den **\_ CIM-ComputerSystemnamen** zu erstellen, der den gleichen Namen generiert und unabhängig vom Ermittlungsprotokoll ist. Dies verhindert Inventur- und Verwaltungsprobleme, wenn dieselbe Ressource oder Entität mehrmals gefunden wird, aber nicht in ein Objekt aufgelöst werden kann. Die Verwendung einer Heuristik wird empfohlen, ist aber nicht erforderlich.

Die Heuristik wird in der CIM V2 Common Model-Spezifikation beschrieben und setzt voraus, dass die dokumentierten Regeln zum Bestimmen und Zuweisen eines Namens verwendet werden. Die **NameFormat-Werteliste** definiert die Reihenfolge, in der ein Computersystemname zugewiesen werden soll. Mehrere Regeln sind demselben Wert zuordnen.

Der [**\_ Cim-ComputerSystemname,**](cim-computersystem.md) der mithilfe der Heuristik berechnet wird, ist der Schlüsselwert des Systems. Verwenden Sie jedoch Aliase, um **CIM \_ ComputerSystem** einen anderen Namen zu geben, der für Ihr Unternehmen eindeutiger sein kann.

Diese Eigenschaft wird vom [**\_ CIM-System geerbt.**](cim-system.md)

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

**HWA** ("HWA")


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

**X25** ("X25")


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

**E.164** ("E.164")


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**SNA** ("SNA")


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

**OID/OSI** ("OID/OSI")


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstiges** ("Sonstige")


</dt> <dd></dd> </dl>

</dd> <dt>

**NetworkServerModeEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SERVER INFO \| [**\_ \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ type SV TYPE \| \_ \_ SERVER")
</dt> </dl>

True **gibt an,** dass der Netzwerkservermodus aktiviert ist.

</dd> <dt>

**NumberOfLogicalProcessors**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Anzahl der auf dem Computer verfügbaren logischen Prozessoren.

Sie können **NumberOfLogicalProcessors** und **NumberOfProcessors** verwenden, um zu ermitteln, ob der Computer Hyperthreading verwendet. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Systeminformationen Structures SYSTEM \| [**\_ INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| dwNumberOfProcessors")
</dt> </dl>

Anzahl der derzeit auf einem System verfügbaren physischen Prozessoren. Dies ist die Anzahl der aktivierten Prozessoren für ein System, die die deaktivierten Prozessoren nicht enthält. Wenn ein Computersystem über zwei physische Prozessoren verfügt, die jeweils zwei logische Prozessoren enthalten, ist der Wert von **NumberOfProcessors** 2 und **NumberOfLogicalProcessors** gleich 4. Die Prozessoren können mehrere Kerne oder Hyperthreadingprozessoren sein. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**OEMLogoBitmap**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Liste der Daten für eine Bitmap, die der Originalgerätehersteller (Original Equipment Manufacturer, OEM) erstellt.

</dd> <dt>

**OEMStringArray**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 11 \| OEM Strings")
</dt> </dl>

Liste der freiformbasierten Zeichenfolgen, die ein OEM definiert. Beispielsweise definiert ein OEM die Teilenummern für Systemverweisdokumente, Kontaktinformationen des Herstellers und so weiter.

</dd> <dt>

**PartOfDomain**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

True **gibt an,** dass der Computer Teil einer Domäne ist. Wenn der Wert **NULL ist,** befindet sich der Computer nicht in einer Domäne, oder der Status ist unbekannt. Wenn Sie den Computer aus einer Domäne entfernen, wird der Wert **false.**

</dd> <dt>

**PauseAfterReset**
</dt> <dd> <dl> <dt>

Datentyp: **sint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 23 \| Timeout"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")
</dt> </dl>

Zeitverzögerung vor dem Starten eines Neustarts in Millisekunden. Sie wird nach einem Systemleistungszyklus, der lokalen oder Remotesystemzurücksetzung und der automatischen Systemzurücksetzung verwendet. Der Wert 1 (minus 1) gibt an, dass der Pausenwert unbekannt ist.

**Windows Vista:** Diese Eigenschaft gibt möglicherweise eine unbekannte Zahl zurück.

</dd> <dt>

**PCSystemType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Typ des computers, der verwendet wird, z. B. Laptop, Desktop oder Tablet.

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

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Arbeitsstation** (3)


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4)


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**SOHO-Server** (5)


</dt> <dd>

Small Office and Home Office (SOHO) Server

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**Appliance-PC** (6)


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Leistungsserver** (7)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**PCSystemTypeEx**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Typ des computers, der verwendet wird, z. B. Laptop, Desktop oder Tablet.

**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor dem Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

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

**Arbeitsstation** (3)


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

**Enterprise Server** (4)


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

**SOHO-Server** (5)


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

**Appliance-PC** (6)


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

**Leistungsserver** (7)


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

**Slate** (8)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Maximum** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Power Controls \| 001.2")
</dt> </dl>

Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.

Diese Eigenschaft wird von **CIM \_ LogicalDevice geerbt.**

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

Die Energieverwaltungsfeatures sind derzeit aktiviert, aber der genaue Funktionssatz ist unbekannt, oder die Informationen sind nicht verfügbar.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiesparmodi** (4)


</dt> <dd>

Das Gerät kann seinen Energiezustand basierend auf der Nutzung oder anderen Kriterien ändern.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)


</dt> <dd>

Die [**SetPowerState-Methode**](setpowerstate-method-in-class-cim-controller.md) wird unterstützt. Diese Methode befindet sich in der übergeordneten **CIM \_ LogicalDevice-Klasse** und kann implementiert werden. Weitere Informationen finden Sie unter [Entwerfen Managed Object Format -Klassen (MOF).](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power-Bike unterstützt** (6)


</dt> <dd>

Die [**SetPowerState-Methode**](setpowerstate-method-in-class-cim-controller.md) kann mit dem *PowerState-Parameter* aufgerufen werden, der auf 5 (Power Cycle) festgelegt ist.

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)


</dt> <dd>

Timed Power-On Supported

Die [**SetPowerState-Methode**](setpowerstate-method-in-class-cim-controller.md) kann aufgerufen werden, wenn der *PowerState-Parameter* auf 5 (Power Cycle) und *Time* auf ein bestimmtes Datum und eine bestimmte Uhrzeit oder ein bestimmtes Intervall für das Ein-/Aus-Setzen festgelegt ist.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass das Gerät mit Strom verwaltet werden kann, z. B. ein Gerät in den Modus "Aussetzen" wechseln kann und so weiter. Diese Eigenschaft gibt nicht an, dass energieverwaltungsfeatures derzeit aktiviert sind, aber sie gibt an, dass das logische Gerät energieverwaltungsfähig ist.

Diese Eigenschaft wird von [**CIM \_ UnitaryComputerSystem geerbt.**](cim-unitarycomputersystem.md)

</dd> <dt>

**PowerOnPasswordStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| Hardware Security Einstellungen \| PowerOnPasswordStatus")
</dt> </dl>

Systemhardwaresicherheitseinstellungen für Power-On Kennwortstatus.

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

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktueller Energiezustand eines Computers und des zugehörigen Betriebssystems. Die Energiesparzustände weisen die folgenden Werte auf: Wert 4 (Unbekannt) gibt an, dass das System bekannterweise im Energiesparmodus ist, aber sein genauer Status in diesem Modus unbekannt ist. 2 (Niedriger Energiemodus) gibt an, dass sich das System in einem Energiesparzustand befindet, aber weiterhin funktioniert und eine beeinträchtigte Leistung zeigen kann. 3 (Standby) gibt an, dass das System nicht funktioniert, aber schnell voll funktionsfähig sein könnte. und 7 (Warnung) geben an, dass sich das Computersystem in einem Warnzustand und im Energiesparmodus befindet.

Diese Eigenschaft wird von [**CIM \_ UnitaryComputerSystem geerbt.**](cim-unitarycomputersystem.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Vollleistung** (1)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Stromsparen – Niedriger Energiemodus** (2)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparen – Standby** (3)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiesparen – Unbekannt** (4)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energiezyklus** (5)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (6)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiesparen – Warnung** (7)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Energiesparen – Ruhezustand** (8)


</dt> <dd>

Energiesparen des Ruhezustands.

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Stromsparen – Soft Off** (9)


</dt> <dd>

Stromsparen – Soft-Off.

</dd> </dl>

</dd> <dt>

**PowerSupplyState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 3 \| System Enclosure or Chassis Power Supply \| State")
</dt> </dl>

Zustand der Stromversorgung oder der Stromversorgung beim letzten Start.

Dieser Wert stammt aus dem **Stromversorgungszustandsmember** der **Systemgehäuse- oder Gehäusestruktur** in den SMBIOS-Informationen.

Die folgende Liste identifiziert die Werte für diese Eigenschaft.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Tresor** (3)


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

Nicht behebbar

</dd> </dl>

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kontaktinformationen für den primären Systembesitzer, z. B. Telefonnummer, E-Mail-Adresse usw.

Diese Eigenschaft wird vom [**\_ CIM-System**](cim-system.md)geerbt.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Name des primären Systembesitzers.

Diese Eigenschaft wird vom [**\_ CIM-System**](cim-system.md)geerbt.

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Hardware Security \| 001.4")
</dt> </dl>

Wenn diese Option aktiviert ist, ist der Wert 4, und das unitäre Computersystem kann mithilfe der Ein- und Zurücksetzungsschaltflächen zurückgesetzt werden. Wenn diese Option deaktiviert ist, ist der Wert 3, und eine Zurücksetzung ist nicht zulässig.

Diese Eigenschaft wird von [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


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

Nicht behebbar

</dd> </dl>

</dd> <dt>

**ResetCount**
</dt> <dd> <dl> <dt>

Datentyp: **sint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 23 \| System Reset Reset \| Count")
</dt> </dl>

Anzahl der automatischen Zurücksetzungen seit der letzten Zurücksetzung. Der Wert 1 (minus eins) gibt an, dass die Anzahl unbekannt ist.

</dd> <dt>

**ResetLimit**
</dt> <dd> <dl> <dt>

Datentyp: **sint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) \| ("SMBIOS Type 23 \| System Reset \| Reset Limit")
</dt> </dl>

Anzahl aufeinanderfolgender Versuche, ein System zurückzusetzen. Der Wert 1 (minus 1) gibt an, dass der Grenzwert unbekannt ist.

</dd> <dt>

**Rollen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Liste, die die Rollen eines Systems in der IT-Umgebung angibt.

Diese Eigenschaft wird vom [**\_ CIM-System**](cim-system.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Aktueller Status eines Objekts.

Für Win32_ComputerSystem lautet der Status immer "OK".

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dl>

</dd> <dt>

**SupportContactDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetPrivateProfileString-Unterstützungsinformationen")**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \|
</dt> </dl>

Liste der Supportkontaktinformationen für das Windows Betriebssystem.

</dd> <dt>

**SystemFamily**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| Systeminformationen \| Family")
</dt> </dl>

Die Familie, zu der ein bestimmter Computer gehört. Eine Familie bezieht sich auf eine Gruppe von Computern, die aus Hardware- oder Softwaresicht ähnlich, aber nicht identisch sind.

Dieser Wert stammt aus dem **Family-Element** der **Systeminformationen-Struktur** in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.

</dd> <dt>

**SystemSKUNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS-Typ \| 1 \| Systeminformationen \| SKU-Nummer")
</dt> </dl>

Identifiziert eine bestimmte Computerkonfiguration für den Verkauf. Dies wird manchmal auch als Produkt-ID oder Bestellnummer bezeichnet.

Dieser Wert stammt aus dem **SKU-Nummer-Member** der **Systeminformationen-Struktur** in den SMBIOS-Informationen.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 10 und Windows Server 2016 nicht unterstützt.

</dd> <dt>

**SystemStartupDelay**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**VERALTET,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**Berechtigungen**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| Boot \| Loader-Timeout"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sekunden")
</dt> </dl>

**SystemStartupDelay** ist nicht mehr für die Verwendung verfügbar, da Boot.ini nicht zum Konfigurieren des Systemstarts verwendet wird. Verwenden Sie stattdessen die [BCD-Klassen,](/previous-versions/windows/desktop/bcd/bcd-classes) die vom WMI-Anbieter Startkonfigurationsdaten (BCD) oder vom **Bcdedit-Befehl** bereitgestellt werden.

</dd> <dt>

**SystemStartupOptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**VERALTET,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**Berechtigungen**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetPrivateProfileSection-Betriebssysteme")**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \|
</dt> </dl>

**SystemStartupOptions** ist nicht mehr für die Verwendung verfügbar, da Boot.ini nicht zum Konfigurieren des Systemstarts verwendet wird. Verwenden Sie stattdessen die [BCD-Klassen,](/previous-versions/windows/desktop/bcd/bcd-classes) die vom WMI-Anbieter Startkonfigurationsdaten (BCD) oder vom **Bcdedit-Befehl** bereitgestellt werden.

</dd> <dt>

**SystemStartupSetting**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**VERALTET,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**Berechtigungen**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

**SystemStartupSetting** kann nicht mehr verwendet werden, da Boot.ini systemstart nicht konfiguriert wird. Verwenden Sie stattdessen die [BCD-Klassen,](/previous-versions/windows/desktop/bcd/bcd-classes) die vom Startkonfigurationsdaten WMI-Anbieter (BCD) oder dem **Bcdedit-Befehl bereitgestellt** werden.

</dd> <dt>

**SystemType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Systeminformationen Structures SYSTEM \| [**\_ INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| wProcessorArchitecture")
</dt> </dl>

System, das auf dem Windows-basierten Computer ausgeführt wird. Diese Eigenschaft muss einen -Wert haben.

In der folgenden Liste sind einige der möglichen Werte für diese Eigenschaft aufgeführt.

<dl> <dd>"x64-basierter PC"</dd> <dd>"X86-basierter PC"</dd> <dd>"MIPS-basierter PC"</dd> <dd>"Alphabasierter PC"</dd> <dd>"Power PC"</dd> <dd>"SH-x PC"</dd> <dd>"StrongARM PC"</dd> <dd>"64-Bit Intel PC"</dd> <dd>"64-Bit-Alpha-PC"</dd> <dd>"Unbekannt"</dd> <dd>"X86-Nec98 PC"</dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

**X86-basierter PC** ("X86-basierter PC")


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

**MIPS-basierter PC** ("MIPS-basierter PC")


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

**Alphabasierter PC** ("Alphabasierter PC")


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

**Power PC** ("Power PC")


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

**SH-x PC** ("SH-x PC")


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

**StrongARM PC** ("StrongARM PC")


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

**64-Bit-Intel-PC** ("64-Bit Intel PC")


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

**x64-basierter PC** ("x64-basierter PC")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("Unbekannt")


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

**X86-Nec98 PC** ("X86-Nec98 PC")


</dt> <dd></dd> </dl>

</dd> <dt>

**ThermoState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 3 \| System Enclosure or Chassis Thermo \| State")
</dt> </dl>

Wärmezustand des Systems beim letzten Start.

Dieser Wert stammt aus dem **Wärmezustands-Member** der **Systemgehäuse-** oder Gehäusestruktur in den SMBIOS-Informationen.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**Tresor** (3)


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

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Memory Management Structures \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| dwTotalPhys"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Gesamtgröße des physischen Speichers. Beachten Sie, dass diese Eigenschaft unter bestimmten Umständen möglicherweise keinen genauen Wert für den physischen Speicher zurück gibt. Beispielsweise ist es nicht genau, wenn das BIOS einen Teil des physischen Speichers verwendet. Um einen genauen Wert zu erhalten, verwenden Sie stattdessen **die Capacity-Eigenschaft** in [**Win32 \_ PhysicalMemory.**](win32-physicalmemory.md)

Beispiel: 67108864

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Systeminformationen Functions \| [**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")
</dt> </dl>

Der Name eines Benutzers, der derzeit angemeldet ist. Diese Eigenschaft muss einen -Wert haben. In einer Terminaldienstsitzung gibt **UserName** den Namen des Benutzers zurück, der bei der Konsole angemeldet ist, nicht den Benutzer, der während der Terminaldienstsitzung angemeldet wurde.

Beispiel: jeffsmith

</dd> <dt>

**WakeUpType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS-Typ \| 1 \| Systeminformationen \| Aktivierungstyp")
</dt> </dl>

Das Ereignis, das dazu führt, dass das System aus- und hochs netzt.

Dieser Wert stammt aus dem **Member Aktivierungstyp** der Systeminformationen **struktur** in den SMBIOS-Informationen.

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

**Modemring** (4)


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

**LAN Remote** (5)


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

**Netzschalter** (6)


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

**PCI-PME \#** (7)


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

**Ac Power Restored** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**Arbeitsgruppe**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Name der Arbeitsgruppe für diesen Computer. Wenn der Wert der **PartOfDomain-Eigenschaft** **False ist,** wird der Name der Arbeitsgruppe zurückgegeben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie die [**Win32 \_ ComputerSystemProcessor-Zuordnungsklasse,**](win32-computersystemprocessor.md) um die Gesamtzahl der Prozessorinstanzen zu bestimmen, die einem Computersystemobjekt zugeordnet sind.

Einer **Win32 \_ ComputerSystem-Instanz,** die über mehrere physische Prozessoren verfügt, sind mehrere [**Win32-Prozessorinstanzen \_**](win32-processor.md) zugeordnet. Wenn der Wert von **NumberOfLogicalProcessors** größer als der Wert von **NumberOfProcessors** ist, ist das Computersystem entweder ein System mit mehreren Kernen oder verfügt über einen oder mehrere Prozessoren, die für Hyperthreading aktiviert sind. Weitere Informationen finden Sie im Abschnitt **NumberOfLogicalProcessors** and NumberOfCores properties and Remarks (Eigenschaften und Hinweise zu NumberOfLogicalProcessors und **NumberOfCores)** unter **Win32-Prozessor. \_**

Die **Win32 \_ ComputerSystem-Klasse** wird von [**CIM \_ UnitaryComputerSystem abgeleitet.**](cim-unitarycomputersystem.md)

## <a name="examples"></a>Beispiele

Im folgenden [Skriptcenter-Codebeispiel](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) wird **das Win32-Computersystem \_** verwendet, um Informationen aus einer Reihe von Computersystemen abzurufen und auf einer grafischen Benutzeroberfläche anzuzeigen.

Ein Beispielskript, das Betriebssystem- und Prozessordaten von **Win32 \_ ComputerSystem,** [**Win32 \_ Processor**](win32-processor.md)und [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) erhält, finden Sie in den Beispielen des [**Themas Win32-Prozessor. \_**](win32-processor.md)

Im folgenden VBScript-Beispiel wird beschrieben, wie der Domänenname des lokalen Computers aus Instanzen von **Win32 \_ ComputerSystem abgerufen wird.**


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



Im folgenden Perl-Beispiel wird beschrieben, wie der Name des lokalen Computers aus Instanzen von **Win32 \_ ComputerSystem abgerufen wird.**


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



Im folgenden Perl-Beispiel wird beschrieben, wie der DNS-Domänenname des lokalen Computers aus Instanzen von **Win32 \_ ComputerSystem abgerufen wird.**


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[WMI-Aufgaben: Konten und Domänen](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[WMI-Aufgaben: Computerhardware](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[WMI-Aufgaben: Desktopverwaltung](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

