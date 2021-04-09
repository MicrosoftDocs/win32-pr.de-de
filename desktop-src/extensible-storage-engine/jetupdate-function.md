---
description: 'Weitere Informationen zu: jetupdate-Funktion'
title: JetUpdate-Funktion
TOCTitle: JetUpdate Function
ms:assetid: 6c9a53d0-46bc-403b-bdba-9020e023c14a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269288(v=EXCHG.10)
ms:contentKeyID: 32765580
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38e17c5bc5ac32ab3b904456f2d97aa465fca670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862892"
---
# <a name="jetupdate-function"></a>JetUpdate-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetupdate-function"></a>JetUpdate-Funktion

Die **jetupdate** -Funktion führt einen Aktualisierungs Vorgang aus, einschließlich des Einfügens einer neuen Zeile in eine Tabelle oder der Aktualisierung einer vorhandenen Zeile. Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von [jetdelete](./jetdelete-function.md).

**Jetupdate** ist der letzte Schritt beim Ausführen eines Einfügevorgangs oder eines Updates. Das Update wird zunächst durch Aufrufen von [jetprepareupdate](./jetprepareupdate-function.md) und anschließendes Aufrufen von [jetsetcolumn](./jetsetcolumn-function.md) oder [jetsetcolumns](./jetsetcolumns-function.md) gestartet, um den Daten Satz Status festzulegen. Schließlich wird **jetupdate** aufgerufen, um den Aktualisierungs Vorgang abzuschließen. Indizes werden nur von **jetupdate** oder [JetUpdate2](./jetupdate2-function.md)und nicht von [jetsetcolumn](./jetsetcolumn-function.md) oder [jetsetcolumns](./jetsetcolumns-function.md)aktualisiert.

```cpp
    JET_ERR JET_API JetUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*pvbookmark*

Zeiger auf ein zurück gegebenes Lesezeichen für eine eingefügte Zeile.

*cbbookmark*

Größe des Puffers, auf den *pvbookmark* zeigt.

*pcbactual*

Die zurückgegebene Größe des Lesezeichens für die eingefügte Zeile, die in *pvbookmark* zurückgegeben wurde.

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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Der angegebene Puffer für das Daten Satz-Lesezeichen ist nicht ausreichend groß genug zum Speichern des Daten Satz-Lesezeichens.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Identisch mit JET_errNullInvalid.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskFull</p></td>
<td><p>Der Aktualisierungs Vorgang erfordert eine Vergrößerung der Datenbankdatei oder die Protokolldatei Zuordnung, aber das Laufwerk, auf dem sich die Datenbankdatei oder die Protokoll Reihe befindet, ist voll. Alternativ dazu befindet sich die Datenbankdatei auf einem auf FAT32 formatierten Volume, und die Datenbankdatei ist bereits 4gbytes, der Grenzwert pro Datei für FAT32.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Der angegebene <em>prep</em> -Parameter in der <a href="gg269339(v=exchg.10).md">jetprepareupdate</a> -Funktion ist kein gültiges Flag.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyDuplicate</p></td>
<td><p>Ein Index Schlüssel für diesen Datensatz ist ein Duplikat eines anderen Index Schlüssels für einen anderen Datensatz, der bereits in der Tabelle vorhanden ist, und der Index lässt keine Duplikate zu.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyTruncated</p></td>
<td><p>Der eingefügte oder aktualisierte Datensatz weist mindestens einen Index auf, für den der generierte Schlüssel die maximal zulässige Größe überschreiten würde. Dies hat zur Folge, dass der Vorgang das Abschneiden von Schlüsseln nicht verhindern konnte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedIndexViolation</p></td>
<td><p>Der eingefügte oder aktualisierte Datensatz verfügt über eine indizierte mehrwertige Spalte mit zwei oder Mehrwerten, die innerhalb der für den Index festgelegten maximalen Längen Schlüsselgröße identisch sind. Folglich hat der Datensatz zwei identische Einträge im Index, die ungültig sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullInvalid</p></td>
<td><p>Mindestens eine Spalte im Datensatz, die eingefügt werden soll, oder der aktualisierte Zustand eines zu ersetzenden Datensatzes ist <strong>null</strong> . Dies verstößt gegen die definierte Einschränkung für diese Spalten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullKeyDisallowed</p></td>
<td><p>Mindestens ein Index ist so definiert, dass kein <strong>null</strong> -Schlüssel zulässig ist, und der eingefügte oder aktualisierte Status eines Datensatzes, der ersetzt wird, verstößt gegen diese definierte Einschränkung.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordPrimaryChanged</p></td>
<td><p>Der Primärschlüssel wurde durch einen Daten Satz Ersetzungs Vorgang aktualisiert. Aktualisierungen an Primärschlüssel Spalten müssen durch Löschen des vorhandenen Datensatzes und Einfügen eines neuen Datensatzes mit den gewünschten Daten erfolgen.</p></td>
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
<td><p>JET_errTransReadOnly</p></td>
<td><p>Es ist nicht zulässig, ein Update zu versuchen, wenn es innerhalb des Gültigkeits Bereichs einer schreibgeschützten Transaktion liegt. Eine schreibgeschützte Transaktion ist eine Transaktion, die mit einem <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> -Aufrufvorgang mit JET_bitTransactionReadOnly gestartet wurde.</p>
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p><a href="gg269339(v=exchg.10).md">Jetprepareupdate</a> wurde mit JET_prepCancel aufgerufen, aber der Cursor befand sich nicht im vorbereiteten Zustand.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher vorhanden ist, um transaktionale Informationen zum Update beizubehalten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Eine andere Sitzung hat den Datensatz bereits für das Update gesperrt. Das von dieser Sitzung versuchte Update schlägt fehl.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg ist der Aktualisierungs Vorgang für den Cursor abgeschlossen. Wenn für die Tabelle eine automatische Inkrement-Spalte definiert ist, wird dieser Wert für eingefügte Datensätze festgelegt. Wenn für die Tabelle eine Versions Spalte definiert ist, wird der Wert für neu eingefügte Datensätze initialisiert oder jedes Mal, wenn ein Datensatz ersetzt wird, um 1 erhöht. Alle Indizes, einschließlich gruppierter und nicht gruppierter Indizes, werden aktualisiert.

Bei einem Fehler werden keine Änderungen an der Datenbank vorgenommen. Vor dem Einfügen und vor dem ersetzen wurden möglicherweise Rückruf Funktionen aufgerufen, aber nach INSERT-und After-replace-Rückrufe wurden die Rückrufe nicht aufgerufen, da letztere nicht bewirken kann, dass ein Update fehlschlägt. Der Kopier Puffer des Cursors verbleibt im vorbereiteten Zustand, sodass die Möglichkeit besteht, die Probleme, die zu Fehlern geführt haben, inkrementell zu korrigieren und den Aktualisierungs Vorgang zu wiederholen.

#### <a name="remarks"></a>Bemerkungen

Rückruf Funktionen können registriert werden, um vor oder nach dem Einfügen und vor oder nach dem Update aufgerufen zu werden.

Einschränkungen der Daten Satz Größe werden von [jetsetcolumn](./jetsetcolumn-function.md)erzwungen, nicht im Allgemeinen durch **jetupdate**.

Es ist wichtig, die Auswirkungen der Ausführung einer großen Anzahl von Aktualisierungs Vorgängen in einer einzelnen Transaktion zu verstehen. Jedes Update der Datenbank muss von der Datenbank-Engine im Versionsspeicher nachverfolgt werden. Der Versionsspeicher enthält einen Live Datensatz aller verschiedenen Versionen der einzelnen Datensatz-oder Indexeinträge in der Datenbank, die von allen aktiven Transaktionen angezeigt werden können. Diese Versionen werden zur Unterstützung der Parallelitäts Steuerung mit mehreren Versionsverwaltung verwendet, die von der Datenbank-Engine verwendet wird, um Transaktionen mithilfe der Momentaufnahme Isolation zu unterstützen. Sobald die Datenbank-Engine die Ressourcen erschöpft hat, die zum Speichern dieser Versionen verwendet werden, kann Sie keine weiteren Änderungen mehr akzeptieren, bis einige Transaktionen abgeschlossen sind, damit diese Ressourcen freigegeben werden können. Wenn sich die Engine in diesem Zustand befindet, schlagen alle Updates mit Jet_errVersionStoreOutOfMemory fehl. Die Ressourcen, die für die Datenbank-Engine zum Speichern dieser Versionen verfügbar sind, können mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit [JET_paramMaxVerPages](./resource-parameters.md) und [JET_paramGlobalMinVerPages](./resource-parameters.md)gesteuert werden.

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
[Jetdelete](./jetdelete-function.md)  
[Jetprepareupdate](./jetprepareupdate-function.md)  
[Jetregistercallback](./jetregistercallback-function.md)  
[Jetretrievecolumschlag](./jetretrievecolumn-function.md)  
[Jetretrievecolumschlag](./jetretrievecolumns-function.md)  
[Jetsetcolumn](./jetsetcolumn-function.md)  
[Jetsetcolumns](./jetsetcolumns-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
