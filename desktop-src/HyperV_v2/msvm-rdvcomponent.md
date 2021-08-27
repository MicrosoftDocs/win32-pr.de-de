---
description: Stellt den Zustand der RDV-Komponente dar, die für die Bereitstellung eines Transports für das übergeordnete Element zum Gast zu Konfigurationszwecken verantwortlich ist.
ms.assetid: 240d2659-01ec-4300-a17e-0b1ec90483df
title: Msvm_RdvComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent
- Msvm_RdvComponent.RequestStateChange
- Msvm_RdvComponent.SetPowerState
- Msvm_RdvComponent.Reset
- Msvm_RdvComponent.EnableDevice
- Msvm_RdvComponent.OnlineDevice
- Msvm_RdvComponent.QuiesceDevice
- Msvm_RdvComponent.SaveProperties
- Msvm_RdvComponent.RestoreProperties
- Msvm_RdvComponent.InstanceID
- Msvm_RdvComponent.Caption
- Msvm_RdvComponent.Description
- Msvm_RdvComponent.ElementName
- Msvm_RdvComponent.InstallDate
- Msvm_RdvComponent.Name
- Msvm_RdvComponent.OperationalStatus
- Msvm_RdvComponent.StatusDescriptions
- Msvm_RdvComponent.Status
- Msvm_RdvComponent.HealthState
- Msvm_RdvComponent.CommunicationStatus
- Msvm_RdvComponent.DetailedStatus
- Msvm_RdvComponent.OperatingStatus
- Msvm_RdvComponent.PrimaryStatus
- Msvm_RdvComponent.EnabledState
- Msvm_RdvComponent.OtherEnabledState
- Msvm_RdvComponent.RequestedState
- Msvm_RdvComponent.EnabledDefault
- Msvm_RdvComponent.TimeOfLastStateChange
- Msvm_RdvComponent.AvailableRequestedStates
- Msvm_RdvComponent.TransitioningToState
- Msvm_RdvComponent.SystemCreationClassName
- Msvm_RdvComponent.SystemName
- Msvm_RdvComponent.CreationClassName
- Msvm_RdvComponent.DeviceID
- Msvm_RdvComponent.PowerManagementSupported
- Msvm_RdvComponent.PowerManagementCapabilities
- Msvm_RdvComponent.Availability
- Msvm_RdvComponent.StatusInfo
- Msvm_RdvComponent.LastErrorCode
- Msvm_RdvComponent.ErrorDescription
- Msvm_RdvComponent.ErrorCleared
- Msvm_RdvComponent.OtherIdentifyingInfo
- Msvm_RdvComponent.PowerOnHours
- Msvm_RdvComponent.TotalPowerOnHours
- Msvm_RdvComponent.IdentifyingDescriptions
- Msvm_RdvComponent.AdditionalAvailability
- Msvm_RdvComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0123ac9112950d074df48386d061f0bfa6f0ba05232fc34892cc52689ba2d7c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046440"
---
# <a name="msvm_rdvcomponent-class"></a>Msvm \_ RdvComponent-Klasse

Stellt den Zustand der RDV-Komponente dar, die für die Bereitstellung eines Transports für das übergeordnete Element zum Gast zu Konfigurationszwecken verantwortlich ist.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "RDV";
  string   Description = "Remote Desktop Virtualization Service";
  string   ElementName = "RDV";
  datetime InstallDate;
  string   Name = "RDV";
  uint16   OperationalStatus[] = {2};
  string   StatusDescriptions[] = {"OK"};
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_RdvComponent";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a>Member

Die **Msvm \_ RdvComponent-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Msvm \_ RdvComponent-Klasse** verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                                                                                                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EnableDevice**                                             | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                            |
| [**EnableEndPoints**](enableendpoints-msvm-rdvcomponent.md) | Fordert die Remotedesktopdienste virtuellen Geräts an, eine Pipeverbindung mit dem virtuellen Computer zu starten. Wenn 0 (null) zurückgegeben wird, war der Vorgang erfolgreich. Jeder andere Rückgabecode gibt einen Fehlerzustand an.<br/> |
| **OnlineDevice**                                             | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                            |
| **QuiesceDevice**                                            | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                            |
| **RequestStateChange**                                       | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                            |
| **Zurücksetzen**                                                    | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                            |
| **RestoreProperties**                                        | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                            |
| **SaveProperties**                                           | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                            |
| **SetPowerState**                                            | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                            |



 

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ RdvComponent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Alle zusätzlichen Verfügbarkeiten und Status des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)aber nicht verwendet.

</dd> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die primäre Verfügbarkeit und der Status des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)aber nicht verwendet.

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Werte für den *RequestedState-Parameter* der **RequestStateChange-Methode** an. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt**](/previous-versions//cc136818(v=vs.85))und immer auf NULL **festgelegt.**

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

Der Name der Erstellungsklasse des Bereichssystems. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

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
</dt> </dl>

Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standard- oder Startkonfiguration eines Administrators für die **EnabledState-Eigenschaft** eines Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Zustände eines Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt**](/previous-versions//cc136818(v=vs.85))und ist einer der folgenden Werte.



| Wert                                                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0</dt> </dl>                                                 | Der Zustand des Elements konnte nicht bestimmt werden.<br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Andere**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Aktiviert**</dt> <dt>2</dt> </dl>                                                 | Das -Element wird ausgeführt.<br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deaktiviert**</dt> <dt>3</dt> </dl>                                             | Das -Element ist deaktiviert.<br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Herunterfahren von**</dt> <dt>4</dt> </dl>                         | Das -Element befindet sich im Zustand Deaktiviert.<br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Nicht zutreffend**</dt> <dt>5</dt> </dl>                     | Das -Element unterstützt nicht das Aktivieren oder Deaktivieren.<br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Aktiviert, aber offline**</dt> <dt>6</dt> </dl> | Das -Element kann Befehle abschließen und alle neuen Anforderungen ablegen.<br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**In Test**</dt> <dt>7</dt> </dl>                                                 | Das Element befindet sich in einem Testzustand.<br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt>**Zurückgestellt**</dt> <dt>8</dt> </dl>                                             | Das -Element kann Befehle abschließen, aber es werden alle neuen Anforderungen in die Warteschlange gestellt.<br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**Ruhe 9**</dt> <dt></dt> </dl>                                                 | Das -Element ist aktiviert, befindet sich jedoch im eingeschränkten Modus. Das Verhalten des Elements ähnelt dem Status Aktiviert (2), verarbeitet jedoch nur einen eingeschränkten Satz von Befehlen. Alle anderen Anforderungen werden in die Warteschlange gestellt.<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**Ab**</dt> <dt>10</dt> </dl>                                            | Das Element befindet sich im Zustand Aktiviert (2). Neue Anforderungen werden in die Warteschlange gestellt.<br/>                                                                                                             |



 

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

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Integrität des Elements. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Freiformzeichenfolgen, die Erklärungen und Details hinter den Einträgen im **OtherIdentifyingInfo-Eigenschaftenarray** bereitstellen. Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)aber nicht verwendet.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Installation des Objekts. Diese Eigenschaft benötigt keinen Wert, um anzugeben, dass das Objekt installiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

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

Die Bezeichnung, unter der das -Objekt bekannt ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

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

Die aktuellen Status des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den aktivierten oder deaktivierten Zustand des Elements beschreibt, wenn die **EnabledState-Eigenschaft** auf 1 (Sonstige) festgelegt ist. Diese Eigenschaft muss auf **NULL** festgelegt werden, wenn die **EnabledState-Eigenschaft** ein anderer Wert als 1 ist. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Alle zusätzlichen Daten, die über geräte-ID-Informationen hinausgehen und zum Identifizieren eines logischen Geräts verwendet werden können. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

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

Der zuletzt angeforderte oder gewünschte Zustand für das Element. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt und immer auf 12 (Nicht zutreffend) festgelegt.

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

Der Name des Bereichssystems. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt und immer auf **NULL** festgelegt.

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

Gibt den Zielzustand an, in den die Instanz übergehen soll. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt und immer auf **NULL** festgelegt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

