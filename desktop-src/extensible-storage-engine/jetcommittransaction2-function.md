---
description: Weitere Informationen finden Sie unter JetCommitTransaction2-Funktion.
title: JetCommitTransaction2-Funktion
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ad6c3584f27421b14ef44ed86b423778a570b63
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465847"
---
# <a name="jetcommittransaction2-function"></a>JetCommitTransaction2-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetCommitTransaction2-Funktion** führt einen Commit für die Änderungen aus, die während des aktuellen Speicherpunkts am Zustand der Datenbank vorgenommen wurden, und migriert sie zum vorherigen Speicherpunkt. Wenn für den äußersten Speicherpunkt ein Committed ausgeführt wird, wird für die während dieses Speicherpunkts vorgenommenen Änderungen ein Committed in den Zustand der Datenbank ausgeführt, und die Sitzung beendet die Transaktion.

Die **JetCommitTransaction2-Funktion** wurde im Windows 8 eingeführt.

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*grbit*

Eine Gruppe von Bits, die null oder mehr der in der folgenden Tabelle aufgeführten Werte angeben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitCommitLazyFlush</p> | <p>Für die Transaktion wird normalerweise ein Committed ausgeführt, aber diese API wartet nicht, bis die Transaktion in die Transaktionsprotokolldatei geleert wird, bevor sie an den Aufrufer zurückkehrt. Dadurch wird die Dauer eines Commit-Vorgangs auf Kosten der Dauerhaftigkeit drastisch reduziert. Jede Transaktion, die vor einem Absturz nicht in das Protokoll geleert wird, wird während der Absturzwiederherstellung beim nächsten Aufruf der <a href="gg294068(v=exchg.10).md">JetInit-Funktion automatisch</a> abgebrochen.</p><p>Wenn JET_bitWaitLastLevel0Commit oder JET_bitWaitAllLevel0Commit angegeben werden, wird diese Option ignoriert.</p><p>Wenn dieser Aufruf von <strong>JetCommitTransaction2</strong> nicht mit dem ersten Aufruf der <a href="gg294083(v=exchg.10).md">JetBeginTransaction-Funktion</a> für diese Sitzung überein passt, wird diese Option ignoriert. Dies liegt daran, dass die letzte Aktion, die auf dem äußersten Speicherpunkt ausgeführt wird, der bestimmende Faktor ist, ob die gesamte Transaktion tatsächlich auf den Datenträger ausgeführt wird.</p> | 
| <p>JET_bitWaitAllLevel0Commit</p> | <p>Alle Transaktionen, für die zuvor ein Committed von einer Sitzung ausgeführt wurde, die noch nicht in die Transaktionsprotokolldatei geleert wurden, werden sofort geleert. Diese API wartet, bis die Transaktionen geleert wurden, bevor sie zum Aufrufer zurückkehrt.</p><p>Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</p><p>Diese Option kann nicht in Kombination mit einer anderen Option verwendet werden.</p><p>Diese Option ist in Versionen des Betriebssystems Windows Server ab Windows Server 2003 verfügbar.</p> | 
| <p>JET_bitWaitLastLevel0Commit</p> | <p>Wenn die Sitzung zuvor transaktionen ausgeführt hat und sie noch nicht in die Transaktionsprotokolldatei geleert wurden, sollten sie sofort geleert werden. Diese API wartet, bis die Transaktionen geleert wurden, bevor sie zum Aufrufer zurückkehrt. Dies ist nützlich, wenn die Anwendung zuvor mehrere Transaktionen mithilfe von JET_bitCommitLazyFlush und nun alle transaktionen auf den Datenträger leeren möchte.</p><p>Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</p><p>Diese Option kann nicht in Kombination mit einer anderen Option verwendet werden.</p> | 



*cmsecDurableCommit*

Die Dauer für den Commit einer verzögerten Transaktion.

*pCommitID*

Die Commit-ID, die diesem Commitdatensatz zugeordnet ist.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der in der folgenden Tabelle aufgeführten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs der <a href="gg269240(v=exchg.10).md">JetStopService-Funktion beendet</a> wurden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von Versionen des Betriebssystems zurückgegeben, Windows xp ab Windows xp.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Eine der angeforderten Optionen war ungültig oder nicht implementiert. Dieser Fehler wird von der <strong>JetCommitTransaction2-Funktion</strong> zurückgegeben, wenn Folgendes auftritt:</p><ul><li><p>Ein <em>ungültiges Grbit</em> wird angegeben.</p></li><li><p>JET_bitWaitLastLevel0Commit wurde in Kombination mit einem anderen <em>Grbit angegeben.</em></p></li><li><p>JET_bitWaitAllLevel0Commit wurde in Kombination mit einem anderen <em>Grbit angegeben.</em></p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Der Vorgang ist fehlgeschlagen, da sich die gegebene Sitzung nicht in einer Transaktion befindet.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p><p>Dieser Fehler wird nur von Versionen des Betriebssystems zurückgegeben, Windows xp ab Windows xp.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg werden alle Änderungen, die während des aktuellen Speicherpunkts für die bestimmte Sitzung an der Datenbank vorgenommen wurden, mit einem Committed abgeschlossen, und dieser Speicherpunkt wird beendet. Wenn der letzte Speicherpunkt für die Sitzung beendet wurde, wird die Transaktion optional in die Transaktionsprotokolldatei geleert, und die Sitzung beendet die Transaktion.

Bei einem Fehler bleibt der Transaktionszustand der Sitzung unverändert. Es erfolgt keine Änderung des Datenbankstatus. Die Anwendung sollte die [JetRollback-Funktion aufrufen,](./jetrollback-function.md) um die Transaktion zu abbrechen.

#### <a name="remarks"></a>Hinweise

Es muss einen Aufruf von **JetCommitTransaction2** oder [JetRollback](./jetrollback-function.md) geben, damit jeder Aufruf von [JetBeginTransaction](./jetbegintransaction-function.md) für eine bestimmte Sitzung übereinstimmen kann.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2012.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
