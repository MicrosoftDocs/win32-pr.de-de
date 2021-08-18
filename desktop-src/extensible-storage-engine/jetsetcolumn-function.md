---
description: Weitere Informationen finden Sie unter JetSetColumn-Funktion.
title: JetSetColumn-Funktion
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 848d575f6fd8598aa3262273e9da3ce4cd1aaed12bcb2dc17e41e0d2f98bfdad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978860"
---
# <a name="jetsetcolumn-function"></a>JetSetColumn-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetcolumn-function"></a>JetSetColumn-Funktion

Die **JetSetColumn-Funktion** ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, um eingefügt oder den aktuellen Datensatz zu aktualisieren. Sie kann einen vorhandenen Wert überschreiben, einer Sequenz von Werten in einer mehrwertigen Spalte einen neuen Wert hinzufügen, einen Wert aus einer Sequenz von Werten in einer mehrwertigen Spalte entfernen oder einen long-Wert ganz oder teilweise aktualisieren, eine Spalte vom Typ [JET_coltypLongText](./jet-coltyp.md) [oder JET_coltypLongBinary](./jet-coltyp.md).

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*Columnid*

Die [JET_COLUMNID](./jet-columnid.md) der abzurufenden Spalte. Alternativ kann ein *columnid-Wert* von 0 (null) angegeben werden. Wenn *columnid* 0 (null) angegeben wird, werden alle markierten Spalten, Sparsespalten und mehrwertige Spalten, als einzelne Spalte behandelt. Dies erleichtert das Abrufen aller Sparsespalten, die in einem Datensatz vorhanden sind.

*pvData*

Eingabepuffer mit Daten, die für den Spaltenwert verwendet werden.

*cbData*

Größe des Eingabepuffers in Bytes.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten:

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
<td><p>JET_bitSetAppendLV</p></td>
<td><p>Diese Option wird verwendet, um Daten an eine Spalte vom Typ JET_coltypLongText <a href="gg269213(v=exchg.10).md">oder</a> <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary.</a> Das gleiche Verhalten kann erreicht werden, indem die Größe des vorhandenen long-Werts bestimmt und <em>ibLongValue</em> in <em>psetinfo angegeben wird.</em> Es ist jedoch einfacher, dieses Grbit zu <em>verwenden,</em> da es nicht erforderlich ist, die Größe des vorhandenen Spaltenwerts zu kennen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetOverwriteLV</p></td>
<td><p>Diese Option wird verwendet, um den vorhandenen Long-Wert durch die neu bereitgestellten Daten zu ersetzen. Wenn diese Option verwendet wird, ist dies so, als ob der vorhandene Long-Wert vor dem Festlegen der neuen Daten auf 0 (null) länge festgelegt wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetRevertToDefaultValue</p></td>
<td><p>Diese Option gilt nur für markierte Spalten, Sparsespalten oder mehrwertige Spalten. Dies bewirkt, dass die Spalte den Standardspaltenwert bei nachfolgenden Abrufspaltenvorgängen zurück gibt. Alle vorhandenen Spaltenwerte werden entfernt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetSeparateLV</p></td>
<td><p>Diese Option wird verwendet, um zu erzwingen, dass ein long-Wert, Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary,</a>getrennt von den restlichen Datensatzdaten gespeichert wird. Dies tritt normalerweise auf, wenn die Größe des long-Werts verhindert, dass er mit den verbleibenden Datensatzdaten gespeichert wird. Diese Option kann jedoch verwendet werden, um zu erzwingen, dass der Long-Wert separat gespeichert wird. Beachten Sie, dass lange Werte mit einer Größe von vier Bytes kleiner nicht voneinander getrennt werden können. In solchen Fällen wird die Option ignoriert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSizeLV</p></td>
<td><p>Diese Option wird verwendet, um den Eingabepuffer als eine ganzzahlige Anzahl von Bytes zu interpretieren, die als Länge des long-Werts festgelegt wird, der von der angegebenen <em>columnid</em> beschrieben wird, und, falls angegeben, als Sequenznummer in psetinfo- &gt; itagSequence. Wenn die größe größer als der vorhandene Spaltenwert ist, wird die Spalte um 0 s erweitert. Wenn die Größe kleiner als der vorhandene Spaltenwert ist, wird der Wert abgeschnitten.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetUniqueMultiValues</p></td>
<td><p>Diese Option wird verwendet, um zu erzwingen, dass alle Werte in einer mehrwertigen Spalte unterschiedlich sind. Diese Option vergleicht die Quellspaltendaten ohne Transformationen mit anderen vorhandenen Spaltenwerten, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird. Wenn diese Option angegeben ist, können JET_bitSetAppendLV, JET_bitSetOverwriteLV und JET_bitSetSizeLV nicht ebenfalls angegeben werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUniqueNormalizedMultiValues</p></td>
<td><p>Diese Option wird verwendet, um zu erzwingen, dass alle Werte in einer mehrwertigen Spalte unterschiedlich sind. Diese Option vergleicht die schlüsselnormierte Transformation von Spaltendaten mit anderen ähnlich transformierten vorhandenen Spaltenwerten, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird. Wenn diese Option angegeben ist, können JET_bitSetAppendLV, JET_bitSetOverwriteLV und JET_bitSetSizeLV nicht ebenfalls angegeben werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetZeroLength</p></td>
<td><p>Mit dieser Option wird ein Wert auf die Länge 0 (null) festgelegt. Normalerweise wird ein Spaltenwert auf <strong>NULL festgelegt,</strong> indem ein cbMax-Wert von 0 (null) übergeben wird. Für einige Typen wie <a href="gg269213(v=exchg.10).md">JET_coltypText</a>kann ein Spaltenwert jedoch eine Länge von 0 (null) anstelle von <strong></strong> <strong>NULL</strong>haben, und diese Option wird verwendet, um zwischen NULL und 0 (null) Länge zu unterscheiden.</p>
<p><strong>Hinweis:</strong>  Wenn es sich bei der Spalte um eine Spalte mit fester Länge handelt, wird dieses Bit im Allgemeinen ignoriert, und die Spalte wird auf <strong>NULL festgelegt.</strong> Wenn es sich bei der Spalte jedoch um eine markierte Spalte mit fester Länge handelt, wird die Spaltenlänge auf 0 festgelegt. Wenn die markierte Spalte mit fester Länge auf 0 (0) festgelegt ist, wird versucht, die Spalte mit <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> oder <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> abzurufen, aber die tatsächliche Länge, die im <em>cbActual-Parameter</em> zurückgegeben wird, ist 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIntrinsicLV</p></td>
<td><p>Diese Option wird verwendet, um den gesamten Long-Wert im Datensatz zu speichern.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetCompressed</p></td>
<td><p>Diese Option wird verwendet, um beim Speichern der Daten eine Datenkomprimierung zu versuchen.</p>
<p><strong>Windows 7:</strong>  JET_bitSetCompressed wird in Windows 7 eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUncompressed</p></td>
<td><p>Diese Option wird verwendet, um beim Speichern der Daten keine Komprimierung zu versuchen.</p>
<p><strong>Windows 7:</strong>  JET_bitSetUnCompressed wird in Windows 7 eingeführt.</p></td>
</tr>
</tbody>
</table>


*psetinfo*

Zeiger auf optionale Eingabeparameter, die für diese Funktion mithilfe der -Struktur JET_SETINFO [werden](./jet-setinfo-structure.md) können.

Wenn *psetinfo* als **NULL** angegeben wird, verhält sich die Funktion so, als ob eine *ItagSequence* von 1 und *ein ibLongValue* von 0 (null) angegeben würden. Dies bewirkt, dass der Spaltensatz den ersten Wert einer mehrwertigen Spalte und lange Daten ab Offset 0 (null) festgelegt.

Für diesen Parameter können die folgenden Optionen festgelegt werden:

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
<td><p>ibLongValue</p></td>
<td><p>Binärer Offset in einen long-Spaltenwert, an dem set-Daten beginnen sollen.</p></td>
</tr>
<tr class="even">
<td><p>itagSequence</p></td>
<td><p>Sequenznummer des gewünschten mehrwertigen Spaltenwerts, der festgelegt werden soll. Wenn <em>itagSequence</em> auf 0 (null) festgelegt ist, sollte der bereitgestellte Wert an das Ende der Sequenz mehrwertiger Werte angefügt werden. Wenn die bereitgestellte Sequenznummer größer als der letzte vorhandene mehrwertige Wert ist, wird der gegebene Wert erneut an das Ende der Sequenz von Werten angefügt. Wenn die Sequenznummer einem vorhandenen Wert entspricht, wird dieser Wert durch den angegebenen Wert ersetzt.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Die angegebenen Spalten-IDs liegen außerhalb der rechtlichen Grenzen einer Spalten-ID.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Die von der angegebenen <em>columnid beschriebene</em> Spalte ist in der Tabelle nicht vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable</p></td>
<td><p>Es wurde ein unzulässiger Versuch unternommen, einen long-Wert während eines Vorgangs zum Löschen des ursprünglichen Updates beim Kopieren von Einfügungen zu aktualisieren.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig</p></td>
<td><p>Die im Eingabepuffer angegebenen Spaltenwertdaten überschreiten die Größenbeschränkung für eine Spalte mit fester Länge oder für Textspalten mit fester Länge oder binäre Spalten. Dieser Fehler wird auch zurückgegeben, wenn mehr als 1.024 Bytes an Daten für eine lange Spalte übergeben und das JET_bitSetIntrinsicLV wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p>
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Die Datengröße des angegebenen Spaltenwerts passt nicht zu dem, was für den Datentyp mit fester Länge natürlich ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Es wurde ein unzulässiger Versuch unternommen, eine Spalte mit automatischer Inkremente entweder während eines Einfüge- oder Aktualisierungsvorgang zu aktualisieren oder eine Versionsspalte während eines Er ersetzten Vorgangs zu aktualisieren.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Die angegebenen Optionen sind unbekannt oder eine unzulässige Kombination bekannter Biteinstellungen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Die psetinfo- &gt; cbStruct ist keine gültige <a href="gg294090(v=exchg.10).md"></a> Größe für die JET_SETINFO Struktur.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate</p></td>
<td><p>Beim Vorgang zum Festlegen der Spalte wurde versucht, einen doppelten Wert zu erstellen, und entweder JET_bitSetUniqueMultiValues oder JET_bitSetUniqueNormalizedMultiValues.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Es wurde ein unzulässiger Versuch unternommen, einen langen Spaltenwert zu aktualisieren, wenn die aufrufende Sitzung nicht in einer Transaktion enthalten war.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid</p></td>
<td><p>Es wurde ein unzulässiger Versuch unternommen, eine<strong>Nicht-NULL-Spalte</strong> auf <strong>NULL zu setzen.</strong></p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Identisch mit JET_errNullInvalid.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig</p></td>
<td><p>Der Spaltenwert konnte nicht auf den Wert im Eingabepuffer festgelegt werden, da dies dazu führte, dass der Datensatz seine Größenbeschränkung für die Seitengröße überschreitet. Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> können getrennt von den verbleibenden Datensatzdaten gespeichert werden. Andere Spalten müssen jedoch mit dem Datensatz gespeichert werden und können dazu führen, dass die Beschränkung der Datensatzgröße überschritten wird. Selbst lange Spalten erfordern 5 Byte Speicherplatz innerhalb des Datensatzes als Verknüpfung. Dies kann auch dazu führen, dass JET_errRecordTooBig zurückgegeben werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p>
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>Der Cursor wird derzeit weder einen neuen Datensatz einfügen noch einen vorhandenen Datensatz aktualisieren.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Dieser Fehler tritt auf, wenn die konfigurierte Größe des Versionsspeichers nicht ausreicht, um alle ausstehenden Updates zu speichern.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Der Spaltenwert im Eingabepuffer hat die maximal konfigurierte Länge für eine Spalte variabler Länge überschritten und wurde abgeschnitten.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der gewünschte Teil eines Spaltenwerts für die gegebene Spalte mit Daten festgelegt, die aus dem Eingabepuffer kopiert werden. Das DataSet wurde möglicherweise abgeschnitten, wenn es die für eine Spalte variabler Länge angegebene maximale Länge überschritten hat.

Bei einem Fehler bleibt die Cursorposition unverändert, und es werden keine Spaltenwertdaten im Kopierpuffer aktualisiert.

#### <a name="remarks"></a>Hinweise

Das Festlegen von long-Werten, Werten für JET_coltypLongBinary [vom](./jet-coltyp.md) Typ [JET_coltypLongText](./jet-coltyp.md) oder [JET_coltypLongBinary](./jet-coltyp.md), sollte nur erfolgen, wenn sich die aufrufende Sitzung in einer Transaktion befindet. Wenn sich die aufrufende Sitzung nicht in einer Transaktion befindet, kann für Änderungen an long-Werten, die separat gespeichert werden, ein vollständiges Committed ausgeführt werden, auch wenn der Aktualisierungsvorgang später abgebrochen wird. Wenn sich die aufrufende Sitzung in einer Transaktion befindet, können die Auswirkungen des Updates vollständig zurückgesetzt werden, indem das Update abgebrochen und die Sitzungstransaktion zurückgesetzt wird.

Indexaktualisierungen werden nicht als Ergebnis von **JetSetColumn-Vorgängen** ausgeführt. Stattdessen werden Indizes erst aktualisiert, nachdem alle Spaltenänderungen abgeschlossen und [JetUpdate](./jetupdate-function.md) aufgerufen wurde. Dies ermöglicht die effizienteste Aktualisierung von Indizes, wenn in Indizes mehr als eine Spalte geändert wird.

Die Größe eines Datensatzes ist basierend auf der Datenbankseitengröße beschränkt. Alle long-Werte im Datensatz, die größer als fünf Bytes sind, werden getrennt vom Datensatz gespeichert, wenn die Daten im Datensatz den Grenzwert als Ergebnis eines **JetSetColumn-Vorgangs** überschreiten. Der Fehler JET_errRecordTooBig wird nur zurückgegeben, nachdem alle trennbaren Datensatzspaltendaten getrennt vom Datensatz gespeichert wurden und der Datensatz weiterhin das Limit für die Datensatzgröße überschreitet.

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
<td><p>In Esent.h deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
