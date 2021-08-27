---
description: Weitere Informationen finden Sie unter JetRollback-Funktion.
title: JetRollback-Funktion
TOCTitle: JetRollback Function
ms:assetid: 685c51f4-8fe4-47cc-8a8e-c42014431b8b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269273(v=EXCHG.10)
ms:contentKeyID: 32765575
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRollback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e23bd408ec88109a0f77635ac53e89003df9a992
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985553"
---
# <a name="jetrollback-function"></a>JetRollback-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetrollback-function"></a>JetRollback-Funktion

Die **JetRollback-Funktion** rückgängig gemachte Änderungen am Zustand der Datenbank und kehrt zum letzten Speicherpunkt zurück. **JetRollback** schließt auch alle Cursor, die während des Speicherpunkts geöffnet wurden. Wenn der äußerste Speicherpunkt rückgängig gemacht wird, beendet die Sitzung die Transaktion.

```cpp
    JET_ERR JET_API JetRollback(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten:


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitRollbackAll</p> | <p>Diese Option fordert an, dass alle Änderungen, die während aller Speicherpunkte am Zustand der Datenbank vorgenommen wurden, rückgängig gemacht werden. Dies führt dazu, dass die Sitzung die Transaktion beendet.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Der Vorgang ist fehlgeschlagen, da sich die gegebene Sitzung nicht in einer Transaktion befindet.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRollbackError</p> | <p>Aufgrund eines schwerwiegenden Fehlers konnte kein Rollback für die Änderungen vorgenommen werden.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg werden alle Änderungen, die während des aktuellen Speicherpunkts für die bestimmte Sitzung an der Datenbank vorgenommen wurden, rückgängig gemacht, und dieser Speicherpunkt wird beendet. Wenn der letzte Speicherpunkt für die Sitzung beendet wurde, beendet die Sitzung die Transaktion.

Bei einem Fehler bleibt der Transaktionszustand der Sitzung unverändert. Es erfolgt keine Änderung des Datenbankstatus. Ein Fehler während des Rollbacks wird als schwerwiegender Datenbankfehler betrachtet.

#### <a name="remarks"></a>Bemerkungen

Es muss einen Aufruf von [JetCommitTransaction oder](./jetcommittransaction-function.md) **JetRollback** geben, damit jeder Aufruf von [JetBeginTransaction](./jetbegintransaction-function.md) für eine bestimmte Sitzung übereinstimmen kann.

Wenn cursors während eines Speicherpunkts geöffnet wurden (z. B. [mit JetOpenTable),](./jetopentable-function.md)der zurückgesetzt wird, wird dieser Cursor geschlossen.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)
