---
description: 'Weitere Informationen zu: JetDupCursor-Funktion'
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
ms.openlocfilehash: 009b84837895ce13f63cc37e4b5b152f4274ee62
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985883"
---
# <a name="jetdupcursor-function"></a>JetDupCursor-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdupcursor-function"></a>JetDupCursor-Funktion

Die **JetDupCursor-Funktion** dupliziert einen geöffneten Cursor und gibt ein Handle an den duplizierten Cursor zurück. Wenn der cursor, der dupliziert wurde, ein schreibgeschützter Cursor war, ist der duplizierte Cursor auch ein schreibgeschützter Cursor. Alle Zustände im Zusammenhang mit der Erstellung eines Suchschlüssels oder dem Aktualisieren eines Datensatzes werden nicht in den doppelten Cursor kopiert. Darüber hinaus wird die Position des ursprünglichen Cursors nicht in den duplizierten Cursor dupliziert. Der duplizierte Cursor wird immer für den gruppierten Index geöffnet, und seine Position befindet sich immer in der ersten Zeile der Tabelle.

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

Zeiger auf *tableid.*

*grbit*

Für die zukünftige Verwendung reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Es sind keine Cursorressourcen verfügbar.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird *ptableid* auf einen duplizierten Cursor festgelegt.

Bei einem Fehler werden keine Änderungen vorgenommen. Der Zustand von *tableid* ist unverändert.

#### <a name="remarks"></a>Bemerkungen

Der duplizierte Cursor hat nicht den gesamten Cursorzustand kopiert. Die Position des doppelten Cursors, einschließlich des aktuellen Indexes, unterscheidet sich in der Regel vom angegebenen Cursor. Der duplizierte Cursor wird immer für den gruppierten Index und für die erste Zeile in der Tabelle zurückgegeben. Wenn die Tabelle leer ist, befindet sich der duplizierte Cursor in keiner Zeile.

Tabellen, die mit **JetDupCursor** geöffnet werden, sollten in der Regel mit [JetCloseTable](./jetclosetable-function.md)geschlossen werden. Die Ausnahme von dieser Regel tritt auf, wenn **JetDupCursor** in einer Transaktion aufgerufen wird und für die Transaktion ein Rollback ausgeführt wird (mit [JetRollback](./jetrollback-function.md)). Beim Rollback einer Transaktion wird der Cursor automatisch geschlossen. In diesem Fall ist es ein Fehler, die Tabelle mit [JetCloseTable](./jetclosetable-function.md)zu schließen.

Die Anzahl der Tabellen, die gleichzeitig geöffnet werden können, wird direkt von [JET_paramMaxOpenTables](./resource-parameters.md)beeinflusst. Weitere Informationen finden Sie unter [Systemparameter.](./extensible-storage-engine-system-parameters.md)

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
