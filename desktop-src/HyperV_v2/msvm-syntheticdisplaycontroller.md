---
description: Stellt den Status des synthetischen Anzeige Controllers dar, der in jeder Konfiguration der virtuellen Maschine vorhanden ist.
ms.assetid: E496B887-9032-43D8-A7D2-67BB77342AFD
title: Msvm_SyntheticDisplayController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayController
- Msvm_SyntheticDisplayController.SetPowerState
- Msvm_SyntheticDisplayController.EnableDevice
- Msvm_SyntheticDisplayController.OnlineDevice
- Msvm_SyntheticDisplayController.QuiesceDevice
- Msvm_SyntheticDisplayController.SaveProperties
- Msvm_SyntheticDisplayController.RestoreProperties
- Msvm_SyntheticDisplayController.InstanceID
- Msvm_SyntheticDisplayController.Caption
- Msvm_SyntheticDisplayController.Description
- Msvm_SyntheticDisplayController.ElementName
- Msvm_SyntheticDisplayController.InstallDate
- Msvm_SyntheticDisplayController.Name
- Msvm_SyntheticDisplayController.OperationalStatus
- Msvm_SyntheticDisplayController.StatusDescriptions
- Msvm_SyntheticDisplayController.Status
- Msvm_SyntheticDisplayController.HealthState
- Msvm_SyntheticDisplayController.CommunicationStatus
- Msvm_SyntheticDisplayController.DetailedStatus
- Msvm_SyntheticDisplayController.OperatingStatus
- Msvm_SyntheticDisplayController.PrimaryStatus
- Msvm_SyntheticDisplayController.EnabledState
- Msvm_SyntheticDisplayController.OtherEnabledState
- Msvm_SyntheticDisplayController.RequestedState
- Msvm_SyntheticDisplayController.EnabledDefault
- Msvm_SyntheticDisplayController.TimeOfLastStateChange
- Msvm_SyntheticDisplayController.AvailableRequestedStates
- Msvm_SyntheticDisplayController.TransitioningToState
- Msvm_SyntheticDisplayController.SystemCreationClassName
- Msvm_SyntheticDisplayController.SystemName
- Msvm_SyntheticDisplayController.CreationClassName
- Msvm_SyntheticDisplayController.DeviceID
- Msvm_SyntheticDisplayController.PowerManagementSupported
- Msvm_SyntheticDisplayController.PowerManagementCapabilities
- Msvm_SyntheticDisplayController.Availability
- Msvm_SyntheticDisplayController.StatusInfo
- Msvm_SyntheticDisplayController.LastErrorCode
- Msvm_SyntheticDisplayController.ErrorDescription
- Msvm_SyntheticDisplayController.ErrorCleared
- Msvm_SyntheticDisplayController.PowerOnHours
- Msvm_SyntheticDisplayController.TotalPowerOnHours
- Msvm_SyntheticDisplayController.OtherIdentifyingInfo
- Msvm_SyntheticDisplayController.IdentifyingDescriptions
- Msvm_SyntheticDisplayController.AdditionalAvailability
- Msvm_SyntheticDisplayController.MaxQuiesceTime
- Msvm_SyntheticDisplayController.TimeOfLastReset
- Msvm_SyntheticDisplayController.ProtocolSupported
- Msvm_SyntheticDisplayController.MaxNumberControlled
- Msvm_SyntheticDisplayController.ProtocolDescription
- Msvm_SyntheticDisplayController.VideoProcessor
- Msvm_SyntheticDisplayController.VideoMemoryType
- Msvm_SyntheticDisplayController.OtherVideoMemoryType
- Msvm_SyntheticDisplayController.NumberOfVideoPages
- Msvm_SyntheticDisplayController.MaxMemorySupported
- Msvm_SyntheticDisplayController.AcceleratorCapabilities
- Msvm_SyntheticDisplayController.CapabilityDescriptions
- Msvm_SyntheticDisplayController.OtherVideoArchitecture
- Msvm_SyntheticDisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7f566bf2a75b3ed4f503da245d7b6ce428dce5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863559"
---
# <a name="msvm_syntheticdisplaycontroller-class"></a>MSVM \_ syntheticdisplaycontroller-Klasse

Stellt den Status des synthetischen Anzeige Controllers dar, der in jeder Konfiguration der virtuellen Maschine vorhanden ist. Es kann immer nur ein Anzeige Controller auf einem virtuellen Computer aktiv sein, und der synthetische Controller kann nur aktiviert werden, wenn das Gast Betriebssystem die erforderlichen Video Beschleunigungs Dienste geladen hat.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Synthetic Display Controller";
  string   ElementName = "Display Controller";
  datetime InstallDate;
  string   Name = "Display Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_SyntheticDisplayController";
  string   DeviceID = "Microsoft:GUID";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 1024;
  uint32   MaxMemorySupported = 4194304;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a>Member

Die **MSVM \_ syntheticdisplaycontroller** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSVM \_ syntheticdisplaycontroller** -Klasse verfügt über diese Methoden.



| Methode                                                                           | BESCHREIBUNG                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                                 | Diese Methode wird nicht unterstützt.<br/> |
| **Onlinedevice**                                                                 | Diese Methode wird nicht unterstützt.<br/> |
| **Inaktiven Geräte**                                                                | Diese Methode wird nicht unterstützt.<br/> |
| [**RequestStateChange**](msvm-syntheticdisplaycontroller-requeststatechange.md) | Fordert eine Statusänderung an.<br/>      |
| [**Zurücksetzen**](msvm-syntheticdisplaycontroller-reset.md)                           | Setzt das virtuelle Gerät zurück.<br/>    |
| **Restoreproperties**                                                            | Diese Methode wird nicht unterstützt.<br/> |
| **SaveProperties**                                                               | Diese Methode wird nicht unterstützt.<br/> |
| **SetPowerState**                                                                | Diese Methode wird nicht unterstützt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ syntheticdisplaycontroller** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Beschleuniger Funktionen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Grafiken und 3D-Funktionen des Anzeige Controllers. Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf 2 (Grafikbeschleuniger) festgelegt.

</dd> <dt>

**Additionalavailability**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf 6 festgelegt (nicht zutreffend).

</dd> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf 6 festgelegt (nicht zutreffend).

</dd> <dt>

**Availablerequestedstates**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Capabilitybeschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Freiform-Zeichen folgen, die Ausführlichere Erläuterungen zu allen Video-Accelerator-Funktionen bereitstellen, die im **acceleratorfunktionalitäten** -Eigenschafts Array angegeben sind. Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **acceleratorfunktionalitäten** -Eigenschafts Array, das sich im gleichen Index befindet. Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf "Graphics Accelerator" festgelegt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Anzeige Controller" festgelegt.

</dd> <dt>

**Communicationstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000.. )
</dt> </dl>

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "MSVM \_ syntheticdisplaycontroller" festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft Synthetic Display Controller" festgelegt.

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000.. )
</dt> </dl>

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "Microsoft:*GUID*" festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist standardmäßig immer auf "Anzeige Controller" festgelegt.

</dd> <dt>

**Enableddefault**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Status eines Elements. Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) oder 3 (deaktiviert) festgelegt.

</dd> <dt>

**Errorgelöscht**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Zustand des Elements. Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Elemente. Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

**LastErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Maxmemorysupported**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximal unterstützte Arbeitsspeicher Größe in Bytes. Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf 4.194.304 (0x400000) festgelegt.

</dd> <dt>

**Maxnuma**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl direkt Adressier barer Entitäten, die von diesem Controller unterstützt werden. Wenn die Zahl unbekannt oder unbegrenzt ist, sollte der Wert 0 verwendet werden. Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird. Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt und ist immer auf 1 festgelegt.

</dd> <dt>

**Maxquiescetime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Bezeichnung, mit der das-Objekt bekannt ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und entspricht der Element **Name** -Eigenschaft.

</dd> <dt>

**Anzahl der videopages**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der unterstützten Videoseiten anhand der aktuellen Auflösungen und des verfügbaren Arbeitsspeichers. Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf 1024 festgelegt.

</dd> <dt>

**Operatingstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )
</dt> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)
</dt> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)
</dt> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)
</dt> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)
</dt> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)
</dt> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000.. )
</dt> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuellen Status des-Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.

</dd> <dt>

**Otherenabledstate**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist. Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Othervideoarchitecture**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Typ der Video Architektur beschreibt, wenn die **Video Architecture** -Eigenschaft 1 ("Other") ist. Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.

</dd> <dt>

**Othervideomemorytype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ des Video Speichers, wenn die **videomemorytype** -Eigenschaft der Instanz 1 (Other) ist. Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Powermanagementfunktionen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Powermanagementsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Poweronhours**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Primarystatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt Statusinformationen auf hoher Ebene bereit. Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**OK** (1)
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000.. )
</dt> </dl>

</dd> <dt>

**Protocoldescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die weitere Informationen bereitstellt, die mit dem vom Controller unterstützten Protokoll verknüpft sind. Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt und ist immer auf "Video" festgelegt.

</dd> <dt>

**Protocolsupported**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird. Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt und immer auf 1 (sonstige) festgelegt.

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der zuletzt angeforderte oder gewünschte Zustand für das Element. Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt. Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen. **RequestStateChange** kann von einer bestimmten Instanz von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) nicht unterstützt werden. Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet. Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt und auf 2 (aktiviert), 3 (deaktiviert) oder 12 (nicht zutreffend) festgelegt.

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
</dt> </dl>

Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Erstellungs Klasse des Bereichs Systems. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "MSVM \_ Computersystem" festgelegt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem die virtuelle Maschine zuletzt eingeschaltet wurde. Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.

</dd> <dt>

**Timeoflaststatechange**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**Totalpoweronhours**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Transitioningumstate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Ziel Status an, in den die-Instanz übergeht. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Videoarchitecture**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Video Architektur des Anzeige Controllers an, mit der das Videosignal generiert wird. In der Regel generiert ein dedizierter Videoprozessor das Videosignal entsprechend der angegebenen Architektur. Es ist ein Indikator für die maximale Auflösungs Funktion des Anzeige Controllers. Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
</dt> <dt>

<span id="CGA"></span><span id="cga"></span>**CGA** (2)
</dt> <dt>

<span id="EGA"></span><span id="ega"></span>**EGA** (3)
</dt> <dt>

<span id="VGA"></span><span id="vga"></span>**VGA** (4)
</dt> <dt>

<span id="SVGA"></span><span id="svga"></span>**SVGA** (5)
</dt> <dt>

<span id="MDA"></span><span id="mda"></span>**MDA** (6)
</dt> <dt>

<span id="HGC"></span><span id="hgc"></span>**HGC** (7)
</dt> <dt>

<span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)
</dt> <dt>

<span id="8514A"></span><span id="8514a"></span>**8514A** (9)
</dt> <dt>

<span id="XGA"></span><span id="xga"></span>**XGA** (10)
</dt> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linearer Rahmen Puffer** (11)
</dt> <dt>

<span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000.. )
</dt> </dl>

</dd> <dt>

**Videomemorytype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ des Video Speichers. Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf 2 (VRAM) festgelegt.

</dd> <dt>

**Videoprocessor**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Videoprozessor/-Controller beschreibt. Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf "synthetischer Video Prozessor" festgelegt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ syntheticdisplaycontroller** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM- \_ Display Controller**](cim-displaycontroller.md)
</dt> <dt>

[**CIM- \_ Display Controller**](/previous-versions//cc136810(v=vs.85))
</dt> <dt>

[Video Klassen](video-classes.md)
</dt> </dl>

 

