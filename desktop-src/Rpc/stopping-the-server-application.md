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
# <a name="stopping-the-server-application"></a><span data-ttu-id="cda64-104">Beenden der Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="cda64-104">Stopping the Server Application</span></span>

<span data-ttu-id="cda64-105">Eine Serveranwendung kann die Überwachung von Clients beenden, indem Sie [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) und [**rpcserverunregisterif**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)aufrufen, oder indem Sie einfach den Host Prozess beenden.</span><span class="sxs-lookup"><span data-stu-id="cda64-105">A server application can stop listening for clients by calling [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif), or by simply exiting the host process.</span></span> <span data-ttu-id="cda64-106">Beide Methoden sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="cda64-106">Both methods are acceptable.</span></span> <span data-ttu-id="cda64-107">Wenn der Server den ersten Ansatz befolgt, sollte er die folgenden Schritte implementieren:</span><span class="sxs-lookup"><span data-stu-id="cda64-107">If the server follows the first approach, it should implement the following steps:</span></span>

<span data-ttu-id="cda64-108">Die Server Funktion [**rpcserverlistener**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) kehrt nicht zum aufrufenden Programm zurück, bis eine Ausnahme auftritt oder bis ein Aufruf von [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) auftritt.</span><span class="sxs-lookup"><span data-stu-id="cda64-108">The server function [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) does not return to the calling program until an exception occurs or until a call to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) occurs.</span></span> <span data-ttu-id="cda64-109">Standardmäßig darf der RPC-Server nur von einem anderen Server Thread mithilfe von **RpcMgmtStopServerListening** angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="cda64-109">By default, only another server thread is allowed to halt the RPC server by using **RpcMgmtStopServerListening**.</span></span> <span data-ttu-id="cda64-110">Clients, die versuchen, den Server anzuhalten, erhalten den Fehler RPC \_ S \_ Access \_ denied.</span><span class="sxs-lookup"><span data-stu-id="cda64-110">Clients who try to halt the server will receive the error RPC\_S\_ACCESS\_DENIED.</span></span> <span data-ttu-id="cda64-111">Es ist jedoch möglich, RPC so zu konfigurieren, dass einige oder alle Clients den Server verhindern können.</span><span class="sxs-lookup"><span data-stu-id="cda64-111">However, it is possible to configure RPC to allow some or all clients to stop the server.</span></span> <span data-ttu-id="cda64-112">Weitere Informationen finden Sie unter **RpcMgmtStopServerListening** .</span><span class="sxs-lookup"><span data-stu-id="cda64-112">See **RpcMgmtStopServerListening** for details.</span></span>

<span data-ttu-id="cda64-113">Sie können auch festlegen, dass die Client Anwendung einen Remote Prozedur Aufrufvorgang für eine Beendigungs Routine auf dem Server durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="cda64-113">You can also have the client application make a remote procedure call to a shutdown routine on the server.</span></span> <span data-ttu-id="cda64-114">Die Routine für das Herunterfahren ruft [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) und [**rpcserverunregisterif**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)auf.</span><span class="sxs-lookup"><span data-stu-id="cda64-114">The shutdown routine calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif).</span></span> <span data-ttu-id="cda64-115">Diese Vorgehensweise wird von dieser Beispielprogramm Anwendung verwendet, indem der Datei "hellop. c" eine neue Remote Funktion **herunter** gefahren wird.</span><span class="sxs-lookup"><span data-stu-id="cda64-115">This tutorial example program application uses this approach by adding a new remote function, **Shutdown**, to the file Hellop.c.</span></span>

<span data-ttu-id="cda64-116">In der **Shutdown** -Funktion gibt der einzelne NULL-Parameter für [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) an, dass die lokale Anwendung das Lauschen auf Remote Prozedur Aufrufe beenden soll.</span><span class="sxs-lookup"><span data-stu-id="cda64-116">In the **Shutdown** function, the single null parameter to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indicates that the local application should stop listening for remote procedure calls.</span></span> <span data-ttu-id="cda64-117">Die beiden NULL-Parameter für [**rpcserverunregisterif**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) sind Platzhalter, die angeben, dass die Registrierung für alle Schnittstellen aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="cda64-117">The two null parameters to [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) are wildcards, indicating that all interfaces should be unregistered.</span></span> <span data-ttu-id="cda64-118">Der **false** -Parameter gibt an, dass die Schnittstelle sofort aus der Registrierung entfernt werden soll, anstatt darauf zu warten, dass ausstehende Aufrufe abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="cda64-118">The **FALSE** parameter indicates that the interface should be removed from the registry immediately, rather than waiting for pending calls to complete.</span></span>


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



 

 




