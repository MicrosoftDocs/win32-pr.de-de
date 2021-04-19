---
description: Die Peer-graphingapi ermöglicht es Anwendungen, Daten zwischen Peers effizient und zuverlässig zu übergeben. Die wichtigsten Konzepte der Peer Graph-Technologie sind die Knoten eines Peer Diagramms und Ereignis Hinweise.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: Informationen zur graphende-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b08e320f1c8d176d0bd34cc7a9a9422c6cfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349233"
---
# <a name="about-the-graphing-api"></a><span data-ttu-id="73fda-104">Informationen zur graphende-API</span><span class="sxs-lookup"><span data-stu-id="73fda-104">About the Graphing API</span></span>

<span data-ttu-id="73fda-105">Die Peer-graphingapi ermöglicht es Anwendungen, Daten zwischen Peers effizient und zuverlässig zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="73fda-105">The Peer Graphing API allows applications to pass data between peers efficiently and reliably.</span></span> <span data-ttu-id="73fda-106">Die wichtigsten Konzepte der Peer Graph-Technologie sind die **Knoten** eines Peer Diagramms und Ereignis Hinweise.</span><span class="sxs-lookup"><span data-stu-id="73fda-106">The core concepts of peer graph technology are the **nodes** of a peer graph, and event notices.</span></span>

## <a name="nodes"></a><span data-ttu-id="73fda-107">Nodes</span><span class="sxs-lookup"><span data-stu-id="73fda-107">Nodes</span></span>

<span data-ttu-id="73fda-108">Ein Knoten stellt eine bestimmte Instanz eines Peers in einem Netzwerk dar.</span><span class="sxs-lookup"><span data-stu-id="73fda-108">A node represents a specific instance of a peer on a network.</span></span> <span data-ttu-id="73fda-109">Die Peer Graph-API-Infrastruktur stellt sicher, dass jeder Knoten über eine konsistente Sicht der Daten in einem Diagramm verfügt.</span><span class="sxs-lookup"><span data-stu-id="73fda-109">The Peer Graphing API infrastructure ensures that each node has a consistent view of the data in a graph.</span></span> <span data-ttu-id="73fda-110">Ein Knoten verfügt über die folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="73fda-110">A node has the following features:</span></span>

-   <span data-ttu-id="73fda-111">Kann eine Verbindung mit einem anderen Knoten herstellen und ein verbundener Netzwerk, das als Peer Diagramm bezeichnet wird, bilden.</span><span class="sxs-lookup"><span data-stu-id="73fda-111">Can connect to a different node, and form an interrelated network called a peer graph.</span></span>
-   <span data-ttu-id="73fda-112">Kann Daten für andere Knoten in einem Diagramm in Form eines [Datensatzes](records.md)freigeben.</span><span class="sxs-lookup"><span data-stu-id="73fda-112">Can share data with other nodes in a graph in the form of a [record](records.md).</span></span>
-   <span data-ttu-id="73fda-113">Direkt von den Peer Diagrammen, die mithilfe der Peer [Gruppierungs-API](about-the-grouping-api.md)hergestellt wurden, können direkte Verbindungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="73fda-113">Can create direct connections separate from the peer graphs established by using the Peer [Grouping API](about-the-grouping-api.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="73fda-114">Direkte Verbindungen ermöglichen es Knoten, private Daten an einander zu senden.</span><span class="sxs-lookup"><span data-stu-id="73fda-114">Direct connections allow nodes to send private data to each other.</span></span>

     

## <a name="event-notices"></a><span data-ttu-id="73fda-115">Ereignis Hinweise</span><span class="sxs-lookup"><span data-stu-id="73fda-115">Event Notices</span></span>

<span data-ttu-id="73fda-116">Die Peer-graphingapi verfügt über eine Ereignis Infrastruktur, die es einer Anwendung ermöglicht, ein Peer Ereignis innerhalb der Peer graphat-API-Infrastruktur zu registrieren und zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="73fda-116">The Peer Graphing API has an event infrastructure that allows an application to register and receive notice of a peer event within the Peer Graphing API infrastructure.</span></span> <span data-ttu-id="73fda-117">Wenn sich etwas innerhalb eines Peer Diagramms ändert, sendet eine Anwendung eine Ereignis Benachrichtigung, um zu ermitteln, ob eine Änderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="73fda-117">When something changes within a peer graph, an application sends an event notice to identify that a change has occurred.</span></span>

 

 



