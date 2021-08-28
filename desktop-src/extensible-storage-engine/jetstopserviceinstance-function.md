---
description: 'Weitere Informationen zu: JetStopServiceInstance-Funktion'
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
ms.openlocfilehash: 74604ed5fb01e92638c0b139f5d29b95b551faef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482746"
---
# <a name="jetstopserviceinstance-function"></a>JetStopServiceInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetstopserviceinstance-function"></a>JetStopServiceInstance-Funktion

Die **JetStopServiceInstance-Funktion** bereitet eine Instanz für die Beendigung vor.

**Windows XP:****JetStopServiceInstance** wurde in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die für den API-Aufruf zu verwendende ausgeführte Instanz.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Der angegebene Instanzparameter weist einen ungültigen Wert auf (keine Instanz, die derzeit ausgeführt wird).</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p> | 



Wenn diese Funktion erfolgreich ist, bereitet sie sich auf eine zukünftige Beendigung vor. Folgende Schritte werden zur Vorbereitung auf eine Beendigung ausgeführt:

  - Beenden Sie die Onlinedefragmentierung, wenn sie ausgeführt wird.

  - Starten Sie eine Versionsspeicherbereinigung.

  - Reduzieren Sie die Prüfpunkttiefe, indem Sie mit dem Leeren geänderter Seiten im Puffer-Manager beginnen.

  - Verhindern Sie zukünftige Aufrufe der meisten Funktionen für diese Instanz.

Wenn diese Funktion fehlschlägt, wird keiner der Schritte zur Vorbereitung auf eine Instanzbeendigung ausgeführt, sodass keine Änderung am Instanzzustand erfolgt.

#### <a name="remarks"></a>Hinweise

Diese Funktion reduziert die Arbeit, die die Instanz erledigen muss, wenn sie beendet wird, beendet die Instanz jedoch nicht. Daher ist diese Funktion nur eine Optimierung und nicht zwingend erforderlich. Beachten Sie, dass die Menge an Vorbereitungsaufwand in Windows 2000 und Windows XP geringer war. Sobald die Funktion erfolgreich ausgeführt wurde, geben aufrufende Funktionen, die nicht mehr zulässig sind, JET_errClientRequestToStopJetService zurück. Funktionen, die nach diesem Aufruf weiterhin zulässig sind: [JetRollback,](./jetrollback-function.md) [JetCloseTable,](./jetclosetable-function.md) [JetEndSession,](./jetendsession-function.md) [JetCloseDatabase,](./jetclosedatabase-function.md) [JetDetachDatabase](./jetdetachdatabase-function.md) und [JetResetSessionContext](./jetresetsessioncontext-function.md).

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



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
