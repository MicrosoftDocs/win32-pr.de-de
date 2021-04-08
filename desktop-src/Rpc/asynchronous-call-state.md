---
title: Asynchroner Aufrufstatus
description: Auf dieser Seite wird der asynchrone Aufruf Status für RPC-Aufrufe beschrieben.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96331a18b267b2e44072840727c8fd06afd11d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856971"
---
# <a name="asynchronous-call-state"></a><span data-ttu-id="c3644-103">Asynchroner Aufrufstatus</span><span class="sxs-lookup"><span data-stu-id="c3644-103">Asynchronous Call State</span></span>

<span data-ttu-id="c3644-104">Auf dieser Seite wird der asynchrone Aufruf Status für RPC-Aufrufe beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c3644-104">This page describes the Asynchronous Call State for RPC calls.</span></span>

## <a name="client-behavior"></a><span data-ttu-id="c3644-105">Client Verhalten</span><span class="sxs-lookup"><span data-stu-id="c3644-105">Client Behavior</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3644-106">State</span><span class="sxs-lookup"><span data-stu-id="c3644-106">State</span></span></th>
<th><span data-ttu-id="c3644-107">Name des Zustands</span><span class="sxs-lookup"><span data-stu-id="c3644-107">State name</span></span></th>
<th><span data-ttu-id="c3644-108">Aktion</span><span class="sxs-lookup"><span data-stu-id="c3644-108">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c3644-109">C</span><span class="sxs-lookup"><span data-stu-id="c3644-109">C</span></span></td>
<td><span data-ttu-id="c3644-110">Ausführen des Aufrufes</span><span class="sxs-lookup"><span data-stu-id="c3644-110">Make the call</span></span></td>
<td><span data-ttu-id="c3644-111">Erstellen des RPC</span><span class="sxs-lookup"><span data-stu-id="c3644-111">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="c3644-112">Bei Erfolg gehe zu Status wcomp</span><span class="sxs-lookup"><span data-stu-id="c3644-112">On success go to state WComp</span></span></li>
<li><span data-ttu-id="c3644-113">Bei Ausnahme gehe zu Ende</span><span class="sxs-lookup"><span data-stu-id="c3644-113">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="c3644-114">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="c3644-114">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3644-115">Kann</span><span class="sxs-lookup"><span data-stu-id="c3644-115">Can</span></span></td>
<td><span data-ttu-id="c3644-116">Abbrechen des Aufrufes</span><span class="sxs-lookup"><span data-stu-id="c3644-116">Cancel the call</span></span></td>
<td><span data-ttu-id="c3644-117">Aufrufen von <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>rpcasynccancelcallgo</strong></a>zu wcomp</span><span class="sxs-lookup"><span data-stu-id="c3644-117">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3644-118">Wcomp</span><span class="sxs-lookup"><span data-stu-id="c3644-118">WComp</span></span></td>
<td><span data-ttu-id="c3644-119">Auf Abschluss warten</span><span class="sxs-lookup"><span data-stu-id="c3644-119">Wait for completion</span></span></td>
<td><span data-ttu-id="c3644-120">Warten Sie, bis notificationcall\benachrichtigungs Benachrichtigung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="c3644-120">Wait for notificationCall-complete notification should be received</span></span><br/> <span data-ttu-id="c3644-121">Gehe zu Comp</span><span class="sxs-lookup"><span data-stu-id="c3644-121">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3644-122">Zuschreiben</span><span class="sxs-lookup"><span data-stu-id="c3644-122">Comp</span></span></td>
<td><span data-ttu-id="c3644-123">Completion</span><span class="sxs-lookup"><span data-stu-id="c3644-123">Completion</span></span></td>
<td><span data-ttu-id="c3644-124">Problem " <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcasynccompletecallgo</strong></a>to End"</span><span class="sxs-lookup"><span data-stu-id="c3644-124">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3644-125">Ende</span><span class="sxs-lookup"><span data-stu-id="c3644-125">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="server-behavior"></a><span data-ttu-id="c3644-126">Server Verhalten</span><span class="sxs-lookup"><span data-stu-id="c3644-126">Server Behavior</span></span>



| <span data-ttu-id="c3644-127">State</span><span class="sxs-lookup"><span data-stu-id="c3644-127">State</span></span> | <span data-ttu-id="c3644-128">Name des Zustands</span><span class="sxs-lookup"><span data-stu-id="c3644-128">State name</span></span>     | <span data-ttu-id="c3644-129">Aktion</span><span class="sxs-lookup"><span data-stu-id="c3644-129">Action</span></span>                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3644-130">D</span><span class="sxs-lookup"><span data-stu-id="c3644-130">D</span></span>     | <span data-ttu-id="c3644-131">Dispatch</span><span class="sxs-lookup"><span data-stu-id="c3644-131">Dispatch</span></span>       | <span data-ttu-id="c3644-132">Der Aufruf wird vom RPC-runtimeprocess gesendet.</span><span class="sxs-lookup"><span data-stu-id="c3644-132">The call is dispatched by the RPC runtimeProcess</span></span><br/> <span data-ttu-id="c3644-133">Gehe zu Comp</span><span class="sxs-lookup"><span data-stu-id="c3644-133">Go to Comp</span></span><br/> <span data-ttu-id="c3644-134">So führen Sie einen fehlerhaften Fehler (während der Ausführung im RPC-Thread) aus: Ausnahme auslösen; Gehe zu Ende</span><span class="sxs-lookup"><span data-stu-id="c3644-134">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="c3644-135">So führen Sie einen fehlerhaften Fehler aus: Gehe zu A</span><span class="sxs-lookup"><span data-stu-id="c3644-135">To fail gracefully: go to A</span></span><br/> |
| <span data-ttu-id="c3644-136">A</span><span class="sxs-lookup"><span data-stu-id="c3644-136">A</span></span>     | <span data-ttu-id="c3644-137">Abbrechen des Aufrufes</span><span class="sxs-lookup"><span data-stu-id="c3644-137">Abort the call</span></span> | <span data-ttu-id="c3644-138">Aufrufen von [**rpcasyncabortcallgo**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)zum Ende</span><span class="sxs-lookup"><span data-stu-id="c3644-138">Call [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Go to End</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="c3644-139">Zuschreiben</span><span class="sxs-lookup"><span data-stu-id="c3644-139">Comp</span></span>  | <span data-ttu-id="c3644-140">Completion</span><span class="sxs-lookup"><span data-stu-id="c3644-140">Completion</span></span>     | <span data-ttu-id="c3644-141">Problem " [**rpcasynccompletecallgo**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)to End"</span><span class="sxs-lookup"><span data-stu-id="c3644-141">Issue [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)Go to End</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="c3644-142">Ende</span><span class="sxs-lookup"><span data-stu-id="c3644-142">End</span></span>   |                |                                                                                                                                                                                                                     |



 

 

 





