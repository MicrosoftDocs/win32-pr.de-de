---
description: Stellt einen IDE-Controller dar.
ms.assetid: DFD4D90E-CA91-42B3-AC88-9E9D26089C36
title: Msvm_IDEController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_IDEController
- Msvm_IDEController.SetPowerState
- Msvm_IDEController.EnableDevice
- Msvm_IDEController.OnlineDevice
- Msvm_IDEController.QuiesceDevice
- Msvm_IDEController.SaveProperties
- Msvm_IDEController.RestoreProperties
- Msvm_IDEController.InstanceID
- Msvm_IDEController.Caption
- Msvm_IDEController.Description
- Msvm_IDEController.ElementName
- Msvm_IDEController.InstallDate
- Msvm_IDEController.Name
- Msvm_IDEController.OperationalStatus
- Msvm_IDEController.StatusDescriptions
- Msvm_IDEController.Status
- Msvm_IDEController.HealthState
- Msvm_IDEController.CommunicationStatus
- Msvm_IDEController.DetailedStatus
- Msvm_IDEController.OperatingStatus
- Msvm_IDEController.PrimaryStatus
- Msvm_IDEController.EnabledState
- Msvm_IDEController.OtherEnabledState
- Msvm_IDEController.RequestedState
- Msvm_IDEController.EnabledDefault
- Msvm_IDEController.TimeOfLastStateChange
- Msvm_IDEController.AvailableRequestedStates
- Msvm_IDEController.TransitioningToState
- Msvm_IDEController.SystemCreationClassName
- Msvm_IDEController.SystemName
- Msvm_IDEController.CreationClassName
- Msvm_IDEController.DeviceID
- Msvm_IDEController.PowerManagementSupported
- Msvm_IDEController.PowerManagementCapabilities
- Msvm_IDEController.Availability
- Msvm_IDEController.StatusInfo
- Msvm_IDEController.LastErrorCode
- Msvm_IDEController.ErrorDescription
- Msvm_IDEController.ErrorCleared
- Msvm_IDEController.OtherIdentifyingInfo
- Msvm_IDEController.PowerOnHours
- Msvm_IDEController.TotalPowerOnHours
- Msvm_IDEController.IdentifyingDescriptions
- Msvm_IDEController.AdditionalAvailability
- Msvm_IDEController.MaxQuiesceTime
- Msvm_IDEController.TimeOfLastReset
- Msvm_IDEController.ProtocolSupported
- Msvm_IDEController.MaxNumberControlled
- Msvm_IDEController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d71755b9aa9bb341b5b4a9feb864c20a16ccaf28bc2ab2ede96a713307adaf82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147759"
---
# <a name="msvm_idecontroller-class"></a>\_Msvm-IDEController-Klasse

Stellt einen IDE-Controller dar. Diese Klasse kann bis zu vier Laufwerke unterstützen, die an den Controller angefügt sind. Der IDE-Controller ist auf dem virtuellen Computer behoben und verfügt daher nicht über einen zugeordneten Ressourcenpool.

> [!Note]  
> Diese Klasse ist für virtuelle Computer der Generation 2 nicht verfügbar.

 

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_IDEController : CIM_IDEController
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual IDE Controller";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_IDEController";
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
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 37;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription = "IDE";
};
```

## <a name="members"></a>Member

Die **\_ Msvm-IDEController-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **\_ Msvm-IDEController-Klasse** verfügt über diese Methoden.



| Methode                                                              | Beschreibung                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                    | Diese Methode wird nicht unterstützt.<br/> |
| **OnlineGeräte**                                                    | Diese Methode wird nicht unterstützt.<br/> |
| **QuiesceDevice**                                                   | Diese Methode wird nicht unterstützt.<br/> |
| [**RequestStateChange**](msvm-idecontroller-requeststatechange.md) | Fordert eine Zustandsänderung an.<br/>      |
| [**Zurücksetzen**](msvm-idecontroller-reset.md)                           | Setzt das virtuelle Gerät zurück.<br/>    |
| **RestoreProperties**                                               | Diese Methode wird nicht unterstützt.<br/> |
| **SaveProperties**                                                  | Diese Methode wird nicht unterstützt.<br/> |
| **SetPowerState**                                                   | Diese Methode wird nicht unterstützt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **\_ Msvm-IDEController-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Alle zusätzlichen Verfügbarkeiten und Status des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die primäre Verfügbarkeit und der Status des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

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

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.



| Wert                                                                                         | Bedeutung                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>"IDE-Controller 0"</dt> </dl> | Die -Instanz stellt den primären Controller dar.<br/>   |
| <dl> <dt>"IDE-Controller 1"</dt> </dl> | Die -Instanz stellt den sekundären Controller dar.<br/> |



 

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

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



| Wert                                                                                         | Bedeutung                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>"IDE-Controller 0"</dt> </dl> | Die -Instanz stellt den primären Controller dar.<br/>   |
| <dl> <dt>"IDE-Controller 1"</dt> </dl> | Die -Instanz stellt den sekundären Controller dar.<br/> |



 

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standard- oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Status eines Elements. Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt.

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

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Integrität des Elements. Dieses Attribut drückt die Integrität dieses Elements aus, jedoch nicht notwendigerweise die Integrität seiner Unterkomponenten. Die möglichen Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionslos ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Freiformzeichenfolgen, die Erklärungen und Details hinter den Einträgen im **OtherIdentifyingInfo-Eigenschaftenarray** bereitstellen. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

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

**LastErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der letzte vom logischen Gerät gemeldete Fehlercode. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**MaxNumberControlled**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl direkt adressierbarer Entitäten, die von diesem Controller unterstützt werden. Der Wert 0 sollte verwendet werden, wenn die Zahl unbekannt oder unbegrenzt ist. Das Protokoll, das vom Controller für den Zugriff auf kontrollierte Geräte verwendet wird. Diese Eigenschaft wird vom [**\_ CIM-Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft ist veraltet. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Bezeichnung, mit der das Objekt bekannt ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und entspricht der **ElementName-Eigenschaft.**

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

Die aktuellen Status des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

**ProtocolDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die weitere Informationen im Zusammenhang mit dem vom Controller unterstützten Protokoll bereitstellt. Diese Eigenschaft wird vom [**\_ CIM-Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.

</dd> <dt>

**ProtocolSupported**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Protokoll, das vom Controller für den Zugriff auf kontrollierte Geräte verwendet wird. Diese Eigenschaft wird vom [**\_ CIM-Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.



| Wert                                                                         | Bedeutung        |
|-------------------------------------------------------------------------------|----------------|
| <dl> <dt>37</dt> </dl> | IDE<br/> |



 

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der zuletzt angeforderte oder gewünschte Zustand für das Element. Der tatsächliche Zustand des Elements wird durch **EnabledState** dargestellt. Diese Eigenschaft wird bereitgestellt, um den zuletzt angeforderten und den aktuellen aktivierten oder deaktivierten Status zu vergleichen. Eine bestimmte Instanz eines aktivierten logischen Elements unterstützt **requestedStateChange** möglicherweise nicht. In diesem Fall wird der Wert 12 (Nicht zutreffend) verwendet. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt.

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

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das letzte Einschalten des virtuellen Computers. Diese Eigenschaft wird vom [**\_ CIM-Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt.

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

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **\_ Msvm-IDEController-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**\_CIM-IDEController**](cim-idecontroller.md)
</dt> <dt>

[**\_CIM-IDEController**](/previous-versions//cc136863(v=vs.85))
</dt> <dt>

[Storage Klassen](storage-classes.md)
</dt> </dl>

 

