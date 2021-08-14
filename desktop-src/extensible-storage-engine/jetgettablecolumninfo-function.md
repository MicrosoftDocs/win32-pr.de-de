---
description: Weitere Informationen finden Sie unter JetGetTableColumnInfo-Funktion.
title: JetGetTableColumnInfo-Funktion
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 63e913e68a3aea8f220c713b07becdeecb785a619b73a833bb6a0e9c3c1d37a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979020"
---
# <a name="jetgettablecolumninfo-function"></a>JetGetTableColumnInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgettablecolumninfo-function"></a>JetGetTableColumnInfo-Funktion

Die **JetGetTableColumnInfo-Funktion** ruft Informationen zu einer Tabellenspalte ab.

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*tableid*

Die Tabelle, die die Spalte enthält, für die Informationen abgerufen werden.

*szColumnName*

Der Name der Spalte, für die Informationen abgerufen werden.

*pvResult*

Zeiger auf einen Puffer, der die Informationen erhält. Der Typ des Puffers ist von *InfoLevel abhängig.* Der Aufrufer muss so konfiguriert werden, dass der Puffer entsprechend ausgerichtet wird.

*cbMax*

Die Größe des Puffers in Bytes, der in *pvResult übergeben wurde.*

*InfoLevel*

Der Typ der Informationen, die für die Spalte abgerufen werden, die durch *szColumnName angegeben wird.* Das Format der in *pvResult* gespeicherten Daten hängt von *InfoLevel ab.* Das Schema der temporären Tabelle finden Sie unter [JET_COLUMNLIST](./jet-columnlist-structure.md).

  - JET_ColInfoListSortColumnid sortiert die temporäre Tabelle nach *columnid*.

  - JET_ColInfoListCompact komprimiert die Ausgabe. Weitere Informationen zur kompakten Ausgabe finden Sie unter [JET_COLUMNLIST](./jet-columnlist-structure.md).

Für diesen Parameter können die folgenden Optionen festgelegt werden:

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
<td><p>JET_ColInfo</p></td>
<td><p><em>pvResult</em> wird als <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>interpretiert, und die Felder der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF-Struktur</a> werden entsprechend ausgefüllt. JET_ColInfo und JET_ColInfoByColid rufen beide dieselben Informationen ab.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBase</p></td>
<td><p><em>pvResult</em> wird als <a href="gg269194(v=exchg.10).md">eine</a> JET_COLUMNBASE interpretiert. Dies ähnelt einer <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> Struktur. Wenn diese Funktion erfolgreich ist, wird die -Struktur mit entsprechenden Werten aufgefüllt. Wenn diese Funktion fehlschlägt, enthält die Struktur nicht definierte Daten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoByColid</p></td>
<td><p><em>pvResult</em> wird als JET_COLUMNDEF <a href="gg294130(v=exchg.10).md">interpretiert,</a>mit der Ausnahme, dass <em>infoLevel</em> angibt, dass die angeforderte Spalte (<em>szColumName</em>) nicht der Name der Zeichenfolgenspalte, sondern ein Zeiger auf eine <a href="gg294104(v=exchg.10).md">JET_COLUMNID.</a> JET_ColInfo und JET_ColInfoByColid rufen beide dieselben Informationen ab.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoList</p></td>
<td><p><em>pvResult</em> wird als <a href="gg269228(v=exchg.10).md">eine</a> JET_COLUMNLIST interpretiert. Wenn diese Funktion erfolgreich ist, wird die -Struktur mit entsprechenden Werten aufgefüllt. Eine temporäre Tabelle wird geöffnet und durch den <em>tableid-Member</em> <a href="gg269228(v=exchg.10).md">von</a>JET_COLUMNLIST. Die Tabelle muss mit <a href="gg294087(v=exchg.10).md">JetCloseTable geschlossen werden.</a> Wenn diese Funktion fehlschlägt, enthält die Struktur nicht definierte Daten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoListCompact</p></td>
<td><p><em>pvResult</em> wird als <a href="gg269228(v=exchg.10).md">eine</a> JET_COLUMNLIST interpretiert. Wenn diese Funktion erfolgreich ist, wird die -Struktur mit entsprechenden Werten aufgefüllt. Eine temporäre Tabelle wird geöffnet und durch den <em>tableid-Member</em> <a href="gg269228(v=exchg.10).md">von</a>JET_COLUMNLIST. Die Tabelle muss mit <a href="gg294087(v=exchg.10).md">JetCloseTable geschlossen werden.</a> Wenn diese Funktion fehlschlägt, enthält die Struktur nicht definierte Daten.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoListSortColumnid</p></td>
<td><p>Wie JET_ColInfoList, wird die resultierende Tabelle jedoch nach <em>columnid</em>statt nach spaltenname sortiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoSysTabCursor</p></td>
<td><p>JET_ColInfoSysTabCursor ist veraltet, und ihre Verwendung gibt JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBaseByColId</p></td>
<td><p>Wie JET_ColInfoBase wird <em>pvResult</em> als JET_COLUMNBASE <a href="gg269194(v=exchg.10).md">interpretiert,</a>außer dass <em>infoLevel</em> angibt, dass die angeforderte Spalte (<em>szColumName</em>) nicht der Name der Zeichenfolgenspalte, sondern ein Zeiger auf eine <a href="gg294104(v=exchg.10).md">JET_COLUMNID.</a></p>
<p><strong>Windows Vista:</strong> Dies ist in Windows Vista und höher verfügbar.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitNonDerivedColumnsOnly</p></td>
<td><p>Geben Sie nur nicht abgeleitete Spalten zurück (wenn die Tabelle von einer Vorlage abgeleitet ist).</p>
<p>Dieser Wert kann logisch oder in <em>InfoLevel sein,</em>wenn die <em>Basisinformationsebene</em> JET_ColInfoList.</p>
<p><strong>Windows Vista:</strong> Dieser Wert wird in Windows Vista eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoGrbitMinimalInfo</p></td>
<td><p>Geben Sie nur den Spaltennamen und die Spalten-ID der einzelnen Spalten zurück.</p>
<p>Dieser Wert kann logisch oder in <em>InfoLevel sein,</em>wenn die <em>Basisinformationsebene</em> JET_ColInfoList.</p>
<p><strong>Windows Vista:</strong> Dieser Wert wird in Windows Vista eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitSortByColumnid</p></td>
<td><p>Sortiert die zurückgegebene Spaltenliste nach columnid (standardmäßig wird die Liste nach Spaltenname sortiert).</p>
<p>Dieser Wert kann logisch oder in <em>InfoLevel sein,</em>wenn die <em>Basisinformationsebene</em> JET_ColInfoList.</p>
<p><strong>Windows Vista:</strong> Dieser Wert wird in Windows Vista eingeführt.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errColumnNotFound</p></td>
<td><p>Die Spalte <em>szColumnName</em> wurde in der Tabelle nicht gefunden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Ein <em>fehlerhafter InfoLevel</em> wurde angegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Dieser Fehler kann zurückgegeben werden, wenn:</p>
<ul>
<li><p>Es wurde ein fehlerhafter Name <em>für szTableName</em> angegeben.</p></li>
<li><p>Es wurde ein fehlerhafter <em>Name für szColumnName</em> angegeben.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Dieser Fehler kann zurückgegeben werden, wenn:</p>
<ul>
<li><p>Ein <em>fehlerhafter InfoLevel</em> wurde angegeben.</p></li>
<li><p>Ein NULL <em>szTableName</em> wurde übergeben.</p></li>
<li><p>Der Puffer ist zu klein.</p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Hinweise

**JetGetTableColumnInfo und** [JetGetColumnInfo](./jetgetcolumninfo-function.md) rufen informationen zu einer Spalte ab. Der Unterschied zwischen ihnen besteht in der Art und Weise, wie die Tabelle identifiziert wird:

  - **JetGetTableColumnInfo** identifiziert eine Tabelle mit *tableid*.

  - [JetGetColumnInfo](./jetgetcolumninfo-function.md) identifiziert eine Tabelle durch *eine Kombination aus dbid* und *szTableName.*

Beim Abrufen von Daten mit JET_ColInfoList, JET_ColInfoListSortColumnid oder JET_ColInfoListCompact wird eine temporäre Tabelle geöffnet. Die temporäre Tabelle enthält Daten, und [JET_COLUMNLIST](./jet-columnlist-structure.md) Struktur enthält genügend Informationen, um die temporäre Tabelle zu durchlaufen. Die temporäre Tabelle muss mit [JetCloseTable geschlossen werden.](./jetclosetable-function.md)

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
<td><p>In Esent.h deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>JetGetTableColumnInfoW</strong> (Unicode) und <strong>JetGetTableColumnInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage Engine-Fehler](./extensible-storage-engine-errors.md)  
[Fehlerbehandlungsparameter](./error-handling-parameters.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetColumnInfo](./jetgetcolumninfo-function.md)  
[JetGetTableColumnInfo]()
