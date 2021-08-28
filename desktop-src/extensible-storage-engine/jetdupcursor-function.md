---
description: Weitere Informationen finden Sie unter JetDupCursor-Funktion.
title: JetDupCursor-Funktion
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a96f93357bc3df143fa63ed690295e40980cfc94
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472656"
---
# <a name="jetdupcursor-function"></a>JetDupCursor-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdupcursor-function"></a>JetDupCursor-Funktion

Die **JetDupCursor-Funktion** dupliziert einen geöffneten Cursor und gibt ein Handle an den duplizierten Cursor zurück. Wenn der cursor, der dupliziert wurde, ein schreibgeschützter Cursor war, ist der duplizierte Cursor auch ein schreibgeschützter Cursor. Jeder Zustand im Zusammenhang mit der Konstruktion eines Suchschlüssels oder dem Aktualisieren eines Datensatzes wird nicht in den duplizierten Cursor kopiert. Darüber hinaus wird die Position des ursprünglichen Cursors nicht im duplizierten Cursor dupliziert. Der duplizierte Cursor wird immer für den gruppierten Index geöffnet, und seine Position befindet sich immer in der ersten Zeile der Tabelle.

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*Ptableid*

Zeiger auf *tableid*.

*grbit*

Für die zukünftige Verwendung reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Es sind keine Cursorressourcen verfügbar.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird *ptableid* auf einen duplizierten Cursor festgelegt.

Bei einem Fehler werden keine Änderungen vorgenommen. Der Status von *tableid* bleibt unverändert.

#### <a name="remarks"></a>Hinweise

Der duplizierte Cursor hat nicht den gesamten Cursorzustand kopiert. Die Position des duplizierten Cursors, einschließlich des aktuellen Indexes, ist in der Regel anders als der gegebene Cursor. Der duplizierte Cursor wird immer für den gruppierten Index und für die erste Zeile in der Tabelle zurückgegeben. Wenn die Tabelle leer ist, befindet sich der duplizierte Cursor nicht in einer Zeile.

Tabellen, die mit **JetDupCursor geöffnet wurden,** sollten normalerweise mit [JetCloseTable geschlossen werden.](./jetclosetable-function.md) Die Ausnahme von dieser Regel tritt auf, wenn **JetDupCursor** in einer Transaktion aufgerufen wird und für die Transaktion ein Rollback ausgeführt wird (mit [JetRollback](./jetrollback-function.md)). Beim Roll back einer Transaktion wird der Cursor automatisch geschlossen. In diesem Fall ist es ein Fehler, die Tabelle mit [JetCloseTable zu schließen.](./jetclosetable-function.md)

Die Anzahl der Tabellen, die gleichzeitig geöffnet werden können, wird direkt [von](./resource-parameters.md)JET_paramMaxOpenTables. Weitere [Informationen finden Sie unter Systemparameter.](./extensible-storage-engine-system-parameters.md)

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
