---
description: 'Weitere Informationen zu: JetGetVersion-Funktion'
title: JetGetVersion-Funktion
TOCTitle: JetGetVersion Function
ms:assetid: f25c3639-ae2b-4357-9947-563ef3df72c6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294133(v=EXCHG.10)
ms:contentKeyID: 32765747
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetVersion
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 480953ace945cc180ae481a6b253336a114c62ea
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984683"
---
# <a name="jetgetversion-function"></a>JetGetVersion-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetversion-function"></a>JetGetVersion-Funktion

Die **JetGetVersion-Funktion** ruft die Version der Datenbank-Engine ab.

```cpp
    JET_ERR JET_API JetGetVersion(
      __in          JET_SESID sesid,
      __out         unsigned long* pwVersion
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*pwVersion*

Ein Zeiger auf die Versionsnummer der Datenbank-Engine.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 



Wenn diese Funktion erfolgreich ausgeführt wird, wird die Version der Datenbank-Engine abgerufen.

Es gibt keine bekannten Fehlermodi.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Fehlerbehandlungsparameter](./error-handling-parameters.md)  
[Extensible Storage Engine Errors (Erweiterbare Storage-Engine-Fehler)](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)
