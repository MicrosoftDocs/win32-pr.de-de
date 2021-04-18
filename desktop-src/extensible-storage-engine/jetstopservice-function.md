---
description: Weitere Informationen finden Sie in der jetstopservice-Funktion
title: JetStopService-Funktion
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e66b4e5242710c89ca7e7964ecd0a72774b719d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368118"
---
# <a name="jetstopservice-function"></a>JetStopService-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetstopservice-function"></a>JetStopService-Funktion

Die **jetstopservice** -Funktion bereitet eine Instanz für die Beendigung vor.

**Jetstopservice** ist der Legacy-Befehl, wenn nur eine Instanz zulässig ist. In diesem Fall ist die einzige aktive Instanz die, die für die Beendigung vorbereitet wird.

```cpp
    JET_ERR JET_API JetStopService(void);
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
<td><p>Es ist nicht klar, welche Instanz für die Beendigung vorbereitet werden soll, wenn <strong>jetstopservice</strong> im Modus für mehrere Instanzen verwendet wird.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
</tbody>
</table>


Wenn diese Funktion erfolgreich ausgeführt wird, wird eine zukünftige Beendigung vorbereitet. Die Schritte zur Vorbereitung auf eine Beendigung umfassen Folgendes:

  - Stoppt die Online Defragmentierung, wenn Sie ausgeführt wird.

  - Starten Sie eine Bereinigung des Versionsspeicher.

  - Verringern Sie die Prüf Punkt Tiefe, indem Sie mit dem leeren von geänderten Seiten im Puffer-Manager beginnen.

  - Vermeiden Sie zukünftige Aufrufe der meisten Funktionen für diese Instanz.

Wenn diese Funktion fehlschlägt, wird keiner der Schritte zur Vorbereitung auf das Beenden einer Instanz durchgeführt, sodass keine Änderung am Instanzstatus erfolgt.

#### <a name="remarks"></a>Bemerkungen

Diese Funktion reduziert den Arbeitsaufwand, den die-Instanz ausführen muss, wenn Sie beendet wird, beendet jedoch nicht die-Instanz. Daher ist diese Funktion nur eine Optimierung und ist nicht für die Verwendung von obligatorisch. Beachten Sie, dass der Aufwand für die Vorbereitung in Windows 2000 und Windows XP geringer war. Wenn die Funktion erfolgreich ausgeführt wird, wird das Aufrufen von Funktionen, die nicht mehr zulässig sind, JET_errClientRequestToStopJetService zurückgeben. Funktionen, die nach diesem Aufrufvorgang weiterhin zulässig sind: [jetrollback](./jetrollback-function.md), [jetclosetable](./jetclosetable-function.md), [jetendsession](./jetendsession-function.md), [jetclosedatabase](./jetclosedatabase-function.md), [jetdetachdatabase](./jetdetachdatabase-function.md) und [jetressitzungscontext](./jetresetsessioncontext-function.md).

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

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetclosedatabase](./jetclosedatabase-function.md)  
[Jetclosetable](./jetclosetable-function.md)  
[Jetdetachdatabase](./jetdetachdatabase-function.md)  
[Jetendsession](./jetendsession-function.md)  
[Jetresessioncontext](./jetresetsessioncontext-function.md)  
[Jetrollback](./jetrollback-function.md)  
[Jetterm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
