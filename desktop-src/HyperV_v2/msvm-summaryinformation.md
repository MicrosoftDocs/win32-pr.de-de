---
description: Wird in den Methoden GetSummaryInformation und GetDefinitionFileSummaryInformation in der Msvm VirtualSystemManagementService-Klasse verwendet, um schnell allgemeine Informationen zu einem virtuellen Computer oder einer Momentaufnahme \_ abzurufen.
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Msvm_SummaryInformation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1f7cefc27c0e4adc507276d118bcca95c274d121
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886620"
---
# <a name="msvm_summaryinformation-class"></a>Msvm \_ SummaryInformation-Klasse

Wird in den [**Methoden GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) und [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) in der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) verwendet, um schnell allgemeine Informationen zu einem virtuellen Computer oder einer Momentaufnahme abzurufen.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a>Member

Die **Msvm \_ SummaryInformation-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ SummaryInformation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AllocatedGPU**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Bezeichner der physischen Grafikprozessor (GPU), die diesem virtuellen Computer zugeordnet ist. Diese Eigenschaft gilt nur für virtuelle Computer, die RemoteFX.

</dd> <dt>

**ApplicationHealth**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Integritätsstatus der Anwendung für den virtuellen Computer. Diese Eigenschaft ist für Instanzen von **Msvm \_ SummaryInformation** ungültig, die eine Momentaufnahme eines virtuellen Computers darstellen.

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (2)


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

**Anwendungskritisch** (32782)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (32896)


</dt> <dd></dd> </dl>

</dd> <dt>

**AsynchronousTasks**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ConcreteJob-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Ein Array von [**Msvm \_ ConcreteJob-Instanzen,**](msvm-concretejob.md) die alle asynchronen Vorgänge im Zusammenhang mit dem virtuellen Computer darstellen, die gerade ausgeführt werden. Diese Eigenschaft ist für Instanzen von **Msvm \_ SummaryInformation** ungültig, die eine Momentaufnahme eines virtuellen Computers darstellen.

</dd> <dt>

**AvailableMemoryBuffer**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Prozentsatz des verfügbaren Arbeitsspeicherpuffers für den virtuellen Computer. Wenn dynamischer Arbeitsspeicher für einen virtuellen Computer aktiviert ist, stellt diese Eigenschaft das Verhältnis des verfügbaren Arbeitsspeicherpuffers zum idealen Arbeitsspeicherpuffer für den virtuellen Computer dar. Die ideale Arbeitsspeicherpuffergröße wird mithilfe der **TargetMemoryBuffer-Eigenschaft** der [**Msvm \_ MemorySettingData-Klasse**](msvm-memorysettingdata.md) konfiguriert.

Diese Eigenschaft ist nicht gültig für Instanzen der **Msvm \_ SummaryInformation-Klasse,** die virtuelle Computer darstellen, für die dynamischer Arbeitsspeicher nicht aktiviert ist.

Diese Eigenschaft ist für Instanzen der **Msvm \_ SummaryInformation-Klasse** ungültig, die eine Momentaufnahme eines virtuellen Computers darstellen.

</dd> <dt>

**Creationtime**
</dt> <dd> <dl> <dt>

Datentyp: **DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitpunkt, zu dem der virtuelle Computer oder die Momentaufnahme erstellt wurde.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Anzeigename für den virtuellen Computer oder die Momentaufnahme.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Status des virtuellen Computers oder der Momentaufnahme. Mögliche Werte finden Sie in der **EnabledState-Eigenschaft** der [**Msvm \_ ComputerSystem-Klasse.**](msvm-computersystem.md)

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Verbindungen im erweiterten Modus vom Host zugelassen werden und ob sie für den virtuellen Computer verfügbar sind, sofern zulässig.

**Windows 8.1:** Dieser Wert wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**Zulässig und verfügbar** (2)


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**Nicht zulässig** (3)


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**Zulässig, aber nicht verfügbar** (6 )


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestOperatingSystem**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Gastbetriebssystems, falls verfügbar. Wenn diese Informationen nicht verfügbar sind, ist der Wert dieser Eigenschaft **NULL.** Diese Eigenschaft ist für Instanzen von **Msvm \_ SummaryInformation** ungültig, die eine Momentaufnahme eines virtuellen Computers darstellen.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Integritätsstatus für den virtuellen Computer. Diese Eigenschaft ist für Instanzen von **Msvm \_ SummaryInformation** ungültig, die eine Momentaufnahme eines virtuellen Computers darstellen.

</dd> <dt>

**Heartbeat**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Heartbeatstatus für den virtuellen Computer. Weitere Informationen finden Sie in der Dokumentation zur [**StatusDescriptions-Eigenschaft**](msvm-heartbeatcomponent.md) der **Msvm \_ HeartbeatComponent-Klasse.** Diese Eigenschaft ist für Instanzen von **Msvm \_ SummaryInformation** ungültig, die eine Momentaufnahme eines virtuellen Computers darstellen.

<dl> <dt>

<span id="OK"></span><span id="ok"></span>**OK** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (6)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (12)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (13)
</dt> </dl>

</dd> <dt>

**HostComputerSystemName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, der diesen virtuellen Computer hosten soll.

> [!Note]  
> Hinzugefügt in Windows 10.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement.InstanceID"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID ist eine optionale Eigenschaft, die verwendet werden kann, um eine Instanz dieser Klasse innerhalb des Bereichs des instanziierenden Namespace undurchsichtig und eindeutig zu identifizieren. Verschiedene Unterklassen dieser Klasse können diese Eigenschaft überschreiben, um sie erforderlich zu machen, oder einen Schlüssel. Solche Unterklassen können auch die bevorzugten Algorithmen ändern, um die Eindeutigkeit sicherzustellen, die unten definiert sind.

Um die Eindeutigkeit innerhalb des NameSpace sicherzustellen, sollte der Wert von InstanceID mit dem folgenden "bevorzugten" Algorithmus erstellt werden:

&lt;OrgID &gt; : &lt; LocalID&gt;

Dabei sind OrgID und LocalID durch einen Doppelpunkt &lt; &gt; &lt; &gt; (:)) getrennt, und dabei muss &lt; OrgID einen urheberrechtlich geschützten, markengebundenen oder anderweitig eindeutigen Namen &gt; enthalten, der im Besitz der Geschäftseinheit ist, die die InstanceID erstellt oder definiert, oder bei der es sich um eine registrierte ID handelt, die der Geschäftseinheit von einer erkannten globalen Autorität zugewiesen wird. (Diese Anforderung ähnelt der <Schema Name> \_ <Class Name> Struktur von Schemaklassennamen.) Um die Eindeutigkeit sicherzustellen, darf &lt; OrgID &gt; außerdem keinen Doppelpunkt (:). Bei Verwendung dieses Algorithmus muss der erste Doppelpunkt, der in InstanceID angezeigt wird, zwischen &lt; OrgID &gt; und &lt; LocalID angezeigt &gt; werden.

&lt;LocalID wird von der Geschäftsentität ausgewählt und sollte nicht wiederverwendet werden, um verschiedene zugrunde liegende &gt; (reale) Elemente zu identifizieren. Wenn nicht NULL festgelegt ist und der oben genannte "bevorzugte" Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende InstanceID nicht für instanceIDs wiederverwendet wird, die von diesem oder anderen Anbietern für den NameSpace dieser Instanz erzeugt werden.

Wenn der Wert für DMTF-definierte Instanzen nicht auf NULL festgelegt ist, muss der "bevorzugte" Algorithmus mit der OrgID verwendet werden, die &lt; &gt; auf CIM festgelegt ist.

> [!Note]  
> Hinzugefügt in Windows 10.

 

</dd> <dt>

**IntegrationServicesVersionState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die auf dem virtuellen Computer installierten Integrationsdienste auf dem neuesten Stand sind.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

**UpToDate** (1)


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

**Konflikt** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**MemoryAvailable**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Prozentsatz des aktuellen Arbeitsspeichers, der für den virtuellen Computer verfügbar ist. Wenn dynamischer Arbeitsspeicher für einen virtuellen Computer aktiviert ist, stellt diese Eigenschaft das Verhältnis des verfügbaren Arbeitsspeichers des virtuellen Computers zum gesamten physischen Arbeitsspeicher dar, der dem virtuellen Computer zugewiesen ist. Wenn ein virtueller Computer über keinen verfügbaren Arbeitsspeicher verfügt, ist diese Eigenschaft negativ und enthält das Verhältnis des für den virtuellen Computer benötigten Arbeitsspeichers zum gesamten physischen Arbeitsspeicher, der dem virtuellen Computer zugewiesen ist.

Diese Eigenschaft ist nicht gültig für Instanzen der **Msvm \_ SummaryInformation-Klasse,** die virtuelle Computer darstellen, für die dynamischer Arbeitsspeicher nicht aktiviert ist.

Diese Eigenschaft ist für Instanzen der **Msvm \_ SummaryInformation-Klasse** ungültig, die eine Momentaufnahme eines virtuellen Computers darstellen.

</dd> <dt>

**MemorySpansPhysicalNumaNodes**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Arbeitsspeicher eines oder mehrerer virtueller NUMA-Knoten (Nonuniform Memory Access) des virtuellen Computers mehrere physische NUMA-Knoten des hostenden Computersystems umfasst. Enthält **TRUE,** wenn der Arbeitsspeicher mehrere physische NUMA-Knoten umfasst, **andernfalls FALSE.**

</dd> <dt>

**MemoryUsage**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Speicherauslastung des virtuellen Computers in Megabyte. Diese Eigenschaft ist für Instanzen von **Msvm \_ SummaryInformation** ungültig, die eine Momentaufnahme eines virtuellen Computers darstellen.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Name für den virtuellen Computer oder die Momentaufnahme.

</dd> <dt>

**Hinweise**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die dem virtuellen Computer oder der Momentaufnahme zugeordneten Notizen.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtzahl der virtuellen Prozessoren, die dem virtuellen Computer oder der Momentaufnahme zugeordnet sind.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Der aktuelle Betriebsstatus des virtuellen Computers. Mögliche Werte finden Sie in der **OperationalStatus-Eigenschaft** der [**\_ Msvm ComputerSystem-Klasse.**](msvm-computersystem.md)

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den aktivierten oder deaktivierten Zustand des Elements beschreibt, wenn die **EnabledState-Eigenschaft** auf 1 festgelegt ist. Diese Eigenschaft wird auf NULL **festgelegt,** wenn **EnabledState** ein anderer Wert als 1 ist.

</dd> <dt>

**ProcessorLoad**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Prozessorauslastung des virtuellen Computers in Prozent. Diese Eigenschaft ist für Instanzen von **Msvm \_ SummaryInformation** ungültig, die eine Momentaufnahme eines virtuellen Computers darstellen.

</dd> <dt>

**ProcessorLoadHistory**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Ein Array der vorherigen 100 Stichproben der Prozessorauslastung in Prozent für den virtuellen Computer. Diese Eigenschaft ist für Instanzen von **Msvm \_ SummaryInformation** ungültig, die eine Momentaufnahme eines virtuellen Computers darstellen.

</dd> <dt>

**Replicationhealth**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm \_ SummaryInformation**.**ReplicationHealthEx**")
</dt> </dl>

Die Replikationszustand für den virtuellen Computer. Mögliche Werte finden Sie in der **ReplicationHealth-Eigenschaft** der [**Msvm \_ ComputerSystem-Klasse.**](msvm-computersystem.md)

> [!Note]  
> Diese Eigenschaft ist veraltet, beginnend mit Windows 8.1; Verwenden Sie stattdessen **replicationHealthEx.**

 

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

**ReplicationHealthEx**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Das Array von Replikationszustandswerten für die verschiedenen Replikationsbeziehungen des virtuellen Computers. Mögliche Werte finden Sie in der **ReplicationHealth-Eigenschaft** der [**Msvm \_ ReplicationRelationship-Klasse.**](msvm-replicationrelationship.md)

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

Der Replikationstyp für den virtuellen Computer. Mögliche Werte finden Sie in der **ReplicationMode-Eigenschaft** der [**\_ Msvm ComputerSystem-Klasse.**](msvm-computersystem.md)

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (0)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

**Primär** (1)


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

**Replikat** (2)


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

**Testreplikat** (3)


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

**Erweitertes Replikat** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationProviderId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Für den primären oder erweiterten virtuellen Replikatcomputer ist dies die ID des primären Replikationsanbieters. Bei einem virtuellen Replikatcomputer und bei aktivierter erweiterter Replikation ist dies die Anbieter-ID für die erweiterte Beziehung.

**Windows 8.1:** Dieser Wert wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm \_ SummaryInformation**.**ReplicationStateEx**")
</dt> </dl>

Der Replikationsstatus für den virtuellen Computer. Mögliche Werte finden Sie in der **ReplicationState-Eigenschaft** der [**Msvm \_ ComputerSystem-Klasse.**](msvm-computersystem.md)

> [!Note]  
> Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen **ReplicationStateEx.**

 

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

**Synchronisierte Replikation abgeschlossen** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

**Wiederhergestellt** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**Commit** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

**Angehalten** (7)


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

**Erneute Synchronisierung angehalten** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

**Failover wird ausgeführt** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationStateEx**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Das Array von Replikationszustandswerten für die verschiedenen Replikationsbeziehungen des virtuellen Computers. Mögliche Werte finden Sie in der **ReplicationState-Eigenschaft** der [**Msvm \_ ReplicationRelationship-Klasse.**](msvm-replicationrelationship.md)

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Bereit für die Replikation** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Warten auf den Abschluss der ersten Replikation** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replizieren** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synchronisierte Replikation abgeschlossen** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Wiederhergestellt** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Commit** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Angehalten** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Warten auf den Start der erneuten Synchronisierung** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Neusynchronisierung** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Erneute Synchronisierung angehalten** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover wird ausgeführt** (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback wird ausgeführt** (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback abgeschlossen** (14)


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Datenträgerupdate wird ausgeführt** (15)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10 Version 1703 und Windows Server 2016.

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Datenträgerupdate kritisch** (16)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10 Version 1703 und Windows Server 2016.

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (17)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10 Version 1703 und Windows Server 2016.

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Replikation wird neuverwendet** (18)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10 Version 1703 und Windows Server 2016.

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Vorbereitet für die Synchronisierungsreplikation** (19)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10 Version 1703 und Windows Server 2016.

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Vorbereitet für die umgekehrte Gruppenreplikation** (20)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10 Version 1703 und Windows Server 2016.

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in Bearbeitung** (21)


</dt> <dd>

> [!Note]  
> Hinzugefügt in Windows 10 Version 1703 und Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**Geschützt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Abschirmung für den virtuellen Computer konfiguriert ist.

> [!Note]  
> Hinzugefügt in Windows 10 Version 1703 und Windows Server 2016.

 

</dd> <dt>

**Snapshots**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ VirtualSystemSettingData-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Ein Array von [**Msvm \_ VirtualSystemSettingData-Instanzen,**](msvm-virtualsystemsettingdata.md) die die Momentaufnahmen für den virtuellen Computer darstellen. Diese Eigenschaft ist für Instanzen von **Msvm \_ SummaryInformation,** die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Zeichenfolgen, die die entsprechenden **OperationalStatus-Arraywerte** beschreiben. Dies entspricht der **StatusDescriptions-Eigenschaft** der [**Msvm \_ ComputerSystem-Klasse.**](msvm-computersystem.md)

</dd> <dt>

**SwapFilesInUse**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob paging auf zweiter Ebene aktiv ist. Enthält **True,** wenn paging der zweiten Ebene aktiv ist, **andernfalls False.**

</dd> <dt>

**TestReplicaSystem**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine [**CIM \_ ComputerSystem-Instanz,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den virtuellen Testreplikatcomputer für den virtuellen Computer darstellt. Diese Eigenschaft ist für Instanzen von **Msvm \_ SummaryInformation,** die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

</dd> <dt>

**ThumbnailImage**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImageWidth**", "**Msvm \_ SummaryInformation**.**ThumbnailImageHeight**")
</dt> </dl>

Ein Array, das ein kleines Miniaturbild des Desktops für den virtuellen Computer oder eine Momentaufnahme im RGB565-Format enthält.

</dd> <dt>

**ThumbnailImageHeight**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImage**")
</dt> </dl>

Die Höhe des Bilds in pixel in der ThumbnailImage-Eigenschaft.

> [!Note]  
> In Windows 10 hinzugefügt.

 

</dd> <dt>

**ThumbnailImageWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImage**")
</dt> </dl>

Die Breite des Bilds in der ThumbnailImage-Eigenschaft in Pixel.

> [!Note]  
> In Windows 10 hinzugefügt.

 

</dd> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeit seit dem letzten Start des virtuellen Computers. Diese Eigenschaft ist für Instanzen von **Msvm \_ SummaryInformation** ungültig, die eine Momentaufnahme eines virtuellen Computers darstellen.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version des virtuellen Systems im Format "major.minor", z.B. "2.0".

> [!Note]  
> Hinzugefügt in Windows 10.

 

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Zeichenfolgen, die die Benutzerfreundlichen Namen der virtuellen Switches angeben, mit denen der virtuelle Computer verbunden ist.

**Windows 8.1:** Dieser Wert wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Untertyp des virtuellen Systems.

**Windows 8.1:** Dieser Wert wird erst unterstützt, wenn Windows 8.1 und Windows Server 2012 R2.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft:Hyper-V:SubType:1** ()


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft:Hyper-V:SubType:2** ()


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ SummaryInformation-Klasse** kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)
</dt> <dt>

[Virtuelle Systemklassen](virtual-system-classes.md)
</dt> </dl>

 

