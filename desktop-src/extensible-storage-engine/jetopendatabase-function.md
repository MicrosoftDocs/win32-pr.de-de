---
description: 'Weitere Informationen zu: JetOpenDatabase-Funktion'
title: JetOpenDatabase-Funktion
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3fc7f484921dab0967ea991ac4060e5af7d78ec0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988494"
---
# <a name="jetopendatabase-function"></a>JetOpenDatabase-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopendatabase-function"></a>JetOpenDatabase-Funktion

Die **JetOpenDatabase-Funktion** öffnet eine zuvor angefügte Datenbank mithilfe der [JetAttachDatabase-](./jetattachdatabase-function.md) oder [JetAttachDatabase2-Funktionen](./jetattachdatabase2-function.md) für die Verwendung mit einer Datenbanksitzung. Diese Funktion kann für dieselbe Datenbank mehrmals aufgerufen werden.

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*szFilename*

Der Name der zu öffnende Datenbank.

*szConnect*

Reserviert. Auf NULL festgelegt.

*pdbid*

Zeiger auf einen Puffer, der bei einem erfolgreichen Aufruf den Bezeichner der Datenbank enthält. Wenn der Aufruf fehlschlägt, ist der Wert nicht definiert.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angeben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitDbExclusive</p> | <p>Ermöglicht nur einer einzelnen Sitzung das Anfügen einer Datenbank. Normalerweise können mehrere Sitzungen eine Datenbank öffnen.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Verhindert Änderungen an der Datenbank.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Exklusiver Zugriff wurde angefordert, konnte aber nicht gewährt werden.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>In <em>szFilename</em>wurde ein ungültiger Pfad angegeben. <em>szFilename</em> muss ungleich NULL sein und auf eine gültige Datei verweisen.</p> | 
| <p>JET_errDatabaseLocked</p> | <p>Eine andere Sitzung hat die Datenbank bereits exklusiv geöffnet (mit JET_bitDbExclusive).</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>Die Datenbank wurde zuvor nicht angefügt (siehe <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</p> | 
| <p>JET_errInvalidDatabase</p> | <p>Es wurde versucht, eine Datei zu öffnen, die keine gültige Datenbankdatei ist.</p> | 
| <p>JET_errOneDatabasePerSession</p> | <p>Es wurde versucht, mehrere Datenbanken zu öffnen, und <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> wurde festgelegt. Weitere Informationen finden Sie unter <a href="gg294139(v=exchg.10).md">Systemparameter.</a></p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>Die Datei wurde schreibgeschützt angefügt, <strong>aber JetOpenDatabase</strong> hat JET_bitDbReadOnly nicht bestanden. Die Datenbank wird weiterhin mit schreibgeschütztem Zugriff geöffnet.</p> | 



#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetOpenDatabaseW</strong> (Unicode) und <strong>JetOpenDatabaseA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
