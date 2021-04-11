---
description: 'Weitere Informationen über: jetsetcolumns-Funktion'
title: JetSetColumns-Funktion
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4535b66064c19257f4bb7b51b059453660916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128160"
---
# <a name="jetsetcolumns-function"></a>JetSetColumns-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetcolumns-function"></a>JetSetColumns-Funktion

Die **jetsetcolumns** -Funktion ähnelt dem Verhalten von [jetsetcolumn](./jetsetcolumn-function.md) , ermöglicht einer Anwendung jedoch das Festlegen mehrerer Spaltenwerte in einem einzelnen Vorgang. Ein Array von [JET_SETCOLUMN](./jet-setcolumn-structure.md) Strukturen wird verwendet, um den Satz von Spaltenwerten zu beschreiben, die festgelegt werden sollen, und um Eingabepuffer für jeden festzulegenden Spaltenwert zu beschreiben.

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*psetcolumn*

Ein Zeiger auf ein Array aus mindestens einer [JET_SETCOLUMN](./jet-setcolumn-structure.md) -Struktur. Jede Struktur enthält Beschreibungen, welcher Spaltenwert festgelegt werden soll und von wo die Spaltendaten festgelegt werden sollen.

*csetcolumn*

Die Anzahl der [JET_SETCOLUMN](./jet-setcolumn-structure.md) Strukturen in dem Array, das von *psetcolumn* angegeben wird.

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
<td><p>JET_errBadColumnId</p></td>
<td><p>Die angegebene Spalten-ID liegt außerhalb der zulässigen Beschränkungen einer Spalten-ID.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Identisch mit JET_errNullInvalid.</p></td>
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
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
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
<td><p>Es wurde ein unzulässiger Versuch unternommen, eine nicht-NULL-Spalte auf NULL festzulegen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>Der Spaltenwert konnte nicht auf den Wert im Eingabepuffer festgelegt werden, da er dazu geführt hätte, dass der Datensatz seine Größenbeschränkung für die Seitengröße überschreitet. Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> können getrennt von den verbleibenden Daten Satz Daten gespeichert werden. Allerdings müssen andere Spalten mit dem Datensatz gespeichert werden und können dazu führen, dass die Einschränkung der Daten Satz Größe überschritten wird. Sogar lange Spalten benötigen 5-Byte-Speicherplatz innerhalb des Datensatzes als Verknüpfung, und dies kann dazu führen, dass JET_errRecordTooBig zurückgegeben werden.</p></td>
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
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>Der Cursor befindet sich derzeit nicht im Prozess, entweder einen neuen Datensatz einzufügen oder einen vorhandenen Datensatz zu aktualisieren.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Der Spaltenwert im Eingabepuffer hat die für eine Spalte mit variabler Länge konfigurierte maximale Länge überschritten und wurde abgeschnitten.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird für jede Spalte, die in den psetcolumns beschrieben wird, der gewünschte Teil des Spaltenwerts mit Daten festgelegt, die aus dem Eingabepuffer kopiert werden. Das Spalten DataSet wurde möglicherweise abgeschnitten, wenn es die für eine Spalte mit variabler Länge angegebene maximale Länge überschreitet.

Bei einem Fehler wird die Cursorposition unverändert bleiben, und im Kopier Puffer werden keine Spaltenwert Daten aktualisiert.

#### <a name="remarks"></a>Bemerkungen

Wenn ein einzelner Satz Spalten Vorgang einen Fehler zurückgibt, gibt der gesamte **jetsetcolumns** -Vorgang einen Fehler zurück. Warnungen werden im Allgemeinen in "psetcolumns- \> Error" und nicht im Rückgabecode dieser Funktion zurückgegeben. Wenn für den letzten Spalten Satz jedoch eine Warnung angezeigt wird, wird diese Warnung von **jetsetcolumns** selbst zurückgegeben.

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[Jetretrievecolumschlag](./jetretrievecolumns-function.md)  
[Jetsetcolumn](./jetsetcolumn-function.md)
