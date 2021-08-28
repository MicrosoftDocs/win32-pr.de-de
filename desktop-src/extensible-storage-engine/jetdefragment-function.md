---
description: Weitere Informationen finden Sie unter JetDefragment-Funktion.
title: JetDefragment-Funktion
TOCTitle: JetDefragment Function
ms:assetid: 8215fd00-f1b8-4ebd-8d55-9bce11d7dc9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269317(v=EXCHG.10)
ms:contentKeyID: 32765607
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragmentA
- JetDefragment
- JetDefragmentW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f9fdce5268e6981fa018f58ed14b31c2c078cce
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985945"
---
# <a name="jetdefragment-function"></a>JetDefragment-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdefragment-function"></a>JetDefragment-Funktion

Die **JetDefragment-Funktion** startet und beendet Datenbankdefragmentierungsaufgaben, die die Datenorganisation innerhalb einer Datenbank verbessern. Dies wird durchgeführt, um das Wachstum der Datenbank zu begrenzen, indem die vorhandene Datenträgerzuordnung innerhalb der Datenbank effizienter verwendet wird. Sie kann auch den Arbeitssatz reduzieren, indem sichergestellt wird, dass die Daten stärker gepackt sind. Schließlich kann sie die Anwendungsleistung verbessern, indem allgemeine Vorgänge durch eine bessere Datenorganisation beschleunigt werden.

Die Datenbankdefragmentierung ist ein Onlinevorgang und unterbricht keine regulären Datenbankaktivitäten wie Abfragevorgänge oder Datenaktualisierungen. **JetDefragment** macht auch keine Kopie aller vorhandenen Daten. Stattdessen wird eine Datenbank defragmentiert. Schließlich stellt **JetDefragment** internen Datenbankspeicherplatz für die Wiederherstellen wieder zur Verfügung, gibt jedoch keinen übermäßigen Speicherplatz für das Betriebssystemdateisystem frei.

Das resultierende Format der Daten kann viel effizienter sein, ist aber im Allgemeinen nicht optimal. Die Defragmentierung ist auf die Freigabe von Datenbankseiten für die erneute Verwendung beschränkt, die bereits logisch gelöschte Daten enthalten. Die Defragmentierung macht Datenbankseiten auch in einigen Fällen für die erneute Verwendung verfügbar, indem Daten von zwei Seiten kombiniert werden, wenn sie auf eine einzelne Seite passen.

Dieser Vorgang unterscheidet sich von [JetCompact,](./jetcompact-function.md) bei dem eine Kopie einer schreibgeschützten Datenbank in eine äußerst optimale Form erstellt wird.

```cpp
    JET_ERR JET_API JetDefragment(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __out_opt     unsigned long* pcPasses,
      __out_opt     unsigned long* pcSeconds,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*Dbid*

Die Datenbank, die defragmentiert wird.

*szTableName*

Nicht verwendeter Parameter. Die Defragmentierung wird für die gesamte Datenbank durchgeführt, die von der angegebenen Datenbank-ID beschrieben wird.

*pcPasses*

Beim Starten einer Onlinedefragmentierungsaufgabe legt dieser Eingabeparameter die maximale Anzahl von Defragmentierungsüberläufen fest. Beim Beenden eines Onlinedefragmentierungs-Task wird dieser Ausgabepuffer auf die Anzahl der ausgeführten Durchläufe festgelegt.

Wenn dieser Parameter auf NULL festgelegt ist, ist die Anzahl der Onlinedefragmentierungsüberläufe unbegrenzt.

*pcSeconds*

Beim Starten einer Onlinedefragmentierungsaufgabe legt dieser Eingabeparameter die maximale Zeit für die Defragmentierung fest. Beim Beenden eines Onlinedefragmentierungs-Task wird dieser Ausgabepuffer auf die Dauer festgelegt, die für die Defragmentierung verwendet wird.

Wenn dieser Parameter auf NULL festgelegt ist oder *pcSeconds* auf einen negativen Wert zeigt, ist die maximale Zeit für die Defragmentierung unbegrenzt.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen an geben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitDefragmentAvailSpaceTreesOnly</p> | <p>Defragmentiert den verfügbaren Speicherplatzteil der ESE-Datenbank-Speicherplatzzuordnung. Der Datenbankspeicherplatz ist in zwei Typen unterteilt: im Besitz des Speicherplatzes und des verfügbaren Speicherplatzes. Der eigene Speicherplatz wird einer Tabelle oder einem Index zugeordnet, während verfügbarer Speicherplatz für die Verwendung innerhalb der Tabelle bzw. des Index bereit ist. Der verfügbare Speicherplatz ist im Verhalten viel dynamischer und erfordert eine Onlinedefragmentierung mehr als speicherplatz- oder tabellen- oder indexeigene Daten.</p> | 
| <p>JET_bitDefragmentBatchStart</p> | <p>Startet eine neue Defragmentierungsaufgabe.</p> | 
| <p>JET_bitDefragmentBatchStop</p> | <p>Beendet eine Defragmentierungsaufgabe.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>Die für die Defragmentierung ausgewählte Datenbank ist schreibgeschützt und kann nicht aktualisiert werden, einschließlich defragmentierung.</p> | 
| <p>JET_errDistributedTransactionAlreadyPreparedToCommit</p> | <p>Die gegebene Sitzung befindet sich im Zustand "Commit vorbereitet" und kann keine neuen Updates starten, bis für die aktuelle Transaktion ein Commit oder Rollback ausgeführt wurde.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>Die gegebene Datenbank-ID passt nicht zu einer bekannten Datenbank in der -Instanz.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Die gegebene Sitzung verfügt nur über schreibgeschützte Berechtigungen und kann keine Aufgabe starten, die ein Update ausführen kann, einschließlich Defragmentierung.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>Dieser Fehler tritt auf, wenn die konfigurierte Größe des Versionsspeichers nicht ausreicht, um alle ausstehenden Updates zu speichern.</p> | 
| <p>JET_wrnDefragAlreadyRunning</p> | <p>Die JET_bitDefragmentBatchStart wurde übergeben, aber ein Defragmentierungs-Task wird bereits in der angegebenen Datenbank defragmentiert.</p> | 
| <p>JET_wrnDefragNotRunning</p> | <p>Die JET_bitDefragmentBatchStop wurde übergeben, aber derzeit wird keine Defragmentierungsaufgabe ausgeführt.</p> | 



Bei Erfolg wird entweder die angeforderte Aktion zum Starten einer Defragmentierungsaufgabe für eine bestimmte Daten mit bestimmten Optionen oder die Aktion zum Beenden einer vorhandenen Defragmentierungsaufgabe ausgeführt.

Bei einem Fehler wird die angeforderte Aktion zum Starten oder Beenden eines Onlinedefragmentierungsauftrags nicht durchgeführt. Es treten keine weiteren Nebeneffekte auf.

#### <a name="remarks"></a>Bemerkungen

Die Onlinedefragmentierung wird sowohl durch eine Parametereinstellung als auch durch diese API gesteuert. Der Standardwert des Systemparameters ist JET_OnlineDefragAll, was bedeutet, dass die Defragmentierung für alle unterstützten Datenstrukturen aktiviert ist. Mit [JetSetSystemParameter](./jetsetsystemparameter-function.md)ist es jedoch möglich, die Onlinedefragmentierung zu deaktivieren oder selektiv nur für Datenbankbereichsstrukturen, nur Datenbanken, nur Streamingdateien oder eine beliebige Kombination dieser Optionen zu aktivieren. Wenn die Systemeinstellung für die Onlinedefragmentierung auf eine veraltete Einstellung festgelegt ist, behandelt **JetDefragment** die Einstellung als JET_OnlineDefragAll.

Für jede Datenbank kann nur ein Task ausgeführt werden. Die Aufgabe wird als Thread in dem Prozess ausgeführt, der ESE hosten soll.

Die Sitzung, die zum Starten des Onlinedefragmentierungs-Task verwendet wird, kann anschließend für Datenbankvorgänge verwendet werden, während der Defragmentierungs-Task fortgesetzt wird, da der Defragmentierungs-Task eine eigene Sitzung zuteilen kann. Die gegebene Sitzung wird nur verwendet, um die Berechtigungen zu überprüfen, die der Taskstartsitzung zugeordnet sind, und wird nicht tatsächlich für die Defragmentierungsvorgänge selbst verwendet.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetDefragmentW</strong> (Unicode) und <strong>JetDefragmentA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment2](./jetdefragment2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
