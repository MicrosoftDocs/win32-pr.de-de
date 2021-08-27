---
description: Weitere Informationen finden Sie unter JetCreateInstance-Funktion.
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
ms.openlocfilehash: f22c411dd68b29b0cf305888f9dcce16add9a2dc
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985043"
---
# <a name="jetcreateinstance-function"></a>JetCreateInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreateinstance-function"></a>JetCreateInstance-Funktion

Die **JetCreateInstance-Funktion** ordnet eine neue Instanz der Datenbank-Engine für die Verwendung in einem einzelnen Prozess zu.

**Windows XP: JetCreateInstance** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a>Parameter

*Pinstance*

Der Ausgabepuffer, der die neu erstellte Instanz empfängt.

*szInstanceName*

Ein eindeutiger Zeichenfolgenbezeichner für die zu erstellende Instanz. Diese Zeichenfolge muss innerhalb eines bestimmten Prozesses, der die Datenbank-Engine hosten, eindeutig sein.

**Hinweis:** Ein NULL-Wert wird als gültiger Zeichenfolgenbezeichner für eine -Instanz behandelt. Nur eine Instanz kann einen NULL-Zeichenfolgenbezeichner haben.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInstanceNameInUse</p> | <p>Der angegebene Instanzname wird für diesen Prozess bereits verwendet.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <strong>JetCreateInstance passieren,</strong> wenn <em>pinstance</em> NULL <strong>ist.</strong></p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>Der Vorgang ist fehlgeschlagen, da er nicht verwendet werden kann, wenn die Datenbank-Engine im Einzelinstanzmodus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird.</p> | 
| <p>JET_errTooManyInstances</p> | <p>Eine neue Instanz konnte nicht erstellt werden, da die maximale Anzahl von Instanzen erreicht wurde. Die maximale Anzahl unterstützter Instanzen wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mithilfe</a> <em>von</em>JET_paramMaxInstances.</p> | 



Bei Erfolg wird eine neue Instanz zugeordnet, und der Bezeichner dafür wird zurückgegeben. An diesem Punkt verfügen alle Systemparameter für die Instanz über die Werte der globalen Standardsystemparameter. Nachdem eine Instanz zugeordnet wurde, muss sie später beendet und/oder wieder aufgehoben werden.

Bei einem Fehler wird ein Fehler zurückgegeben, der die Fehlerursache darstellt, und es wird keine Instanz zugeordnet.

#### <a name="remarks"></a>Bemerkungen

Eine -Instanz muss mit einem Aufruf von [JetInit](./jetinit-function.md) initialisiert werden, bevor sie von etwas anderem als [JetSetSystemParameter verwendet werden kann.](./jetsetsystemparameter-function.md)

Eine -Instanz wird durch einen Aufruf der [JetTerm-Funktion](./jetterm-function.md) zerstört, auch wenn diese Instanz nie mit [JetInit initialisiert wurde.](./jetinit-function.md) Die maximale Anzahl von Instanzen, die zu einem beliebigen Zeitpunkt erstellt werden können, wird durch [JET_paramMaxInstances](./resource-parameters.md)gesteuert, das durch einen Aufruf von [JetSetSystemParameter konfiguriert werden kann.](./jetsetsystemparameter-function.md) Eine -Instanz ist die Einheit der Wiederherstellbarkeit für die Datenbank-Engine. Sie steuert den Lebenszyklus aller Dateien, die zum Schutz der Integrität der Daten in einer Gruppe von Datenbankdateien verwendet werden. Zu diesen Dateien gehören die Prüfpunktdatei und die Transaktionsprotokolldateien.

Wenn die Funktion erfolgreich ausgeführt wird, wird die Datenbank-Engine als Nebeneffekt dieses Aufrufs automatisch in den Modus mit mehreren Instanzen geändert. Wenn die Anwendung nur eine Instanz im Prozess zulassen möchte, sollte [JetInit](./jetinit-function.md) verwendet werden, um die Datenbank-Engine im Windows 2000-Kompatibilitätsmodus zu starten.

Falls vorhanden, wird *szDisplayName* verwendet, um die Instanz an Stellen wie dem Ereignisprotokoll oder für andere Aufrufer wie Sicherungsanwendungen (über Funktionen wie [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) oder [JetOSSnapshotFreeze) zu identifizieren.](./jetossnapshotfreeze-function.md) Wenn der Anzeigename nicht angegeben wird, wird stattdessen der eindeutige *szInstanceName* verwendet, sofern vorhanden. Andernfalls wird eine leere Zeichenfolge zurückgegeben. Wenn für die Engine der Ausführungsmodus nicht festgelegt wurde, wird sie nach diesem Aufruf auf den Modus mit mehreren Instanzen festgelegt.

Die typische Startsequenz für einen Prozess, der möglicherweise mehrere Jet-Instanzen ausführen kann, wäre:

  - Ein Aufruf von [JetCreateInstance2,](./jetcreateinstance2-function.md) der die Instanz zuteilen und benennen wird.

  - Mehrere Aufrufe von [JetSetSystemParameter für](./jetsetsystemparameter-function.md) diese Instanz, um unterschiedliche Systemparameter festlegen zu können. Beachten Sie, dass einige Systemparameter pro Instanz eindeutig sein müssen (z. B. [JET_paramSystemPath](./transaction-log-parameters.md) oder [JET_paramLogFilePath),](./transaction-log-parameters.md)sodass sie höchstwahrscheinlich jeweils festgelegt werden müssen.

  - Starten Sie die Instanz mit [JetInit](./jetinit-function.md) oder [JetInit2.](./jetinit2-function.md) Um eine Instanz zu beenden und/oder frei zu geben, müssen [JetTerm](./jetterm-function.md)und [JetTerm2](./jetterm2-function.md) verwendet werden.

Wenn dies die erste Instanz ist, die gestartet werden soll, gibt es eine Reihe zusätzlicher Schritte, die während dieses Aufrufs ausgeführt werden, um grundlegende Systemin initialisierung und Konfiguration auszuführen. Eine Reihe dieser Schritte kann zu bestimmten Fehlern führen, die mit JET_errOutOfMemory, aber auch anderen (siehe Fehler oben).

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetCreateInstanceW</strong> (Unicode) und <strong>JetCreateInstanceA</strong> (ANSI) implementiert.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage-Engine-Dateien](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
