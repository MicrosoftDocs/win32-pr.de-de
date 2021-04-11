---
description: Weitere Informationen finden Sie in der jetstopbackupinstance-Funktion.
title: Jetstopbackupinstance-Funktion
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
ms.openlocfilehash: c1813658ed1fb569795bdfa65ccada3ef8ee629c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128632"
---
# <a name="jetstopbackupinstance-function"></a>Jetstopbackupinstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetstopbackupinstance-function"></a>Jetstopbackupinstance-Funktion

Die **jetstopbackupinstance** -Funktion verhindert, dass streamingsicherungsbezogene Aktivitäten auf einer bestimmten laufenden Instanz fortgesetzt werden, sodass die Streamingsicherung auf vorhersagbare Weise beendet wird.

**Windows XP:**  **jetstopbackupinstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parameter

*lichen*

Identifiziert die für den API-Befehl zu verwendende laufende Instanz.

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Der angegebene Instanzparameter weist einen ungültigen Wert auf (keine Instanz, die derzeit ausgeführt wird).</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, startet die Instanz, die angegeben wurde, alle neuen Streamingsicherungs-APIs.

Wenn diese Funktion fehlschlägt, werden keine Schritte zur Vorbereitung der Sicherung auf der-Instanz ausgeführt, und es wird keine Änderung am Instanzzustand vorgenommen.

#### <a name="remarks"></a>Bemerkungen

Die Sicherung wird in der Regel durch ein Ereignis außerhalb des Prozess Mechanismus ausgelöst. durch die Verwendung dieser API führt die ESENT-Anwendung selbst weitere Aufrufe an die Streamingsicherungs-APIs aus. Der Großteil der APIs für die Streaming-Sicherung beginnt mit dem JET_errBackupAbortByServer. Daher wird bei allen streamingsicherungsweiterungen (z. b. [jetreadfilanstance](./jetreadfileinstance-function.md)) ein Fehler zurückgegeben. Sicherungs Vorgänge, die Teil der Sicherungs Beendigung sind (z. b. [jetendexternalbackupinstance](./jetendexternalbackupinstance-function.md)), sind weiterhin zulässig.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
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

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetendexternalbackupinstance](./jetendexternalbackupinstance-function.md)  
[Jetreadfilinput Stance](./jetreadfileinstance-function.md)  
[Jetstopservice](./jetstopservice-function.md)
