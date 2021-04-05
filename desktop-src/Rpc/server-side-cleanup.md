---
title: Server seitiges Cleanup
description: Server seitiges Bereinigung und Remote Prozedur Aufruf (RPC).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a66272fc3cca209d6825ac34d5158094ddff39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037221"
---
# <a name="server-side-cleanup"></a><span data-ttu-id="6311b-103">Server seitiges Cleanup</span><span class="sxs-lookup"><span data-stu-id="6311b-103">Server-side Cleanup</span></span>

<span data-ttu-id="6311b-104">Stellen Sie sich das folgende Szenario vor:</span><span class="sxs-lookup"><span data-stu-id="6311b-104">Imagine the following scenario:</span></span>

<span data-ttu-id="6311b-105">Ein Client öffnet ein Kontext Handle und beendet oder verliert die Verbindung mit dem Server.</span><span class="sxs-lookup"><span data-stu-id="6311b-105">A client opens a context handle, and then either stops or loses connectivity to the server.</span></span> <span data-ttu-id="6311b-106">Wie erkennt der Server, dass der Client fehlgeschlagen ist und der Kontext Handle ausgeführt werden soll?</span><span class="sxs-lookup"><span data-stu-id="6311b-106">How does the server detect that the client has failed and the context handle should be run down?</span></span> <span data-ttu-id="6311b-107">Es gibt zwei unter Szenarios: eine besteht darin, dass der Client ordnungsgemäß heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="6311b-107">There are two subscenarios: one is that the client is shut down in an orderly manner.</span></span> <span data-ttu-id="6311b-108">In diesem Fall wird der Server benachrichtigt, dass er heruntergefahren wird, und der Server kann bereinigt werden, einschließlich der Ausführung von Kontext-Laufzeiten.</span><span class="sxs-lookup"><span data-stu-id="6311b-108">In such case, it notifies the server that it is shutting down, and the server can clean up, including performing context run downs.</span></span> <span data-ttu-id="6311b-109">Wenn der Client nicht ordnungsgemäß heruntergefahren wird oder der Server nicht benachrichtigt werden kann, verwendet der Server Keep-Alives, um zu bestimmen, ob der Client noch verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6311b-109">If the client does not shut down in an orderly manner or it cannot notify the server, the server uses keep alives to determine whether the client is still available.</span></span> <span data-ttu-id="6311b-110">Auf der Serverseite hat die [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) -Funktion keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="6311b-110">On the server side, the [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) function has no effect.</span></span> <span data-ttu-id="6311b-111">Stattdessen verwendet der Server die Einstellung Global pro Computer – Keep Alive, die standardmäßig ungefähr zwei Stunden beträgt.</span><span class="sxs-lookup"><span data-stu-id="6311b-111">Instead, the server uses the global per machine–keep alive setting, which defaults to approximately two hours.</span></span> <span data-ttu-id="6311b-112">Wenn der Client nicht auf die Keep-Alives des Servers antwortet, wird die Verbindung geschlossen.</span><span class="sxs-lookup"><span data-stu-id="6311b-112">If the client does not respond to the server's keep alives, the connection is closed.</span></span> <span data-ttu-id="6311b-113">Wenn alle Verbindungen mit einem bestimmten Client Prozess geschlossen sind, bereinigt der Server die ausstehenden Kontext Handles und führt Sie aus.</span><span class="sxs-lookup"><span data-stu-id="6311b-113">When all connections to a given client process are closed, the server cleans up and runs down outstanding context handles.</span></span>

 

 




