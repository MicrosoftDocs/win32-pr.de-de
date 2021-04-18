---
description: 'Weitere Informationen über: jetdupcursor-Funktion'
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
ms.openlocfilehash: 590b9b08c5386aaf1cd2dd541ac496a5fa0871d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366148"
---
# <a name="jetdupcursor-function"></a>JetDupCursor-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdupcursor-function"></a>JetDupCursor-Funktion

Die **jetdupcursor** -Funktion dupliziert einen geöffneten Cursor und gibt ein Handle für den duplizierten Cursor zurück. Wenn der duplizierte Cursor ein Schreib geschützter Cursor war, ist der duplizierte Cursor ebenfalls ein Schreib geschützter Cursor. Jeder Status im Zusammenhang mit dem Erstellen eines Suchschlüssels oder dem Aktualisieren eines Datensatzes wird nicht in den doppelten Cursor kopiert. Außerdem wird der Speicherort des ursprünglichen Cursors nicht in den doppelten Cursor dupliziert. Der doppelte Cursor wird immer auf dem gruppierten Index geöffnet, und sein Speicherort ist immer in der ersten Zeile der Tabelle.

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*pTableID*

Zeiger auf *TableID*.

*grbit*

Für die zukünftige Verwendung reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Es sind keine verfügbaren Cursor Ressourcen vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird *pTableID* auf einen doppelten Cursor festgelegt.

Bei einem Fehler werden keine Änderungen vorgenommen. Der Status von *TableID* ist unverändert.

#### <a name="remarks"></a>Bemerkungen

Beim duplizierten Cursor ist nicht der gesamte Cursor Zustand kopiert. Der Speicherort des duplizierten Cursors, einschließlich des aktuellen Indexes, unterscheidet sich in der Regel vom angegebenen Cursor. Der doppelte Cursor wird immer für den gruppierten Index und für die erste Zeile in der Tabelle zurückgegeben. Wenn die Tabelle leer ist, befindet sich der duplizierte Cursor nicht in einer Zeile.

Tabellen, die mit **jetdupcursor** geöffnet werden, sollten normalerweise mit [jetclosetable](./jetclosetable-function.md)geschlossen werden. Die Ausnahme von dieser Regel tritt auf, wenn **jetdupcursor** in einer Transaktion aufgerufen wird und für die Transaktion ein Rollback ausgeführt wird (mit [jetrollback](./jetrollback-function.md)). Beim Rollback einer Transaktion wird der Cursor automatisch geschlossen. In diesem Fall ist es ein Fehler, die Tabelle mit [jetclosetable](./jetclosetable-function.md)zu schließen.

Die Anzahl der Tabellen, die gleichzeitig geöffnet werden können, wird von [JET_paramMaxOpenTables](./resource-parameters.md)direkt beeinflusst. Weitere Informationen finden Sie unter [System Parameter](./extensible-storage-engine-system-parameters.md) .

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetclosetable](./jetclosetable-function.md)  
[Jetrollback](./jetrollback-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
