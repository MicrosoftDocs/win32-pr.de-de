---
description: 'Weitere Informationen zu: jetkreateinzustance-Funktion'
title: JetCreateInstance-Funktion
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366484"
---
# <a name="jetcreateinstance-function"></a>JetCreateInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreateinstance-function"></a>JetCreateInstance-Funktion

Die **jetkreateinstance** -Funktion weist eine neue Instanz der Datenbank-Engine für die Verwendung in einem einzelnen Prozess zu.

**Windows XP: jetkreateinstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a>Parameter

*pinstance*

Der Ausgabepuffer, der die neu erstellte-Instanz empfängt.

*szinstancename*

Ein eindeutiger Zeichen folgen Bezeichner für die zu erstellende-Instanz. Diese Zeichenfolge muss innerhalb eines bestimmten Prozesses, der die Datenbank-Engine gehostet, eindeutig sein.

**Hinweis** Ein NULL-Wert wird als gültiger Zeichen folgen Bezeichner für eine-Instanz behandelt. Es darf nur eine Instanz eine NULL-Zeichen folgen Kennung enthalten.

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
<td><p>JET_errInstanceNameInUse</p></td>
<td><p>Der angegebene Instanzname wird bereits für diesen Vorgang verwendet.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dies kann bei <strong>jetkreateinstance</strong> vorkommen, wenn <em>pinstance</em> <strong>null</strong>ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil er nicht verwendet werden kann, wenn die Datenbank-Engine im Einzel Instanz-Modus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances</p></td>
<td><p>Es konnte keine neue Instanz erstellt werden, da die maximale Anzahl von Instanzen erreicht wurde. Die maximale Anzahl unterstützter Instanzen wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mithilfe von <em>JET_paramMaxInstances</em>konfiguriert.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird eine neue Instanz zugewiesen, und der Bezeichner für die Instanz wird zurückgegeben. An diesem Punkt verfügen alle Systemparameter für die-Instanz über die Werte der globalen Standardsystem Parameter. Sobald eine Instanz zugewiesen wird, muss Sie beendet und/oder später freigegeben werden.

Bei einem Fehler wird ein Fehler zurückgegeben, der die Ursache des Fehlers darstellt, und es wird keine Instanz zugeordnet.

#### <a name="remarks"></a>Bemerkungen

Eine Instanz muss mit einem [calltinit](./jetinit-function.md) -Namen initialisiert werden, bevor Sie von einem anderen als [jetsetsystemparameter](./jetsetsystemparameter-function.md)verwendet werden kann.

Eine Instanz wird durch einen-Rückruf der [jetterm](./jetterm-function.md) -Funktion zerstört, auch wenn diese Instanz nicht mit [jetinit](./jetinit-function.md)initialisiert wurde. Die maximale Anzahl von Instanzen, die zu einem beliebigen Zeitpunkt erstellt werden können, wird durch [JET_paramMaxInstances](./resource-parameters.md)gesteuert, der durch einen Aufruf von [jetsetsystemparameter](./jetsetsystemparameter-function.md)konfiguriert werden kann. Eine Instanz ist die Wiederherstellbarkeits Einheit für die Datenbank-Engine. Er steuert den Lebenszyklus aller Dateien, mit denen die Integrität der Daten in einem Satz von Datenbankdateien geschützt wird. Diese Dateien enthalten die Prüf Punkt Datei und die Transaktionsprotokoll Dateien.

Wenn die Funktion erfolgreich ausgeführt wird, wird die Datenbank-Engine als Nebeneffekt dieses Aufrufes automatisch in den Modus für mehrere Instanzen geändert. Wenn die Anwendung nur eine Instanz im Prozess zulassen möchte, sollte [jetinit](./jetinit-function.md) verwendet werden, um die Datenbank-Engine im Windows 2000-Kompatibilitätsmodus zu starten.

Falls vorhanden, wird der *szDisplayName* verwendet, um die Instanz an Orten wie dem Ereignisprotokoll oder an anderen Aufrufern wie Sicherungs Anwendungen (über Funktionen wie [jetgetinstanceinfo](./jetgetinstanceinfo-function.md) oder [jetossnapshotfreeze](./jetossnapshotfreeze-function.md)) zu identifizieren. Wenn der Anzeige Name nicht angegeben wird, wird stattdessen der eindeutige *szinstancename* verwendet, sofern vorhanden. andernfalls wird eine leere Zeichenfolge zurückgegeben. Wenn für die Engine nicht der laufende Modus festgelegt wurde, wird Sie nach diesem-Befehl auf den Modus für mehrere Instanzen festgelegt.

Die typische Startsequenz für einen Prozess, bei dem möglicherweise mehrere Jet-Instanzen ausgeführt werden, wäre Folgendes:

  - Ein [JetCreateInstance2](./jetcreateinstance2-function.md) -Befehl, der die-Instanz zuweist und deren Namen bezeichnet.

  - Mehrere Aufrufe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) für diese Instanz, um unterschiedliche Systemparameter festzulegen. Beachten Sie, dass einige Systemparameter pro Instanz eindeutig sein müssen (wie z. b. [JET_paramSystemPath](./transaction-log-parameters.md) oder [JET_paramLogFilePath](./transaction-log-parameters.md)), sodass wahrscheinlich eine dieser Parameter festgelegt werden muss.

  - Starten Sie die Instanz mit [jetinit](./jetinit-function.md) oder [JetInit2](./jetinit2-function.md). Um eine Instanz zu beenden und/oder freizugeben, muss [jetterm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) verwendet werden.

Wenn dies die erste Instanz ist, die gestartet werden soll, gibt es eine Reihe zusätzlicher Schritte, die während dieses Aufrufes ausgeführt werden, um eine grundlegende Systeminitialisierung und Konfiguration zu ermöglichen. Einige dieser Schritte können zu bestimmten Fehlern führen, die mit JET_errOutOfMemory beginnen, aber auch andere (siehe Fehler oben).

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jetkreateingestancew</strong> (Unicode) und <strong>jetkreateingestancea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[Extensible Storage Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[Jetenablemultiinstance](./jetenablemultiinstance-function.md)  
[Jetgetinstanceingefo](./jetgetinstanceinfo-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[Jeto ssnapshotfreeze](./jetossnapshotfreeze-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[Jetterm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
