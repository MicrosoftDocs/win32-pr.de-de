---
description: 'Weitere Informationen zu: jetretrievecolenn-Funktion'
title: JetRetrieveColumn-Funktion
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 074fb2471733afac40f76dcae1a4ce3ff38edc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362943"
---
# <a name="jetretrievecolumn-function"></a>JetRetrieveColumn-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetretrievecolumn-function"></a>JetRetrieveColumn-Funktion

Die **jetretrievecolenn** -Funktion Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist. Zusätzlich zum Abrufen des tatsächlichen Spaltenwerts kann **jetretrievecolumschlag** auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, sodass die Größe der Anwendungs Puffer entsprechend angepasst werden kann.

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*ColumnID*

Der [JET_COLUMNID](./jet-columnid.md) der abzurufenden Spalte.

Ein *ColumnID* -Wert von 0 (null) kann angegeben werden, der sich nicht selbst auf eine einzelne Spalte bezieht. Wenn *ColumnID* 0 (null) angegeben wird, werden alle markierten Spalten, sparsespalten und mehrwertigen Spalten als einzelne Spalte behandelt. Dadurch wird das Abrufen aller sparsespalten ermöglicht, die in einem Datensatz vorhanden sind.

*pvData*

Der Ausgabepuffer, der den Spaltenwert empfängt.

*cbData*

Die maximale Größe des Ausgabepuffers in Bytes.

*pcbactual*

Empfängt die tatsächliche Größe (in Bytes) des Spaltenwerts.

Wenn dieser Parameter **null** ist, wird die tatsächliche Größe des Spaltenwerts nicht zurückgegeben.

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
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>Dieses Flag bewirkt, dass die Spalte "abrufen" den geänderten Wert anstelle des ursprünglichen Werts abruft. Wenn der Wert nicht geändert wurde, wird der ursprüngliche Wert abgerufen. Auf diese Weise kann ein Wert, der noch nicht eingefügt oder aktualisiert wurde, beim Einfügen oder Aktualisieren eines Datensatzes abgerufen werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveFromIndex</p></td>
<td><p>Diese Option wird verwendet, um nach Möglichkeit Spaltenwerte aus dem Index abzurufen, ohne auf den Datensatz zuzugreifen. Auf diese Weise kann das unnötige Laden von Datensätzen vermieden werden, wenn benötigte Daten aus Indexeinträgen selbst verfügbar sind. In Fällen, in denen der ursprüngliche Spaltenwert nicht aus dem Index abgerufen werden kann, wird auf den Datensatz zugegriffen, und die Daten werden als normal abgerufen, weil Sie nicht rückgängig gemacht werden. Dies ist eine Leistungs Option und sollte nur angegeben werden, wenn es wahrscheinlich ist, dass der Spaltenwert aus dem Index abgerufen werden kann. Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte Index ist, da die Indexeinträge für den gruppierten Index bzw. den primären Index die Datensätze selbst sind. Dieses Bit kann nicht festgelegt werden, wenn JET_bitRetrieveFromPrimaryBookmark ebenfalls festgelegt ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveFromPrimaryBookmark</p></td>
<td><p>Diese Option wird zum Abrufen von Spaltenwerten aus dem Index-Lesezeichen verwendet und unterscheidet sich möglicherweise vom Indexwert, wenn eine Spalte sowohl im primären Index als auch im aktuellen Index angezeigt wird. Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte Index oder der primäre Index ist. Dieses Bit kann nicht festgelegt werden, wenn JET_bitRetrieveFromIndex ebenfalls festgelegt ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveTag</p></td>
<td><p>Diese Option wird verwendet, um die Sequenznummer eines mehrwertigen Spaltenwerts in pretinfo- &gt; itagsequence abzurufen. Das Feld itagsequence ist häufig eine Eingabe zum Abrufen von Werten mit mehrwertigen Spalten aus einem Datensatz. Beim Abrufen von Werten aus einem Index ist es jedoch auch möglich, den Index Eintrag einer bestimmten Sequenznummer zuzuordnen und auch diese Sequenznummer abzurufen. Das Abrufen der Sequenznummer kann ein kostspieliger Vorgang sein und sollte nur bei Bedarf ausgeführt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveNull</p></td>
<td><p>Diese Option wird verwendet, um <strong>null</strong> -Werte für mehrwertige Spalten abzurufen. Wenn diese Option nicht angegeben ist, werden <strong>null</strong> -Werte für mehrwertige Spalten automatisch übersprungen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveIgnoreDefault</p></td>
<td><p>Diese Option wirkt sich nur auf mehrwertige Spalten aus und bewirkt, dass ein <strong>null</strong> -Wert zurückgegeben wird, wenn die angeforderte Sequenznummer 1 ist und für die Spalte im Datensatz keine Werte festgelegt sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveLongId</p></td>
<td><p>Dieses Flag ist nur für die interne Verwendung bestimmt und nicht für die Verwendung in der Anwendung bestimmt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveLongValueRefCount</p></td>
<td><p>Dieses Flag ist nur für die interne Verwendung bestimmt und nicht für die Verwendung in der Anwendung bestimmt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveTuple</p></td>
<td><p>Dieses Flag ermöglicht das Abrufen eines tupelsegments des Indexes. Dieses Bit muss mit JET_bitRetrieveFromIndex angegeben werden.</p></td>
</tr>
</tbody>
</table>


*pretinfo*

Wenn *pretinfo* als **null** angegeben wird, verhält sich die Funktion so, als ob eine *itagsequence* von 1 und ein *iblongvalue-Wert* von 0 (null) angegeben wurde. Dies bewirkt, dass der Spalten Abruf den ersten Wert einer mehrwertigen Spalte abruft und lange Daten bei Offset 0 (null) abruft.

Dieser Parameter wird verwendet, um eine oder mehrere der folgenden Punkte bereitzustellen:

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
<td><p>iblongvalue</p></td>
<td><p>Gibt beim Abrufen eines Teils eines Spaltenwerts einen binären Offset in einen Long-Spaltenwert an.</p></td>
</tr>
<tr class="even">
<td><p>itagsequence</p></td>
<td><p>Gibt die Sequenznummer des gewünschten Werts für mehrwertige Spalten an. Beachten Sie, dass dieses Feld nur festgelegt wird, wenn das JET_bitRetrieveTag angegeben wird. Andernfalls ist die Änderung unverändert.</p></td>
</tr>
<tr class="odd">
<td><p>columnidnexttaging</p></td>
<td><p>Gibt die Spalten-ID des zurückgegebenen Spaltenwerts zurück, wenn alle markierten Spalten, Spalten mit geringer Dichte und mehrwertigen Spalten abgerufen werden. dabei wird die Spalten-ID 0 (NULL <em>) übergeben.</em></p></td>
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
<td><p>JET_errBadColumnId</p></td>
<td><p>Die angegebene Spalten-ID liegt außerhalb der zulässigen Beschränkungen einer Spalten-ID.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadItagSequence</p></td>
<td><p>Ein ungültiger Wert für eine mehrwertige spaltensequenznummer wurde in "pretinfo- &gt; itagsequence" übergeben. Gültige Werte für die Sequenznummern der mehrwertigen Spaltenwerte sind 1 oder höher. Der Wert 0 (null) ist für diese Funktion ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Die von der angegebenen Spalte beschriebene Spalte ist in der <em>Tabelle nicht vorhanden</em> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex</p></td>
<td><p>Als Teil Zeichenfolgen indizierte Spalten können nicht aus dem Index abgerufen werden, da in jedem Index Eintrag normalerweise nur ein kleiner Teil der Spalte vorhanden ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>In einigen Fällen muss der für die Spalte abrufen angegebene Puffer ausreichend groß sein, um eine beliebige Menge an Spaltenwerten zurückzugeben. So werden z. b. die aktualisierbaren Spalten für die Spalten Anpassung angepasst, damit Sie für den Transaktionskontext der aufrufenden Sitzung konsistent sind. diese Anpassung erfordert den vom Aufrufer bereitgestellten Puffer. Wenn nicht genügend Pufferspeicher bereitgestellt wird, wird JET_errInvalidBufferSize zurückgegeben, und es werden keine Spaltendaten zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Mindestens einer der angegebenen Parameter ist falsch. Dies kann vorkommen, wenn "retinfo. cbStruct" kleiner ist als die Größe der <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Die angegebenen Optionen sind unbekannt oder eine ungültige Kombination bekannter Biteinstellungen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor ist nicht in einem Datensatz positioniert. Dafür sind viele verschiedene Gründe möglich. Dies ist beispielsweise der Fall, wenn der Cursor aktuell nach dem letzten Datensatz im aktuellen Index positioniert ist.</p></td>
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
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>Der gesamte Spaltenwert konnte nicht abgerufen werden, da der angegebene Puffer kleiner ist als die Größe der Spalte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>Der abgerufene Spaltenwert ist <strong>null</strong>.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der Spaltenwert für die angegebene Spalte in den angegebenen Puffer kopiert. Weniger als alle Spaltenwerte werden mit der Warnung kopiert, JET_wrnBufferTruncated zurückgegeben wird. Wenn *pcbactual* angegeben wurde, wird die tatsächliche Größe des Spaltenwerts zurückgegeben. Beachten Sie, dass **null** -Werte eine Länge von 0 (null) aufweisen und die zurückgegebene Größe somit auf 0 (null) festgelegt wird. Wenn es sich bei der abgerufenen Spalte um eine mehrwertige Spalte handelt und *pretinfo* angegeben wurde und JET_bitReturnTag als Option festgelegt wurde, wird die Sequenznummer des Spaltenwerts in pretinfo- \> itagsequence zurückgegeben.

Bei einem Fehler wird die Cursorposition unverändert bleiben, und es werden keine Daten in den bereitgestellten Puffer kopiert.

#### <a name="remarks"></a>Bemerkungen

Dieser-Befehl wird nur einmal zum Abrufen von Daten mit fester oder bekannter Größe für nicht mehrwertige Spalten verwendet. Wenn die Größe der Spaltendaten jedoch unbekannt ist, wird dieser Befehl in der Regel zweimal verwendet. Sie wird zuerst aufgerufen, um die Größe der Daten zu ermitteln, damit Sie den erforderlichen Speicherplatz zuordnen kann. Der gleiche Rückruf wird dann erneut zum Abrufen der Spaltendaten durchgeführt. Wenn die tatsächliche Anzahl von Werten unbekannt ist, weil eine Spalte mehr wertig ist, wird der-Befehl in der Regel dreimal verwendet. Rufen Sie zuerst die Anzahl der Werte ab, und wiederholen Sie dann den Speicher, und rufen Sie die eigentlichen Daten ab.

Zum Abrufen aller Werte für eine mehrwertige Spalte können Sie diese Funktion wiederholt mit einem pretinfo- \> itagsequence-Wert aufrufen, beginnend bei 1 und bei jedem nachfolgenden Aufruf. Der letzte Spaltenwert muss abgerufen werden, wenn ein JET_wrnColumnNull von der Funktion zurückgegeben wird. Beachten Sie, dass diese Methode nicht ausgeführt werden kann, wenn die Spalte mit mehreren Werten explizite **null** -Werte enthält, die in der Wert Sequenz festgelegt sind, da diese Werte übersprungen werden. Wenn eine Anwendung alle mehrwertigen Spaltenwerte abrufen möchte, einschließlich derjenigen, die explizit auf **null** festgelegt sind, muss [jetretrievecolenumns](./jetretrievecolumns-function.md) anstelle von **jetretrievecolbin** verwendet werden. Beachten Sie, dass diese Funktion nicht die Anzahl der Werte für eine mehrwertige Funktion zurückgibt, wenn ein *itagsequence* -Wert von 0 (null) angegeben wird. Nur [jetretrievecolenumns](./jetretrievecolumns-function.md) gibt die Anzahl der Werte eines Spaltenwerts zurück, wenn ein *itagsequence* -Wert von 0 (null) übergeben wird.

Wenn diese Funktion auf Transaktionsebene 0 (null) aufgerufen wird, z. b. wenn sich die Aufruf Sitzung nicht selbst in einer Transaktion befindet, wird eine Transaktion in der Funktion geöffnet und geschlossen. Der Zweck dieses Werts besteht darin, konsistente Ergebnisse zurückzugeben, wenn ein Long-Wert Datenbankseiten umfasst. Beachten Sie, dass die Transaktion zwischen Funktionsaufrufen und einer Reihe von Aufrufen dieser Funktion freigegeben wird, wenn die Sitzung nicht in einer Transaktion ausgeführt wird und nach dem ersten Aufruf dieser Funktion aktualisierte Daten zurückgeben kann.

Der Standard Spaltenwert wird abgerufen, wenn die Spalte nicht explizit auf einen anderen Wert festgelegt wurde, es sei denn, die JET_bitRetrieveIgnoreDefault-Option ist festgelegt.

Das Abrufen des Werts der AUTOINCREMENT-Spalte aus dem Kopier Puffer vor dem Einfügen ist ein gängiges Mittel, einen Datensatz eindeutig für die Verknüpfung zu identifizieren, wenn normalisierte Daten in mehrere Tabellen eingefügt werden. Der AutoIncrement-Wert wird zugewiesen, wenn der Einfügevorgang beginnt und jederzeit aus dem Kopier Puffer abgerufen werden kann, bis das Update beendet ist.

Wenn Sie alle markierten Spalten mit mehreren Werten und geringer Dichte abrufen, indem Sie *ColumnID* auf 0 (null) festlegen, werden die Spalten in der *ColumnID* -Reihenfolge vom niedrigsten *ColumnID* zum höchsten *ColumnID* abgerufen. Die gleiche Reihenfolge von Spaltenwerten wird jedes Mal zurückgegeben, wenn Spaltenwerte abgerufen werden. Die Reihenfolge ist deterministisch.

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[Jetsetcolumn](./jetretrievekey-function.md)  
[Jetretrievecolumschlag](./jetretrievecolumns-function.md)
