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
ms.openlocfilehash: 8433c8fda6d438e4f77fb763be42467aab05ab976927f018e895a30d5f9c6226
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149300"
---
# <a name="msvm_bioselement-class"></a>Msvm \_ BIOSElement-Klasse

Stellt die Software auf niedriger Ebene dar, die in den RAM geladen wird, um das System zu konfigurieren und zu starten. Das BIOS ist kein logisches Gerät, daher sollte das virtuelle BIOS nicht als virtuelles Computergerät bezeichnet werden. Da es sich nicht um ein Gerät handelt, verfügt es nicht über einen entsprechenden Ressourcenpool. Das BIOS-Objekt wird dem virtuellen Computer über die [**\_ Msvm-SystemBIOS-Zuordnung**](msvm-systembios.md) zugeordnet.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **Msvm \_ BIOSElement-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ BIOSElement-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BaseBoardSerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Seriennummer für das Basisboard auf dem virtuellen Computer.

</dd> <dt>

**BIOSGUID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Bezeichner für das BIOS.

</dd> <dt>

**BIOSNumLock**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte Zustand der Num-Sperre im BIOS.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Seriennummer für das BIOS.

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indiziert"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

Die Reihenfolge, in der Geräte beim Start nach einem Startsektor durchsucht werden.

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (64)
</dt> </dl>

Der interne Bezeichner für diese Kompilierung des Softwareelements. Diese Eigenschaft wird von [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und immer auf 14 festgelegt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (64)
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ChassisAssetTag**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird automatisch vom BIOS aufgefüllt, wenn der virtuelle Computer erstellt wird.

</dd> <dt>

**ChassisSerialNumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird automatisch vom BIOS aufgefüllt, wenn der virtuelle Computer erstellt wird.

</dd> <dt>

**CodeSet**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (64)
</dt> </dl>

Der vom Softwareelement verwendete Codesatz. Diese Eigenschaft wird von [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die derzeit ausgewählte Sprache für das BIOS. Diese Eigenschaft wird von [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und immer auf "en \| US \| iso8859-1" festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ergänzt die **PrimaryStatus-Eigenschaft** durch zusätzliche Statusdetails. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Element. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die aktuelle Integrität des Elements an. Dieses Attribut drückt die Integrität dieses Elements aus, jedoch nicht notwendigerweise die Integrität seiner Unterkomponenten.

Wenn ein kritischer Fehler auftritt, überprüfen Sie das Ereignisprotokoll auf Details. Die **EnabledState-Eigenschaft** kann auch weitere Informationen enthalten. Wenn der Speicherplatz auf dem Datenträger beispielsweise sehr gering ist, **healthState** auf 25 festgelegt ist, der virtuelle Computer angehalten wird und **EnabledState** auf 32768 (Angehalten) festgelegt ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.



| Wert                                                                                                                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>5</dt> </dl>                                                                               | Der virtuelle Computer ist voll funktionsfähig und funktioniert innerhalb normaler Betriebsparameter und ohne Fehler.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Hauptfehler**</dt> <dt>20</dt> </dl>             | Auf dem virtuellen Computer ist ein schwerwiegender Fehler aufgetreten. Dieser Wert wird verwendet, wenn mindestens ein Datenträger, der die VHDs des virtuellen Computers enthält, wenig Speicherplatz auf dem Datenträger hat und der virtuelle Computer angehalten wurde.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Kritischer Fehler**</dt> <dt>25</dt> </dl> | Das Element ist nicht funktional, und die Wiederherstellung ist möglicherweise nicht möglich. Dies kann darauf hinweisen, dass der Arbeitsprozess für den virtuellen Computer (Vmwp.exe) nicht auf Steuerungs- oder Informationsanforderungen reagiert oder dass mindestens ein Datenträger, der die VHDs für den virtuellen Computer enthält, nicht über wenig Speicherplatz verfügt.<br/> |



 

</dd> <dt>

**IdentificationCode**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (64)
</dt> </dl>

Der Bezeichner des Herstellers für dieses Softwareelement. Häufig handelt es sich dabei um eine Lagerhaltungseinheit (Stock Keeping Unit, SKU) oder eine Teilenummer. Diese Eigenschaft wird von [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wird automatisch vom BIOS aufgefüllt, wenn der virtuelle Computer erstellt wird. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**LanguageEdition**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (32)
</dt> </dl>

Die Sprachversion dieses Softwareelements. Diese Eigenschaft wird von [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste der installierbaren Sprachen für das BIOS. DIESE Eigenschaft wird von [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und immer auf "en \| US \| iso8859-1" festgelegt.

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **unit64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Endadresse des Arbeitsspeichers, der von diesem BIOS belegt wird. Diese Eigenschaft wird von [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und immer auf 0xFFFFF festgelegt.

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **unit64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Startadresse des Arbeitsspeichers, der von diesem BIOS belegt wird. Diese Eigenschaft wird von [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und immer auf 0xE0000 festgelegt.

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die das BIOS-Flash-/Ladehilfsprogramm beschreibt, das zum Aktualisieren des BIOS-Elements erforderlich ist. Version und andere Informationen können in dieser Eigenschaft angegeben werden. Diese Eigenschaft wird von [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (256)
</dt> </dl>

Der Hersteller dieses BIOS. Diese Eigenschaft wird von [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und immer auf "Microsoft Corporation" festgelegt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (1024)
</dt> </dl>

Der Name, der zum Identifizieren dieses Softwareelements verwendet wird. Bei Einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden. Diese Eigenschaft wird von [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und immer auf "BIOS" festgelegt.

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt aktuelle Statusinformationen für die Betriebsbedingung des Elements bereit und kann zum Bereitstellen weiterer Details in Bezug auf den Wert der **EnabledState-Eigenschaft** verwendet werden. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das die aktuellen Status des -Objekts enthält. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt. Der Wert bei Index null (0) ist einer der folgenden Werte.



| Wert                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>2</dt> </dl>                                                                                      | Der virtuelle Computer ist funktionsfähig und funktioniert normal.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Heruntergestuft**</dt> <dt>3</dt> </dl>                                         | Der virtuelle Computer ist nur teilweise funktionsfähig. Dies gibt an, dass auf den Speicher, der die Konfiguration enthält, nicht zugegriffen werden kann. Ein virtueller Computer in diesem Zustand kann nur deaktiviert oder gelöscht werden. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Vorhersagefehler**</dt> <dt>5</dt> </dl> | Der virtuelle Computer ist funktionsfähig, kann aber in Zukunft fehlschlagen. Dies gibt an, dass für den Speicher, der die virtuelle Festplatte des virtuellen Computers enthält, wenig freier Speicherplatz verfügbar ist. Der virtuelle Computer wird angehalten, wenn nicht mehr Speicherplatz verfügbar gemacht wird.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt>**Beendet**</dt> <dt>10</dt> </dl>                                            | Dieser Wert wird nicht unterstützt. Wenn der virtuelle Computer beendet wird, hat die **EnabledState-Eigenschaft** den Wert 3 (Deaktiviert).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**In Dienst**</dt> <dt>11</dt> </dl>                                | Der virtuelle Computer verarbeitet eine Anforderung.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**Ruhende**</dt> <dt>15</dt> </dl>                                            | Dieser Wert wird nicht unterstützt. Wenn der virtuelle Computer angehalten oder angehalten wird, hat die **EnabledState-Eigenschaft** den Wert 32769 (Angehalten) oder 32768 (Angehalten).<br/>                                                                                    |



 

Der Wert am Index 1 ist optional und enthält sekundäre Statusinformationen. Ein Client sollte den primären Status von Index null (0) verwenden, um zu bestimmen, ob eine neue Anforderung an den virtuellen Computer ausgegeben werden kann. Wenn **OperationalStatus** \[ 0 \] 2 (OK) ist, kann der durch **OperationalStatus** 1 angegebene Vorgang unterbrochen \[ \] werden.

Der Wert bei **OperationalStatus** \[ 1 \] ist einer der folgenden Werte.



| Wert                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Erstellen der Momentaufnahme**</dt> <dt>32768</dt> </dl>                                 | Eine Momentaufnahme wird gerade für den virtuellen Computer erstellt.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Anwenden der Momentaufnahme**</dt> <dt>32769</dt> </dl>                                 | Eine Momentaufnahme wird gerade auf den virtuellen Computer angewendet.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Löschen der Momentaufnahme**</dt> <dt>32770</dt> </dl>                                 | Eine Momentaufnahme wird gerade vom virtuellen Computer gelöscht.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**Warten auf Start**</dt> <dt>32771</dt> </dl>                                     | Der virtuelle Computer wird gestartet, nachdem die automatische Startverzögerung verstrichen ist.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Zusammenführen von Datenträgern**</dt> <dt>32772</dt> </dl>                                                 | Virtuelle Festplatten aus zuvor gelöschten Momentaufnahmen werden zusammengeführt.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Exportieren eines virtuellen Computers**</dt> <dt>32773</dt> </dl> | Der virtuelle Computer wird exportiert.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Migrieren eines virtuellen Computers**</dt> <dt>32774</dt> </dl> | Der virtuelle Computer wird live von einem physischen Computer zu einem anderen migriert.<br/>  |



 

</dd> <dt>

**OtherTargetOS**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (64)
</dt> </dl>

Der Hersteller und das Betriebssystem für ein Softwareelement, wenn die **TargetOperatingSystem-Eigenschaft** den Wert 1 (Other) hat, was erfordert, dass die **OtherTargetOS-Eigenschaft** über einen Wert ungleich **NULL** verfügt. Für alle anderen Werte von **TargetOperatingSystem** muss die **OtherTargetOS-Eigenschaft** **NULL** sein. Diese Eigenschaft wird von [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass dies das primäre BIOS des Computersystems ist. Diese Eigenschaft wird von [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und immer auf **True** festgelegt.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt statusinformationen auf hoher Ebene bereit. Diese Eigenschaft sollte in Verbindung mit der **DetailedStatus-Eigenschaft** verwendet werden, um detaillierte und detaillierte Integritätsstatusinformationen für das Element und seine Unterkomponenten bereitzustellen. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichenfolgen, das den Veröffentlichungsspeicherort der BIOS-Attributregistrierung oder der Registrierungen darstellt, denen die Implementierung entspricht. Diese Eigenschaft wird von [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt.

</dd> <dt>

**Released**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum, an dem das BIOS veröffentlicht wurde. Diese Eigenschaft wird von [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt.

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (64)
</dt> </dl>

Die zugewiesene Seriennummer des BIOS. Diese Eigenschaft wird von [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt.

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (256)
</dt> </dl>

Ein Bezeichner für das Softwareelement. Diese Eigenschaft wird von [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und immer auf "Microsoft:*GUID-gerätespezifische* \\ *Daten"* festgelegt.

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zustand des Lebenszyklus eines Softwareelements. Diese Eigenschaft wird von [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und immer auf 2 (Ausführbare Datei) festgelegt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **ArrayType** ("Indexed")
</dt> </dl>

Ein Array, das Zeichenfolgen enthält, die die entsprechenden **OperationalStatus-Arraywerte** beschreiben. Wenn beispielsweise 11 (In Service) der Wert ist, der **OperationalStatus** 0 zugewiesen \[ \] ist, enthält **StatusDescriptions** \[ 0 \] möglicherweise eine Erklärung dazu, warum der virtuelle Computer eine Anforderung verarbeitet. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Betriebssystemumgebung des Elements. Diese Eigenschaft wird von [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)geerbt und immer auf 0 (Unbekannt) festgelegt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (64)
</dt> </dl>

Die Version des BIOS. Diese Eigenschaft wird von [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)geerbt und immer auf "8.02.00" festgelegt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ BIOSElement-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ BIOSElement**](cim-bioselement.md)
</dt> <dt>

[BIOS-Klassen](bios-classes.md)
</dt> <dt>

[**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 

