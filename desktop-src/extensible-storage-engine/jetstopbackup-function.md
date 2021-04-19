---
description: Weitere Informationen finden Sie in der jetstopbackup-Funktion.
title: Jetstopbackup-Funktion
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
ms.openlocfilehash: c47a1454e5846fae510a7b91c197d4b180fd14a7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106369348"
---
# <a name="jetstopbackup-function"></a>Jetstopbackup-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetstopbackup-function"></a>Jetstopbackup-Funktion

Die **jetstopbackup** -Funktion verhindert, dass alle streamingsicherungsbezogenen Aktivitäten auf einer bestimmten laufenden Instanz fortgesetzt werden, sodass die Streamingsicherung auf vorhersagbare Weise beendet wird.

**Windows XP:**  Diese Funktion wird in Windows XP eingeführt.

[Jetstopservice](./jetstopservice-function.md) ist der Legacy-Befehl, wenn nur eine Instanz zulässig ist. In diesem Fall ist die einzige aktive Instanz die, die für die Beendigung vorbereitet wird.

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Es ist nicht klar, welche Instanz für die Beendigung vorbereitet werden soll, wenn <a href="gg269240(v=exchg.10).md">jetstopservice</a> im Modus für mehrere Instanzen verwendet wird.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, startet die Instanz alle neuen Streamingsicherungs-APIs.

Wenn diese Funktion fehlschlägt, werden keine Schritte zur Vorbereitung der Sicherung auf der-Instanz ausgeführt, und es wird keine Änderung am Instanzzustand vorgenommen.

#### <a name="remarks"></a>Bemerkungen

Die Sicherung wird in der Regel durch ein Ereignis außerhalb des Prozess Mechanismus ausgelöst. durch die Verwendung dieser API führt die ESENT-Anwendung selbst weitere Aufrufe an die Streamingsicherungs-APIs aus. Der Großteil der APIs für die Streaming-Sicherung beginnt mit dem JET_errBackupAbortByServer. Daher wird bei jedem Fortschritt der Streamingsicherung (z.b. [jetreadfilanstance](./jetreadfileinstance-function.md)) ein Fehler zurückgegeben. Sicherungs Vorgänge, die Teil der Sicherungs Beendigung sind (z. b. [jetendexternalbackupinstance](./jetendexternalbackupinstance-function.md)), sind weiterhin zulässig.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Jetendexternalbackupinstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetreadfilinput Stance](./jetreadfileinstance-function.md)  
[Jetstopservice](./jetstopservice-function.md)
