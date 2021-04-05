---
title: Beibehalten des Zustands auf dem Server zwischen Aufrufen
description: Es ist häufig erforderlich, den Zustand auf dem Server zwischen separaten RPC-Aufrufen \ 8212 beizubehalten. die Verwendung von Kontext Handles ist die beste Möglichkeit. Mit wenigen Worten, wie Kontext Handles intern funktionieren, hilft Ihnen zu verstehen, wann Kontext Handles am besten funktionieren.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- Remote Prozedur Aufruf RPC, bewährte Methoden, aufrechterhalten des Zustands zwischen Aufrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00090fb317cba8c33e7b60ac81762d7d21dd4dc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707187"
---
# <a name="maintaining-state-on-the-server-between-calls"></a><span data-ttu-id="3acd8-105">Beibehalten des Zustands auf dem Server zwischen Aufrufen</span><span class="sxs-lookup"><span data-stu-id="3acd8-105">Maintaining State on the Server Between Calls</span></span>

<span data-ttu-id="3acd8-106">Es ist häufig erforderlich, den Zustand auf dem Server zwischen separaten RPC-Aufrufen beizubehalten – mithilfe von Kontext Handles ist dies die beste Möglichkeit.</span><span class="sxs-lookup"><span data-stu-id="3acd8-106">It is often necessary to maintain state on the server between separate RPC calls—using context handles is the best way to do so.</span></span> <span data-ttu-id="3acd8-107">Mit wenigen Worten, wie Kontext Handles intern funktionieren, hilft Ihnen zu verstehen, wann Kontext Handles am besten funktionieren.</span><span class="sxs-lookup"><span data-stu-id="3acd8-107">A few words about how context handles operate internally helps in understanding when context handles work best.</span></span>

<span data-ttu-id="3acd8-108">Der Client erhält nie den Status, der auf dem Server beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="3acd8-108">The client never receives the state kept on the server.</span></span> <span data-ttu-id="3acd8-109">In den meisten Fällen ist der Status auf dem Server ein Zeiger auf einen Speicherblock, und der Client hat keine Informationen dazu.</span><span class="sxs-lookup"><span data-stu-id="3acd8-109">Most often the state on the server is a pointer to a memory block, and the client has no information about it.</span></span> <span data-ttu-id="3acd8-110">Alle Client Empfangs Vorgänge sind eine große eindeutige Zahl, mit anderen Informationen, die vom Server an den Client gesendet werden und die das Kontext Handle in allen nachfolgenden Vorgängen darstellt.</span><span class="sxs-lookup"><span data-stu-id="3acd8-110">All the client receives is a large unique number, with other information associated with it, that the server sends to the client and which represents the context handle in all subsequent operations.</span></span> <span data-ttu-id="3acd8-111">Wenn sich der Client auf ein geöffnetes Handle bezieht, sendet es die große Zahl, die er vom Server empfangen hat, als dieses Kontext Handle geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="3acd8-111">Whenever the client refers to an opened handle, it sends the large number it received from the server when that context handle was opened.</span></span>

<span data-ttu-id="3acd8-112">Der Server verfolgt alle großen Zahlen, die er an einen Client sendet.</span><span class="sxs-lookup"><span data-stu-id="3acd8-112">The server keeps track of all large numbers it sends to a client.</span></span> <span data-ttu-id="3acd8-113">Wenn der Server eine große Zahl empfängt, die ein Kontext Handle darstellt, sucht er die Zahl in der Auflistung gültiger, ausstehender Kontext Handles für diesen Client und sucht den serverseitigen Kontext, der einer bestimmten großen Zahl entspricht.</span><span class="sxs-lookup"><span data-stu-id="3acd8-113">When the server receives a large number representing a context handle, it looks up the number in the collection of valid, outstanding context handles for that client, and finds the server-side context corresponding to a given large number.</span></span> <span data-ttu-id="3acd8-114">Diese wird an die Server Routine übergeben.</span><span class="sxs-lookup"><span data-stu-id="3acd8-114">This is passed to the server routine.</span></span> <span data-ttu-id="3acd8-115">Wenn die große Zahl nicht gefunden wird, wird eine RPC \_ X \_ SS \_ -Kontext Konflikt \_ Ausnahme ausgelöst und an den Client weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="3acd8-115">If the large number is not found, an RPC\_X\_SS\_CONTEXT\_MISMATCH exception is raised and propagated to the client.</span></span>

<span data-ttu-id="3acd8-116">Dies sind die folgenden:</span><span class="sxs-lookup"><span data-stu-id="3acd8-116">The corollaries of this design are as follows:</span></span>

-   <span data-ttu-id="3acd8-117">Ein Kontext Handle ist nur im Kontext der vorhandenen Client-/Serversitzung gültig.</span><span class="sxs-lookup"><span data-stu-id="3acd8-117">A context handle is valid only in the context of the existing client/server session.</span></span> <span data-ttu-id="3acd8-118">Sie kann nicht an einen anderen Client übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="3acd8-118">It cannot be passed to another client.</span></span>
-   <span data-ttu-id="3acd8-119">Ein Kontext Handle wird ungültig, wenn der Server neu gestartet wird oder andernfalls seine Verbindung mit dem Client verliert.</span><span class="sxs-lookup"><span data-stu-id="3acd8-119">A context handle becomes invalid if the server is rebooted, or otherwise loses its connection to the client.</span></span>
-   <span data-ttu-id="3acd8-120">Der Client kann nicht interpretieren, was das Kontext Handle auf dem Server darstellt.</span><span class="sxs-lookup"><span data-stu-id="3acd8-120">The client cannot interpret what the context handle represents on the server.</span></span> <span data-ttu-id="3acd8-121">Für einen Client sind alle Kontext Handles einfach eine große Zahl.</span><span class="sxs-lookup"><span data-stu-id="3acd8-121">To a client, all context handles are simply large numbers.</span></span>

<span data-ttu-id="3acd8-122">Wenn der Client fehlschlägt, erhält der Server eine Benachrichtigung, und die Kontext Handles werden mithilfe des-Lauf Mechanismus bereinigt.</span><span class="sxs-lookup"><span data-stu-id="3acd8-122">If the client fails, the server will get a notification and will clean up its context handles using the run-down mechanism.</span></span>

 

 




