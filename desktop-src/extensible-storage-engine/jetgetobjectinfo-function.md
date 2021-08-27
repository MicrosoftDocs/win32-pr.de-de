---
description: Weitere Informationen finden Sie unter JetGetObjectInfo-Funktion.
title: JetGetObjectInfo-Funktion
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e6317280c5e794e9809c15f47f01d55ffd48eeb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982423"
---
# <a name="jetgetobjectinfo-function"></a>JetGetObjectInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetobjectinfo-function"></a>JetGetObjectInfo-Funktion

Die **JetGetObjectInfo-Funktion** ruft Informationen zu Datenbankobjekten ab. Derzeit werden nur Tabellen unterstützt. [JetGetTableInfo](./jetgettableinfo-function.md) kann verwendet werden, um mehr Informationen als **JetGetObjectInfo zu erhalten.**

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der zu verwendende Datenbanksitzungskontext.

*Dbid*

Die Datenbank, aus der die Informationen abgerufen werden.

*objtyp*

Die Objekte, die abzurufende Informationen enthalten. Derzeit werden nur JET_objtypNil und JET_objtypTable unterstützt, die sich beide identisch verhalten. Es werden nur Tabellen abgerufen.

*szContainerName*

Dieser Parameter ist für die zukünftige Verwendung reserviert und übergibt **NULL.** Der Name der Objekttypen, über die Informationen abgerufen werden.

*szObjectName*

Der Name des Objekts, das abzurufende Informationen enthält. Wenn *InfoLevel* die optionen JET_ObjInfoList oder JET_ObjInfoListNoStats verwendet, um eine Liste aller Objekte abzurufen, sollte dieser Wert **NULL** oder eine leere Zeichenfolge sein.

Derzeit werden nur Tabellennamen unterstützt.

*pvResult*

Zeiger auf einen Puffer, der die angegebenen Informationen empfängt.

Die Größe des Puffers in Bytes wird in *cbMax übergeben.* Bei einem Fehler ist der Inhalt *von pvResult* nicht definiert.

Die in *pvResult* gespeicherten Informationen hängen von *InfoLevel ab.*

*cbMax*

Die Größe des in pvResult übergebenen Puffers in *Bytes.*

*InfoLevel*

Gibt an, welche Art von Informationen für das angegebene Objekt abgerufen werden soll. Dies wirkt sich darauf *aus, wie pvResult* interpretiert wird.

Die folgenden Optionen können für diesen Parameter festgelegt werden.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_ObjInfo</p> | <p><em>pvResult</em> wird als <a href="gg269353(v=exchg.10).md">eine</a> JET_OBJECTINFO interpretiert.</p><p>Die <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO-Struktur</a> wird mit Informationen zu dem Objekt aufgefüllt, das in <em>szObjectName benannt ist.</em></p><p>Wenn der Aufrufer die Anzahl der Datensätze und Seiten für das Objekt nicht kennen möchte, sollten Sie die JET_ObjInfoNoStats verwenden. Dies kann schneller sein, da Statistiken nicht enthalten sind.</p> | 
| <p>JET_ObjInfoList</p> | <p><em>pvResult</em> wird als <a href="gg269348(v=exchg.10).md">eine</a> JET_OBJECTLIST interpretiert. Informationen zu allen Objekten werden abgerufen. Eine temporäre Tabelle wird erstellt, und die Informationen, die zum Durchlaufen der temporären Tabelle erforderlich sind, werden in der JET_OBJECTLIST <a href="gg269348(v=exchg.10).md">beschrieben.</a> Weitere Informationen finden Sie unter <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. Wenn der Aufrufer die Anzahl der Datensätze und Seiten für das Objekt nicht kennen möchte, sollten Sie die Verwendung von JET_ObjInfoListNoStats verwenden, was möglicherweise schneller ist.</p> | 
| <p>JET_ObjInfoListACM</p> | <p>Veraltet und derzeit nicht unterstützt.</p> | 
| <p>JET_ObjInfoListNoStats</p> | <p><em>pvResult</em> wird als <a href="gg269348(v=exchg.10).md">eine</a> JET_OBJECTLIST interpretiert. Informationen zu allen Objekten werden abgerufen. Eine temporäre Tabelle wird erstellt, und die Informationen, die zum Durchlaufen der temporären Tabelle erforderlich sind, werden in der JET_OBJECTLIST <a href="gg269348(v=exchg.10).md">beschrieben.</a> Weitere Informationen finden Sie unter <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. JET_ObjInfoListNoStats ist mit JET_ObjInfoList identisch, außer dass die Spalten, die die Anzahl der Datensätze (<em>columnidcRecord</em>) und Seiten (<em>columnidcPage</em>) melden, nicht aktualisiert werden.</p> | 
| <p>JET_ObjInfoMax</p> | <p><em>pvResult</em> wird als <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO.</a> Die maximale Größe des Objekts ist in Seiten. Derzeit werden nur Tabellen zurückgegeben.</p> | 
| <p>JET_ObjInfoNoStats</p> | <p><em>pvResult</em> wird als <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO.</a> Es werden nur Informationen zu dem in <em>szObjectName</em> angegebenen Objekt abgerufen.</p><p>Die <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO-Struktur</a> wird mit Informationen zu dem Objekt aufgefüllt, das in <em>szObjectName benannt ist.</em></p><p>JET_ObjInfoNoStats ist mit JET_ObjInfo identisch, mit der Ausnahme, dass die Felder, die die Anzahl von Datensätzen und Seiten melden, auf 0 (null) festgelegt sind.</p> | 
| <p>JET_ObjInfoRulesLoaded</p> | <p>Veraltet und derzeit nicht unterstützt.</p> | 
| <p>JET_ObjInfoSysTabCursor</p> | <p>Veraltet und derzeit nicht unterstützt.</p> | 
| <p>JET_ObjInfoSysTabReadOnly</p> | <p>Veraltet und derzeit nicht unterstützt.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Die Größe des Puffers, der in <em>cbMax angegeben</em> wurde, war zu klein, um die gewünschten Informationen zu enthalten.</p> | 
| <p>JET_errInvalidName</p> | <p>In <em>szObjectName</em> oder szContainerName wurde ein <em>ungültiger Name angegeben.</em></p> | 
| <p>JET_errInvalidParameter</p> | <p>Ein fehlerhafter Parameter wurde angegeben. Es ist möglich, dass eine fehlerhafte Ebene an <em>InfoLevel übergeben wurde.</em></p> | 



#### <a name="remarks"></a>Bemerkungen

Wenn **JetGetObjectInfo** erfolgreich eine temporäre Tabelle erstellt (z. B. JET_ObjInfoList oder JET_ObjInfoNoStats), ist der Aufrufer dafür verantwortlich, die temporäre Tabelle mit [JetCloseTable zu schließen.](./jetclosetable-function.md)

**JetGetObjectInfo unterstützt** derzeit nur das Abrufen von Informationen zu Tabellen.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetGetObjectInfoW</strong> (Unicode) und <strong>JetGetObjectInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
