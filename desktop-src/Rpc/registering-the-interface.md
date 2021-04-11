---
title: Registrieren der-Schnittstelle
description: Durch das Registrieren der Schnittstelle, die von einem Serverprogramm unterstützt wird, können Remote Prozedur Aufrufe von Client Programmen an die richtige Server Routine weitergeleitet werden.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Registrieren der Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a12de37b39c719de246ceb79a92d6a51fc361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206234"
---
# <a name="registering-the-interface"></a><span data-ttu-id="8fc65-104">Registrieren der-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8fc65-104">Registering the Interface</span></span>

<span data-ttu-id="8fc65-105">Durch das Registrieren der Schnittstelle, die von einem Serverprogramm unterstützt wird, können Remote Prozedur Aufrufe von Client Programmen an die richtige Server Routine weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="8fc65-105">Registering the interface that a server program supports enables remote procedure calls from client programs to be dispatched to the proper server routine.</span></span> <span data-ttu-id="8fc65-106">Server Programme aufrufen [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) , um ihre Schnittstellen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="8fc65-106">Server programs call [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to register their interfaces.</span></span> <span data-ttu-id="8fc65-107">Das folgende Code Fragment veranschaulicht seine Verwendung:</span><span class="sxs-lookup"><span data-stu-id="8fc65-107">The following code fragment demonstrates its use:</span></span>


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



<span data-ttu-id="8fc65-108">Der erste Parameter für die [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) -Funktion ist eine Struktur, die der mittlerer l-Compiler aus der IDL-Datei generiert, die die Schnittstelle (bzw. Schnittstellen) für den Server definiert.</span><span class="sxs-lookup"><span data-stu-id="8fc65-108">The first parameter to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is a structure the MIDL compiler generates from the IDL file that defines the interface (or interfaces) for the server.</span></span> <span data-ttu-id="8fc65-109">Der zweite und dritte Parameter sind eine UUID bzw. ein Einstiegspunkt Vektor.</span><span class="sxs-lookup"><span data-stu-id="8fc65-109">The second and third parameters are a UUID and an entry-point vector, respectively.</span></span> <span data-ttu-id="8fc65-110">Sie werden in diesem Beispiel auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8fc65-110">They are set to **NULL** in this example.</span></span> <span data-ttu-id="8fc65-111">In vielen Fällen werden diese Parameterwerte von Ihrem Serverprogramm auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8fc65-111">In many instances, your server program will set these parameter values to **NULL**.</span></span> <span data-ttu-id="8fc65-112">Server Programme verwenden den zweiten und dritten Parameter, wenn Sie mehrere Implementierungen derselben Prozeduren in einer Schnittstelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8fc65-112">Server programs use the second and third parameters when they provide multiple implementations of the same procedures in an interface.</span></span> <span data-ttu-id="8fc65-113">Weitere Informationen finden Sie unter [Einstiegspunkt Vektoren](registering-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="8fc65-113">For more information, see [Entry-Point Vectors](registering-interfaces.md).</span></span>

<span data-ttu-id="8fc65-114">Server Programme können auch [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) zum Registrieren einer Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fc65-114">Server programs can also use [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) to register an interface.</span></span> <span data-ttu-id="8fc65-115">Ein Vorteil der Verwendung dieser Funktion besteht darin, dass Sie Ihrer Anwendung die Möglichkeit bietet, eine Sicherheits Rückruffunktion festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8fc65-115">One advantage of using this function is that it provides your application with the ability to set a security-callback function.</span></span> <span data-ttu-id="8fc65-116">Die Verwendung von Sicherheits Rückruf Funktionen ist die empfohlene Vorgehensweise zum Sichern einer Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8fc65-116">Using security-callback functions is the recommended approach to securing an interface.</span></span>

> [!Note]  
> <span data-ttu-id="8fc65-117">Die Mittel l erzeugt zwei sehr ähnliche Strukturen, eine für den Client und eine für den Server.</span><span class="sxs-lookup"><span data-stu-id="8fc65-117">MIDL produces two very similar structures, one for the client and one for the server.</span></span> <span data-ttu-id="8fc65-118">Die an die Funktion [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) übermittelte Struktur ist die Server Version der von der Mitte erstellten Struktur.</span><span class="sxs-lookup"><span data-stu-id="8fc65-118">The structure passed to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is the server version of the MIDL-produced structure.</span></span>

 

 

 




