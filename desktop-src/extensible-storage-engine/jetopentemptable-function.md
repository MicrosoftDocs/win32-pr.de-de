---
description: Weitere Informationen finden Sie unter JetOpenTempTable-Funktion.
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
ms.openlocfilehash: 0f2aa3fdd1ae95fa377f65b5422a2a236868fc62
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469767"
---
# <a name="jetopentemptable-function"></a>JetOpenTempTable-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopentemptable-function"></a>JetOpenTempTable-Funktion

Die **JetOpenTempTable-Funktion** erstellt eine temporäre Tabelle mit einem einzelnen Index. Eine temporäre Tabelle speichert und ruft Datensätze genau wie eine normale Tabelle ab, die mit [JetCreateTableColumnIndex erstellt wurde.](./jetcreatetablecolumnindex-function.md) Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um sehr schnell zu sortieren und doppelte Entfernungen für Datensatzgruppen durchzuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird.

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

*sesid*

Die zu verwendende Sitzung.

*prgcolumndef*

Spaltendefinitionen für die in der temporären Tabelle erstellten Spalten.

**Für**   die Spaltendefinitionsoptionen, die mit einer temporären Tabelle verwendet werden, gelten wichtige Einschränkungen. Weitere Informationen finden Sie im Abschnitt Hinweise.

Zusätzlich zu den üblichen Spaltendefinitionsoptionen können 0 oder mehr der folgenden Optionen angegeben werden, die nur im Kontext einer temporären Tabelle relevant sind.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>Die Sortierreihenfolge der Schlüsselspalte für die temporäre Tabelle sollte absteigend und nicht aufsteigend sein. Wenn diese Option ohne JET_bitColumnTTKey angegeben wird, wird diese Option ignoriert.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Die Spalte ist eine Schlüsselspalte für die temporäre Tabelle.</p><p>Die Reihenfolge der Spaltendefinitionen mit dieser Option, die im Eingabearray angegeben ist, bestimmt die Rangfolge der einzelnen Schlüsselspalten für die temporäre Tabelle. Die erste Spaltendefinition im Array, für die diese Option festgelegt ist, ist die wichtigste Schlüsselspalte und so weiter. Wenn mehr Schlüsselspalten angefordert werden, als von der Datenbank-Engine unterstützt werden können, wird diese Option für die nicht unterstützten Schlüsselspalten ignoriert.</p> | 



*ccolumn*

Siehe *prgcolumndef*.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen an geben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Jeder Versuch, einen Datensatz mit demselben Indexschlüssel wie ein zuvor eingefügter Datensatz einfüge, würde sofort JET_errKeyDuplicate. Wenn diese Option nicht angefordert wird, wird sofort ein Duplikat erkannt und schlägt fehl oder wird später automatisch entfernt. Dies hängt von der Strategie ab, die die Datenbank-Engine für die Implementierung der temporären Tabelle basierend auf der angeforderten Funktionalität gewählt hat.</p><p>Wenn diese Funktionalität nicht erforderlich ist, sollten Sie sie nicht anfordern. Wenn diese Funktionalität nicht angefordert wird, kann der Manager für temporäre Tabellen möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Zwingt den temporären Tabellen-Manager, die Suche nach der besten Strategie aufzugeben, um die Verwaltung der temporären Tabelle zu verwenden, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>Die temporäre Tabelle wird nur erstellt, wenn der Temporäre Tabellen-Manager die Implementierung verwenden kann, die für Zwischenabfrageergebnisse optimiert ist. Wenn ein Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, kann der Vorgang nicht durchgeführt JET_errCannotMaterializeForwardOnlySort.</p><p>Ein Nebeneffekt dieser Option besteht im Zulassen, dass die temporäre Tabelle Datensätze mit doppelten Indexschlüsseln enthält. Weitere JET_bitTTUnique finden Sie unter .</p><p>Diese Option ist nur auf Windows Server 2003 und höher verfügbar.</p> | 
| <p>JET_bitTTIndexed</p> | <p>Diese Option fordert, dass die temporäre Tabelle flexibel genug ist, um die Verwendung von <a href="gg294103(v=exchg.10).md">JetSeek</a> zum Suchen von Datensätzen nach Indexschlüsseln zu ermöglichen.</p><p>Wenn diese Funktionalität nicht erforderlich ist, sollten Sie sie nicht anfordern. Wenn diese Funktionalität nicht angefordert wird, kann der Manager für temporäre Tabellen möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTUnique</p> | <p>Anforderungen, dass Datensätze mit doppelten Indexschlüsseln aus dem letzten Satz von Datensätzen in der temporären Tabelle entfernt werden.</p><p>Vor Windows Server 2003 hat die Datenbank-Engine diese Option immer als wirksam angenommen, da alle gruppierten Indizes ebenfalls ein Primärschlüssel sein müssen und daher eindeutig sein müssen. Ab Windows Server 2003 ist es jetzt möglich, eine temporäre Tabelle zu erstellen, die keine Duplikate entfernt, wenn die option JET_bitTTForwardOnly angegeben wird.</p><p>Es ist nicht möglich zu wissen, welches Duplikat erfolgreich ist und welche Duplikate im Allgemeinen verworfen werden. Wenn jedoch die JET_bitTTErrorOnDuplicateInsertion angefordert wird, ist der erste Datensatz mit einem bestimmten Indexschlüssel, der in die temporäre Tabelle eingefügt werden soll, immer erfolgreich.</p> | 
| <p>JET_bitTTUpdatable</p> | <p>Fordert an, dass die temporäre Tabelle flexibel genug ist, damit datensätze, die zuvor eingefügt wurden, später geändert werden können. Wenn diese Funktionalität nicht erforderlich ist, sollten Sie sie nicht anfordern.</p><p>Wenn diese Funktionalität nicht angefordert wird, kann der Manager für temporäre Tabellen möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTScrollable</p> | <p>Fordert an, dass die temporäre Tabelle flexibel genug ist, damit Datensätze in beliebiger Reihenfolge und Richtung mit <a href="gg294117(v=exchg.10).md">JetMove gescannt werden können.</a></p><p>Wenn diese Funktionalität nicht erforderlich ist, sollten Sie sie nicht anfordern. Wenn diese Funktionalität nicht angefordert wird, kann der Manager für temporäre Tabellen möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>Fordert an, dass NULL-Schlüsselspaltenwerte näher am Ende des Indexes sortiert werden als Spaltenwerte, die keine NULL-Schlüsselspalten sind.</p><p></p> | 
| <p>JET_bitTTIntrinsicLVsOnly</p> | <p>Anforderungen, die nur systeminterne Long-Werte zulassen.</p><p><strong>Windows 7:</strong> <strong>JET_bitTTIntrinsicLVsOnly</strong> wird in Windows 7 eingeführt.</p> | 



*Ptableid*

Der Ausgabepuffer, der den neuen Cursor empfängt, der für die neu erstellte temporäre Tabelle geöffnet wurde.

*prgcolumnid*

Der Ausgabepuffer, der das Array von Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden.

Die Spalten-IDs in diesem Array entsprechen genau dem Eingabearray von Spaltendefinitionen. Daher muss die Größe dieses Puffers der Größe des Eingabearrays entsprechen.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort</p> | <p><strong>Fehler bei JetOpenTempTable,</strong> JET_bitTTForwardOnly angegeben wurde und die temporäre Tabelle wie angegeben nicht mit der Vorwärtsoptimierung erstellt werden konnte. Dieser Fehler wird nur von Windows Server 2003 und höher zurückgegeben.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Der Index konnte nicht erstellt werden, da eine ungültige Indexdefinition angegeben wurde.</p><p><strong>JetOpenTempTable gibt</strong> diesen Fehler zurück, wenn:</p><ul><li><p>Das sprachneutrale -Locale wird angegeben.</p></li><li><p>Es wird ein ungültiger Satz von Normalisierungsflags angegeben.</p></li></ul><p>Dieser Fehler wird nur von Windows 2000 zurückgegeben.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Das Feld cp <a href="gg294130(v=exchg.10).md">des</a> JET_COLUMNDEF wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Das <em>Coltypfeld</em> des <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf einen gültigen Spaltentyp festgelegt.</p> | 
| <p>JET_errInvalidLanguageId</p> | <p>Der Index konnte nicht erstellt werden, da versucht wurde, eine ungültige Gebietsschema-ID zu verwenden. Die Gebietsschema-ID ist möglicherweise vollständig ungültig, oder das zugeordnete Sprachpaket ist möglicherweise nicht installiert.</p> | 
| <p>JET_errInvalidLCMapStringFlags</p> | <p>Der Index konnte nicht erstellt werden, da versucht wurde, einen ungültigen Satz von Normalisierungsflags zu verwenden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben. Bei Windows 2000 führen ungültige Normalisierungsflags stattdessen zu JET_errIndexInvalidDef.</p> | 
| <p>JET_errInvalidSesid</p> | <p>Das Sitzungshandle ist ungültig oder verweist auf eine geschlossene Sitzung.</p><p><strong>Hinweis</strong>  Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Der Vorgang ist fehlgeschlagen, weil die Engine nicht die Ressourcen zuordnen kann, die zum Öffnen eines neuen Cursors erforderlich sind. Cursorressourcen werden mit <a href="gg294044(v=exchg.10).md">jetSetSystemParameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>konfiguriert.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler beim Vorgang, weil nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</p><p><strong>JetOpenTempTable</strong> kann JET_errOutOfMemory zurückgeben, wenn der Adressraum des Hostprozesses zu fragmentiert wird. Der temporäre Tabellen-Manager ordnet für jede erstellte temporäre Tabelle unabhängig von der zu speichernden Datenmenge immer einen Adressraum von 1 MB zu.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p><p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle darf nicht mehr als JET_ccolFixedMost festen Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierten Spalten enthalten.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>Fehler beim Vorgang, weil die Engine die ressourcen, die zum Zwischenspeichern der Indizes der Tabelle erforderlich sind, nicht zuordnen kann. Die Anzahl der Indizes, deren Schema zwischengespeichert werden kann, wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>konfiguriert.</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>Der Vorgang ist fehlgeschlagen, weil die Engine nicht die Ressourcen zuordnen kann, die zum Zwischenspeichern des Schemas der Tabelle erforderlich sind. Die Anzahl der Tabellen, deren Schema zwischengespeichert werden kann, wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>konfiguriert.</p> | 
| <p>JET_errTooManySorts</p> | <p>Fehler beim Vorgang, weil die Engine die zum Erstellen einer temporären Tabelle erforderlichen Ressourcen nicht zuordnen kann. Temporäre Tabellenressourcen werden mit <a href="gg294044(v=exchg.10).md">jetSetSystemParameter</a> mit <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>konfiguriert.</p> | 



Bei Erfolg wird ein Cursor zurückgegeben, der für die neu erstellte temporäre Tabelle geöffnet wurde. Der Status der temporären Datenbank wird darauf vorbereitet, die neue temporäre Tabelle zu enthalten. Der Zustand aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

Bei einem Fehler wird die temporäre Tabelle nicht erstellt, und es wird kein Cursor zurückgegeben. Der Status der temporären Datenbank kann geändert werden. Der Zustand aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

#### <a name="remarks"></a>Hinweise

Temporäre Tabellen unterstützen nicht das vollständige Komplement der Spaltendefinitionsoptionen, die normalerweise von der Datenbank-Engine unterstützt werden. Tatsächlich werden nur JET_bitColumnFixed und JET_bitColumnTagged unterstützt. Dies bedeutet, dass es nicht möglich ist, eine automatische Inkrement-, Versions- oder mehrwertige Spalte in einer temporären Tabelle zu erstellen. Schließlich werden Spalten zur Zeilenüberlegung nicht unterstützt, da sie in einer temporären Tabelle nicht nützlich sind, da sie jeweils nur von einer Sitzung verwendet werden können. Wenn eine dieser Optionen angefordert wird, werden sie ignoriert.

Temporäre Tabellen unterstützen keine Standardwerte. Wenn eine Spaltendefinition bereitgestellt wird, die eine Standardwertspezifikation enthält, wird diese Spezifikation ignoriert.

Temporäre Tabellen werden aufgrund vieler verschiedener ESE-Funktionen an den Aufrufer zurückgegeben. Beispielsweise gibt [JetGetIndexInfo](./jetgetindexinfo-function.md) mit der option JET_IdxInfo, die im *InfoLevel-Parameter* festgelegt ist, eine temporäre Tabelle zurück, die eine Liste aller Schlüsselspalten in einem bestimmten Index enthält. Die temporären Tabellen folgen den gleichen Lebenszyklusregeln wie normale temporäre Tabellen, wie hier beschrieben.

Temporäre Tabellen werden auch intern von der Datenbank-Engine für viele Aufgaben verwendet. Die wichtigste dieser Aufgaben ist die Erstellung eines Indexes für eine vorhandene Tabelle. Eine temporäre Tabelle wird verwendet, um die Indexschlüssel zu sortieren, die zum Erstellen dieses Indexes verwendet werden.

Alle temporären Tabellen werden in der temporären Datenbank gespeichert. Die temporäre Datenbank ist eine spezielle Datenbankdatei, die während der Lebensdauer einer ESE-Instanz verwaltet wird und gelöscht wird, wenn diese Instanz heruntergefahren oder neu gestartet wird. Der Speicherort der temporären Datenbank kann mit [jetSetSystemParameter](./jetsetsystemparameter-function.md) mit [JET_paramTempPath](./temporary-database-parameters.md)konfiguriert werden. Die Platzierung der temporären Datenbank auf dem Datenträger relativ zu Ihren Transaktionsprotokolldateien und Datenbankdateien kann wichtig sein, wenn Ihre Anwendung temporäre Tabellen stark nutzt oder häufig Indizes erstellt.

Der Lebenszyklus einer temporären Tabelle ist an die Cursor gebunden, die darauf verweisen. Wenn alle Cursor, die auf eine temporäre Tabelle verweisen, entweder implizit oder explizit geschlossen sind, wird die temporäre Tabelle gelöscht. Wenn eine temporäre Tabelle innerhalb einer Transaktion erstellt wird und anschließend ein Rollback für diese Transaktion ausgeführt wird, wird die temporäre Tabelle gelöscht, da alle Cursor, auf die zu diesem Zeitpunkt verwiesen wird, implizit geschlossen werden. Neue Cursor können nur mithilfe von [JetDupCursor](./jetdupcursor-function.md)auf eine temporäre Tabelle verweisen. In diesem Fall werden die neuen Cursor auf dem ersten Indexeintrag der temporären Tabelle positioniert. [JetDupCursor](./jetdupcursor-function.md) funktioniert nur in bestimmten Verwendungsphasen für die temporäre Tabelle. Weitere Informationen finden Sie in den Hinweisen zu temporären Tabellencursorfunktionen. Es ist nicht möglich, von mehreren Sitzungen gleichzeitig auf eine temporäre Tabelle zu verweisen.

Es gibt ein wichtiges Problem in [JetDupCursor,](./jetdupcursor-function.md) das sich auf temporäre Tabellen auswirkt. Wenn versucht wird, eine temporäre Tabelle zu duplizieren, die sich im Vorwärtsmodus befindet, wird der resultierende Cursor nicht ordnungsgemäß erstellt und funktioniert nicht. Es ist immer noch sicher, einen Cursor über einer materialisierten temporären Tabelle zu duplizieren.

Der temporäre Tabellen-Manager kann eine temporäre Tabelle auf drei Arten implementieren. Die erste Methode besteht darin, eine In-Memory-Tabelle zu verwalten. Diese Strategie ist die schnellste, kann aber nur für kleine, einfache temporäre Tabellen verwendet werden. Die zweite Methode besteht darin, eine datenträgerbasierte Sortierung zu erstellen, die mit einem vorwärts gerichteten Iterator gesteuert werden kann. Diese Strategie kann nur unter bestimmten Umständen verwendet werden und ist die schnellste Möglichkeit zum Sortieren und Entfernen von Duplikaten aus einem sehr großen Datensatz. Die dritte Methode besteht darin, eine B+-Struktur in der temporären Datenbank zu erstellen, die die temporäre Tabelle enthält. Diese Strategie ist die langsamste, aber vielseitigste Strategie und wird als materialisierte temporäre Tabelle bezeichnet. Diese Strategien können in Kombination verwendet werden, um letztendlich die Funktionalität zu erreichen, die von der temporären Tabelle angefordert wird.

Wenn die temporäre Tabelle nicht materialisiert wird, wird sie in erster Linie in zwei Hauptphasen verwendet. Die erste Phase ist die Einfügephase, in der die Tabelle mit ihrem anfänglichen Datensatz aufgefüllt wird. Während dieser Phase ist nur das Einfügen von Daten zulässig. Diese Phase endet, wenn versucht wird, den Cursor mit [JetMove](./jetmove-function.md) oder [JetSeek](./jetseek-function.md)zu bewegen. Die zweite Phase ist die Datenextraktionsphase. Während dieser Phase können die in der temporären Tabelle gespeicherten Daten gemäß den Funktionen extrahiert werden, die beim Erstellen der temporären Tabelle angefordert wurden.

**Funktionen des temporären Tabellencursors**

Wenn die temporäre Tabelle materialisiert wird, verfügt der Cursor über die folgenden Funktionen, kann aber durch die angeforderten Optionen weiter eingeschränkt werden:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDelete](./jetdelete-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetCursorInfo](./jetgetcursorinfo-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordSize](./jetgetrecordsize-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetGotoBookmark](./jetgotobookmark-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrikey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetSetIndexRange](./jetsetindexrange-function.md)

  - [JetSetLS](./jetsetls-function.md)

  - [JetUpdate](./jetupdate-function.md)

Wenn die temporäre Tabelle nicht materialisiert wird und sich in der Einfügephase befindet, verfügt der Cursor über die folgenden Funktionen, kann aber durch die angeforderten Optionen weiter eingeschränkt werden:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)
    
    **Hinweis:**  Bewirkt den Übergang in die Extraktionsphase.

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrikey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)
    
    **Hinweis:**  Bewirkt den Übergang in die Extraktionsphase.

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetUpdate](./jetupdate-function.md)

Wenn die temporäre Tabelle nicht materialisiert ist und sich in der Extraktionsphase befindet, verfügt der Cursor über die folgenden Funktionen, kann aber durch die angeforderten Optionen weiter eingeschränkt werden:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)
    
    **Hinweis:**  Wenn versucht wird, eine temporäre Tabelle zu duplizieren, die sich im Vorwärtsmodus befindet, wird der resultierende Cursor nicht ordnungsgemäß erstellt und funktioniert nicht. Es ist immer noch sicher, einen Cursor über eine materialisierte temporäre Tabelle zu duplizieren.

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordSize](./jetgetrecordsize-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetGotoBookmark](./jetgotobookmark-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrikey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [JetSetIndexRange](./jetsetindexrange-function.md)

  - [JetSetLS](./jetsetls-function.md)

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

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
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Temporäre Datenbankparameter](./temporary-database-parameters.md)
