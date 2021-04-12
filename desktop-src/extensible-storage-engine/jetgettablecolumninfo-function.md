---
description: 'Weitere Informationen zu: jetgettablecolumninfo-Funktion'
title: Jetgettablecolumninfo-Funktion
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
ms.openlocfilehash: f8c7b073ca9be90e89a1c6b99c010707e6405323
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104219739"
---
# <a name="jetgettablecolumninfo-function"></a>Jetgettablecolumninfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgettablecolumninfo-function"></a>Jetgettablecolumninfo-Funktion

Die **jetgettablecolumninfo** -Funktion Ruft Informationen über eine Tabellenspalte ab.

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

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*TableID*

Die Tabelle, die die Spalte enthält, für die Informationen abgerufen werden sollen.

*szcolumnname*

Der Name der Spalte, für die Informationen abgerufen werden sollen.

*pvresult*

Zeiger auf einen Puffer, der die Informationen empfängt. Der Typ des Puffers ist von *infolevel* abhängig. Der Aufrufer muss so konfiguriert werden, dass der Puffer entsprechend ausgerichtet wird.

*cbmax*

Die Größe (in Bytes) des Puffers, der in *pvresult* übergeben wurde.

*Infolevel*

Der Typ der Informationen, die für die durch *szcolumnname* angegebene Spalte abgerufen werden. Das Format der Daten, die in *pvresult* gespeichert sind, ist von *infolevel* abhängig. Das Schema der temporären Tabelle finden Sie unter [JET_COLUMNLIST](./jet-columnlist-structure.md).

  - JET_ColInfoListSortColumnid sortiert die temporäre Tabelle nach *ColumnID*.

  - Mit JET_ColInfoListCompact wird die Ausgabe komprimiert. Weitere Informationen zur Compact-Ausgabe finden Sie unter [JET_COLUMNLIST](./jet-columnlist-structure.md).

Die folgenden Optionen können für diesen Parameter festgelegt werden:

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
<td><p><em>pvresult</em> wird als <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>interpretiert, und die Felder der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> Struktur werden entsprechend ausgefüllt. JET_ColInfo und JET_ColInfoByColid beide die gleichen Informationen abrufen.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBase</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> Struktur interpretiert. Dies ähnelt einer <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> -Struktur. Wenn diese Funktion erfolgreich ausgeführt wird, wird die Struktur mit entsprechenden Werten aufgefüllt. Wenn diese Funktion fehlschlägt, enthält die Struktur nicht definierte Daten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoByColid</p></td>
<td><p><em>pvresult</em> wird als <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>interpretiert, mit dem Unterschied, dass die angeforderte Spalte (<em>szcolumname</em>) nicht der Zeichen <em>folgen</em> Spaltenname, sondern ein Zeiger auf einen <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>ist. JET_ColInfo und JET_ColInfoByColid beide die gleichen Informationen abrufen.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoList</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> Struktur interpretiert. Wenn diese Funktion erfolgreich ausgeführt wird, wird die Struktur mit entsprechenden Werten aufgefüllt. Eine temporäre Tabelle wird geöffnet und wird durch das <em>TableID</em> -Element von <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>identifiziert. Die Tabelle muss mit <a href="gg294087(v=exchg.10).md">jetclosetable</a>geschlossen werden. Wenn diese Funktion fehlschlägt, enthält die Struktur nicht definierte Daten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoListCompact</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> Struktur interpretiert. Wenn diese Funktion erfolgreich ausgeführt wird, wird die Struktur mit entsprechenden Werten aufgefüllt. Eine temporäre Tabelle wird geöffnet und wird durch das <em>TableID</em> -Element von <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>identifiziert. Die Tabelle muss mit <a href="gg294087(v=exchg.10).md">jetclosetable</a>geschlossen werden. Wenn diese Funktion fehlschlägt, enthält die Struktur nicht definierte Daten.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoListSortColumnid</p></td>
<td><p>Identisch mit JET_ColInfoList, die sich ergebende Tabelle wird jedoch nach <em>ColumnID</em>sortiert, anstelle des Spaltennamens.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoSysTabCursor</p></td>
<td><p>JET_ColInfoSysTabCursor ist veraltet, und die Verwendung von wird JET_errFeatureNotAvailable zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBaseByColId</p></td>
<td><p>Wie JET_ColInfoBase wird <em>pvresult</em> als <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>interpretiert, mit dem Unterschied, dass die angeforderte Spalte (<em>szcolumname</em>) nicht der Name der Zeichen <em>folgen</em> Spalte, sondern ein Zeiger auf eine <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>ist.</p>
<p><strong>Windows Vista:  </strong> Diese ist in Windows Vista und höher verfügbar.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitNonDerivedColumnsOnly</p></td>
<td><p>Gibt nur nicht abgeleitete Spalten zurück (wenn die Tabelle von einer Vorlage abgeleitet ist).</p>
<p>Dieser Wert kann logisch oder in <em>infolevel</em>sein, wenn die Basis- <em>infolevel</em> JET_ColInfoList ist.</p>
<p><strong>Windows Vista:  </strong> Dieser Wert wird in Windows Vista eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoGrbitMinimalInfo</p></td>
<td><p>Gibt nur den Spaltennamen und den Spaltennamen für jede Spalte zurück.</p>
<p>Dieser Wert kann logisch oder in <em>infolevel</em>sein, wenn die Basis- <em>infolevel</em> JET_ColInfoList ist.</p>
<p><strong>Windows Vista:  </strong> Dieser Wert wird in Windows Vista eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitSortByColumnid</p></td>
<td><p>Dient zum Sortieren der zurückgegebenen Spaltenliste nach ColumnID (Standardmäßig wird die Liste nach Spaltennamen sortiert).</p>
<p>Dieser Wert kann logisch oder in <em>infolevel</em>sein, wenn die Basis- <em>infolevel</em> JET_ColInfoList ist.</p>
<p><strong>Windows Vista:  </strong> Dieser Wert wird in Windows Vista eingeführt.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errColumnNotFound</p></td>
<td><p>Die Spalte mit dem Namen <em>szcolumnname</em> wurde in der Tabelle nicht gefunden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Es wurde eine ungültige <em>infolevel</em> angegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Dieser Fehler kann zurückgegeben werden, wenn Folgendes gilt:</p>
<ul>
<li><p>Es wurde ein ungültiger Name für <em>sztablename</em> angegeben.</p></li>
<li><p>Ein ungültiger Name für <em>szcolumnname</em> wurde angegeben.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Dieser Fehler kann zurückgegeben werden, wenn Folgendes gilt:</p>
<ul>
<li><p>Es wurde eine ungültige <em>infolevel</em> angegeben.</p></li>
<li><p>Ein NULL- <em>sztablename</em> -Wert wurde übermittelt.</p></li>
<li><p>Der Puffer ist zu klein.</p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

**Jetgettablecolumninfo** und [jetgetcolumninfo](./jetgetcolumninfo-function.md) rufen Informationen zu einer Spalte ab. Der Unterschied besteht darin, wie die Tabelle identifiziert wird:

  - **Jetgettablecolumninfo** identifiziert eine Tabelle nach *TableID*.

  - [Jetgetcolumninfo](./jetgetcolumninfo-function.md) identifiziert eine Tabelle mit der Kombination aus *DBID* und *sztablename* .

Beim Abrufen von Daten mit JET_ColInfoList, JET_ColInfoListSortColumnid oder JET_ColInfoListCompact wird eine temporäre Tabelle geöffnet. Die temporäre Tabelle enthält Daten, und die [JET_COLUMNLIST](./jet-columnlist-structure.md) Struktur enthält ausreichende Informationen, um die temporäre Tabelle zu durchlaufen. Die temporäre Tabelle muss mit [jetclosetable](./jetclosetable-function.md)geschlossen werden.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jetgettablecolumninfow</strong> (Unicode) und <strong>jetgettablecolumninfoa</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Speicher-Engine-Fehler](./extensible-storage-engine-errors.md)  
[Fehler Behandlungsparameter](./error-handling-parameters.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetclosetable](./jetclosetable-function.md)  
[Jetgetcolumninfo](./jetgetcolumninfo-function.md)  
[Jetgettablecolumninfo]()
