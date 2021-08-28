---
description: Weitere Informationen finden Sie unter JetStopServiceInstance-Funktion.
title: JetStopServiceInstance-Funktion
TOCTitle: JetStopServiceInstance Function
ms:assetid: d8d3d047-91d6-4054-b3e1-44174666900e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294108(v=EXCHG.10)
ms:contentKeyID: 32765723
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopServiceInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55f9a8c6e91a70e447f03bc19bcd191d01ba0e08
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984303"
---
# <a name="jetstopserviceinstance-function"></a>JetStopServiceInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetstopserviceinstance-function"></a>JetStopServiceInstance-Funktion

Die **JetStopServiceInstance-Funktion** bereitet eine Instanz für die Beendigung vor.

**Windows XP:****JetStopServiceInstance** wird in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die ausgeführte Instanz, die für den API-Aufruf verwendet werden soll.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Der angegebene Instanzparameter hat einen ungültigen Wert (keine Instanz, die derzeit ausgeführt wird).</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in xp Windows eingeführt.</p> | 



Wenn diese Funktion erfolgreich ist, bereitet sie sich auf eine zukünftige Beendigung vor. Die Schritte zur Vorbereitung auf eine Beendigung umfassen Folgendes:

  - Beenden Sie die Onlinedefragmentierung, wenn sie ausgeführt wird.

  - Starten Sie eine Versionsspeicherbereinigung.

  - Verringern Sie die Prüfpunkttiefe, indem Sie mit dem Leeren von dirty pages im Puffer-Manager beginnen.

  - Verhindern sie zukünftige Aufrufe der meisten Funktionen für diese Instanz.

Wenn diese Funktion fehlschlägt, wird keiner der Schritte zur Vorbereitung auf eine Instanzbeendigung unternommen, sodass keine Änderung des Instanzzustands erfolgt.

#### <a name="remarks"></a>Bemerkungen

Diese Funktion reduziert die Arbeit, die die Instanz beim Beenden der Instanz zu tun hat, beendet die Instanz jedoch nicht. Daher ist diese Funktion nur eine Optimierung und nicht zwingend erforderlich. Beachten Sie, dass die Menge an Vorbereitungen im Jahr Windows 2000 und Windows XP geringer war. Sobald die Funktion erfolgreich ist, geben aufrufende Funktionen, die nicht mehr zulässig sind, JET_errClientRequestToStopJetService. Funktionen, die nach diesem Aufruf weiterhin zulässig sind, sind: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) und [JetResetSessionContext](./jetresetsessioncontext-function.md).

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



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
