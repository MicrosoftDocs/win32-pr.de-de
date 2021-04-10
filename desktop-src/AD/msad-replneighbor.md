---
title: MSAD_ReplNeighbor-Klasse
description: Stellt die DS- \_ repl \_ -Nachbar Struktur dar, die die eingehenden Replikations Zustandsinformationen für einen bestimmten namens Kontext (NC) und das Quell Server Paar enthält.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- MSAD_ReplNeighbor-Klasse Active Directory
- MSAD_ReplNeighbor Klasse Active Directory, beschrieben
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor
- MSAD_ReplNeighbor.NamingContextDN
- MSAD_ReplNeighbor.SourceDsaObjGuid
- MSAD_ReplNeighbor.NamingContextObjGuid
- MSAD_ReplNeighbor.SourceDsaDN
- MSAD_ReplNeighbor.SourceDsaAddress
- MSAD_ReplNeighbor.SourceDsaInvocationID
- MSAD_ReplNeighbor.AsyncIntersiteTransportDN
- MSAD_ReplNeighbor.AsyncIntersiteTransportObjGuid
- MSAD_ReplNeighbor.USNLastObjChangeSynced
- MSAD_ReplNeighbor.USNAttributeFilter
- MSAD_ReplNeighbor.TimeOfLastSyncSuccess
- MSAD_ReplNeighbor.TimeOfLastSyncAttempt
- MSAD_ReplNeighbor.LastSyncResult
- MSAD_ReplNeighbor.NumConsecutiveSyncFailures
- MSAD_ReplNeighbor.ReplicaFlags
- MSAD_ReplNeighbor.Writeable
- MSAD_ReplNeighbor.SyncOnStartup
- MSAD_ReplNeighbor.DoScheduledSyncs
- MSAD_ReplNeighbor.UseAsyncIntersiteTransport
- MSAD_ReplNeighbor.TwoWaySync
- MSAD_ReplNeighbor.FullSyncInProgress
- MSAD_ReplNeighbor.FullSyncNextPacket
- MSAD_ReplNeighbor.NeverSynced
- MSAD_ReplNeighbor.IgnoreChangeNotifications
- MSAD_ReplNeighbor.DisableScheduledSync
- MSAD_ReplNeighbor.CompressChanges
- MSAD_ReplNeighbor.NoChangeNotifications
- MSAD_ReplNeighbor.SourceDsaSite
- MSAD_ReplNeighbor.SourceDsaCN
- MSAD_ReplNeighbor.Domain
- MSAD_ReplNeighbor.IsDeletedSourceDsa
- MSAD_ReplNeighbor.ModifiedNumConsecutiveSyncFailures
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9554c73c7fb84aad10ae6dda51480a7644d8434a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956512"
---
# <a name="msad_replneighbor-class"></a>MSAD \_ ReplNeighbor-Klasse

Stellt die [**DS- \_ repl- \_ Nachbar**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) Struktur dar, die die eingehenden Replikations Zustandsinformationen für einen bestimmten namens Kontext (NC) und das Quell Server Paar enthält, wie von der [**dsreplicagetinfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) -Funktion zurückgegeben.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplNeighbor
{
  String   NamingContextDN;
  String   SourceDsaObjGuid;
  String   NamingContextObjGuid;
  String   SourceDsaDN;
  String   SourceDsaAddress;
  String   SourceDsaInvocationID;
  String   AsyncIntersiteTransportDN;
  String   AsyncIntersiteTransportObjGuid;
  uint64   USNLastObjChangeSynced;
  uint64   USNAttributeFilter;
  datetime TimeOfLastSyncSuccess;
  datetime TimeOfLastSyncAttempt;
  uint32   LastSyncResult;
  uint32   NumConsecutiveSyncFailures;
  uint32   ReplicaFlags;
  boolean  Writeable = FALSE;
  boolean  SyncOnStartup = FALSE;
  boolean  DoScheduledSyncs = FALSE;
  boolean  UseAsyncIntersiteTransport = FALSE;
  boolean  TwoWaySync = FALSE;
  boolean  FullSyncInProgress = FALSE;
  boolean  FullSyncNextPacket = FALSE;
  boolean  NeverSynced = FALSE;
  boolean  IgnoreChangeNotifications = FALSE;
  boolean  DisableScheduledSync = FALSE;
  boolean  CompressChanges = FALSE;
  boolean  NoChangeNotifications = FALSE;
  String   SourceDsaSite;
  String   SourceDsaCN;
  String   Domain;
  boolean  IsDeletedSourceDsa = FALSE;
  uint32   ModifiedNumConsecutiveSyncFailures;
};
```

## <a name="members"></a>Member

Die **MSAD \_ ReplNeighbor** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSAD \_ ReplNeighbor** -Klasse verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Syncnamingcontext**](syncnamingcontext-msad-replneighbor.md) | Synchronisiert einen Ziel namens Kontext mit einer seiner Quellen.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MSAD \_ ReplNeighbor** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Asyncintersitetransportdn**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den X. 500-Pfad des [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) -Objekts ab, das dem Transport entspricht, über den die Replikation ausgeführt wird. Legen Sie für die RPC/IP-Replikation auf **null** fest.

</dd> <dt>

**Asyncintersitetransportobjguid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die GUID des standortübergreifenden Transport Objekts ab, das der **asyncintersitetransportdn** -Eigenschaft entspricht.

</dd> <dt>

**Compresschanges**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **DS- \_ repl- \_ NBR \_ \_** -Flag zum Komprimieren von Änderungen in der **replicaflags** -Eigenschaft festgelegt wurde.

</dd> <dt>

**Disablescheduledsync**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das Flag zum **\_ \_ \_ Deaktivieren \_ geplanter \_ Synchronisierung in DS repl** in der **replicaflags** -Eigenschaft festgelegt wurde.

</dd> <dt>

**Domäne**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den kanonischen Namen der Domäne des replizierten NC ab.

</dd> <dt>

**Doscheduledsyncs**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das Flag " **DS \_ repl \_ NBR \_ do \_ Scheduled \_ syncs** " in der **replicaflags** -Eigenschaft festgelegt wurde.

</dd> <dt>

**Fullsyncinprogress**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob in der **replicaflags** -Eigenschaft das Flag **\_ für die \_ \_ vollständige Synchronisierung von DS repl NBR \_ \_ in \_ Progress** festgelegt wurde.

</dd> <dt>

**Fullsyncnextpacket**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das Flag für die **\_ vollständige Synchronisierung der DS-repl- \_ \_ voll \_ Synchronisierung des \_ nächsten \_ Pakets** in der **replicaflags** -Eigenschaft

</dd> <dt>

**Ignorechangenotifications**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das Flag " **DS \_ repl \_ NBR- \_ \_ Änderungs \_ Benachrichtigungen ignorieren** " in der **replicaflags** -Eigenschaft festgelegt wurde.

</dd> <dt>

**Isdeletedsourcedsa**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den-Wert ab, der angibt, ob diese Verbindung einen Quell-DC darstellt, der gelöscht wurde. **True** , wenn diese Verbindung einen Quell-DC darstellt, der gelöscht wurde. andernfalls **false**. In der Entwurfszeit repliziert die DS diese Verbindungen für einige Zeit nach dem Löschen des Quell Domänen Controllers.

</dd> <dt>

**Lastsynkresult**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den **HRESULT** -Fehlercode für den letzten Replikations Versuch ab.

</dd> <dt>

**ModifiedNumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Anzahl der aufeinander folgenden fehlgeschlagenen Replikations Versuche ab, ohne die Verbindungen, für die ein Fehler erwartet wird. Wenn z. b. die **isdeletedsourcedsa** -Eigenschaft auf **true** festgelegt ist, wird erwartet, dass Sie fehlschlägt.

</dd> <dt>

**Namingcontextdn**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den X. 500-Pfad für den NC ab, der von dieser Verbindung repliziert wird.

</dd> <dt>

**Namingcontextobjguid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die GUID für den replizierten NC ab.

</dd> <dt>

**Nicht synchronisiert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das Flag " **DS \_ repl \_ NBR \_ nie \_ synchronisiert** " in der **replicaflags** -Eigenschaft festgelegt wurde.

</dd> <dt>

**Nochangenotifications**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das Flag " **DS \_ repl \_ NBR \_ No \_ Change \_** Notification" in der **replicaflags** -Eigenschaft festgelegt wurde.

</dd> <dt>

**Numaufeinanderfolgende tivesyncfailure**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Anzahl der aufeinanderfolgenden fehlgeschlagenen Replikations Versuche ab.

</dd> <dt>

**Replicaflags**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Satz von Flags ab, die Attribute und Optionen für die Replikations Daten angeben. Diese Eigenschaft kann NULL sein oder eine Kombination aus einem oder mehreren der folgenden Flags aufweisen.

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS \_ \_ \_ Beschreibbares repl-NBR** (16 (0x10))


</dt> <dd>

Die lokale Kopie des Namenskontexts ist nicht schreibgeschützt.

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS \_ REPL- \_ NBR- \_ Synchronisierung \_ beim \_ Start** (32 (0x20))


</dt> <dd>

Beim Starten des Zielservers wird versucht, diesen namens Kontext aus dieser Quelle zu replizieren. Dieses Flag gilt normalerweise nur für Standort interne Nachbarn.

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS \_ REPL \_ NBR \_ \_ geplante \_ Synchronisierungen** (64 (0x40))


</dt> <dd>

Die Replikation nach einem Zeitplan ausführen. Dieses Flag wird normalerweise festgelegt, es sei denn, der Zeitplan für diesen namens Kontext oder diese Quelle ist "Never", d. h. der leere Zeitplan.

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS \_ REPL \_ NBR \_ verwendet \_ Async- \_ standortübergreifenden \_ Transport** (128 (0x80))


</dt> <dd>

Die Replikation indirekt über den standortübergreifenden Meldungsdienst ausführen. Dieses Flag wird nur festgelegt, wenn über SMTP repliziert wird. Dieses Flag wird nicht festgelegt, wenn über standortübergreifendes RPC/IP repliziert wird.

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS \_ REPL NBR bidirektionale \_ \_ \_ \_ Synchronisierung** (512 (0x200))


</dt> <dd>

Wenn festgelegt, wird angegeben, dass der Zielserver nach Abschluss der eingehenden Replikation den Quell Server in umgekehrter Richtung synchronisieren muss. Dieses Feature wird in DFÜ-Szenarien verwendet, in denen nur einer der beiden Server eine DFÜ-Verbindung initiieren kann. Diese Option kann z. b. in einer Unternehmenszentrale und Filiale verwendet werden, in der die Zweigstelle mithilfe einer DFÜ-ISP-Verbindung eine Verbindung mit dem Unternehmens Hauptsitz über das Internet herstellt.

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS \_ REPL \_ NBR \_ Rückgabe \_ Objekt \_** -übergeordnete Elemente (2048 (0x800))


</dt> <dd>

Dieser Nachbar befindet sich in einem Zustand, in dem er vor untergeordneten Objekten übergeordnete Objekte zurückgibt. Der Nachbar wechselt in diesen Zustand, nachdem er ein untergeordnetes Element vor dem zugehörigen übergeordneten Element empfangen hat.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS \_ \_ \_ Vollständige \_ Synchronisierung \_ der \_ repl NBR** wird ausgeführt (65536 (0x10000))


</dt> <dd>

Der Zielserver führt eine vollständige Synchronisierung vom Quellserver aus. Vollständige Synchronisierung verwenden keine Vektoren, die Aktualisierungen (z. b. [**DS- \_ repl- \_ Cursors**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) zum Filtern von Aktualisierungen erstellen. Vollständige Synchronisierung wird nicht als Teil des standardmäßigen Replikations Protokolls verwendet.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS \_ REPL \_ NBR- \_ vollständige \_ Synchronisierung \_ Nächster \_ Paket** (131072 (0x20000))


</dt> <dd>

Das letzte Paket aus der Quelle hat eine Änderung eines Objekts angegeben, das vom Zielserver noch nicht erstellt wurde. Das nächste Paket, das angefordert werden soll, weist den Quell Server an, alle Attribute des geänderten Objekts in das Paket einzufügen.

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS \_ REPL \_ NBR \_ nie \_ synchronisiert** (2097152 (0x200000))


</dt> <dd>

Eine Synchronisierung ist von dieser Quelle nie erfolgreich abgeschlossen worden.

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS \_ REPL \_ NBR \_ vorzeitig** entfernt (16777216 (0x1000000))


</dt> <dd>

Die Replikations-Engine hat die Verarbeitung dieses Nachbarn vorübergehend beendet, um einen anderen Nachbar mit höherer Priorität zu verarbeiten, entweder für diese Partition oder für eine andere Partition. Die Replikations-Engine fährt mit der Verarbeitung dieses Nachbarn fort, nachdem die Arbeit mit der höheren Priorität abgeschlossen wurde.

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS \_ REPL \_ NBR \_ - \_ Änderungs \_ Benachrichtigungen ignorieren** (67108864 (0x4000000))


</dt> <dd>

Dieser Nachbar ist darauf festgelegt, Benachrichtigungs basierte Synchronisierung zu deaktivieren. Innerhalb eines Standorts werden Domänencontroller bei Vornahme von Änderungen auf Grundlage von Benachrichtigungen miteinander synchronisiert. Diese Einstellung verhindert, dass dieser Nachbar Synchronisierung durchführt, die von Benachrichtigungen ausgelöst werden. Der Nachbar führt weiterhin Synchronisierung basierend auf dem Zeitplan oder als Reaktion auf manuell angeforderte Synchronisierung durch.

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS \_ REPL \_ NBR \_ , \_ geplante \_ Synchronisierung deaktivieren** (134217728 (0x8000000))


</dt> <dd>

Dieser Nachbar ist so festgelegt, dass keine Synchronisierung basierend auf dem Zeitplan durchgeführt wird. Die einzige Möglichkeit, mit der die Synchronisierung durchgeführt wird, ist die Antwort auf Änderungs Benachrichtigungen oder manuell angeforderte Synchronisierung.

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS \_ Änderungen an der \_ NBR- \_ Komprimierung \_** (268435456 (0x10000000))


</dt> <dd>

Die von dieser Quelle empfangenen Änderungen müssen komprimiert werden. Die Komprimierung erfolgt in der Regel nur, wenn sich der Quell Server an einem anderen Standort befindet.

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS \_ REPL \_ NBR \_ keine \_ Änderungs \_ Benachrichtigungen** (536870912 (0x20000000))


</dt> <dd>

Von dieser Quelle sollten keine Änderungsbenachrichtigungen empfangen werden. Wird normalerweise nur dann festgelegt, wenn sich der Quell Server an einem anderen Standort befindet.

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS \_ \_ \_ Teil \_ Attribut \_ Satz für repl-NBR** (1073741824 (0x40000000))


</dt> <dd>

Dieser Nachbar befindet sich in einem Zustand, in dem er den Inhalt dieses Replikats aufgrund einer Änderung im Teilattributsatz neu erstellt.

</dd> </dl>

</dd> <dt>

**Sourcedsaaddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die DNS-Adresse des Quell Domänen Controllers ab.

> [!Note]  
> Diese Zeichenfolge enthält eine geänderte GUID, nicht den häufig verwendeten kanonischen DNS-Namen.

 

</dd> <dt>

**SourceDsaCN**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Objekt Pfadkomponente für das DSA ab, das den Quell Domänen Controller darstellt. Diese Zeichenfolge ähnelt häufig dem Computernamen, ist aber nicht immer identisch.

</dd> <dt>

**Sourcedsadn**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den X. 500-Pfad für das DSA ab, das den Quell Domänen Controller darstellt.

</dd> <dt>

**Sourcedsainvocationid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Aufruf-ID ab, die vom Quell Server bei der letzten Replikation verwendet wurde.

</dd> <dt>

**Sourcedsaobjguid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft die GUID für den Verzeichnisdienst-Agent (DSA) ab, der den Quell Domänen Controller (DC) darstellt.

</dd> <dt>

**Sourcedsasite**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Site ab, die den Quell Domänen Controller enthält.

</dd> <dt>

**Synchronisierungs Start**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das Flag **DS \_ repl \_ NBR \_ Sync \_ on \_ Startup** in der **replicaflags** -Eigenschaft festgelegt wurde.

</dd> <dt>

**Timeoflastsyncatcher**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel für den letzten Replikations Versuch ab.

</dd> <dt>

**TimeOfLastSyncSuccess**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel für den letzten erfolgreichen Replikations Versuch ab.

</dd> <dt>

**Twowaysync**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das Flag für die bidirektionale **\_ \_ \_ \_ \_ Synchronisierung von DS repl NBR** in der **replicaflags** -Eigenschaft festgelegt wurde

</dd> <dt>

**Useasyncintersitetransport**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **DS \_ repl-NBR-Transport Flag für die \_ \_ \_ \_ Standort \_ übergreifende Verwendung** in der **replicaflags** -Eigenschaft festgelegt wurde.

</dd> <dt>

**"", "".**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert der Eigenschaft "Wert der Eigenschaft" "für" " **für das Ende** des letzten erfolgreichen abgeschlossenen Replikations Prozesses ab. NULL, wenn keine erfolgreich abgeschlossenen Replikations Zyklen vorhanden waren.

</dd> <dt>

**"" Für "" "" ".**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den [**unveränderten**](/windows/desktop/ADSchema/a-usnchanged) Attribut Wert des letzten empfangenen Objekt Updates ab.

</dd> <dt>

**Schreibbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das Flag zum Schreiben von **DS- \_ repl \_ NBR \_** in der **replicaflags** -Eigenschaft festgelegt wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Microsoftactivedirectory-Stammverzeichnis<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

