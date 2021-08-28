---
description: Stellt ein physisches Computersystem oder einen virtuellen Computer dar.
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Msvm_ComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem
- Msvm_ComputerSystem.SetPowerState
- Msvm_ComputerSystem.InstanceID
- Msvm_ComputerSystem.Caption
- Msvm_ComputerSystem.Description
- Msvm_ComputerSystem.ElementName
- Msvm_ComputerSystem.InstallDate
- Msvm_ComputerSystem.OperationalStatus
- Msvm_ComputerSystem.StatusDescriptions
- Msvm_ComputerSystem.Status
- Msvm_ComputerSystem.HealthState
- Msvm_ComputerSystem.CommunicationStatus
- Msvm_ComputerSystem.DetailedStatus
- Msvm_ComputerSystem.OperatingStatus
- Msvm_ComputerSystem.PrimaryStatus
- Msvm_ComputerSystem.EnabledState
- Msvm_ComputerSystem.OtherEnabledState
- Msvm_ComputerSystem.RequestedState
- Msvm_ComputerSystem.EnabledDefault
- Msvm_ComputerSystem.TimeOfLastStateChange
- Msvm_ComputerSystem.AvailableRequestedStates
- Msvm_ComputerSystem.TransitioningToState
- Msvm_ComputerSystem.CreationClassName
- Msvm_ComputerSystem.Name
- Msvm_ComputerSystem.PrimaryOwnerName
- Msvm_ComputerSystem.PrimaryOwnerContact
- Msvm_ComputerSystem.Roles
- Msvm_ComputerSystem.NameFormat
- Msvm_ComputerSystem.OtherIdentifyingInfo
- Msvm_ComputerSystem.IdentifyingDescriptions
- Msvm_ComputerSystem.Dedicated
- Msvm_ComputerSystem.OtherDedicatedDescriptions
- Msvm_ComputerSystem.ResetCapability
- Msvm_ComputerSystem.PowerManagementCapabilities
- Msvm_ComputerSystem.OnTimeInMilliseconds
- Msvm_ComputerSystem.ProcessID
- Msvm_ComputerSystem.TimeOfLastConfigurationChange
- Msvm_ComputerSystem.NumberOfNumaNodes
- Msvm_ComputerSystem.ReplicationState
- Msvm_ComputerSystem.ReplicationHealth
- Msvm_ComputerSystem.ReplicationMode
- Msvm_ComputerSystem.FailedOverReplicationType
- Msvm_ComputerSystem.LastReplicationType
- Msvm_ComputerSystem.LastApplicationConsistentReplicationTime
- Msvm_ComputerSystem.LastReplicationTime
- Msvm_ComputerSystem.LastSuccessfulBackupTime
- Msvm_ComputerSystem.EnhancedSessionModeState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e35ebd6000dfae5e99c4b589f4c0a62e84f1e1d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880913"
---
# <a name="msvm_computersystem-class"></a>Msvm \_ ComputerSystem-Klasse

Stellt ein physisches Computersystem oder einen virtuellen Computer dar.

Um Informationen für VMMS abzurufen, verwenden Sie die [**Msvm \_ VirtualSystemManagementService-Klasse.**](msvm-virtualsystemmanagementservice.md)

Die folgende Syntax wird Managed Object Format MOF-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ComputerSystem : CIM_ComputerSystem
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
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 1;
  uint16   PowerManagementCapabilities[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
  uint16   NumberOfNumaNodes;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   ReplicationMode;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  DateTime LastApplicationConsistentReplicationTime;
  DateTime LastReplicationTime;
  DateTime LastSuccessfulBackupTime;
  uint16   EnhancedSessionModeState;
};
```

## <a name="members"></a>Member

Die **Msvm \_ ComputerSystem-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Msvm \_ ComputerSystem-Klasse** verfügt über diese Methoden.



| Methode                                                                                         | Beschreibung                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md)           | Fügt einen nicht maskierbaren Interrupt in den virtuellen Computer ein. Diese Methode wird nur für Instanzen der **Msvm \_ ComputerSystem-Klasse** unterstützt, die einen virtuellen Computer darstellen.<br/> **Windows 8.1:** Diese Methode wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.<br/>                                    |
| [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md)     | Fordert an, dass der Replikationsstatus des virtuellen Computers in den angegebenen Wert geändert wird. Diese Methode wird nur für Instanzen der **Msvm \_ ComputerSystem-Klasse** unterstützt, die einen virtuellen Computer darstellen.<br/>                                                                                                        |
| [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) | Fordert an, dass der Replikationsstatus des virtuellen Computers in den angegebenen Wert geändert wird. Diese Methode wird nur für Instanzen der **Msvm \_ ComputerSystem-Klasse** unterstützt, die einen virtuellen Computer darstellen.<br/> **Windows 8.1:** Diese Methode wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.<br/> |
| [**RequestStateChange**](requeststatechange-msvm-computersystem.md)                           | Fordert an, dass der Status des virtuellen Computers geändert wird. Diese Methode wird nur für Instanzen der **Msvm \_ ComputerSystem-Klasse** unterstützt, die einen virtuellen Computer darstellen.<br/>                                                                                                                                           |
| **SetPowerState**                                                                              | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ComputerSystem-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Werte für den *RequestedState-Parameter* der [**RequestStateChange-Methode**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) an, die zum Initiieren einer Zustandsänderung verwendet wird. Die aufgeführten Werte sind eine Teilmenge der Werte, die in der **RequestedStatesSupported-Eigenschaft** der zugeordneten Instanz von **CIM \_ EnabledLogicalElementCapabilities** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ EnabledLogicalElement-Objekts**](/previous-versions//cc136818(v=vs.85)) sind. Diese Eigenschaft kann nicht NULL sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands anknullen kann. Diese Eigenschaft ist **NULL,** wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.

Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunterfahren** (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Zurückern** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Ruhe** (9)
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (.. )
</dt> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von der [**CIM \_ ManagedElement-Klasse geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) und enthält einen der folgenden Werte.



| Wert                                                                                                | Bedeutung                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>"Virtueller Computer"</dt> </dl>         | Die -Instanz stellt einen virtuellen Computer dar.<br/>    |
| <dl> <dt>"Hosten des Computersystems"</dt> </dl> | Die -Instanz stellt den Hostcomputer dar.<br/> |



 

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Diese Eigenschaft wird vom [**\_ CIM-System geerbt**](/windows/desktop/CIMWin32Prov/cim-system)und immer auf "Msvm \_ ComputerSystem" festgelegt.

</dd> <dt>

**Dediziert**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob es sich bei dem Computersystem um ein spezielles System handelt (das für eine bestimmte Verwendung vorgesehen ist) und ob es sich nicht um ein allgemeines System handelt. Diese Eigenschaft wird von [**CIM \_ ComputerSystem geerbt**](/windows/desktop/CIMWin32Prov/cim-computersystem)und immer auf 0 (Nicht de dedicated) festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und enthält einen der folgenden Werte.



| Wert                                                                                                          | Bedeutung                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>"Microsoft Virtual Computer System"</dt> </dl> | Die -Instanz stellt einen virtuellen Computer dar.<br/>    |
| <dl> <dt>"Microsoft Hosting Computer System"</dt> </dl> | Die -Instanz stellt den Hostcomputer dar.<br/> |



 

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ergänzt die **PrimaryStatus-Eigenschaft** durch zusätzliche Statusdetails. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf den Anzeigenamen des Computers für einen virtuellen Computer oder den NetBIOS-Namen des Verwaltungsbetriebssystems festgelegt.

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standard- oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist einer der folgenden Werte.

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Aktiviert, aber offline** (6)
</dt> </dl>

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Status eines Elements. Diese Eigenschaft kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben. Diese Eigenschaft wird von der [**CIM \_ EnabledLogicalElement-Klasse**](/previous-versions//cc136818(v=vs.85)) geerbt und für einen physischen Computer auf 2 (Aktiviert) oder auf einen der folgenden Werte für einen virtuellen Computer festgelegt. Eine grafische Ansicht dieser Zustände finden Sie unter Hinweise.



| Wert                                                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0</dt> </dl>                                                 | Der Zustand des Elements konnte nicht bestimmt werden.<br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Andere**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Aktiviert**</dt> <dt>2</dt> </dl>                                                 | Das Element wird ausgeführt.<br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deaktiviert**</dt> <dt>3</dt> </dl>                                             | Das Element ist deaktiviert.<br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Herunterfahren**</dt> <dt>4</dt> </dl>                         | Das Element befindet sich im Zustand Deaktiviert.<br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Nicht zutreffend**</dt> <dt>5</dt> </dl>                     | Das -Element unterstützt nicht das Aktivieren oder Deaktivieren.<br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Aktiviert, aber offline**</dt> <dt>6</dt> </dl> | Das -Element kann Befehle abschließen und alle neuen Anforderungen löschen.<br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**In Test**</dt> <dt>7</dt> </dl>                                                 | Das Element befindet sich in einem Testzustand.<br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt>**Verzögert 8**</dt> <dt></dt> </dl>                                             | Das Element schließt möglicherweise Befehle ab, stellt jedoch alle neuen Anforderungen in die Warteschlange.<br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**Stille**</dt> <dt>9</dt> </dl>                                                 | Das Element ist aktiviert, befindet sich jedoch im eingeschränkten Modus. Das Verhalten des Elements ähnelt dem Zustand Aktiviert (2), verarbeitet aber nur einen eingeschränkten Satz von Befehlen. Alle anderen Anforderungen werden in die Warteschlange eingereiht.<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**Ab**</dt> <dt>10</dt> </dl>                                            | Das Element befindet sich im Zustand Aktiviert (2). Neue Anforderungen werden in die Warteschlange eingereiht.<br/>                                                                                                             |



 

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktuellen Zustand des erweiterten Sitzungsmodus auf dem virtuellen Computer an.

Der Hyper-V-WMI-Anbieter löst jedes Mal ein [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) aus, wenn sich **der EnhancedSessionModeState** der **Msvm \_ ComputerSystem-Klasse** ändert. Wenn eine aktive vmconnection-Sitzung ein **\_ \_ InstanceModificationEvent** empfängt, wird versucht, in den erweiterten Sitzungsmodus zu wechseln, wenn der Benutzer diese Einstellung aktiviert hat.

**Windows 8.1:** Dieser Wert wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.

**EnhancedSessionModeState** kann einer der folgenden Werte sein:

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Zulässig und verfügbar** (2)


</dt> <dd>

Der erweiterte Modus ist auf dem virtuellen Computer zulässig und verfügbar.

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Nicht zulässig** (3)


</dt> <dd>

Der erweiterte Modus ist auf dem virtuellen Computer nicht zulässig.

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Zulässig, aber nicht verfügbar** (6)


</dt> <dd>

Der erweiterte Modus ist zulässig und derzeit auf dem virtuellen Computer nicht verfügbar.

</dd> </dl>

</dd> <dt>

**FailedOverReplicationType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")
</dt> </dl>

Der Typ des Wiederherstellungsdatenpunkts, der während des Failovervorgangs angewendet wurde.

> [!Note]  
> Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die -Eigenschaft mit dem gleichen Namen in der [**Msvm \_ ReplicationRelationship-Klasse,**](msvm-replicationrelationship.md) um den Wert für die primäre oder erweiterte Beziehung abzurufen.

 

Mögliche Werte:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**None** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normal** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Anwendungskonsens** (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Geplant** (3)


</dt> <dd></dd> </dl>

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
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>5</dt> </dl>                                                                               | Der virtuelle Computer ist voll funktionsfähig und arbeitet innerhalb normaler Betriebsparameter und ohne Fehler.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Hauptfehler**</dt> <dt>20</dt> </dl>             | Auf dem virtuellen Computer ist ein schwerwiegender Fehler aufgetreten. Dieser Wert wird verwendet, wenn mindestens ein Datenträger, der die VHDs des virtuellen Computers enthält, wenig Speicherplatz auf dem Datenträger hat und der virtuelle Computer angehalten wurde.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Kritischer Fehler**</dt> <dt>25</dt> </dl> | Das Element ist nicht funktionstmöglich, und eine Wiederherstellung ist möglicherweise nicht möglich. Dies kann darauf hinweisen, dass der Arbeitsprozess für den virtuellen Computer (Vmwp.exe) nicht auf Steuerungs- oder Informationsanforderungen reagiert oder dass mindestens ein Datenträger, der die VHDs für den virtuellen Computer enthält, wenig Speicherplatz auf dem Datenträger hat.<br/> |



 

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit, zu der die Konfiguration des virtuellen Computers für einen virtuellen Computer erstellt wurde, oder **NULL** für ein Verwaltungsbetriebssystem. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

In Windows 8 gibt es eine einzelne Instanz von [**ReplicationSettingData**](msvm-replicationsettingdata.md) für jedes Computersystem oder jeden virtuellen Computer. Für Windows 8.1 verfügt ein virtueller Wiederherstellungscomputer über zwei Instanzen von **ReplicationSettingData.** Diese Änderung unterscheidet und ordnet Einstellungsdaten der Replikationsbeziehung zu.



| Eigenschaftenname  | Windows 8 Wert               | Windows 8.1 Wert                          |
|----------------|-------------------------------|--------------------------------------------|
| **InstanceID** | Microsoft: &lt; vmguid &gt; \\ HVR | Microsoft: &lt; vmguid &gt; \\ HVR \\<0/1> |



 

Im Windows 8.1 Wert steht 0 für primär und 1 für erweiterte Replikation. Weitere Informationen zur erweiterten Replikation finden Sie unter [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).

</dd> <dt>

**LastApplicationConsistentReplicationTime**
</dt> <dd> <dl> <dt>

Datentyp: **DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")
</dt> </dl>

Der Zeitpunkt, zu dem die letzte anwendungskonsente Replikation für den virtuellen Computer empfangen wurde.

> [!Note]  
> Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die -Eigenschaft mit dem gleichen Namen in der [**Msvm \_ ReplicationRelationship-Klasse,**](msvm-replicationrelationship.md) um den Wert für die primäre oder erweiterte Beziehung abzurufen.

 

</dd> <dt>

**LastReplicationTime**
</dt> <dd> <dl> <dt>

Datentyp: **DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")
</dt> </dl>

Der Zeitpunkt, zu dem die letzte Replikation bei der Wiederherstellung für den virtuellen Computer empfangen wird.

> [!Note]  
> Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die -Eigenschaft mit dem gleichen Namen in der [**Msvm \_ ReplicationRelationship-Klasse,**](msvm-replicationrelationship.md) um den Wert für die primäre oder erweiterte Beziehung abzurufen.

 

</dd> <dt>

**LastReplicationType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")
</dt> </dl>

Der Typ der letzten Replikation, die für den virtuellen Computer empfangen wurde.

> [!Note]  
> Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die -Eigenschaft mit dem gleichen Namen in der [**Msvm \_ ReplicationRelationship-Klasse,**](msvm-replicationrelationship.md) um den Wert für die primäre oder erweiterte Beziehung abzurufen.

 

Mögliche Werte:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**None** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normal** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Anwendungskonsens** (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Geplant** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastSuccessfulBackupTime**
</dt> <dd> <dl> <dt>

Datentyp: **DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem die letzte erfolgreiche Sicherung für den virtuellen Computer abgeschlossen wurde.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Bezeichnung, mit der das Objekt bekannt ist. Diese Eigenschaft wird vom [**\_ CIM-System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und immer auf *"GUID"* festgelegt.

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die mithilfe der Unterklassenhuristik angibt, wie der Systemname generiert wurde. Diese Eigenschaft wird von [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**NumberOfNumaNodes**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der NUMA-Knoten (Nonuniform Memory Access) des Computersystems. Wenn **Msvm \_ ComputerSystem** das Hostcomputersystem darstellt, enthält diese Eigenschaft die Anzahl der physischen NUMA-Knoten. Wenn **Msvm \_ ComputerSystem** einen virtuellen Computer darstellt, enthält diese Eigenschaft die Anzahl der virtuellen NUMA-Knoten, die dem Gastbetriebssystem über die ACPI-Systemressourcenaffinitätstabelle (SRAT) angezeigt werden.

</dd> <dt>

**OnTimeInMilliseconds**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")
</dt> </dl>

Für den virtuellen Computer gibt diese Eigenschaft die Zeit in Millisekunden an, seit der Computer zuletzt eingeschaltet, zurückgesetzt oder wiederhergestellt wurde. Dieses Mal schließt die Zeit aus, zu der sich der virtuelle Computer im angehaltenen Zustand befand. Für das Verwaltungsbetriebssystem wird diese Eigenschaft auf **NULL** festgelegt.

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



 

Der Wert am Index 1 ist optional und enthält sekundäre Statusinformationen. Ein Client sollte den primären Status von Index null (0) verwenden, um zu bestimmen, ob eine neue Anforderung an den virtuellen Computer ausgegeben werden kann. Wenn **OperationalStatus** \[ 0 \] 2 (OK) ist, kann der von **OperationalStatus** 1 angegebene Vorgang unterbrochen \[ \] werden.

Der Wert bei **OperationalStatus** \[ 1 \] ist einer der folgenden Werte.



| Wert                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Erstellen der Momentaufnahme**</dt> <dt>32768</dt> </dl>                                 | Eine Momentaufnahme wird gerade für den virtuellen Computer erstellt.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Anwenden von Momentaufnahme**</dt> <dt>32769</dt> </dl>                                 | Eine Momentaufnahme wird gerade auf den virtuellen Computer angewendet.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Löschen von Momentaufnahme**</dt> <dt>32770</dt> </dl>                                 | Eine Momentaufnahme wird gerade vom virtuellen Computer gelöscht.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**Warten auf Start**</dt> <dt>32771</dt> </dl>                                     | Der virtuelle Computer wird gestartet, nachdem die automatische Startverzögerung verstrichen ist.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Zusammenführen von Datenträgern**</dt> <dt>32772</dt> </dl>                                                 | Virtuelle Festplatten aus zuvor gelöschten Momentaufnahmen werden zusammengeführt.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Exportieren des virtuellen Computers**</dt> <dt>32773</dt> </dl> | Der virtuelle Computer wird exportiert.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Migrieren des virtuellen Computers**</dt> <dt>32774</dt> </dl> | Der virtuelle Computer wird live von einem physischen Computer zu einem anderen migriert.<br/>  |



 

</dd> <dt>

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die beschreibt, wie oder warum das System de dedicated ist, wenn das **Dedicated-Array** den Wert 2 (Other) enthält. Diese Eigenschaft wird von [**CIM \_ ComputerSystem geerbt**](/windows/desktop/CIMWin32Prov/cim-computersystem)und immer auf **NULL festgelegt.**

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte oder deaktivierte Zustand des virtuellen Computers, wenn die **EnabledState-Eigenschaft** auf 1 (Sonstige) festgelegt ist. Diese Eigenschaft muss auf NULL **festgelegt** werden, wenn **EnabledState** ein anderer Wert als 1 ist. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt**](/previous-versions//cc136818(v=vs.85))und immer auf NULL **festgelegt.**

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ComputerSystem geerbt**](/windows/desktop/CIMWin32Prov/cim-computersystem)und immer auf **NULL festgelegt.**

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ComputerSystem geerbt,**](/windows/desktop/CIMWin32Prov/cim-computersystem)aber nicht verwendet.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die angibt, wie der primäre Systembesitzer erreicht werden kann (z. B. eine Telefonnummer oder eine E-Mail-Adresse). Diese Eigenschaft wird vom [**\_ CIM-System geerbt**](/windows/desktop/CIMWin32Prov/cim-system)und immer auf **NULL festgelegt.**

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des primären Systembesitzers. Diese Eigenschaft wird vom [**\_ CIM-System geerbt**](/windows/desktop/CIMWin32Prov/cim-system)und immer auf **NULL festgelegt.**

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt Statusinformationen auf hoher Ebene zur Verfügung. Diese Eigenschaft sollte in Verbindung mit der **DetailedStatus-Eigenschaft** verwendet werden, um detaillierte Informationen zum Integritätsstatus für das Element und seine Unterkomponenten zu erhalten. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Bezeichner des Prozesses, unter dem dieser virtuelle Computer ausgeführt wird. Dieser Wert kann verwendet werden, um die Instanz von Vmwp.exe auf dem System, auf dem der virtuelle Computer ausgeführt wird, eindeutig zu identifizieren.

</dd> <dt>

**Replicationhealth**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")
</dt> </dl>

Die Replikationszustand für den virtuellen Computer.

> [!Note]  
> Diese Eigenschaft ist veraltet, beginnend mit Windows 8.1; Verwenden Sie stattdessen die -Eigenschaft mit demselben Namen in der [**Msvm \_ ReplicationRelationship-Klasse,**](msvm-replicationrelationship.md) um den Wert für die primäre oder erweiterte Beziehung zu erhalten.

 

Mögliche Werte:

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Nicht zutreffend** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**OK** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Warnung** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Kritisch** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Replikationsmodus für den virtuellen Computer an. Dies ist einer der folgenden Werte.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Keine** (0)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primär** (1)


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Replikat** (2)


</dt> <dd>

Wiederherstellung

</dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Testreplikat** (3)


</dt> <dd>

Replikat

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Erweitertes Replikat** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")
</dt> </dl>

Der Replikationsstatus für den virtuellen Computer.

> [!Note]  
> Diese Eigenschaft ist veraltet, beginnend mit Windows 8.1; Verwenden Sie stattdessen die -Eigenschaft mit demselben Namen in der [**Msvm \_ ReplicationRelationship-Klasse,**](msvm-replicationrelationship.md) um den Wert für die primäre oder erweiterte Beziehung zu erhalten.

 

Mögliche Werte:

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**Bereit für die Replikation** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**Warten auf den Abschluss der ersten Replikation** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

**Replizieren** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

**Abgeschlossene synchronisierte Replikation** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

**Wiederhergestellt** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**Committed** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

**Angehalten** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Kritisch** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**Warten auf den Start der Neusynchronisierung** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

**Erneute Synchronisierung** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

**Erneute Synchronisierung angehalten** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

**Failover wird ausgeführt** (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

**Failback in Bearbeitung** (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

**Failback abgeschlossen** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der letzte angeforderte oder gewünschte Zustand für den virtuellen Computer, der an die [**RequestStateChange-Methode**](requeststatechange-msvm-computersystem.md) übergeben wird, oder 12 (Nicht zutreffend), wenn keine Zustandsänderung ausgeführt wird. Der tatsächliche Zustand des Elements wird durch **EnabledState dargestellt.** Diese Eigenschaft wird bereitgestellt, um den zuletzt angeforderten und den aktuell aktivierten oder deaktivierten Zustand zu vergleichen. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ComputerSystem geerbt**](/windows/desktop/CIMWin32Prov/cim-computersystem)und immer auf 1 (Sonstige) festgelegt.

</dd> <dt>

**Rollen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichenfolgen, die die Rollen beschreiben, die das System in der Informationstechnologieumgebung spielt. Diese Eigenschaft wird vom [**\_ CIM-System geerbt**](/windows/desktop/CIMWin32Prov/cim-system)und immer auf **NULL festgelegt.**

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt,**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)aber nicht verwendet.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **ArrayType** ("Indexed")
</dt> </dl>

Ein Array, das Zeichenfolgen enthält, die die entsprechenden **OperationalStatus-Arraywerte** beschreiben. Wenn z. B. 11 (In Service) der Wert ist, der **OperationalStatus** 0 zugewiesen ist, enthält \[ \] **StatusDescriptions** 0 möglicherweise eine Erklärung dazu, warum der virtuelle Computer eine Anforderung \[ \] verarbeitet. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**TimeOfLastConfigurationChange**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der letzten Änderung der Konfigurationsdatei des virtuellen Computers. Die Konfigurationsdatei wird bei bestimmten Vorgängen virtueller Computer sowie beim Hinzugefügt, Ändern oder Entfernen der Einstellungen des virtuellen Computers oder Geräts geändert.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

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

Die folgende Abbildung zeigt die **EnabledState-Werte.**

![Statusdiagramm für enabledstate-Werte für Windows Server 2008 r2](images/msvm-computersystem-enabledstate-win2008r2.png)

Wenn sich eine Eigenschaft der **Msvm \_ ComputerSystem-Klasse** ändert, gibt der WMI-Anbieter ein [**\_ \_ InstanceModificationEvent-Ereignis**](/windows/desktop/WmiSdk/--instancemodificationevent) an, das die Änderungen beschreibt. Der vorherige Zustand ist in der **PreviousInstance-Eigenschaft** enthalten, und der neue Zustand ist in der **TargetInstance-Eigenschaft** enthalten. Dieses Ereignis ist asynchron. Wenn das **\_ \_ InstanceModificationEvent-Ereignis** verarbeitet wird, spiegelt die **TargetInstance-Eigenschaft** möglicherweise nicht den aktuellen Zustand wider.

Der Zugriff auf die **Msvm \_ ComputerSystem-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Beispiele

Weitere Informationen [finden Sie unter Abfragen von Netzwerkobjekten.](querying-networking-objects.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-ComputerSystem**](cim-computersystem.md)
</dt> <dt>

[**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[**\_CIM-ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[**Msvm \_ ComputerSystem (V1)**](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[Virtuelle Systemklassen](virtual-system-classes.md)
</dt> </dl>

 

