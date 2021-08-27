---
description: 'Weitere Informationen zu: JetStopBackupInstance-Funktion'
title: JetStopBackupInstance-Funktion
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4dae676cfbbb0f2509a7d86fbb6507b8e2110f1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987243"
---
# <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance-Funktion

Die **JetStopBackupInstance-Funktion** verhindert, dass sicherungsbezogene Streamingaktivitäten auf einer bestimmten ausgeführten Instanz fortgesetzt werden, wodurch die Streamingsicherung auf vorhersagbare Weise beendet wird.

**Windows XP:****JetStopBackupInstance** wird in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Identifiziert die ausgeführte Instanz, die für den API-Aufruf verwendet werden soll.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Der angegebene Instanzparameter weist einen ungültigen Wert auf (keine Instanz, die derzeit ausgeführt wird).</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p> | 



Wenn diese Funktion erfolgreich ist, schlägt die angegebene Instanz alle neuen Streamingsicherungs-APIs fehl.

Wenn diese Funktion fehlschlägt, werden keine Schritte zur Vorbereitung auf die Sicherungsbeendigung auf der Instanz ausgeführt, und es erfolgt keine Änderung des Instanzzustands.

#### <a name="remarks"></a>Bemerkungen

Die Sicherung wird in der Regel durch ein Ereignis außerhalb des Prozessmechanismus ausgelöst, und mithilfe dieser API führt die ESENT-Anwendung selbst alle weiteren Aufrufe der Streamingsicherungs-APIs aus, um einen Fehler zu erzielen. Die meisten Streamingsicherungs-APIs treten mit JET_errBackupAbortByServer auf. Daher gibt jeder Fortschritt der Streamingsicherung (z. [B. JetReadFileInstance)](./jetreadfileinstance-function.md)einen Fehler zurück. Sicherungsvorgänge, die Teil der Sicherungsbeendigung sind (z. B. [JetEndExternalBackupInstance),](./jetendexternalbackupinstance-function.md)sind weiterhin zulässig.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
