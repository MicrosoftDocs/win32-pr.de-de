---
description: 'Weitere Informationen zu: jetsetindexrange-Funktion'
title: JetSetIndexRange-Funktion
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 883085633bebf25180c82f0f8917f6fa31fe7304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214755"
---
# <a name="jetsetindexrange-function"></a>JetSetIndexRange-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetindexrange-function"></a>JetSetIndexRange-Funktion

Die **jetsetindexrange** -Funktion schränkt vorübergehend den Satz von Indexeinträgen ein, den der Cursor mithilfe von [jetmove](./jetmove-function.md) durchlaufen kann, beginnend mit dem aktuellen Index Eintrag und endet mit dem Index Eintrag, der mit den Suchkriterien übereinstimmt, die durch den Suchschlüssel in diesem Cursor und den angegebenen gebundenen Kriterien festgelegt wurden. Ein Suchschlüssel muss zuvor mithilfe von [jetmakekey](./jetmakekey-function.md)erstellt worden sein.

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*tableidsrc*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*grbit*

Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten:

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
<td><p>JET_bitRangeInclusive</p></td>
<td><p>Diese Option gibt die Begrenzungs Kriterien des Index Bereichs an. Wenn diese Option vorhanden ist, gibt diese Option an, dass die Beschränkung des Index Bereichs inklusiv ist. Wenn diese Option nicht vorhanden ist, gibt diese Option an, dass die Beschränkung des Index Bereichs exklusiv ist. Wenn das Limit des Index Bereichs inklusiv ist, werden alle Indexeinträge, die genau mit den Suchkriterien übereinstimmen, in den Bereich eingeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRangeInstantDuration</p></td>
<td><p>Mit dieser Option wird angefordert, dass der Index Bereich entfernt wird, sobald er erstellt wurde. Alle anderen Aspekte des Vorgangs bleiben unverändert. Dies ist hilfreich, um zu testen, ob Indexeinträge vorhanden sind, die mit den Suchkriterien übereinstimmen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRangeRemove</p></td>
<td><p>Mit dieser Option wird angefordert, dass ein vorhandener Index Bereich im Cursor abgebrochen wird. Nachdem der Index Bereich abgebrochen wurde, kann er über das Ende des Index Bereichs mithilfe von <a href="gg294117(v=exchg.10).md">jetmove</a>verschoben werden. Wenn ein Index Bereich nicht bereits in Kraft ist, schlägt <strong>jetsetindexrange</strong> mit JET_errInvalidOperation fehl.</p>
<p>Wenn diese Option angegeben wird, werden alle anderen Optionen ignoriert.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRangeUpperLimit</p></td>
<td><p>Wenn diese Option verwendet wird, stellt der Suchschlüssel im Cursor die Suchkriterien für den Index Eintrag dar, der am Ende des Indexes liegt, der mit dem Index Bereich übereinstimmt. Der Index Bereich wird zwischen der aktuellen Position des Cursors und diesem Index Eintrag festgelegt, sodass alle Übereinstimmungen gefunden werden können, indem Sie den Index mithilfe von <a href="gg294117(v=exchg.10).md">jetmove</a> mit JET_MoveNext oder einem positiven Offset durchlaufen.</p>
<p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde, indem eine Platzhalter Option verwendet wurde, um Indexeinträge zu suchen, die dem Anfang des Indexes am nächsten liegen.</p>
<p>Wenn diese Option weggelassen wird, stellt der Suchschlüssel im Cursor die Suchkriterien für den Index Eintrag dar, der am Anfang des Indexes liegt, der mit dem Index Bereich übereinstimmt. Der Index Bereich wird zwischen der aktuellen Position des Cursors und diesem Index Eintrag festgelegt, sodass alle Übereinstimmungen gefunden werden können, indem Sie mithilfe von <a href="gg294117(v=exchg.10).md">jetmove</a> mit JET_MovePrevious oder einem negativen Offset auf den Index zurückgehen.</p>
<p>Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel auszulassen, der mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde, indem eine Platzhalter Option verwendet wurde, um Indexeinträge zu suchen, die dem Ende des Indexes am nächsten sind.</p></td>
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
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p>
<p>Für <strong>jetsetindexrange</strong>bedeutet dies, dass entweder ein vorhandener Index Bereich abgebrochen wurde oder dass mindestens ein Index Eintrag innerhalb des Index Bereichs vorhanden ist.</p></td>
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
<td><p>JET_errInvalidOperation</p></td>
<td><p>Dieser Fehler wird von <strong>jetsetindexrange</strong> zurückgegeben, wenn JET_bitRangeRemove angegeben wurde und kein Index Bereich in Kraft war.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyNotMade</p></td>
<td><p>Es ist kein aktueller Suchschlüssel für den Cursor vorhanden. <strong>Jetsetindexrange</strong> erfordert, dass der Cursor über einen gültigen Suchschlüssel verfügt, da er diesen für die Suchkriterien verwendet, die zum Suchen von Indexeinträgen verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>Es ist kein aktueller Index für den Cursor vorhanden. Dies geschieht für <strong>jetsetindexrange</strong> , wenn sich der Cursor auf dem gruppierten Index einer Tabelle befindet. es wurde kein primärer Index definiert. Das Festlegen eines Index Bereichs über einen solchen Index wird nicht unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Dieser Fehler wird von <strong>jetsetindexrange</strong> zurückgegeben, um anzugeben, dass innerhalb des Index Bereichs keine Indexeinträge vorhanden sind.</p></td>
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
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p>Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Wenn JET_bitRangeRemove angegeben wird, wird der derzeit in Kraft gelegte Index Bereich abgebrochen. Wenn JET_bitRangeRemove nicht angegeben ist und JET_bitRangeInstantDuration angegeben ist, ist kein Index Bereich in Kraft. Wenn weder JET_bitRangeRemove noch JET_bitRangeInstantDuration angegeben ist, ist ein neuer Index Bereich in Kraft. Dieser Index Bereich schränkt temporär den Satz der Indexeinträge ein, die der Cursor mithilfe von [jetmove](./jetmove-function.md) durchlaufen kann, beginnend mit dem aktuellen Index Eintrag und endet mit dem Index Eintrag, der mit den Suchkriterien übereinstimmt. Die Position des Cursors bleibt unverändert. Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht. Es erfolgt keine Änderung des Daten Bank Status.

Bei einem Fehler wird kein Index Bereich wirksam, wenn JET_errNoCurrentRecord nicht zurückgegeben wird. Wenn JET_errNoCurrentRecord zurückgegeben wird, ist ein neuer Index Bereich wirksam. Dieser Index Bereich schränkt temporär den Satz der Indexeinträge ein, die der Cursor mithilfe von [jetmove](./jetmove-function.md) durchlaufen kann, beginnend mit dem aktuellen Index Eintrag und endet mit dem Index Eintrag, der mit den Suchkriterien übereinstimmt. Die Position des Cursors bleibt unverändert. Wenn JET_errNoCurrentRecord zurückgegeben wurde und ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Ein Index Bereich ist flüchtig und wird automatisch abgebrochen, wenn eine andere Navigation als [jetmove](./jetmove-function.md) für den Cursor ausgeführt wird.

Index Bereiche funktionieren nur in einer Richtung. Wenn eine Obergrenze festgelegt wird, wird nur Vorwärtsbewegung mithilfe von [jetmove](./jetmove-function.md) mit JET_MoveNext oder ein positiver Offset verhindert, sobald das Ende des Index Bereichs erreicht wurde. Es ist weiterhin möglich, den Index Bereich in diesem Fall mithilfe von [jetmove](./jetmove-function.md) mit JET_MovePrevious oder einem negativen Offset zu belassen. Eine analoge Situation tritt bei einer niedrigeren Grenze auf.

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
[Jetmove](./jetmove-function.md)  
[Jetsetindexrange]()  
[Jetstopservice](./jetstopservice-function.md)
