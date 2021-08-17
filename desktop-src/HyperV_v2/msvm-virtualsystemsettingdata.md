---
description: Stellt die virtualisierungsspezifischen Einstellungen für einen virtuellen Computer dar.
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Msvm_VirtualSystemSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fb57c7b96a6e2cd1839f4d830074bb69d742aef688325a37d61b67589d026436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147893"
---
# <a name="msvm_virtualsystemsettingdata-class"></a>Msvm \_ VirtualSystemSettingData-Klasse

Stellt die virtualisierungsspezifischen Einstellungen für einen virtuellen Computer dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a>Member

Die **Msvm \_ VirtualSystemSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VirtualSystemSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AdditionalRecoveryInformation**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Alle zusätzlichen Informationen, die für die Wiederherstellungsaktion bereitgestellt werden. Die Bedeutung dieser Eigenschaft wird durch die Aktion in **AutomaticRecoveryAction definiert.** Wenn **AutomaticRecoveryAction** 0 ("None") oder 1 ("Restart") ist, ist dieser Wert **NULL.** Wenn **AutomaticRecoveryAction** den Wert 2 ("Auf Momentaufnahme wiederherstellen") beträgt, ist dies der Objektpfad zu einer Momentaufnahme, die bei einem Fehler des Workerprozesses des virtuellen Computers angewendet werden sollte.

</dd> <dt>

**AllowFullSCSICommandSet**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**TRUE,** wenn SCSI-Befehle aus dem Gastbetriebssystem an Pass-Through-Datenträger übergeben werden. andernfalls **False.** True **gibt an,** dass SCSI-Befehle, die vom Gastbetriebssystem an Pass-Through-Datenträger ausgegeben werden, nicht gefiltert werden. Es wird empfohlen, die SCSI-Filterung für Produktionsbereitstellungen aktiviert zu lassen.

</dd> <dt>

**AllowReducedFcRedundancy**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Livemigration eines virtuellen Computers, der mit einem virtuellen Fibre Channel-Adapter konfiguriert ist, auf einen Zielcomputer zulässig ist, der möglicherweise keine oder nur eingeschränkte Pfade zu den Zielcomputern Fibre Channel hat. Diese Eigenschaft sollte nach einer Livemigration entfernt werden.



| Wert                                                                            | Bedeutung                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>False</dt> </dl> | Der virtuelle Computer kann nicht live zu einem Zielcomputer migriert werden, der möglicherweise keine oder nur eingeschränkte Pfade zum Zielcomputer auf Fibre Channel hat.<br/>                                                                                                     |
| <dl> <dt>True</dt> </dl>  | Der virtuelle Computer kann live zu einem Zielcomputer migriert werden, der möglicherweise keine oder nur eingeschränkte Pfade zum Zielcomputer Fibre Channel hat. Das Gastbetriebssystem verliert möglicherweise die Verbindung mit dem Speicher und verhält sich möglicherweise unvorhersehbar.<br/> |



 

</dd> <dt>

**Architektur**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Architektur dieses Systems.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

<dt>

<span id="x64"></span><span id="X64"></span>

**x64** ()


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

**arm64** ()


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticCriticalErrorAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Identifiziert die Aktion, die auf dem virtuellen Computer ausgeführt werden soll, wenn ein kritischer Fehler auftritt, z. B. die Trennung der Speichertrennung.

> [!Note]  
> Hinzugefügt in Windows 10 und Windows Server 2016.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Keine** (0)


</dt> <dd>

Für kritische Fehlerbedingungen wird keine spezifische Aktion ergriffen.

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Fortsetzen anhalten** (1)


</dt> <dd>

Bewirkt, dass der virtuelle Computer angehalten und automatisch fortgesetzt wird, wenn der kritische Fehlerzustand behoben wird.

</dd> </dl>

</dd> <dt>

**AutomaticCriticalErrorActionTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**Untertyp**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("interval")
</dt> </dl>

Gibt die maximale Dauer an, für die **die AutomaticCriticalErrorAction** ausgeführt wird, um den kritischen Fehler zu beheben. Dies gilt nur, wenn der Wert der **AutomaticCriticalErrorAction-Eigenschaft** nicht 0 (None) ist. Nach Ablauf des Timeouts wird die VM ausgeschaltet. Der Wert wird auf die nächste Minute aufgerundet. Der Wert 0 impliziert, dass die VM sofort ausgeschaltet werden sollte, wenn eine kritische Fehlerbedingung auftritt.

> [!Note]  
> Hinzugefügt in Windows 10 und Windows Server 2016.

 

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktion, die für den virtuellen Computer ausgeführt werden soll, wenn die vom virtuellen Computer ausgeführte Software ausfällt. Fehler sind in diesem Fall ein Fehler, der von der Hostplattform erkannt werden kann, z. B. eine nicht unterbrechungsfreie Wartezustandsbedingung. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

Dies kann einer der folgenden Werte sein.



| Wert                                                                               | Bedeutung                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>2</dt> </dl>        | Keine.<br/>               |
| <dl> <dt>3</dt> </dl>        | Neu starten<br/>            |
| <dl> <dt>4</dt> </dl>        | Wiederherstellen der Momentaufnahme.<br/> |
| <dl> <dt>5..32768</dt> </dl> | Reserviert.<br/>           |



 

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktion, die für den virtuellen Computer ausgeführt werden soll, wenn der Host heruntergefahren wird. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

Dies kann einer der folgenden Werte sein.



| Wert                                                                               | Bedeutung                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <dt>2</dt> </dl>        | Ausschalten.<br/>   |
| <dl> <dt>3</dt> </dl>        | Speichern des Zustands.<br/> |
| <dl> <dt>4</dt> </dl>        | Herunterfahren<br/>   |
| <dl> <dt>5..32768</dt> </dl> | Reserviert.<br/>   |



 

</dd> <dt>

**AutomaticSnapshotsEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob für diesen virtuellen Computer automatische Momentaufnahmen aktiviert sein sollen.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktion, die für den virtuellen Computer ausgeführt werden soll, wenn der Host gestartet wird. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

Dies kann einer der folgenden Werte sein.



| Wert                                                                               | Bedeutung                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>2</dt> </dl>        | Keine.<br/>                         |
| <dl> <dt>3</dt> </dl>        | Starten Sie neu, wenn sie zuvor aktiv waren.<br/> |
| <dl> <dt>4</dt> </dl>        | Starten Sie immer.<br/>                 |
| <dl> <dt>5..32768</dt> </dl> | Reserviert.<br/>                     |



 

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Verzögerung bis zum automatischen Start des virtuellen Computers. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zahl, die die relative Sequenz der Aktivierung virtueller Computer angibt, wenn das Hostsystem gestartet wird. Eine niedrigere Zahl gibt eine frühere Aktivierung an. Wenn eine oder mehrere Konfigurationen den gleichen Wert anzeigen, ist die Sequenz von der Implementierung abhängig. Der Wert 0 gibt an, dass die Sequenz implementierungsabhängig ist. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**BaseBoardSerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Seriennummer des Basisboards für den virtuellen Computer.

</dd> <dt>

**BIOSGUID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der global eindeutige Bezeichner für das BIOS des virtuellen Computers.

</dd> <dt>

**BIOSNumLock**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**TRUE,** wenn der Num-Sperrschlüssel vom BIOS auf on festgelegt ist; **FALSE,** wenn die Num-Sperre durch das BIOS auf off festgelegt ist.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Seriennummer des BIOS für den virtuellen Computer.

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

Die startbasierte Reihenfolge, die im BIOS des virtuellen Computers festgelegt ist. Diese Eigenschaft ist ein Array von Werten, **BootOrder** \[ 0 \] bis **BootOrder** 3 , einschließlich , wobei jeder Wert ein Gerät angibt, von dem \[ aus gestartet werden \] soll. Jeder der vier Werte im Array muss festgelegt werden und darf nicht mit einem anderen Wert im Array identisch sein. Der virtuelle Computer versucht zunächst, von dem Gerät aus zu starten, das durch den ersten Wert im Array angegeben wird. Wenn dieses Gerät keinen Startsektor enthält, versucht der virtuelle Computer, von dem nächsten Gerät aus zu starten, das von der **BootOrder-Eigenschaft** angegeben wird, und so weiter. Wenn kein in der **BootOrder** angegebenes Gerät einen Startsektor enthält, kann der virtuelle Computer nicht gestartet werden. Der Standardwert für einen virtuellen Computer ist \[ 0, 1, 2, \] 3.

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Diskette** (0)


</dt> <dd>

Der virtuelle Computer versucht, von der Diskette auf dem Diskettenlaufwerk zu starten.

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)


</dt> <dd>

Der virtuelle Computer versucht, von der ersten CD- oder DVD-Festplatte zu starten, die mit einem Startsektor gefunden wurde.

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**IDE-Festplatte** (2)


</dt> <dd>

Der virtuelle Computer versucht, von der ersten Festplatte aus zu starten, die mit einem Startsektor gefunden wurde.

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**PXE-Start** (3)


</dt> <dd>

Der virtuelle Computer versucht, PXE aus dem Netzwerk zu starten.

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**SCSI-Festplatte** (4)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserviert** (5..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**BootSourceOrder**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Reihenfolge der Startquelle für den virtuellen Computer.

**Windows 8.1:** Dieser Wert wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ChassisAssetTag**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Assettag des Gehäuses für den virtuellen Computer.

</dd> <dt>

**ChassisSerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Seriennummer des Gehäuses für den virtuellen Computer.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zur Konfiguration des virtuellen Computers gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Pfad und Dateiname einer Datei, in der Informationen zur Konfiguration des virtuellen Computers gespeichert werden. Dieser Pfad ist relativ zur **ConfigurationDataRoot-Eigenschaft.** Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Bezeichner der Konfiguration des virtuellen Computers. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**ConsoleMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Identifiziert den Konsolenmodus für den virtuellen Computer.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10 und Windows Server 2016 hinzugefügt.

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Standard** (0)


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

**COM1** (1)


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

**COM2** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Creationtime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit, zu der die Einstellungen für den virtuellen Computer erstellt wurden. Wenn dieses Objekt die aktuellen Einstellungen für den virtuellen Computer darstellt, ist dieser Wert der Zeitpunkt, zu dem das System erstellt wurde. Wenn dieses Objekt die Momentaufnahmeeinstellungen für den virtuellen Computer darstellt, ist dieser Wert der Zeitpunkt, zu dem die Momentaufnahme erstellt wurde. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**DebugChannelId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Kanalbezeichner, der zum Debuggen des virtuellen Computers mithilfe des einheitlichen Debuggers verwendet wird.

</dd> <dt>

**DebugPort**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der TCP/IP-Port, der zum Debuggen des virtuellen Computers mit synthetischem Debuggen verwendet wird.

</dd> <dt>

**DebugPortEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der virtuelle Computer synthetisches Debuggen verwendet. Dies kann einer der folgenden Werte sein.

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>**Aus** (0)


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span id="On"></span><span id="on"></span><span id="ON"></span>**Ein** (1)


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)


</dt> <dd>

Automatisch zugewiesen

</dd> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf einen der folgenden Werte festgelegt.



| Wert                                                                                                                  | Bedeutung                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>"Aktive Einstellungen für den virtuellen Computer"</dt> </dl>   | Diese Instanz bezieht sich auf einen virtuellen Computer.<br/> |
| <dl> <dt>"Momentaufnahmeeinstellungen für den virtuellen Computer"</dt> </dl> | Diese Instanz verweist auf eine Momentaufnahme.<br/>        |



 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))geerbt und immer auf den Anzeigenamen für den Computer festgelegt. Dieser Name darf 100 Zeichen nicht überschreiten.

</dd> <dt>

**EnhancedSessionTransportType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt den Transporttyp an, der beim Herstellen einer Verbindung mit einer erweiterten Sitzung verwendet werden soll.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10 Version 1803 hinzugefügt.

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

**VMBus Pipe** (0)


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

**Hyper-V-Socket** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestControlledCacheTypes**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der Gast Cachetypen steuern kann.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**GuestStateDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Dateipfad eines Verzeichnisses, in dem Informationen zum Zustand der Gastruntime gespeichert werden.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

</dd> <dt>

**GuestStateFile**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Dateipfad einer Datei, in der Informationen zum Zustand der Gastruntime gespeichert werden. Ein relativer Pfad wird an den Wert der **GuestStateDataRoot-Eigenschaft** angefügt.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

</dd> <dt>

**HighMmioGapSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Größe von High (über 4 GB) Memory-Mapped E/A-Lücke in MB

> [!Note]  
> Diese Eigenschaft wurde in Windows 10 Version 1703 hinzugefügt.

 

</dd> <dt>

**IncrementalBackupEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der Hyper-V VSS Writer das Erstellen inkrementeller Sicherungen dieses virtuellen Computers unterstützt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.

</dd> <dt>

**IsAutomaticSnapshot**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob es sich um eine Momentaufnahme handelt, die automatisch für den Benutzer erstellt wird.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1709.

 

</dd> <dt>

**IsSaved**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn die Konfiguration einen Verweis auf eine gespeicherte Zustandsdatei enthält. Andernfalls **FALSE.** Dies gibt nicht das Vorhandensein einer solchen Datei an, sondern nur, dass die Konfiguration eine Datei angibt.

</dd> <dt>

**LockOnDisconnect**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Sperren Sie die Konsole, wenn Sie die Verbindung mit vmconnect trennen.

> [!Note]  
> Hinzugefügt in Windows 10 und Windows Server 2016.

 

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Protokollinformationen für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**LowMmioGapSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Konfiguriert die Größe der ersten MMIO-Lücke für einen virtuellen Computer (VM) in Megabyte.

**Windows 8.1:** Dieser Wert wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.

Bereich: 128 3584

</dd> <dt>

**NetworkBootPreferredProtocol**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Bestimmt, ob das bevorzugte Protokoll für den PXE-Start IPv4 oder IPv6 ist.

**Windows 8.1:** Dieser Wert wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (4097)


</dt> <dd></dd> </dl>

</dd> <dt>

**Notizen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vom Benutzer bereitgestellte Hinweise im Zusammenhang mit dem virtuellen Computer. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn diese Instanz kein System basierend auf einer Momentaufnahme eines virtuellen Computers repräsentiert, ist diese Eigenschaft **NULL.** Andernfalls enthält die -Eigenschaft den Objektpfad des **Msvm \_ VirtualSystemSettingData-Objekts,** auf dem diese Instanz basiert. Beim Erstellen einer Momentaufnahmestrukturhierarchie für den virtuellen Computer verweist diese Eigenschaft auf das Objekt, von dem die aktuelle Instanz abgeleitet wird (die aktuelle Instanz ist der untergeordnete Knoten, und das Objekt, auf das in dieser Eigenschaft verwiesen wird, ist der übergeordnete Knoten.)

</dd> <dt>

**ParentPackage**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wenn es sich bei diesem System um einen Container handelt, ist dies der Pfad zu dem Msvm \_ ContainerPackage, auf dem dieses System basiert.

> [!Note]  
> Hinzugefügt in Windows 10; wurde in Windows 10 Version 1703 entfernt.

 

</dd> <dt>

**PauseAfterBootFailure**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob das BIOS nach jedem Starteintragsfehler angehalten wird, der darauf wartet, dass der Benutzer eine Taste drückt. **TRUE,** wenn das BIOS angehalten wird; andernfalls **False.**

**Windows 8.1:** Dieser Wert wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der vollständige Pfad einer Datei, in der wiederherstellungsbezogene Informationen für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**SecureBootEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der sichere Start für den virtuellen Computer (VM) aktiviert ist. **True,** wenn aktiviert; andernfalls **False.**

> [!Note]  
> Der sichere Start kann nur für VMs der Generation 2 aktiviert werden.

 

**Windows 8.1:** Dieser Wert wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.

</dd> <dt>

**SecureBootTemplateId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der global eindeutige Bezeichner der Vorlage von Initialwerten von Variablen im Zusammenhang mit UEFI Secure Boot.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyVirtualSystem-Methode**](https://www.bing.com/search?q=**ModifyVirtualSystem**) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

> [!Note]  
> Hinzugefügt in Windows 10 und Windows Server 2016.

 

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zu den Momentaufnahmen des virtuellen Computers gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zu den informationen zum Angehalten des virtuellen Computers gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Auslagerungsdateien für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**UserSnapshotType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt den benutzerdefinierten Momentaufnahmetyp an.

> [!Note]  
> Hinzugefügt in Windows 10 und Windows Server 2016.

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deaktivieren** (2)


</dt> <dd>

Deaktivieren Sie die Erstellung von Momentaufnahmen.

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)


</dt> <dd>

Daten konsistente Momentaufnahme für die Verwendung in der Produktionsumgebung. Führt eine Momentaufnahme mit anwendungsstatus aus, wenn die Möglichkeit zum Erstellen einer daten konsistenten Momentaufnahme nicht verfügbar ist.

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)


</dt> <dd>

Daten konsistente Momentaufnahme für die Verwendung in der Produktionsumgebung. Erstellt keine Momentaufnahme mit anwendungsstatus, wenn es nicht möglich ist, eine daten konsistente Momentaufnahme zu erstellen.

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)


</dt> <dd>

Momentaufnahme, die Speicher- und Geräteinformationen für Test- und Entwicklungsziele enthält.

</dd> </dl>

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version des virtuellen Computers im Format "major.minor", z.B. "2.0".

</dd> <dt>

**VirtualNumaEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**", "[**Msvm \_ MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")
</dt> </dl>

**True,** wenn virtuelle NUMA-Knoten (Non-Uniform Memory Access) in den virtuellen Computer projiziert werden. **False,** wenn der virtuelle Computer einen einzelnen Knoten hat. True **gibt** an, dass die Anzahl der in den virtuellen Computer projizierten virtuellen NUMA-Knoten anhand der Werte der [**Eigenschaften Msvm \_ ProcessorSettingData.MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) und [**Msvm \_ MemorySettingData.MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) bestimmt wird.

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemSettingData.VirtualSystemIdentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**")
</dt> </dl>

Der Name des [**CIM \_ ComputerSystem-Objekts,**](/windows/desktop/CIMWin32Prov/cim-computersystem) zu dem diese Einstellungsdaten gehören. Diese Eigenschaft ist eine Außerkraftsetzung von [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die gültigen Werte für diese Eigenschaft sind Microsoft:Hyper-V:SubType:1 und Microsoft:Hyper-V:SubType:2. Ein virtueller Computer der Generation 1 ist der Untertyp 1. Ein virtueller Computer der Generation 2 ist der Untertyp 2.

**Windows 8.1:** Dieser Wert wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ des virtuellen Computers an, den die Einstellungsdaten darstellen. Diese Eigenschaft wird von der [**CIM \_ VirtualSystemSettingData-Klasse**](/previous-versions//cc136954(v=vs.85)) geerbt. Dies ist einer der folgenden Werte.



| Wert                                                                                                                                 | Bedeutung                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>"Microsoft:Hyper-V:System:Realized"</dt> </dl>                        | Ein realisierter virtueller Computer.<br/>               |
| <dl> <dt>"Microsoft:Hyper-V:System:Planned"</dt> </dl>                         | Ein geplanter virtueller Computer.<br/>                |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Realized"</dt> </dl>                      | Eine Momentaufnahme eines realisierten virtuellen Computers.<br/> |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Recovery"</dt> </dl>                      | Eine Momentaufnahme eines virtuellen Wiederherstellungscomputers.<br/> |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Planned"</dt> </dl>                       | Eine Momentaufnahme eines geplanten virtuellen Computers.<br/>  |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Missing"</dt> </dl>                       | Eine fehlende Momentaufnahme.<br/>                       |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Replica:Standard"</dt> </dl>              | Eine zeitbasierte Replikationspunktmomentaufnahme.<br/>  |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Replica:ApplicationConsistent"</dt> </dl> | Eine Momentaufnahme des VSS-Replikationspunkts.<br/>         |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Replica:PlannedFailover"</dt> </dl>       | Eine geplante Replikationsmomentaufnahme.<br/>           |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ VirtualSystemSettingData-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[Virtuelle Systemklassen](virtual-system-classes.md)
</dt> </dl>

 

