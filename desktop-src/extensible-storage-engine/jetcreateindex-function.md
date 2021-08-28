---
description: Weitere Informationen finden Sie unter JetCreateIndex-Funktion.
title: JetCreateIndex-Funktion
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 698f9a050415568c06c8e10819cfed12a4a17181
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478396"
---
# <a name="jetcreateindex-function"></a>JetCreateIndex-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreateindex-function"></a>JetCreateIndex-Funktion

Mit **der JetCreateIndex-Funktion** können Sie einen Datenindex in einer Ese-Datenbank (Extensible Storage Engine) erstellen, mit der Sie bestimmte Daten schnell finden können.

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für einen bestimmten API-Aufruf verwendet werden soll.

*tableid*

Die Tabelle, für die ein Index erstellt wird.

*szIndexName*

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des zu erstellenden Indexes angibt.

Der Indexname muss den folgenden Richtlinien entsprechen:

  - Sie muss weniger Zeichen enthalten als JET_cbNameMost, ohne das beendende NULL-Zeichen.

  - Sie darf nur Zeichen aus den folgenden Kategorien enthalten: 0 bis 9, A bis Z, a bis z und alle Interpunktionszeichen außer " \! " " (Ausrufezeichen), "," (Komma), " " (öffnende Klammer) und " " ( schließende Klammer) – das heißt, die ASCII-Zeichen 0x20, 0x22 bis 0x2d, 0x2f bis 0x5a, 0x5c und 0x5d \[ \] bis 0x7f.

  - Er darf nicht mit einem Leerzeichen beginnen.

  - Sie muss mindestens ein Zeichen enthalten, das kein Leerzeichen ist.

*grbit*

Eine Gruppe von Bits, die die Optionen enthält, die für einen bestimmten Aufruf verwendet werden sollen. Dieser Parameter kann null oder mehr der Optionen enthalten, die in der struktur [JET_INDEXCREATE](./jet-indexcreate-structure.md) sind.

*szKey*

Ein Zeiger auf eine double-NULL-terminierte Zeichenfolge von Token mit NULL-Trennzeichen.

Weitere Informationen zu diesem Parameter finden Sie in [der](./jet-indexcreate-structure.md) JET_INDEXCREATE Struktur.

*cbKey*

Die Länge des *szKey-Parameters* in Bytes, einschließlich der beiden endenden NULL-Zeichen.

*lDensity*

Die Prozentuale Dichte der anfänglichen B+-Indexstruktur.

Weitere Informationen zu diesem Parameter finden Sie in [der](./jet-indexcreate-structure.md) JET_INDEXCREATE Struktur.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der in der folgenden Tabelle aufgeführten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Bedeutung</p> | 
|--------------------|----------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 



Eine Liste der zusätzlichen Fehler, die von der **JetCreateIndex-Funktion** zurückgegeben werden können, finden Sie unter [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="remarks"></a>Hinweise

Das Aufrufen der **JetCreateIndex-Funktion** ist identisch mit dem Aufrufen der [JetCreateIndex2-Funktion](./jetcreateindex2-function.md) mit einer [JET_INDEXCREATE-Struktur,](./jet-indexcreate-structure.md) die die gleichen Einstellungen wie die Parameter von **JetCreateIndex** und einem *cIndexCreate-Parameter* gleich 1 enthält. Für die Felder [](./jet-indexcreate-structure.md) der JET_INDEXCREATE-Struktur, die keine entsprechenden Parameter in **JetCreateIndex** haben, wird der Wert 0 angenommen.

Beachten **Sie, dass JetCreateIndex** durch [JetCreateIndex2 ersetzt wurde.](./jetcreateindex2-function.md)

#### <a name="requirements"></a>Anforderungen


| | | <p>Client</p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p>Server</p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p>Header</p> | <p>Wird in Esent.h deklariert.</p> | | <p>Bibliothek</p> | <p>Verwendet ESENT.lib.</p> | | <p>DLL</p> | <p>Erfordert ESENT.dll.</p> | | <p>Unicode</p> | <p>Wird als <strong>JetCreateIndexW</strong> (Unicode) und <strong>JetCreateIndexA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
