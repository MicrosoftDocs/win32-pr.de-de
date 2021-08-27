---
description: 'Weitere Informationen zu: JetStopBackup-Funktion'
title: JetStopBackup-Funktion
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd5f7fe7096b0562aa9fc4ce8d15f77a4ccf205f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469697"
---
# <a name="jetstopbackup-function"></a>JetStopBackup-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetstopbackup-function"></a>JetStopBackup-Funktion

Die **JetStopBackup-Funktion** verhindert, dass streamingsicherungsbezogene Aktivitäten auf einer bestimmten ausgeführten Instanz fortgesetzt werden, wodurch die Streamingsicherung auf vorhersagbare Weise beendet wird.

**Windows XP:**  Diese Funktion wird in Windows XP eingeführt.

[JetStopService](./jetstopservice-function.md) ist der Legacyaufruf, wenn nur eine Instanz zulässig ist. In diesem Fall ist die einzige aktive Instanz die Instanz, die für die Beendigung vorbereitet wird.

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Es ist nicht klar, welche Instanz für die Beendigung vorbereitet werden soll, wenn <a href="gg269240(v=exchg.10).md">JetStopService</a> im Modus für mehrere Instanzen verwendet wird.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p> | 



Wenn diese Funktion erfolgreich ausgeführt wird, schlägt die Instanz alle neuen Streamingsicherungs-APIs fehl.

Wenn diese Funktion fehlschlägt, werden keine Schritte zum Vorbereiten der Sicherungsbeendigung auf der Instanz ausgeführt, und es erfolgt keine Änderung des Instanzzustands.

#### <a name="remarks"></a>Hinweise

Die Sicherung wird in der Regel durch ein Ereignis außerhalb des Prozessmechanismus ausgelöst, und mithilfe dieser API führt die ESENT-Anwendung selbst alle weiteren Aufrufe der Streamingsicherungs-APIs aus, um einen Fehler zu erzielen. Bei den meisten Streamingsicherungs-APIs tritt ein Fehler mit JET_errBackupAbortByServer auf. Daher gibt jeder Fortschritt der Streamingsicherung [(z. B. JetReadFileInstance)](./jetreadfileinstance-function.md)einen Fehler zurück. Sicherungsvorgänge, die Teil der Sicherungsbeendigung sind (z. B. [JetEndExternalBackupInstance),](./jetendexternalbackupinstance-function.md)sind weiterhin zulässig.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
