---
title: Verfügbar machung des Servers im Netzwerk
description: Bevor eine Serveranwendung Remote Prozedur Aufrufe akzeptieren kann, muss Sie im Netzwerk verfügbar sein.
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Bereitstellen des Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2826e4e63e7e78e7f87f6afc120b80e885cd3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037170"
---
# <a name="making-the-server-available-on-the-network"></a><span data-ttu-id="06abe-104">Verfügbar machung des Servers im Netzwerk</span><span class="sxs-lookup"><span data-stu-id="06abe-104">Making the Server Available on the Network</span></span>

<span data-ttu-id="06abe-105">Bevor eine Serveranwendung Remote Prozedur Aufrufe akzeptieren kann, muss Sie im Netzwerk verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="06abe-105">Before a server application can accept remote procedure calls, it must be available on the network.</span></span> <span data-ttu-id="06abe-106">Zu diesem Zweck zeigt der Server der RPC-Laufzeit an, dass er bereit ist, Aufrufe für eine oder mehrere Protokoll Sequenzen zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="06abe-106">To do this, the server indicates to the RPC Run time that it is willing to accept calls on one or more protocol sequences.</span></span> <span data-ttu-id="06abe-107">Die Auswahl der Protokoll Sequenzen, die eine Serveranwendung unterstützt, ist eine wichtige Entscheidung. verschiedene Protokoll Sequenzen verfügen über sehr unterschiedliche Funktionen.</span><span class="sxs-lookup"><span data-stu-id="06abe-107">Choosing the protocol sequences a server application supports is an important decision; different protocol sequences have very different capabilities.</span></span> <span data-ttu-id="06abe-108">Server, die erwarten, dass Aufrufe lokal empfangen werden, sollten **Ncalrpc** verwenden.</span><span class="sxs-lookup"><span data-stu-id="06abe-108">Servers that expect calls to be received locally should use **ncalrpc**.</span></span> <span data-ttu-id="06abe-109">Server, die Remote Aufrufe akzeptieren, sollten **ncacn \_ IP \_ TCP** verwenden.</span><span class="sxs-lookup"><span data-stu-id="06abe-109">Servers that accept remote calls should use **ncacn\_ip\_tcp**.</span></span> <span data-ttu-id="06abe-110">Server sollten nicht überprüfen, ob die Protokoll Sequenz, für die Sie Aufrufe empfangen, die Protokoll Sequenz ist, für die Sie erwarten, dass Sie Aufrufe empfangen.</span><span class="sxs-lookup"><span data-stu-id="06abe-110">Servers should not verify that the protocol sequence on which they receive calls is the protocol sequence on which they expect to receive calls.</span></span> <span data-ttu-id="06abe-111">Weitere Informationen finden Sie unter warnen von anderen RPC-Endpunkten, die in demselben Prozess ausgeführt werden, bei den Best Practices für die RPC-Programmierung.</span><span class="sxs-lookup"><span data-stu-id="06abe-111">See Be Wary of Other RPC Endpoints Running in the Same Process in Best RPC Programming Practices for more information.</span></span>

<span data-ttu-id="06abe-112">Im folgenden Beispiel wird **ncacn \_ IP \_ TCP** verwendet.</span><span class="sxs-lookup"><span data-stu-id="06abe-112">The following example uses **ncacn\_ip\_tcp**.</span></span>

<span data-ttu-id="06abe-113">In den meisten Serverprogrammen werden alle im Netzwerk verfügbaren Protokoll Sequenzen verwendet.</span><span class="sxs-lookup"><span data-stu-id="06abe-113">Most server programs use all protocol sequences available on the network.</span></span> <span data-ttu-id="06abe-114">Dazu rufen Sie die [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) -Funktion auf, wie im folgenden Code Fragment gezeigt:</span><span class="sxs-lookup"><span data-stu-id="06abe-114">To do this, they invoke the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function, as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



<span data-ttu-id="06abe-115">Der erste Parameter für die [**rpcserveruseprotabq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) -Funktion ist die Protokoll Sequenz.</span><span class="sxs-lookup"><span data-stu-id="06abe-115">The first parameter to the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function is the protocol sequence.</span></span> <span data-ttu-id="06abe-116">Der zweite Parameter ist von der Protokoll Sequenz abhängig.</span><span class="sxs-lookup"><span data-stu-id="06abe-116">The second parameter is dependent on the protocol sequence.</span></span> <span data-ttu-id="06abe-117">Wie im Code Fragment dargestellt, legen die meisten Serverprogramme diesen Parameter auf **RPC \_ C \_ Protseq \_ Max \_ reqs \_ default** fest.</span><span class="sxs-lookup"><span data-stu-id="06abe-117">As illustrated in the code fragment, most server programs set this parameter to **RPC\_C\_PROTSEQ\_MAX\_REQS\_DEFAULT**.</span></span> <span data-ttu-id="06abe-118">Dieser Wert legt fest, dass die RPC-Bibliothek den Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="06abe-118">This value sets the RPC library to use the default value.</span></span> <span data-ttu-id="06abe-119">Der dritte Parameter ist eine Sicherheits Beschreibung und sollte nicht in Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06abe-119">The third parameter is a security descriptor and should not be used in applications.</span></span> <span data-ttu-id="06abe-120">Weitere Informationen finden Sie unter [**Sicherheit**](security.md).</span><span class="sxs-lookup"><span data-stu-id="06abe-120">For more information, see [**Security**](security.md).</span></span>

<span data-ttu-id="06abe-121">Sie können auch die Funktionen [**rpcserveruseallprotabqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**rpcserveruseprotsqex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**rpcserveruseprotsetqep**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)oder [**rpcserveruseprotabqepex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) verwenden.</span><span class="sxs-lookup"><span data-stu-id="06abe-121">You can also use the [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep), or [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) functions.</span></span>

<span data-ttu-id="06abe-122">Nachdem eine Serveranwendung mindestens eine Protokoll Sequenz ausgewählt hat, müssen Server, die dynamische Endpunkte verwenden, Bindungs Informationen für jede verwendete Protokoll Sequenz erstellen.</span><span class="sxs-lookup"><span data-stu-id="06abe-122">After a server application selects at least one protocol sequence, servers that use dynamic endpoints must create binding information for each protocol sequence it uses.</span></span> <span data-ttu-id="06abe-123">Der Server speichert die Bindungs Informationen in einem Bindungs Vektor, den er dann in den Endpunkt Mapper-Dienst exportieren kann.</span><span class="sxs-lookup"><span data-stu-id="06abe-123">The server stores the binding information in a binding vector that it can then export to the endpoint mapper service.</span></span>

<span data-ttu-id="06abe-124">Verwenden Sie die Funktion [**rpcserverinqbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) , um einen Bindungs Vektor für die Serveranwendung zu erhalten, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="06abe-124">Use the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function to obtain a binding vector for the server application, as shown in the following example:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



<span data-ttu-id="06abe-125">Der einzige Parameter, der an die [**rpcserverinqbinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) -Funktion übergeben wird, ist ein Zeiger auf einen Zeiger auf eine [**RPC- \_ Bindungs \_ Vektor**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) Struktur.</span><span class="sxs-lookup"><span data-stu-id="06abe-125">The only parameter passed to the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function is a pointer to a pointer to an [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) structure.</span></span> <span data-ttu-id="06abe-126">Die RPC-Lauf Zeit Bibliothek weist dynamisch ein Array von Bindungs Vektoren zu und speichert die Adresse des Arrays in der Parameter Variablen (in diesem Fall **rpcbindingvector**).</span><span class="sxs-lookup"><span data-stu-id="06abe-126">The RPC run-time library dynamically allocates an array of binding vectors and stores the address of the array in the parameter variable (in this case, **rpcBindingVector**).</span></span> <span data-ttu-id="06abe-127">Jede Serveranwendung ist dafür verantwortlich, diesen Bindungs Vektor mithilfe der [**rpcbindingvectorfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) -Funktion freizugeben, sobald Sie die Verwendung abgeschlossen hat (z. b. Nachdem Sie an die entsprechenden Funktionen übermittelt wurde).</span><span class="sxs-lookup"><span data-stu-id="06abe-127">Each server application is responsible for freeing this binding vector using the [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) function once it has finished using it (for example, after it has passed it to the appropriate functions).</span></span>

 

 




