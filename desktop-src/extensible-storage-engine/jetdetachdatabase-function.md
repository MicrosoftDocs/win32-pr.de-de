---
description: Weitere Informationen finden Sie unter JetDetachDatabase-Funktion.
title: JetDetachDatabase-Funktion
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 028e156cffd5eef0d4baa1f043dddf5105fd1023
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985873"
---
# <a name="jetdetachdatabase-function"></a>JetDetachDatabase-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdetachdatabase-function"></a>JetDetachDatabase-Funktion

Die **JetDetachDatabase-Funktion** gibt eine Datenbankdatei frei, die zuvor an eine Datenbanksitzung angefügt wurde.

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*szFilename*

Der Name der zu trennenden Datenbank. Wenn *szFilename* **NULL oder** eine leere Zeichenfolge ist, werden alle datenbanken, die an *sesid* angefügt sind, getrennt.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Die Datenbank wird sichern und kann nicht getrennt werden.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Die Datenbank wurde von <a href="gg269299(v=exchg.10).md">JetOpenDatabase geöffnet.</a> Datenbanken müssen vor dem Trennen geschlossen werden.</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>Die Datenbank war zuvor nicht angefügt (siehe <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> oder <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</p> | 
| <p>JET_errInTransaction</p> | <p>Es wurde versucht, eine Datenbank während einer Transaktion zu trennen.</p> | 



#### <a name="remarks"></a>Bemerkungen

Wenn eine angefügte Datenbank geöffnet wurde (mit [JetAttachDatabase](./jetattachdatabase-function.md)), muss sie vor dem Trennen mit [JetCloseDatabase](./jetclosedatabase-function.md) geschlossen werden.

Windows nur 2000: Datenbanken, die vor dem Aufrufen von [JetTerm](./jetterm-function.md) nicht getrennt wurden, werden automatisch erneut angefügt, wenn [JetInit](./jetinit-function.md) das nächste Mal aufgerufen wird.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetDetachDatabaseW</strong> (Unicode) und <strong>JetDetachDatabaseA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetTerm](./jetterm-function.md)
