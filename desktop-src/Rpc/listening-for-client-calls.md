---
title: Lauschen auf Client Anrufe
description: Nachdem die Serveranwendung ihre Schnittstellen registriert, die erforderlichen Bindungs Informationen erstellt und ihre Endpunkte registriert hat, ist Sie bereit, mit dem lauschen auf Remote Prozedur Aufrufe von Client Programmen zu beginnen.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Überwachen von Client aufrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f375a4620e301f59d168bf5f7a4dbeedc0fb89f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856743"
---
# <a name="listening-for-client-calls"></a><span data-ttu-id="f68c3-104">Lauschen auf Client Anrufe</span><span class="sxs-lookup"><span data-stu-id="f68c3-104">Listening for Client Calls</span></span>

<span data-ttu-id="f68c3-105">Nachdem die Serveranwendung ihre Schnittstellen registriert, die erforderlichen Bindungs Informationen erstellt und ihre Endpunkte registriert hat, ist Sie bereit, mit dem lauschen auf Remote Prozedur Aufrufe von Client Programmen zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="f68c3-105">After your server application has registered its interfaces, created the necessary binding information, and registered its endpoints, it is ready to begin listening for remote procedure calls from client programs.</span></span>

<span data-ttu-id="f68c3-106">Um Remote Prozedur Aufrufe zu lauschen, muss das Serverprogramm [**rpcserverlistener**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)aufrufen, wie im folgenden Code Fragment gezeigt:</span><span class="sxs-lookup"><span data-stu-id="f68c3-106">To listen for remote procedure calls, your server program must call [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



<span data-ttu-id="f68c3-107">Ein RPC-Server verfügt über einen oder mehrere Threads, die Client Aufrufe abrufen und an die Routinen in den registrierten Schnittstellen übermitteln.</span><span class="sxs-lookup"><span data-stu-id="f68c3-107">An RPC Server has one or more threads that pick up client calls and deliver them to the routines in the registered interfaces.</span></span> <span data-ttu-id="f68c3-108">Der erste Parameter für die [**rpcserverlauschen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) -Funktion ist die Mindestanzahl der zu erstellenden Threads.</span><span class="sxs-lookup"><span data-stu-id="f68c3-108">The first parameter to the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function is the minimum number of threads to create.</span></span> <span data-ttu-id="f68c3-109">Der-Parameter ist nur ein Hinweis. die RPC-Laufzeit kann diese ignorieren.</span><span class="sxs-lookup"><span data-stu-id="f68c3-109">The parameter is only a hint; the RPC run time may chose to ignore it.</span></span>

<span data-ttu-id="f68c3-110">Der zweite Parameter für [**rpcserverlauschen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) ist die maximale Anzahl von gleichzeitigen Remote Prozedur aufrufen, die verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f68c3-110">The second parameter to [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) is the maximum number of concurrent remote procedure calls to handle.</span></span> <span data-ttu-id="f68c3-111">Wenn Sie möchten, dass Ihre Anwendung den maximalen Standardwert verwendet, wird der Standardwert für "RPC-C-lauschen (max)" \_ \_ \_ \_ \_ als Wert für diesen Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="f68c3-111">If you want your application to use the default maximum value, pass RPC\_C\_LISTEN\_MAX\_CALLS\_DEFAULT as the value for this parameter.</span></span>

<span data-ttu-id="f68c3-112">Die DCE-Spezifikation erfordert, dass [**rpcserverlauschen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) weiterhin ausgeführt wird, bis ein Signal zum Abbrechen empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="f68c3-112">The DCE specification calls for [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) to keep running until it receives a signal to stop.</span></span> <span data-ttu-id="f68c3-113">Eine Microsoft-Erweiterung für diese Funktion besteht darin, Sie zu aktivieren, um die Überwachung zu starten und sofort zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="f68c3-113">One Microsoft extension to this function is to enable it to begin listening and return immediately.</span></span> <span data-ttu-id="f68c3-114">Wenn Sie möchten, dass Ihre Anwendung das standardmäßige DCE-Verhalten verwendet, legen Sie den dritten Parameter auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="f68c3-114">If you want your application to use the default DCE behavior, set the third parameter to zero.</span></span> <span data-ttu-id="f68c3-115">Weitere Informationen finden Sie unter [**rpcserverlistener**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)und [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) .</span><span class="sxs-lookup"><span data-stu-id="f68c3-115">See [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), and [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) for details.</span></span>

 

 




