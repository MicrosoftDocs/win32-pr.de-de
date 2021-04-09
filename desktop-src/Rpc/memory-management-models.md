---
title: Memory-Management Modelle
description: Memory-Management Modelle
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8114f11755829be9d5f7b17b751e075701ac0aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948099"
---
# <a name="memory-management-models"></a><span data-ttu-id="30751-103">Memory-Management Modelle</span><span class="sxs-lookup"><span data-stu-id="30751-103">Memory-Management Models</span></span>

<span data-ttu-id="30751-104">Als Entwickler haben Sie mehrere Möglichkeiten, wie Arbeitsspeicher zugeordnet und freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="30751-104">As a developer, you have several choices for how memory is allocated and freed.</span></span> <span data-ttu-id="30751-105">Angenommen, eine komplexe Datenstruktur besteht aus Knoten, die mit Zeigern verbunden sind, z. b. eine verknüpfte Liste oder eine Struktur.</span><span class="sxs-lookup"><span data-stu-id="30751-105">Consider a complex data structure that consists of nodes connected with pointers, such as a linked list or a tree.</span></span> <span data-ttu-id="30751-106">Sie können Attribute anwenden, mit denen eines der folgenden Modelle ausgewählt wird:</span><span class="sxs-lookup"><span data-stu-id="30751-106">You can apply attributes that select one of the following models:</span></span>

-   <span data-ttu-id="30751-107">[Zuordnung und Aufhebung der Zuordnung von Knoten zu Knoten](node-by-node-allocation-and-deallocation.md).</span><span class="sxs-lookup"><span data-stu-id="30751-107">[Node-by-node allocation and deallocation](node-by-node-allocation-and-deallocation.md).</span></span>
-   <span data-ttu-id="30751-108">[Ein einzelner linearer Puffer, der vom Stub für die gesamte Struktur zugeordnet wird](stub-allocated-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="30751-108">[A single linear buffer allocated by the stub for the entire tree](stub-allocated-buffers.md).</span></span>
-   [<span data-ttu-id="30751-109">Server-Stub-Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="30751-109">Server stub memory management</span></span>](server-stub-memory-management.md)
-   <span data-ttu-id="30751-110">[Ein einzelner linearer Puffer, der von der Client Anwendung für die gesamte Struktur zugewiesen wird](application-allocated-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="30751-110">[A single linear buffer allocated by the client application for the entire tree](application-allocated-buffer.md).</span></span>
-   <span data-ttu-id="30751-111">[Persistente Speicherung auf dem Server](persistent-storage-on-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="30751-111">[Persistent storage on the server](persistent-storage-on-the-server.md).</span></span>

 

 




