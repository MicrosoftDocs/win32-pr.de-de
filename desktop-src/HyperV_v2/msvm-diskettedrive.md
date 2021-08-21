---
description: Stellt ein Diskettenlaufwerk innerhalb des virtuellen Computers dar.
ms.assetid: 4624ABAF-3761-416F-9044-7A39EBF53D3D
title: Msvm_DisketteDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive
- Msvm_DisketteDrive.SetPowerState
- Msvm_DisketteDrive.EnableDevice
- Msvm_DisketteDrive.OnlineDevice
- Msvm_DisketteDrive.QuiesceDevice
- Msvm_DisketteDrive.SaveProperties
- Msvm_DisketteDrive.RestoreProperties
- Msvm_DisketteDrive.InstanceID
- Msvm_DisketteDrive.Caption
- Msvm_DisketteDrive.Description
- Msvm_DisketteDrive.ElementName
- Msvm_DisketteDrive.InstallDate
- Msvm_DisketteDrive.Name
- Msvm_DisketteDrive.OperationalStatus
- Msvm_DisketteDrive.StatusDescriptions
- Msvm_DisketteDrive.Status
- Msvm_DisketteDrive.HealthState
- Msvm_DisketteDrive.CommunicationStatus
- Msvm_DisketteDrive.DetailedStatus
- Msvm_DisketteDrive.OperatingStatus
- Msvm_DisketteDrive.PrimaryStatus
- Msvm_DisketteDrive.EnabledState
- Msvm_DisketteDrive.OtherEnabledState
- Msvm_DisketteDrive.RequestedState
- Msvm_DisketteDrive.EnabledDefault
- Msvm_DisketteDrive.TimeOfLastStateChange
- Msvm_DisketteDrive.AvailableRequestedStates
- Msvm_DisketteDrive.TransitioningToState
- Msvm_DisketteDrive.SystemCreationClassName
- Msvm_DisketteDrive.SystemName
- Msvm_DisketteDrive.CreationClassName
- Msvm_DisketteDrive.DeviceID
- Msvm_DisketteDrive.PowerManagementSupported
- Msvm_DisketteDrive.PowerManagementCapabilities
- Msvm_DisketteDrive.Availability
- Msvm_DisketteDrive.StatusInfo
- Msvm_DisketteDrive.LastErrorCode
- Msvm_DisketteDrive.ErrorDescription
- Msvm_DisketteDrive.ErrorCleared
- Msvm_DisketteDrive.OtherIdentifyingInfo
- Msvm_DisketteDrive.PowerOnHours
- Msvm_DisketteDrive.TotalPowerOnHours
- Msvm_DisketteDrive.IdentifyingDescriptions
- Msvm_DisketteDrive.AdditionalAvailability
- Msvm_DisketteDrive.MaxQuiesceTime
- Msvm_DisketteDrive.Capabilities
- Msvm_DisketteDrive.CapabilityDescriptions
- Msvm_DisketteDrive.ErrorMethodology
- Msvm_DisketteDrive.CompressionMethod
- Msvm_DisketteDrive.NumberOfMediaSupported
- Msvm_DisketteDrive.MaxMediaSize
- Msvm_DisketteDrive.DefaultBlockSize
- Msvm_DisketteDrive.MaxBlockSize
- Msvm_DisketteDrive.MinBlockSize
- Msvm_DisketteDrive.NeedsCleaning
- Msvm_DisketteDrive.MediaIsLocked
- Msvm_DisketteDrive.Security
- Msvm_DisketteDrive.LastCleaned
- Msvm_DisketteDrive.MaxAccessTime
- Msvm_DisketteDrive.UncompressedDataRate
- Msvm_DisketteDrive.LoadTime
- Msvm_DisketteDrive.UnloadTime
- Msvm_DisketteDrive.MountCount
- Msvm_DisketteDrive.TimeOfLastMount
- Msvm_DisketteDrive.TotalMountTime
- Msvm_DisketteDrive.UnitsDescription
- Msvm_DisketteDrive.MaxUnitsBeforeCleaning
- Msvm_DisketteDrive.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4428d3f1de37b704312753223825f04c1ad251bdc5775ae68a2d7e291b2cfe0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148609"
---
# <a name="msvm_diskettedrive-class"></a>Msvm \_ DisketteDrive-Klasse

Stellt ein Diskettenlaufwerk innerhalb des virtuellen Computers dar. Ein Diskettenlaufwerk kann mit einer Datei aufgefüllt werden, die Diskettenmedien darstellt, oder das Laufwerk kann leer sein. Physische Medien werden nicht unterstützt. Es gibt genau ein Diskettenlaufwerk pro Diskettencontroller und ist nicht wechselbar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteDrive : CIM_DisketteDrive
{
  string   InstanceID;
  string   Caption = "Diskette Drive";
  string   Description = "Microsoft Virtual Diskette Drive";
  string   ElementName = "Diskette Drive";
  datetime InstallDate;
  string   Name = "Diskette Drive";
  uint16   OperationalStatus[] = { 2 };
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
  uint16   CreationClassName = "Msvm_DisketteDrive";
  string   DeviceID = "Microsoft:GUID\device-specific-data";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint16   Capabilities[] = {3, 4, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Writing", "Supports Removable Media"};
  string   ErrorMethodology = { "None" };
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 1440;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize = 512;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = False;
  uint16   Security = 3;
  datetime LastCleaned;
  uint64   MaxAccessTime = 0;
  uint32   UncompressedDataRate;
  uint64   LoadTime = 0;
  uint64   UnloadTime = 0;
  uint64   MountCount = 0;
  datetime TimeOfLastMount;
  uint64   TotalMountTime = 0;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning = 18446744073709551615;
  uint64   UnitsUsed = 0;
};
```

## <a name="members"></a>Member

Die **Msvm \_ DisketteDrive-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Msvm \_ DisketteDrive-Klasse** verfügt über diese Methoden.



| Methode                                                              | Beschreibung                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                    | Diese Methode wird nicht unterstützt.<br/> |
| [**LockMedia**](msvm-diskettedrive-lockmedia.md)                   | Sperrt oder gibt die Medien frei.<br/>  |
| **OnlineDevice**                                                    | Diese Methode wird nicht unterstützt.<br/> |
| **QuiesceDevice**                                                   | Diese Methode wird nicht unterstützt.<br/> |
| [**RequestStateChange**](msvm-diskettedrive-requeststatechange.md) | Fordert eine Zustandsänderung an.<br/>      |
| [**Zurücksetzen**](msvm-diskettedrive-reset.md)                           | Setzt das virtuelle Gerät zurück.<br/>    |
| **RestoreProperties**                                               | Diese Methode wird nicht unterstützt.<br/> |
| **SaveProperties**                                                  | Diese Methode wird nicht unterstützt.<br/> |
| **SetPowerState**                                                   | Diese Methode wird nicht unterstützt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ DisketteDrive-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Alle zusätzlichen Verfügbarkeiten und Status des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)



| Wert                                                                        | Bedeutung                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>6</dt> </dl> | Nicht zutreffend<br/> |



 

</dd> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die primäre Verfügbarkeit und der Status des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)



| Wert                                                                        | Bedeutung                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>6</dt> </dl> | Nicht zutreffend<br/> |



 

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Werte für den *RequestedState-Parameter* der [**RequestStateChange-Methode**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) an, die zum Initiieren einer Zustandsänderung verwendet wird. Die aufgeführten Werte sind eine Teilmenge der Werte, die in der **RequestedStatesSupported-Eigenschaft** der zugeordneten Instanz von **CIM \_ EnabledLogicalElementCapabilities** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ EnabledLogicalElement-Objekts**](/previous-versions//cc136818(v=vs.85)) sind. Diese Eigenschaft kann nicht NULL sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands anknullen kann. Diese Eigenschaft ist **NULL,** wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.

Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Funktionen des Medienzugriffsgeräts. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)und auf die folgenden Werte festgelegt.



| Wert                                                                                | Bedeutung                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>{3, 4, 7}</dt> </dl> |                                                                                                 |
| <dl> <dt>3</dt> </dl>         | Der entsprechende Eintrag in **CapabilityDescriptions** ist "Random Access".<br/>            |
| <dl> <dt>4</dt> </dl>         | Der entsprechende Eintrag in **CapabilityDescriptions ist** "Supports Writing".<br/>         |
| <dl> <dt>7</dt> </dl>         | Der entsprechende Eintrag in **CapabilityDescriptions ist** "Supports Removable Media".<br/> |



 

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Freiformzeichenfolgen, das ausführliche Erläuterungen zu Den Zugriffsgerätefeatures bietet, die im **Capabilities-Eigenschaftenarray** angegeben sind. Jeder Eintrag dieses Arrays bezieht sich  auf den Eintrag im Capabilities-Array, der sich am gleichen Index befindet. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Algorithmus oder das Tool zum Komprimieren der logischen Datei angibt. Wenn das Komprimierungsschema unbekannt oder nicht beschrieben ist, verwenden Sie "Unknown". Wenn die logische Datei komprimiert ist, das Komprimierungsschema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "Compressed". Wenn die logische Datei nicht komprimiert ist, verwenden Sie "Nicht komprimiert". Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.

"Nicht komprimiert"

"Unbekannt"

"Komprimiert"

"Nicht komprimiert"

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**DefaultBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standardblockgröße für das Gerät in Bytes. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.

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

**Deviceid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und auf "Microsoft:*GUID* \\ *device-specific-data"* festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standard- oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) geerbt und immer auf 2 (Aktiviert) festgelegt.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Status eines Elements. Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt und immer auf 5 (Nicht zutreffend) festgelegt.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die weitere Informationen zu dem in **LastErrorCode** aufgezeichneten Fehler und Informationen zu möglichen Korrekturmaßnahmen bereitstellt. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die die Typen der Fehlererkennung und -korrektur beschreibt, die von diesem Gerät unterstützt werden. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Integrität des Elements. Dieses Attribut drückt die Integrität dieses Elements aus, jedoch nicht notwendigerweise die Integrität seiner Unterkomponenten. Die möglichen Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionslos ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und immer auf 5 festgelegt.

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Freiformzeichenfolgen, die Erklärungen und Details hinter den Einträgen im **OtherIdentifyingInfo-Eigenschaftenarray** bereitstellen. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und auf **NULL** festgelegt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der Konfiguration des virtuellen Computers. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

**LastCleaned**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit der letzten Bereinigung des Geräts. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der letzte vom logischen Gerät gemeldete Fehlercode. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**LoadTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeit in Millisekunden vom Laden bis zum Lesen oder Schreiben eines Mediums. Bei Datenträgerlaufwerken ist dies z. B. das Intervall zwischen einem Datenträger, der sich nicht auf den Datenträger bewegt und meldet, dass er für Lese-/Schreibzugriff bereit ist (d. h. der Datenträger, der mit nominalen Geschwindigkeiten rotiert). Bei Bandlaufwerken ist dies die Zeit zwischen dem Einjizierten eines Mediums und dem Melden, dass es für eine Anwendung bereit ist. Dies befindet sich in der Regel im BOT-Bereich des Bandes. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)

</dd> <dt>

**MaxAccessTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeit in Millisekunden, die vom ersten Speicherort auf dem Medium zu dem Ort bewegt werden soll, der in Bezug auf die Zeit am weitesten ist. Bei einem Laufwerk stellt dies eine vollständige Such- und vollständige Drehverzögerung dar. Bei Bandlaufwerken stellt dies eine Suche vom Anfang des Bandes bis zum physisch entferntesten Punkt dar. (Das Ende eines Bandes kann sich an seinem physisch am weitesten entfernten Punkt befindet, aber dies ist nicht notwendigerweise der Fall.) Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)

</dd> <dt>

**MaxBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Blockgröße (in Bytes) für Medien, auf die vom Gerät zugegriffen wird. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)

</dd> <dt>

**MaxMediaSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Größe der von diesem Gerät unterstützten Medien in Kilobyte. Kilobytes werden als Anzahl von Bytes multipliziert mit 1000 interpretiert (nicht als Anzahl von Bytes multipliziert mit 1024). Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft ist veraltet. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)aber nicht verwendet.

</dd> <dt>

**MaxUnitsBeforeCleaning**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximalen Einheiten, die verwendet werden können, bevor das Gerät bereinigt werden soll. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)

</dd> <dt>

**MediaIsLocked**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn das Medium auf dem Gerät gesperrt ist und nicht ausjiziert werden kann. andernfalls **False.** Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)

</dd> <dt>

**MinBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die minimale Blockgröße in Byte für Medien, auf die vom Gerät zugegriffen wird. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)

</dd> <dt>

**MountCount**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Für ein Gerät, das Wechselmedien unterstützt, die Anzahl der Einlagerungen von Medien für die Datenübertragung oder die Bereinigung des Geräts. Für Geräte, die auf nicht bewegbare Medien wie Festplatten zugreifen, ist diese Eigenschaft nicht anwendbar und sollte auf 0 festgelegt werden. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Bezeichnung, unter der das -Objekt bekannt ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)und ist mit der **ElementName-Eigenschaft** identisch.

</dd> <dt>

**NeedsCleaning**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True,** wenn das Medienzugriffsgerät eine Bereinigung benötigt. andernfalls **False.** Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)

</dd> <dt>

**NumberOfMediaSupported**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von mehreren einzelnen Medien, die unterstützt oder eingefügt werden können. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)

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
</dt> </dl>

Die aktuellen Status des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt,**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)und jedes Arrayelement ist immer auf 2 (OK) festgelegt.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte oder deaktivierte Zustand des Elements, wenn die **EnabledState-Eigenschaft** auf 1 (Sonstige) festgelegt ist. Diese Eigenschaft muss auf NULL **festgelegt** werden, wenn **EnabledState** ein anderer Wert als 1 ist. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt**](/previous-versions//cc136818(v=vs.85))und immer auf NULL **festgelegt.**

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Alle zusätzlichen Daten, die über die Geräte-ID-Informationen hinausgehen und zum Identifizieren eines logischen Geräts verwendet werden können. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)und auf NULL **festgelegt.**

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Energieverwaltungsfunktionen des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)aber nicht verwendet.

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Gerät mit Strom verwaltet werden kann. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)aber nicht verwendet.

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der aufeinanderfolgenden Stunden, die dieses Gerät seit seinem letzten Energiezyklus eingeschaltet wurde. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)aber nicht verwendet.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt statusinformationen auf hoher Ebene bereit. Diese Eigenschaft sollte in Verbindung mit der **DetailedStatus-Eigenschaft** verwendet werden, um detaillierte und detaillierte Integritätsstatusinformationen für das Element und seine Unterkomponenten bereitzustellen. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der zuletzt angeforderte oder gewünschte Zustand für das Element. Der tatsächliche Zustand des Elements wird durch **EnabledState** dargestellt. Diese Eigenschaft wird bereitgestellt, um den zuletzt angeforderten und den aktuellen aktivierten oder deaktivierten Status zu vergleichen. Eine bestimmte Instanz von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) unterstützt **requestStateChange** möglicherweise nicht. In diesem Fall wird der Wert 12 (Nicht zutreffend) verwendet. Diese Eigenschaft wird von **CIM \_ EnabledLogicalElement** geerbt und immer auf 12 (Nicht zutreffend) festgelegt.

</dd> <dt>

**Sicherheit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die für das Gerät definierte Betriebssicherheit. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.



| Wert                                                                        | Bedeutung         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <dt>3</dt> </dl> | Keine<br/> |



 

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

Zeichenfolgen, die die verschiedenen **OperationalStatus-Arraywerte** beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Arrayelement ist immer auf "OK" festgelegt.

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

**TimeOfLastMount**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Für ein Gerät, das Wechselmedien unterstützt, ist dies das datums- und uhrzeit letzte Datum und die uhrzeit, zu der das Medium auf dem Gerät eingebunden wurde. Für Geräte, die auf nicht wechselbare Medien wie Festplatten zugreifen, hat diese Eigenschaft keine Bedeutung und ist nicht anwendbar. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**TotalMountTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Für ein Gerät, das Wechselmedien unterstützt, die Gesamtzeit (in Sekunden), die das Medium für die Datenübertragung oder zum Bereinigen des Geräts bereitgestellt wurde. Für Geräte, die auf nicht wechselbare Medien wie Festplatten zugreifen, ist diese Eigenschaft nicht anwendbar und sollte auf 0 festgelegt werden. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtzahl der Stunden, in denen dieses Gerät eingeschaltet wurde. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Zielzustand an, in den die Instanz übergehen soll. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.

</dd> <dt>

**UncompressedDataRate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die dauerhafte Datenübertragungsrate in KB/s, die das Gerät aus einem Medium lesen und auf ein Medium schreiben kann. Dies ist eine dauerhafte Rohdatenrate. Maximale Raten oder Raten unter der Annahme der Komprimierung sollten in dieser Eigenschaft nicht gemeldet werden. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.

</dd> <dt>

**UnitsDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Einheiten relativ zur Verwendung in **MaxUnitsBeforeCleaning.** Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und auf **NULL** festgelegt.

</dd> <dt>

**UnitsUsed**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Anzahl der verwendeten Einheiten. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.

</dd> <dt>

**UnloadTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeit in Millisekunden, nach der ein Medium gelesen oder geschrieben werden kann, bis es entladen wird. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ DisketteDrive-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ DisketteDrive**](cim-diskettedrive.md)
</dt> <dt>

[**CIM \_ DisketteDrive**](/windows/desktop/CIMWin32Prov/cim-diskettedrive)
</dt> <dt>

[Storage Klassen](storage-classes.md)
</dt> </dl>

 

