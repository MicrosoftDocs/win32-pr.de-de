---
description: Weitere Informationen finden Sie unter JetCommitTransaction-Funktion.
title: JetCommitTransaction-Funktion
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9592c9b596a7794cc130b7ed599b7c8562ff8b2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477626"
---
# <a name="jetcommittransaction-function"></a>JetCommitTransaction-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcommittransaction-function"></a>JetCommitTransaction-Funktion

Die **JetCommitTransaction-Funktion** führt einen Commit für die Änderungen aus, die während des aktuellen Speicherpunkts am Zustand der Datenbank vorgenommen wurden, und migriert sie zum vorherigen Speicherpunkt. Wenn für den äußersten Speicherpunkt ein Committed ausgeführt wird, wird für die während dieses Speicherpunkts vorgenommenen Änderungen ein Committed in den Zustand der Datenbank ausgeführt, und die Sitzung beendet die Transaktion.

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen an geben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitCommitLazyFlush</p> | <p>Für die Transaktion wird normalerweise ein Committed ausgeführt, aber diese API wartet nicht, bis die Transaktion in die Transaktionsprotokolldatei geleert wird, bevor sie an den Aufrufer zurückkehrt. Dadurch wird die Dauer eines Commit-Vorgangs auf Kosten der Dauerhaftigkeit drastisch reduziert. Jede Transaktion, die vor einem Absturz nicht in das Protokoll geleert wird, wird während der Absturzwiederherstellung beim nächsten Aufruf von <a href="gg294068(v=exchg.10).md">JetInit automatisch abgebrochen.</a></p><p>Wenn JET_bitWaitLastLevel0Commit oder JET_bitWaitAllLevel0Commit angegeben werden, wird diese Option ignoriert.</p><p>Wenn dieser Aufruf von <strong>JetCommitTransaction</strong> nicht mit dem ersten Aufruf von <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> für diese Sitzung überein passt, wird diese Option ignoriert. Dies liegt daran, dass die letzte Aktion, die auf dem äußersten Speicherpunkt ausgeführt wird, der bestimmende Faktor ist, ob die gesamte Transaktion tatsächlich auf den Datenträger ausgeführt wird.</p> | 
| <p>JET_bitWaitAllLevel0Commit</p> | <p>Alle Transaktionen, für die zuvor ein Committed von einer Sitzung ausgeführt wurde, die noch nicht in die Transaktionsprotokolldatei geleert wurden, werden sofort geleert. Diese API wartet, bis die Transaktionen geleert wurden, bevor sie zum Aufrufer zurückkehrt.</p><p>Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</p><p>Diese Option kann nicht in Kombination mit einer anderen Option verwendet werden.</p><p>Diese Option ist nur ab Windows Server 2003 verfügbar.</p> | 
| <p>JET_bitWaitLastLevel0Commit</p> | <p>Wenn die Sitzung zuvor transaktionen ausgeführt hat und sie noch nicht in die Transaktionsprotokolldatei geleert wurden, sollten sie sofort geleert werden. Diese API wartet, bis die Transaktionen geleert wurden, bevor sie zum Aufrufer zurückkehrt. Dies ist nützlich, wenn die Anwendung zuvor mehrere Transaktionen mithilfe von JET_bitCommitLazyFlush und nun alle transaktionen auf den Datenträger leeren möchte.</p><p>Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</p><p>Diese Option kann nicht in Kombination mit einer anderen Option verwendet werden.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Eine der angeforderten Optionen war ungültig oder nicht implementiert. Dieser Fehler wird von <strong>JetCommitTransaction zurückgegeben, wenn:</strong></p><ul><li><p>Ein <em>ungültiges Grbit</em> wird angegeben.</p></li><li><p>JET_bitWaitLastLevel0Commit wurde in Kombination mit einem anderen <em>Grbit angegeben.</em></p></li><li><p>JET_bitWaitAllLevel0Commit wurde in Kombination mit einem anderen <em>Grbit angegeben.</em></p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Der Vorgang ist fehlgeschlagen, da sich die gegebene Sitzung nicht in einer Transaktion befindet.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg werden alle Änderungen, die während des aktuellen Speicherpunkts für die bestimmte Sitzung an der Datenbank vorgenommen wurden, mit einem Committed abgeschlossen, und dieser Speicherpunkt wird beendet. Wenn der letzte Speicherpunkt für die Sitzung beendet wurde, wird die Transaktion optional in die Transaktionsprotokolldatei geleert, und die Sitzung beendet die Transaktion.

Bei einem Fehler bleibt der Transaktionszustand der Sitzung unverändert. Es erfolgt keine Änderung des Datenbankstatus. Die Anwendung sollte [JetRollback aufrufen,](./jetrollback-function.md) um die Transaktion zu abbrechen.

#### <a name="remarks"></a>Hinweise

Es muss einen Aufruf von **JetCommitTransaction oder** [JetRollback](./jetrollback-function.md) geben, damit jeder Aufruf von [JetBeginTransaction](./jetbegintransaction-function.md) für eine bestimmte Sitzung übereinstimmen kann.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction]()  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
