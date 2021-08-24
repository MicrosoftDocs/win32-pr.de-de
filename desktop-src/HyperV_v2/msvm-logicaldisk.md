---
description: Stellt Speicherlaufwerkmedien dar und wird zum Auffüllen der Speicherlaufwerke verwendet.
ms.assetid: 06955C09-CA56-4B4C-997B-9B65AF125375
title: Msvm_LogicalDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalDisk
- Msvm_LogicalDisk.SetPowerState
- Msvm_LogicalDisk.EnableDevice
- Msvm_LogicalDisk.OnlineDevice
- Msvm_LogicalDisk.QuiesceDevice
- Msvm_LogicalDisk.SaveProperties
- Msvm_LogicalDisk.RestoreProperties
- Msvm_LogicalDisk.InstanceID
- Msvm_LogicalDisk.Caption
- Msvm_LogicalDisk.Description
- Msvm_LogicalDisk.ElementName
- Msvm_LogicalDisk.InstallDate
- Msvm_LogicalDisk.Name
- Msvm_LogicalDisk.OperationalStatus
- Msvm_LogicalDisk.StatusDescriptions
- Msvm_LogicalDisk.Status
- Msvm_LogicalDisk.HealthState
- Msvm_LogicalDisk.CommunicationStatus
- Msvm_LogicalDisk.DetailedStatus
- Msvm_LogicalDisk.OperatingStatus
- Msvm_LogicalDisk.PrimaryStatus
- Msvm_LogicalDisk.EnabledState
- Msvm_LogicalDisk.OtherEnabledState
- Msvm_LogicalDisk.RequestedState
- Msvm_LogicalDisk.EnabledDefault
- Msvm_LogicalDisk.TimeOfLastStateChange
- Msvm_LogicalDisk.AvailableRequestedStates
- Msvm_LogicalDisk.TransitioningToState
- Msvm_LogicalDisk.SystemCreationClassName
- Msvm_LogicalDisk.SystemName
- Msvm_LogicalDisk.CreationClassName
- Msvm_LogicalDisk.DeviceID
- Msvm_LogicalDisk.PowerManagementSupported
- Msvm_LogicalDisk.PowerManagementCapabilities
- Msvm_LogicalDisk.Availability
- Msvm_LogicalDisk.StatusInfo
- Msvm_LogicalDisk.LastErrorCode
- Msvm_LogicalDisk.ErrorDescription
- Msvm_LogicalDisk.ErrorCleared
- Msvm_LogicalDisk.OtherIdentifyingInfo
- Msvm_LogicalDisk.PowerOnHours
- Msvm_LogicalDisk.TotalPowerOnHours
- Msvm_LogicalDisk.IdentifyingDescriptions
- Msvm_LogicalDisk.AdditionalAvailability
- Msvm_LogicalDisk.MaxQuiesceTime
- Msvm_LogicalDisk.DataOrganization
- Msvm_LogicalDisk.Purpose
- Msvm_LogicalDisk.Access
- Msvm_LogicalDisk.ErrorMethodology
- Msvm_LogicalDisk.BlockSize
- Msvm_LogicalDisk.NumberOfBlocks
- Msvm_LogicalDisk.ConsumableBlocks
- Msvm_LogicalDisk.IsBasedOnUnderlyingRedundancy
- Msvm_LogicalDisk.SequentialAccess
- Msvm_LogicalDisk.ExtentStatus
- Msvm_LogicalDisk.NoSinglePointOfFailure
- Msvm_LogicalDisk.DataRedundancy
- Msvm_LogicalDisk.PackageRedundancy
- Msvm_LogicalDisk.DeltaReservation
- Msvm_LogicalDisk.Primordial
- Msvm_LogicalDisk.NameFormat
- Msvm_LogicalDisk.NameNamespace
- Msvm_LogicalDisk.OtherNameNamespace
- Msvm_LogicalDisk.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a8bcc9121a6c1f11b57cad8df096713a29edf7a58551de76b6f1cfa2d1f20ab2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521740"
---
# <a name="msvm_logicaldisk-class"></a>Msvm \_ LogicalDisk-Klasse

Stellt Speicherlaufwerkmedien dar und wird zum Auffüllen der Speicherlaufwerke verwendet. Zu den unterstützten Medientypen gehören virtuelle Festplattendateien, virtuelle Diskettendateien, ISO-Dateien und physische Gerätemedien.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalDisk : CIM_LogicalDisk
{
  string   InstanceID;
  string   Caption;
  uint64   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_LogicalDisk";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint16   DataOrganization = 2;
  string   Purpose;
  uint16   Access;
  string   ErrorMethodology;
  uint64   BlockSize = 512;
  uint64   NumberOfBlocks = 266338304;
  uint64   ConsumableBlocks = 0;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = { 2 };
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 0;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial = False;
  uint16   NameFormat = 12;
  uint16   NameNamespace = 8;
  string   OtherNameNamespace;
  string   OtherNameFormat;
};
```

## <a name="members"></a>Member

Die **Msvm \_ LogicalDisk-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Msvm \_ LogicalDisk-Klasse** verfügt über diese Methoden.



| Methode                                                            | Beschreibung                              |
|:------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                  | Diese Methode wird nicht unterstützt.<br/> |
| **OnlineGeräte**                                                  | Diese Methode wird nicht unterstützt.<br/> |
| **QuiesceDevice**                                                 | Diese Methode wird nicht unterstützt.<br/> |
| [**RequestStateChange**](msvm-logicaldisk-requeststatechange.md) | Fordert eine Zustandsänderung an.<br/>      |
| [**Zurücksetzen**](msvm-logicaldisk-reset.md)                           | Setzt den Dienst zurück.<br/>           |
| **RestoreProperties**                                             | Diese Methode wird nicht unterstützt.<br/> |
| **SaveProperties**                                                | Diese Methode wird nicht unterstützt.<br/> |
| **SetPowerState**                                                 | Diese Methode wird nicht unterstützt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ LogicalDisk-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**zugreifen**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Medium lesbar, beschreibbar oder beides ist. Diese Eigenschaft wird von [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.



| Wert                                                                        | Bedeutung                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unbekannt<br/>     |
| <dl> <dt>1</dt> </dl> | Lesbar.<br/>   |
| <dl> <dt>2</dt> </dl> | Beschreibbare.<br/>  |
| <dl> <dt>3</dt> </dl> | Lese-/Schreibzugriff.<br/> |
| <dl> <dt>4</dt> </dl> | Einmal schreiben.<br/> |



 

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Alle zusätzlichen Verfügbarkeiten und Status des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.



| Wert                                                                            | Bedeutung                    |
|----------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>{ 6 }</dt> </dl> | Nicht zutreffend<br/> |



 

</dd> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die primäre Verfügbarkeit und der Status des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.



| Wert                                                                        | Bedeutung                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>6</dt> </dl> | Nicht zutreffend<br/> |



 

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Werte für den *RequestedState-Parameter* der [**RequestStateChange-Methode**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) an, die zum Initiieren einer Zustandsänderung verwendet wird. Die aufgelisteten Werte sind eine Teilmenge der Werte, die in der **RequestedStatesSupported-Eigenschaft** der zugeordneten Instanz von **CIM \_ EnabledLogicalElementCapabilities** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ EnabledLogicalElement-Objekts**](/previous-versions//cc136818(v=vs.85)) sind. Diese Eigenschaft kann ungleich **NULL** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann. Diese Eigenschaft ist **NULL,** wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.

Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**Blöcke**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Größe der Blöcke, die den Speicherblock bilden, in Bytes. Wenn die Blockgröße variabel ist, sollte die maximale Blockgröße in Bytes angegeben werden. Wenn die Blockgröße unbekannt ist oder ein Blockkonzept ungültig ist (z. B. für Aggregatblöcke, Arbeitsspeicher oder logische Datenträger), enthält dies 1. Diese Eigenschaft wird von [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

"ISO-Datenträgerimage"

"Festplattenimage"

"Diskettenimage"

"CD/DVD-Datenträger"

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**ConsumableBlocks**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von Blöcken der Größe **BlockSize,** die bei der Überlagerung von Speicherblöcken mithilfe der [**Msvm \_ BasedOn-Zuordnung zur Nutzung verfügbar**](msvm-basedon.md) sind. Diese Eigenschaft wird von [**CIM \_ StorageExtent geerbt.**](/windows/desktop/CIMWin32Prov/cim-storageextent)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

</dd> <dt>

**DataOrganization**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der verwendeten Datenorganisation. Diese Eigenschaft wird von [**CIM \_ StorageExtent geerbt.**](/windows/desktop/CIMWin32Prov/cim-storageextent)



| Wert                                                                        | Bedeutung                 |
|------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>2</dt> </dl> | Block behoben.<br/> |



 

</dd> <dt>

**DataRedundancy**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der vollständigen Kopien der derzeit verwalteten Daten. Diese Eigenschaft wird von [**CIM \_ StorageExtent geerbt.**](/windows/desktop/CIMWin32Prov/cim-storageextent)

</dd> <dt>

**DeltaReservation**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Prozentsatz, der den Speicherplatz angibt, der in einem Replikat für das Zwischenspeichern von Änderungen reserviert werden soll. Diese Eigenschaft wird von [**CIM \_ StorageExtent geerbt.**](/windows/desktop/CIMWin32Prov/cim-storageextent)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ergänzt die **PrimaryStatus-Eigenschaft** durch zusätzliche Statusdetails. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)und auf "Microsoft:*GUID* \\ *device-specific-data"* festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

"ISO-Datenträgerimage"

"Festplattenimage"

"Diskettenimage"

"CD/DVD Disk"

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standard- oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Zustände eines Elements. Sie kann auch die Übergänge zwischen diesen angeforderten Zuzuständen angeben. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der in **LastErrorCode gemeldete** Fehler jetzt nicht mehr angezeigt wird. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)aber nicht verwendet.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die weitere Informationen zum in **LastErrorCode** aufgezeichneten Fehler sowie Informationen zu allen Korrekturmaßnahmen enthält, die durchgeführt werden können. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)aber nicht verwendet.

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die die Typen der Fehlererkennung und -korrektur beschreibt, die von diesem Gerät unterstützt werden. Diese Eigenschaft wird von [**CIM \_ StorageExtent geerbt.**](/windows/desktop/CIMWin32Prov/cim-storageextent)

</dd> <dt>

**ExtentStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Alle zusätzlichen Statusinformationen, die über die in **OperationalStatus und** anderen geerbten Eigenschaften erfassten hinausgehen.



| Wert                                                                            | Bedeutung                         |
|----------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>{ 2 }</dt> </dl> | Keine/Nicht zutreffend.<br/> |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Integrität des Elements. Dieses Attribut drückt die Integrität dieses Elements aus, aber nicht notwendigerweise die Integrität seiner Unterkomponenten. Die möglichen Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist, und 30 bedeutet, dass das Element vollständig nichtfunktional ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Freiformzeichenfolgen, die Erklärungen und Details hinter den Einträgen im **OtherIdentifyingInfo-Eigenschaftenarray** bereitstellen. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)und auf NULL **festgelegt.**

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der Konfiguration des virtuellen Computers. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**IsBasedOnUnderlyingRedundancy**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die zugrunde liegenden Speicherwerte in einer Speicherredundanzgruppe beteiligt sind. Diese Eigenschaft wird von [**CIM \_ StorageExtent geerbt.**](/windows/desktop/CIMWin32Prov/cim-storageextent)

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der letzte vom logischen Gerät gemeldete Fehlercode. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)aber nicht verwendet.

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft ist veraltet. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)aber nicht verwendet.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Bezeichnung, unter der das -Objekt bekannt ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)und ist mit der **ElementName-Eigenschaft** identisch.

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ StorageExtent geerbt.**](/windows/desktop/CIMWin32Prov/cim-storageextent)



| Wert                                                                         | Bedeutung                                 |
|-------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>1</dt> </dl>  | Andere<br/>                        |
| <dl> <dt>12</dt> </dl> | Name des Betriebssystemgeräts<br/> |



 

</dd> <dt>

**NameNamespace**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ StorageExtent geerbt.**](/windows/desktop/CIMWin32Prov/cim-storageextent)



| Wert                                                                        | Bedeutung                                      |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>1</dt> </dl> | Andere<br/>                             |
| <dl> <dt>8</dt> </dl> | Namespace des Betriebssystemgeräts<br/> |



 

</dd> <dt>

**NoSinglePointOfFailure**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob kein Single Point of Failure vorhanden ist. Diese Eigenschaft wird von [**CIM \_ StorageExtent geerbt.**](/windows/desktop/CIMWin32Prov/cim-storageextent)

</dd> <dt>

**NumberOfBlocks**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der aufeinander folgenden Blöcke, die jeweils die Größe des Werts in der **BlockSize-Eigenschaft** enthalten, die den Speicherblock bilden. Die Gesamtgröße des Speicherumfangs kann berechnet werden, indem der Wert der **BlockSize-Eigenschaft** mit dem Wert dieser Eigenschaft multipliziert wird. Wenn der Wert von **BlockSize** 1 ist, ist diese Eigenschaft die Gesamtgröße des Speicherblocks. Diese Eigenschaft wird von [**CIM \_ StorageExtent geerbt.**](/windows/desktop/CIMWin32Prov/cim-storageextent)

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt aktuelle Statusinformationen für die Betriebsbedingung des Elements zur Verfügung und kann verwendet werden, um weitere Details in Bezug auf den Wert der **EnabledState-Eigenschaft** zu erhalten. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Die aktuellen Status des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

Wenn die erforderliche QoS-Ebene für den virtuellen Datenträger nicht erfüllt werden kann, wird der primäre Status (OperationalStatus 0 ) auf Heruntergestuft (3) festgelegt, und das OperationalStatus-Array enthält zusätzlich einen sekundären Statuswert, der den spezifischen Grund für die \[ QoS-Bedingung angibt, gemäß dieser \] Tabelle.



| Wert                                                                                                                                                                                                    | Beschreibung                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Unzureichender Durchsatz (32788)<br/> | Die angeforderte MINDEST-IOPS-Rate ist für das Gerät derzeit nicht verfügbar. <br/> |



 

> [!Note]  
> OperationalStatus wird auch verwendet, um andere Fehler- oder Warnungsbedingungen zu melden (z. B. Protokollkonflikte zwischen VSP und VSC). Wenn mehrere Bedingungen vorhanden sind, wird der primäre Status heruntergestuft festgelegt, und mindestens ein sekundärer Statuswert wird in beliebiger Reihenfolge ab Index 1 in das Array gefüllt.

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span id="OK"></span><span id="ok"></span>**OK** (2)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Heruntergestuft** (3)


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht behebtbarer Fehler** (7)


</dt> <dd></dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10.

 

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (12)


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (13)


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität im Fehler** (16)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10.

 

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protokollkonflikt** (32775)


</dt> <dd></dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Kommunikations-Timed out** (32783)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10.

 

</dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Unzureichender Durchsatz** (32788)


</dt> <dd></dd> <dt>

<span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>

<span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**Unbekannte QoS-Richtlinien-ID** (32791)


</dt> <dd></dd> <dt>

<span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>

<span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS nicht unterstützt** (32792)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10.

 

</dd> <dt>

<span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>

<span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**QoS-Konfigurationskonflikt** (32793)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10.

 

</dd> <dt>

<span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>

<span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Datenträger voll** (32794)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10.

 

</dd> </dl>

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte oder deaktivierte Zustand des Elements, wenn die **EnabledState-Eigenschaft** auf 1 (Sonstige) festgelegt ist. Diese Eigenschaft muss auf **NULL** festgelegt werden, wenn **EnabledState** ein anderer Wert als 1 ist. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Alle zusätzlichen Daten, die über geräte-ID-Informationen hinausgehen und zum Identifizieren eines logischen Geräts verwendet werden können. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und auf **NULL** festgelegt.

</dd> <dt>

**OtherNameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die das Format der **Name-Eigenschaft** beschreibt, wenn **NameFormat** den Wert 1 (Other) enthält. Diese Eigenschaft wird von [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.

</dd> <dt>

**OtherNameNamespace**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Namespace der **Name-Eigenschaft** beschreibt, wenn **NameNamespace** den Wert 1 (Other) enthält. Diese Eigenschaft wird von [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.

</dd> <dt>

**PackageRedundancy**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der physischen Pakete, die derzeit ohne Datenverlust ausfallen können. Diese Eigenschaft wird von [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Energieverwaltungsfunktionen des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Gerät mit Strom verwaltet werden kann. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der aufeinanderfolgenden Stunden, in denen dieses Gerät seit dem letzten Energiesparzyklus eingeschaltet wurde. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt statusinformationen auf hoher Ebene bereit. Diese Eigenschaft sollte in Verbindung mit der **DetailedStatus-Eigenschaft** verwendet werden, um detaillierte und detaillierte Integritätsstatusinformationen für das Element und seine Unterkomponenten bereitzustellen. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Ursprünglich**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das enthaltende System dieses betriebsbereite Element erstellen oder löschen kann. Diese Eigenschaft wird von [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und für dateibasierte Medien auf **False** und für Pass-Through-Medien auf **True** festgelegt.

</dd> <dt>

**Zweck**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die die Medien und/oder deren Verwendung beschreibt. Diese Eigenschaft wird von [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der zuletzt angeforderte oder gewünschte Zustand für das Element. Der tatsächliche Zustand des Elements wird durch **EnabledState** dargestellt. Diese Eigenschaft wird bereitgestellt, um den zuletzt angeforderten und den aktuellen aktivierten oder deaktivierten Status zu vergleichen. Eine bestimmte Instanz von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) unterstützt die **RequestStateChange-Methode** möglicherweise nicht. In diesem Fall wird der Wert 12 (Nicht zutreffend) verwendet. Diese Eigenschaft wird von **CIM \_ EnabledLogicalElement** geerbt.

</dd> <dt>

**SequentialAccess**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob ein Medienzugriffsgerät sequenziell auf den Speicher zugreift. Pass-Through-Bandmedien sind ein Beispiel für einen Speicherbereich, auf den sequenziell zugegriffen wird. Diese Eigenschaft wird von [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Status des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeichenfolgen, die die verschiedenen **OperationalStatus-Arraywerte** beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Status des logischen Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Erstellungsklasse des Bereichssystems. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Bezeichner für den bereichsspezifischen virtuellen Computer. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der Stunden, in denen dieses Gerät eingeschaltet wurde. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)aber nicht verwendet.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Zielzustand an, in den die Instanz übergibt. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt,**](/previous-versions//cc136818(v=vs.85))aber nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ LogicalDisk-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ LogicalDisk**](cim-logicaldisk.md)
</dt> <dt>

[**CIM \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk)
</dt> <dt>

[**Msvm \_ StorageAlert**](msvm-storagealert.md)
</dt> <dt>

[Storage Klassen](storage-classes.md)
</dt> </dl>

 

