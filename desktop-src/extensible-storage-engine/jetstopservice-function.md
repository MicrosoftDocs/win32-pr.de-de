---
description: Weitere Informationen finden Sie unter JetStopService-Funktion.
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
ms.openlocfilehash: 75e8622d79f2757bee8ab3041250b2ba78499194
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480306"
---
# <a name="jetstopservice-function"></a>JetStopService-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetstopservice-function"></a>JetStopService-Funktion

Die **JetStopService-Funktion** bereitet eine Instanz für die Beendigung vor.

**JetStopService ist** der Legacyaufruf, wenn nur eine Instanz zulässig ist. In diesem Fall ist die einzige aktive Instanz die Instanz, die für die Beendigung vorbereitet wird.

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Es ist nicht klar, welche Instanz für die Beendigung vorbereitet werden soll, wenn <strong>JetStopService mit</strong> dem Modus für mehrere Instanzen verwendet wird.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in xp Windows eingeführt.</p> | 



Wenn diese Funktion erfolgreich ist, bereitet sie sich auf eine zukünftige Beendigung vor. Die Schritte zur Vorbereitung auf eine Beendigung umfassen Folgendes:

  - Beenden Sie die Onlinedefragmentierung, wenn sie ausgeführt wird.

  - Starten Sie eine Versionsspeicherbereinigung.

  - Verringern Sie die Prüfpunkttiefe, indem Sie mit dem Leeren von dirty pages im Puffer-Manager beginnen.

  - Verhindern sie zukünftige Aufrufe der meisten Funktionen für diese Instanz.

Wenn diese Funktion fehlschlägt, wird keiner der Schritte zur Vorbereitung auf eine Instanzbeendigung unternommen, sodass keine Änderung des Instanzzustands erfolgt.

#### <a name="remarks"></a>Hinweise

Diese Funktion reduziert die Arbeit, die die Instanz beim Beenden tun muss, beendet die Instanz jedoch nicht. Daher ist diese Funktion nur eine Optimierung und nicht zwingend erforderlich. Beachten Sie, dass der Umfang der vorbereitungsbereiten Arbeit im Jahr Windows 2000 und Windows XP geringer war. Sobald die Funktion erfolgreich ist, geben aufrufende Funktionen, die nicht mehr zulässig sind, JET_errClientRequestToStopJetService. Funktionen, die nach diesem Aufruf weiterhin zulässig sind, sind: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) und [JetResetSessionContext](./jetresetsessioncontext-function.md).

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
