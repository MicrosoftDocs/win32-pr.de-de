---
description: 'Weitere Informationen zu: jetgettableinfo-Funktion'
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
ms.openlocfilehash: 3362b5da8c6a79d78782e37920b9761b9888b15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960680"
---
# <a name="jetgettableinfo-function"></a>JetGetTableInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgettableinfo-function"></a>JetGetTableInfo-Funktion

Die **jetgettableinfo** -Funktion Ruft verschiedene Informationen zu einer Tabelle in einer Datenbank ab.

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

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*TableID*

Die Tabelle, auf die die Informationen angewendet werden.

*pvresult*

Zeiger auf einen Puffer, der die Informationen empfängt. Der Typ des Puffers ist von *infolevel* abhängig. Es liegt in der Verantwortung des Aufrufers, den Puffer entsprechend auszurichten.

*cbmax*

Die Größe (in Bytes) des Puffers, der in *pvresult* übergeben wurde.

*Infolevel*

Der Typ der Informationen, die für die durch *TableID* angegebene Tabelle abgerufen werden. Das Format der Daten, die in *pvresult* gespeichert sind, ist von *infolevel* abhängig.

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
<td><p>JET_TblInfo</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> Struktur interpretiert. Wenn die Methode erfolgreich ist, wird die <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> Struktur mit den entsprechenden Daten ausgefüllt. Wenn ein Fehler auftritt, ist der Inhalt nicht definiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoDbid</p></td>
<td><p><em>pvresult</em> wird als ein Array von zwei <a href="gg269248(v=exchg.10).md">JET_DBID</a> Objekten behandelt. Der Daten Bank Bezeichner der Datenbank, die Besitzer der Tabelle ist, wird in diesem Array zweimal gespeichert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoDumpTable</p></td>
<td><p>JET_TblInfoDumpTable ist veraltet. Die API gibt JET_errFeatureNotAvailable zurück.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoName</p></td>
<td><p>JET_TblInfoName Ruft den Namen der Tabelle ab und speichert Sie in <em>pvresult</em>. Wenn der Puffer zu klein ist, ist das Verhalten nicht definiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoMostMany</p></td>
<td><p>JET_TblInfoMostMany Ruft den Namen der Tabelle ab und speichert Sie in <em>pvresult</em>. Wenn der Puffer zu klein ist, ist das Verhalten nicht definiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoOLC</p></td>
<td><p>JET_TblInfoOLC ist veraltet. Die API gibt JET_errFeatureNotAvailable zurück.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoRvt</p></td>
<td><p>JET_TblInfoRvt ist veraltet. Die API gibt JET_errQueryNotSupported zurück.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoResetOLC</p></td>
<td><p>JET_TblInfoResetOLC ist veraltet. Die API gibt JET_errFeatureNotAvailable zurück.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoSpaceAlloc</p></td>
<td><p><em>pvresult</em> wird als ein Array aus zwei ulongs interpretiert:</p>
<ul>
<li><p>Der erste <strong>ulong</strong> -Wert ist die Anzahl der Seiten in der Tabelle.</p></li>
<li><p>Der zweite <strong>ulong</strong> -Wert ist die zieldichte von Seiten für die Tabelle.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoSpaceAvailable</p></td>
<td><p><em>pvresult</em> wird als <strong>ulong</strong>interpretiert. Der <strong>ulong</strong> ist die Summe aus der Anzahl der Seiten, die in der Tabelle, den Indizes und der Struktur für lange Werte verfügbar sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoSpaceOwned</p></td>
<td><p><em>pvresult</em> wird als <strong>ulong</strong>interpretiert. <strong>Ulong</strong> ist die Summe der Anzahl der Seiten, die im Besitz der Tabelle sind (einschließlich der Indizes und der Long-Wert-Struktur und sämtlicher verfügbarer Seiten).</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoSpaceUsage</p></td>
<td><p>Das Verhalten der API hängt davon ab, wie groß der an die API weiter gegebene Puffer ist. Zwei <em>cbmax</em> -Werte müssen mindestens (2 * sizeof (ULONG)) sein.</p>
<ul>
<li><p>Wenn <em>cbmax</em> (2 * sizeof (ULONG)) ist, wird <em>pvresult</em> als ein Array aus zwei ulongs interpretiert:</p>
<ul>
<li><p>Der erste <strong>ulong</strong> -Wert ist die Anzahl der im Besitz befindlichen Blöcke der Tabelle.</p></li>
<li><p>Der zweite <strong>ulong</strong> -Wert ist die Anzahl der verfügbaren Blöcke der Tabelle.</p></li>
</ul></li>
<li><p><em>pvresult</em> wird als ein Array von interpretiert:</p>
<ul>
<li><p>Der erste <strong>ulong</strong> -Wert ist die Anzahl der im Besitz befindlichen Blöcke der Tabelle.</p></li>
<li><p>Der zweite <strong>ulong</strong> -Wert ist die Anzahl der verfügbaren Blöcke der Tabelle.</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoTemplateTableName</p></td>
<td><p><em>pvresult</em> wird als Zeichen folgen Puffer interpretiert. Der Puffer muss mindestens JET_cbNameMost + 1 sein, einschließlich des abschließenden <strong>null</strong>-Werte. Wenn die Tabelle eine abgeleitete Tabelle ist, wird der Puffer mit dem Namen der Tabelle ausgefüllt, von der die abgeleitete Tabelle Ihre DDL geerbt hat. Wenn die Tabelle keine abgeleitete Tabelle ist, wird für den Puffer eine leere Zeichenfolge verwendet.</p></td>
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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Der Puffer war zu klein.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Es wurde eine veraltete <em>infolevel</em> angegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Der Puffer war nicht die richtige Größe.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidOperation</p></td>
<td><p>Die Tabelle, die in die Tabelle übertragen wurde, war eine temporäre Tabelle, und die angeforderte <em>infolevel</em> kann für eine temporäre Tabelle nicht abgerufen werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errObjectNotFound</p></td>
<td><p>Die Tabelle, die in die Tabelle übertragen wurde, war eine temporäre Tabelle, und die angeforderte <em>infolevel</em> kann für eine temporäre Tabelle nicht abgerufen werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errQueryNotSupported</p></td>
<td><p><em>Infolevel</em> wird nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Die Tabelle wird von einem anderen Daten Bank Vorgang verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableLocked</p></td>
<td><p>Die Tabelle wird durch einen anderen Daten Bank Vorgang gesperrt.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableInUseBySystem</p></td>
<td><p>Die Tabelle wird vom System verwendet. Diese Warnung ist nicht schwerwiegend.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Einige Informationen sind für temporäre Tabellen ungültig (siehe [jetopdtemptable](./jetopentemptable-function.md)).

Die Tabellenstatistiken enthalten die Anzahl der Datensätze und die Anzahl der Seiten im gruppierten Index (d. h. den Index, der die Daten des Datensatzes enthält). Der Zugriff auf die Index Statistiken erfolgt separat über den Namen, mithilfe von [jetgetindexinfo](./jetgetindexinfo-function.md) oder [jetgettableindexinfo](./jetgettableindexinfo-function.md).

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
<td><p>Implementiert als <strong>jetgettableinfow</strong> (Unicode) und <strong>jetgettableinfoa</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[Jetgetindexinfo](./jetgetindexinfo-function.md)  
[Jetgetobjectinfo](./jetgetobjectinfo-function.md)  
[Jetgettableindexinfo](./jetgettableindexinfo-function.md)  
[Jetopumtemptable](./jetopentemptable-function.md)
