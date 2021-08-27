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
ms.openlocfilehash: a94af3f142fb7449a95ddf67ad9a0d16f2e37c43
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982403"
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
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Jeder Versuch, einen Datensatz mit demselben Indexschlüssel wie ein zuvor eingefügter Datensatz einfügungen, ist sofort JET_errKeyDuplicate. Wenn diese Option nicht angefordert wird, wird sofort ein Duplikat erkannt und schlägt fehl oder wird später automatisch entfernt. Dies hängt von der Strategie ab, die die Datenbank-Engine für die Implementierung der temporären Tabelle basierend auf der angeforderten Funktionalität gewählt hat.</p><p>Wenn diese Funktionalität nicht erforderlich ist, sollten Sie sie nicht anfordern. Wenn diese Funktionalität nicht angefordert wird, kann der Manager für temporäre Tabellen möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Zwingt den temporären Tabellen-Manager, die Suche nach der besten Strategie aufzugeben, um die Verwaltung der temporären Tabelle zu verwenden, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>Die temporäre Tabelle wird nur erstellt, wenn der Temporäre Tabellen-Manager die Implementierung verwenden kann, die für Zwischenabfrageergebnisse optimiert ist. Wenn ein Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, wird der Vorgang mit einem Fehler JET_errCannotMaterializeForwardOnlySort.</p><p>Ein Nebeneffekt dieser Option besteht im Zulassen, dass die temporäre Tabelle Datensätze mit doppelten Indexschlüsseln enthält. Weitere JET_bitTTUnique finden Sie unter .</p><p>Diese Option ist nur auf Windows Server 2003 und höher verfügbar.</p> | 
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
| <p>JET_errInvalidColumnType</p> | <p>Das <em>Coltyp-Feld</em> des <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf einen gültigen Spaltentyp festgelegt.</p> | 
| <p>JET_errInvalidLanguageId</p> | <p>Der Index konnte nicht erstellt werden, da versucht wurde, eine ungültige Locale ID zu verwenden. Die Locale-ID ist möglicherweise vollständig ungültig, oder das zugeordnete Sprachpaket ist möglicherweise nicht installiert.</p> | 
| <p>JET_errInvalidLCMapStringFlags</p> | <p>Der Index konnte nicht erstellt werden, weil versucht wurde, einen ungültigen Satz von Normalisierungsflags zu verwenden. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben. In Windows 2000 führen ungültige Normalisierungsflags stattdessen zu JET_errIndexInvalidDef.</p> | 
| <p>JET_errInvalidSesid</p> | <p>Das Sitzungshandy ist ungültig oder verweist auf eine geschlossene Sitzung.</p><p><strong>Hinweis:</strong>  Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Öffnen eines neuen Cursors erforderlich sind. Cursorressourcen werden mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter und</a> <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors.</a></p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler beim Vorgang, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um ihn abschließen zu können.</p><p><strong>JetOpenTempTable</strong> kann JET_errOutOfMemory zurückgeben, wenn der Adressraum des Hostprozesses zu fragmentiert wird. Der temporäre Tabellen-Manager ordnet für jede temporäre Tabelle, die erstellt wird, immer einen Adressraum von 1 MB zu, unabhängig von der zu speichernden Datenmenge.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle darf nicht mehr als JET_ccolFixedMost Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost spalten enthalten.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Zwischenspeichern der Indizes der Tabelle erforderlich sind. Die Anzahl der Indizes, deren Schema zwischengespeichert werden kann, wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mit</a> <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables.</a></p> | 
| <p>JET_errTooManyOpenTables</p> | <p>Fehler beim Vorgang, da die Engine nicht die Ressourcen zuordnen kann, die zum Zwischenspeichern des Schemas der Tabelle erforderlich sind. Die Anzahl der Tabellen, deren Schema zwischengespeichert werden kann, wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mit</a> <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables.</a></p> | 
| <p>JET_errTooManySorts</p> | <p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Erstellen einer temporären Tabelle erforderlich sind. Temporäre Tabellenressourcen werden mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mit JET_paramMaxTemporaryTables.</a> <a href="gg294140(v=exchg.10).md"></a></p> | 



Bei Erfolg wird ein Cursor zurückgegeben, der in der neu erstellten temporären Tabelle geöffnet wird. Der Status der temporären Datenbank wird so vorbereitet, dass er die neue temporäre Tabelle enthält. Der Status normaler Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

Bei einem Fehler wird die temporäre Tabelle nicht erstellt, und es wird kein Cursor zurückgegeben. Der Status der temporären Datenbank kann geändert werden. Der Status normaler Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

#### <a name="remarks"></a>Bemerkungen

Temporäre Tabellen unterstützen nicht das vollständige Komplement der Spaltendefinitionsoptionen, die normalerweise von der Datenbank-Engine unterstützt werden. Tatsächlich werden nur JET_bitColumnFixed und JET_bitColumnTagged unterstützt. Dies bedeutet, dass es nicht möglich ist, eine automatische Inkrement-, Versions- oder mehrwertige Spalte in einer temporären Tabelle zu erstellen. Schließlich werden Zeilenumklassungsspalten nicht unterstützt, da sie in einer temporären Tabelle nicht nützlich sind, da sie nur von einer Sitzung gleichzeitig verwendet werden können. Wenn eine dieser Optionen angefordert wird, werden sie ignoriert.

Temporäre Tabellen unterstützen keine Standardwerte. Wenn eine Spaltendefinition bereitgestellt wird, die eine Standardwertspezifikation enthält, wird diese Spezifikation ignoriert.

Temporäre Tabellen werden als Ergebnis vieler verschiedener ESE-Funktionen an den Aufrufer zurückgegeben. Beispielsweise gibt [JetGetIndexInfo](./jetgetindexinfo-function.md) mit der option JET_IdxInfo, die im *InfoLevel-Parameter* festgelegt ist, eine temporäre Tabelle zurück, die eine Liste aller Schlüsselspalten in einem bestimmten Index enthält. Die temporären Tabellen folgen denselben Lebenszyklusregeln wie normale temporäre Tabellen, wie hier beschrieben.

Temporäre Tabellen werden auch intern von der Datenbank-Engine für viele Aufgaben verwendet. Die wichtigste dieser Aufgaben ist die Erstellung eines Indexes für eine vorhandene Tabelle. Eine temporäre Tabelle wird verwendet, um die Indexschlüssel zu sortieren, die zum Erstellen dieses Indexes verwendet werden.

Alle temporären Tabellen werden in der temporären Datenbank gespeichert. Die temporäre Datenbank ist eine spezielle Datenbankdatei, die während der Lebensdauer einer ESE-Instanz verwaltet wird und gelöscht wird, wenn diese Instanz heruntergefahren oder neu gestartet wird. Der Speicherort der temporären Datenbank kann mit [JetSetSystemParameter und](./jetsetsystemparameter-function.md) [JET_paramTempPath.](./temporary-database-parameters.md) Die Platzierung der temporären Datenbank auf dem Datenträger relativ zu Ihren Transaktionsprotokolldateien und Datenbankdateien kann wichtig sein, wenn Ihre Anwendung häufig temporäre Tabellen verwendet oder Indizes erstellt.

Der Lebenszyklus einer temporären Tabelle ist an die Cursor gebunden, die darauf verweisen. Wenn alle Cursor, die auf eine temporäre Tabelle verweisen, entweder implizit oder explizit geschlossen werden, wird die temporäre Tabelle gelöscht. Wenn eine temporäre Tabelle innerhalb einer Transaktion erstellt wird und anschließend ein Rollback für diese Transaktion ausgeführt wird, wird die temporäre Tabelle gelöscht, da alle Cursor, die zu diesem Zeitpunkt darauf verwiesen haben, implizit geschlossen werden. Neue Cursor verweisen möglicherweise nur mit [JetDupCursor](./jetdupcursor-function.md)auf eine temporäre Tabelle. In diesem Fall werden die neuen Cursor am ersten Indexeintrag der temporären Tabelle positioniert. [JetDupCursor funktioniert](./jetdupcursor-function.md) nur in bestimmten Verwendungsphasen für die temporäre Tabelle. Weitere Informationen finden Sie in den Anmerkungen zu temporären Tabellencursorfunktionen. Es ist nicht möglich, von mehr als einer Sitzung gleichzeitig auf eine temporäre Tabelle zu verweisen.

Es gibt ein wichtiges Problem in [JetDupCursor,](./jetdupcursor-function.md) das temporäre Tabellen betrifft. Wenn versucht wird, eine temporäre Tabelle zu duplizieren, die sich im Vorwärtsmodus befindet, wird der resultierende Cursor nicht ordnungsgemäß erstellt und funktioniert nicht. Es ist immer noch sicher, einen Cursor über eine materialisierte temporäre Tabelle zu duplizieren.

Der Manager für temporäre Tabellen kann eine temporäre Tabelle auf drei Arten implementieren. Die erste Methode besteht im Verwalten einer In-Memory-Tabelle. Diese Strategie ist die schnellste, kann aber nur für kleine, einfache temporäre Tabellen verwendet werden. Die zweite Methode besteht in der Erstellung einer datenträgerbasierten Sortierung, die mit einem Vorwärts-Iterator gesteuert werden kann. Diese Strategie kann nur unter bestimmten Umständen verwendet werden und ist die schnellste Möglichkeit, Duplikate aus einem sehr großen DataSet zu sortieren und zu entfernen. Die dritte Methode besteht im Erstellen einer B+-Struktur in der temporären Datenbank zum Speichern der temporären Tabelle. Diese Strategie ist die langsamste, aber vielseitigste strategie und wird als materialisierte temporäre Tabelle bezeichnet. Diese Strategien können in Kombination verwendet werden, um letztendlich die funktionalität zu erreichen, die von der temporären Tabelle angefordert wird.

Wenn die temporäre Tabelle nicht materialisiert wird, wird sie hauptsächlich in zwei Hauptphasen verwendet. Die erste Phase ist die Einfügephase, in der die Tabelle mit dem ursprünglichen DataSet aufgefüllt wird. In dieser Phase ist nur das Einfügen von Daten zulässig. Diese Phase endet, wenn versucht wird, den Cursor mit [JetMove](./jetmove-function.md) oder [JetSeek zu verschieben.](./jetseek-function.md) Die zweite Phase ist die Datenextraktionsphase. Während dieser Phase können die in der temporären Tabelle gespeicherten Daten entsprechend den Funktionen extrahiert werden, die beim Erstellen der temporären Tabelle angefordert wurden.

**Temporäre Tabellencursorfunktionen**

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


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



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
