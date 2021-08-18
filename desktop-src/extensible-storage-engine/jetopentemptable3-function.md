---
description: Weitere Informationen finden Sie unter JetOpenTempTable3-Funktion.
title: JetOpenTempTable3-Funktion
TOCTitle: JetOpenTempTable3 Function
ms:assetid: 58d6e264-705e-402b-928f-96eefe5e9771
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269255(v=EXCHG.10)
ms:contentKeyID: 32765557
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable3
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 616a1a5a93c10ae79894c81e4530edc618848716190b887f16e850f89e3a79e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978815"
---
# <a name="jetopentemptable3-function"></a>JetOpenTempTable3-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopentemptable3-function"></a>JetOpenTempTable3-Funktion

Die **JetOpenTempTable3-Funktion** erstellt eine temporäre Tabelle mit einem einzelnen Index, der zum Speichern und Abrufen von Datensätzen verwendet werden kann, genau wie eine normale Tabelle, die mit [JetCreateTableColumnIndex erstellt wurde.](./jetcreatetablecolumnindex-function.md) Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um sehr schnell zu sortieren und doppelte Entfernungen für Datensatzgruppen durchzuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird.

```cpp
    JET_ERR JET_API JetOpenTempTable3(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in_opt      JET_UNICODEINDEX* pidxunicode,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*prgcolumndef*

Identifiziert die Spaltendefinitionen der Spalten, die in der temporären Tabelle erstellt werden sollen.

Für die Spaltendefinitionsoptionen, die mit einer temporären Tabelle verwendet werden können, gelten wichtige Einschränkungen. Weitere Informationen finden Sie im Abschnitt Hinweise.

Zusätzlich zu den üblichen Spaltendefinitionsoptionen können null oder mehr der folgenden Optionen angegeben werden, die nur im Kontext einer temporären Tabelle relevant sind.

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
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Diese Option gibt an, dass die Sortierreihenfolge der Schlüsselspalte für die temporäre Tabelle absteigend und nicht aufsteigend sein sollte. Wenn diese Option ohne JET_bitColumnTTKey angegeben wird, wird diese Option ignoriert.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Diese Option gibt an, dass die Spalte eine Schlüsselspalte für die temporäre Tabelle ist.</p>
<p>Die Reihenfolge der Spaltendefinitionen mit dieser Option, die im Eingabearray angegeben ist, bestimmt die Rangfolge der einzelnen Schlüsselspalten für die temporäre Tabelle. Die erste Spaltendefinition im Array, für die diese Option festgelegt ist, ist die wichtigste Schlüsselspalte und so weiter. Wenn mehr Schlüsselspalten angefordert werden, als von der Datenbank-Engine unterstützt werden können, wird diese Option für die nicht unterstützten Schlüsselspalten ignoriert.</p></td>
</tr>
</tbody>
</table>


*ccolumn*

Siehe *prgcolumndef*.

*pidxunicode*

Die Locale ID- und Normalisierungsflags, die zum Vergleichen von Unicode-Schlüsselspaltendaten in der temporären Tabelle verwendet werden.

Wenn dieser Parameter nicht vorhanden ist, wird die Standard-LCID verwendet, um alle Unicode-Schlüsselspalten in der temporären Tabelle zu vergleichen. Die Standard-LCID ist das us-englische Locale.

Wenn dieser Parameter nicht vorhanden ist, werden die Standardnormalisierungsflags verwendet, um Unicode-Schlüsselspaltendaten in der temporären Tabelle zu vergleichen. Die Standardnormalisierungsflags sind: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten.

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
<td><p>JET_bitTTErrorOnDuplicateInsertion</p></td>
<td><p>Diese Option fordert an, dass jeder Versuch, einen Datensatz mit demselben Indexschlüssel wie ein zuvor eingefügter Datensatz einfüge, sofort fehlschlägt, JET_errKeyDuplicate. Wenn diese Option nicht angefordert wird, wird möglicherweise sofort ein Duplikat erkannt, das fehlschlägt oder später automatisch entfernt wird. Dies hängt von der Strategie ab, die von der Datenbank-Engine gewählt wurde, um die temporäre Tabelle basierend auf der angeforderten Funktionalität zu implementieren.</p>
<p>Wenn diese Funktionalität nicht erforderlich ist, sollten Sie sie nicht anfordern. Wenn diese Funktionalität nicht angefordert wird, kann der Manager für temporäre Tabellen möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForceMaterialization</p></td>
<td><p>Diese Option zwingt den temporären Tabellen-Manager, jeglichen Versuch zu verabschlagen, eine clevere Strategie für die Verwaltung der temporären Tabelle zu wählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTForwardOnly</p></td>
<td><p>Diese Option fordert an, dass die temporäre Tabelle nur erstellt wird, wenn der temporäre Tabellen-Manager die für Zwischenabfrageergebnisse optimierte Implementierung verwenden kann. Wenn ein Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, kann der Vorgang nicht durchgeführt JET_errCannotMaterializeForwardOnlySort.</p>
<p>Ein Nebeneffekt dieser Option besteht im Zulassen, dass die temporäre Tabelle Datensätze mit doppelten Indexschlüsseln enthält. Weitere JET_bitTTUnique finden Sie unter .</p>
<p>Diese Option ist nur auf Windows Server 2003 und höher verfügbar.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTIndexed</p></td>
<td><p>Diese Option fordert, dass die temporäre Tabelle flexibel genug ist, um die Verwendung von <a href="gg294103(v=exchg.10).md">JetSeek</a> zum Suchen von Datensätzen nach Indexschlüsseln zu ermöglichen.</p>
<p>Wenn diese Funktionalität nicht erforderlich ist, sollten Sie sie nicht anfordern. Wenn diese Funktionalität nicht angefordert wird, kann der Manager für temporäre Tabellen möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTUnique</p></td>
<td><p>Diese Option fordert an, dass Datensätze mit doppelten Indexschlüsseln aus dem letzten Satz von Datensätzen in der temporären Tabelle entfernt werden.</p>
<p>Vor Windows Server 2003 hat die Datenbank-Engine diese Option immer als wirksam angenommen, da alle gruppierten Indizes ebenfalls ein Primärschlüssel sein müssen und daher eindeutig sein müssen. Ab Windows Server 2003 ist es jetzt möglich, eine temporäre Tabelle zu erstellen, die keine Duplikate entfernt, wenn die option JET_bitTTForwardOnly angegeben ist.</p>
<p>Es ist nicht möglich zu wissen, welches Duplikat gewinnt und welche Duplikate im Allgemeinen verworfen werden. Wenn jedoch die JET_bitTTErrorOnDuplicateInsertion angefordert wird, wird der erste Datensatz mit einem bestimmten Indexschlüssel, der in die temporäre Tabelle eingefügt werden soll, immer gewonnen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTUpdatable</p></td>
<td><p>Diese Option fordert, dass die temporäre Tabelle flexibel genug ist, damit datensätze, die zuvor eingefügt wurden, anschließend geändert werden können. Wenn diese Funktionalität nicht erforderlich ist, sollten Sie sie nicht anfordern.</p>
<p>Wenn diese Funktionalität nicht angefordert wird, kann der Manager für temporäre Tabellen möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTScrollable</p></td>
<td><p>Diese Option fordert, dass die temporäre Tabelle flexibel genug ist, damit Datensätze in beliebiger Reihenfolge und Richtung mit <a href="gg294117(v=exchg.10).md">JetMove gescannt werden können.</a></p>
<p>Wenn diese Funktionalität nicht erforderlich ist, sollten Sie sie nicht anfordern. Wenn diese Funktionalität nicht angefordert wird, kann der Manager für temporäre Tabellen möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTSortNullsHigh</p></td>
<td><p>Diese Option fordert an, dass Nullschlüsselspaltenwerte näher am Ende des Indexes sortiert werden als Spaltenwerte, die keine NULL-Schlüsselspalten sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTIntrinsicLVsOnly</p></td>
<td><p>Anforderungen, die nur systeminterne Long-Werte zulassen.</p>
<p><strong>Windows 7:</strong> <strong>JET_bitTTIntrinsicLVsOnly</strong> wird in Windows 7 eingeführt.</p></td>
</tr>
</tbody>
</table>


*Ptableid*

Der Ausgabepuffer, der den neuen Cursor erhält, der in der neu erstellten temporären Tabelle geöffnet wird.

*prgcolumnid*

Der Ausgabepuffer, der das Array von Spalten-IDs erhält, die während der Erstellung der temporären Tabelle generiert wurden.

Die Spalten-IDs in diesem Array entsprechen genau dem Eingabearray von Spaltendefinitionen. Daher muss die Größe dieses Puffers der Größe des Eingabearrays entsprechen.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR-Datentyp](./jet-err.md) mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p><strong>Fehler bei JetOpenTempTable3,</strong> JET_bitTTForwardOnly angegeben wurde und die temporäre Tabelle wie angegeben nicht mit der Vorwärtsoptimierung erstellt werden konnte. Dieser Fehler wird nur von Windows Server 2003 und höher zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Der Index konnte nicht erstellt werden, da eine ungültige Indexdefinition angegeben wurde. <strong>JetOpenTempTable3 gibt</strong> diesen Fehler zurück, wenn:</p>
<ul>
<li><p>Das sprachneutrale -Locale wird angegeben.</p></li>
<li><p>Es wird ein ungültiger Satz von Normalisierungsflags angegeben.</p></li>
</ul>
<p>Dieser Fehler wird nur von Windows 2000 zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Der <strong>cp-Member</strong> der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF-Struktur</a> wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Der <strong>Coltyp-Member</strong> der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf einen gültigen Spaltentyp festgelegt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Der Index konnte nicht erstellt werden, da versucht wurde, eine ungültige Locale ID zu verwenden. Die Locale-ID ist möglicherweise vollständig ungültig, oder das zugeordnete Sprachpaket ist möglicherweise nicht installiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>Der Index konnte nicht erstellt werden, weil versucht wurde, einen ungültigen Satz von Normalisierungsflags zu verwenden. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben. In Windows 2000 führen ungültige Normalisierungsflags stattdessen zu JET_errIndexInvalidDef.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>Das Sitzungshandy ist ungültig oder verweist auf eine geschlossene Sitzung. Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Öffnen eines neuen Cursors erforderlich sind. Cursorressourcen werden mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mit JET_paramMaxCursors.</a> <a href="gg269201(v=exchg.10).md"></a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Fehler beim Vorgang, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um ihn abschließen zu können.</p>
<p><strong>JetOpenTempTable3 kann</strong> JET_errOutOfMemory zurückgeben, wenn der Adressraum des Hostprozesses zu fragmentiert wird. Der temporäre Tabellen-Manager ordnet für jede temporäre Tabelle, die erstellt wird, immer einen Adressraum von 1 MB zu, unabhängig von der zu speichernden Datenmenge.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p>
<p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle kann nicht mehr als JET_ccolFixedMost Spalten enthalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierte Spalten.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Zwischenspeichern der Indizes der Tabelle erforderlich sind. Die Anzahl der Indizes, deren Schema zwischengespeichert werden kann, wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mit</a> <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>Fehler beim Vorgang, da die Engine nicht die Ressourcen zuordnen kann, die zum Zwischenspeichern des Schemas der Tabelle erforderlich sind. Die Anzahl der Tabellen, deren Schema zwischengespeichert werden kann, wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mit</a> <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Erstellen einer temporären Tabelle erforderlich sind. Temporäre Tabellenressourcen werden mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter und</a> <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables.</a></p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird ein Cursor zurückgegeben, der in der neu erstellten temporären Tabelle geöffnet wird. Der Status der temporären Datenbank wird so vorbereitet, dass er die neue temporäre Tabelle enthält. Der Status normaler Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

Bei einem Fehler wird die temporäre Tabelle nicht erstellt, und es wird kein Cursor zurückgegeben. Der Status der temporären Datenbank kann geändert werden. Der Status normaler Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

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
<td><p>Wird in Esent.h deklariert.</p></td>
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

[Erweiterbare Storage Engine-Fehler](./extensible-storage-engine-errors.md)  
[Fehlerbehandlungsparameter](./error-handling-parameters.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetMove](./jetmove-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
