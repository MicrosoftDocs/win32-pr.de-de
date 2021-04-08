---
title: Server-Side Pipe-Implementierung
description: Server Programme für verteilte Anwendungen, die Pipes verwenden, müssen keine Push-, Pull-oder Zuordnungsfunktionen implementieren.
ms.assetid: de733075-5767-4d46-b294-089c7e3cc695
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6927350e10061850c5fac0ab0db7c18570dd2bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037220"
---
# <a name="server-side-pipe-implementation"></a><span data-ttu-id="e977b-103">Server-Side Pipe-Implementierung</span><span class="sxs-lookup"><span data-stu-id="e977b-103">Server-Side Pipe Implementation</span></span>

<span data-ttu-id="e977b-104">Server Programme für verteilte Anwendungen, die Pipes verwenden, müssen keine Push-, Pull-oder Zuordnungsfunktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="e977b-104">Server programs for distributed applications that use pipes need not implement any push, pull, or alloc functions.</span></span> <span data-ttu-id="e977b-105">Sie müssen Prozeduren enthalten, die Clients Remote aufrufen können, um Datenübertragungen zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="e977b-105">They do need to contain procedures that clients can invoke remotely to initiate data transfers.</span></span> <span data-ttu-id="e977b-106">In den folgenden Themen wird in diesem Abschnitt erläutert, wie die Remote Prozeduren des Servers implementiert werden können.</span><span class="sxs-lookup"><span data-stu-id="e977b-106">In the following topics, this section explains how the server's remote procedures can be implemented.</span></span>

-   [<span data-ttu-id="e977b-107">Implementieren von eingabepipes auf dem Server</span><span class="sxs-lookup"><span data-stu-id="e977b-107">Implementing Input Pipes on the Server</span></span>](implementing-input-pipes-on-the-server.md)
-   [<span data-ttu-id="e977b-108">Implementieren von ausgabepipes auf dem Server</span><span class="sxs-lookup"><span data-stu-id="e977b-108">Implementing Output Pipes on the Server</span></span>](implementing-output-pipes-on-the-server.md)

 

 




