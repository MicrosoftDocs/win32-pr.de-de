---
description: 'Weitere Informationen zu: JetSeek-Funktion'
title: JetSeek-Funktion
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c386ae3af5353b95d9d1d3c67df4d680c52bff68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360827"
---
# <a name="jetseek-function"></a>JetSeek-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetseek-function"></a>JetSeek-Funktion

Die **JetSeek** -Funktion positioniert einen Cursor effizient auf einen Index Eintrag, der mit den Suchkriterien übereinstimmt, die durch den Suchschlüssel in diesem Cursor und die angegebene Ungleichheit festgelegt wurden. Ein Suchschlüssel muss zuvor mithilfe von [jetmakekey](./jetmakekey-function.md)erstellt worden sein.

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*grbit*

Eine Gruppe von Bits, die die Optionen enthalten, die für diesen-Befehl verwendet werden sollen. *Grbit* darf nicht NULL sein und muss mindestens einen der Werte enthalten, die in der folgenden Tabelle aufgeführt sind.

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
<td><p>JET_bitCheckUniqueness</p></td>
<td><p>Ein spezieller Fehlercode, der JET_wrnUniqueKey, wird zurückgegeben, wenn er mit einer kostengünstigen Bestimmung feststellen kann, dass es genau einen Index Eintrag gibt, der mit dem Suchschlüssel übereinstimmt.</p>
<p>Diese Option wird ignoriert, es sei denn, JET_bitSeekEQ ebenfalls angegeben wird.</p>
<p>Diese Option ist nur für Windows Server 2003 und spätere Versionen verfügbar.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekEQ</p></td>
<td><p>Der Cursor wird am Index Eintrag positioniert, der am nächsten am Anfang des Indexes liegt, der exakt mit dem Suchschlüssel übereinstimmt. Der Index Anfang ist der Index Eintrag, der beim Verschieben in den ersten Datensatz in diesem Index gefunden wird. Der Index Anfang ist nicht mit dem unteren Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</p>
<p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe einer Platzhalter Option mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSeekGE</p></td>
<td><p>Der Cursor wird am Index Eintrag positioniert, der dem Anfang des Indexes am nächsten liegt, der größer als oder gleich einem Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt. Der Index Anfang ist der Index Eintrag, der beim Verschieben in den ersten Datensatz in diesem Index gefunden wird. Der Index Anfang ist nicht mit dem unteren Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</p>
<p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde, indem eine Platzhalter Option verwendet wurde, um Indexeinträge zu suchen, die dem Ende des Indexes am nächsten sind.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekGT</p></td>
<td><p>Der Cursor wird am Index Eintrag positioniert, der dem Anfang des Indexes am nächsten liegt, der größer als ein Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt. Der Index Anfang ist der Index Eintrag, der beim Verschieben in den ersten Datensatz in diesem Index gefunden wird. Der Index Anfang ist nicht mit dem unteren Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</p>
<p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde, indem eine Platzhalter Option verwendet wurde, um Indexeinträge zu suchen, die dem Anfang des Indexes am nächsten liegen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSeekLE</p></td>
<td><p>Der Cursor wird am Index Eintrag positioniert, der am nächsten am Ende des Indexes liegt, der kleiner oder gleich einem Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt. Das Ende des Indexes ist der Index Eintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wurde. Das Ende des Indexes ist nicht mit dem hohen Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</p>
<p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde, indem eine Platzhalter Option verwendet wurde, um Indexeinträge zu suchen, die dem Anfang des Indexes am nächsten liegen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekLT</p></td>
<td><p>Der Cursor wird am Index Eintrag positioniert, der am nächsten am Ende des Indexes liegt, der kleiner als ein Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt. Das Ende des Indexes ist der Index Eintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wurde. Das Ende des Indexes ist nicht mit dem hohen Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</p>
<p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde, indem eine Platzhalter Option verwendet wurde, um Indexeinträge zu suchen, die dem Ende des Indexes am nächsten sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIndexRange</p></td>
<td><p>Ein Index Bereich wird automatisch für alle Schlüssel eingerichtet, die exakt mit dem Suchschlüssel übereinstimmen. Der resultierende Index Bereich ist identisch mit einem Index Bereich, der andernfalls durch einen Aufrufen von <a href="gg294112(v=exchg.10).md">jetsetindexrange</a> mit den Optionen JET_bitRangeInclusive und JET_bitRangeUpperLimit erstellt worden wäre. Weitere Informationen finden Sie unter <a href="gg294112(v=exchg.10).md">jetsetindexrange</a> .</p>
<p>Dies ist eine bequeme Methode zum Ermitteln aller Indexeinträge, die denselben Suchkriterien entsprechen.</p>
<p>Diese Option wird ignoriert, es sei denn, JET_bitSeekEQ ebenfalls angegeben wird.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion ermöglicht die Rückgabe von [JET_ERRs](./jet-err.md) , die in dieser API definiert sind. Weitere Informationen zu Jet-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p>
<p>Für <strong>JetSeek</strong>bedeutet dies, dass ein Index Eintrag gefunden wurde, der genau mit den Suchkriterien übereinstimmt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p>Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyNotMade</p></td>
<td><p>Es ist kein aktueller Suchschlüssel für den Cursor vorhanden. <strong>JetSeek</strong> erfordert, dass der Cursor über einen gültigen Suchschlüssel verfügt, da er diesen für die Suchkriterien verwendet, die zum Suchen von Indexeinträgen verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNotFound</p></td>
<td><p>Es wurde kein Index Eintrag gefunden, der mit den Suchkriterien übereinstimmt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSeekNotEqual</p></td>
<td><p>Es wurde ein Index Eintrag gefunden, der mit den Suchkriterien übereinstimmt. Dieser Index Eintrag war jedoch keine genaue Entsprechung.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p>Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnUniqueKey</p></td>
<td><p>Es wurde genau ein Index Eintrag gefunden, der genau mit den Suchkriterien übereinstimmt. Dieser Fehler wird nur zurückgegeben, wenn JET_bitSeekCheckUniqueness angegeben wurde, und es war sehr billig, zu ermitteln, ob der übereinstimmende Index Eintrag der einzige Index Eintrag war, der genau mit den Suchkriterien übereinstimmt.</p>
<p>Dieser Fehler wird nur von Windows Server 2003 und höheren Versionen zurückgegeben.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der Cursor an einem Index Eintrag positioniert, der den Suchkriterien entspricht. Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen. Wenn ein Index Bereich wirksam ist, wird dieser Index Bereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht. Es erfolgt keine Änderung des Daten Bank Status. Wenn mehrere Indexeinträge denselben Wert aufweisen, wird der am Anfang des Indexes am nächsten liegenden Eintrag immer ausgewählt.

Bei einem Fehler bleibt die Position des Cursors unverändert, es sei denn, JET_errRecordNotFound zurückgegeben wurde. In diesem Fall wird der Cursor positioniert, wo der Index Eintrag, der mit den Suchkriterien übereinstimmt, die durch den Suchschlüssel in diesem Cursor und der angegebenen Ungleichheit angegeben wurden, wäre. Der Cursor kann relativ zu dieser Position verschoben werden, befindet sich jedoch noch nicht in einem gültigen Index Eintrag. Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen. Wenn ein Index Bereich wirksam ist, wird dieser Index Bereich abgebrochen. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht. Es erfolgt keine Änderung des Daten Bank Status.

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetmakekey](./jetmakekey-function.md)  
[Jetsetindexrange](./jetsetindexrange-function.md)  
[Jetstopservice](./jetstopservice-function.md)
