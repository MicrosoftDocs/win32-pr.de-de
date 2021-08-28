---
description: Weitere Informationen finden Sie unter JetStopBackup-Funktion.
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
ms.openlocfilehash: cd11857be7096ce30f2fcf06f8ab4f975185da57
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982363"
---
# <a name="jetstopbackup-function"></a>JetStopBackup-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetstopbackup-function"></a>JetStopBackup-Funktion

Die **JetStopBackup-Funktion** verhindert, dass aktivitäten im Zusammenhang mit Streamingsicherungen auf einer bestimmten ausgeführten Instanz fortgesetzt werden, wodurch die Streamingsicherung auf vorhersagbare Weise beendet wird.

**Windows XP:**  Diese Funktion wird in xp Windows eingeführt.

[JetStopService ist](./jetstopservice-function.md) der Legacyaufruf, wenn nur eine Instanz zulässig ist. In diesem Fall ist die einzige aktive Instanz die Instanz, die für die Beendigung vorbereitet wird.

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Es ist nicht klar, welche Instanz für die Beendigung vorbereitet werden soll, wenn <a href="gg269240(v=exchg.10).md">JetStopService mit</a> dem Modus für mehrere Instanzen verwendet wird.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in xp Windows eingeführt.</p> | 



Wenn diese Funktion erfolgreich ist, tritt bei der Instanz ein Fehler bei allen neuen Streamingsicherungs-APIs auf.

Wenn diese Funktion fehlschlägt, werden keine Schritte zum Vorbereiten der Sicherungsbeendigung auf der Instanz und keine Änderung des Instanzzustands unternommen.

#### <a name="remarks"></a>Bemerkungen

Die Sicherung wird in der Regel durch ein Ereignis außerhalb des Prozessmechanismus ausgelöst, und mit dieser API ruft die ESENT-Anwendung selbst alle weiteren Aufrufe der Streamingsicherungs-APIs auf, um einen Fehler zu erhalten. Der Großteil der Streamingsicherungs-APIs wird mit einem Fehler JET_errBackupAbortByServer. Daher wird bei jedem Streamingsicherungsfortschritt (z. B. [JetReadFileInstance)](./jetreadfileinstance-function.md)ein Fehler zurückgegeben. Sicherungsvorgänge, die Teil der Sicherungsbeendigung sind (z. B. [JetEndExternalBackupInstance),](./jetendexternalbackupinstance-function.md)sind weiterhin zulässig.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
