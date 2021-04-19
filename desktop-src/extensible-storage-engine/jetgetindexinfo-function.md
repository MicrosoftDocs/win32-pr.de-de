---
description: 'Weitere Informationen zu: jetgetindexinfo-Funktion'
title: JetGetIndexInfo-Funktion
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362611"
---
# <a name="jetgetindexinfo-function"></a>JetGetIndexInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetindexinfo-function"></a>JetGetIndexInfo-Funktion

Die **jetgetindexinfo** -Funktion Ruft Informationen zu einem Index ab.

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*DBID*

Der für den API-Befehl zu verwendende Daten Bank Bezeichner.

*sztablename*

Der Name der Tabelle mit dem Index, der die abzurufenden Informationen enthält.

*szindexname*

Der Name des Indexes mit den abzurufenden Informationen.

*pvresult*

Zeiger auf einen Puffer, der die gewünschten Informationen empfängt. Der Puffer muss so ausgerichtet werden, dass er den erforderlichen Typ enthält. Der Typ des Puffers ist abhängig vom *infolevel* -Parameter.

*cbresult*

Die Größe (in Bytes) des Puffers, der als *pvresult* übergeben wird.

*Infolevel*

Die Informationen, die in *pvresult* gespeichert werden. Die folgenden Optionen können für diesen Parameter verwendet werden.

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
<td><p>JET_IdxInfoCount</p></td>
<td><p><em>pvresult</em> wird als ULONG interpretiert. Bei Erfolg enthält der ULONG die Anzahl der Indizes für die angegebene Tabelle. <em>szindexname</em> wird ignoriert. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoIndexId</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>interpretiert. Bei Erfolg empfängt die <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> Strukturinformationen über den Index. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoLangid</p></td>
<td><p>JET_IdxInfoLangid ist veraltet. Verwenden Sie stattdessen JET_IdxInfoLCID und das <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">langidfromlcid</a> -Makro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoLCID</p></td>
<td><p><em>pvresult</em> wird als LCID interpretiert. Bei Erfolg enthält die LCID den Gebiets Schema Bezeichner des Indexes. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p>
<p><strong>Windows XP:  </strong> JET_IdxInfoLCID wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoList</p></td>
<td><p><em>pvresult</em> wird als <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Struktur interpretiert. Bei Erfolg empfängt die <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> Strukturinformationen über den Index. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoOLC</p></td>
<td><p>JET_IdxInfoOLC ist veraltet.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoResetOLC</p></td>
<td><p>JET_IdxInfoResetOLC ist veraltet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoSpaceAlloc</p></td>
<td><p><em>pvresult</em> wird als ULONG interpretiert. Bei Erfolg enthält der ULONG die Speicherplatz Verwendung des Indexes. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoSysTabCursor</p></td>
<td><p>JET_IdxInfoSysTabCursor ist veraltet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoVarSegMac</p></td>
<td><p><em>pvresult</em> wird als ushort interpretiert. Bei Erfolg enthält der ushort den Wert von <em>cbvarsegmac</em> , der beim Erstellen des Indexes verwendet wurde. Unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> finden Sie eine Beschreibung von <em>cbvarsegmac</em>. Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoKeyMost</p></td>
<td><p><em>pvresult</em> wird als ushort interpretiert. Bei Erfolg enthält der ushort den Wert von <em>cbkeymost</em> , der beim Erstellen des Indexes verwendet wurde. Eine Beschreibung von <em>cbkeymost</em>finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . Bei einem Fehler ist der Inhalt von <em>pvbuffer</em> nicht definiert.</p>
<p><strong>Windows Vista:  </strong> JET_IdxInfoKeyMost wird in Windows Vista eingeführt.</p></td>
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

**Jetgetindexinfo** und [jetgettableindexinfo](./jetgettableindexinfo-function.md) rufen identische Informationen zu einem Index ab. Der Unterschied besteht darin, wie die Tabelle angegeben wird. **Jetgetindexinfo** erwartet eine Datenbank (*DBID*) und den Namen einer Tabelle (*sztablename*), während [jetgettableindexinfo](./jetgettableindexinfo-function.md) einen Tabellen Bezeichner (*TableID*) erwartet.

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
<td><p>Implementiert als <strong>jetgetindexinfow</strong> (Unicode) und <strong>jetgetindexinfoa</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetgettableindexinfo](./jetgettableindexinfo-function.md)
