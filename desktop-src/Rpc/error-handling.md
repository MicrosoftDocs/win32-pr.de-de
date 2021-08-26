---
title: Fehlerbehandlung (RPC)
description: In synchronem RPC wird von einem Client ein Remoteaufruf ausgeführt, der entweder mit einem Erfolgs- oder Fehlercode zurückgegeben wird.
ms.assetid: 7dfc9f84-ce3c-49f3-8f72-b212095133fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6daf29091602c36a23c0ed7e08eb0459985e13ca26ec128f401754f64c2329ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021659"
---
# <a name="error-handling-rpc"></a>Fehlerbehandlung (RPC)

In synchronem RPC wird von einem Client ein Remoteaufruf ausgeführt, der entweder mit einem Erfolgs- oder Fehlercode zurückgegeben wird. Asynchroner RPC bietet mehr Möglichkeiten für einen Fehleraufruf, und diese Fehler werden je nach Ort und Wann unterschiedlich behandelt. In der folgenden Tabelle werden die Möglichkeiten beschrieben, wie ein Aufruf fehlschlagen kann und wie er behandelt wird.

## <a name="client-side-cleanup"></a>Clientseitige Bereinigung



| Fehlersymptom                                                                                                                                  | Cleanup                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Der Client fängt eine Ausnahme ab, wenn er die Remoteprozedur aufruft.                                                                                  | Es sind keine RPC-API-Aufrufe erforderlich. Der rpc-Status wurde bereinigt.                                                              |
| Der Client empfängt eine Benachrichtigung zum Abschluss des Aufrufs, aber wenn er [**RpcAsyncCompleteCall aufruft,**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)erhält er einen Fehlercode. | Es sind keine RPC-API-Aufrufe erforderlich. Der rpc-Status wurde bereinigt.                                                              |
| Der Client gibt einen nicht abortiven oder abortiven Abbruch aus.                                                                                                   | Der Client muss auf eine Benachrichtigung warten und [**RpcAsyncCompleteCall aufrufen,**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) wenn die Benachrichtigung eintrifft. |



 

Bei der serverseitigen Bereinigung ist ein schlüsselorientiertes Konzept der Übergabepunkt. Während der serverseitigen Verarbeitung eines asynchronen Aufrufs wird in der Regel ein Teil der Verarbeitung für den Thread ausgeführt, der den Aufruf empfangen hat (auch als Verteilerthread bezeichnet). Optional legt der Verteilerthread genügend Zustand in einen Speicherblock ein und signalisiert einem anderen Thread (auch als Arbeitsthread bezeichnet), um die Verarbeitung für den Aufruf fortzufahren. Der Moment, an dem der Verteilerthread erfolgreich signalisiert, dass der Arbeitsthread als *Übergabepunkt bezeichnet wird.*

## <a name="server-side-cleanup"></a>Serverseitige Bereinigung



| Fehler aufgetreten      | Cleanup                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vor dem Übergabepunkt. | Ausnahme auslösen. Es ist kein [**Aufruf von RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) erforderlich.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Nach dem Übergabepunkt.  | Rufen [**Sie RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) auf, oder , wenn der Fehler nicht schwerwiegender ist und ergebnisse weiterhin an den Client zurückgegeben werden können, [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall). Wenn der **RpcAsyncCompleteCall-Funktionsaufruf** fehlschlägt, gibt die RPC-Laufzeit die Parameter frei. Der Benutzer darf nicht auf diese Parameter zugreifen. Der Verteilerthread darf keine wesentliche Verarbeitung durchführen, die nach dem Übergabepunkt fehlschlagen kann, da er den Aufruf nicht mehr sicher abbrechen kann. Insbesondere darf nach dem Übergabepunkt keine Ausnahme ausgelöst werden, da der Server möglicherweise abstürzt. |



 

## <a name="special-error-handling-cases-for-pipes"></a>Spezielle Fehlerbehandlungsfälle für Pipes

Es gibt Sonderfälle für die Fehlerbehandlung bei der Verwendung von Pipes. In der folgenden Liste werden die Fehlerquelle und die Fehlerbehandlung erläutert.



| Fehlerquelle                                                                                                 | Wie behandelt wird                                                                                                |
|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Der Client ruft push auf, und der Aufruf schlägt fehl.                                                                             | Es sind keine RPC-API-Aufrufe erforderlich. Der rpc-Status wurde bereinigt.                                         |
| Der Client ruft [**RpcAsyncCompleteCall auf,**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) bevor [**die in-Pipes**](/windows/desktop/Midl/in) entleert werden. | Der Aufruf schlägt mit dem entsprechenden Pipefüllfehlercode fehl.                                                   |
| Der Client ruft pull auf, und der Aufruf schlägt fehl.                                                                             | Es sind keine RPC-API-Aufrufe erforderlich. Der rpc-Status wurde bereinigt.                                         |
| Entweder der Client oder Der Server ruft Push oder Pull in der falschen Reihenfolge auf.                                                    | Die Laufzeit gibt den Fehlerstatus der Pipefüllung zurück.                                                                |
| Der Server ruft Push oder Pull auf, und der Aufruf schlägt fehl.                                                                     | Push gibt einen Fehlercode zurück. Es ist kein [**Aufruf von RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) erforderlich. |
| Der Server ruft **RpcAsyncCompleteCall auf,** bevor die Pipes entleert wurden.                                         | Der Pipeaufruf gibt einen Pipefüllfehlerstatus zurück.                                                         |
| Nach der Versendung schlägt ein Empfangsvorgang fehl.                                                                    | Wenn der Server das nächste Mal pull aufruft, um Pipedaten zu empfangen, wird ein Fehler zurückgegeben.                            |



 

 

 
