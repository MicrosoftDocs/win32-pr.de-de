---
description: 'Weitere Informationen über: jetsetcolumn-Funktion'
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
ms.openlocfilehash: 3c1fd267bea6bbb995a13ce65f97f1f531572a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347800"
---
# <a name="jetsetcolumn-function"></a>JetSetColumn-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetcolumn-function"></a>JetSetColumn-Funktion

Die **jetsetcolumn** -Funktion ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, um eingefügt zu werden, oder um den aktuellen Datensatz zu aktualisieren. Es kann einen vorhandenen Wert überschreiben, einen neuen Wert zu einer Sequenz von Werten in einer mehrwertigen Spalte hinzufügen, einen Wert aus einer Sequenz von Werten in einer mehrwertigen Spalte entfernen oder den gesamten oder einen Teil eines Long-Werts aktualisieren, eine Spalte vom Typ [JET_coltypLongText](./jet-coltyp.md) oder [JET_coltypLongBinary](./jet-coltyp.md).

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

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*ColumnID*

Der [JET_COLUMNID](./jet-columnid.md) der Spalte, die abgerufen werden soll. Alternativ kann ein *ColumnID* -Wert von 0 (null) angegeben werden. Wenn *ColumnID* 0 (null) angegeben wird, werden alle markierten Spalten, Spalten mit geringer Dichte und mehrwertigen Spalten als einzelne Spalte behandelt. Dadurch wird das Abrufen aller sparsespalten ermöglicht, die in einem Datensatz vorhanden sind.

*pvData*

Eingabepuffer, der Daten enthält, die für den Spaltenwert verwendet werden.

*cbData*

Größe des Eingabe Puffers in Bytes.

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
<td><p>JET_bitSetAppendLV</p></td>
<td><p>Diese Option wird zum Anfügen von Daten an eine Spalte vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>verwendet. Das gleiche Verhalten können Sie erreichen, indem Sie die Größe des vorhandenen Long-Werts ermitteln und <em>iblongvalue</em> in <em>psetup</em>angeben. Es ist jedoch einfacher, dieses <em>grbit</em> zu verwenden, da es nicht erforderlich ist, die Größe des vorhandenen Spaltenwerts zu kennen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetOverwriteLV</p></td>
<td><p>Diese Option wird verwendet, um den vorhandenen Long-Wert durch die neu bereitgestellten Daten zu ersetzen. Wenn diese Option verwendet wird, ist es so, als ob der vorhandene Long-Wert auf 0 (null) festgelegt wurde, bevor die neuen Daten festgelegt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetRevertToDefaultValue</p></td>
<td><p>Diese Option gilt nur für markierte, Spalten mit geringer Dichte oder mehrwertige Spalten. Dies bewirkt, dass die Spalte bei nachfolgenden Spalten Abruf Vorgängen den Standard Spaltenwert zurückgibt. Alle vorhandenen Spaltenwerte werden entfernt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetSeparateLV</p></td>
<td><p>Diese Option wird verwendet, um zu erzwingen, dass ein langer Wert, Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>getrennt vom Rest der Daten Satz Daten gespeichert werden. Dies tritt normalerweise auf, wenn die Größe des Long-Werts verhindert, dass Sie mit den verbleibenden Daten Satz Daten gespeichert wird. Diese Option kann jedoch verwendet werden, um zu erzwingen, dass der lange Wert separat gespeichert wird. Beachten Sie, dass lange Werte mit einer Größe von vier Bytes, die kleiner als getrennt sind, nicht erzwungen werden können. In solchen Fällen wird die Option ignoriert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSizeLV</p></td>
<td><p>Diese Option wird verwendet, um den Eingabepuffer als ganzzahlige Anzahl von Bytes zu interpretieren, die als Länge des Long-Werts festgelegt werden, der durch das angegebene <em>ColumnID</em> und ggf. die Sequenznummer in psetinfo- &gt; itagsequence beschrieben wird. Wenn die angegebene Größe größer ist als der vorhandene Spaltenwert, wird die Spalte um 0s erweitert. Wenn die Größe kleiner als der vorhandene Spaltenwert ist, wird der Wert abgeschnitten.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetUniqueMultiValues</p></td>
<td><p>Diese Option wird verwendet, um zu erzwingen, dass alle Werte in einer mehrwertigen Spalte voneinander abweichen. Mit dieser Option werden die Quell Spaltendaten ohne Transformationen mit anderen vorhandenen Spaltenwerten verglichen, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird. Wenn diese Option angegeben wird, können JET_bitSetAppendLV, JET_bitSetOverwriteLV und JET_bitSetSizeLV nicht ebenfalls angegeben werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUniqueNormalizedMultiValues</p></td>
<td><p>Diese Option wird verwendet, um zu erzwingen, dass alle Werte in einer mehrwertigen Spalte voneinander abweichen. Mit dieser Option wird die normalisierte Transformation von Spaltendaten mit anderen ähnlich transformierten vorhandenen Spaltenwerten verglichen, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird. Wenn diese Option angegeben wird, können JET_bitSetAppendLV, JET_bitSetOverwriteLV und JET_bitSetSizeLV nicht ebenfalls angegeben werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetZeroLength</p></td>
<td><p>Diese Option wird verwendet, um einen Wert auf die Länge 0 (null) festzulegen. Normalerweise wird ein Spaltenwert auf <strong>null</strong> festgelegt, indem ein cbmax-Wert von 0 (null) übergeben wird. Bei manchen Typen, wie z. b. <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, kann ein Spaltenwert jedoch eine Länge von 0 (null) anstelle von <strong>null</strong>sein, und diese Option wird verwendet, um zwischen <strong>null</strong> und 0 (null) zu unterscheiden.</p>
<p><strong>Hinweis</strong>  Im Allgemeinen wird dieses Bit ignoriert, wenn die Spalte eine Spalte mit fester Länge ist und die Spalte auf <strong>null</strong>festgelegt ist. Wenn die Spalte jedoch eine markierte Spalte mit fester Länge ist, wird die Länge der Spalte auf 0 festgelegt. Wenn die markierte Spalte mit fester Länge auf 0 (null) festgelegt ist, wird versucht, die Spalte mit <a href="gg269198(v=exchg.10).md">jetretrievecolumschlag</a> oder <a href="gg294135(v=exchg.10).md">jetretrievecolumschlag</a> abzurufen, aber die tatsächliche Länge, die im <em>cbactual</em> -Parameter zurückgegeben wird, ist 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIntrinsicLV</p></td>
<td><p>Diese Option wird verwendet, um den gesamten Long-Wert im Datensatz zu speichern.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetCompressed</p></td>
<td><p>Diese Option wird verwendet, um die Datenkomprimierung beim Speichern der Daten zu versuchen.</p>
<p><strong>Windows 7:</strong>  JET_bitSetCompressed wurde in Windows 7 eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUncompressed</p></td>
<td><p>Diese Option wird verwendet, wenn beim Speichern der Daten keine Komprimierung versucht wird.</p>
<p><strong>Windows 7:</strong>  JET_bitSetUnCompressed wurde in Windows 7 eingeführt.</p></td>
</tr>
</tbody>
</table>


*psetup-Info*

Zeiger auf optionale Eingabeparameter, die für diese Funktion mithilfe der [JET_SETINFO](./jet-setinfo-structure.md) Struktur festgelegt werden können.

Wenn *psetinfo* als **null** angegeben wird, verhält sich die Funktion so, als ob eine *itagsequence* von 1 und ein *iblongvalue-Wert* von 0 (null) angegeben wurde. Dies bewirkt, dass der erste Wert einer mehrwertigen Spalte von Spalten Satz festgelegt wird und lange Daten beginnend am Offset 0 (null) festgelegt werden.

Die folgenden Optionen können für diesen Parameter festgelegt werden:

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
<td><p>Binärer Offset in einen Long-Spaltenwert, in dem Set Data beginnen soll.</p></td>
</tr>
<tr class="even">
<td><p>itagsequence</p></td>
<td><p>Die Sequenznummer des gewünschten Werts der mehrwertigen Spalte, die festgelegt werden soll. Wenn <em>itagsequence</em> auf 0 (null) festgelegt ist, sollte der angegebene Wert an das Ende der Sequenz von mehrwertigen Werten angehängt werden. Wenn die angegebene Sequenznummer größer als der letzte vorhandene mehrwertige Wert ist, wird der angegebene Wert erneut an das Ende der Sequenz von Werten angehängt. Wenn die Sequenznummer einem vorhandenen Wert entspricht, wird dieser Wert durch den angegebenen Wert ersetzt.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Die von der angegebenen Spalte beschriebene Spalte ist in der <em>Tabelle nicht vorhanden</em> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable</p></td>
<td><p>Es wurde ein unzulässiger Versuch unternommen, einen Long-Wert während eines INSERT-Vorgangs zum Löschen des ursprünglichen Updates zu aktualisieren.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig</p></td>
<td><p>Die angegebenen Spaltenwert Daten, die im Eingabepuffer angegeben sind, überschreiten die Größenbeschränkung für eine Spalte mit fester Länge oder für Text oder Binär Spalten mit fester Länge. Dieser Fehler wird auch zurückgegeben, wenn mehr als 1024 Bytes an Daten für eine lange Spalte übergeben werden und das JET_bitSetIntrinsicLV-Flag festgelegt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Die angegebene Datengröße für den Spaltenwert stimmt nicht mit dem Wert für den Datentyp mit fester Länge identisch.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Es wurde ein unzulässiger Versuch unternommen, eine automatische Inkrement-Spalte entweder während eines INSERT-oder Update-Vorgangs zu aktualisieren oder eine Versions Spalte während eines Ersetzungs Vorgangs zu aktualisieren.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Die angegebenen Optionen sind unbekannt oder eine ungültige Kombination bekannter Biteinstellungen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Die angegebene "psetup Info- &gt; cbStruct" ist keine gültige Größe für die <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> Struktur.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate</p></td>
<td><p>Der Vorgang zum Festlegen der Spalte hat versucht, einen doppelten Wert zu erstellen und entweder JET_bitSetUniqueMultiValues oder JET_bitSetUniqueNormalizedMultiValues anzugeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Es wurde ein unzulässiger Versuch unternommen, einen Long-Spaltenwert zu aktualisieren, wenn sich die aufrufende Sitzung nicht in einer Transaktion befand.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid</p></td>
<td><p>Es wurde ein unzulässiger Versuch unternommen, eine nicht-<strong>null</strong> -Spalte auf <strong>null</strong>festzulegen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Identisch mit JET_errNullInvalid.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig</p></td>
<td><p>Der Spaltenwert konnte nicht auf den Wert im Eingabepuffer festgelegt werden, da er dazu geführt hätte, dass der Datensatz seine Größenbeschränkung für die Seitengröße überschreitet. Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> können getrennt von den verbleibenden Daten Satz Daten gespeichert werden. Allerdings müssen andere Spalten mit dem Datensatz gespeichert werden und können dazu führen, dass die Einschränkung der Daten Satz Größe überschritten wird. Sogar lange Spalten benötigen 5-Byte-Speicherplatz innerhalb des Datensatzes als Verknüpfung, und dies kann dazu führen, dass JET_errRecordTooBig zurückgegeben werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>Der Cursor befindet sich derzeit nicht im Prozess, entweder einen neuen Datensatz einzufügen oder einen vorhandenen Datensatz zu aktualisieren.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Dieser Fehler tritt auf, wenn die konfigurierte Größe des Versionsspeicher nicht ausreicht, um alle ausstehenden Updates zu speichern.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Der Spaltenwert im Eingabepuffer hat die für eine Spalte mit variabler Länge konfigurierte maximale Länge überschritten und wurde abgeschnitten.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der gewünschte Teil eines Spaltenwerts für die angegebene Spalte mit Daten, die aus dem Eingabepuffer kopiert wurden, festgelegt. Das DataSet wurde möglicherweise abgeschnitten, wenn es die für eine Spalte mit variabler Länge angegebene maximale Länge überschreitet.

Bei einem Fehler wird die Cursorposition unverändert bleiben, und im Kopier Puffer werden keine Spaltenwert Daten aktualisiert.

#### <a name="remarks"></a>Bemerkungen

Das Festlegen langer Werte, Werte für Spalten [JET_coltypLongBinary](./jet-coltyp.md) vom Typ [JET_coltypLongText](./jet-coltyp.md) oder [JET_coltypLongBinary](./jet-coltyp.md)sollten nur dann erfolgen, wenn sich die aufrufende Sitzung in einer Transaktion befindet. Wenn sich die aufrufende Sitzung nicht in einer Transaktion befindet, werden Änderungen an langen Werten, die separat gespeichert werden, möglicherweise auch dann vollständig ausgeführt, wenn der Aktualisierungs Vorgang später abgebrochen wird. Wenn sich die aufrufende Sitzung in einer Transaktion befindet, können die Auswirkungen des Updates vollständig rückgängig gemacht werden, indem das Update abgebrochen und ein Rollback für die Sitzungs Transaktion ausgeführt wird.

Index Aktualisierungen werden nicht als Ergebnis von **jetsetcolumn** -Vorgängen ausgeführt. Stattdessen werden Indizes erst aktualisiert, nachdem alle Spalten Änderungen vollständig sind und [jetupdate](./jetupdate-function.md) aufgerufen wird. Dies ermöglicht die effizienteste Aktualisierung von Indizes, wenn die Indizes mehr als eine Spalte ändern.

Die Größe eines Datensatzes hängt von der Größe der Datenbankseite ab. Alle langen Werte im Datensatz, die größer als fünf Bytes sind, werden getrennt vom Datensatz gespeichert, wenn die Daten im Datensatz aufgrund eines **jetsetcolumn** -Vorgangs den Grenzwert überschreiten. Der Fehler JET_errRecordTooBig wird nur zurückgegeben, nachdem alle trennbaren Daten Satz Spaltendaten getrennt vom Datensatz gespeichert wurden und der Datensatz weiterhin das Daten Satz Größenlimit überschreitet.

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
[JET_SETINFO](./jet-setinfo-structure.md)  
[Jetretrievecolumschlag](./jetretrievecolumn-function.md)  
[Jetsetcolumns](./jetsetcolumns-function.md)
