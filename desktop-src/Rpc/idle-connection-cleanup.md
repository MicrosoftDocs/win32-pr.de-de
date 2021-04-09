---
title: Cleanup für Leerlaufverbindung
description: Standardmäßig werden Verbindungen im Thread Pool erst geschlossen, wenn die gesamte Zuordnung heruntergefahren wird.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75587781991c2aae86968d90c9da51331d7a29e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855623"
---
# <a name="idle-connection-cleanup"></a><span data-ttu-id="db9b1-103">Cleanup für Leerlaufverbindung</span><span class="sxs-lookup"><span data-stu-id="db9b1-103">Idle Connection Cleanup</span></span>

<span data-ttu-id="db9b1-104">Standardmäßig werden Verbindungen im Thread Pool erst geschlossen, wenn die gesamte Zuordnung heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="db9b1-104">By default, connections in the thread pool are not closed until the whole association is shut down.</span></span> <span data-ttu-id="db9b1-105">Diese Richtlinie ermöglicht es Clients mit einer großen Anzahl von Threads oder Sicherheits Identitäten, RPC-Aufrufe an den Server auf effiziente Weise durchführen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="db9b1-105">This policy enables clients with a large number of threads or security identities to make RPC calls to the server in an efficient manner.</span></span> <span data-ttu-id="db9b1-106">Der Nachteil ist, dass eine unordinalmenge von Ressourcen für die Verwaltung dieser Verbindungen zugesichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="db9b1-106">The drawback is that an inordinate amount of resources may be committed to maintaining those connections.</span></span> <span data-ttu-id="db9b1-107">Um den Prozess zu verwalten, stellt RPC die [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) -Funktion bereit.</span><span class="sxs-lookup"><span data-stu-id="db9b1-107">To manage the process, RPC provides the [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) function.</span></span> <span data-ttu-id="db9b1-108">Diese Funktion ermöglicht das Cleanup für Leerlaufverbindungen. der Client scannt den Verbindungspool in regelmäßigen Abständen und schließt Verbindungen, die noch nicht verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="db9b1-108">This function enables idle connection cleanup; the client periodically scans the connection pool and closes connections that have not been recently used.</span></span> <span data-ttu-id="db9b1-109">Wenn die Zuordnung über Kontext Handles verfügt, werden bei der Bereinigung der Leerlaufverbindung alle Verbindungen im Leerlauf geschlossen. es wird jedoch sichergestellt, dass mindestens eine Verbindung offen bleibt, auch wenn sich die Verbindung im Leerlauf befindet (andernfalls erhält der Server die Durchführung von Kontext Handles).</span><span class="sxs-lookup"><span data-stu-id="db9b1-109">If the association has maintained context handles, the idle connection cleanup closes all idle connections, but makes sure at least one connection is left open, even if the connection is idle (otherwise the server gets context handle run downs).</span></span> <span data-ttu-id="db9b1-110">Wenn die Zuordnung keine Kontext Handles beibehalten hat, werden bei der Bereinigung der Leerlaufverbindung alle Verbindungen im Leerlauf geschlossen, auch wenn keine Verbindungen im Pool bestehen.</span><span class="sxs-lookup"><span data-stu-id="db9b1-110">If the association has not maintained context handles, idle connection cleanup closes all idle connections, even if doing so leaves no connections in the pool.</span></span>

<span data-ttu-id="db9b1-111">Unter Windows XP wird die Anzahl der geöffneten Verbindungen in einer Zuordnung von der RPC-Laufzeit nachverfolgt. wenn die Anzahl der Verbindungen in einer Zuordnung einen bestimmten Schwellenwert überschreitet, wird automatisch die Verbindungs Bereinigung im Leerlauf übernommen.</span><span class="sxs-lookup"><span data-stu-id="db9b1-111">On Windows XP, the RPC run time keeps track of the number of open connections in an association, and automatically turns on idle connection cleanup if the number of connections in any association exceeds a certain threshold.</span></span>

 

 




