---
description: 'Weitere Informationen: jetmove-Funktion'
title: JetMove-Funktion
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e42cb2258d373f8c4edb96309c6db0853eab4fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214383"
---
# <a name="jetmove-function"></a>JetMove-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetmove-function"></a>JetMove-Funktion

Die **jetmove** -Funktion positioniert einen Cursor am Anfang oder Ende eines Indexes und durchläuft die Einträge in diesem Index entweder vorwärts oder rückwärts. Es ist auch möglich, den Cursor auf dem aktuellen Index um eine angegebene Anzahl von Indexeinträgen vorwärts oder rückwärts zu verschieben. Ein anderer Ansatz besteht darin, die Indexeinträge, die mithilfe von **jetmove** aufgezählt werden können, durch das Einrichten eines Index Bereichs auf dem Cursor mithilfe von [jetsetindexrange](./jetsetindexrange-function.md)künstlich einzuschränken.

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*beschäftigen*

Ein beliebiger Offset, der die gewünschte Bewegung des Cursors des aktuellen Indexes angibt.

Zusätzlich zu Standard Offsets kann dieser Parameter auch mit einer der folgenden Optionen festgelegt werden.

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
<td><p>JET_MoveFirst</p></td>
<td><p>Verschiebt den Cursor zum ersten Index Eintrag im Index (sofern vorhanden).</p>
<p><strong>Hinweis</strong>   Der Literalwert "-2147483648" wird verwendet, um diese Option anzugeben. Verwenden Sie diesen Wert nicht als normalen Offset oder unbeabsichtigtes Verhalten.</p></td>
</tr>
<tr class="even">
<td><p>JET_MoveLast</p></td>
<td><p>Verschiebt den Cursor auf den letzten Index Eintrag im Index (sofern vorhanden).</p>
<p><strong>Hinweis</strong>   Der Literalwert 2147483647 wird verwendet, um diese Option anzugeben. Verwenden Sie diesen Wert nicht als normalen Offset oder unbeabsichtigtes Verhalten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_MoveNext</p></td>
<td><p>Verschiebt den Cursor zum nächsten Index Eintrag im Index (sofern vorhanden). Dieser Wert ist genau gleich dem normalen Offset von + 1.</p></td>
</tr>
<tr class="even">
<td><p>JET_MovePrevious</p></td>
<td><p>Verschiebt den Cursor zum vorherigen Index Eintrag im Index (sofern vorhanden).</p>
<p>Dieser Wert ist genau gleich dem normalen Offset von-1 oder 0 (null).</p>
<p>Der Cursor bleibt an der aktuellen logischen Position, und das vorhanden sein des Index Eintrags, der dieser logischen Position entspricht, wird getestet.</p></td>
</tr>
</tbody>
</table>


*grbit*

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angeben.

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
<td><p>JET_bitMoveKeyNE</p></td>
<td><p>Verschiebt den Cursor um die Anzahl der Indexeinträge, die erforderlich sind, um die angeforderte Anzahl von Index Schlüsselwerten im Index zu überspringen. Dies hat den Effekt, dass Indexeinträge mit doppelten Schlüsselwerten in einem einzelnen Index Eintrag reduziert werden. Normalerweise verschiebt ein Offset den Cursor um die angegebene Anzahl von Indexeinträgen, unabhängig von den Schlüsselwerten.</p></td>
</tr>
</tbody>
</table>


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
<td><p>Der Vorgang wurde erfolgreich abgeschlossen. Für <strong>jetmove</strong>bedeutet dies, dass ein Index Eintrag am angeforderten Speicherort oder Offset des aktuellen Indexes gefunden wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor befindet sich derzeit nicht auf einem Index Eintrag. Für <strong>jetmove</strong>bedeutet dies, dass am angeforderten Speicherort oder Offset des aktuellen Indexes kein Index Eintrag gefunden wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Der Cursor ist zurzeit logisch auf einem Index Eintrag positioniert, der einem Datensatz entspricht, der gelöscht wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird der Cursor an einem Index Eintrag positioniert, der mit dem angeforderten Speicherort oder Offset übereinstimmt. Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen. Wenn ein Index Bereich wirksam ist und JET_MoveFirst oder JET_MoveLast angegeben wurde, wird dieser Index Bereich abgebrochen. Es erfolgt keine Änderung des Daten Bank Status.

Wenn diese Funktion fehlschlägt, bleibt die Position des Cursors unverändert, es sei denn, JET_errNoCurrentRecord zurückgegeben wurde. In diesem Fall wird der Cursor positioniert, wo der Index Eintrag, der mit dem angeforderten Speicherort oder Offset übereinstimmt, wäre. Der Cursor kann relativ zu dieser Position verschoben werden, befindet sich jedoch noch nicht in einem gültigen Index Eintrag. Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen. Wenn ein Index Bereich wirksam ist und JET_MoveFirst oder JET_MoveLast angegeben wurde, wird dieser Index Bereich abgebrochen. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Ein Cursor kann mithilfe von **jetmove**, vor der ersten und nach der letzten, an zwei Sonderpositionen verschoben werden. Wenn sich der Cursor auf dem ersten Index Eintrag in der Tabelle befindet und **jetmove** mit JET_MovePrevious aufgerufen wird, schlägt der Aufruf mit JET_errNoCurrentRecord fehl, und der Cursor wird logisch vor dem ersten Eintrag im Index positioniert. Diese logische Position wird auch dann beibehalten, wenn vor dem ersten Eintrag im Index ein anderer Index Eintrag eingefügt wird. Eine analoge Situation tritt für den letzten relativ zum Ende des Indexes ein. Vor der ersten und nach der letzten sind besonders nützlich, wenn Sie einen Bereich von Indexeinträgen einrichten, die mithilfe von **jetmove** durchlaufen werden sollen. dabei wird ein iteratormodell verwendet, das erwartet, dass immer zum nächsten (oder vorherigen) Element wechselt, bevor dieses Element verwendet wird.

Der Satz von Indexeinträgen, der von **jetmove** besucht werden kann, kann durch das Einrichten eines Index Bereichs auf dem Cursor eingeschränkt werden. Dies ist nützlich für Anwendungen, die einen Satz von Indexeinträgen auflisten, die einfache Kriterien erfüllen, die über ein paar von Suchschlüsseln ausgedrückt werden können, die für diesen Index erstellt wurden. Weitere Informationen finden Sie unter [jetsetindexrange](./jetsetindexrange-function.md).

In Releases vor Windows Server 2003 SP1 liegt ein Problem in **jetmove** vor, das in einigen bestimmten Fällen auftritt, das sich auf die korrekte Durchsetzung eines Index Bereichs auswirkt, wie von der [jetsetindexrange](./jetsetindexrange-function.md) -Funktion festgelegt. Wenn sich der Cursor derzeit vor dem ersten Index Eintrag befindet und ein Index Bereich mit einer Obergrenze festgelegt ist, die kleiner als der erste Index Eintrag ist, wird der nächste **jetmove** -Befehl fälschlicherweise zu diesem Index Eintrag gewechselt, anstatt wie erwartet mit JET_errNoCurrentRecord. Der gleiche Fehler tritt für die analoge Situation auf, beginnend ab dem Index Ende. Diese Situation kann in einer Anwendung auftreten, die einen Index Bereich einrichtet und mithilfe eines Iterators navigiert, der erwartet, dass vor dem ersten Index Eintrag begonnen wird, der ein Member der aufzuzählenden Menge von Einträgen ist, anstatt mit dem ersten Index Eintrag dieses Satzes zu beginnen. Diese Situation tritt auch in dem analogen Fall auf, beginnend ab dem Ende des Indexes. Die Problem Umgehung besteht darin, dass die Anwendung manuell prüft, ob sich der erfassten Index Eintrag innerhalb des Index Bereichs befindet, indem der Schlüssel für den aktuellen Index Eintrag (abgerufen mit [jetretrievekey](./jetretrievekey-function.md)) mit dem Schlüssel verglichen wird, der das Ende des aktuellen Index Bereichs darstellt (abgerufen mit [jetretrievekey](./jetretrievekey-function.md) mithilfe JET_bitRetrieveCopy).

Es ist wichtig, bei der Übergabe berechneter Offsets an **jetmove** vorsichtig zu sein. Wenn der berechnete Offset kleiner als oder gleich JET_MoveFirst ist, muss dieser Offset in mehrere Teile aufgeteilt werden, von denen jeder separat an **jetmove** übermittelt wird, aber innerhalb einer einzelnen Transaktion, um den gewünschten Effekt zu erzielen. Das gleiche gilt für Offsets, die größer oder gleich JET_MoveNext sind. Es ist unwahrscheinlich, dass eine Anwendung diese in der realen Welt durchlaufen würde, aber es ist gut, bei der unterschiedlichen Semantik von JET_MoveFirst und JET_MoveLast von einem normalen Offset eine Verteidigung gegen diesen Fall zu haben.

Wenn **jetmove** mit einem sehr großen Offset aufgerufen wird, z. b. wenn der Parameter "cRow" auf 1000 festgelegt ist, durchläuft **jetmove** alle 1000-Indexeinträge, um die endgültige Position zu erreichen. Derzeit bietet die ESE-API keine effiziente Möglichkeit, direkt zu einem bestimmten Index Eintrag zu wechseln, ohne jeden Index Eintrag durchlaufen zu müssen.

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
[Jetretrievekey](./jetretrievekey-function.md)  
[Jetsetindexrange](./jetsetindexrange-function.md)
