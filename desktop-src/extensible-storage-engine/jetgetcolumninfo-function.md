---
description: Weitere Informationen finden Sie unter JetGetColumnInfo-Funktion.
title: JetGetColumnInfo-Funktion
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97b6dfc76de520249880314ecd32769951c7b927
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479106"
---
# <a name="jetgetcolumninfo-function"></a>JetGetColumnInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetcolumninfo-function"></a>JetGetColumnInfo-Funktion

Die **JetGetColumnInfo-Funktion** ruft Informationen zu einer Spalte ab.

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*Dbid*

Identifiziert zusammen mit *szTableName* die Tabelle, die die Spalte enthält, aus der die Informationen abgerufen werden.

*szTableName*

Identifiziert zusammen mit *dbid* die Tabelle, die die Spalte enthält, aus der die Informationen abgerufen werden.

*szColumnName*

Der Name der Spalte, für die Informationen abgerufen werden.

*pvResult*

Zeiger auf einen Puffer, der die Informationen erhält. Der Typ des Puffers ist von *InfoLevel abhängig.* Der Aufrufer muss so konfiguriert werden, dass der Puffer entsprechend ausgerichtet wird.

*cbMax*

Die Größe des Puffers in Bytes, der in *pvResult übergeben wird.*

*InfoLevel*

Der Typ der Informationen, die für die Spalte abgerufen werden, die durch *szColumnName angegeben wird.* Das Format der in *pvResult* gespeicherten Daten hängt von diesem Parameter ab. Das Schema der temporären Tabelle finden Sie unter [JET_COLUMNLIST](./jet-columnlist-structure.md).

Diese *InfoLevels unterscheiden* sich durch:

  - JET_ColInfoListSortColumnid sortiert die temporäre Tabelle nach *columnid*.

  - JET_ColInfoListCompact komprimiert die Ausgabe. Weitere Informationen zur kompakten Ausgabe finden Sie unter [JET_COLUMNLIST](./jet-columnlist-structure.md).

Die folgenden Optionen stehen für die Verwendung mit diesem Parameter zur Verfügung.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_ColInfo</p> | <p>JET_ColInfo und JET_ColInfoByColid rufen beide die gleichen Informationen ab. <em>pvResult</em> wird als <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>interpretiert, und die Felder der JET_COLUMNDEF <a href="gg294130(v=exchg.10).md">werden</a> entsprechend ausgefüllt.</p> | 
| <p>JET_ColInfoBase</p> | <p><em>pvResult</em> wird als <a href="gg269194(v=exchg.10).md">eine</a> JET_COLUMNBASE interpretiert. Dies ähnelt einer <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> Struktur. Wenn diese Funktion erfolgreich ist, wird die -Struktur mit entsprechenden Werten aufgefüllt. Wenn diese Funktion fehlschlägt, enthält die Struktur nicht definierte Daten.</p> | 
| <p>JET_ColInfoByColid</p> | <p>Wie JET_ColInfo wird <em>pvResult</em> als <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF interpretiert,</a>mit der Ausnahme, dass <em>infoLevel</em> angibt, dass die angeforderte Spalte (<em>szColumName</em>) nicht der Name der Zeichenfolgenspalte, sondern ein Zeiger auf eine <a href="gg294104(v=exchg.10).md">JET_COLUMNID.</a></p> | 
| <p>JET_ColInfoList</p> | <p><em>pvResult</em> wird als <a href="gg269228(v=exchg.10).md">eine</a> JET_COLUMNLIST interpretiert. Wenn diese Funktion erfolgreich ist, wird die -Struktur mit entsprechenden Werten aufgefüllt. Eine temporäre Tabelle wird geöffnet und durch den <strong>tableid-Member</strong> der JET_COLUMNLIST <a href="gg269228(v=exchg.10).md">identifiziert.</a> Die Tabelle muss mit <a href="gg294087(v=exchg.10).md">JetCloseTable geschlossen werden.</a> Wenn diese Funktion fehlschlägt, enthält die Struktur nicht definierte Daten.</p> | 
| <p>JET_ColInfoListCompact</p> | <p>Identisch mit JET_ColInfoList.</p> | 
| <p>JET_ColInfoListSortColumnid</p> | <p>Identisch mit JET_ColInfoList; die resultierende Tabelle wird jedoch nach columnid anstatt nach spaltenname sortiert.</p> | 
| <p>JET_ColInfoSysTabCursor</p> | <p>JET_ColInfoSysTabCursor ist veraltet, und ihre Verwendung gibt JET_errFeatureNotAvailable.</p> | 
| <p>JET_ColInfoBaseByColId</p> | <p>Wie JET_ColInfoBase wird <em>pvResult</em> als <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE interpretiert,</a>außer dass <em>infoLevel</em> angibt, dass die angeforderte Spalte (<em>szColumName</em>) nicht der Name der Zeichenfolgenspalte, sondern ein Zeiger auf eine <a href="gg294104(v=exchg.10).md">JET_COLUMNID.</a></p><p><strong>Windows Vista:</strong> Dieser Wert wird in Windows Vista eingeführt.</p> | 
| <p>JET_ColInfoGrbitNonDerivedColumnsOnly</p> | <p>Geben Sie nur nicht abgeleitete Spalten zurück (wenn die Tabelle von einer Vorlage abgeleitet ist).</p><p>Dieser Wert kann logisch oder in <em>infoLevel</em>sein, wenn der <em>InfoLevel-Basiswert</em> JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Dieser Wert wird in Windows Vista eingeführt.</p> | 
| <p>JET_ColInfoGrbitMinimalInfo</p> | <p>Geben Sie nur den Spaltennamen und die Spalten-ID der einzelnen Spalten zurück.</p><p>Dieser Wert kann logisch oder in <em>infoLevel</em>sein, wenn der <em>InfoLevel-Basiswert</em> JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Dieser Wert wird in Windows Vista eingeführt.</p> | 
| <p>JET_ColInfoGrbitSortByColumnid</p> | <p>Sortiert die zurückgegebene Spaltenliste nach columnid (standardmäßig wird die Liste nach Spaltenname sortiert).</p><p>Dieser Wert kann logisch oder in <em>infoLevel</em>sein, wenn der <em>InfoLevel-Basiswert</em> JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Dieser Wert wird in Windows Vista eingeführt.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Die Spalte <em>szColumnName</em> wurde in der Tabelle nicht gefunden.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Ein <em>fehlerhafter InfoLevel</em> wurde angegeben.</p> | 
| <p>JET_errInvalidName</p> | <p>Dieser Fehler kann zurückgegeben werden, wenn:</p><ul><li><p>Es wurde ein fehlerhafter Name <em>für szTableName</em> angegeben.</p></li><li><p>Es wurde ein fehlerhafter <em>Name für szColumnName</em> angegeben.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Dieser Fehler kann zurückgegeben werden, wenn:</p><ul><li><p>Ein <em>fehlerhafter InfoLevel</em> wurde angegeben.</p></li><li><p>Ein NULL <em>szTableName</em> wurde übergeben.</p></li><li><p>Der Puffer ist zu klein.</p></li></ul> | 



#### <a name="remarks"></a>Hinweise

[JetGetTableColumnInfo und](./jetgettablecolumninfo-function.md) **JetGetColumnInfo** rufen informationen zu einer Spalte ab. Der Unterschied zwischen ihnen besteht in der Art und Weise, wie die Tabelle identifiziert wird:

  - [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifiziert eine Tabelle mit *tableid*.

  - **JetGetColumnInfo** identifiziert eine Tabelle durch *eine Kombination aus dbid* und *szTableName.*

Beim Abrufen von Daten mit JET_ColInfoList, JET_ColInfoListSortColumnid oder JET_ColInfoListCompact wird eine temporäre Tabelle geöffnet. Die temporäre Tabelle enthält Daten, und [JET_COLUMNLIST](./jet-columnlist-structure.md) Struktur enthält genügend Informationen, um die temporäre Tabelle zu durchlaufen. Die temporäre Tabelle muss mit [JetCloseTable geschlossen werden.](./jetclosetable-function.md)

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetGetColumnInfoW</strong> (Unicode) und <strong>JetGetColumnInfoA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Fehlerbehandlungsparameter](./error-handling-parameters.md)  
[Erweiterbare Storage-Engine-Fehler](./extensible-storage-engine-errors.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
