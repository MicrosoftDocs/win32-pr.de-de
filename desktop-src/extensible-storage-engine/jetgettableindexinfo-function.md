---
description: 'Weitere Informationen zu: jetgettableindexinfo-Funktion'
title: JetGetTableIndexInfo-Funktion
TOCTitle: JetGetTableIndexInfo Function
ms:assetid: d250d254-2b10-4fe7-bbb1-72bb967f22dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294102(v=EXCHG.10)
ms:contentKeyID: 32765717
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableIndexInfoW
- JetGetTableIndexInfoA
- JetGetTableIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 904391218fbd073cd273655ce74fdec116b6a22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218588"
---
# <a name="jetgettableindexinfo-function"></a>JetGetTableIndexInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgettableindexinfo-function"></a>JetGetTableIndexInfo-Funktion

Die **jetgettableindexinfo** -Funktion Ruft Informationen zu einem Index ab.

```cpp
    JET_ERR JET_API JetGetTableIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*TableID*

Die Datenbanktabelle, die den Index enthält, der die erforderlichen Informationen enthält.

*szindexname*

Der Name des Indexes, der Informationen enthält, die abgerufen werden.

*pvresult*

Zeiger auf einen Puffer, der die Informationen empfängt. Der Puffer muss so ausgerichtet werden, dass er den erforderlichen Typ enthält. Der Typ des Puffers ist abhängig vom *infolevel* -Parameter.

*cbresult*

Die Größe (in Bytes) des Puffers, der im *pvresult* -Parameter übergeben wird.

*Infolevel*

Gibt an, welche Informationen in *pvresult* gespeichert werden. Gültige Werte sind:

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
<td><p>JET_IdxInfo</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Struktur interpretiert. Bei Erfolg empfängt die <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Strukturinformationen über den Index. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoLCID</p></td>
<td><p><em>pvresult</em> wird als LCID interpretiert. Bei Erfolg enthält die LCID den Gebiets Schema Bezeichner des Indexes. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoList</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Struktur interpretiert. Bei Erfolg empfängt die <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Strukturinformationen über den Index. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoOLC</p></td>
<td><p>JET_IdxInfoOLC ist veraltet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoResetOLC</p></td>
<td><p>JET_IdxInfoResetOLC ist veraltet.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoSpaceAlloc</p></td>
<td><p><em>pvresult</em> wird als ULONG interpretiert. Bei Erfolg enthält der ULONG die Speicherplatz Verwendung des Indexes. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoSysTabCursor</p></td>
<td><p>JET_IdxInfoSysTabCursor ist veraltet.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoLangid</p></td>
<td><p>JET_IdxInfoLangid ist veraltet. Verwenden Sie stattdessen JET_IdxInfoLCID und das-Makro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">langidfromlcid</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoCount</p></td>
<td><p><em>pvresult</em> wird als ULONG interpretiert. Bei Erfolg enthält der ULONG die Anzahl der Indizes für die angegebene Tabelle. <em>szindexname</em> wird ignoriert. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoVarSegMac</p></td>
<td><p><em>pvresult</em> wird als ushort interpretiert. Bei Erfolg enthält der ushort den Wert von <em>cbvarsegmac</em> , der beim Erstellen des Indexes verwendet wurde. Unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> finden Sie eine Beschreibung von <em>cbvarsegmac</em>. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoIndexId</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>interpretiert. Bei Erfolg empfängt die <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> Strukturinformationen über den Index. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoKeyMost</p></td>
<td><p><em>pvresult</em> wird als ushort interpretiert. Bei Erfolg enthält der ushort den Wert von cbkeymost, der beim Erstellen des Indexes verwendet wurde. Eine Beschreibung von cbkeymost finden Sie in der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoCreateIndex</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur interpretiert. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p>
<p><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex wurde in Windows 7 eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoCreateIndex2</p></td>
<td><p><em>pvresult</em> wird als <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur interpretiert. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p>
<p><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 wurde in Windows 7 eingeführt.</p></td>
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
<td><p>JET_errIndexNotFound</p></td>
<td><p>Der angegebene Index wurde in der angegebenen Tabelle nicht gefunden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>Der als <em>pvresult</em> weiter gegebene Puffer war zu klein. Der Inhalt des Puffers ist nicht definiert.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

[Jetgetindexinfo](./jetgetindexinfo-function.md) und **jetgettableindexinfo** rufen identische Informationen zu einem Index ab. Der Unterschied besteht darin, wie die Tabelle angegeben wird. [Jetgetindexinfo](./jetgetindexinfo-function.md) erwartet eine Datenbank (*DBID*) und den Namen einer Tabelle (*sztablename*), während **jetgettableindexinfo** einen Tabellen Bezeichner (*TableID*) erwartet.

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
<td><p>Implementiert als <strong>jetgettableindexinfow</strong> (Unicode) und <strong>jetgettableindexinfoa</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[Jetgetindexinfo](./jetgetindexinfo-function.md)
