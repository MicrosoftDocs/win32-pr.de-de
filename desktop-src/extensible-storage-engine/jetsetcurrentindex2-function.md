---
description: 'Weitere Informationen finden Sie hier: JetSetCurrentIndex2-Funktion'
title: JetSetCurrentIndex2-Funktion
TOCTitle: JetSetCurrentIndex2 Function
ms:assetid: da94465e-bd35-45c2-9ccc-1d2e8c34aa9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294110(v=EXCHG.10)
ms:contentKeyID: 32765725
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex2W
- JetSetCurrentIndex2A
- JetSetCurrentIndex2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c95e665b549fff82e0beaaca9682329217ebb0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345470"
---
# <a name="jetsetcurrentindex2-function"></a>JetSetCurrentIndex2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetcurrentindex2-function"></a>JetSetCurrentIndex2-Funktion

Die **JetSetCurrentIndex2** -Funktion legt den aktuellen Index eines Cursors fest, der definiert, welche Datensätze in einer Tabelle für diesen Cursor sichtbar sind, und die Reihenfolge, in der Sie angezeigt werden, indem Sie den Satz von Indexeinträgen auswählen, der zum verfügbar machen dieser Datensätze verwendet wird

```cpp
    JET_ERR JET_API JetSetCurrentIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*szindexname*

Der Name des Indexes, der für den Cursor ausgewählt werden soll.

Wenn dieser Parameter NULL oder eine leere Zeichenfolge ist, wird der gruppierte Index ausgewählt. Wenn ein primärer Index für die Tabelle definiert ist, wird dieser Index ausgewählt, da er mit dem gruppierten Index identisch ist. Wenn kein primärer Index für die Tabelle definiert ist, wird der sequenzielle Index ausgewählt. Der sequenzielle Index hat keine Index Definition. Weitere Informationen finden Sie unter [jetkreateindex](./jetcreateindex-function.md) .

Wenn *pIndexID* nicht NULL ist, wird der Indexname ignoriert, und der Index wird durch die Index-ID ausgewählt.

*grbit*

Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.

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
<td><p>JET_bitMoveFirst</p></td>
<td><p>Diese Option gibt an, dass der Cursor auf dem ersten Eintrag des angegebenen Indexes positioniert werden soll. Wenn der gruppierte Index ausgewählt wird (primärer Index oder sequenzieller Index) und der aktuelle Index ein sekundärer Index ist, wird JET_bitMoveFirst angenommen. Wenn der aktuelle Index ausgewählt wird, wird diese Option ignoriert, und es erfolgt keine Änderung an der Cursorposition.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitNoMove</p></td>
<td><p>Diese Option gibt an, dass der Cursor auf dem Index Eintrag des neuen Indexes positioniert werden soll, der dem Datensatz entspricht, der mit dem Index Eintrag an der aktuellen Position des Cursors auf dem alten Index verknüpft ist.</p>
<p>Wenn die Definition für den neuen Index mindestens eine mehrwertige Schlüssel Spalte enthält, ist der Ziel Index Eintrag mehrdeutig. In diesem Fall wird die angegebene <em>itagsequence</em> verwendet, um auszuwählen, welcher mehrwertige Wert der signifikantesten mehrwertigen Schlüssel Spalte zum Positionieren des Cursors verwendet wird. Es ist nur notwendig, eine einzelne <em>itagsequence</em> zu übergeben, auch wenn es mehrere mehrwertige Schlüssel Spalten gibt, da die Engine nur alle Werte für die signifikanteste mehrwertige Schlüssel Spalte erweitert. Weitere Informationen finden Sie unter <a href="gg294099(v=exchg.10).md">jetkreateingedex</a> .</p>
<p>Wenn JET_bitMoveFirst angegeben wird, wird diese Option ignoriert.</p>
<p>Wenn der aktuelle Index ausgewählt wird, wird diese Option ignoriert, und es erfolgt keine Änderung an der Cursorposition. Wenn dieser Parameter nicht vorhanden ist, wird davon ausgegangen, dass sein Wert JET_bitMoveFirst wird.</p></td>
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
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadItagSequence</p></td>
<td><p>Ein sekundärer Index wird mit der JET_bitNoMove-Option ausgewählt, und es gibt keinen Wert für die erste mehrwertige Schlüssel Spalte in der neuen Definition für den Index, der der angegebenen Sequenznummer entspricht.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p>Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidIndexId</p></td>
<td><p>Der Inhalt der Index-ID war ungültig oder abgelaufen und muss aktualisiert werden. Dies kann für <strong>JetSetCurrentIndex2</strong> vorkommen, wenn:</p>
<ul>
<li><p>pIndexID- &gt; cbStruct weist nicht die erwartete Größe auf (Windows Server 2003 und spätere Releases).</p></li>
<li><p>Die Engine wurde heruntergefahren, seit die Index-ID abgerufen wurde.</p></li>
<li><p>Alle Cursor, die auf die Tabelle verweisen, die den Index enthält, der der Index-ID entspricht, wurden geschlossen, und die Engine hat die Definition für den Index aus dem Schema Cache entfernt.</p></li>
<li><p>Die Index-ID wird mit einem Cursor verwendet, der für die falsche Tabelle geöffnet ist.</p></li>
<li><p>Der Index wurde gelöscht oder ist für die Sitzung noch nicht sichtbar.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Einer der angegebenen Objektnamen war ungültig. Alle Objektnamen müssen mit demselben Regelsatz übereinstimmen. Nachfolgend sind diese Regeln aufgeführt:</p>
<ul>
<li><p>Objektnamen müssen aus ASCII-Zeichen bestehen.</p></li>
<li><p>Objektnamen müssen mindestens ein Zeichen lang sein.</p></li>
<li><p>Objektnamen dürfen nicht mehr als JET_cbNameMost (64) Zeichen lang sein.</p></li>
<li><p>Objektnamen dürfen nicht mit einem Leerzeichen beginnen.</p></li>
<li><p>Objektnamen dürfen keine ASCII-Steuerzeichen (0x00 bis 0x1F) enthalten.</p></li>
<li><p>Objektnamen dürfen keine Ausrufezeichen (!), Punkte (.), linke eckige Klammer ([) oder rechte eckige Klammer (]) enthalten.</p></li>
<li><p>Nach der Validierung wird nur der Teil der Zeichenfolge bis zum ersten Leerzeichen (sofern vorhanden) für den Objektnamen verwendet. Dies bedeutet, dass Objektnamen keine Leerzeichen enthalten dürfen.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dies kann bei <strong>JetSetCurrentIndex2</strong> vorkommen, wenn <em>pIndexID</em> nicht NULL ist und pIndexID- &gt; cbStruct nicht die erwartete Größe aufweist (Windows XP und frühere Versionen).</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Ein sekundärer Index wird mit der JET_bitNoMove-Option ausgewählt, und es gibt keinen Index Eintrag im neuen Index, der dem Datensatz entspricht, der mit dem Index Eintrag an der aktuellen Position des Cursors auf dem alten Index verknüpft ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Die Engine hat den Ressourcenpool erschöpft, der zum Öffnen von Cursorn verwendet wird. Die maximale Anzahl von Cursorn, die zu einem beliebigen Zeitpunkt geöffnet werden können, wird mit <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>gesteuert. Weitere Informationen finden Sie unter <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> . Dies kann bei <strong>JetSetCurrentIndex2</strong> vorkommen, wenn ein sekundärer Index ausgewählt wurde und die Engine keinen internen Cursor öffnen kann, um diesen Index zu verwenden.</p></td>
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


Bei Erfolg wird der aktuelle Index des Cursors auf den angeforderten Index festgelegt. Indexeinträge können nun mithilfe von [JetSeek](./jetseek-function.md) entsprechend der Index Definition des angeforderten Indexes gesucht werden. Index Einträge können auch mithilfe von [jetmove](./jetmove-function.md) in der von dieser Index Definition angegebenen Reihenfolge aufgelistet werden. Die aktuelle Position des Cursors ist entweder auf den ersten Index Eintrag im Index (JET_bitMoveFirst) oder auf einen bestimmten Index Eintrag festgelegt, der mit der aktuellen Position des Cursors im alten Index (JET_bitNoMove) verknüpft ist. Es erfolgt keine Änderung des Daten Bank Status.

Bei einem Fehler sind der aktuelle Index und die aktuelle Position des Cursors in einem nicht definierten Zustand. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Wenn der Index-ID-Hinweis veraltet ist, schlägt die API einfach fehl. Es gibt in diesem Fall keinen Fall Back auf den Textnamen des Indexes, wie dies zu erwarten ist. Dieser Fall Back muss manuell vom Aufrufer der API durchgeführt werden.

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
<td><p>Implementiert als <strong>JetSetCurrentIndex2W</strong> (Unicode) und <strong>JetSetCurrentIndex2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[Jetkreateingedex](./jetcreateindex-function.md)  
[Jetgetcurrentindex](./jetgetcurrentindex-function.md)  
[Jetgetindexinfo](./jetgetindexinfo-function.md)  
[Jetgettableindexinfo](./jetgettableindexinfo-function.md)  
[Jetmove](./jetmove-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[JetSeek](./jetseek-function.md)  
[Jetstopservice](./jetstopservice-function.md)
