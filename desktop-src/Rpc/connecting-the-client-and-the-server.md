---
title: Verbinden des Clients und des Servers
description: Zur Kommunikation müssen Client-und Serverprogramme eine Kommunikationssitzung im Netzwerk oder in Netzwerken einrichten, die Sie miteinander verbinden.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Verbinden von Client und Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a22ea7a9a6dd30f2b9495b6d2ee868aac217f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471389"
---
# <a name="connecting-the-client-and-the-server"></a><span data-ttu-id="876c0-104">Verbinden des Clients und des Servers</span><span class="sxs-lookup"><span data-stu-id="876c0-104">Connecting the Client and the Server</span></span>

<span data-ttu-id="876c0-105">Zur Kommunikation müssen Client-und Serverprogramme eine Kommunikationssitzung im Netzwerk oder in Netzwerken einrichten, die Sie miteinander verbinden.</span><span class="sxs-lookup"><span data-stu-id="876c0-105">To communicate, client and server programs must establish a communication session across the network or networks that connect them.</span></span> <span data-ttu-id="876c0-106">Nachdem Sie die Verbindung hergestellt haben, kann der Client Remote Prozeduren im Serverprogramm so abrufen, als wären Sie lokal für das Client Programm.</span><span class="sxs-lookup"><span data-stu-id="876c0-106">Once they establish the connection, the client can call remote procedures in the server program as if they were local to the client program.</span></span>

<span data-ttu-id="876c0-107">Dieser Abschnitt enthält eine konzeptionelle Übersicht über das Herstellen einer Verbindung zwischen Clients und Servern für Remote Prozedur Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="876c0-107">This section provides a conceptual overview of how to establish a connection between clients and servers for remote procedure calls.</span></span> <span data-ttu-id="876c0-108">Es wird keine ausführliche Erörterung dieses Themas bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="876c0-108">It does not provide an in-depth discussion of this topic.</span></span> <span data-ttu-id="876c0-109">Alle Konzepte in diesem Abschnitt werden in späteren Kapiteln und im Abschnitt zur RPC-Funktionsreferenz ausführlich dargestellt.</span><span class="sxs-lookup"><span data-stu-id="876c0-109">All of the concepts in this section are presented in detail in later chapters and in the RPC Function Reference section.</span></span>

<span data-ttu-id="876c0-110">Die in diesem Abschnitt gezeigte Diskussion ist in die folgenden Themen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="876c0-110">The discussion presented in this section is divided into the following topics:</span></span>

-   [<span data-ttu-id="876c0-111">Wichtige RPC-Bindungs Terminologie</span><span class="sxs-lookup"><span data-stu-id="876c0-111">Essential RPC Binding Terminology</span></span>](essential-rpc-binding-terminology.md)
-   [<span data-ttu-id="876c0-112">Wie der Server eine Verbindung vorbereitet</span><span class="sxs-lookup"><span data-stu-id="876c0-112">How the Server Prepares for a Connection</span></span>](how-the-server-prepares-for-a-connection.md)
-   [<span data-ttu-id="876c0-113">Einrichten einer Verbindung durch den Client</span><span class="sxs-lookup"><span data-stu-id="876c0-113">How the Client Establishes a Connection</span></span>](how-the-client-establishes-a-connection.md)

<span data-ttu-id="876c0-114">Beachten Sie, dass die Diskussion explizite Bindungs Handles annimmt.</span><span class="sxs-lookup"><span data-stu-id="876c0-114">Note that the discussion assumes explicit binding handles.</span></span> <span data-ttu-id="876c0-115">Wenn Ihre Anwendung jedoch andere Typen von Bindungs Handles verwendet, müssen Sie möglicherweise die in diesem Abschnitt beschriebenen Schritte ändern.</span><span class="sxs-lookup"><span data-stu-id="876c0-115">However, if your application uses other types of binding handles, you may have to modify the steps presented in this section.</span></span> <span data-ttu-id="876c0-116">Weitere Informationen finden Sie unter [Bindung und Handles](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="876c0-116">For more information, see [Binding and Handles](binding-and-handles.md).</span></span>

 

 




