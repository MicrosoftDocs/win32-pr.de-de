---
description: Weitere Informationen finden Sie unter JetCloseDatabase-Funktion.
title: JetCloseDatabase-Funktion
TOCTitle: JetCloseDatabase Function
ms:assetid: e17a05dd-c30b-4e8f-8538-91a65e8052d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294123(v=EXCHG.10)
ms:contentKeyID: 32765737
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef8bbc98d4cee68ecb8c5fab1ba62ea9be290e87
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466647"
---
# <a name="jetclosedatabase-function"></a>JetCloseDatabase-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetclosedatabase-function"></a>JetCloseDatabase-Funktion

Die **JetCloseDatabase-Funktion** schließt eine Datenbankdatei, die zuvor mit [JetOpenDatabase geöffnet wurde.](./jetopendatabase-function.md)

```cpp
    JET_ERR JET_API JetCloseDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet wird.

*Dbid*

Die zu schließende Datenbank.

*grbit*

Für die zukünftige Verwendung reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errDatabaseNotFound</p> | <p>Die Datenbank wurde zuvor nicht geöffnet.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>Der <em>dbid-Parameter</em> war kein gültiger Datenbankbezeichner.</p> | 
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 



#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)
