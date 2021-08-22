---
description: Bietet die Möglichkeit, Metriken zu verwalten.
ms.assetid: 39dee432-995d-472a-84c3-eede95dccb43
title: Msvm_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService
- Msvm_MetricService.InstanceID
- Msvm_MetricService.Caption
- Msvm_MetricService.Description
- Msvm_MetricService.ElementName
- Msvm_MetricService.InstallDate
- Msvm_MetricService.OperationalStatus
- Msvm_MetricService.StatusDescriptions
- Msvm_MetricService.Status
- Msvm_MetricService.HealthState
- Msvm_MetricService.CommunicationStatus
- Msvm_MetricService.DetailedStatus
- Msvm_MetricService.OperatingStatus
- Msvm_MetricService.PrimaryStatus
- Msvm_MetricService.EnabledState
- Msvm_MetricService.OtherEnabledState
- Msvm_MetricService.RequestedState
- Msvm_MetricService.EnabledDefault
- Msvm_MetricService.TimeOfLastStateChange
- Msvm_MetricService.AvailableRequestedStates
- Msvm_MetricService.TransitioningToState
- Msvm_MetricService.SystemCreationClassName
- Msvm_MetricService.SystemName
- Msvm_MetricService.Name
- Msvm_MetricService.CreationClassName
- Msvm_MetricService.PrimaryOwnerName
- Msvm_MetricService.PrimaryOwnerContact
- Msvm_MetricService.StartMode
- Msvm_MetricService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 940496e5154732fcec1912c79e4166786c48fba455a50687f508a962e7462b70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148313"
---
# <a name="msvm_metricservice-class"></a>Msvm \_ MetricService-Klasse

Bietet die Möglichkeit, Metriken zu verwalten.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricService : CIM_MetricService
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service";
  string   Description = "Provides Hyper-V Metric WMI management";
  string   ElementName = "Hyper-V Metric Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "metricsvc";
  string   CreationClassName = "Msvm_MetricService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a>Member

Die **Msvm \_ MetricService-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Msvm \_ MetricService-Klasse** verfügt über diese Methoden.



| Methode                                                                    | Beschreibung                                                                             |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**ControlMetrics**](controlmetrics-msvm-metricservice.md)               | Wird verwendet, um die Sammlung von Metriken für ein verwaltetes Element oder ein verwaltetes Element zu steuern.<br/> |
| [**ControlMetricsByClass**](msvm-metricservice-controlmetricsbyclass.md) | Steuert die Metriken nach Klasse.<br/>                                               |
| [**ControlSampleTimes**](msvm-metricservice-controlsampletimes.md)       | Legt die Beispielzeiten des Steuerelements fest.<br/>                                               |
| [**GetMetricValues**](msvm-metricservice-getmetricvalues.md)             | Ruft die Metrikwerte ab.<br/>                                                 |
| [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) | Ändert die Einstellungsdaten für den Dienst.<br/>                                   |
| [**RequestStateChange**](msvm-metricservice-requeststatechange.md)       | Fordert eine Zustandsänderung an.<br/>                                                     |
| [**ShowMetrics**](msvm-metricservice-showmetrics.md)                     | Zeigt die angegebenen Metriken an.<br/>                                                 |
| [**ShowMetricsByClass**](msvm-metricservice-showmetricsbyclass.md)       | Zeigt die Metriken nach Klasse an.<br/>                                                  |
| [**Startservice**](msvm-metricservice-startservice.md)                   | Startet den Dienst.<br/>                                                          |
| [**StopService**](msvm-metricservice-stopservice.md)                     | Beendet den Dienst.<br/>                                                           |



 

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ MetricService-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Werte für den *RequestedState-Parameter* der **RequestStateChange-Methode** an. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf "Hyper-V Metric Service" festgelegt.

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
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und immer auf "Msvm \_ MetricService" festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf "Stellt WMI-Verwaltung von Hyper-V-Metriken bereit".

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ergänzt die **PrimaryStatus-Eigenschaft** um zusätzliche Statusdetails. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Wird** (2)
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht wiederherstellbarer Fehler** (4)
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität im Fehler** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Reservierter Anbieter** (0x8000. )
</dt> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf "Hyper-V Metric Service" festgelegt.

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standard- oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt und immer auf 2 (Aktiviert) festgelegt.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Status eines Elements. Diese Eigenschaft kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt und immer auf 2 (Aktiviert) festgelegt.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Integrität des Elements. Dieses Attribut drückt die Integrität dieses Elements aus, jedoch nicht notwendigerweise die Integrität seiner Unterkomponenten. Die möglichen Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionslos ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und immer auf 5 (OK) festgelegt.

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

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Bezeichnung, mit der das Objekt bekannt ist. Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und immer auf "metricsvc" festgelegt.

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt aktuelle Statusinformationen für die Betriebsbedingung des Elements bereit und kann zum Bereitstellen weiterer Details in Bezug auf den Wert der **EnabledState-Eigenschaft** verwendet werden. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Ab** (3)
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Beenden** (4)
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

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Glückwunschgrating** (10)
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Momentaufnahme** (12)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunterfahren** (13)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)
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

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuellen Status des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Arrayelement ist immer auf 2 (OK) festgelegt.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den aktivierten oder deaktivierten Zustand des Elements beschreibt, wenn die **EnabledState-Eigenschaft** auf 1 (Sonstige) festgelegt ist. Diese Eigenschaft muss auf **NULL** festgelegt werden, wenn **EnabledState** ein anderer Wert als 1 ist. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein -Wert, der Informationen darüber bereitstellt, wie der primäre Besitzer des Diensts erreicht werden kann (z. B. Telefonnummer, E-Mail-Adresse usw.). Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des primären Besitzers für den Dienst, sofern definiert. Der primäre Besitzer ist der erste Supportkontakt für den Dienst. Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt statusinformationen auf hoher Ebene bereit. Diese Eigenschaft sollte in Verbindung mit der **DetailedStatus-Eigenschaft** verwendet werden, um einen hohen und detaillierten Integritätsstatus des Elements und seiner Unterkomponenten bereitzustellen. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

Der zuletzt angeforderte oder gewünschte Zustand für das Element. Der tatsächliche Zustand des Elements wird durch **EnabledState** dargestellt. Diese Eigenschaft wird bereitgestellt, um den zuletzt angeforderten und den aktuellen aktivierten oder deaktivierten Status zu vergleichen. Eine bestimmte Instanz von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) unterstützt die **RequestStateChange-Methode** möglicherweise nicht. In diesem Fall wird der Wert 12 (Nicht zutreffend) verwendet. Diese Eigenschaft wird von **CIM \_ EnabledLogicalElement** geerbt und immer auf 12 (Nicht zutreffend) festgelegt.

</dd> <dt>

**Begann**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Dienst derzeit ausgeführt wird. Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Zeichenfolgenwert, der angibt, ob der Dienst automatisch von einem System, einem Betriebssystem oder nur auf Anforderung gestartet wird. Diese Eigenschaft wird vom [**\_ CIM-Dienst geerbt**](/windows/desktop/CIMWin32Prov/cim-service)und immer auf **NULL festgelegt.**

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)und immer auf "OK" festgelegt.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeichenfolgen, die die verschiedenen **OperationalStatus-Arraywerte** beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt,**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)und die Zeichenfolgen werden immer auf "OK" festgelegt.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Erstellungsklasse des Bereichssystems. Diese Eigenschaft wird vom [**\_ CIM-Dienst geerbt**](/windows/desktop/CIMWin32Prov/cim-service)und immer auf "Msvm \_ ComputerSystem" festgelegt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Hostcomputersystems. Diese Eigenschaft wird vom [**CIM-Dienst \_ geerbt.**](/windows/desktop/CIMWin32Prov/cim-service)

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Zielzustand an, in den die Instanz übergibt. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

