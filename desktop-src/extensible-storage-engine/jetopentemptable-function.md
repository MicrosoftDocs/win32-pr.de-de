---
description: 'Weitere Informationen zu: jetopentemptable-Funktion'
title: JetOpenTempTable-Funktion
TOCTitle: JetOpenTempTable Function
ms:assetid: 29261333-a1bc-4159-9046-c32c36f47410
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269211(v=EXCHG.10)
ms:contentKeyID: 32765514
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66c58abc5cff433bb4d944e39c283ba712d7cebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344246"
---
# <a name="jetopentemptable-function"></a>JetOpenTempTable-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopentemptable-function"></a>JetOpenTempTable-Funktion

Die **jetopentemptable** -Funktion erstellt eine temporäre Tabelle mit einem einzelnen Index. Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)erstellt wurde. Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird.

```cpp
    JET_ERR JET_API JetOpenTempTable(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die zu verwendende Sitzung.

*prgcolumndef*

Spaltendefinitionen für die Spalten, die in der temporären Tabelle erstellt werden.

**Wichtige**   Einschränkungen gelten für die Spalten Definitions Optionen, die für eine temporäre Tabelle verwendet werden. Weitere Informationen finden Sie im Abschnitt Hinweise.

Zusätzlich zu den üblichen Spalten Definitions Optionen können auch keine oder mehrere der folgenden Optionen angegeben werden, die nur im Kontext einer temporären Tabelle relevant sind.

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
<td><p>Die Sortierreihenfolge der Schlüssel Spalte für die temporäre Tabelle sollte absteigend und nicht aufsteigend sein. Wenn diese Option ohne JET_bitColumnTTKey angegeben wird, wird diese Option ignoriert.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Die Spalte ist eine Schlüssel Spalte für die temporäre Tabelle.</p>
<p>Die Reihenfolge der Spaltendefinitionen, bei denen diese Option im Eingabe Array angegeben ist, bestimmt die Rangfolge der einzelnen Schlüssel Spalten für die temporäre Tabelle. Die erste Spaltendefinition im Array, für die diese Option festgelegt ist, ist die wichtigste Schlüssel Spalte usw. Wenn mehr Schlüssel Spalten angefordert werden, als von der Datenbank-Engine unterstützt werden können, wird diese Option für die nicht supportablen Schlüssel Spalten ignoriert.</p></td>
</tr>
</tbody>
</table>


*CColumn*

Siehe *prgcolumndef*.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.

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
<td><p>Jeder Versuch, einen Datensatz mit dem gleichen Index Schlüssel wie ein zuvor eingefügter Datensatz einzufügen, schlägt mit JET_errKeyDuplicate sofort fehl. Wenn diese Option nicht angefordert wird, wird sofort ein Duplikat erkannt, und es wird ein Fehler zurückgegeben. Dies hängt von der Strategie ab, die von der Datenbank-Engine zum Implementieren der temporären Tabelle basierend auf der angeforderten Funktionalität gewählt wurde.</p>
<p>Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern. Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForceMaterialization</p></td>
<td><p>Zwingt den temporären Tabellen-Manager, die Suche nach der optimalen Strategie zu verwerfen, um die Verwaltung der temporären Tabelle zu verbessern, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTForwardOnly</p></td>
<td><p>Die temporäre Tabelle wird nur erstellt, wenn der temporäre Tabellen-Manager die-Implementierung verwenden kann, die für zwischen Abfrageergebnisse optimiert ist. Wenn ein beliebiges Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, schlägt der Vorgang mit JET_errCannotMaterializeForwardOnlySort fehl.</p>
<p>Ein Nebeneffekt dieser Option besteht darin, zuzulassen, dass die temporäre Tabelle Datensätze mit doppelten Index Schlüsseln enthält. Weitere Informationen finden Sie unter JET_bitTTUnique.</p>
<p>Diese Option ist nur für Windows Server 2003 und spätere Versionen verfügbar.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTIndexed</p></td>
<td><p>Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, um die Verwendung von <a href="gg294103(v=exchg.10).md">JetSeek</a> für die Suche nach Datensätzen nach Index Schlüssel zuzulassen.</p>
<p>Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern. Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTUnique</p></td>
<td><p>Fordert an, dass Datensätze mit doppelten Index Schlüsseln aus dem endgültigen Satz von Datensätzen in der temporären Tabelle entfernt werden.</p>
<p>Vor Windows Server 2003 hat die Datenbank-Engine immer angenommen, dass diese Option wirksam ist, weil alle gruppierten Indizes auch ein Primärschlüssel sein müssen und daher eindeutig sein müssen. Ab Windows Server 2003 ist es möglich, eine temporäre Tabelle zu erstellen, die keine Duplikate entfernt, wenn die JET_bitTTForwardOnly-Option ebenfalls angegeben ist.</p>
<p>Im Allgemeinen ist es nicht möglich, zu ermitteln, welches Duplikat erfolgreich ist und welche Duplikate verworfen werden. Wenn jedoch die JET_bitTTErrorOnDuplicateInsertion-Option angefordert wird, ist der erste Datensatz mit einem bestimmten Index Schlüssel, der in die temporäre Tabelle eingefügt werden soll, immer erfolgreich.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTUpdatable</p></td>
<td><p>Fordert an, dass die temporäre Tabelle flexibel genug ist, damit Datensätze, die zuvor eingefügt wurden, geändert werden können. Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</p>
<p>Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTScrollable</p></td>
<td><p>Fordert an, dass die temporäre Tabelle flexibel genug ist, um das Scannen von Datensätzen in beliebiger Reihenfolge und Richtung mithilfe von <a href="gg294117(v=exchg.10).md">jetmove</a>zuzulassen.</p>
<p>Wenn diese Funktionalität nicht erforderlich ist, ist es am besten, Sie nicht anzufordern. Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTSortNullsHigh</p></td>
<td><p>Fordert an, dass NULL-Schlüssel Spaltenwerte näher am Ende des Indexes liegen als Schlüssel Spaltenwerte ungleich NULL.</p>
<p></p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTIntrinsicLVsOnly</p></td>
<td><p>Anforderungen, um nur systeminterne Long-Werte zuzulassen.</p>
<p><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> wurde in Windows 7 eingeführt.</p></td>
</tr>
</tbody>
</table>


*pTableID*

Der Ausgabepuffer, der den neuen Cursor empfängt, der in der neu erstellten temporären Tabelle geöffnet wurde.

*prgcolumnid*

Der Ausgabepuffer, der das Array der Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden.

Die Spalten-IDs in diesem Array entsprechen exakt dem Eingabe Array von Spaltendefinitionen. Folglich muss die Größe dieses Puffers der Größe des Eingabe Arrays entsprechen.

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
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p>Fehler bei <strong>jetopentemptable</strong> , weil JET_bitTTForwardOnly angegeben wurde und die temporäre Tabelle wie angegeben nicht mithilfe der vorwärts Optimierung erstellt werden konnte. Dieser Fehler wird nur von Windows Server 2003 und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Der Index konnte nicht erstellt werden, da eine ungültige Index Definition angegeben wurde.</p>
<p><strong>Jetopertemptable</strong> gibt den folgenden Fehler zurück:</p>
<ul>
<li><p>Das sprachneutrale Gebiets Schema ist angegeben.</p></li>
<li><p>Es wurde ein ungültiger Satz von normalisierungs Flags angegeben.</p></li>
</ul>
<p>Dieser Fehler wird nur von Windows 2000 zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Das CP-Feld des <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Das <em>colyp</em> -Feld des <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf einen gültigen Spaltentyp festgelegt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Der Index konnte nicht erstellt werden, da versucht wurde, eine ungültige Gebiets Schema-ID zu verwenden. Die Gebiets Schema-ID ist möglicherweise vollständig ungültig, oder das zugehörige Sprachpaket ist möglicherweise nicht installiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>Der Index konnte nicht erstellt werden, da versucht wurde, einen ungültigen Satz von normalisierungs Flags zu verwenden. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben. Bei Windows 2000 resultieren ungültige normalisierungs Flags stattdessen JET_errIndexInvalidDef.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>Das Sitzungs Handle ist ungültig oder verweist auf eine geschlossene Sitzung.</p>
<p><strong>Hinweis</strong>  Dieser Fehler wird unter allen Umständen nicht zurückgegeben. Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine die zum Öffnen eines neuen Cursors erforderlichen Ressourcen nicht zuordnen kann. Cursor Ressourcen werden mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>konfiguriert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</p>
<p><strong>Jetopertemptable</strong> kann JET_errOutOfMemory zurückgeben, wenn der Adressraum des Host Prozesses zu fragmentiert wird. Der temporäre Tabellen-Manager weist immer einen 1-MB-Adressraum für jede temporäre Tabelle zu, die unabhängig von der zu speichernden Datenmenge erstellt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p>Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle kann nicht mehr als JET_ccolFixedMost fester Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierte Spalten aufweisen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern der Indizes der Tabelle erforderlichen Ressourcen nicht zuordnen kann. Die Anzahl der Indizes, deren Schema zwischengespeichert werden kann, wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>konfiguriert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern des Schemas der Tabelle erforderlichen Ressourcen nicht zuordnen kann. Die Anzahl der Tabellen, deren Schema zwischengespeichert werden kann, wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>konfiguriert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine die zum Erstellen einer temporären Tabelle erforderlichen Ressourcen nicht zuordnen kann. Temporäre Tabellen Ressourcen werden mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>konfiguriert.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird ein Cursor zurückgegeben, der für die neu erstellte temporäre Tabelle geöffnet wurde. Der Status der temporären Datenbank wird darauf vorbereitet, die neue temporäre Tabelle zu enthalten. Der Status aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

Bei einem Fehler wird die temporäre Tabelle nicht erstellt, und ein Cursor wird nicht zurückgegeben. Der Status der temporären Datenbank kann geändert werden. Der Status aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

#### <a name="remarks"></a>Bemerkungen

Temporäre Tabellen unterstützen nicht die vollständige Ergänzung der Spalten Definitions Optionen, die normalerweise von der Datenbank-Engine unterstützt werden. Tatsächlich werden nur JET_bitColumnFixed und JET_bitColumnTagged unterstützt. Dies bedeutet, dass es nicht möglich ist, eine automatische Inkrement-, Versions-oder mehrwertige Spalte in einer temporären Tabelle zu erstellen. Zum Schluss werden die Spalten zum Aktualisieren von Spalten nicht unterstützt, da Sie in einer temporären Tabelle nicht nützlich sind, da Sie nur von einer Sitzung gleichzeitig verwendet werden können. Wenn eine dieser Optionen angefordert wird, werden Sie ignoriert.

Temporäre Tabellen unterstützen keine Standardwerte. Wenn eine Spaltendefinition bereitgestellt wird, die eine Standardwert Spezifikation enthält, wird diese Angabe ignoriert.

Temporäre Tabellen werden als Ergebnis vieler unterschiedlicher ESE-Funktionen an den Aufrufer zurückgegeben. Beispielsweise gibt [jetgetindexinfo](./jetgetindexinfo-function.md) mit der JET_IdxInfo-Option, die im *infolevel* -Parameter festgelegt ist, eine temporäre Tabelle zurück, die eine Liste aller Schlüssel Spalten in einem bestimmten Index enthält. Die temporären Tabellen folgen den gleichen Lebenszyklus Regeln wie gewöhnliche temporäre Tabellen, wie hier beschrieben.

Temporäre Tabellen werden auch intern von der Datenbank-Engine für viele Tasks verwendet. Die wichtigsten dieser Aufgaben sind die Erstellung eines Indexes für eine vorhandene Tabelle. Eine temporäre Tabelle wird zum Sortieren der Index Schlüssel verwendet, die zum Erstellen dieses Indexes verwendet werden.

Alle temporären Tabellen werden in der temporären Datenbank gespeichert. Die temporäre Datenbank ist eine spezielle Datenbankdatei, die während der Lebensdauer einer ESE-Instanz verwaltet wird und gelöscht wird, wenn diese Instanz heruntergefahren oder neu gestartet wird. Der Speicherort der temporären Datenbank kann mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit [JET_paramTempPath](./temporary-database-parameters.md)konfiguriert werden. Die Platzierung der temporären Datenbank auf dem Datenträger in Relation zu den Transaktionsprotokoll Dateien und Datenbankdateien ist möglicherweise wichtig, wenn die Anwendung temporäre Tabellen stark nutzt oder häufig Indizes erstellt.

Der Lebenszyklus einer temporären Tabelle ist an die Cursor gebunden, die auf diese Tabelle verweisen. Wenn alle Cursor, die auf eine temporäre Tabelle verweisen, entweder implizit oder explizit geschlossen werden, wird die temporäre Tabelle gelöscht. Wenn eine temporäre Tabelle innerhalb einer Transaktion erstellt wird und anschließend ein Rollback für diese Transaktion ausgeführt wird, wird die temporäre Tabelle gelöscht, da alle Cursor, auf die Sie zu diesem Zeitpunkt verwiesen hat, implizit geschlossen werden. Neue Cursor können nur durch die Verwendung von [jetdupcursor](./jetdupcursor-function.md)auf eine temporäre Tabelle verweisen. In diesem Fall werden die neuen Cursor auf dem ersten Index Eintrag der temporären Tabelle positioniert. [Jetdupcursor](./jetdupcursor-function.md) funktioniert nur in bestimmten Phasen der Verwendung für die temporäre Tabelle. Weitere Informationen finden Sie in den Hinweisen zu den Cursor Funktionen für temporäre Tabellen. Es ist nicht möglich, auf eine temporäre Tabelle von mehreren Sitzungen gleichzeitig zu verweisen.

In [jetdupcursor](./jetdupcursor-function.md) liegt ein wichtiges Problem vor, das sich auf temporäre Tabellen auswirkt. Wenn versucht wird, eine temporäre Tabelle zu duplizieren, die sich im vorwärts Modus befindet, wird der resultierende Cursor nicht ordnungsgemäß erstellt und funktioniert nicht. Es ist immer noch sicher, einen Cursor über eine materialisierte temporäre Tabelle zu duplizieren.

Der temporäre Tabellen-Manager kann eine temporäre Tabelle auf drei Arten implementieren. Die erste Methode besteht darin, eine in-Memory-Tabelle beizubehalten. Diese Strategie ist der schnellste, kann aber nur für kleine, einfache temporäre Tabellen verwendet werden. Die zweite Methode besteht darin, eine Datenträger basierte Sortierung zu erstellen, die mit einem vorwärts-Iterator gesteuert werden kann. Diese Strategie kann nur unter bestimmten Umständen verwendet werden und ist die schnellste Möglichkeit, Duplikate aus einem sehr großen Dataset zu sortieren und zu entfernen. Die dritte Methode ist das Erstellen einer B +-Struktur in der temporären Datenbank, um die temporäre Tabelle zu speichern. Diese Strategie ist die langsamste, aber die vielseitigste und wird als materialisierte temporäre Tabelle bezeichnet. Diese Strategien können in Kombination verwendet werden, um letztendlich die von der temporären Tabelle angeforderte Funktionalität zu erreichen.

Wenn die temporäre Tabelle nicht materialisiert ist, wird Sie in erster Linie in zwei Hauptphasen verwendet. Die erste Phase ist die Einfügungs Phase, in der die Tabelle mit dem ersten DataSet aufgefüllt wird. In dieser Phase ist nur die Daten Einfügung zulässig. Diese Phase endet, wenn versucht wird, den Cursor mithilfe von [jetmove](./jetmove-function.md) oder [JetSeek](./jetseek-function.md)zu verschieben. Die zweite Phase ist die Daten Extraktions Phase. In dieser Phase können die in der temporären Tabelle gespeicherten Daten gemäß den Funktionen extrahiert werden, die beim Erstellen der temporären Tabelle angefordert wurden.

**Cursor Funktionen für temporäre Tabellen**

Wenn die temporäre Tabelle materialisiert ist, verfügt der Cursor über die folgenden Funktionen, kann jedoch durch die angeforderten Optionen weiter eingeschränkt werden:

  - [Jetclosetable](./jetclosetable-function.md)

  - [Jetdelete](./jetdelete-function.md)

  - [Jetdupcursor](./jetdupcursor-function.md)

  - [Jetenreeratecolumschlag](./jetenumeratecolumns-function.md)

  - [Jetescrowupdate](./jetescrowupdate-function.md)

  - [Jetgetbookmark](./jetgetbookmark-function.md)

  - [Jetgetcursor Info](./jetgetcursorinfo-function.md)

  - [Jetgetls](./jetgetls-function.md)

  - [Jetgetrecordsize](./jetgetrecordsize-function.md)

  - [Jetgettableinfo](./jetgettableinfo-function.md)

  - [Jetgojebookmark](./jetgotobookmark-function.md)

  - [Jetmakekey](./jetmakekey-function.md)

  - [Jetmove](./jetmove-function.md)

  - [Jetprepareupdate](./jetprepareupdate-function.md)

  - [Jetretrievecolumschlag](./jetretrievecolumn-function.md)

  - [Jetretrievecolumschlag](./jetretrievecolumns-function.md)

  - [Jetretrievekey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [Jetsetcolumn](./jetsetcolumn-function.md)

  - [Jetsetcolumns](./jetsetcolumns-function.md)

  - [Jetsetindexrange](./jetsetindexrange-function.md)

  - [Jetsetls](./jetsetls-function.md)

  - [Jetupdate](./jetupdate-function.md)

Wenn die temporäre Tabelle nicht materialisiert wird und sich in der einfügephase befindet, verfügt der Cursor über die folgenden Funktionen, kann jedoch durch die angeforderten Optionen weiter eingeschränkt werden:

  - [Jetclosetable](./jetclosetable-function.md)

  - [Jetescrowupdate](./jetescrowupdate-function.md)

  - [Jetmakekey](./jetmakekey-function.md)

  - [Jetmove](./jetmove-function.md)
    
    **Hinweis**  Bewirkt einen Übergang zur Extrahierungs Phase.

  - [Jetprepareupdate](./jetprepareupdate-function.md)

  - [Jetretrievekey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)
    
    **Hinweis**  Bewirkt einen Übergang zur Extrahierungs Phase.

  - [Jetsetcolumn](./jetsetcolumn-function.md)

  - [Jetsetcolumns](./jetsetcolumns-function.md)

  - [Jetupdate](./jetupdate-function.md)

Wenn die temporäre Tabelle nicht materialisiert wird und sich in der Extrahierungs Phase befindet, verfügt der Cursor über die folgenden Funktionen, kann jedoch durch die angeforderten Optionen weiter eingeschränkt werden:

  - [Jetclosetable](./jetclosetable-function.md)

  - [Jetdupcursor](./jetdupcursor-function.md)
    
    **Hinweis**  Wenn versucht wird, eine temporäre Tabelle zu duplizieren, die sich im vorwärts Modus befindet, wird der resultierende Cursor nicht ordnungsgemäß erstellt und funktioniert nicht. Es ist immer noch sicher, einen Cursor über eine materialisierte temporäre Tabelle zu duplizieren.

  - [Jetenreeratecolumschlag](./jetenumeratecolumns-function.md)

  - [Jetgetbookmark](./jetgetbookmark-function.md)

  - [Jetgetls](./jetgetls-function.md)

  - [Jetgetrecordsize](./jetgetrecordsize-function.md)

  - [Jetgettableinfo](./jetgettableinfo-function.md)

  - [Jetgojebookmark](./jetgotobookmark-function.md)

  - [Jetmakekey](./jetmakekey-function.md)

  - [Jetmove](./jetmove-function.md)

  - [Jetretrievecolumschlag](./jetretrievecolumn-function.md)

  - [Jetretrievecolumschlag](./jetretrievecolumns-function.md)

  - [Jetretrievekey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [Jetsetindexrange](./jetsetindexrange-function.md)

  - [Jetsetls](./jetsetls-function.md)

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

[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[Jetclosetable](./jetclosetable-function.md)  
[Jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)  
[Jetdupcursor](./jetdupcursor-function.md)  
[Jetmove](./jetmove-function.md)  
[Jetrollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[Temporäre Daten Bank Parameter](./temporary-database-parameters.md)
