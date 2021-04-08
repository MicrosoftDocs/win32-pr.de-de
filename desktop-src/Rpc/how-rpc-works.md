---
title: Funktionsweise von RPC
description: Die RPC-Tools machen es Benutzern so angezeigt, als ob ein Client eine Prozedur direkt aufruft, die sich in einem Remote Serverprogramm befindet.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12832d0de4eb972bb1d9d51df0c871191d4d079a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711832"
---
# <a name="how-rpc-works"></a><span data-ttu-id="81bde-103">Funktionsweise von RPC</span><span class="sxs-lookup"><span data-stu-id="81bde-103">How RPC Works</span></span>

<span data-ttu-id="81bde-104">Die RPC-Tools machen es Benutzern so angezeigt, als ob ein Client eine Prozedur direkt aufruft, die sich in einem Remote Serverprogramm befindet.</span><span class="sxs-lookup"><span data-stu-id="81bde-104">The RPC tools make it appear to users as though a client directly calls a procedure located in a remote server program.</span></span> <span data-ttu-id="81bde-105">Client und Server verfügen jeweils über eigene Adressräume. Das heißt, jede verfügt über eine eigene Speicher Ressource, die den Daten zugeordnet ist, die von der Prozedur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81bde-105">The client and server each have their own address spaces; that is, each has its own memory resource allocated to data used by the procedure.</span></span> <span data-ttu-id="81bde-106">Die folgende Abbildung veranschaulicht die RPC-Architektur.</span><span class="sxs-lookup"><span data-stu-id="81bde-106">The following figure illustrates the RPC architecture.</span></span>

![RPC-Architektur](images/prog-a11.png)

<span data-ttu-id="81bde-108">Wie die Abbildung zeigt, ruft die Client Anwendung anstelle des eigentlichen Codes, der die Prozedur implementiert, eine lokale Stub-Prozedur auf.</span><span class="sxs-lookup"><span data-stu-id="81bde-108">As the illustration shows, the client application calls a local stub procedure instead of the actual code implementing the procedure.</span></span> <span data-ttu-id="81bde-109">Stusb werden kompiliert und mit der Client Anwendung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="81bde-109">Stubs are compiled and linked with the client application.</span></span> <span data-ttu-id="81bde-110">Anstatt den eigentlichen Code zu enthalten, der die Remote Prozedur implementiert, wird der Client-Stub-Code:</span><span class="sxs-lookup"><span data-stu-id="81bde-110">Instead of containing the actual code that implements the remote procedure, the client stub code:</span></span>

-   <span data-ttu-id="81bde-111">Ruft die erforderlichen Parameter aus dem Client Adressbereich ab.</span><span class="sxs-lookup"><span data-stu-id="81bde-111">Retrieves the required parameters from the client address space.</span></span>
-   <span data-ttu-id="81bde-112">Übersetzt die Parameter nach Bedarf in ein Standardmäßiges NDR-Format für die Übertragung über das Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="81bde-112">Translates the parameters as needed into a standard NDR format for transmission over the network.</span></span>
-   <span data-ttu-id="81bde-113">Ruft Funktionen in der RPC-Client Lauf Zeit Bibliothek auf, um die Anforderung und ihre Parameter an den Server zu senden.</span><span class="sxs-lookup"><span data-stu-id="81bde-113">Calls functions in the RPC client run-time library to send the request and its parameters to the server.</span></span>

<span data-ttu-id="81bde-114">Der Server führt die folgenden Schritte aus, um die Remote Prozedur aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="81bde-114">The server performs the following steps to call the remote procedure.</span></span>

1.  <span data-ttu-id="81bde-115">Die Server-RPC-Lauf Zeit Bibliotheksfunktionen akzeptieren die Anforderung und wenden die Stub-Prozedur des Servers an.</span><span class="sxs-lookup"><span data-stu-id="81bde-115">The server RPC run-time library functions accept the request and call the server stub procedure.</span></span>
2.  <span data-ttu-id="81bde-116">Der Serverstub Ruft die Parameter aus dem Netzwerk Puffer ab und konvertiert sie aus dem Netzwerk Übertragungsformat in das Format, das der Server benötigt.</span><span class="sxs-lookup"><span data-stu-id="81bde-116">The server stub retrieves the parameters from the network buffer and converts them from the network transmission format to the format the server needs.</span></span>
3.  <span data-ttu-id="81bde-117">Der Serverstub Ruft das eigentliche Verfahren auf dem Server auf.</span><span class="sxs-lookup"><span data-stu-id="81bde-117">The server stub calls the actual procedure on the server.</span></span>

<span data-ttu-id="81bde-118">Anschließend wird die Remote Prozedur ausgeführt, die möglicherweise Ausgabeparameter und einen Rückgabewert erzeugt.</span><span class="sxs-lookup"><span data-stu-id="81bde-118">The remote procedure then runs, possibly generating output parameters and a return value.</span></span> <span data-ttu-id="81bde-119">Wenn die Remote Prozedur beendet ist, werden die Daten mit einer ähnlichen Sequenz von Schritten an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81bde-119">When the remote procedure is complete, a similar sequence of steps returns the data to the client.</span></span>

1.  <span data-ttu-id="81bde-120">Die Remote Prozedur gibt die Daten an den Serverstub zurück.</span><span class="sxs-lookup"><span data-stu-id="81bde-120">The remote procedure returns its data to the server stub.</span></span>
2.  <span data-ttu-id="81bde-121">Der Serverstub konvertiert Ausgabeparameter in das Format, das für die Übertragung über das Netzwerk erforderlich ist, und gibt Sie an die RPC-Lauf Zeit Bibliotheksfunktionen zurück.</span><span class="sxs-lookup"><span data-stu-id="81bde-121">The server stub converts output parameters to the format required for transmission over the network and returns them to the RPC run-time library functions.</span></span>
3.  <span data-ttu-id="81bde-122">Die Server-RPC-Lauf Zeit Bibliotheksfunktionen übertragen die Daten im Netzwerk an den Client Computer.</span><span class="sxs-lookup"><span data-stu-id="81bde-122">The server RPC run-time library functions transmit the data on the network to the client computer.</span></span>

<span data-ttu-id="81bde-123">Der Client schließt den Prozess ab, indem er die Daten über das Netzwerk akzeptiert und an die aufrufende Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="81bde-123">The client completes the process by accepting the data over the network and returning it to the calling function.</span></span>

1.  <span data-ttu-id="81bde-124">Die Client-RPC-Lauf Zeit Bibliothek empfängt die Remote Prozedur Rückgabewerte und gibt Sie an den Client-Stub zurück.</span><span class="sxs-lookup"><span data-stu-id="81bde-124">The client RPC run-time library receives the remote-procedure return values and returns them to the client stub.</span></span>
2.  <span data-ttu-id="81bde-125">Der Clientstub konvertiert die Daten aus dem Mandanten in das Format, das vom Client Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81bde-125">The client stub converts the data from its NDR to the format used by the client computer.</span></span> <span data-ttu-id="81bde-126">Der Stub schreibt Daten in den Client Speicher und gibt das Ergebnis an das Aufruf Programm auf dem Client zurück.</span><span class="sxs-lookup"><span data-stu-id="81bde-126">The stub writes data into the client memory and returns the result to the calling program on the client.</span></span>
3.  <span data-ttu-id="81bde-127">Die aufrufende Prozedur wird so fortgesetzt, als ob die Prozedur auf dem gleichen Computer aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="81bde-127">The calling procedure continues as if the procedure had been called on the same computer.</span></span>

<span data-ttu-id="81bde-128">Die Laufzeitbibliotheken werden in zwei Teilen bereitgestellt: eine Import Bibliothek, die mit der Anwendung verknüpft ist, und die RPC-Lauf Zeit Bibliothek, die als Dynamic Link Library (dll) implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="81bde-128">The run-time libraries are provided in two parts: an import library, which is linked with the application and the RPC run-time library, which is implemented as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="81bde-129">Die Serveranwendung enthält Aufrufe der Server Lauf Zeit Bibliotheksfunktionen, die die-Schnittstelle des Servers registrieren und dem Server das akzeptieren von Remote Prozedur aufrufen erlauben.</span><span class="sxs-lookup"><span data-stu-id="81bde-129">The server application contains calls to the server run-time library functions which register the server's interface and allow the server to accept remote procedure calls.</span></span> <span data-ttu-id="81bde-130">Die Serveranwendung enthält auch die anwendungsspezifischen Remote Prozeduren, die von den Client Anwendungen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="81bde-130">The server application also contains the application-specific remote procedures that are called by the client applications.</span></span>

 

 




