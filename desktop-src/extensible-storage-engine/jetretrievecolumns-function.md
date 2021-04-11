---
description: 'Weitere Informationen finden Sie hier: jetretrievecolumschlag-Funktion'
title: JetRetrieveColumns-Funktion
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 515be3a36932c9a56843f51d2e1b32a41ca94e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218129"
---
# <a name="jetretrievecolumns-function"></a>JetRetrieveColumns-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetretrievecolumns-function"></a>JetRetrieveColumns-Funktion

Die **jetretrievecolenumns** -Funktion ruft in einem einzelnen Vorgang mehrere Spaltenwerte aus dem aktuellen Datensatz ab. Ein Array von [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) Strukturen wird verwendet, um den Satz von Spaltenwerten zu beschreiben, die abgerufen werden sollen, und um Ausgabepuffer für jeden abzurufenden Spaltenwert zu beschreiben.

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*predreifach-ecolumschlag*

Ein Zeiger auf ein Array aus mindestens einer [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) -Struktur. Jede Struktur enthält Beschreibungen, welche Spaltenwerte abgerufen werden sollen und wo die zurückgegebenen Daten gespeichert werden sollen.

*"kretrevecolumschlag"*

Die Anzahl der [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) Strukturen im Array, angegeben durch *prezevecolenumn*.

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
<td><p>Ein ungültiger Wert für eine mehrwertige spaltensequenznummer wurde in "pretinfo- &gt; itagsequence" übergeben. Gültige Werte für die Sequenznummern der mehrwertigen Spaltenwerte sind 1 oder höher. Der Wert 0 (null) ist für diese Funktion gültig, aber für <a href="gg269198(v=exchg.10).md">jetretrievecolumschlag</a>ungültig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadColumnId</p></td>
<td><p>Die angegebene Spalten-ID liegt außerhalb der zulässigen Beschränkungen einer Spalten-ID.</p></td>
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
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>In einigen Fällen muss der für die Spalte abrufen angegebene Puffer ausreichend groß sein, um eine beliebige Menge an Spaltenwerten zurückzugeben. So werden z. b. die aktualisierbaren Spalten für die Spalten Anpassung angepasst, damit Sie für den Transaktionskontext der aufrufenden Sitzung konsistent sind. diese Anpassung erfordert den vom Aufrufer bereitgestellten Puffer. Wenn nicht genügend Pufferspeicher bereitgestellt wird, wird JET_errInvalidBufferSize zurückgegeben, und es werden keine Spaltendaten zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Die angegebenen Optionen sind unbekannt oder eine ungültige Kombination bekannter Biteinstellungen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Mindestens einer der angegebenen Parameter ist falsch. Dies kann vorkommen, wenn "retinfo. cbStruct" kleiner ist als die Größe der <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
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
</tbody>
</table>


Bei Erfolg werden Spaltendaten und Spaltengröße in den bereitgestellten Puffern zurückgegeben, die Unterarray von [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) Strukturen beschrieben werden. Wenn eine *itagsequence* auf 0 (null) festgelegt wurde, um anzugeben, dass die Anzahl der Instanzen eines mehrwertigen Felds anstelle von Spaltendaten erwünscht war, wird die Anzahl der Instanzen einer mehrwertigen Spalte im Feld *itagsequence* selbst zurückgegeben. Jede [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) Struktur verfügt über ein Fehler Feld, das Warnungen für die abgerufene Spalte enthält. Wenn die Spalte den Wert **null** hat, wird der Fehlercode auf JET_wrnColumnNull festgelegt.

Bei einem Fehler wird die Cursorposition unverändert bleiben, und es werden keine Daten in den bereitgestellten Puffer kopiert.

#### <a name="remarks"></a>Bemerkungen

**Jetretrievecolenns** unterstützt ein Feature, das [jetretrievecolenn](./jetretrievecolumn-function.md) nicht unterstützt. Mit dieser Option können Sie die Anzahl der Instanzen einer mehrwertigen Spalte abrufen. Der Zweck dieses Features besteht darin, dass eine Anwendung alle Werte einer Spalte abrufen kann. Dies kann erreicht werden, indem zuerst die Anzahl der Werte bestimmt wird, die eine Spalte aufweist. Anschließend können Ihre Längen durch das erneute Aufrufen von **jetretrievecolumschlag** durch eine [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) Struktur bestimmt werden, die jedem Wert zugeordnet ist, um die Länge der Spaltendaten zu bestimmen. Dies kann erreicht werden, indem **null**_pvData_ -Zeiger mit *cbmax* von 0 (null) übergeben und die Spaltenlänge in *cbactial* abgerufen wird. Der dritte und letzte-Befehl können mit zugeordnetem Arbeitsspeicher für die Spaltenwert Daten erstellt werden.

Wenn eine abgerufene Spalte aufgrund eines unzureichenden Längen Puffers abgeschnitten wird, gibt die API JET_wrnBufferTruncated zurück. Andere Fehler, JET_wrnColumnNull werden jedoch nur im Feld Fehler in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)zurückgegeben. Der Grund hierfür ist, dass Anwendungen häufig sicherstellen möchten, dass alle Daten abgerufen wurden, und diese Fehlermeldung von **jetretrievecolumschlag** zurückgeben.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[Jetenreeratecolumschlag](./jetenumeratecolumns-function.md)  
[Jetretrievecolumschlag](./jetretrievecolumn-function.md)  
[Jetsetcolumns](./jetsetcolumns-function.md)
