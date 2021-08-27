---
description: Weitere Informationen finden Sie unter JetCreateInstance2-Funktion.
title: JetCreateInstance2-Funktion
TOCTitle: JetCreateInstance2 Function
ms:assetid: 1f894b19-fa15-4d89-a3d1-ee13b346f545
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269202(v=EXCHG.10)
ms:contentKeyID: 32765505
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstance2
- JetCreateInstance2W
- JetCreateInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc09639d48fe4cea93b115c9243587653ad70f44
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465047"
---
# <a name="jetcreateinstance2-function"></a>JetCreateInstance2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetcreateinstance2-function"></a>JetCreateInstance2-Funktion

Die **JetCreateInstance2-Funktion** wird verwendet, um eine neue Instanz der Datenbank-Engine für die Verwendung in einem einzelnen Prozess mit einem angegebenen Anzeigenamen zu zuordnen.

**Windows XP:****JetCreateInstance2** wird in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetCreateInstance2(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName,
      __in_opt      const tchar* szDisplayName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*Pinstance*

Der Ausgabepuffer, der die neu erstellte Instanz erhält.

*szInstanceName*

Gibt einen eindeutigen Zeichenfolgenbezeichner für die zu erstellende Instanz an. Diese Zeichenfolge muss innerhalb eines bestimmten Prozesses, der die Datenbank-Engine hosten, eindeutig sein.

**Hinweis:** Ein NULL-Wert wird als gültiger Zeichenfolgenbezeichner für eine -Instanz behandelt. Nur eine Instanz kann einen NULL-Zeichenfolgenbezeichner haben.

*szDisplayName*

Ein Anzeigename für die zu erstellende Instanz. Wenn dieser Parameter nicht vorhanden ist, wird davon ausgegangen, dass sein Wert NULL ist.

*grbit*

Für die zukünftige Verwendung reserviert. Wenn dieser Parameter nicht vorhanden ist, wird davon ausgegangen, dass sein Wert 0 (null) ist.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInstanceNameInUse</p> | <p>Der angegebene Instanzname wird für diesen Prozess bereits verwendet.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <a href="gg269354(v=exchg.10).md">JetCreateInstance passieren,</a> wenn <em>pinstance</em> NULL ist.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>Der Vorgang ist fehlgeschlagen, da er nicht verwendet werden kann, wenn die Datenbank-Engine im Einzelinstanzmodus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird.</p> | 
| <p>JET_errTooManyInstances</p> | <p>Eine neue Instanz konnte nicht erstellt werden, da die maximale Anzahl von Instanzen erreicht wurde. Die maximale Anzahl unterstützter Instanzen wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter mithilfe</a> <em>von</em>JET_paramMaxInstances.</p> | 



Bei Erfolg wird eine neue Instanz zugeordnet, und der Bezeichner dafür wird zurückgegeben. An diesem Punkt verfügen alle Systemparameter für die Instanz über die Werte der globalen Standardsystemparameter. Nachdem eine Instanz zugeordnet wurde, muss sie später beendet und/oder wieder aufgehoben werden.

Bei einem Fehler wird ein Fehler zurückgegeben, der die Fehlerursache darstellt, und es wird keine Instanz zugeordnet.

#### <a name="remarks"></a>Hinweise

Eine -Instanz muss mit einem Aufruf von [JetInit](./jetinit-function.md) initialisiert werden, bevor sie von etwas anderem als [JetSetSystemParameter verwendet werden kann.](./jetsetsystemparameter-function.md)

Eine -Instanz wird durch einen Aufruf der [JetTerm-Funktion](./jetterm-function.md) zerstört, auch wenn diese Instanz nie mit [JetInit initialisiert wurde.](./jetinit-function.md) Die maximale Anzahl von Instanzen, die zu einem beliebigen Zeitpunkt erstellt werden können, wird durch *JET_paramMaxInstances* gesteuert, das durch einen Aufruf von [JetSetSystemParameter konfiguriert werden kann.](./jetsetsystemparameter-function.md) Eine -Instanz ist die Einheit der Wiederherstellbarkeit für die Datenbank-Engine. Sie steuert den Lebenszyklus aller Dateien, die zum Schutz der Integrität der Daten in einer Gruppe von Datenbankdateien verwendet werden. Zu diesen Dateien gehören die Prüfpunktdatei und die Transaktionsprotokolldateien.

Wenn die Funktion erfolgreich ausgeführt wird, wird die Datenbank-Engine als Nebeneffekt dieses Aufrufs automatisch in den Modus mit mehreren Instanzen geändert. Wenn die Anwendung nur eine Instanz im Prozess zulassen möchte, sollte [JetInit](./jetinit-function.md) verwendet werden, um die Datenbank-Engine im Windows 2000-Kompatibilitätsmodus zu starten.

Falls vorhanden, wird der *szDisplayName-Parameter* verwendet, um die Instanz an Stellen wie dem Ereignisprotokoll oder für andere Aufrufer wie Sicherungsanwendungen (über Funktionen wie [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) oder [JetOSSnapshotFreeze) zu identifizieren.](./jetossnapshotfreeze-function.md) Wenn der Anzeigename nicht angegeben wird, wird stattdessen der eindeutige *szInstanceName-Parameter* verwendet, sofern vorhanden, andernfalls wird eine leere Zeichenfolge zurückgegeben. Wenn für die Engine der Ausführungsmodus nicht festgelegt wurde, wird sie nach diesem Aufruf auf den Modus mit mehreren Instanzen festgelegt.

Die typische Startsequenz für einen Prozess, der möglicherweise mehrere Jet-Instanzen ausführen kann, wäre:

  - Ein Aufruf von **JetCreateInstance2,** der die Instanz zuteilen und benennen wird.

  - Mehrere Aufrufe von [JetSetSystemParameter für](./jetsetsystemparameter-function.md) diese Instanz, um unterschiedliche Systemparameter festlegen zu können. Beachten Sie, dass einige Systemparameter für jede Instanz eindeutig sein müssen (z. B. *JET_paramSystemPath* oder *JET_paramLogFilePath),* sodass wahrscheinlich jeder dieser Parameter festgelegt werden muss.

  - Starten Sie die Instanz mit [JetInit](./jetinit-function.md) oder [JetInit2.](./jetinit2-function.md) Um eine Instanz zu beenden und/oder frei zu geben, verwenden Sie [JetTerm](./jetterm-function.md) oder [JetTerm2](./jetterm2-function.md).

Wenn dies die erste Instanz ist, die gestartet werden soll, gibt es eine Reihe zusätzlicher Schritte, die während dieses Aufrufs ausgeführt werden, um grundlegende Systemin initialisierung und Konfiguration auszuführen. Eine Reihe dieser Schritte kann zu bestimmten Fehlern führen, die mit JET_errOutOfMemory, aber auch anderen führen (weitere Informationen finden Sie unter Rückgabewerte).

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetCreateInstance2W</strong> (Unicode) und <strong>JetCreateInstance2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
