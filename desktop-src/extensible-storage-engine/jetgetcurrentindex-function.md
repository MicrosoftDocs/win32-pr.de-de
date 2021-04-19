---
description: 'Weitere Informationen: jetgetcurrentindex-Funktion'
title: Jetgetcurrentindex-Funktion
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3337ddaefbea803a137ad8366d2e3df665bacd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363604"
---
# <a name="jetgetcurrentindex-function"></a>Jetgetcurrentindex-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetcurrentindex-function"></a>Jetgetcurrentindex-Funktion

Die **jetgetcurrentindex** -Funktion bestimmt den Namen des aktuellen Indexes eines angegebenen Cursors. Dieser Name wird auch verwendet, um den Index später mithilfe von [jetsetcurrentindex](./jetsetcurrentindex-function.md)als aktuellen Index erneut auszuwählen. Sie kann auch verwendet werden, um die Eigenschaften dieses Indexes mithilfe von [jetgettableindexinfo](./jetgettableindexinfo-function.md)zu ermitteln.

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*szindexname*

Der Ausgabepuffer, der den Namen des aktuellen Index des Cursors empfängt.

*cchindexname*

Die maximale Größe des Ausgabepuffers in Zeichen.

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
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen, aber der Ausgabepuffer war zu klein, um den gesamten Indexnamen zu empfangen.</p>
<p>Der Ausgabepuffer wurde mit dem gleichen Namen wie der Indexname gefüllt. Wenn der Ausgabepuffer mindestens ein Zeichen lang ist, wird die Zeichenfolge in diesem Ausgabepuffer Null beendet.</p>
<p><strong>Hinweis  </strong> Dieser Fehler wird nicht zurückgegeben, wenn "cchindexname" 0 (null) ist. Weitere Informationen finden Sie im Abschnitt "Hinweise".</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der Name des aktuellen Index des angegebenen Cursors im Ausgabepuffer zurückgegeben. Wenn JET_wrnBufferTruncated zurückgegeben wird, enthält der Ausgabepuffer den Wert des Index namens, der in den bereitgestellten Speicherplatz passt. Wenn der Ausgabepuffer mindestens ein Zeichen lang ist, wird die in diesem Puffer zurückgegebene Zeichenfolge Null beendet. Es erfolgt keine Änderung des Daten Bank Status.

Bei einem Fehler wird der Status des Ausgabepuffers nicht definiert. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Wenn kein aktueller Index für den Cursor vorhanden ist, wird eine leere Zeichenfolge zurückgegeben. Dies kann vorkommen, wenn sich der Cursor auf dem gruppierten Index der Tabelle befindet und kein primärer Index definiert wurde. Dieser Index wird als sequenzieller Index der Tabelle bezeichnet und weist keine Definition auf. Wenn Sie den aktuellen Index auf eine leere Zeichenfolge mithilfe von [jetsetcurrentindex](./jetsetcurrentindex-function.md) festlegen, wird der gruppierte Index unabhängig davon ausgewählt, ob eine primär Index Definition vorhanden ist.

In dieser Funktion gibt es einen wichtigen Fehler, der in allen Releases vorhanden ist. Wenn der Ausgabepuffer zu klein ist, um den gesamten Indexnamen zu empfangen, und der Ausgabepuffer mindestens ein Zeichen lang ist, wird JET_wrnBufferTruncated nicht zurückgegeben. Stattdessen wird JET_errSuccess zurückgegeben. Um dieses Problem zu vermeiden, sollte der Ausgabepuffer immer mindestens JET_cbNameMost + 1 (65) Zeichen lang sein.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jetgetcurrentindexw</strong> (Unicode) und <strong>jetgetcurrentindexa</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetgettableindexinfo](./jetgettableindexinfo-function.md)  
[Jetsetcurrentindex](./jetsetcurrentindex-function.md)
