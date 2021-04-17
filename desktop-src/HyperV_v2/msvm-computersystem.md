---
description: Stellt ein physisches Computersystem oder eine virtuelle Maschine dar.
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
ms.openlocfilehash: ae36179e14b584bad4e68350e27d485cdc10c42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554813"
---
# <a name="msvm_computersystem-class"></a>MSVM \_ Computersystem-Klasse

Stellt ein physisches Computersystem oder eine virtuelle Maschine dar.

Verwenden Sie zum Abrufen von Informationen für die VMMS die Klasse [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) .

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **MSVM \_ Computersystem** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSVM \_ Computersystem** -Klasse verfügt über diese Methoden.



| Methode                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Injetnonmaskableinterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md)           | Fügt einen nicht maskierbaren Interrupt in den virtuellen Computer ein. Diese Methode wird nur für Instanzen der **MSVM \_ Computersystem** -Klasse unterstützt, die eine virtuelle Maschine darstellen.<br/> **Windows 8.1:** Diese Methode wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.<br/>                                    |
| [**Requestreplicationstatechange**](msvm-computersystem-requestreplicationstatechange.md)     | Fordert an, dass der Replikations Status der virtuellen Maschine auf den angegebenen Wert geändert wird. Diese Methode wird nur für Instanzen der **MSVM \_ Computersystem** -Klasse unterstützt, die eine virtuelle Maschine darstellen.<br/>                                                                                                        |
| [**Requestreplicationstatechangeex**](msvm-requestreplicationstatechangeex-computersystem.md) | Fordert an, dass der Replikations Status der virtuellen Maschine auf den angegebenen Wert geändert wird. Diese Methode wird nur für Instanzen der **MSVM \_ Computersystem** -Klasse unterstützt, die eine virtuelle Maschine darstellen.<br/> **Windows 8.1:** Diese Methode wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.<br/> |
| [**RequestStateChange**](requeststatechange-msvm-computersystem.md)                           | Fordert an, dass der Zustand des virtuellen Computers geändert wird. Diese Methode wird nur für Instanzen der **MSVM \_ Computersystem** -Klasse unterstützt, die eine virtuelle Maschine darstellen.<br/>                                                                                                                                           |
| **SetPowerState**                                                                              | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ Computersystem** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Availablerequestedstates**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird. Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte, die in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Objekts sind. Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann. Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.

Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (.. )
</dt> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von der [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse geerbt und enthält einen der folgenden Werte.



| Wert                                                                                                | Bedeutung                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>"Virtueller Computer"</dt> </dl>         | Die-Instanz stellt einen virtuellen Computer dar.<br/>    |
| <dl> <dt>"Hosting Computer System"</dt> </dl> | Die-Instanz stellt den hostingcomputer dar.<br/> |



 

</dd> <dt>

**Communicationstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird. Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf "MSVM \_ Computer System" festgelegt.

</dd> <dt>

**Dediziert**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob es sich bei dem Computersystem um ein spezielles System handelt (dediziert für eine bestimmte Verwendung) und ob es sich um ein allgemeines System handelt. Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf 0 (nicht dediziert) festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und enthält einen der folgenden Werte.



| Wert                                                                                                          | Bedeutung                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>"Microsoft Virtual Computer System"</dt> </dl> | Die-Instanz stellt einen virtuellen Computer dar.<br/>    |
| <dl> <dt>"Microsoft Hosting Computer System"</dt> </dl> | Die-Instanz stellt den hostingcomputer dar.<br/> |



 

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

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf den anzeigen amen des Computers für eine virtuelle Maschine oder den NetBIOS-Namen des Verwaltungs Betriebssystems festgelegt.

</dd> <dt>

**Enableddefault**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist einer der folgenden Werte.

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

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Status eines Elements. Diese Eigenschaft kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben. Diese Eigenschaft wird von der [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Klasse geerbt und auf 2 (aktiviert) für einen physischen Computer oder auf einen der folgenden Werte für eine virtuelle Maschine festgelegt. Eine grafische Ansicht dieser Zustände finden Sie unter "Hinweise".



| Wert                                                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannter**</dt> Wert <dt>0</dt> </dl>                                                 | Der Zustand des Elements konnte nicht bestimmt werden.<br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Sonstige**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Aktiviert**</dt> <dt>2</dt> </dl>                                                 | Das-Element wird ausgeführt.<br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deaktiviert**</dt> <dt>3</dt> </dl>                                             | Das Element ist deaktiviert.<br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>4</dt> wird <dt>**heruntergefahren**</dt> </dl>                         | Das Element wird gerade in den deaktivierten Zustand versetzt.<br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Nicht zutreffend**</dt> <dt>5</dt> </dl>                     | Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.<br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Aktiviert, aber offline**</dt> <dt>6</dt> </dl> | Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.<br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**In Test**</dt> <dt>7</dt> </dl>                                                 | Das-Element befindet sich in einem Testzustand.<br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt></dt> Verzögert <dt>8</dt> </dl>                                             | Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.<br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**Inesce**</dt> <dt>9</dt> </dl>                                                 | Das Element ist aktiviert, jedoch in einem eingeschränkten Modus. Das Verhalten des-Elements ähnelt dem aktivierten Status (2), aber es verarbeitet nur einen eingeschränkten Satz von Befehlen. Alle anderen Anforderungen werden in die Warteschlange eingereiht.<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**Start**</dt> <dt>10</dt> </dl>                                            | Das Element wechselt in den Zustand "aktiviert" (2). Neue Anforderungen werden in die Warteschlange eingereiht.<br/>                                                                                                             |



 

</dd> <dt>

**Enhancedsessionmodestate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktuellen Status des erweiterten Sitzungs Modus auf dem virtuellen Computer an.

Der Hyper-V-WMI-Anbieter löst jedes Mal, wenn sich der **enhancedsessionmodestate** der **MSVM \_ Computersystem** -Klasse ändert, ein [**\_ \_ instancemodificationevent-Ereignis**](/windows/desktop/WmiSdk/--instancemodificationevent) aus. Wenn eine aktive vmconnection-Sitzung ein **\_ \_ instancemodificationevent-Ereignis** empfängt, wird versucht, in den erweiterten Sitzungs Modus zu wechseln, wenn der Benutzer diese Einstellung aktiviert hat.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

**Enhancedsessionmodestate** kann einen der folgenden Werte aufweisen:

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Zulässig und verfügbar** (2)


</dt> <dd>

Der erweiterte Modus ist zulässig und auf dem virtuellen Computer verfügbar.

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Nicht zulässig** (3)


</dt> <dd>

Der erweiterte Modus ist auf dem virtuellen Computer nicht zulässig.

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Zulässig, aber nicht verfügbar** (6)


</dt> <dd>

Der erweiterte Modus ist zulässig, aber zurzeit nicht auf dem virtuellen Computer verfügbar.

</dd> </dl>

</dd> <dt>

**Failedoverreplicationtype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).**Failedoverreplicationtype**")
</dt> </dl>

Der Typ des Wiederherstellungsdaten Punkts, der während des Failovervorgangs angewendet wurde.

> [!Note]  
> Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die-Eigenschaft mit demselben Namen in der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, um den Wert für die primäre oder erweiterte Beziehung zu erhalten.

 

Dabei sind folgende Werte möglich:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Regulär** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Anwendungs konsistent** (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Geplant** (3)


</dt> <dd></dd> </dl>

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

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit, zu der die Konfiguration der virtuellen Maschine für eine virtuelle Maschine oder **null** für ein Verwaltungs Betriebssystem erstellt wurde. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

In Windows 8 gibt es für jedes Computersystem oder jeden virtuellen Computer eine einzelne Instanz von [**replicationsettingdata**](msvm-replicationsettingdata.md) . Für Windows 8.1 hat ein virtueller Wiederherstellungs Computer zwei Instanzen von **replicationsettingdata**. Diese Änderung unterscheidet und ordnet Einstellungsdaten der Replikations Beziehung zu.



| Eigenschaftenname  | Windows 8-Wert               | Windows 8.1 Wert                          |
|----------------|-------------------------------|--------------------------------------------|
| **InstanceID** | Microsoft: <vmguid> \\ HVR | Microsoft: <vmguid> \\ HVR \\<0/1> |



 

Im Windows 8.1 Wert gibt 0 den primär Wert und 1 die erweiterte Replikation an. Weitere Informationen zur erweiterten Replikation finden Sie unter [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).

</dd> <dt>

**Lastapplicationkonsistentreplicationtime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).**Lastapplicationkonsistentreplicationtime**")
</dt> </dl>

Der Zeitpunkt, zu dem die letzte Anwendungs konsistente Replikation für den virtuellen Computer empfangen wurde.

> [!Note]  
> Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die-Eigenschaft mit demselben Namen in der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, um den Wert für die primäre oder erweiterte Beziehung zu erhalten.

 

</dd> <dt>

**Lastreplicationtime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).**Lastreplicationtime**")
</dt> </dl>

Der Zeitpunkt, zu dem die letzte Replikation bei der Wiederherstellung für den virtuellen Computer empfangen wird.

> [!Note]  
> Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die-Eigenschaft mit demselben Namen in der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, um den Wert für die primäre oder erweiterte Beziehung zu erhalten.

 

</dd> <dt>

**Lastreplicationtype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).**Lastreplicationtype**")
</dt> </dl>

Der Typ der letzten Replikation, die für den virtuellen Computer empfangen wurde.

> [!Note]  
> Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die-Eigenschaft mit demselben Namen in der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, um den Wert für die primäre oder erweiterte Beziehung zu erhalten.

 

Dabei sind folgende Werte möglich:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Regulär** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Anwendungs konsistent** (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Geplant** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Lasterfolgreicher BackupTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem die letzte erfolgreiche Sicherung für den virtuellen Computer abgeschlossen wurde.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Bezeichnung, mit der das-Objekt bekannt ist. Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf "*GUID*" festgelegt.

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die angibt, wie der Systemname mithilfe der Unterklasse heuristic generiert wurde. Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**NumberOfNumaNodes**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der NUMA-Knoten (nicht einheitlicher Speicherzugriff) des Computer Systems. Wenn **MSVM \_ Computersystem** das hostingcomputersystem darstellt, enthält diese Eigenschaft die Anzahl der physischen NUMA-Knoten. Wenn **MSVM \_ Computersystem** einen virtuellen Computer darstellt, enthält diese Eigenschaft die Anzahl der virtuellen NUMA-Knoten, die dem Gast Betriebssystem über die ACPI-SRAT (System Resource Affinitäts Tabelle) angezeigt werden.

</dd> <dt>

**Ontimeinmilliseconds**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")
</dt> </dl>

Für den virtuellen Computer gibt diese Eigenschaft die Zeit in Millisekunden an, seit der Computer zuletzt eingeschaltet, zurückgesetzt oder wieder hergestellt wurde. Diese Zeit schließt die Zeit aus, zu der sich der virtuelle Computer im angehaltenen Zustand befunden hat. Für das Verwaltungs Betriebssystem wird diese Eigenschaft auf **null** festgelegt.

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

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die beschreibt, wie oder warum das System dediziert ist, wenn das **dedizierte** Array den Wert 2 (Sonstiges) enthält. Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Otherenabledstate**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte oder deaktivierte Status der virtuellen Maschine, wenn die **enabledstate** -Eigenschaft auf 1 (sonstige) festgelegt ist. Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Powermanagementfunktionen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt, aber nicht verwendet.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die angibt, wie der primäre Systembesitzer erreicht werden kann (z. b. eine Telefonnummer oder eine e-Mail-Adresse). Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Primaryownername**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des primären System Besitzers. Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Primarystatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt Statusinformationen auf hoher Ebene bereit. Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Bezeichner des Prozesses, unter dem dieser virtuelle Computer ausgeführt wird. Dieser Wert kann verwendet werden, um die Instanz von Vmwp.exe auf dem System, auf dem der virtuelle Computer ausgeführt wird, eindeutig zu identifizieren.

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")
</dt> </dl>

Die Replikations Integrität für den virtuellen Computer.

> [!Note]  
> Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die-Eigenschaft mit demselben Namen in der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, um den Wert für die primäre oder erweiterte Beziehung zu erhalten.

 

Dabei sind folgende Werte möglich:

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

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Replikations Modus für den virtuellen Computer an. Dabei handelt es sich um einen der folgenden Werte.

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

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Test Replikat** (3)


</dt> <dd>

Replikat

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Erweitertes Replikat** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).**Replicationstate**")
</dt> </dl>

Der Replikations Status für den virtuellen Computer.

> [!Note]  
> Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die-Eigenschaft mit demselben Namen in der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, um den Wert für die primäre oder erweiterte Beziehung zu erhalten.

 

Dabei sind folgende Werte möglich:

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**Bereit für Replikation** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**Warten auf Abschluss der ersten Replikation** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

**Replizieren** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

**Synchronisierungs Replikation beendet** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

**Wieder hergestellt** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

Commit **ausgeführt (6** )


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

Angeh **alten (7** )


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Kritisch** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**Warten auf den Start der erneuten Synchronisierung** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

**Neusynchronisierung** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

**Neusynchronisierung** angehalten (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

**Failover** wird ausgeführt (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

**Failback** wird ausgeführt (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

**Failback ist beendet** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der zuletzt angeforderte oder gewünschte Status für den virtuellen Computer, der an die [**requestStateChange**](requeststatechange-msvm-computersystem.md) -Methode weitergegeben wird, oder 12 (nicht zutreffend), wenn keine Zustandsänderung ausgeführt wird. Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt. Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**Resetcapability**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf 1 (sonstige) festgelegt.

</dd> <dt>

**Rollen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Zeichen folgen, das die Rollen beschreibt, die das System in der Informationstechnologie Umgebung spielt. Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf **null** festgelegt.

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

**Timeoflastconfigurationchange**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der letzten Änderung der Konfigurationsdatei des virtuellen Computers. Die Konfigurationsdatei wird bei bestimmten virtuellen Maschinen Vorgängen geändert, sowie beim Hinzufügen, ändern oder Entfernen von virtuellen Computern oder Geräteeinstellungen.

</dd> <dt>

**Timeoflaststatechange**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**Transitioningumstate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Ziel Status an, in den die-Instanz übergeht. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die folgende Abbildung zeigt die **enabledstate** -Werte.

![Zustandsdiagramm für enabledstate-Werte für Windows Server 2008 R2](images/msvm-computersystem-enabledstate-win2008r2.png)

Wenn sich eine Eigenschaft der **MSVM \_ Computersystem** -Klasse ändert, gibt der WMI-Anbieter ein [**\_ \_ instancemodificationevent**](/windows/desktop/WmiSdk/--instancemodificationevent) -Ereignis an, das die Änderungen beschreibt. Der vorherige Zustand ist in der Eigenschaft **PreviousInstance** enthalten, und der neue Zustand ist in der Eigenschaft **TargetInstance** enthalten. Dieses Ereignis ist asynchron. Wenn das **\_ \_ instancemodificationevent** -Ereignis verarbeitet wird, spiegelt die **TargetInstance** -Eigenschaft möglicherweise nicht den aktuellen Zustand wider.

Der Zugriff auf die **MSVM \_ Computersystem** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Beispiele

Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).

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

[**CIM- \_ Computersystem**](cim-computersystem.md)
</dt> <dt>

[**\_\_Instancemodificationevent**](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[**CIM- \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[**MSVM \_ Computersystem (v1)**](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[Klassen des virtuellen Systems](virtual-system-classes.md)
</dt> </dl>

 

