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
ms.openlocfilehash: 08e6cf618be4f3bf7f6eee1b903559db579973c0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984983"
---
# <a name="jetdefragment2-function"></a>JetDefragment2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdefragment2-function"></a>JetDefragment2-Funktion

Die **JetDefragment2-Funktion** startet und beendet Datenbankdefragmentierungsaufgaben, wodurch die Datenorganisation innerhalb einer Datenbank verbessert wird, wobei ein Rückrufparameter verfügbar ist, um den Fortschritt der Defragmentierung zu melden. Dies wird durchgeführt, um das Wachstum der Datenbank zu begrenzen, indem die vorhandene Datenträgerzuordnung innerhalb der Datenbank effizienter verwendet wird. Sie kann auch den Arbeitssatz reduzieren, indem sichergestellt wird, dass die Daten genauer gepackt werden. Schließlich kann sie die Anwendungsleistung verbessern, indem allgemeine Vorgänge durch eine bessere Datenorganisation beschleunigt werden.

**Windows XP:****JetDefragment2** wird in Windows XP eingeführt.  

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

Manchmal ist *szTableName* erforderlich, und manchmal ist es unzulässig:

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | Muss `NULL`lauten. |
| `JET_bitDefragmentBTree` | Gibt den Namen der zu defragmentierenden Tabelle/BTree an. |
| *Andere* | Muss `NULL`lauten. |
 
Die Defragmentierung wird für die gesamte Datenbank ausgeführt, die von der angegebenen Datenbank-ID beschrieben wird.

*pcPasses*

Beim Starten einer Onlinedefragmentierungsaufgabe legt dieser optionale Eingabeparameter die maximale Anzahl von Defragmentierungsdurchläufen fest. Beim Beenden einer Onlinedefragmentierungsaufgabe wird dieser optionale Ausgabepuffer auf die Anzahl der ausgeführten Durchläufe festgelegt.

Wenn dieser Parameter auf NULL festgelegt ist, ist die Anzahl der Onlinedefragmentierungsdurchläufe unbegrenzt.

*pcSeconds*

Beim Starten einer Onlinedefragmentierungsaufgabe legt dieser optionale Eingabeparameter die maximale Zeit für die Defragmentierung fest. Beim Beenden einer Onlinedefragmentierungsaufgabe wird dieser optionale Ausgabepuffer auf die Für die Defragmentierung verwendete Zeitspanne festgelegt.

Wenn dieser Parameter auf NULL festgelegt ist oder *pcSeconds* auf einen negativen Wert zeigt, ist die maximale Zeit für die Defragmentierung unbegrenzt.

*Rückruf*

Rückruffunktion, die die Defragmentierung regelmäßig aufruft, um den Fortschritt zu melden.

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | Muss `NULL`lauten. |
| `JET_bitDefragmentBTree` | Muss `NULL`lauten. |
| *Andere* | Optional.


*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitDefragmentAvailSpaceTreesOnly</p> | <p>Diese Option wird verwendet, um den verfügbaren Speicherplatzteil der ESE-Datenbankspeicherplatzbelegung zu defragmentieren. Der Datenbankspeicherplatz ist in zwei Typen unterteilt: eigener Speicherplatz und verfügbarer Speicherplatz. Der eigene Speicherplatz wird einer Tabelle oder einem Index zugeordnet, während der verfügbare Speicherplatz für die Verwendung innerhalb der Tabelle bzw. des Indexes bereit ist. Der verfügbare Speicherplatz ist im Verhalten viel dynamischer und erfordert eine größere Onlinedefragmentierung als speicherplatz- oder tabellen- oder indexeigene Daten.</p> | 
| <p>JET_bitDefragmentBatchStart</p> | <p>Diese Option wird verwendet, um eine neue Defragmentierungsaufgabe zu starten.</p> | 
| <p>JET_bitDefragmentBatchStop</p> | <p>Diese Option wird verwendet, um eine vorhandene gestartete Defragmentierungsaufgabe zu beenden.</p> | 
| <p>JET_bitDefragmentBTree</p> | <p>Diese Option wird verwendet, um eine durch szTableName angegebene B-Struktur zu defragmentieren.</p> | 
| <p>JET_bitDefragmentBTreeBatch</p> | <p>Diese Option wird verwendet, um OLD2 für die gesamte Datenbank aufzurufen.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>Die für die Defragmentierung ausgewählte Datenbank ist schreibgeschützte Datenbank und kann nicht aktualisiert werden, einschließlich der Defragmentierung.</p> | 
| <p>JET_errDistributedTransactionAlreadyPreparedToCommit</p> | <p>Die angegebene Sitzung befindet sich im Zustand bereit für den Commit und kann keine neuen Updates starten, bis für die aktuelle Transaktion ein Commit oder Rollback ausgeführt wurde.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>Die angegebene Datenbank-ID stimmt nicht mit einer bekannten Datenbank in der -Instanz überein.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Die angegebene Sitzung verfügt nur über schreibgeschützte Berechtigungen und kann keine Aufgabe starten, die möglicherweise ein Update ausführt, einschließlich Defragmentierung.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>Dieser Fehler tritt auf, wenn die konfigurierte Größe des Versionsspeichers nicht ausreicht, um alle ausstehenden Updates zu speichern.</p> | 
| <p>JET_wrnDefragAlreadyRunning</p> | <p>Die option JET_bitDefragmentBatchStart wurde übergeben, aber eine Defragmentierungsaufgabe führt bereits die Defragmentierung für die angegebene Datenbank aus.</p> | 
| <p>JET_wrnDefragNotRunning</p> | <p>Die option JET_bitDefragmentBatchStop wurde übergeben, aber derzeit wird keine Defragmentierungsaufgabe ausgeführt.</p> | 



Bei Erfolg wird die angeforderte Aktion ausgeführt, entweder eine Defragmentierungsaufgabe für bestimmte Daten mit angegebenen Optionen zu starten, oder die Aktion zum Beenden einer vorhandenen Defragmentierungsaufgabe wird ausgeführt.

Bei einem Fehler wird die angeforderte Aktion zum Starten oder Beenden eines Onlinedefragmentierungsauftrags nicht ausgeführt. Es treten keine weiteren Nebeneffekte auf.

#### <a name="remarks"></a>Bemerkungen

Die Onlinedefragmentierung wird sowohl durch eine Parametereinstellung als auch durch diese API gesteuert. Der Standardwert des Systemparameters ist JET_OnlineDefragAll. Dies bedeutet, dass die Defragmentierung für alle unterstützten Datenstrukturen aktiviert ist. Bei Verwendung von [JetSetSystemParameter](./jetsetsystemparameter-function.md)ist es jedoch möglich, die Onlinedefragmentierung zu deaktivieren oder sie selektiv nur für Datenbankspeicherplatzstrukturen, nur Datenbanken, nur Streamingdateien oder eine beliebige Kombination dieser Optionen zu aktivieren. Wenn die Systemeinstellung für die Onlinedefragmentierung auf eine veraltete Einstellung festgelegt ist, behandelt **JetDefragment2** die Einstellung als JET_OnlineDefragAll.

Es kann höchstens eine Aufgabe für jede Datenbank ausgeführt werden. Die Aufgabe wird als Thread im Prozess ausgeführt, der ESE hostet.

Die Sitzung, die zum Starten des Onlinedefragmentierungstasks verwendet wird, kann anschließend für Datenbankvorgänge verwendet werden, während der Defragmentierungstask fortgesetzt wird, da der Defragmentierungstask eine eigene Sitzung zuordnet. Die angegebene Sitzung wird nur verwendet, um die Berechtigungen zu überprüfen, die der Startsitzung des Tasks zugeordnet sind, und wird nicht tatsächlich für die Defragmentierungsvorgänge selbst verwendet.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetDefragment2W</strong> (Unicode) und <strong>JetDefragment2A</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
