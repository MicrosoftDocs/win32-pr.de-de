---
description: Weitere Informationen finden Sie unter JetGetTableInfo-Funktion.
title: JetGetTableInfo-Funktion
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c17e1c5aa23e8e2fe77aaa07f98fee1b2df0c12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465797"
---
# <a name="jetgettableinfo-function"></a>JetGetTableInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgettableinfo-function"></a>JetGetTableInfo-Funktion

Die **JetGetTableInfo-Funktion** ruft verschiedene Informationen zu einer Tabelle in einer Datenbank ab.

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*tableid*

Die Tabelle, für die die Informationen gelten.

*pvResult*

Zeiger auf einen Puffer, der die Informationen erhält. Der Typ des Puffers ist von *InfoLevel abhängig.* Es liegt in der Verantwortung des Aufrufers, den Puffer entsprechend auszurichten.

*cbMax*

Die Größe des Puffers in Bytes, der in *pvResult übergeben wurde.*

*InfoLevel*

Der Typ der Informationen, die für die Tabelle abgerufen werden, die durch *tableid angegeben wird.* Das Format der in *pvResult* gespeicherten Daten hängt von *InfoLevel ab.*

Für diesen Parameter können die folgenden Optionen festgelegt werden:


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_TblInfo</p> | <p><em>pvResult</em> wird als <a href="gg269353(v=exchg.10).md">eine</a> JET_OBJECTINFO interpretiert. Wenn die Methode erfolgreich ist, <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> die Struktur mit den entsprechenden Daten aufgefüllt. Wenn ein Fehler auftritt, ist der Inhalt nicht definiert.</p> | 
| <p>JET_TblInfoDbid</p> | <p><em>pvResult</em> wird als Array von zwei JET_DBID <a href="gg269248(v=exchg.10).md">behandelt.</a> Der Datenbankbezeichner der Datenbank, die die Tabelle besitzt, wird zweimal in diesem Array gespeichert.</p> | 
| <p>JET_TblInfoDumpTable</p> | <p>JET_TblInfoDumpTable ist veraltet. Die API gibt JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoName</p> | <p>JET_TblInfoName ruft den Namen der Tabelle ab und speichert ihn in <em>pvResult</em>. Wenn der Puffer zu klein ist, ist das Verhalten nicht definiert.</p> | 
| <p>JET_TblInfoMostMany</p> | <p>JET_TblInfoMostMany ruft den Namen der Tabelle ab und speichert ihn in <em>pvResult</em>. Wenn der Puffer zu klein ist, ist das Verhalten nicht definiert.</p> | 
| <p>JET_TblInfoOLC</p> | <p>JET_TblInfoOLC ist veraltet. Die API gibt JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoRvt</p> | <p>JET_TblInfoRvt ist veraltet. Die API gibt JET_errQueryNotSupported.</p> | 
| <p>JET_TblInfoResetOLC</p> | <p>JET_TblInfoResetOLC ist veraltet. Die API gibt JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoSpaceAlloc</p> | <p><em>pvResult</em> wird als Array von zwei ULONGs interpretiert:</p><ul><li><p>Die erste <strong>ULONG ist</strong> die Anzahl der Seiten in der Tabelle.</p></li><li><p>Die zweite <strong>ULONG ist</strong> die Zieldichte der Seiten für die Tabelle.</p></li></ul> | 
| <p>JET_TblInfoSpaceAvailable</p> | <p><em>pvResult</em> wird als <strong>ULONG interpretiert.</strong> Der <strong>ULONG-Wert</strong> ist die Summe der Anzahl der in der Tabelle verfügbaren Seiten, ihrer Indizes und der Long-Value-Struktur.</p> | 
| <p>JET_TblInfoSpaceOwned</p> | <p><em>pvResult</em> wird als <strong>ULONG interpretiert.</strong> Der <strong>ULONG-Wert</strong> ist die Summe der Anzahl der Seiten, die sich im Besitz der Tabelle befinden (einschließlich der Indizes, der Long-Value-Struktur und aller verfügbaren Seiten).</p> | 
| <p>JET_TblInfoSpaceUsage</p> | <p>Das Verhalten der API hängt davon ab, wie groß der Puffer ist, der an die API übergeben wird. Zwei <em>cbMax-Werte</em> müssen mindestens ( 2 * sizeof( ULONG ) ) sein.</p><ul><li><p>Wenn <em>cbMax</em> ist ( 2 * sizeof( ULONG ) ), <em>wird pvResult</em> als Array von zwei ULONGs interpretiert:</p><ul><li><p>Die erste <strong>ULONG ist</strong> die Anzahl der eigenen Extents der Tabelle.</p></li><li><p>Das zweite <strong>ULONG ist</strong> die Anzahl der verfügbaren Extents der Tabelle.</p></li></ul></li><li><p><em>pvResult</em> wird als Array von interpretiert:</p><ul><li><p>Die erste <strong>ULONG ist</strong> die Anzahl der eigenen Extents der Tabelle.</p></li><li><p>Das zweite <strong>ULONG ist</strong> die Anzahl der verfügbaren Extents der Tabelle.</p></li></ul></li></ul> | 
| <p>JET_TblInfoTemplateTableName</p> | <p><em>pvResult</em> wird als Zeichenfolgenpuffer interpretiert. Der Puffer muss mindestens JET_cbNameMost + 1 sein, einschließlich des beendenden <strong>NULL-Werts.</strong> Wenn es sich bei der Tabelle um eine abgeleitete Tabelle handelt, wird der Puffer mit dem Namen der Tabelle gefüllt, von der die abgeleitete Tabelle ihre DDL geerbt hat. Wenn die Tabelle keine abgeleitete Tabelle ist, ist der Puffer eine leere Zeichenfolge.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Der Puffer war zu klein.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Ein veraltetes <em>InfoLevel</em> wurde angegeben.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Der Puffer hat nicht die richtige Größe.</p> | 
| <p>JET_errInvalidOperation</p> | <p>Die übergebene Tabelle war eine temporäre Tabelle, und der angeforderte <em>InfoLevel</em> kann nicht für eine temporäre Tabelle abgerufen werden.</p> | 
| <p>JET_errObjectNotFound</p> | <p>Die übergebene Tabelle war eine temporäre Tabelle, und der angeforderte <em>InfoLevel</em> kann nicht für eine temporäre Tabelle abgerufen werden.</p> | 
| <p>JET_errQueryNotSupported</p> | <p><em>InfoLevel</em> wird nicht unterstützt.</p> | 
| <p>JET_errTableInUse</p> | <p>Die Tabelle wird von einem anderen Datenbankvorgang verwendet.</p> | 
| <p>JET_errTableLocked</p> | <p>Die Tabelle wird durch einen anderen Datenbankvorgang gesperrt.</p> | 
| <p>JET_wrnTableInUseBySystem</p> | <p>Die Tabelle wird vom System verwendet. Diese Warnung ist nichtfatal.</p> | 



#### <a name="remarks"></a>Hinweise

Einige Informationen sind für temporäre Tabellen ungültig (siehe [JetOpenTempTable](./jetopentemptable-function.md)).

Die Tabellenstatistiken enthalten die Anzahl von Datensätzen und die Anzahl der Seiten im gruppierten Index (d.amp;n.b. der Index, der die Datensatzdaten enthält). Auf die Indexstatistiken wird separat anhand des Namens zugegriffen, indem [JetGetIndexInfo](./jetgetindexinfo-function.md) oder [JetGetTableIndexInfo verwendet](./jetgettableindexinfo-function.md)wird.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetGetTableInfoW</strong> (Unicode) und <strong>JetGetTableInfoA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)
