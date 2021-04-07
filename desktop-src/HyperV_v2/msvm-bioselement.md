---
description: Stellt die Software auf niedriger Ebene dar, die in den RAM geladen wird, um das System zu konfigurieren und zu starten.
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Msvm_BIOSElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8d36ea50791bf6f1413815583fe1168f564d50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863115"
---
# <a name="msvm_bioselement-class"></a>MSVM- \_ bioselements-Klasse

Stellt die Software auf niedriger Ebene dar, die in den RAM geladen wird, um das System zu konfigurieren und zu starten. Das BIOS ist kein logisches Gerät, daher sollte das virtuelle BIOS nicht als Gerät eines virtuellen Computers betrachtet werden. Da es sich nicht um ein Gerät handelt, verfügt es nicht über einen entsprechenden Ressourcenpool. Das BIOS-Objekt wird der virtuellen Maschine über die [**MSVM- \_ Systembios**](msvm-systembios.md) -Zuordnung zugeordnet.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ bioselements** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ bioselements** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Baseboardserialnumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Seriennummer für das Basisboard auf dem virtuellen Computer.

</dd> <dt>

**Biosguid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Bezeichner für das BIOS.

</dd> <dt>

**Biosnumlock**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte Status der NUM-Sperre im BIOS.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Seriennummer für das BIOS.

</dd> <dt>

**"Bootorder"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

Die Reihenfolge, in der Geräte beim Start nach einem Startsektor durchsucht werden.

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (64)
</dt> </dl>

Der interne Bezeichner für diese Kompilierung des Software Elements. Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf 14 festgelegt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (64)
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Chassisassettag**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird automatisch durch das BIOS aufgefüllt, wenn der virtuelle Computer erstellt wird.

</dd> <dt>

**Chassisserialnumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird automatisch durch das BIOS aufgefüllt, wenn der virtuelle Computer erstellt wird.

</dd> <dt>

**Codesatz**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (64)
</dt> </dl>

Der vom Softwareelement verwendete Codesatz. Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Communicationstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuell für das BIOS ausgewählte Sprache. Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf "en \| US \| ISO8859-1" festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das Element. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktuellen Zustand des Elements an. Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.

Wenn ein kritischer Fehler auftritt, finden Sie im Ereignisprotokoll weitere Informationen. Die **enabledstate** -Eigenschaft kann auch weitere Informationen enthalten. Wenn z. b. der Speicherplatz kritisch ist, ist **healthstate** auf 25 festgelegt, der virtuelle Computer wird angehalten, und **enabledstate** wird auf 32768 (angehalten) festgelegt.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.



| Wert                                                                                                                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>5</dt> </dl>                                                                               | Der virtuelle Computer ist voll funktionsfähig und wird in normalen Betriebsparametern und ohne Fehler ausgeführt.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Hauptfehler**</dt> <dt>20</dt> </dl>             | Der virtuelle Computer hat einen schwerwiegenden Fehler verursacht. Dieser Wert wird verwendet, wenn auf einem oder mehreren Datenträgern, die die virtuellen Festplatten des virtuellen Computers enthalten, wenig Speicherplatz auf dem Datenträger und die virtuelle Maschine angehalten wurde.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Kritischer Fehler**</dt> <dt>25</dt> </dl> | Das Element ist nicht funktionsfähig, und die Wiederherstellung ist möglicherweise nicht möglich. Dies kann darauf hinweisen, dass der Arbeitsprozess für den virtuellen Computer (Vmwp.exe) nicht auf Steuerungs-oder Informationsanforderungen antwortet oder dass auf einem oder mehreren Datenträgern, die die virtuellen Festplatten für die virtuelle Maschine enthalten, wenig Speicherplatz zur Neige ist.<br/> |



 

</dd> <dt>

**Identificationcode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (64)
</dt> </dl>

Der Bezeichner des Herstellers für dieses Softwareelement. Häufig handelt es sich hierbei um eine Stock Keeping Unit (SKU) oder eine Teilenummer. Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird automatisch durch das BIOS aufgefüllt, wenn der virtuelle Computer erstellt wird. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Languageedition**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (32)
</dt> </dl>

Die Language Edition dieses Software Elements. Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**ListOf-Sprachen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste installier barer Sprachen für das BIOS. Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf "en \| US \| ISO8859-1" festgelegt.

</dd> <dt>

**Loadedendingaddress**
</dt> <dd> <dl> <dt>

Datentyp: **unit64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Endadresse des Speichers, der von diesem BIOS belegt wird. Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf 0xFFFFF festgelegt.

</dd> <dt>

**Loadedstartingaddress**
</dt> <dd> <dl> <dt>

Datentyp: **unit64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Startadresse des Speichers, der von diesem BIOS belegt wird. Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf 0xe0000 festgelegt.

</dd> <dt>

**Loadutilityinformation**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die das zum Aktualisieren des BIOS-Elements erforderliche BIOS-Flash-/Auslastungs-Hilfsprogramm beschreibt. Die Version und andere Informationen können in dieser Eigenschaft angegeben werden. Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (256)
</dt> </dl>

Der Hersteller dieses BIOS. Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf "Microsoft Corporation" festgelegt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (1024)
</dt> </dl>

Der Name, der zum Identifizieren dieses Software Elements verwendet wird. Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden. Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf "BIOS" festgelegt.

</dd> <dt>

**Operatingstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das die aktuellen Status des-Objekts enthält. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt. Der Wert bei Index NULL (0) ist einer der folgenden Werte.



| Wert                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>2</dt> </dl>                                                                                      | Der virtuelle Computer ist funktionsfähig und funktioniert ordnungsgemäß.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt></dt> Heruntergestuft <dt>3</dt> </dl>                                         | Der virtuelle Computer ist nur teilweise funktionsfähig. Dies gibt an, dass auf den Speicher, der die Konfiguration enthält, nicht zugegriffen werden kann. Ein virtueller Computer in diesem Zustand kann nur ausgeschaltet oder gelöscht werden. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Vorhersagefehler**</dt> <dt>5</dt> </dl> | Der virtuelle Computer ist funktionsfähig, kann aber in Zukunft fehlschlagen. Dies deutet darauf hin, dass der Speicherplatz im Speicher, der die virtuelle Festplatte des virtuellen Computers enthält, nicht mehr verfügbar ist. Der virtuelle Computer wird angehalten, wenn kein Speicherplatz mehr verfügbar ist.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt></dt> <dt>10</dt> beendet </dl>                                            | Dieser Wert wird nicht unterstützt. Wenn der virtuelle Computer beendet wird, hat die **enabledstate** -Eigenschaft den Wert 3 (deaktiviert).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**In Dienst**</dt> <dt>11</dt> </dl>                                | Die virtuelle Maschine verarbeitet eine Anforderung.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**Ruhender**</dt> <dt>15</dt> </dl>                                            | Dieser Wert wird nicht unterstützt. Wenn die virtuelle Maschine angehalten oder angehalten wird, hat die **enabledstate** -Eigenschaft den Wert 32769 (angehalten) oder 32768 (angehalten).<br/>                                                                                    |



 

Der Wert bei Index eins (1) ist optional und enthält sekundäre Statusinformationen. Ein Client sollte den primären Status von Index 0 (null) verwenden, um zu bestimmen, ob eine neue Anforderung an den virtuellen Computer ausgegeben werden kann. Wenn **OperationalStatus** \[ 0 \] den Wert 2 (OK) hat, kann der von **OperationalStatus** 1 festgestellte Vorgang \[ \] unterbrochen werden.

Der Wert für **OperationalStatus** \[ 1 \] ist einer der folgenden Werte.



| Wert                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Erstellen der Momentaufnahme**</dt> <dt>32768</dt> </dl>                                 | Für den virtuellen Computer wird gerade eine Momentaufnahme erstellt.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Anwenden der Momentaufnahme**</dt> <dt>32769</dt> </dl>                                 | Eine Momentaufnahme wird gerade auf den virtuellen Computer angewendet.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Momentaufnahme**</dt> <dt>32770</dt> wird gelöscht </dl>                                 | Eine Momentaufnahme wird gerade vom virtuellen Computer gelöscht.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**Warten auf Start**</dt> <dt>32771</dt> </dl>                                     | Der virtuelle Computer wird gestartet, nachdem die automatische Startverzögerung abgelaufen ist.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt></dt> Zusammenführen von Datenträgern <dt>32772</dt> </dl>                                                 | Virtuelle Festplatten aus zuvor gelöschten Momentaufnahmen werden zusammengeführt.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Virtueller Computer wird exportiert**</dt> <dt>32773</dt> </dl> | Der virtuelle Computer wird exportiert.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Virtuelle Maschine**</dt> <dt>32774</dt> wird migriert. </dl> | Der virtuelle Computer wird Live von einem physischen Computer zu einem anderen migriert.<br/>  |



 

</dd> <dt>

**OtherTargetOS**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (64)
</dt> </dl>

Der Hersteller und das Betriebssystem für ein Softwareelement, wenn die **TargetOperatingSystem** -Eigenschaft den Wert 1 (Sonstiges) aufweist, was erfordert, dass die **OtherTargetOS** -Eigenschaft einen nicht-**null** -Wert aufweist. Für alle anderen Werte von **TargetOperatingSystem** muss die **OtherTargetOS** -Eigenschaft **null** sein. Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Primarybios**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass dies das primäre BIOS des Computer Systems ist. Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf **true** festgelegt.

</dd> <dt>

**Primarystatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt Statusinformationen auf hoher Ebene bereit. Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Registryuris**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichen folgen, das den Veröffentlichungs Speicherort der BIOS-Attribut Registrierung oder Registrierungen darstellt, denen die Implementierung entspricht. Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt.

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum, an dem das BIOS freigegeben wurde. Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (64)
</dt> </dl>

Die zugewiesene Seriennummer des BIOS. Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt.

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (256)
</dt> </dl>

Ein Bezeichner für das Softwareelement. Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf "Microsoft:*GUID* \\ *gerätespezifische Daten*" festgelegt.

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Status des Lebenszyklus eines Software Elements. Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf 2 (ausführbare Datei) festgelegt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.

</dd> <dt>

**Status Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **arrayType** ("indiziert")
</dt> </dl>

Ein Array, das Zeichen folgen enthält, die die entsprechenden **OperationalStatus** -Array Werte beschreiben. Wenn z. b. 11 (in Service) der Wert ist, der **OperationalStatus** \[ 0 zugewiesen ist \] , enthält **Statusbeschreibungen** \[ 0 \] möglicherweise eine Erläuterung, warum der virtuelle Computer eine Anforderung verarbeitet. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Betriebssystemumgebung des-Elements. Diese Eigenschaft wird von [**CIM \_ Softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und ist immer auf 0 (unbekannt) festgelegt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (64)
</dt> </dl>

Die BIOS-Version. Diese Eigenschaft wird von [**CIM \_ bioselements**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und ist immer auf "8.02.00" festgelegt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM-Klasse " \_ bioselements** " kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM- \_ bioselare**](cim-bioselement.md)
</dt> <dt>

[BIOS-Klassen](bios-classes.md)
</dt> <dt>

[**CIM- \_ bioselare**](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 

