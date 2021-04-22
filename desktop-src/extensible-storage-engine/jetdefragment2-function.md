---
description: 'Weitere Informationen zu: JetDefragment2-Funktion'
title: JetDefragment2-Funktion
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bcde8d55032d2e07466668b5a4d96b9a447d843
ms.sourcegitcommit: 35baf9ba19918a38c4ca8714f88c004af0c6f518
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107838804"
---
# <a name="jetdefragment2-function"></a>JetDefragment2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdefragment2-function"></a>JetDefragment2-Funktion

Die **JetDefragment2-Funktion** startet und beendet Datenbankdefragmentierungsaufgaben, wodurch die Datenorganisation innerhalb einer Datenbank verbessert wird, wobei ein Rückrufparameter verfügbar ist, um den Fortschritt der Defragmentierung zu melden. Dies wird durchgeführt, um das Wachstum der Datenbank zu begrenzen, indem die vorhandene Datenträgerzuordnung innerhalb der Datenbank effizienter verwendet wird. Sie kann auch den Arbeitssatz reduzieren, indem sichergestellt wird, dass die Daten genauer gepackt werden. Schließlich kann sie die Anwendungsleistung verbessern, indem allgemeine Vorgänge durch eine bessere Datenorganisation beschleunigt werden.

**Windows XP:**  **JetDefragment2** wird in Windows XP eingeführt.

**JetDefragment2** enthält auch einen Rückruffunktionsparameter, der zum Melden des Fortschritts des Defragmentierungsprozesses verwendet wird.

Die Datenbankdefragmentierung ist ein Onlinevorgang und unterbricht keine regulären Datenbankaktivitäten wie Abfragevorgänge oder Datenaktualisierungen. **JetDefragment2** erstellt auch keine Kopie aller vorhandenen Daten. Stattdessen wird eine Datenbank an Ort und Stelle defragmentiert. Schließlich stellt **JetDefragment2** den internen Datenbankspeicherplatz für die Wiederverwendung wieder her, gibt jedoch keinen zusätzlichen Speicherplatz für das Betriebssystemdateisystem frei.

Das resultierende Format der Daten kann viel effizienter sein, ist aber im Allgemeinen nicht optimal. Die Defragmentierung ist auf die Freigabe von Datenbankseiten zur erneuten Verwendung beschränkt, die Daten enthalten, die bereits logisch gelöscht wurden. Durch die Defragmentierung können Datenbankseiten in einigen Fällen auch wiederverwendet werden, indem Daten von zwei Seiten kombiniert werden, wenn sie auf eine einzelne Seite passen.

Dieser Vorgang unterscheidet sich von [JetCompact,](./jetcompact-function.md) bei dem eine Kopie einer schreibgeschützten Datenbank in eine äußerst optimale Form umgewandelt wird.

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*Dbid*

Die zu defragmentierende Datenbank.

*szTableName*

Manchmal *ist szTableName* erforderlich, und manchmal ist es verboten:

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | Muss `NULL`lauten. |
| `JET_bitDefragmentBTree` | Gibt den Namen der tabelle/BTree an, die defragmentiert werden soll. |
| *Andere* | Muss `NULL`lauten. |
 
Die Defragmentierung wird für die gesamte Datenbank durchgeführt, die von der angegebenen Datenbank-ID beschrieben wird.

*pcPasses*

Beim Starten einer Onlinedefragmentierungsaufgabe legt dieser optionale Eingabeparameter die maximale Anzahl von Defragmentierungsüberläufen fest. Beim Beenden eines Onlinedefragmentierungs-Task wird dieser optionale Ausgabepuffer auf die Anzahl der ausgeführten Durchläufe festgelegt.

Wenn dieser Parameter auf NULL festgelegt ist, ist die Anzahl der Onlinedefragmentierungsüberläufe unbegrenzt.

*pcSeconds*

Beim Starten einer Onlinedefragmentierungsaufgabe legt dieser optionale Eingabeparameter die maximale Zeit für die Defragmentierung fest. Beim Beenden eines Onlinedefragmentierungs-Task wird dieser optionale Ausgabepuffer auf die Dauer festgelegt, die für die Defragmentierung verwendet wird.

Wenn dieser Parameter auf NULL festgelegt ist oder *pcSeconds* auf einen negativen Wert zeigt, ist die maximale Zeit für die Defragmentierung unbegrenzt.

*Rückruf*

Rückruffunktion, die bei der Defragmentierung regelmäßig aufruft, um den Fortschritt zu melden.

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | Muss `NULL`lauten. |
| `JET_bitDefragmentBTree` | Muss `NULL`lauten. |
| *Andere* | Optional.


*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitDefragmentAvailSpaceTreesOnly</p></td>
<td><p>Diese Option wird verwendet, um den verfügbaren Speicherplatzteil der ESE-Datenbankspeicherplatzbelegung zu defragmentieren. Der Datenbankspeicherplatz ist in zwei Typen unterteilt: eigener Speicherplatz und verfügbarer Speicherplatz. Der eigene Speicherplatz wird einer Tabelle oder einem Index zugeordnet, während der verfügbare Speicherplatz für die Verwendung innerhalb der Tabelle bzw. des Indexes bereit ist. Der verfügbare Speicherplatz ist im Verhalten viel dynamischer und erfordert eine größere Onlinedefragmentierung als speicherplatz- oder tabellen- oder indexeigene Daten.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBatchStart</p></td>
<td><p>Diese Option wird verwendet, um eine neue Defragmentierungsaufgabe zu starten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDefragmentBatchStop</p></td>
<td><p>Diese Option wird verwendet, um eine vorhandene gestartete Defragmentierungsaufgabe zu beenden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBTree</p></td>
<td><p>Diese Option wird verwendet, um eine durch szTableName angegebene B-Struktur zu defragmentieren.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDefragmentBTreeBatch</p></td>
<td><p>Diese Option wird verwendet, um OLD2 für die gesamte Datenbank aufzurufen.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly</p></td>
<td><p>Die für die Defragmentierung ausgewählte Datenbank ist schreibgeschützt und kann nicht aktualisiert werden, einschließlich defragmentierung.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDistributedTransactionAlreadyPreparedToCommit</p></td>
<td><p>Die gegebene Sitzung befindet sich im Zustand "Commit vorbereitet" und kann keine neuen Updates starten, bis für die aktuelle Transaktion ein Commit oder Rollback ausgeführt wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>Die gegebene Datenbank-ID passt nicht zu einer bekannten Datenbank in der -Instanz.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Die angegebene Sitzung verfügt nur über schreibgeschützte Berechtigungen und kann keine Aufgabe starten, die möglicherweise ein Update ausführt, einschließlich Defragmentierung.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Dieser Fehler tritt auf, wenn die konfigurierte Größe des Versionsspeichers nicht ausreicht, um alle ausstehenden Updates zu speichern.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragAlreadyRunning</p></td>
<td><p>Die option JET_bitDefragmentBatchStart wurde übergeben, aber eine Defragmentierungsaufgabe führt bereits die Defragmentierung für die angegebene Datenbank aus.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragNotRunning</p></td>
<td><p>Die option JET_bitDefragmentBatchStop wurde übergeben, aber derzeit wird keine Defragmentierungsaufgabe ausgeführt.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird die angeforderte Aktion ausgeführt, entweder eine Defragmentierungsaufgabe für bestimmte Daten mit angegebenen Optionen zu starten, oder die Aktion zum Beenden einer vorhandenen Defragmentierungsaufgabe wird ausgeführt.

Bei einem Fehler wird die angeforderte Aktion zum Starten oder Beenden eines Onlinedefragmentierungsauftrags nicht ausgeführt. Es treten keine weiteren Nebeneffekte auf.

#### <a name="remarks"></a>Bemerkungen

Die Onlinedefragmentierung wird sowohl durch eine Parametereinstellung als auch durch diese API gesteuert. Der Standardwert des Systemparameters ist JET_OnlineDefragAll. Dies bedeutet, dass die Defragmentierung für alle unterstützten Datenstrukturen aktiviert ist. Bei Verwendung von [JetSetSystemParameter](./jetsetsystemparameter-function.md)ist es jedoch möglich, die Onlinedefragmentierung zu deaktivieren oder sie selektiv nur für Datenbankspeicherplatzstrukturen, nur Datenbanken, nur Streamingdateien oder eine beliebige Kombination dieser Optionen zu aktivieren. Wenn die Systemeinstellung für die Onlinedefragmentierung auf eine veraltete Einstellung festgelegt ist, behandelt **JetDefragment2** die Einstellung als JET_OnlineDefragAll.

Es kann höchstens eine Aufgabe für jede Datenbank ausgeführt werden. Die Aufgabe wird als Thread im Prozess ausgeführt, der ESE hostet.

Die Zum Starten des Onlinedefragmentierungstasks verwendete Sitzung kann anschließend für Datenbankvorgänge verwendet werden, während der Defragmentierungstask fortgesetzt wird, da der Defragmentierungstask eine eigene Sitzung zuordnet. Die angegebene Sitzung wird nur verwendet, um die Berechtigungen zu überprüfen, die der Startsitzung des Tasks zugeordnet sind, und wird nicht tatsächlich für die Defragmentierungsvorgänge selbst verwendet.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In Esent.h deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JetDefragment2W</strong> (Unicode) und <strong>JetDefragment2A</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
