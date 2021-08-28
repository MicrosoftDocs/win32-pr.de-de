---
description: Dienst zum Erstellen, Anwenden und Zerstören von Momentaufnahmen virtueller Computer.
ms.assetid: 34efe124-d198-4bad-a3c9-e8457a5faa5e
title: Msvm_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService
- Msvm_VirtualSystemSnapshotService.StartService
- Msvm_VirtualSystemSnapshotService.StopService
- Msvm_VirtualSystemSnapshotService.InstanceID
- Msvm_VirtualSystemSnapshotService.Caption
- Msvm_VirtualSystemSnapshotService.Description
- Msvm_VirtualSystemSnapshotService.ElementName
- Msvm_VirtualSystemSnapshotService.InstallDate
- Msvm_VirtualSystemSnapshotService.Name
- Msvm_VirtualSystemSnapshotService.OperationalStatus
- Msvm_VirtualSystemSnapshotService.StatusDescriptions
- Msvm_VirtualSystemSnapshotService.Status
- Msvm_VirtualSystemSnapshotService.HealthState
- Msvm_VirtualSystemSnapshotService.CommunicationStatus
- Msvm_VirtualSystemSnapshotService.DetailedStatus
- Msvm_VirtualSystemSnapshotService.OperatingStatus
- Msvm_VirtualSystemSnapshotService.PrimaryStatus
- Msvm_VirtualSystemSnapshotService.EnabledState
- Msvm_VirtualSystemSnapshotService.OtherEnabledState
- Msvm_VirtualSystemSnapshotService.RequestedState
- Msvm_VirtualSystemSnapshotService.EnabledDefault
- Msvm_VirtualSystemSnapshotService.TimeOfLastStateChange
- Msvm_VirtualSystemSnapshotService.AvailableRequestedStates
- Msvm_VirtualSystemSnapshotService.TransitioningToState
- Msvm_VirtualSystemSnapshotService.SystemCreationClassName
- Msvm_VirtualSystemSnapshotService.SystemName
- Msvm_VirtualSystemSnapshotService.CreationClassName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerContact
- Msvm_VirtualSystemSnapshotService.StartMode
- Msvm_VirtualSystemSnapshotService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c253cf37d2e9cfaf2dd4d5d9f6867dd22736ad8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471056"
---
# <a name="msvm_virtualsystemsnapshotservice-class"></a>Msvm \_ VirtualSystemSnapshotService-Klasse

Dienst zum Erstellen, Anwenden und Zerstören von Momentaufnahmen virtueller Computer.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSnapshotService : CIM_VirtualSystemSnapshotService
{
  string   InstanceID;
  string   Caption = "Hyper-V Virtual System Snapshot Service";
  string   Description = "Service for creating, destroying, and applying virtual machine snapshots";
  string   ElementName;
  datetime InstallDate;
  string   Name = "vssnapsvc";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemSnapshotService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a>Member

Die **Msvm \_ VirtualSystemSnapshotService-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Msvm \_ VirtualSystemSnapshotService-Klasse** verfügt über diese Methoden.




| Methode | BESCHREIBUNG | 
|--------|-------------|
| <a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a> | Wendet eine Momentaufnahme des virtuellen Computers auf den virtuellen Computer an, aus dem er erstellt wurde.<br /> | 
| <a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a> | Löscht den Speicherzustand aus einer vorhandenen Momentaufnahme.<br /> | 
| <a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a> | Konvertieren sie eine vorhandene Momentaufnahme des virtuellen Systems in einen Verweispunkt. Die Momentaufnahme wird als Nebeneffekt gelöscht. Nur Wiederherstellungsmomentaufnahmen können in Verweispunkte konvertiert werden.<br /><blockquote>[!Note]<br />Unterstützung für diese Methode wurde in Windows 10 hinzugefügt.</blockquote><br /> | 
| <a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a> | Erstellt eine Momentaufnahme eines virtuellen Computers.<br /> | 
| <a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a> | Zerstört eine vorhandene Momentaufnahme eines virtuellen Computers. Diese Methode kann als Nebeneffekt andere Momentaufnahmen zerstören, die von der betroffenen Momentaufnahme abhängig sind.<br /> | 
| <a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a> | Entfernt eine vorhandene Momentaufnahme und alle untergeordneten Elemente eines virtuellen Computers.<br /> | 
| <a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a> | Fordert eine Zustandsänderung für das Element an.<br /><blockquote>[!Note]<br />Unterstützung für diese Methode wurde in Windows 10 hinzugefügt.</blockquote><br /> | 
| <strong>Startservice</strong> | Diese Methode wird nicht unterstützt.<br /> | 
| <strong>StopService</strong> | Diese Methode wird nicht unterstützt.<br /> | 




 

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VirtualSystemSnapshotService-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Werte für den *RequestedState-Parameter* der **RequestStateChange-Methode** an, die zum Initiieren einer Zustandsänderung verwendet wird. Die aufgelisteten Werte sind eine Teilmenge der Werte, die in der **RequestedStatesSupported-Eigenschaft** der zugeordneten Instanz von **CIM \_ EnabledLogicalElementCapabilities** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ EnabledLogicalElement-Objekts**](/previous-versions//cc136818(v=vs.85)) sind. Diese Eigenschaft kann ungleich **NULL** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann. Diese Eigenschaft ist **NULL,** wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.

Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt.

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

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Zurückstellen** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Stille** (9)
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

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf "Hyper-V Virtual System Snapshot Service" festgelegt.

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

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel,** **MaxLen** ( 256 )
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und immer auf "Msvm \_ VirtualSystemSnapshotService" festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf "Dienst zum Erstellen, Zerstören und Anwenden von Momentaufnahmen virtueller Computer" festgelegt.

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

Datentyp: **Zeichenfolge**
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

Die Standard- oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt**](/previous-versions//cc136818(v=vs.85))und immer auf 2 (Aktiviert) festgelegt.



| Wert                                                                        | Bedeutung            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | Aktiviert<br/> |



 

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Zustände eines Elements. Sie kann auch die Übergänge zwischen diesen angeforderten Zuzuständen angeben. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt**](/previous-versions//cc136818(v=vs.85))und immer auf 2 (Aktiviert) festgelegt.



| Wert                                                                        | Bedeutung            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | Aktiviert<br/> |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Integrität des Elements. Dieses Attribut drückt die Integrität dieses Elements aus, aber nicht notwendigerweise die Integrität seiner Unterkomponenten. Die möglichen Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist, und 30 bedeutet, dass das Element vollständig nichtfunktional ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)und immer auf 5 (OK) festgelegt.



| Wert                                                                        | Bedeutung                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>5</dt> </dl> | Der Integritätsstatus ist normal.<br/> |



 

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

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **MaxLen** ( 256 )
</dt> </dl>

Die Bezeichnung, unter der das -Objekt bekannt ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)und immer auf "vssnapsvc" festgelegt.

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

Die aktuellen Status des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt,**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)und jedes Arrayelement ist immer auf 2 (OK) festgelegt.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den aktivierten oder deaktivierten Zustand des Elements beschreibt, wenn die **EnabledState-Eigenschaft** auf 1 (Sonstige) festgelegt ist. Diese Eigenschaft muss auf NULL **festgelegt** werden, wenn **EnabledState** ein anderer Wert als 1 ist. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt**](/previous-versions//cc136818(v=vs.85))und immer auf NULL **festgelegt.**

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** ( 256 )
</dt> </dl>

Alle Informationen darüber, wie der primäre Besitzer des Diensts erreicht werden kann (z. B. Telefonnummer, E-Mail-Adresse und so weiter). Diese Eigenschaft wird vom [**\_ CIM-Dienst geerbt**](/windows/desktop/CIMWin32Prov/cim-service)und immer auf **NULL festgelegt.**

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** ( 64 )
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

Der zuletzt angeforderte oder gewünschte Zustand für das Element. Der tatsächliche Zustand des Elements wird durch **EnabledState** dargestellt. Diese Eigenschaft wird bereitgestellt, um den letzten angeforderten und den aktuellen Status für ein Element zu vergleichen. Eine bestimmte Instanz der [**CIM \_ EnabledLogicalElement-Klasse**](/previous-versions//cc136818(v=vs.85)) unterstützt die **RequestedState-Eigenschaft** möglicherweise nicht. In diesem Fall wird der Wert 12 (Nicht zutreffend) verwendet. Diese Eigenschaft wird von **CIM \_ EnabledLogicalElement** geerbt und immer auf 12 (Nicht zutreffend) festgelegt.



| Wert                                                                         | Bedeutung                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | Nicht zutreffend<br/> |



 

</dd> <dt>

**Begann**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Dienst derzeit ausgeführt wird. Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und immer auf **True** festgelegt.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** ( 10 )
</dt> </dl>

Ein Zeichenfolgenwert, der angibt, ob der Dienst automatisch von einem System, einem Betriebssystem oder nur auf Anforderung gestartet wird. Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **String**
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
</dt> </dl>

Zeichenfolgen, die die verschiedenen **OperationalStatus-Arraywerte** beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Arrayelement ist immer auf "Der Dienst wird normal ausgeführt" festgelegt.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel,** **MaxLen** ( 256 )
</dt> </dl>

Der Name der Erstellungsklasse des Bereichssystems. Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und immer auf "Msvm \_ ComputerSystem" festgelegt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel,** **MaxLen** ( 256 )
</dt> </dl>

Der NetBIOS-Name des Hostcomputersystems. Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Zielzustand an, in den die Instanz übergehen soll. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt.



| Wert                                                                                                                                                                                                                                                     | Bedeutung                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0</dt> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Aktiviert**</dt> <dt>2</dt> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deaktiviert**</dt> <dt>3</dt> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <dt>**Herunterfahren**</dt> <dt>4</dt> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <dt>**Keine Änderung**</dt> <dt>5</dt> </dl>                       | Es wird kein Übergang ausgeführt.<br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <dt>**Offline**</dt> <dt>6</dt> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <dt>**Test**</dt> <dt>7</dt> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <dt>**Zurückstellen**</dt> <dt>8</dt> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**Stille**</dt> <dt>9</dt> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <dt>**Neustart**</dt> <dt>10</dt> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <dt>**Zurücksetzen**</dt> <dt>11</dt> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Nicht zutreffend**</dt> <dt>12</dt> </dl>  | Die Implementierung unterstützt keine Darstellung laufender Übergänge.<br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <dt> **DMTF Reserved**</dt> <dt>..</dt> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

