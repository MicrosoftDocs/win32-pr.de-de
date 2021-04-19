---
description: Wird in der getsummaryinformation-Methode und der GetDefinitionFileSummaryInformation-Methode in der MSVM \_ virtualsystemmanagementservice-Klasse verwendet, um schnell allgemeine Informationen zu einem virtuellen Computer oder einer Momentaufnahme abzurufen.
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
ms.openlocfilehash: 817d025551ae10002b008a181edd8a7dfd2ec68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348436"
---
# <a name="msvm_summaryinformation-class"></a>MSVM \_ SummaryInformation-Klasse

Wird in der [**getsummaryinformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) -Methode und der [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) -Methode in der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse verwendet, um schnell allgemeine Informationen zu einem virtuellen Computer oder einer Momentaufnahme abzurufen.

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

Die **MSVM \_ SummaryInformation** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ SummaryInformation** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Zugedgpu**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Bezeichner der physischen Grafikverarbeitungseinheit (GPU), die dieser virtuellen Maschine zugeordnet ist. Diese Eigenschaft gilt nur für virtuelle Maschinen, die remotefx verwenden.

</dd> <dt>

**Applicationhealth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Integritäts Status der Anwendung für die virtuelle Maschine. Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (2)


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

**Anwendungs kritisch** (32782)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (32896)


</dt> <dd></dd> </dl>

</dd> <dt>

**Asynchronoustasks**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ concretejob** -Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Ein Array von [**MSVM-" \_ concretejob**](msvm-concretejob.md) "-Instanzen, die alle asynchronen Vorgänge im Zusammenhang mit dem derzeit ausgeführten virtuellen Computer darstellen. Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

</dd> <dt>

**Availablememorybuffer**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Prozentsatz des verfügbaren Arbeitsspeicher Puffers für die virtuelle Maschine. Wenn dynamischer Arbeitsspeicher für eine virtuelle Maschine aktiviert ist, stellt diese Eigenschaft das Verhältnis des verfügbaren Arbeitsspeicher Puffers zum idealen Speicherpuffer für den virtuellen Computer dar. Die ideale Größe des Arbeitsspeicher Puffers wird mit der **targetmemorybuffer** -Eigenschaft der [**MSVM \_ memorysettingdata**](msvm-memorysettingdata.md) -Klasse konfiguriert.

Diese Eigenschaft ist für Instanzen der **MSVM-Klasse " \_ SummaryInformation** " ungültig, die virtuelle Computer darstellt, für die der dynamische Arbeitsspeicher nicht aktiviert ist.

Diese Eigenschaft ist für Instanzen der **MSVM \_ SummaryInformation** -Klasse, die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
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

Der Anzeige Name für den virtuellen Computer oder die Momentaufnahme.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Zustand des virtuellen Computers oder der Momentaufnahme. Mögliche Werte finden Sie unter der **enabledstate** -Eigenschaft der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse.

</dd> <dt>

**Enhancedsessionmodestate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Verbindungen im erweiterten Modus vom Host zugelassen werden und ob Sie für den virtuellen Computer verfügbar sind.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**Zulässig und verfügbar** (2)


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**Nicht zulässig** (3)


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**Zulässig, aber nicht verfügbar** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**Guestoperatingsystem**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Gast Betriebssystems, falls verfügbar. Wenn diese Informationen nicht verfügbar sind, ist der Wert dieser Eigenschaft **null**. Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Integritäts Status für den virtuellen Computer. Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

</dd> <dt>

**Heartbeat**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Takt Status für den virtuellen Computer. Weitere Informationen finden Sie in der Dokumentation für die [**Statusbeschreibungen**](msvm-heartbeatcomponent.md) -Eigenschaft der **MSVM \_ heartbeatcomponent** -Klasse. Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

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

**Hostcomputersystemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, auf dem dieser virtuelle Computer gehostet wird.

> [!Note]  
> In Windows 10 hinzugefügt.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ managedelta Element. InstanceId"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

"InstanceId" ist eine optionale Eigenschaft, die verwendet werden kann, um eine Instanz dieser Klasse innerhalb des Gültigkeits Bereichs des instanziierten Namespace eindeutig und eindeutig zu identifizieren. Verschiedene Unterklassen dieser Klasse können diese Eigenschaft überschreiben, um Sie erforderlich zu machen, oder einen Schlüssel. Diese Unterklassen können auch die bevorzugten Algorithmen zum Sicherstellen der Eindeutigkeit ändern, die unten definiert sind.

Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert von InstanceId mit dem folgenden "bevorzugten" Algorithmus erstellt werden:

<OrgID>:<LocalID>

Dabei <OrgID> <LocalID> sind und durch einen Doppelpunkt (:) und wobei <OrgID> ein urheberrechtlich geschütztes, mit einem oder ein oder anderweitig eindeutiger Name enthalten muss, der der Geschäfts Entität entspricht, die die InstanceId erstellt oder definiert, oder die eine registrierte ID ist, die der Geschäfts Entität von einer anerkannten globalen Autorität zugewiesen ist. (Diese Anforderung ähnelt der <Schema Name> \_ <Class Name> Struktur von Schema Klassennamen.) Außerdem <OrgID> darf keine Doppelpunkte (:) enthalten, um die Eindeutigkeit sicherzustellen. Wenn dieser Algorithmus verwendet wird, muss der erste Doppelpunkt, der in InstanceId angezeigt wird, zwischen und angezeigt werden <OrgID> <LocalID> .

<LocalID> wird von der Business-Entität gewählt und sollte nicht wieder verwendet werden, um verschiedene zugrunde liegende (reale) Elemente zu identifizieren. Wenn not NULL und der oben genannte "bevorzugte" Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende InstanceId nicht in allen instanceids wieder verwendet wird, die von diesem oder anderen Anbietern für den Namespace dieser Instanz erstellt werden.

Wenn für von DMTF definierte Instanzen nicht auf NULL festgelegt ist, muss der "bevorzugte" Algorithmus verwendet werden, wobei <OrgID> auf CIM festgelegt ist.

> [!Note]  
> In Windows 10 hinzugefügt.

 

</dd> <dt>

**Integrationservicesversionstate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die auf dem virtuellen Computer installierten Integrationsdienste auf dem neuesten Stand sind.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

**Update** (1)


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

Nicht **überein** stimmende (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Memoryavailable**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Prozentsatz des aktuellen Arbeitsspeichers, der für den virtuellen Computer verfügbar ist. Wenn dynamischer Arbeitsspeicher für eine virtuelle Maschine aktiviert ist, stellt diese Eigenschaft das Verhältnis zwischen dem verfügbaren Arbeitsspeicher des virtuellen Computers und dem gesamten physischen Arbeitsspeicher dar, der dem virtuellen Computer zugewiesen ist. Wenn für eine virtuelle Maschine kein Arbeitsspeicher verfügbar ist, ist diese Eigenschaft negativ und enthält das Verhältnis des Arbeitsspeichers, der für die virtuelle Maschine benötigt wird, zum gesamten physischen Arbeitsspeicher, der der virtuellen Maschine zugewiesen ist.

Diese Eigenschaft ist für Instanzen der **MSVM-Klasse " \_ SummaryInformation** " ungültig, die virtuelle Computer darstellt, für die der dynamische Arbeitsspeicher nicht aktiviert ist.

Diese Eigenschaft ist für Instanzen der **MSVM \_ SummaryInformation** -Klasse, die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

</dd> <dt>

**Memoryspansphysicalnumanodes**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Arbeitsspeicher eines oder mehrerer der virtuellen NUMA-Knoten (nicht einheitlicher Speicherzugriff) der virtuellen Maschine mehrere physische NUMA-Knoten des hostingcomputersystems umfasst. Enthält **true** , wenn der Arbeitsspeicher mehrere physische NUMA-Knoten umfasst, andernfalls **false** .

</dd> <dt>

**MemoryUsage**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Speicherauslastung (in Megabyte) der virtuellen Maschine. Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

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

Die Anmerkungen, die dem virtuellen Computer oder der Momentaufnahme zugeordnet sind.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der virtuellen Prozessoren, die dem virtuellen Computer oder der Momentaufnahme zugeordnet sind.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Der aktuelle Betriebsstatus der virtuellen Maschine. Mögliche Werte finden Sie unter der **OperationalStatus** -Eigenschaft der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse.

</dd> <dt>

**Otherenabledstate**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 festgelegt ist. Diese Eigenschaft wird auf **null** festgelegt, wenn **enabledstate** ein anderer Wert als 1 ist.

</dd> <dt>

**Processorload**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Prozessorauslastung der virtuellen Maschine (in Prozent). Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

</dd> <dt>

**Processorloadhistory**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Ein Array der vorherigen 100-Stichproben der Prozessorauslastung in Prozent für den virtuellen Computer. Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**MSVM \_ SummaryInformation**.**Replicationhealthex**")
</dt> </dl>

Die Replikations Integrität für den virtuellen Computer. Mögliche Werte finden Sie unter der **ReplicationHealth** -Eigenschaft der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse.

> [!Note]  
> Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen " **replicationhealthex**".

 

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

**Replicationhealthex**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Das Array der Replikations Integritäts Werte für die verschiedenen Replikations Beziehungen der virtuellen Maschine. Mögliche Werte finden Sie unter der **ReplicationHealth** -Eigenschaft der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse.

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

Der Replikationstyp für die virtuelle Maschine. Mögliche Werte finden Sie unter der **replicationmode** -Eigenschaft der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse.

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

**Test Replikat** (3)


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

**Erweitertes Replikat** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationProviderId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Für den primären oder erweiterten virtuellen Replikat Computer ist dies die primäre Replikations Anbieter-ID. Bei einem virtuellen Replikat Computer und bei aktivierter erweiterter Replikation ist dies die Anbieter-ID für die erweiterte Beziehung.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**MSVM \_ SummaryInformation**.**Replicationstateex**")
</dt> </dl>

Der Replikations Status für den virtuellen Computer. Mögliche Werte finden Sie unter der **replicationstate** -Eigenschaft der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse.

> [!Note]  
> Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen **replicationstateex**.

 

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


</dt> <dd></dd> </dl>

</dd> <dt>

**Replicationstateex**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Das Array von Replikations Zustands Werten für die verschiedenen Replikations Beziehungen der virtuellen Maschine. Mögliche Werte finden Sie unter der **replicationstate** -Eigenschaft der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Bereit für Replikation** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Warten auf Abschluss der ersten Replikation** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replizieren** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synchronisierungs Replikation beendet** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Wieder hergestellt** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>Commit **ausgeführt (6** )


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>Angeh **alten (7** )


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

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Neusynchronisierung** angehalten (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover** wird ausgeführt (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback** wird ausgeführt (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback ist beendet** (14)


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>Datenträger **Update läuft** (15)


</dt> <dd>

> [!Note]  
> In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>Datenträger **Update kritisch** (16)


</dt> <dd>

> [!Note]  
> In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (17)


</dt> <dd>

> [!Note]  
> In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose Replication in Progress** (18)


</dt> <dd>

> [!Note]  
> In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Vorbereitet für Synchronisierungs Replikation** (19)


</dt> <dd>

> [!Note]  
> In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Vorbereitet für Gruppen umgekehrte Replikation** (20)


</dt> <dd>

> [!Note]  
> In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill läuft** (21)


</dt> <dd>

> [!Note]  
> In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> </dl>

</dd> <dt>

**Geschützt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Schutz für die virtuelle Maschine konfiguriert ist.

> [!Note]  
> In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**Momentaufnahmen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ virtualsystemsettingdata** -Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Ein Array von [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Instanzen, die die Momentaufnahmen für den virtuellen Computer darstellen. Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

</dd> <dt>

**Status Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Zeichen folgen, die die entsprechenden **OperationalStatus** -Array Werte beschreiben. Dies entspricht der Eigenschaft **Status Beschreibungen** der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse.

</dd> <dt>

**Austauschen von Dateien**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Paging auf zweiter Ebene aktiv ist. Enthält **true** , wenn Paging auf zweiter Ebene aktiv ist, andernfalls **false** .

</dd> <dt>

**Testreplicasystem**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Computersystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer des virtuellen Computers für den virtuellen Computer darstellt. Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

</dd> <dt>

**Thumbnailimage**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

**Qualifizierer: octetstring**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**ThumbnailImageWidth**","**MSVM \_ SummaryInformation**.**Thumbnailimageheight**")
</dt> </dl>

Ein Array, das ein kleines Bild des Desktops für die Miniaturansicht des Desktops für den virtuellen Computer oder die Momentaufnahme im RGB565-Format enthält.

</dd> <dt>

**Thumbnailimageheight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**Thumbnailimage**")
</dt> </dl>

Die Höhe des Bilds in der thumbnailimage-Eigenschaft in Pixel.

> [!Note]  
> In Windows 10 hinzugefügt.

 

</dd> <dt>

**ThumbnailImageWidth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**Thumbnailimage**")
</dt> </dl>

Die Breite des Bilds in der thumbnailimage-Eigenschaft in Pixel.

> [!Note]  
> In Windows 10 hinzugefügt.

 

</dd> <dt>

**Betriebszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeitspanne seit dem letzten Starten des virtuellen Computers. Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version des virtuellen Systems im Format "Major. Minor", z. b. "2,0".

> [!Note]  
> In Windows 10 hinzugefügt.

 

</dd> <dt>

**Virtualswitchnames**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Zeichen folgen, die die anzeigen amen der virtuellen Switches angeben, mit denen der virtuelle Computer verbunden ist.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Untertyp des virtuellen Systems.

**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft: Hyper-V: Untertyp: 1** ()


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft: Hyper-V: Untertyp: 2** ()


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM-Klasse " \_ SummaryInformation** " kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**MSVM \_ summaryinformationbase**](msvm-summaryinformationbase.md)
</dt> <dt>

[Klassen des virtuellen Systems](virtual-system-classes.md)
</dt> </dl>

 

