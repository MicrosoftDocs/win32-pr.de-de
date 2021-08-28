---
description: Weitere Informationen zur JetGetIndexInfo-Funktion
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
ms.openlocfilehash: e4d7c835d5077d2bfee87025b202480a888de981
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988583"
---
# <a name="jetgetindexinfo-function"></a>JetGetIndexInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetindexinfo-function"></a>JetGetIndexInfo-Funktion

Die **JetGetIndexInfo-Funktion** ruft Informationen zu einem Index ab.

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

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*Dbid*

Der Datenbankbezeichner, der für den API-Aufruf verwendet werden soll.

*szTableName*

Der Name der Tabelle, die den Index mit den abzurufenden Informationen enthält.

*szIndexName*

Der Name des Indexes mit den abzurufende Informationen.

*pvResult*

Zeiger auf einen Puffer, der die gewünschten Informationen empfängt. Der Puffer sollte so ausgerichtet sein, dass er den erforderlichen Typ aufnehmen kann. Der Typ des Puffers ist vom *InfoLevel-Parameter* abhängig.

*cbResult*

Die Größe des Puffers in Bytes, der als *pvResult* übergeben wird.

*InfoLevel*

Die Informationen, die in *pvResult* gespeichert werden. Für diesen Parameter können die folgenden Optionen verwendet werden.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_IdxInfo</p> | <p><em>pvResult</em> wird als <a href="gg269185(v=exchg.10).md">JET_INDEXLIST-Struktur</a> interpretiert. Bei Erfolg empfängt die <a href="gg269185(v=exchg.10).md">JET_INDEXLIST-Struktur</a> Informationen über den Index. Bei einem Fehler ist der Inhalt von <em>pvBuffer</em> nicht definiert.</p> | 
| <p>JET_IdxInfoCount</p> | <p><em>pvResult</em> wird als ULONG interpretiert. Bei Erfolg enthält ULONG die Anzahl der Indizes für die angegebene Tabelle. <em>szIndexName</em> wird ignoriert. Bei einem Fehler ist der Inhalt von <em>pvBuffer</em> nicht definiert.</p> | 
| <p>JET_IdxInfoIndexId</p> | <p><em>pvResult</em> wird als <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>interpretiert. Bei Erfolg empfängt die <a href="gg269327(v=exchg.10).md">JET_INDEXID-Struktur</a> Informationen über den Index. Bei einem Fehler ist der Inhalt von <em>pvBuffer</em> nicht definiert.</p> | 
| <p>JET_IdxInfoLangid</p> | <p>JET_IdxInfoLangid ist veraltet. Verwenden Sie stattdessen JET_IdxInfoLCID und das <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID-Makro.</a></p> | 
| <p>JET_IdxInfoLCID</p> | <p><em>pvResult</em> wird als LCID interpretiert. Bei Erfolg enthält die LCID den Gebietsschemabezeichner des Indexes. Bei einem Fehler ist der Inhalt von <em>pvBuffer</em> nicht definiert.</p><p><strong>Windows XP:</strong> JET_IdxInfoLCID wird in Windows XP eingeführt.</p> | 
| <p>JET_IdxInfoList</p> | <p><em>pvResult</em> wird als <a href="gg269185(v=exchg.10).md">JET_INDEXLIST-Struktur</a> interpretiert. Bei Erfolg empfängt die <a href="gg269185(v=exchg.10).md">JET_INDEXLIST-Struktur</a> Informationen über den Index. Bei einem Fehler ist der Inhalt von <em>pvBuffer</em> nicht definiert.</p> | 
| <p>JET_IdxInfoOLC</p> | <p>JET_IdxInfoOLC ist veraltet.</p> | 
| <p>JET_IdxInfoResetOLC</p> | <p>JET_IdxInfoResetOLC ist veraltet.</p> | 
| <p>JET_IdxInfoSpaceAlloc</p> | <p><em>pvResult</em> wird als ULONG interpretiert. Bei Erfolg enthält ULONG die Speicherplatznutzung des Indexes. Bei einem Fehler ist der Inhalt von <em>pvBuffer</em> nicht definiert.</p> | 
| <p>JET_IdxInfoSysTabCursor</p> | <p>JET_IdxInfoSysTabCursor ist veraltet.</p> | 
| <p>JET_IdxInfoVarSegMac</p> | <p><em>pvResult</em> wird als USHORT interpretiert. Bei Erfolg enthält USHORT den Wert <em>cbVarSegMac,</em> der beim Erstellen des Indexes verwendet wurde. Eine Beschreibung von <em>cbVarSegMac</em>finden Sie <a href="gg269186(v=exchg.10).md">unter JET_INDEXCREATE</a> . Bei einem Fehler ist der Inhalt von <em>pvBuffer</em> nicht definiert.</p> | 
| <p>JET_IdxInfoKeyMost</p> | <p><em>pvResult</em> wird als USHORT interpretiert. Bei Erfolg enthält USHORT den Wert <em>cbKeyMost,</em> der beim Erstellen des Indexes verwendet wurde. Eine Beschreibung von <em>cbKeyMost</em>finden Sie <a href="gg269186(v=exchg.10).md">unter JET_INDEXCREATE.</a> Bei einem Fehler ist der Inhalt von <em>pvBuffer</em> nicht definiert.</p><p><strong>Windows Vista:</strong> JET_IdxInfoKeyMost wird in Windows Vista eingeführt.</p> | 
| <p>JET_IdxInfoCreateIndex</p> | <p><em>pvResult</em> wird als <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE-Struktur</a> interpretiert. Bei einem Fehler ist der Inhalt von <em>pvBuffer</em> nicht definiert.</p><p><strong>Windows 7:</strong> JET_IdxInfoCreateIndex wird in Windows 7 eingeführt.</p> | 
| <p>JET_IdxInfoCreateIndex2</p> | <p><em>pvResult</em> wird als <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2-Struktur</a> interpretiert. Bei einem Fehler ist der Inhalt von <em>pvBuffer</em> nicht definiert.</p><p><strong>Windows 7:</strong> JET_IdxInfoCreateIndex2 wird in Windows 7 eingeführt.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errIndexNotFound</p> | <p>Der angegebene Index kann in der angegebenen Tabelle nicht gefunden werden.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>Der als <em>pvResult</em> übergebene Puffer war zu klein. Der Inhalt des Puffers ist nicht definiert.</p> | 



#### <a name="remarks"></a>Bemerkungen

**JetGetIndexInfo** und [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) rufen identische Informationen zu einem Index ab. Der Unterschied besteht darin, wie die Tabelle angegeben wird. **JetGetIndexInfo** erwartet eine Datenbank (*dbid*) und den Namen einer Tabelle (*szTableName*), während [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) einen Tabellenbezeichner (*tableid*) erwartet.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetGetIndexInfoW</strong> (Unicode) und <strong>JetGetIndexInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
