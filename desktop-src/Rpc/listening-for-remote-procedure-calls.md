---
title: Lauschen auf Remote Prozedur Aufrufe
description: Nachdem ein Serverprogramm seine Bindungs Informationen registriert und seine Anwesenheit in einer Name Service-Datenbank angekündigt hat, kann es mit dem lauschen an den Endpunkt für Remote Prozedur Aufrufe beginnen.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d9463e0591279377502394541190be685cccd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036248"
---
# <a name="listening-for-remote-procedure-calls"></a><span data-ttu-id="20b3d-103">Lauschen auf Remote Prozedur Aufrufe</span><span class="sxs-lookup"><span data-stu-id="20b3d-103">Listening for Remote Procedure Calls</span></span>

<span data-ttu-id="20b3d-104">Nachdem ein Serverprogramm seine Bindungs Informationen registriert und seine Anwesenheit in einer Name Service-Datenbank angekündigt hat, kann es mit dem lauschen an den Endpunkt für Remote Prozedur Aufrufe beginnen.</span><span class="sxs-lookup"><span data-stu-id="20b3d-104">After a server program registers its binding information and advertises its presence in a name service database, it can begin listening to the endpoint for remote procedure calls.</span></span> <span data-ttu-id="20b3d-105">Server Programme aufrufen die Funktion [**rpcserverlauschen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) , um Endpunkte für Client Aufrufe von Remote Prozeduren zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="20b3d-105">Server programs call the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to monitor endpoints for client invocations of remote procedures.</span></span>

<span data-ttu-id="20b3d-106">Die DCE-Spezifikation von [**rpcserverlauschen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) gibt an, dass Sie nicht zurückgegeben werden sollte, bis eine Funktion im Serverprogramm [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)aufruft.</span><span class="sxs-lookup"><span data-stu-id="20b3d-106">The DCE specification of [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indicates that it should not return until a function in the server program calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening).</span></span> <span data-ttu-id="20b3d-107">Die Microsoft RPC-Implementierung von **rpcserverlauschen** verwendet zwei Parameter, die nicht in der DCE-Spezifikation vorkommen: *dontwait* und *minimumcallthreads*.</span><span class="sxs-lookup"><span data-stu-id="20b3d-107">The Microsoft RPC implementation of **RpcServerListen** uses two parameters that do not appear in the DCE specification: *DontWait* and *MinimumCallThreads*.</span></span> <span data-ttu-id="20b3d-108">Das Serverprogramm kann einen Wert ungleich 0 (null) für den *dontwait* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="20b3d-108">Your server program can pass a nonzero value for the *DontWait* parameter.</span></span> <span data-ttu-id="20b3d-109">Wenn dies der Fall ist, wird die **rpcserverlauschen** -Funktion sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="20b3d-109">If it does, the **RpcServerListen** function will return immediately.</span></span> <span data-ttu-id="20b3d-110">Verwenden Sie die [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) -Routine, um den warte Vorgang auszuführen, der normalerweise mit **rpcserverlauschen** verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="20b3d-110">Use the [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) routine to perform the wait operation usually associated with **RpcServerListen**.</span></span>

 

 




