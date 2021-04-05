---
title: COM-Clients und-Server
description: Ein wichtiger Aspekt von com ist die Interaktion von Clients und Servern.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7c3e29e4a4a3e2fcefe1c3473350d3423a8c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710968"
---
# <a name="com-clients-and-servers"></a><span data-ttu-id="a8ac2-103">COM-Clients und-Server</span><span class="sxs-lookup"><span data-stu-id="a8ac2-103">COM Clients and Servers</span></span>

<span data-ttu-id="a8ac2-104">Ein wichtiger Aspekt von com ist die Interaktion von Clients und Servern.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-104">A critical aspect of COM is how clients and servers interact.</span></span> <span data-ttu-id="a8ac2-105">Bei einem *com-Client* handelt es sich um einen beliebigen Code oder ein Objekt, das einen Zeiger auf einen com-Server erhält</span><span class="sxs-lookup"><span data-stu-id="a8ac2-105">A *COM client* is whatever code or object gets a pointer to a COM server and uses its services by calling the methods of its interfaces.</span></span> <span data-ttu-id="a8ac2-106">Ein *com-Server* ist ein beliebiges Objekt, das Dienste für Clients bereitstellt. Diese Dienste sind in Form von COM-Schnittstellen Implementierungen, die von jedem Client aufgerufen werden können, der einen Zeiger auf eine der Schnittstellen des Server Objekts erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-106">A *COM server* is any object that provides services to clients; these services are in the form of COM interface implementations that can be called by any client that is able to get a pointer to one of the interfaces on the server object.</span></span>

<span data-ttu-id="a8ac2-107">Es gibt zwei Haupttypen von Servern: *in-Process* und *out-of-Process*.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-107">There are two main types of servers, *in-process* and *out-of-process*.</span></span> <span data-ttu-id="a8ac2-108">Prozess interne Server werden in einer dynamischen verknüpften Bibliothek (dll) implementiert, und prozessübergreifende Server werden in einer ausführbaren Datei (exe) implementiert.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-108">In-process servers are implemented in a dynamic linked library (DLL), and out-of-process servers are implemented in an executable file (EXE).</span></span> <span data-ttu-id="a8ac2-109">Out-of-Process-Server können sich entweder auf dem lokalen Computer oder auf einem Remote Computer befinden.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-109">Out-of-process servers can reside either on the local computer or on a remote computer.</span></span> <span data-ttu-id="a8ac2-110">Außerdem bietet com einen Mechanismus, mit dem ein Prozess interner Server (eine DLL) in einem Ersatz-exe-Prozess ausgeführt werden kann, um den Vorteil zu erhalten, dass der Prozess auf einem Remote Computer ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-110">In addition, COM provides a mechanism that allows an in-process server (a DLL) to run in a surrogate EXE process to gain the advantage of being able to run the process on a remote computer.</span></span> <span data-ttu-id="a8ac2-111">Weitere Informationen finden Sie unter [dll-Surrogates](dll-surrogates.md).</span><span class="sxs-lookup"><span data-stu-id="a8ac2-111">For more information, see [DLL Surrogates](dll-surrogates.md).</span></span>

<span data-ttu-id="a8ac2-112">Das COM-Programmiermodell und die Konstrukte wurden nun erweitert, sodass COM-Clients und-Server über das Netzwerk hinweg zusammenarbeiten können, nicht nur innerhalb eines bestimmten Computers.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-112">The COM programming model and constructs have now been extended so that COM clients and servers can work together across the network, not just within a given computer.</span></span> <span data-ttu-id="a8ac2-113">Dadurch können vorhandene Anwendungen mit neuen Anwendungen und untereinander in Netzwerken mit ordnungsgemäßer Verwaltung interagieren, und neue Anwendungen können so geschrieben werden, dass Sie die Netzwerk Features nutzen können.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-113">This enables existing applications to interact with new applications and with each other across networks with proper administration, and new applications can be written to take advantage of networking features.</span></span>

<span data-ttu-id="a8ac2-114">COM-Client Anwendungen müssen nicht wissen, wie Server Objekte verpackt werden, unabhängig davon, ob Sie als Prozess interne Objekte (in DLLs) oder als lokale oder Remote Objekte (in exe) verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-114">COM client applications do not need to be aware of how server objects are packaged, whether they are packaged as in-process objects (in DLLs) or as local or remote objects (in EXEs).</span></span> <span data-ttu-id="a8ac2-115">Mithilfe von verteiltem com können Objekte als Dienst Anwendungen verpackt werden, und com wird mit den umfassenden Verwaltungs-und System Integrationsfunktionen von Windows synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-115">Distributed COM further allows objects to be packaged as service applications, synchronizing COM with the rich administrative and system-integration capabilities of Windows.</span></span>

> [!Note]  
> <span data-ttu-id="a8ac2-116">In dieser Dokumentation wird das Akronym com im Gegensatz zu DCOM verwendet.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-116">Throughout this documentation the acronym COM is used in preference to DCOM.</span></span> <span data-ttu-id="a8ac2-117">Dies liegt daran, dass DCOM nicht getrennt ist, sondern nur com mit einem längeren Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-117">This is because DCOM is not separate;it is just COM with a longer wire.</span></span> <span data-ttu-id="a8ac2-118">In Fällen, in denen beschrieben wird, was speziell ein Remote Vorgang ist, wird der Begriff *verteilte com* verwendet.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-118">In cases where what is being described is specifically a remote operation, the term *distributed COM* is used.</span></span>

 

<span data-ttu-id="a8ac2-119">COM ist so konzipiert, dass es möglich ist, die Unterstützung für Standort Transparenz hinzuzufügen, die sich über ein Netzwerk erstreckt.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-119">COM is designed to make it possible to add the support for location transparency that extends across a network.</span></span> <span data-ttu-id="a8ac2-120">Dadurch können Anwendungen, die für einzelne Computer geschrieben werden, in einem Netzwerk ausgeführt werden, und es werden Features bereitgestellt, die diese Funktionen erweitern und die in einem Netzwerk erforderliche Sicherheit erhöhen.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-120">It allows applications written for single computers to run across a network and provides features that extend these capabilities and add to the security necessary in a network.</span></span> <span data-ttu-id="a8ac2-121">(Weitere Informationen finden Sie unter [Sicherheit in com](security-in-com.md).)</span><span class="sxs-lookup"><span data-stu-id="a8ac2-121">(For more information, see [Security in COM](security-in-com.md).)</span></span>

<span data-ttu-id="a8ac2-122">COM gibt einen Mechanismus an, mit dem der Klassen Code von vielen verschiedenen Anwendungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a8ac2-122">COM specifies a mechanism by which the class code can be used by many different applications.</span></span>

<span data-ttu-id="a8ac2-123">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="a8ac2-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a8ac2-124">Einen Zeiger auf ein Objekt zu erhalten</span><span class="sxs-lookup"><span data-stu-id="a8ac2-124">Getting a Pointer to an Object</span></span>](getting-a-pointer-to-an-object.md)
-   [<span data-ttu-id="a8ac2-125">Erstellen eines Objekts über ein Klassenobjekt</span><span class="sxs-lookup"><span data-stu-id="a8ac2-125">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
-   [<span data-ttu-id="a8ac2-126">Zuständigkeiten von com-Servern</span><span class="sxs-lookup"><span data-stu-id="a8ac2-126">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
-   [<span data-ttu-id="a8ac2-127">Persistentes Objektstatus</span><span class="sxs-lookup"><span data-stu-id="a8ac2-127">Persistent Object State</span></span>](persistent-object-state.md)
-   [<span data-ttu-id="a8ac2-128">Bereitstellen von Klassen Informationen</span><span class="sxs-lookup"><span data-stu-id="a8ac2-128">Providing Class Information</span></span>](providing-class-information.md)
-   [<span data-ttu-id="a8ac2-129">Kommunikation zwischen Objekten</span><span class="sxs-lookup"><span data-stu-id="a8ac2-129">Inter-Object Communication</span></span>](inter-object-communication.md)

## <a name="related-topics"></a><span data-ttu-id="a8ac2-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a8ac2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8ac2-131">Rückruf Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="a8ac2-131">Call Synchronization</span></span>](call-synchronization.md)
</dt> <dt>

[<span data-ttu-id="a8ac2-132">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="a8ac2-132">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




