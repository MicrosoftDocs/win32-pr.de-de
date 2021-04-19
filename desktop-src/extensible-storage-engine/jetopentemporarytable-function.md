---
description: 'Weitere Informationen zu: jetopentemporarytable-Funktion'
title: Jetopentemporarytable-Funktion
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
ms.openlocfilehash: 2335f6d6426b321d5db55b4ed005c6220484d509
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353837"
---
# <a name="jetopentemporarytable-function"></a>Jetopentemporarytable-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopentemporarytable-function"></a>Jetopentemporarytable-Funktion

Die **jetopentemporarytable** -Funktion erstellt eine flüchtige Tabelle mit einem einzelnen Index, der zum Speichern und Abrufen von Datensätzen verwendet werden kann, genau wie eine gewöhnliche Tabelle, die über [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)erstellt wird.

**Windows Vista:**  **jetopertemporarytable** wird in Windows Vista eingeführt.

Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur schneller als normale Tabellen. Sie können eine doppelte Entfernung von Daten Satz Gruppen schnell Sortieren und durchführen, wenn auf Sie in einer rein sequenziellen Weise darauf zugegriffen wird.

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet wird.

*popendtemporarytable*

Ein Zeiger auf eine [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) -Struktur, die die Beschreibung der in der Eingabe zu erstellenden temporären Tabelle enthält. Nach einem erfolgreichen-Vorgang enthält die-Struktur das Handle für die temporären Tabellen-und Spalten Identifizierungen.

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</p>
<p><strong>Jetopumtemporarytable</strong> kann JET_errOutOfMemory zurückgeben, wenn der Adressraum des Host Prozesses zu fragmentiert wird. Der temporäre Tabellen-Manager weist für jede temporäre Tabelle, die unabhängig von der gespeicherten Datenmenge erstellt wird, 1 MB Adressraum zu.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte führte zu einem unerwarteten Ergebnis.</p>
<p>Dieser Fehler wird von <strong>jetopertemporarytable</strong> unter den folgenden Bedingungen zurückgegeben:</p>
<ul>
<li><p>Der <strong>cbStruct</strong> -Member der <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> Struktur entspricht keiner Version dieser Struktur, die von dieser Version der Datenbank-Engine unterstützt wird.</p></li>
<li><p>Der <strong>cbkeymost</strong> -Member der <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> -Struktur ist kleiner als JET_cbKeyMostMin.</p></li>
<li><p>Der <strong>cbkeymost</strong> -Member der <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> -Struktur ist größer als der größte unterstützte Wert für die Datenbankseiten Größe für die-Instanz (JET_paramDatabasePageSize). Weitere Informationen finden Sie unter dem JET_paramKeyMost-Parameter in der Liste mit <a href="gg269241(v=exchg.10).md">Informations Parametern</a> .</p></li>
<li><p>Der cbvarsegmac-Member der <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> Struktur ist größer als der <strong>cbkeymost</strong> -Member.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet war, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da der-Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität der Daten zu schützen.</p>
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
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
<td><p>JET_errInvalidSesid</p></td>
<td><p>Das Sitzungs Handle ist ungültig oder verweist auf eine geschlossene Sitzung.</p>
<p><strong>Hinweis</strong>  Dieser Fehler wird unter allen Umständen nicht zurückgegeben. Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine die zum Öffnen eines neuen Cursors erforderlichen Ressourcen nicht zuordnen kann. Cursor Ressourcen werden mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>konfiguriert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine die zum Erstellen einer temporären Tabelle erforderlichen Ressourcen nicht zuordnen kann. Temporäre Tabellen Ressourcen werden mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>konfiguriert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p>Fehler bei <strong>jetopentemporarytable</strong> , weil JET_bitTTForwardOnly angegeben wurde und die angegebene temporäre Tabelle nicht mithilfe der vorwärts Optimierung erstellt werden konnte.</p>
<p><strong>Windows Server 2003:</strong>  Dieser Fehler wird nur von Windows Server 2003 und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle kann nicht mehr als JET_ccolFixedMost fester Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierte Spalten aufweisen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern des Schemas der Tabelle erforderlichen Ressourcen nicht zuordnen kann. Um die Anzahl der Tabellen zu konfigurieren, die Schemas aufweisen, die zwischengespeichert werden können, verwenden Sie <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Der <strong>CP</strong> -Member der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> Struktur wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Der <strong>colttmember</strong> des <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf einen gültigen Spaltentyp festgelegt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Der Index konnte nicht erstellt werden, da versucht wurde, eine ungültige Gebiets Schema-ID zu verwenden. Die Gebiets Schema-ID ist möglicherweise vollständig ungültig, oder das zugehörige Sprachpaket ist möglicherweise nicht installiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>Der Index konnte nicht erstellt werden, da versucht wurde, einen ungültigen Satz von normalisierungs Flags zu verwenden.</p>
<p><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p>
<p><strong>Windows 2000:</strong>  Unter Windows 2000 führen ungültige normalisierungs Flags zu JET_errIndexInvalidDef.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Der Index konnte nicht erstellt werden, da eine ungültige Index Definition angegeben wurde. <strong>Jetopumtemporarytable</strong> gibt diesen Fehler unter den folgenden Bedingungen zurück:</p>
<ul>
<li><p>Das sprachneutrale Gebiets Schema ist angegeben.</p></li>
<li><p>Es wurde ein ungültiger Satz von normalisierungs Flags angegeben.</p></li>
</ul>
<p><strong>Windows 2000:</strong>  Dieser Fehler wird nur von Windows 2000 zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern der Indizes der Tabelle erforderlichen Ressourcen nicht zuordnen kann. Um die Anzahl der Indizes zu konfigurieren, die Schemas aufweisen, die zwischengespeichert werden können, verwenden Sie <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird ein Cursor zurückgegeben, der für die neu erstellte temporäre Tabelle geöffnet wurde. Der Status der temporären Datenbank wird darauf vorbereitet, die neue temporäre Tabelle zu enthalten. Der Status aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

Bei einem Fehler wird die temporäre Tabelle nicht erstellt, und ein Cursor wird nicht zurückgegeben. Der Status der temporären Datenbank kann geändert werden. Der Status aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.

#### <a name="remarks"></a>Bemerkungen

Temporäre Tabellen unterstützen nicht die vollständige Ergänzung der Spalten Definitions Optionen, die normalerweise von der Datenbank-Engine unterstützt werden. Tatsächlich werden nur JET_bitColumnFixed und JET_bitColumnTagged unterstützt. Dies bedeutet, dass es nicht möglich ist, eine automatische Inkrement-, Versions-oder mehrwertige Spalte in einer temporären Tabelle zu erstellen. Zum Schluss werden die Spalten zum Aktualisieren von Spalten nicht unterstützt, da Sie nur von einer Sitzung gleichzeitig verwendet werden können. Wenn eine dieser Optionen angefordert wird, werden Sie ignoriert.

Temporäre Tabellen unterstützen keine Standardwerte. Wenn eine Spaltendefinition bereitgestellt wird, die eine Standardwert Spezifikation enthält, wird diese Angabe ignoriert.

Temporäre Tabellen werden als Ergebnis vieler unterschiedlicher ESE-Funktionen an den Aufrufer zurückgegeben. Beispielsweise gibt [jetgetindexinfo](./jetgetindexinfo-function.md) mit dem JET_IdxInfo Options Satz eine temporäre Tabelle zurück, die eine Liste aller Schlüssel Spalten in einem bestimmten Index enthält. Die temporären Tabellen folgen den gleichen Lebenszyklus Regeln wie gewöhnliche temporäre Tabellen, wie hier beschrieben.

Temporäre Tabellen werden auch intern von der Datenbank-Engine für viele Tasks verwendet. Die wichtigsten dieser Aufgaben sind die Erstellung eines Indexes für eine vorhandene Tabelle. Eine temporäre Tabelle wird zum Sortieren der Index Schlüssel verwendet, die zum Erstellen dieses Indexes verwendet werden.

Alle temporären Tabellen werden in der temporären Datenbank gespeichert. Die temporäre Datenbank ist eine spezielle Datenbankdatei, die während der Lebensdauer einer ESE-Instanz verwaltet wird und gelöscht wird, wenn diese Instanz heruntergefahren oder neu gestartet wird. Der Speicherort der temporären Datenbank kann mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit [JET_paramTempPath](./temporary-database-parameters.md)konfiguriert werden. Die Platzierung der temporären Datenbank auf dem Datenträger in Relation zu den Transaktionsprotokoll Dateien und Datenbankdateien ist möglicherweise wichtig, wenn die Anwendung temporäre Tabellen stark nutzt oder häufig Indizes erstellt.

Der Lebenszyklus einer temporären Tabelle ist an die Cursor gebunden, die auf diese Tabelle verweisen. Wenn alle Cursor, die auf eine temporäre Tabelle verweisen, entweder implizit oder explizit geschlossen werden, wird die temporäre Tabelle gelöscht. Wenn eine temporäre Tabelle innerhalb einer Transaktion erstellt wird und anschließend ein Rollback für diese Transaktion ausgeführt wird, wird die temporäre Tabelle gelöscht, da alle Cursor, auf die Sie zu diesem Zeitpunkt verwiesen hat, implizit geschlossen werden. Neue Cursor können nur durch die Verwendung von [jetdupcursor](./jetdupcursor-function.md)auf eine temporäre Tabelle verweisen. In diesem Fall werden die neuen Cursor auf dem ersten Index Eintrag der temporären Tabelle positioniert. [Jetdupcursor](./jetdupcursor-function.md) funktioniert nur in bestimmten Phasen der Verwendung für die temporäre Tabelle. Weitere Informationen finden Sie in den Hinweisen zu den Cursor Funktionen für temporäre Tabellen. Es ist nicht möglich, auf eine temporäre Tabelle von mehreren Sitzungen gleichzeitig zu verweisen.

**Vorsicht**  In [jetdupcursor](./jetdupcursor-function.md) liegt ein wichtiges Problem vor, das sich auf temporäre Tabellen auswirkt. Wenn versucht wird, eine temporäre Tabelle zu duplizieren, die sich im vorwärts Modus befindet, wird der resultierende Cursor nicht ordnungsgemäß erstellt und funktioniert nicht. Es ist immer noch sicher, einen Cursor über eine materialisierte temporäre Tabelle zu duplizieren.

Der temporäre Tabellen-Manager kann auf drei Arten eine temporäre Tabelle implementieren. Die erste Methode besteht darin, eine in-Memory-Tabelle beizubehalten. Diese Strategie ist der schnellste, kann aber nur für kleine, einfache, temporäre Tabellen verwendet werden. Die zweite Methode besteht darin, eine Datenträger basierte Sortierung zu erstellen, die mit einem vorwärts-Iterator gesteuert werden kann. Diese Strategie kann nur unter bestimmten Umständen verwendet werden und ist die schnellste Möglichkeit, Duplikate aus einem sehr großen Dataset zu sortieren und zu entfernen. Die dritte Methode ist das Erstellen einer B +-Struktur in der temporären Datenbank, um die temporäre Tabelle zu speichern. Diese Strategie ist die langsamste, aber die vielseitigste und wird als materialisierte temporäre Tabelle bezeichnet. Diese Strategien können in Kombination verwendet werden, um letztendlich die Funktionalität zu erreichen, die für die temporäre Tabelle angefordert wird.

Wenn die temporäre Tabelle nicht materialisiert ist, wird Sie in erster Linie in zwei Hauptphasen verwendet. Die erste Phase ist die Einfügungs Phase, in der die Tabelle mit dem ersten DataSet aufgefüllt wird. In dieser Phase ist nur die Daten Einfügung zulässig. Diese Phase endet, wenn versucht wird, den Cursor mithilfe von [jetmove](./jetmove-function.md) oder [JetSeek](./jetseek-function.md)zu verschieben. Die zweite Phase ist die Daten Extraktions Phase. In dieser Phase können die in der temporären Tabelle gespeicherten Daten anhand der Funktionen extrahiert werden, die beim Erstellen der temporären Tabelle angefordert wurden.

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

Wenn die temporäre Tabelle nicht materialisiert ist und sich in der einfügephase befindet, verfügt der Cursor über die folgenden Funktionen, kann jedoch durch die angeforderten Optionen weiter eingeschränkt werden:

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
<td><p>Erfordert Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008.</p></td>
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
[JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md)  
[Jetclosetable](./jetclosetable-function.md)  
[Jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)  
[Jetdupcursor](./jetdupcursor-function.md)  
[Jetmove](./jetmove-function.md)  
[Jetrollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[Informations Parameter](./informational-parameters.md)  
[Temporäre Daten Bank Parameter](./temporary-database-parameters.md)
