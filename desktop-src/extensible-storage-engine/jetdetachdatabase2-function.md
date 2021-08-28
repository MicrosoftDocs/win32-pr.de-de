---
description: Weitere Informationen finden Sie unter JetDetachDatabase2-Funktion.
title: JetDetachDatabase2-Funktion
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4f29253f3b320abb662f7a4334a14c1c49ed546
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984883"
---
# <a name="jetdetachdatabase2-function"></a>JetDetachDatabase2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdetachdatabase2-function"></a>JetDetachDatabase2-Funktion

Die **JetDetachDatabase2-Funktion** gibt eine Datenbankdatei frei, die zuvor an eine Datenbanksitzung angefügt wurde.

**Windows XP:****JetDetachDatabase2** wird in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*szFilename*

Der Name der zu trennenden Datenbank. Wenn *szFilename* **NULL oder** eine leere Zeichenfolge ist, werden alle datenbanken, die an *sesid* angefügt sind, getrennt.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen an geben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitForceCloseAndDetach</p> | <p>Erzwingt, dass die Datenbank geschlossen und getrennt wird. Wenn JET_bitForceCloseAndDetach nicht unterstützt wird, JET_errForceDetachNotAllowed zurückgegeben.</p> | 
| <p>JET_bitForceDetach</p> | <p>Erzwingt, dass die Datenbank getrennt wird. Wenn JET_bitForceDetach nicht unterstützt wird, JET_errForceDetachNotAllowed zurückgegeben.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Die Datenbank wird sichern und kann nicht getrennt werden.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Die Datenbank wurde von <a href="gg269299(v=exchg.10).md">JetOpenDatabase geöffnet.</a> Datenbanken müssen vor dem Trennen geschlossen werden.</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>Die Datenbank war zuvor nicht angefügt (siehe <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> oder <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</p> | 
| <p>JET_errForceDetachNotAllowed</p> | <p>JET_bitForceDetach wird nicht unterstützt.</p> | 
| <p>JET_errInTransaction</p> | <p>Es wurde versucht, eine Datenbank während einer Transaktion zu trennen.</p> | 



#### <a name="remarks"></a>Bemerkungen

Wenn eine angefügte Datenbank geöffnet wurde (mit [JetAttachDatabase](./jetattachdatabase-function.md)), muss sie vor dem Trennen mit [JetCloseDatabase](./jetclosedatabase-function.md) geschlossen werden.

Windows 2000: Datenbanken, die vor dem Aufrufen von [JetTerm](./jetterm-function.md) nicht getrennt wurden, werden automatisch erneut angefügt, wenn [JetInit](./jetinit-function.md) das nächste Mal aufgerufen wird.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetDetachDatabase2W</strong> (Unicode) und <strong>JetDetachDatabase2A</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetInit](./jetinit-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetTerm](./jetterm-function.md)
