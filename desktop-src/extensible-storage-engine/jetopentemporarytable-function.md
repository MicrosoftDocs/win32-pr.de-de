---
description: Weitere Informationen finden Sie unter JetOpenTemporaryTable-Funktion.
title: JetOpenTemporaryTable-Funktion
TOCTitle: JetOpenTemporaryTable Function
ms:assetid: feacd0b8-2298-4ec6-aa59-0fede08474bc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294144(v=EXCHG.10)
ms:contentKeyID: 32765758
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTemporaryTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e0b0b0ee437e24bd66c8d2f4a8afd178bc4a3ef4b6199434f8da79f50128bf8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944620"
---
# <a name="jetopentemporarytable-function"></a>JetOpenTemporaryTable-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopentemporarytable-function"></a>JetOpenTemporaryTable-Funktion

Die **JetOpenTemporaryTable-Funktion** erstellt eine flüchtige Tabelle mit einem einzelnen Index, der zum Speichern und Abrufen von Datensätzen verwendet werden kann, genau wie eine normale Tabelle, die über [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)erstellt wird.

**Windows Vista:****JetOpenTemporaryTable** wird in Windows Vista eingeführt.  

Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur schneller als normale Tabellen. Sie können Datensätze schnell sortieren und duplizieren, wenn auf sie rein sequenziell zugegriffen wird.

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet wird.

*popentemporarytable*

Ein Zeiger auf [](./jet-opentemporarytable-structure.md) eine JET_OPENTEMPORARYTABLE-Struktur, die die Beschreibung der temporären Tabelle enthält, die bei der Eingabe erstellt werden soll. Nach einem erfolgreichen Aufruf enthält die -Struktur das Handle für die temporäre Tabelle und die Spaltenidentifikationen.

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>Fehler beim Vorgang, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um ihn abschließen zu können.</p>
<p><strong>JetOpenTemporaryTable</strong> kann JET_errOutOfMemory zurückgeben, wenn der Adressraum des Hostprozesses zu fragmentiert wird. Der Temporäre Tabellen-Manager ordnet für jede temporäre Tabelle, die erstellt wird, unabhängig von der gespeicherten Datenmenge einen Adressraum von 1 MB zu.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte führte zu einem unerwarteten Ergebnis.</p>
<p>Dieser Fehler wird von <strong>JetOpenTemporaryTable unter</strong> den folgenden Bedingungen zurückgegeben:</p>
<ul>
<li><p>Der <strong>cbStruct-Member</strong> <a href="gg269206(v=exchg.10).md">der</a> JET_OPENTEMPORARYTABLE-Struktur entspricht nicht einer Version dieser Struktur, die von dieser Version der Datenbank-Engine unterstützt wird.</p></li>
<li><p>Der <strong>cbKeyMost-Member</strong> der <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE-Struktur</a> ist kleiner als JET_cbKeyMostMin.</p></li>
<li><p>Das <strong>cbKeyMost-Member</strong> der <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE-Struktur</a> ist größer als der größte unterstützte Wert für die Datenbankseitengröße für die Instanz (JET_paramDatabasePageSize). Weitere Informationen finden JET_paramKeyMost Parameter in der Liste <a href="gg269241(v=exchg.10).md">der Informationsparameter.</a></p></li>
<li><p>Das cbVarSegMac-Member <a href="gg269206(v=exchg.10).md"></a> der JET_OPENTEMPORARYTABLE-Struktur ist größer als das <strong>cbKeyMost-Member.</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet war, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die -Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p>
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
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
<td><p>JET_errInvalidSesid</p></td>
<td><p>Das Sitzungshandy ist ungültig oder verweist auf eine geschlossene Sitzung.</p>
<p><strong>Hinweis:</strong>  Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Öffnen eines neuen Cursors erforderlich sind. Cursorressourcen werden mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mit JET_paramMaxCursors.</a> <a href="gg269201(v=exchg.10).md"></a></p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Erstellen einer temporären Tabelle erforderlich sind. Temporäre Tabellenressourcen werden mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter und</a> <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p><strong>Fehler bei JetOpenTemporaryTable,</strong> JET_bitTTForwardOnly angegeben wurde und die angegebene temporäre Tabelle nicht mit der Vorwärtsoptimierung erstellt werden konnte.</p>
<p><strong>Windows Server 2003:</strong>  Dieser Fehler wird nur von Windows Server 2003 und höher zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle kann nicht mehr als JET_ccolFixedMost spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost Spalten enthalten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Zwischenspeichern des Schemas der Tabelle erforderlich sind. Um die Anzahl der Tabellen zu konfigurieren, die Schemas enthalten, die zwischengespeichert werden können, verwenden Sie <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">mit JET_paramMaxOpenTables.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Der <strong>cp-Member</strong> der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Das <strong>Coltyp-Member</strong> der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf einen gültigen Spaltentyp festgelegt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Der Index konnte nicht erstellt werden, da versucht wurde, eine ungültige Locale ID zu verwenden. Die Locale ID ist möglicherweise entweder vollständig ungültig, oder das zugeordnete Sprachpaket ist möglicherweise nicht installiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>Der Index konnte nicht erstellt werden, weil versucht wurde, einen ungültigen Satz von Normalisierungsflags zu verwenden.</p>
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p>
<p><strong>Windows 2000:</strong>  In Windows 2000 führen ungültige Normalisierungsflags zu JET_errIndexInvalidDef.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Der Index konnte nicht erstellt werden, da eine ungültige Indexdefinition angegeben wurde. <strong>JetOpenTemporaryTable</strong> gibt diesen Fehler unter den folgenden Bedingungen zurück:</p>
<ul>
<li><p>Das sprachneutrale -Locale wird angegeben.</p></li>
<li><p>Es wird ein ungültiger Satz von Normalisierungsflags angegeben.</p></li>
</ul>
<p><strong>Windows 2000:</strong>  Dieser Fehler wird nur von Windows 2000 zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen kann, die zum Zwischenspeichern der Indizes der Tabelle erforderlich sind. Um die Anzahl der Indizes zu konfigurieren, die Schemas haben, die zwischengespeichert werden können, verwenden Sie <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">mit JET_paramMaxOpenTables.</a></p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird ein Cursor zurückgegeben, der in der neu erstellten temporären Tabelle geöffnet wird. Der Status der temporären Datenbank wird so vorbereitet, dass er die neue temporäre Tabelle enthält. Der Status normaler Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

Bei einem Fehler wird die temporäre Tabelle nicht erstellt, und es wird kein Cursor zurückgegeben. Der Status der temporären Datenbank kann geändert werden. Der Status normaler Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

#### <a name="remarks"></a>Hinweise

Temporäre Tabellen unterstützen nicht das vollständige Komplement der Spaltendefinitionsoptionen, die normalerweise von der Datenbank-Engine unterstützt werden. Tatsächlich werden nur JET_bitColumnFixed und JET_bitColumnTagged unterstützt. Dies bedeutet, dass es nicht möglich ist, eine automatische Inkrement-, Versions- oder mehrwertige Spalte in einer temporären Tabelle zu erstellen. Schließlich werden Spalten mit Zeilenumknurung nicht unterstützt, da sie nur von einer Sitzung gleichzeitig verwendet werden können. Wenn eine dieser Optionen angefordert wird, werden sie ignoriert.

Temporäre Tabellen unterstützen keine Standardwerte. Wenn eine Spaltendefinition bereitgestellt wird, die eine Standardwertspezifikation enthält, wird diese Spezifikation ignoriert.

Temporäre Tabellen werden als Ergebnis vieler verschiedener ESE-Funktionen an den Aufrufer zurückgegeben. Beispielsweise gibt [JetGetIndexInfo](./jetgetindexinfo-function.md) mit dem optionsset JET_IdxInfo eine temporäre Tabelle zurück, die eine Liste aller Schlüsselspalten in einem bestimmten Index enthält. Die temporären Tabellen folgen denselben Lebenszyklusregeln wie normale temporäre Tabellen, wie hier beschrieben.

Temporäre Tabellen werden auch intern von der Datenbank-Engine für viele Aufgaben verwendet. Die wichtigste dieser Aufgaben ist die Erstellung eines Indexes für eine vorhandene Tabelle. Eine temporäre Tabelle wird verwendet, um die Indexschlüssel zu sortieren, die zum Erstellen dieses Indexes verwendet werden.

Alle temporären Tabellen werden in der temporären Datenbank gespeichert. Die temporäre Datenbank ist eine spezielle Datenbankdatei, die während der Lebensdauer einer ESE-Instanz verwaltet wird und gelöscht wird, wenn diese Instanz heruntergefahren oder neu gestartet wird. Der Speicherort der temporären Datenbank kann mit [JetSetSystemParameter mit](./jetsetsystemparameter-function.md) [JET_paramTempPath.](./temporary-database-parameters.md) Die Platzierung der temporären Datenbank auf dem Datenträger relativ zu Ihren Transaktionsprotokolldateien und Datenbankdateien kann wichtig sein, wenn Ihre Anwendung häufig temporäre Tabellen verwendet oder Indizes erstellt.

Der Lebenszyklus einer temporären Tabelle ist an die Cursor gebunden, die darauf verweisen. Wenn alle Cursor, die auf eine temporäre Tabelle verweisen, entweder implizit oder explizit geschlossen werden, wird die temporäre Tabelle gelöscht. Wenn eine temporäre Tabelle innerhalb einer Transaktion erstellt wird und anschließend ein Rollback für diese Transaktion ausgeführt wird, wird die temporäre Tabelle gelöscht, da alle Cursor, die zu diesem Zeitpunkt darauf verwiesen haben, implizit geschlossen werden. Neue Cursor können nur mit [JetDupCursor](./jetdupcursor-function.md)auf eine temporäre Tabelle verweisen. In diesem Fall werden die neuen Cursor am ersten Indexeintrag der temporären Tabelle positioniert. [JetDupCursor funktioniert](./jetdupcursor-function.md) nur in bestimmten Verwendungsphasen für die temporäre Tabelle. Weitere Informationen finden Sie in den Anmerkungen zu temporären Tabellencursorfunktionen. Es ist nicht möglich, von mehr als einer Sitzung gleichzeitig auf eine temporäre Tabelle zu verweisen.

**Vorsicht**  Es gibt ein wichtiges Problem in [JetDupCursor,](./jetdupcursor-function.md) das temporäre Tabellen betrifft. Wenn versucht wird, eine temporäre Tabelle zu duplizieren, die sich im Vorwärtsmodus befindet, wird der resultierende Cursor nicht ordnungsgemäß erstellt und funktioniert nicht. Es ist immer noch sicher, einen Cursor über eine materialisierte temporäre Tabelle zu duplizieren.

Der Manager für temporäre Tabellen kann eine temporäre Tabelle auf drei Arten implementieren. Die erste Methode besteht im Verwalten einer In-Memory-Tabelle. Diese Strategie ist die schnellste, kann aber nur für kleine, einfache temporäre Tabellen verwendet werden. Die zweite Methode besteht in der Erstellung einer datenträgerbasierten Sortierung, die mit einem Vorwärts-Iterator gesteuert werden kann. Diese Strategie kann nur unter bestimmten Umständen verwendet werden und ist die schnellste Möglichkeit, Duplikate aus einem sehr großen DataSet zu sortieren und zu entfernen. Die dritte Methode besteht im Erstellen einer B+-Struktur in der temporären Datenbank zum Speichern der temporären Tabelle. Diese Strategie ist die langsamste, aber vielseitigste strategie und wird als materialisierte temporäre Tabelle bezeichnet. Diese Strategien können in Kombination verwendet werden, um letztendlich die Funktionalität zu erreichen, die von der temporären Tabelle angefordert wird.

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Deklariert in Esent.h.</p></td>
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

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetMove](./jetmove-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Informationsparameter](./informational-parameters.md)  
[Temporäre Datenbankparameter](./temporary-database-parameters.md)
