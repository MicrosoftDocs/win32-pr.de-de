---
title: Fehlerbehandlung (RPC)
description: Beim synchronen RPC führt ein Client einen Remote Aufruf aus, der entweder mit einem Erfolgs-oder einem Fehlercode zurückgibt.
ms.assetid: 7dfc9f84-ce3c-49f3-8f72-b212095133fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017892b94438cc73f88cbfe60c03c088bf3ebcc9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104040012"
---
# <a name="error-handling-rpc"></a>Fehlerbehandlung (RPC)

Beim synchronen RPC führt ein Client einen Remote Aufruf aus, der entweder mit einem Erfolgs-oder einem Fehlercode zurückgibt. Asynchronous RPC bietet mehr Möglichkeiten für einen Aufruf von, und diese Fehler werden unterschiedlich behandelt, je nachdem, wo und wann Sie auftreten. In der folgenden Tabelle werden die Methoden beschrieben, mit denen ein-Befehl fehlschlagen kann und wie er verarbeitet wird.

## <a name="client-side-cleanup"></a>Client seitiges Cleanup



| Fehler Symptom                                                                                                                                  | Cleanup                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Der Client fängt eine Ausnahme ab, wenn er die Remote Prozedur aufruft.                                                                                  | Es sind keine RPC-API-Aufrufe erforderlich. Der gesamte RPC-Status wurde bereinigt.                                                              |
| Der Client empfängt eine Benachrichtigung zum Abschluss eines Aufrufs, aber wenn er [**rpcasynccompletecallaufruft**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall), empfängt er einen Fehlercode. | Es sind keine RPC-API-Aufrufe erforderlich. Der gesamte RPC-Status wurde bereinigt.                                                              |
| Der Client gibt einen nicht abgebrochenen oder Abbruch Abbruch aus.                                                                                                   | Der Client muss auf eine Benachrichtigung warten und beim Eintreffen der Benachrichtigung [**rpcasynccompletecallanrufen**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) . |



 

Bei der serverseitigen Bereinigung ist ein Schlüsselkonzept der Hand Punkt. Während der serverseitigen Verarbeitung eines asynchronen Aufrufes wird ein Teil der Verarbeitung in der Regel für den Thread durchgeführt, der den-Befehl empfangen hat (auch als Verteiler *Thread* bezeichnet). der Verteiler Thread fügt dann optional einen ausreichenden Zustand in einen Speicherblock ein und signalisiert einem anderen Thread (auch als Arbeits *Thread* bezeichnet), die Verarbeitung des Aufrufes fortzusetzen. Der Zeitpunkt, zu dem der Verteiler Thread erfolgreich signalisiert hat, dass der Arbeits Thread als *Übergabepunkt* bezeichnet wird.

## <a name="server-side-cleanup"></a>Server seitiges Cleanup



| Fehler aufgetreten      | Cleanup                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vor dem Übergabepunkt. | Ausnahme auslösen. Es ist kein Aufrufe von [**rpcasynccompletecallerforderlich**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Nach dem Übergabepunkt.  | Ruft [**rpcasyncabortcallor**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) auf, wenn der Fehler nicht schwerwiegend ist und die Ergebnisse weiterhin an den Client zurückgegeben werden können, [**RpcAsyncCompleteCall.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) Wenn der **RpcAsyncCompleteCall-Funktionsaufruf** fehlschlägt, gibt die RPC-Laufzeit die Parameter frei. Der Benutzer darf nicht auf diese Parameter zugreifen. Der Verteiler Thread darf keine wesentliche Verarbeitung ausführen, die nach dem Hand Punkt fehlschlagen kann, weil er den-Vorgang nicht mehr sicher abbrechen kann. Vor allem darf keine Ausnahme ausgelöst werden, da der Server möglicherweise abstürzt. |



 

## <a name="special-error-handling-cases-for-pipes"></a>Besondere Fehler Behandlungsfälle für Pipes

Bei der Verwendung von Pipes gibt es spezielle Fälle für die Fehlerbehandlung. In der folgenden Liste wird die Quelle des Fehlers erläutert und erläutert, wie der Fehler behandelt wird.



| Fehlerquelle                                                                                                 | Vorgehensweise                                                                                                |
|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client ruft Push auf, und der Aufruf schlägt fehl.                                                                             | Es sind keine RPC-API-Aufrufe erforderlich. Der gesamte RPC-Status wurde bereinigt.                                         |
| Der Client ruft [**rpcasynccompletecallauf**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) , bevor die [**in**](/windows/desktop/Midl/in) Pipes entladen werden. | Der-Rückruf schlägt mit dem entsprechenden Fehlercode für die Pipe-Füllung fehl.                                                   |
| Client ruft Pull auf, und der Aufruf schlägt fehl.                                                                             | Es sind keine RPC-API-Aufrufe erforderlich. Der gesamte RPC-Status wurde bereinigt.                                         |
| Entweder ruft der Client oder der Serverpush oder Pull in falscher Reihenfolge auf.                                                    | Die Laufzeit gibt den Fehlerstatus der Pipe-Füllung zurück.                                                                |
| Der Server ruft Push oder Pull auf, und der Aufruf schlägt fehl.                                                                     | Push gibt einen Fehlercode zurück. Es ist kein Aufrufe von [**rpcasynccompletecallerforderlich**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) . |
| Der Server ruft **rpcasynccompletecallauf** , bevor die Pipes entladen wurden.                                         | Der Pipe-Befehl gibt den Status der Pipe zum Auffüllen des Fehlers zurück.                                                         |
| Nach dem Dispatch schlägt ein Empfangsvorgang fehl.                                                                    | Wenn der Server das nächste Mal einen Pull-Vorgang zum Empfangen von Pipe-Daten aufruft, wird ein Fehler zurückgegeben.                            |



 

 

 
