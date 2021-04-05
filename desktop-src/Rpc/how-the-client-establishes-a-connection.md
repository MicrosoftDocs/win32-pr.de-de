---
title: Einrichten einer Verbindung durch den Client
description: Um eine Client/Server-Kommunikationssitzung mit einem Serverprogramm einzurichten, müssen Client Anwendungen mit expliziten Handles ein Bindungs Handle erstellen.
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5fd8437fb5821c2b52240256a1938e8de31c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037079"
---
# <a name="how-the-client-establishes-a-connection"></a><span data-ttu-id="d5434-103">Einrichten einer Verbindung durch den Client</span><span class="sxs-lookup"><span data-stu-id="d5434-103">How the Client Establishes a Connection</span></span>

<span data-ttu-id="d5434-104">Um eine Client/Server-Kommunikationssitzung mit einem Serverprogramm einzurichten, müssen Client Anwendungen mit expliziten Handles ein Bindungs Handle erstellen.</span><span class="sxs-lookup"><span data-stu-id="d5434-104">To establish a client/server communication session with a server program, client applications with explicit handles need to create a binding handle.</span></span> <span data-ttu-id="d5434-105">Danach findet die RPC-Lauf Zeit Bibliothek den Computer, der das Serverprogramm hostet.</span><span class="sxs-lookup"><span data-stu-id="d5434-105">After they do, the RPC run-time library finds the computer that hosts the server program.</span></span> <span data-ttu-id="d5434-106">Anschließend findet der Endpunkt den Endpunkt, an dem das Serverprogramm lauscht, und leitet ihn an ihn weiter.</span><span class="sxs-lookup"><span data-stu-id="d5434-106">It then finds the endpoint that the server program is listening to and directs the call to it.</span></span> <span data-ttu-id="d5434-107">Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d5434-107">The following diagram illustrates this process.</span></span>

![ein RPC-Client stellt eine Verbindung mit einem RPC-Server her.](images/clntcon.png)

<span data-ttu-id="d5434-109">Dieser Abschnitt enthält Informationen darüber, wie der Client eine Verbindung mit dem Serverprogramm herstellt und die von ihm angebotenen Remote Prozeduren ausführt.</span><span class="sxs-lookup"><span data-stu-id="d5434-109">This section presents information about how the client connects to the server program and executes remote procedures that it offers.</span></span> <span data-ttu-id="d5434-110">Es gibt viele Ansätze für die Ausführung dieser Schritte. je nach ausgewähltem Entwurf kann eine Anwendung eine andere Gruppe von Schritten auswählen.</span><span class="sxs-lookup"><span data-stu-id="d5434-110">There are many approaches to completing these steps; depending on the design chosen, an application may choose a different set of steps.</span></span> <span data-ttu-id="d5434-111">Dieses Beispiel ist einfach eine Möglichkeit.</span><span class="sxs-lookup"><span data-stu-id="d5434-111">This example is simply one way of doing so.</span></span>

<span data-ttu-id="d5434-112">Die Diskussion ist in die folgenden Abschnitte unterteilt:</span><span class="sxs-lookup"><span data-stu-id="d5434-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="d5434-113">Erstellen eines Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="d5434-113">Creating a Binding Handle</span></span>](creating-a-binding-handle.md)
-   [<span data-ttu-id="d5434-114">Ausführen eines Remote Prozedur Aufrufes</span><span class="sxs-lookup"><span data-stu-id="d5434-114">Making a Remote Procedure Call</span></span>](making-a-remote-procedure-call.md)
-   [<span data-ttu-id="d5434-115">Suchen des Server Programms</span><span class="sxs-lookup"><span data-stu-id="d5434-115">Finding the Server Program</span></span>](finding-the-server-program.md)
-   [<span data-ttu-id="d5434-116">Senden des Aufrufes an das Server Programm</span><span class="sxs-lookup"><span data-stu-id="d5434-116">Sending the Call to the Server Program</span></span>](sending-the-call-to-the-server-program.md)

 

 




