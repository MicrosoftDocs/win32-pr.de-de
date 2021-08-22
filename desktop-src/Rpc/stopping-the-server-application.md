---
title: Beenden der Serveranwendung
description: Eine Serveranwendung kann das Lauschen auf Clients beenden, indem rpcMgmtStopServerListening und RpcServerUnregisterIf aufgerufen oder der Hostprozess einfach beendet wird.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- Remoteprozeduraufruf RPC , Tasks, Beenden der Serveranwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83f0a96732b1c862cf3e00d25cc2d2d9caf27ae5d764a9edab00c78aaf18682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925140"
---
# <a name="stopping-the-server-application"></a>Beenden der Serveranwendung

Eine Serveranwendung kann das Lauschen auf Clients beenden, indem [**rpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) und [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)aufgerufen oder der Hostprozess einfach beendet wird. Beide Methoden sind akzeptabel. Wenn der Server den ersten Ansatz verfolgt, sollte er die folgenden Schritte implementieren:

Die Serverfunktion [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) kehrt erst dann zum aufrufenden Programm zurück, wenn eine Ausnahme auftritt oder bis ein Aufruf von [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) erfolgt. Standardmäßig darf nur ein anderer Serverthread den RPC-Server mithilfe von **RpcMgmtStopServerListening** anhalten. Clients, die versuchen, den Server anzuhalten, erhalten den Fehler RPC \_ S \_ ACCESS \_ DENIED. Es ist jedoch möglich, RPC so zu konfigurieren, dass einige oder alle Clients den Server beenden können. Weitere Informationen finden Sie unter **RpcMgmtStopServerListening.**

Die Clientanwendung kann auch einen Remoteprozeduraufruf an eine Routine zum Herunterfahren auf dem Server durchführen. Die Routine zum Herunterfahren ruft [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) und [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)auf. In diesem Tutorial-Beispielprogramm wird dieser Ansatz verwendet, indem der Datei Hellop.c die neue Remotefunktion **Herunterfahren** hinzugefügt wird.

In der **Shutdown-Funktion** gibt der einzelne NULL-Parameter für [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) an, dass die lokale Anwendung das Lauschen auf Remoteprozeduraufrufe beenden soll. Die beiden NULL-Parameter für [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) sind Platzhalter, die angeben, dass die Registrierung aller Schnittstellen aufgehoben werden soll. Der **FALSE-Parameter** gibt an, dass die Schnittstelle sofort aus der Registrierung entfernt werden soll, anstatt auf den Abschluss ausstehender Aufrufe zu warten.


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



 

 




