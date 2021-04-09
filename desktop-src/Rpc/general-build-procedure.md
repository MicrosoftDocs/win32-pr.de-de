---
title: Allgemeine buildprozedur
description: Navigationsseite für den Prozess zum Erstellen einer Client/Server-Anwendung mithilfe eines Remote Prozedur Aufrufs (RPC).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b223bf7482cd7cbb65f5b737c90502a6b6dd3de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036837"
---
# <a name="general-build-procedure"></a><span data-ttu-id="7e842-103">Allgemeine buildprozedur</span><span class="sxs-lookup"><span data-stu-id="7e842-103">General Build Procedure</span></span>

<span data-ttu-id="7e842-104">Der Prozess zum Erstellen einer Client-/Serveranwendung mithilfe von Microsoft RPC lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7e842-104">The process for creating a client/server application using Microsoft RPC is:</span></span>

-   <span data-ttu-id="7e842-105">Entwickeln Sie die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7e842-105">Develop the interface.</span></span>
-   <span data-ttu-id="7e842-106">Entwickeln Sie den Server, der die-Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="7e842-106">Develop the server that implements the interface.</span></span>
-   <span data-ttu-id="7e842-107">Entwickeln Sie den Client, der die-Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e842-107">Develop the client that uses the interface.</span></span>

<span data-ttu-id="7e842-108">Diese Schritte werden in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7e842-108">The following figure illustrates these steps.</span></span>

![Prozess zum Erstellen einer Client-/Serveranwendung mithilfe von Microsoft RPC](images/appdev.png)

<span data-ttu-id="7e842-110">Es ist möglich und üblich, die Client-und Server Anwendungen gleichzeitig zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="7e842-110">It is feasible and common to develop the client and server applications concurrently.</span></span> <span data-ttu-id="7e842-111">Da sowohl das Client-als auch das Serverprogramm von der-Schnittstelle abhängig sind, muss die Schnittstelle zwischen Ihnen jedoch vor der Entwicklung des Clients und des Servers entwickelt werden, wie im obigen Diagramm gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7e842-111">Since both the client and server programs are dependent on the interface, however, the interface between them must be developed before the client and server are developed, as shown in the preceding diagram.</span></span>

<span data-ttu-id="7e842-112">In diesem Abschnitt werden die erforderlichen Schritte zum Aufbauen einer Client/Server-Anwendung mit RPC erläutert.</span><span class="sxs-lookup"><span data-stu-id="7e842-112">This section discusses the steps required for building a client/server application with RPC.</span></span> <span data-ttu-id="7e842-113">Die Informationen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="7e842-113">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="7e842-114">Entwickeln der Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7e842-114">Developing the Interface</span></span>](developing-the-interface.md)
-   [<span data-ttu-id="7e842-115">Entwickeln des Servers</span><span class="sxs-lookup"><span data-stu-id="7e842-115">Developing the Server</span></span>](developing-the-server.md)
-   [<span data-ttu-id="7e842-116">Entwickeln des Clients</span><span class="sxs-lookup"><span data-stu-id="7e842-116">Developing the Client</span></span>](developing-the-client.md)

 

 




