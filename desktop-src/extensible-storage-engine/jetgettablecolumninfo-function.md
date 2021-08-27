---
description: 'Weitere Informationen zu: JetGetTableColumnInfo-Funktion'
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
ms.openlocfilehash: e3940c07cc641d8c8d077c420f8c492ab5122b3f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984733"
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

Die Tabelle, die die Spalte enthält, für die Informationen abgerufen werden sollen.

*szColumnName*

Der Name der Spalte, für die Informationen abgerufen werden sollen.

*pvResult*

Zeiger auf einen Puffer, der die Informationen empfängt. Der Typ des Puffers ist von *InfoLevel* abhängig. Der Aufrufer muss so konfiguriert werden, dass er den Puffer entsprechend ausrichtet.

*cbMax*

Die Größe des Puffers in Bytes, der in *pvResult* übergeben wurde.

*InfoLevel*

Der Informationstyp, der für die spalte abgerufen wird, die von *szColumnName* angegeben wird. Das Format der in *pvResult* gespeicherten Daten hängt von *InfoLevel ab.* Das Schema der temporären Tabelle finden Sie unter [JET_COLUMNLIST](./jet-columnlist-structure.md).

  - JET_ColInfoListSortColumnid sortiert die temporäre Tabelle nach *columnid.*

  - JET_ColInfoListCompact komprimiert die Ausgabe. Weitere Informationen zur kompakten Ausgabe finden Sie unter [JET_COLUMNLIST](./jet-columnlist-structure.md).

Für diesen Parameter können die folgenden Optionen festgelegt werden:


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_ColInfo</p> | <p><em>pvResult</em> wird als <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>interpretiert, und die Felder der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> Struktur werden entsprechend ausgefüllt. JET_ColInfo und JET_ColInfoByColid beide die gleichen Informationen abrufen.</p> | 
| <p>JET_ColInfoBase</p> | <p><em>pvResult</em> wird als <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE-Struktur</a> interpretiert. Dies ähnelt einer <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> Struktur. Wenn diese Funktion erfolgreich ausgeführt wird, wird die Struktur mit entsprechenden Werten aufgefüllt. Wenn diese Funktion fehlschlägt, enthält die -Struktur nicht definierte Daten.</p> | 
| <p>JET_ColInfoByColid</p> | <p><em>pvResult</em> wird als <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>interpretiert, mit dem Unterschied, dass <em>die</em> angeforderte Spalte (<em>szColumName</em>) nicht der Name der Zeichenfolgenspalte ist, sondern ein Zeiger auf einen <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>. JET_ColInfo und JET_ColInfoByColid beide die gleichen Informationen abrufen.</p> | 
| <p>JET_ColInfoList</p> | <p><em>pvResult</em> wird als <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST-Struktur</a> interpretiert. Wenn diese Funktion erfolgreich ausgeführt wird, wird die Struktur mit entsprechenden Werten aufgefüllt. Eine temporäre Tabelle wird geöffnet und durch den <em>tableid-Member</em> von <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>identifiziert. Die Tabelle muss mit <a href="gg294087(v=exchg.10).md">JetCloseTable</a>geschlossen werden. Wenn diese Funktion fehlschlägt, enthält die -Struktur nicht definierte Daten.</p> | 
| <p>JET_ColInfoListCompact</p> | <p><em>pvResult</em> wird als <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST-Struktur</a> interpretiert. Wenn diese Funktion erfolgreich ausgeführt wird, wird die Struktur mit entsprechenden Werten aufgefüllt. Eine temporäre Tabelle wird geöffnet und durch den <em>tableid-Member</em> von <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>identifiziert. Die Tabelle muss mit <a href="gg294087(v=exchg.10).md">JetCloseTable</a>geschlossen werden. Wenn diese Funktion fehlschlägt, enthält die -Struktur nicht definierte Daten.</p> | 
| <p>JET_ColInfoListSortColumnid</p> | <p>Wie JET_ColInfoList wird die resultierende Tabelle jedoch anstelle des Spaltennamens nach <em>columnid</em>sortiert.</p> | 
| <p>JET_ColInfoSysTabCursor</p> | <p>JET_ColInfoSysTabCursor ist veraltet, und ihre Verwendung gibt JET_errFeatureNotAvailable zurück.</p> | 
| <p>JET_ColInfoBaseByColId</p> | <p>Wie JET_ColInfoBase wird <em>pvResult</em> als <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>interpretiert, außer dass dieses <em>InfoLevel</em> angibt, dass die angeforderte Spalte (<em>szColumName</em>) nicht der Name der Zeichenfolgenspalte ist, sondern ein Zeiger auf einen <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p><p><strong>Windows Vista:</strong> Dies ist in Windows Vista und höher verfügbar.</p> | 
| <p>JET_ColInfoGrbitNonDerivedColumnsOnly</p> | <p>Gibt nur nicht abgeleitete Spalten zurück (wenn die Tabelle von einer Vorlage abgeleitet ist).</p><p>Dieser Wert kann logisch oder in <em>infoLevel</em>aufgenommen werden, wenn der <em>Basis-InfoLevel</em> JET_ColInfoList ist.</p><p><strong>Windows Vista:</strong> Dieser Wert wird in Windows Vista eingeführt.</p> | 
| <p>JET_ColInfoGrbitMinimalInfo</p> | <p>Gibt nur den Spaltennamen und columnid jeder Spalte zurück.</p><p>Dieser Wert kann logisch oder in <em>infoLevel</em>aufgenommen werden, wenn der <em>Basis-InfoLevel</em> JET_ColInfoList ist.</p><p><strong>Windows Vista:</strong> Dieser Wert wird in Windows Vista eingeführt.</p> | 
| <p>JET_ColInfoGrbitSortByColumnid</p> | <p>Sortiert die zurückgegebene Spaltenliste nach columnid (standardmäßig wird die Liste nach Spaltenname sortiert).</p><p>Dieser Wert kann logisch oder in <em>infoLevel</em>aufgenommen werden, wenn der <em>Basis-InfoLevel</em> JET_ColInfoList ist.</p><p><strong>Windows Vista:</strong> Dieser Wert wird in Windows Vista eingeführt.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Die Spalte mit dem Namen <em>szColumnName</em> wurde in der Tabelle nicht gefunden.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Ein ungültiger <em>InfoLevel</em> wurde angegeben.</p> | 
| <p>JET_errInvalidName</p> | <p>Dieser Fehler kann zurückgegeben werden, wenn:</p><ul><li><p>Ein ungültiger Name für <em>szTableName</em> wurde angegeben.</p></li><li><p>Ein ungültiger Name für <em>szColumnName</em> wurde angegeben.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Dieser Fehler kann zurückgegeben werden, wenn:</p><ul><li><p>Ein ungültiger <em>InfoLevel</em> wurde angegeben.</p></li><li><p>Ein NULL <em>szTableName</em> wurde übergeben.</p></li><li><p>Der Puffer ist zu klein.</p></li></ul> | 



#### <a name="remarks"></a>Bemerkungen

**JetGetTableColumnInfo** und [JetGetColumnInfo](./jetgetcolumninfo-function.md) rufen informationen zu einer Spalte ab. Der Unterschied besteht darin, wie die Tabelle identifiziert wird:

  - **JetGetTableColumnInfo** identifiziert eine Tabelle anhand von *tableid.*

  - [JetGetColumnInfo](./jetgetcolumninfo-function.md) identifiziert eine Tabelle anhand der Kombinationen *dbid* und *szTableName.*

Beim Abrufen von Daten mit JET_ColInfoList, JET_ColInfoListSortColumnid oder JET_ColInfoListCompact wird eine temporäre Tabelle geöffnet. Die temporäre Tabelle enthält Daten, und die [JET_COLUMNLIST-Struktur](./jet-columnlist-structure.md) enthält ausreichende Informationen, um die temporäre Tabelle zu durchlaufen. Die temporäre Tabelle muss mit [JetCloseTable](./jetclosetable-function.md)geschlossen werden.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetGetTableColumnInfoW</strong> (Unicode) und <strong>JetGetTableColumnInfoA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Extensible Storage Engine Errors (Erweiterbare Storage-Engine-Fehler)](./extensible-storage-engine-errors.md)  
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
