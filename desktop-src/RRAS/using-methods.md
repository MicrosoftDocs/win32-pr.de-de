---
title: Verwenden von Methoden
description: Wenn ein Client beim Routing Tabellen-Manager registriert wird, kann er eine Reihe von Methoden exportieren. Diese Methoden werden von anderen Clients zum Abrufen von Client spezifischen Informationen verwendet. Methoden ermöglichen die private Kommunikation zwischen Clients des Routing Tabellen-Managers.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd895fbb3f8f54224522786b5794c5c6c57a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947797"
---
# <a name="using-methods"></a><span data-ttu-id="1d572-105">Verwenden von Methoden</span><span class="sxs-lookup"><span data-stu-id="1d572-105">Using Methods</span></span>

<span data-ttu-id="1d572-106">Wenn ein Client beim Routing Tabellen-Manager registriert wird, kann er eine Reihe von Methoden exportieren.</span><span class="sxs-lookup"><span data-stu-id="1d572-106">When a client registers with the routing table manager, it can export a set of methods.</span></span> <span data-ttu-id="1d572-107">Diese Methoden werden von anderen Clients zum Abrufen von Client spezifischen Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d572-107">These methods are used by other clients to obtain client-specific information.</span></span> <span data-ttu-id="1d572-108">Methoden ermöglichen die private Kommunikation zwischen Clients des Routing Tabellen-Managers.</span><span class="sxs-lookup"><span data-stu-id="1d572-108">Methods enable private communication between clients of the routing table manager.</span></span>

<span data-ttu-id="1d572-109">Ein Client kann die Liste der von einem anderen Client exportierten Methoden abrufen.</span><span class="sxs-lookup"><span data-stu-id="1d572-109">A client can obtain the list of methods exported by another client.</span></span> <span data-ttu-id="1d572-110">Der Client ruft die [**rtmgetentitymethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) -Funktion auf und stellt das Handle des Ziel Clients bereit.</span><span class="sxs-lookup"><span data-stu-id="1d572-110">The client calls the [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) function, supplying the target client's handle.</span></span>

<span data-ttu-id="1d572-111">Jede Methode, die von einem Client exportiert wird, wird durch den Methoden Bezeichner eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1d572-111">Each method exported by a client is uniquely identified by its method identifier.</span></span> <span data-ttu-id="1d572-112">Jeder Client kann bis zu 32 Methoden exportieren.</span><span class="sxs-lookup"><span data-stu-id="1d572-112">Each client can export up to 32 methods.</span></span> <span data-ttu-id="1d572-113">Jede Methode entspricht einem Bit, das im **methodType** -Member der Struktur der [**RTM- \_ Entitäts \_ Export \_ Methode**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1d572-113">Each method corresponds to a bit set in the **MethodType** member of the [**RTM\_ENTITY\_EXPORT\_METHOD**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) structure.</span></span> <span data-ttu-id="1d572-114">Um mehrere Methoden aufzurufen, muss der Client eine logische OR-ID für diese Methoden ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d572-114">To invoke multiple methods, the client should perform a logical OR of the identifiers for those methods.</span></span> <span data-ttu-id="1d572-115">Die Syntax und Semantik der Eingabe-und Ausgabe Strukturen für jedes Protokoll muss angegeben werden, wenn das Protokoll implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="1d572-115">The syntax and semantics of input and output structures for each protocol must be specified when the protocol is implemented.</span></span>

> [!Note]  
> <span data-ttu-id="1d572-116">Methodenbezeichnerwerte, die einem Bit entsprechen, das in der unteren Hälfte des **methodType** -Members (die unteren 16 Bits) festgelegt ist, sind von Microsoft reserviert.</span><span class="sxs-lookup"><span data-stu-id="1d572-116">Method identifier values that correspond to a bit set in the lower half of the **MethodType** member (the lower 16 bits) are reserved by Microsoft.</span></span>

 

<span data-ttu-id="1d572-117">Um die-Methode eines zweiten Clients aufzurufen, Ruft ein Client die [**rtminvokemethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="1d572-117">To invoke a second client's method, a client calls the [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) function.</span></span> <span data-ttu-id="1d572-118">Der Routing Tabellen-Manager gibt alle Anforderungen zum Aufrufen der Methoden eines Clients ein.</span><span class="sxs-lookup"><span data-stu-id="1d572-118">The routing table manager arbitrates all requests to invoke a client's methods.</span></span> <span data-ttu-id="1d572-119">Der Routing Tabellen-Manager führt zwei Funktionen aus, wenn er zwischen Clients unterscheidet:</span><span class="sxs-lookup"><span data-stu-id="1d572-119">The routing table manager performs two functions when it arbitrates between clients:</span></span>

-   <span data-ttu-id="1d572-120">Verhindern, dass der zweite Client eine Methode für einen Client aufruft, dessen Registrierung aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="1d572-120">Preventing the second client from invoking a method for a client that is unregistering.</span></span>
-   <span data-ttu-id="1d572-121">Eine Aufruf Anforderung, wenn Methoden blockiert werden und die Anforderung fortgesetzt werden kann, wenn die Blockierung der Methoden aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="1d572-121">Holding an "invoke" request when methods are blocked, and allowing the request to continue when the methods are unblocked.</span></span>

<span data-ttu-id="1d572-122">Wenn ein Client die Ausführung seiner Methoden durch andere Clients verhindern muss, kann der Client [**rtmblockmethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1d572-122">If a client must prevent other clients from executing its methods, the client can call [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods).</span></span> <span data-ttu-id="1d572-123">Der Routing Tabellen-Manager lässt die Verarbeitung von [**rtminvokemethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) erst dann zu, wenn der Client die Blockierung seiner Methoden wieder aufhebt.</span><span class="sxs-lookup"><span data-stu-id="1d572-123">The routing table manager will not allow a call to [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) to be processed until the client unblocks its methods again.</span></span>

<span data-ttu-id="1d572-124">Clients blockieren in der Regel Methoden, wenn Änderungen an den privaten Daten vorgenommen werden, die zwischen Clients ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="1d572-124">Clients typically block methods when making changes to the private data that is exchanged between clients.</span></span> <span data-ttu-id="1d572-125">Blockierungs Methoden sind eine optionale Aktion.</span><span class="sxs-lookup"><span data-stu-id="1d572-125">Blocking methods is an optional action.</span></span> <span data-ttu-id="1d572-126">Ein Client kann auch interne Sperren verwenden, um zu verhindern, dass andere Clients Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1d572-126">A client can also use internal locks to prevent other clients from invoking methods.</span></span>

<span data-ttu-id="1d572-127">Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter Abrufen [und Abrufen der exportierten Methoden für einen Client](obtain-and-call-the-exported-methods-for-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="1d572-127">For sample code that shows how to use these functions, see [Obtain and Call the Exported Methods for a Client](obtain-and-call-the-exported-methods-for-a-client.md).</span></span>

 

 




