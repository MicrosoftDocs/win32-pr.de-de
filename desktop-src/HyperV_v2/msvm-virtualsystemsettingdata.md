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
ms.openlocfilehash: 2787abbacfe4220b135544eecd3aeb7e86596c81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958741"
---
# <a name="msvm_virtualsystemsettingdata-class"></a>MSVM \_ virtualsystemsettingdata-Klasse

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

Die **MSVM \_ virtualsystemsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualsystemsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Additionalherstellungsinformationen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Alle zusätzlichen Informationen, die für die Wiederherstellungs Aktion bereitgestellt werden. Die Bedeutung dieser Eigenschaft wird durch die Aktion in **automatikrecoveryaction** definiert. Wenn **automatikrecoveryaction** den Wert 0 ("None") oder 1 ("Restart") hat, ist dieser Wert **null**. Wenn **automatidecoveryaction** den Wert 2 hat ("Momentaufnahme wiederherstellen"), ist dies der Objekt Pfad zu einer Momentaufnahme, die bei einem Fehler des Arbeitsprozesses der virtuellen Maschine angewendet werden soll.

</dd> <dt>

**Allowfullscsicommandset**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** , wenn SCSI-Befehle vom Gast Betriebssystem an Pass-Through-Datenträger übergeben werden. andernfalls **false**. **True** gibt an, dass SCSI-Befehle, die vom Gast Betriebssystem an Pass-Through-Datenträger ausgegeben werden, nicht gefiltert werden. Es wird empfohlen, die SCSI-Filterung für Produktions Bereitstellungen zu aktivieren.

</dd> <dt>

**Allowreducedf | dundancy**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Live Migration eines virtuellen Computers, der mit einem virtuellen Fibre Channel Adapter konfiguriert ist, zu einem Zielcomputer zulässig ist, der möglicherweise über keine oder reduzierten Pfad zum Ziel Fibre Channel Geräten verfügt. Diese Eigenschaft sollte nach einer Live Migration gelöscht werden.



| Wert                                                                            | Bedeutung                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>False</dt> </dl> | Der virtuelle Computer kann nicht auf einen Zielcomputer migriert werden, der möglicherweise keine oder weniger Pfade zum Ziel Fibre Channel Geräten hat.<br/>                                                                                                     |
| <dl> <dt>True</dt> </dl>  | Der virtuelle Computer kann Live zu einem Zielcomputer migriert werden, der möglicherweise keine oder weniger Pfade zum Ziel Fibre Channel Geräten hat. Das Gast Betriebssystem verliert möglicherweise die Konnektivität mit dem Speicher und kann sich auf unvorhersehbare Weise Verhalten.<br/> |



 

</dd> <dt>

**Architektur**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Architektur dieses Systems.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

<dt>

<span id="x64"></span><span id="X64"></span>

**x64** ()


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

**arm64** ()


</dt> <dd></dd> </dl>

</dd> <dt>

**Automaticcriticalerroraction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt die Aktion an, die auf dem virtuellen Computer ausgeführt werden soll, wenn ein kritischer Fehler auftritt, z. b. Speicher Trennung.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Keine** (0)


</dt> <dd>

Für kritische Fehlerbedingungen wird keine spezielle Aktion ausgeführt.

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>Fortsetzung **anhalten (1** )


</dt> <dd>

Bewirkt, dass der virtuelle Computer angehalten und automatisch fortgesetzt wird, wenn der kritische Fehlerzustand behoben ist.

</dd> </dl>

</dd> <dt>

**Automaticcriticalerroraktiontimeout**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**Untertyp**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Intervall")
</dt> </dl>

Gibt die maximale Dauer an, für die die **automaticcriticalerroraction** ausgeführt wird, um den kritischen Fehler zu beheben. Dies gilt nur, wenn der Wert der **automaticcriticalerroraction** -Eigenschaft nicht 0 (None) ist. Nach Ablauf des Timeouts wird der virtuelle Computer ausgeschaltet. Der Wert wird auf die nächste Minute aufgerundet. Der Wert 0 bedeutet, dass der virtuelle Computer sofort ausgeschaltet werden sollte, wenn er auf einen kritischen Fehlerzustand stößt.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**Automatikrecoveryaction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die für den virtuellen Computer auszuführende Aktion, wenn die von der virtuellen Maschine ausgeführte Software ausfällt. Fehler sind in diesem Fall ein Fehler, der von der Host Plattform erkannt werden kann, z. b. eine nicht unter brechbare Bedingung für den Wartezustand. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

Dies kann einer der folgenden Werte sein:



| Wert                                                                               | Bedeutung                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>2</dt> </dl>        | Keine.<br/>               |
| <dl> <dt>3</dt> </dl>        | Neu starten<br/>            |
| <dl> <dt>4</dt> </dl>        | Momentaufnahme wiederherstellen.<br/> |
| <dl> <dt>5.. 32768</dt> </dl> | Reserviert.<br/>           |



 

</dd> <dt>

**Automaticshutdownaction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktion, die beim Herunterfahren des Hosts für die virtuelle Maschine ausgeführt werden soll. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

Dies kann einer der folgenden Werte sein:



| Wert                                                                               | Bedeutung                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <dt>2</dt> </dl>        | Ausschalten.<br/>   |
| <dl> <dt>3</dt> </dl>        | Speichern Sie den Zustand.<br/> |
| <dl> <dt>4</dt> </dl>        | Herunterfahren<br/>   |
| <dl> <dt>5.. 32768</dt> </dl> | Reserviert.<br/>   |



 

</dd> <dt>

**Automaticsnapshotsenabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob für diesen virtuellen Computer automatische Momentaufnahmen aktiviert werden sollen.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**Automaticstartupaction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktion, die für den virtuellen Computer ausgeführt werden soll, wenn der Host gestartet wird. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

Dies kann einer der folgenden Werte sein:



| Wert                                                                               | Bedeutung                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>2</dt> </dl>        | Keine.<br/>                         |
| <dl> <dt>3</dt> </dl>        | Neu starten, wenn zuvor aktiv.<br/> |
| <dl> <dt>4</dt> </dl>        | Immer starten.<br/>                 |
| <dl> <dt>5.. 32768</dt> </dl> | Reserviert.<br/>                     |



 

</dd> <dt>

**Automaticstartupactiondelay**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Verzögerungszeit, bevor der virtuelle Computer automatisch gestartet wird. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Automaticstartupactionsequencenumschlag**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zahl, die die relative Sequenz der Aktivierung virtueller Maschinen angibt, wenn das Host System gestartet wird. Eine niedrigere Zahl deutet auf eine frühere Aktivierung hin. Wenn eine oder mehrere Konfigurationen denselben Wert aufweisen, ist die Sequenz implementierungsabhängig. Der Wert 0 gibt an, dass die Sequenz implementierungsabhängig ist. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Baseboardserialnumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Seriennummer des Basis Boards für die virtuelle Maschine.

</dd> <dt>

**Biosguid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Globally Unique Identifier für das BIOS der virtuellen Maschine.

</dd> <dt>

**Biosnumlock**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** , wenn der NUM-Sperr Schlüssel vom BIOS auf ON festgelegt ist. **False** , wenn der NUM-Sperr Schlüssel vom BIOS auf OFF festgelegt ist.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Seriennummer des BIOS für den virtuellen Computer.

</dd> <dt>

**"Bootorder"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

Die Start Reihenfolge, die innerhalb des BIOS der virtuellen Maschine festgelegt ist. Diese Eigenschaft ist ein Array von Werten, **booterder** \[ 0 \] bis **bootor** \[ 3 ( \] inklusiv), wobei jeder Wert ein Gerät angibt, von dem aus gestartet werden soll. Jeder der vier Werte im Array muss festgelegt werden und darf nicht mit einem anderen Wert im Array identisch sein. Der virtuelle Computer versucht zunächst, über das Gerät zu starten, das durch den ersten Wert im Array angegeben wird. Wenn dieses Gerät keinen Startsektor enthält, versucht die virtuelle Maschine, vom nächsten Gerät zu starten, das von der **bootorder** -Eigenschaft angegeben wird, und so weiter. Wenn kein im **bootor** angegebener Gerät einen Startsektor enthält, kann der virtuelle Computer nicht gestartet werden. Der Standardwert für eine virtuelle Maschine ist \[ 0, 1, 2, 3 \] .

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Diskette** (0)


</dt> <dd>

Der virtuelle Computer wird versuchen, von der Diskette innerhalb des Disketten Laufwerks zu starten.

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)


</dt> <dd>

Der virtuelle Computer versucht, von der ersten CD oder DVD-Festplatte zu starten, die mit einem Startsektor gefunden wurde.

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**IDE-Festplatte** (2)


</dt> <dd>

Der virtuelle Computer versucht, vom ersten Festplattenlaufwerk aus zu starten, das sich in einem Startsektor befand.

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

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserviert** (5.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Bootsourceorder**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Start Quell Reihenfolge für den virtuellen Computer.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Chassisassettag**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Bestands Kennzeichen des Chassis für den virtuellen Computer.

</dd> <dt>

**Chassisserialnumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Seriennummer des Chassis für den virtuellen Computer.

</dd> <dt>

**Configurationdataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zur Konfiguration der virtuellen Maschine gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Pfad und der Dateiname einer Datei, in der Informationen zur Konfiguration der virtuellen Maschine gespeichert werden. Dieser Pfad ist relativ zur **configurationdataroot** -Eigenschaft. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Bezeichner der Konfiguration der virtuellen Maschine. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Consolemode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Identifiziert den Konsolenmodus für die VM.

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

**CreationTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der Einstellungen für die virtuelle Maschine. Wenn dieses-Objekt die aktuellen Einstellungen für die virtuelle Maschine darstellt, ist dieser Wert die Zeit, zu der das System erstellt wurde. Wenn dieses-Objekt die Momentaufnahme Einstellungen für die virtuelle Maschine darstellt, ist dieser Wert die Zeit, zu der die Momentaufnahme erstellt wurde. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**"Debug-channelid"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Kanal Bezeichner, der zum Debuggen des virtuellen Computers mit dem Unified Debugger verwendet wird.

</dd> <dt>

**Debugport**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der TCP/IP-Port, der zum Debuggen des virtuellen Computers verwendet wird.

</dd> <dt>

**"Debug-portenabled"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der virtuelle Computer synthetisches Debuggen verwendet. Dies kann einer der folgenden Werte sein:

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>**Aus** (0)


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span id="On"></span><span id="on"></span><span id="ON"></span>Ein **(1** )


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**Onautoassigned** (2)


</dt> <dd>

Automatisch zugewiesen

</dd> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf einen der folgenden Werte festgelegt.



| Wert                                                                                                                  | Bedeutung                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>"Aktive Einstellungen für den virtuellen Computer"</dt> </dl>   | Diese Instanz verweist auf einen virtuellen Computer.<br/> |
| <dl> <dt>"Momentaufnahme Einstellungen für den virtuellen Computer"</dt> </dl> | Diese Instanz verweist auf eine Momentaufnahme.<br/>        |



 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird immer auf den anzeigen Amen für den Computer festgelegt. Dieser Name darf nicht länger als 100 Zeichen sein.

</dd> <dt>

**Enhancedsessiontransporttype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt den Transporttyp an, der beim Herstellen einer Verbindung mit einer erweiterten Sitzung verwendet wird.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10, Version 1803, hinzugefügt.

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

**VMBus-Pipe** (0)


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

**Hyper-V-Socket** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Guestcontrolledcachetypes**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der Gast Cache Typen steuern kann.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**Gueststatedataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Dateipfad eines Verzeichnisses, in dem Informationen über den Gast Lauf Zeit Zustand gespeichert werden.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**Gueststatefile**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Dateipfad einer Datei, in der Informationen über den Gast Lauf Zeit Zustand gespeichert werden. Ein relativer Pfad wird an den Wert der **gueststatedataroot** -Eigenschaft angefügt.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**Highmmiogapsize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Größe des oberen (über 4 GB) Memory-Mapped e/a-GAP in MB

> [!Note]  
> Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.

 

</dd> <dt>

**Incrementalbackupabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die Hyper-V-VSS Writer die das inkrementelle sichern dieser virtuellen Maschine unterstützt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.

</dd> <dt>

**Isautomaticsnapshot**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob es sich um eine für den Benutzer automatisch erstellte Momentaufnahme handelt.

> [!Note]  
> Hinzugefügt in Windows 10, Version 1709.

 

</dd> <dt>

**IsSaved**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** , wenn die Konfiguration einen Verweis auf eine gespeicherte Zustands Datei enthält. andernfalls **false**. Dies deutet nicht darauf hin, dass eine solche Datei vorhanden ist, sondern nur, dass die Konfiguration eine Datei angibt.

</dd> <dt>

**Lockondisconnect**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Sperren Sie die Konsole, wenn Sie die Verbindung mit VMConnect trennen.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**Logdataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Protokollinformationen für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Lowmmiogapsize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Hiermit wird die Größe der ersten MMIO-Lücke für einen virtuellen Computer (VM) in Megabyte konfiguriert.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

Bereich: 128 3584

</dd> <dt>

**Network bootpreferredprotocol**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Bestimmt, ob das bevorzugte Protokoll für den PXE-Start IPv4 oder IPv6 ist.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (4097)


</dt> <dd></dd> </dl>

</dd> <dt>

**Hinweise**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vom Benutzer bereitgestellte Hinweise zum virtuellen Computer. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn diese Instanz kein System darstellt, das auf einer Momentaufnahme einer virtuellen Maschine basiert, ist diese Eigenschaft **null**. Andernfalls enthält die Eigenschaft den Objekt Pfad des **MSVM \_ virtualsystemsettingdata** -Objekts, auf dem diese Instanz basiert. Beim Erstellen einer Momentaufnahme Struktur Hierarchie für den virtuellen Computer verweist diese Eigenschaft auf das Objekt, von dem die aktuelle Instanz abgeleitet wird (die aktuelle Instanz ist der untergeordnete Knoten, und das Objekt, auf das in dieser Eigenschaft verwiesen wird, ist der übergeordnete Knoten.)

</dd> <dt>

**Paket Paket**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wenn es sich um einen Container handelt, ist dies der Pfad zum MSVM- \_ containerpackage, auf dem dieses System basiert.

> [!Note]  
> In Windows 10 hinzugefügt entfernt in Windows 10, Version 1703.

 

</dd> <dt>

**Pauseafterbootfailure**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob das BIOS nach jedem Fehler beim Start Eintrag angehalten wird, wenn der Benutzer eine Taste drückt. **True** , wenn das BIOS angehalten wird. andernfalls **false**.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

</dd> <dt>

**Wiederherstellbare Datei**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der vollständige Pfad einer Datei, in der Wiederherstellungs bezogene Informationen für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**"Securebootenabled"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der sichere Start für den virtuellen Computer (VM) aktiviert ist. **True** , wenn aktiviert; andernfalls **false**.

> [!Note]  
> Der sichere Start kann nur für VMS der Generation 2 aktiviert werden.

 

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

</dd> <dt>

**Secureboottemplateid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Global eindeutige Bezeichner der Vorlage mit den Anfangs-Werten von UEFI-Variablen für den sicheren Start.

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyvirtualsystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**Snapshotdataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zu den Momentaufnahmen der virtuellen Maschine gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Suspenddataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zu den Informationen zum Aussetzen der virtuellen Maschine gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Austauschen von Daten**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem die Auslagerungs Dateien für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Usersnapshottype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt den Typ der benutzerdefinierten Momentaufnahme an.

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deaktivieren** (2)


</dt> <dd>

Hiermit wird die Erstellung einer Momentaufnahme deaktiviert.

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**Productionfallbacktetest** (3)


</dt> <dd>

Daten konsistente Momentaufnahme für die Verwendung in der Produktionsumgebung. Führt eine Momentaufnahme mit einem Anwendungs Zustand aus, wenn die Möglichkeit zum Erstellen einer Daten konsistenten Momentaufnahme nicht verfügbar ist.

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**Productionnofallback** (4)


</dt> <dd>

Daten konsistente Momentaufnahme für die Verwendung in der Produktionsumgebung. Erstellt keine Momentaufnahme mit dem Anwendungs Zustand, wenn keine Daten konsistente Momentaufnahme erstellt werden kann.

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)


</dt> <dd>

Momentaufnahme, die Arbeitsspeicher-und Geräteinformationen zu Test-und Entwicklungszwecken enthält.

</dd> </dl>

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version des virtuellen Computers im Format "Major. Minor", z. b. "2,0".

</dd> <dt>

**Virtualnumaaktivierte**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ processorsettingdata**](msvm-processorsettingdata.md).**Maxprocessorspernumanode**","[**MSVM \_ memorysettingdata**](msvm-memorysettingdata.md).**Maxmemoryblockspernumanode**")
</dt> </dl>

**True** , wenn virtuelle NUMA-Knoten (Non-Uniform Memory Access, nicht einheitlicher Speicherzugriff) in den virtuellen Computer projiziert werden. **False** , wenn der virtuelle Computer über einen einzelnen Knoten verfügt. **True** gibt an, dass die Anzahl der virtuellen NUMA-Knoten, die in den virtuellen Computer projiziert werden, von den Werten der Eigenschaften [**MSVM \_ processorsettingdata. maxprocessorspernumanode**](msvm-processorsettingdata.md) und [**MSVM \_ memorysettingdata. maxmemoryblockspernumanode**](msvm-memorysettingdata.md) bestimmt wird.

</dd> <dt>

**Virtualsystemidentifier**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ virtualsystemsettingdata. virtualsystedentifier"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Computersystem**](cim-computersystem.md).**Name**")
</dt> </dl>

Der Name des [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Objekts, zu dem diese Einstellungsdaten gehören. Diese Eigenschaft ist eine außer Kraft Setzung von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gültige Werte für diese Eigenschaft sind Microsoft: Hyper-v: SubType: 1 und Microsoft: Hyper-v: SubType: 2. Eine VM der Generation 1 ist Untertyp 1. Eine VM der Generation 2 ist der Untertyp 2.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft: Hyper-v: Untertyp: 1** ("Microsoft: Hyper-v: SubType: 1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft: Hyper-v: SubType: 2** ("Microsoft: Hyper-v: SubType: 2")


</dt> <dd></dd> </dl>

</dd> <dt>

**Virtualsystemtype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ der virtuellen Maschine an, die die Einstellungsdaten darstellen. Diese Eigenschaft wird von der [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Klasse geerbt. Dabei handelt es sich um einen der folgenden Werte.



| Wert                                                                                                                                 | Bedeutung                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>"Microsoft: Hyper-V: System: realisiert"</dt> </dl>                        | Ein realisierter virtueller Computer.<br/>               |
| <dl> <dt>"Microsoft: Hyper-V: System: geplant"</dt> </dl>                         | Eine geplante virtuelle Maschine.<br/>                |
| <dl> <dt>"Microsoft: Hyper-V: Snapshot: realisiert"</dt> </dl>                      | Eine Momentaufnahme eines erkannten virtuellen Computers.<br/> |
| <dl> <dt>"Microsoft: Hyper-V: Snapshot: Recovery"</dt> </dl>                      | Eine Momentaufnahme eines virtuellen Wiederherstellungs Computers.<br/> |
| <dl> <dt>"Microsoft: Hyper-V: Snapshot: geplant"</dt> </dl>                       | Eine Momentaufnahme eines geplanten virtuellen Computers.<br/>  |
| <dl> <dt>"Microsoft: Hyper-V: Snapshot: Missing"</dt> </dl>                       | Eine fehlende Momentaufnahme.<br/>                       |
| <dl> <dt>"Microsoft: Hyper-V: Snapshot: Replica: Standard"</dt> </dl>              | Eine zeitbasierte Replikations Punkt Momentaufnahme.<br/>  |
| <dl> <dt>"Microsoft: Hyper-V: Snapshot: Replica: applicationkonsistentes"</dt> </dl> | Eine VSS-Replikations Punkt Momentaufnahme.<br/>         |
| <dl> <dt>"Microsoft: Hyper-V: Snapshot: Replica: plannedfailover"</dt> </dl>       | Eine geplante Replikations Momentaufnahme.<br/>           |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ virtualsystemsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[Klassen des virtuellen Systems](virtual-system-classes.md)
</dt> </dl>

 

