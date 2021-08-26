---
description: Stellt ein PS2-Mausgerät dar.
ms.assetid: 5e02ec15-95e6-4d82-833e-a48ca117a890
title: Msvm_Ps2Mouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse
- Msvm_Ps2Mouse.SetPowerState
- Msvm_Ps2Mouse.EnableDevice
- Msvm_Ps2Mouse.OnlineDevice
- Msvm_Ps2Mouse.QuiesceDevice
- Msvm_Ps2Mouse.SaveProperties
- Msvm_Ps2Mouse.RestoreProperties
- Msvm_Ps2Mouse.InstanceID
- Msvm_Ps2Mouse.Caption
- Msvm_Ps2Mouse.Description
- Msvm_Ps2Mouse.ElementName
- Msvm_Ps2Mouse.InstallDate
- Msvm_Ps2Mouse.Name
- Msvm_Ps2Mouse.OperationalStatus
- Msvm_Ps2Mouse.StatusDescriptions
- Msvm_Ps2Mouse.Status
- Msvm_Ps2Mouse.HealthState
- Msvm_Ps2Mouse.CommunicationStatus
- Msvm_Ps2Mouse.DetailedStatus
- Msvm_Ps2Mouse.OperatingStatus
- Msvm_Ps2Mouse.PrimaryStatus
- Msvm_Ps2Mouse.EnabledState
- Msvm_Ps2Mouse.OtherEnabledState
- Msvm_Ps2Mouse.RequestedState
- Msvm_Ps2Mouse.EnabledDefault
- Msvm_Ps2Mouse.TimeOfLastStateChange
- Msvm_Ps2Mouse.AvailableRequestedStates
- Msvm_Ps2Mouse.TransitioningToState
- Msvm_Ps2Mouse.SystemCreationClassName
- Msvm_Ps2Mouse.SystemName
- Msvm_Ps2Mouse.CreationClassName
- Msvm_Ps2Mouse.DeviceID
- Msvm_Ps2Mouse.PowerManagementSupported
- Msvm_Ps2Mouse.PowerManagementCapabilities
- Msvm_Ps2Mouse.Availability
- Msvm_Ps2Mouse.StatusInfo
- Msvm_Ps2Mouse.LastErrorCode
- Msvm_Ps2Mouse.ErrorDescription
- Msvm_Ps2Mouse.ErrorCleared
- Msvm_Ps2Mouse.OtherIdentifyingInfo
- Msvm_Ps2Mouse.PowerOnHours
- Msvm_Ps2Mouse.TotalPowerOnHours
- Msvm_Ps2Mouse.IdentifyingDescriptions
- Msvm_Ps2Mouse.AdditionalAvailability
- Msvm_Ps2Mouse.MaxQuiesceTime
- Msvm_Ps2Mouse.IsLocked
- Msvm_Ps2Mouse.PointingType
- Msvm_Ps2Mouse.NumberOfButtons
- Msvm_Ps2Mouse.Handedness
- Msvm_Ps2Mouse.Resolution
- Msvm_Ps2Mouse.AbsoluteCoordinates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8f5c23b5845dcceaf1ec8b7ad813596308a5625c9446cc18bfc5b82e9e73494e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046450"
---
# <a name="msvm_ps2mouse-class"></a>Msvm \_ Ps2Mouse-Klasse

Stellt ein PS2-Mausgerät dar. Instanzen dieser Klasse sind logische Geräte, die immer auf einem virtuellen Computer vorhanden sind und daher nicht über einen Ressourcenpool zugeordnet werden. Eine Instanz ist immer auf einem virtuellen Computer vorhanden.

> [!Note]  
> Diese Klasse ist für virtuelle Computer der Generation 2 nicht verfügbar.

 

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Ps2Mouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Emulated Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_PS2Mouse";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = False;
};
```

## <a name="members"></a>Member

Die **Msvm \_ Ps2Mouse-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Msvm \_ Ps2Mouse-Klasse** verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                                                                           |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**ClickButton**](clickbutton-msvm-ps2mouse.md)                 | Simuliert einen Klick auf eine Schaltfläche , eine Nach-unten-Sequenz, auf der angegebenen Geräteschaltfläche.<br/>              |
| **EnableDevice**                                                 | Diese Methode wird nicht unterstützt.<br/>                                                              |
| [**GetButtonState**](getbuttonstate-msvm-ps2mouse.md)           | Ruft den aktuellen Zustand der angegebenen Geräteschaltfläche ab.<br/>                                |
| **OnlineGeräte**                                                 | Diese Methode wird nicht unterstützt.<br/>                                                              |
| **QuiesceDevice**                                                | Diese Methode wird nicht unterstützt.<br/>                                                              |
| [**RequestStateChange**](msvm-ps2mouse-requeststatechange.md)   | Fordert eine Zustandsänderung an.<br/>                                                                   |
| [**Zurücksetzen**](msvm-ps2mouse-reset.md)                             | Setzt das Gerät zurück.<br/>                                                                         |
| **RestoreProperties**                                            | Diese Methode wird nicht unterstützt.<br/>                                                              |
| **SaveProperties**                                               | Diese Methode wird nicht unterstützt.<br/>                                                              |
| [**SetButtonState**](setbuttonstate-msvm-ps2mouse.md)           | Legt den aktuellen Zustand der angegebenen Geräteschaltfläche fest.<br/>                                     |
| **SetPowerState**                                                | Diese Methode wird nicht unterstützt.<br/>                                                              |
| [**SetRelativePosition**](setrelativeposition-msvm-ps2mouse.md) | Versetzt die Position des Mauszeigers durch die angegebenen horizontalen und vertikalen Deltas.<br/> |
| [**SetScrollPosition**](setscrollposition-msvm-ps2mouse.md)     | Passt die Z-Koordinate des Radsteuerelements des zeigenden Geräts an.<br/>                      |



 

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ Ps2Mouse-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AbsoluteCoordinates**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Gerät mit absoluten Koordinaten arbeitet. Wenn diese Einstellung nicht festgelegt ist, sind die Koordinaten des Geräts relativ.

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Alle zusätzlichen Verfügbarkeiten und Status des Geräts, die über den in der **Availability-Eigenschaft** angegebenen hinausgehen. Die **Availability-Eigenschaft** gibt den primären Status und die Verfügbarkeit des Geräts an. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.



| Wert                                                                        | Bedeutung                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>6</dt> </dl> | Nicht zutreffend<br/> |



 

</dd> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die primäre Verfügbarkeit und der Status des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.



| Wert                                                                        | Bedeutung                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>6</dt> </dl> | Nicht zutreffend<br/> |



 

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Werte für den *RequestedState-Parameter* der **RequestStateChange-Methode** an. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)
</dt> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Reservierter Anbieter** (0x8000. )
</dt> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (256)
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit anderen Schlüsseleigenschaften der -Klasse ermöglicht diese Eigenschaft die eindeutige Identifizierung aller Instanzen der -Klasse und ihrer Unterklassen. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
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

Ergänzt die **PrimaryStatus-Eigenschaft** um zusätzliche Statusdetails. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Besendung** (2)
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht behebtbarer Fehler** (4)
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität im Fehler** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Reservierter Anbieter** (0x8000. )
</dt> </dl>

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (64)
</dt> </dl>

Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)und immer auf "Microsoft:*GUID"* festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Mit dieser Eigenschaft kann jede Instanz zusätzlich zu ihren Schlüsseleigenschaften, Identitätsdaten und Beschreibungsinformationen einen Anzeigenamen definieren. Die [**Name-Eigenschaft**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) der **CIM \_ ManagedSystemElement-Klasse** wird auch als Anzeigename definiert. Es wird jedoch häufig als Unterklasse als Schlüssel klassifiziert. Es ist nicht sinnvoll, dass dieselbe Eigenschaft sowohl Identität als auch einen Anzeigenamen ohne Inkonsistenzen vermitteln kann. Wenn [**Name**](msvm-keyboard.md) vorhanden ist und kein Schlüssel ist (z. B. für Instanzen von [**CIM \_ LogicalDevice),**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)können die gleichen Informationen sowohl in den **Eigenschaften Name** als auch **ElementName vorhanden** sein. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Mouse" festgelegt.

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standard- oder Startkonfiguration eines Administrators für den Aktiviert-Zustand eines Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Zustände eines Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

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

**Händigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Konfiguration des zeigenden Geräts für den rechten oder linken Betrieb. Diese Eigenschaft wird von [**CIM \_ PointingDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)



| Wert                                                                        | Bedeutung                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>0</dt> </dl> | Unbekannt<br/>                 |
| <dl> <dt>1</dt> </dl> | Nicht zutreffend<br/>         |
| <dl> <dt>2</dt> </dl> | Rechtshändiger Vorgang.<br/> |
| <dl> <dt>3</dt> </dl> | Linkshändiger Vorgang.<br/>  |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Integrität des Elements. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)und immer auf 5 (OK) festgelegt.

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Freiformzeichenfolgen, die Erklärungen und Details hinter den Einträgen im [**OtherIdentifyingInfo-Array**](msvm-keyboard.md) bereitstellen. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung des virtuellen Computers. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

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

**IsLocked**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Gerät gesperrt ist, was Benutzereingaben oder -ausgaben verhindert. Diese Eigenschaft wird von [**CIM \_ UserDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-userdevice)

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

Diese Eigenschaft ist veraltet. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (1024)
</dt> </dl>

Die Bezeichnung, unter der das -Objekt bekannt ist. Bei Unterklassen kann diese Eigenschaft überschrieben werden, um eine Schlüsseleigenschaft zu sein. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**NumberOfButtons**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der Schaltflächen auf dem zeigenden Gerät. Diese Eigenschaft wird von [**CIM \_ PointingDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt aktuelle Statusinformationen für die Betriebsbedingung des Elements zur Verfügung und kann verwendet werden, um weitere Details in Bezug auf den Wert der **EnabledState-Eigenschaft** zu erhalten. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Ab** (3)
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Wird beendet** (4)
</dt> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)
</dt> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)
</dt> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhend** (7)
</dt> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)
</dt> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)
</dt> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Sollgrating** (10)
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Momentaufnahmen** (12)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunterfahren** (13)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Im Test** (14)
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Reservierter Anbieter** (0x8000. )
</dt> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Status des Elements. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)und immer auf 2 (OK) festgelegt.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte oder deaktivierte Zustand des Elements, wenn die [**EnabledState-Eigenschaft**](msvm-keyboard.md) auf 1 (Sonstige) festgelegt ist. Diese Eigenschaft muss auf NULL **festgelegt** werden, wenn **EnabledState** ein anderer Wert als 1 ist. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Alle zusätzlichen Daten, die über die Geräte-ID-Informationen hinausgehen und zum Identifizieren eines logischen Geräts verwendet werden können. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

</dd> <dt>

**PointingType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ des zeigenden Geräts. Diese Eigenschaft wird von [**CIM \_ PointingDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)



| Wert                                                                        | Bedeutung          |
|------------------------------------------------------------------------------|------------------|
| <dl> <dt>3</dt> </dl> | Maus<br/> |



 

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

Stellt Statusinformationen auf hoher Ebene zur Verfügung. Diese Eigenschaft sollte in Verbindung mit der **DetailedStatus-Eigenschaft** verwendet werden, um einen hohen und detaillierten Integritätsstatus des Elements und seiner Unterkomponenten zu bieten. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**OK** (1)
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Heruntergestuft** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Reservierter Anbieter** (0x8000. )
</dt> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der zuletzt angeforderte oder gewünschte Zustand für das Element. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))



| Wert                                                                         | Bedeutung                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | Nicht zutreffend<br/> |



 

</dd> <dt>

**Auflösung**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Nachverfolgungsauflösung des zeigenden Geräts in Anzahl pro Zoll. Diese Eigenschaft wird von [**CIM \_ PointingDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Status des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt,**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)aber nicht verwendet.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeichenfolgen, die die verschiedenen [**OperationalStatus-Arraywerte**](msvm-bioselement.md) beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) und immer auf "OK" festgelegt.

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Zustand des logischen Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)aber nicht verwendet.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (256)
</dt> </dl>

Der Name der Erstellungsklasse des Bereichssystems. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (256)
</dt> </dl>

Der Name des Bereichssystems. Dieser Wert entspricht dem Wert der [**Name-Eigenschaft**](msvm-computersystem.md) der **Msvm \_ ComputerSystem-Klasse** für den virtuellen Bereichscomputer. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements. Wenn sich der Zustand des Elements nicht geändert hat und diese Eigenschaft aufgefüllt wird, muss sie auf einen Intervallwert von 0 festgelegt werden. Wenn eine Zustandsänderung angefordert, aber abgelehnt oder noch nicht verarbeitet wurde, darf die Eigenschaft nicht aktualisiert werden. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

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

Gibt den Zielzustand an, in den die Instanz übergibt. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt**](/previous-versions//cc136818(v=vs.85))und immer auf NULL **festgelegt.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ Ps2Mouse-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ PointingDevice**](cim-pointingdevice.md)
</dt> <dt>

[**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[Eingabeklassen](input-classes.md)
</dt> </dl>

 

