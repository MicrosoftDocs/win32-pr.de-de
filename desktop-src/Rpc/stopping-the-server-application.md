---
title: Beenden der Server Anwendung
description: Eine Serveranwendung kann die Überwachung von Clients beenden, indem Sie RpcMgmtStopServerListening und rpcserverunregisterif aufrufen, oder indem Sie einfach den Host Prozess beenden.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Beenden der Serveranwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f95ba05588e0575949614e05370f86de78207d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713680"
---
# <a name="stopping-the-server-application"></a>Beenden der Server Anwendung

Eine Serveranwendung kann die Überwachung von Clients beenden, indem Sie [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) und [**rpcserverunregisterif**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)aufrufen, oder indem Sie einfach den Host Prozess beenden. Beide Methoden sind zulässig. Wenn der Server den ersten Ansatz befolgt, sollte er die folgenden Schritte implementieren:

Die Server Funktion [**rpcserverlistener**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) kehrt nicht zum aufrufenden Programm zurück, bis eine Ausnahme auftritt oder bis ein Aufruf von [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) auftritt. Standardmäßig darf der RPC-Server nur von einem anderen Server Thread mithilfe von **RpcMgmtStopServerListening** angehalten werden. Clients, die versuchen, den Server anzuhalten, erhalten den Fehler RPC \_ S \_ Access \_ denied. Es ist jedoch möglich, RPC so zu konfigurieren, dass einige oder alle Clients den Server verhindern können. Weitere Informationen finden Sie unter **RpcMgmtStopServerListening** .

Sie können auch festlegen, dass die Client Anwendung einen Remote Prozedur Aufrufvorgang für eine Beendigungs Routine auf dem Server durchführen soll. Die Routine für das Herunterfahren ruft [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) und [**rpcserverunregisterif**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)auf. Diese Vorgehensweise wird von dieser Beispielprogramm Anwendung verwendet, indem der Datei "hellop. c" eine neue Remote Funktion **herunter** gefahren wird.

In der **Shutdown** -Funktion gibt der einzelne NULL-Parameter für [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) an, dass die lokale Anwendung das Lauschen auf Remote Prozedur Aufrufe beenden soll. Die beiden NULL-Parameter für [**rpcserverunregisterif**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) sind Platzhalter, die angeben, dass die Registrierung für alle Schnittstellen aufgehoben werden soll. Der **false** -Parameter gibt an, dass die Schnittstelle sofort aus der Registrierung entfernt werden soll, anstatt darauf zu warten, dass ausstehende Aufrufe abgeschlossen werden.


```C++
/* add this function to hellop.c */
void Shutdown(void)
{
    RPC_STATUS status;
 
    status = RpcMgmtStopServerListening(NULL);
 
    if (status) 
    {
       exit(status);
    }
 
    status = RpcServerUnregisterIf(NULL, NULL, FALSE);
 
    if (status) 
    {
       exit(status);
    }
} //end Shutdown
```



 

 




