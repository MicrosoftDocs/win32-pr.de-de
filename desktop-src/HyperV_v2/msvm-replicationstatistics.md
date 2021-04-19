---
description: Stellt Replikations Statistiken für eine virtuelle Maschine bereit.
ms.assetid: 52d944a7-9309-4b56-97b7-e050a9501c57
title: Msvm_ReplicationStatistics-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationStatistics
- Msvm_ReplicationStatistics.InstanceID
- Msvm_ReplicationStatistics.Caption
- Msvm_ReplicationStatistics.Description
- Msvm_ReplicationStatistics.ElementName
- Msvm_ReplicationStatistics.StartStatisticTime
- Msvm_ReplicationStatistics.EndStatisticTime
- Msvm_ReplicationStatistics.ReplicationSuccessCount
- Msvm_ReplicationStatistics.ReplicationSize
- Msvm_ReplicationStatistics.MaxReplicationSize
- Msvm_ReplicationStatistics.ReplicationLatency
- Msvm_ReplicationStatistics.ReplicationMissCount
- Msvm_ReplicationStatistics.MaxReplicationLatency
- Msvm_ReplicationStatistics.NetworkFailureCount
- Msvm_ReplicationStatistics.ReplicationFailureCount
- Msvm_ReplicationStatistics.PendingReplicationSize
- Msvm_ReplicationStatistics.ApplicationConsistentSnapshotFailureCount
- Msvm_ReplicationStatistics.ReplicationHealth
- Msvm_ReplicationStatistics.LastTestFailoverTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f18501c2da875a9c3514549271fbc91620abef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349304"
---
# <a name="msvm_replicationstatistics-class"></a>MSVM \_ replicationstatistics-Klasse

Stellt Replikations Statistiken für eine virtuelle Maschine bereit. Diese Statistiken decken den Zeitraum ab, der durch die Eigenschaften **monitoringstarttime** und **monitoringinterval** der [**MSVM \_ replicationservicesettingdata**](msvm-replicationservicesettingdata.md) -Klasse festgelegt wird.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationStatistics : CIM_ManagedElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime StartStatisticTime;
  datetime EndStatisticTime;
  uint32   ReplicationSuccessCount;
  uint64   ReplicationSize;
  uint64   MaxReplicationSize;
  uint32   ReplicationLatency;
  uint32   ReplicationMissCount;
  uint32   MaxReplicationLatency;
  uint32   NetworkFailureCount;
  uint32   ReplicationFailureCount;
  uint64   PendingReplicationSize;
  uint32   ApplicationConsistentSnapshotFailureCount;
  uint32   ReplicationHealth;
  datetime LastTestFailoverTime;
};
```

## <a name="members"></a>Member

Die **MSVM \_ replicationstatistics** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ replicationstatistics** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Applicationkonsistentsnapshotfailucomplete**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der VSS-Momentaufnahme Fehler.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Endstatistictime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeit in UTC, zu der der Hyper-V-Replikat Dienst das Sammeln von Replikations Statistikdaten beendet hat. Zu diesem Zeitpunkt wird ein neuer Replikations Statistik-Cycle gestartet.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Lasttestfailovertime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den letzten Zeitpunkt an, zu dem ein Test Replikat System für einen Replikations fähigen virtuellen Computer auf dem Wiederherstellungs Server erstellt wurde

</dd> <dt>

**Maxreplicationlatency**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Zeitspanne in Sekunden, die für einen einzelnen Replikations Vorgang benötigt wird.

</dd> <dt>

**Maxreplicationsize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Anzahl an Replikations Daten, die an das Wiederherstellungs Host System übertragen werden Dies stellt die maximale Größe von Replikations Daten dar, die für dieses Intervall in einem einzelnen Intervall gesendet werden.

</dd> <dt>

**Networkfailudie**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der Netzwerkfehler, die für den Replikations Kanal mit dem Wiederherstellungs Host System aufgetreten sind.

</dd> <dt>

**"Pdingreplicationsize"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Größe der Daten für eine ausstehende Replikation in Bytes.

</dd> <dt>

**Replicationfailuder**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der Replikations Fehler. Dies schließt Fehler für den Replikations Vorgang ein.

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Replikations Integrität für den virtuellen Computer. Dabei handelt es sich um einen der folgenden Werte.

<dl> <dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (0)
</dt> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>**OK** (1)
</dt> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (2)
</dt> <dt>

<span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Kritisch** (3)
</dt> </dl>

</dd> <dt>

**ReplicationLatency**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gesamt Replikations Latenz beim Übertragen der Daten an das Wiederherstellungs Host System in Sekunden.

</dd> <dt>

**Replicationmisscount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der verpassten Replikations Zyklen. Dies kann auf hohe Arbeitsauslastung, Netzwerkprobleme oder Replikations Fehler liegen.

</dd> <dt>

**Replicationsize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtmenge der Replikations Daten, die auf das Wiederherstellungs Host System übertragen werden (in Bytes)

</dd> <dt>

**Replicationerfolgreiches count**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der erfolgreichen Replikationen für den virtuellen Computer.

</dd> <dt>

**Startstatistictime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeit in UTC, zu der der Hyper-V-Replikat Dienst mit dem Sammeln von Replikations Statistikdaten begonnen hat

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

