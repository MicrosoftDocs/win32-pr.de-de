---
description: 'Weitere Informationen zu: JetGetDatabaseInfo-Funktion'
title: JetGetDatabaseInfo-Funktion
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c92ed1d5d42511971c53e6116574cd8d9a882124
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982568"
---
# <a name="jetgetdatabaseinfo-function"></a>JetGetDatabaseInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetdatabaseinfo-function"></a>JetGetDatabaseInfo-Funktion

Die **JetGetDatabaseInfo-Funktion** ruft verschiedene Arten von Informationen zur Datenbank ab. Diese API kann aufgerufen werden, während eine Datenbank angefügt oder online ist (mit **JetGetDatabaseInfo)** oder während die Datenbank oder Datenbank-Engine offline ist (mit [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*Dbid*

Die [JET_DBID](./jet-dbid.md) für die Datenbank, aus der die Informationen abgerufen werden sollen.

*pvResult*

Zeiger auf einen Puffer, der die angegebenen Informationen empfängt. Die Größe des Puffers in Bytes wird in *cbMax* übergeben.

Bei einem Fehler sind die Inhalte von *pvResult* nicht definiert.

Die in *pvResult* gespeicherten Informationen hängen von *InfoLevel ab.*

*cbMax*

Die Größe des Puffers in Bytes, der in *pvResult* übergeben wurde.

*InfoLevel*

*InfoLevel* gibt an, welcher Informationstyp über die angegebene Datenbank abgerufen werden soll. Dies wirkt sich darauf aus, wie *pvResult* interpretiert wird. *InfoLevel* sind nur in der Offlineversion [(JetGetDatabaseFileInfo)](./jetgetdatabasefileinfo-function.md)oder online **(JetGetDatabaseInfo)** der API verfügbar.

Wenn der *bereitgestellte pvResult-Puffer* zu klein ist, werden je nach *InfoLevel* entweder JET_errInvalidBufferSize oder JET_errBufferTooSmall zurückgegeben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_DbInfoCollate</p> | <p>Noch nicht unterstützt und Gibt Standardwerte zurück. Darf nicht verwendet werden.</p> | 
| <p>JET_DbInfoConnect</p> | <p>Diese <em>InfoLevels</em> sind veraltet und werden derzeit nicht unterstützt. Darf nicht verwendet werden.</p> | 
| <p>JET_DbInfoCountry</p> | <p>Noch nicht unterstützt und Gibt Standardwerte zurück. Darf nicht verwendet werden.</p> | 
| <p>JET_DbInfoCp</p> | <p>Noch nicht unterstützt und Gibt Standardwerte zurück. Darf nicht verwendet werden.</p> | 
| <p>JET_DbInfoFilename</p> | <p><em>pvResult</em> wird als Zeichenfolgenpuffer (char *) interpretiert. Es wird ein MAX_PATH Puffer vorgeschlagen, jedoch nicht erforderlich. Wenn der Puffer nicht lang genug ist, werden JET_errBufferTooSmall zurückgegeben. Die Zeichenfolge wird mit dem Pfad der Datenbank für diese DBID aufgefüllt.</p> | 
| <p>JET_DbInfoFilesize</p> | <p><em>pvResult</em> wird als DWORD (4 Bytes) interpretiert. Gibt die Größe der Datenbank auf Seiten zurück.</p> | 
| <p>JET_DbInfoIsam</p> | <p>Diese <em>InfoLevels</em> sind veraltet und werden derzeit nicht unterstützt. Darf nicht verwendet werden.</p> | 
| <p>JET_DbInfoLCID</p> | <p>(Windows XP und höher) Dieses <em>InfoLevel</em> wurde ursprünglich als JET_DbInfoLangid (Windows 2000) angegeben.</p><p><em>pvResult</em> wird als long interpretiert. Dadurch wird der Gebietsschemabezeichner (LCID) zurückgegeben, der dieser Datenbank zugeordnet ist.</p> | 
| <p>JET_DbInfoMisc</p> | <p><em>pvResult</em> wird als <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>interpretiert. Die <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC-Struktur</a> wird mit Informationen zur angegebenen Datenbank aufgefüllt.</p> | 
| <p>JET_DbInfoOptions</p> | <p><em>pvResult</em> wird als <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD) interpretiert. Dadurch wird zurückgegeben, ob die Datenbank im exklusiven Modus geöffnet ist. Wenn sich die Datenbank im exklusiven Modus befindet, wird JET_bitDbExclusive in der <a href="gg294066(v=exchg.10).md">angegebenen JET_GRBIT</a> festgelegt, andernfalls wird 0 (null) festgelegt. Beachten Sie, dass andere <em>Grbitoptionen</em> für Die Datenbank für <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> und <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> nicht zurückgegeben werden.</p> | 
| <p>JET_DbInfoPageSize</p> | <p>Nur für Windows XP und höher verfügbar. <em>pvResult</em> wird als unsigned long interpretiert. Dadurch wird die Seitengröße der Datenbank in Bytes zurückgegeben.</p> | 
| <p>JET_DbInfoSpaceAvailable</p> | <p><em>pvResult</em> wird als DWORD interpretiert. Dadurch wird der verfügbare Speicherplatz für die Datenbank auf Seiten zurückgegeben.</p> | 
| <p>JET_DbInfoSpaceOwned</p> | <p><em>pvResult</em> wird als DWORD interpretiert. Dadurch wird der eigene Speicherplatz für die Datenbank auf Seiten zurückgegeben.</p> | 
| <p>JET_DbInfoTransactions</p> | <p><em>pvResult</em> wird als long interpretiert. Dadurch wird ein Wert zurückgegeben, der größer als die maximale Ebene ist, auf der Transaktionen geschachtelt werden können. Wenn <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> (geschachtelt, d. h. in derselben Sitzung, ohne Commit oder Rollback) so oft wie dieser Wert aufgerufen wird, wird beim letzten Aufruf JET_errTransTooDeep von <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>zurückgegeben. Beachten Sie, dass der Wert in Windows 2000, Windows XP und Windows Server 2003 7 ist.</p> | 
| <p>JET_DbInfoVersion</p> | <p><em>pvResult</em> wird als long interpretiert. Dadurch wird die native Hauptversion der Datenbank-Engine zurückgegeben. Dieser Wert wird für Windows 2000, Windows XP und Windows Server 2003 0x620.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Die Größe des in <em>cbMax</em> angegebenen Puffers war zu klein (oder nicht richtig), um die gewünschten Informationen zu speichern.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Das angeforderte <em>InfoLevel</em> wurde JET_DbInfoIsam. Dieser Vorgang wird nicht unterstützt.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Die Größe des in <em>cbMax</em> angegebenen Puffers war zu klein (oder nicht richtig), um die gewünschten Informationen zu speichern.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dieser Fehler wird von <strong>JetGetDatabaseInfo</strong> zurückgegeben, wenn die bereitgestellte <a href="gg269248(v=exchg.10).md">JET_DBID</a> keine gültige (angefügte) Datenbank ist. Dieser Fehler wird von <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> und <strong>JetGetDatabaseInfo</strong> zurückgegeben, wenn ein angeforderter <em>InfoLevel</em> von dieser Version der Funktion nicht unterstützt wird.</p> | 



Bei Erfolg werden die angeforderten Daten im Ausgabepuffer zurückgegeben.

Bei einem Fehler befindet sich der Ausgabepuffer in einem nicht definierten Zustand.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetGetDatabaseInfoW</strong> (Unicode) und <strong>JetGetDatabaseInfoA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
