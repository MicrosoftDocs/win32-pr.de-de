---
title: Asynchroner Pipe-Zustand
description: Auf dieser Seite wird der asynchrone Pipezustand für RPC-Aufrufe beschrieben.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8396b08c7ef7b8152457d9426883645fab39bdef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038565"
---
# <a name="asynchronous-pipe-state"></a><span data-ttu-id="9c100-103">Asynchroner Pipe-Zustand</span><span class="sxs-lookup"><span data-stu-id="9c100-103">Asynchronous Pipe State</span></span>

<span data-ttu-id="9c100-104">Auf dieser Seite wird der asynchrone Pipezustand für RPC-Aufrufe beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9c100-104">This page describes the Asynchronous Pipe State for RPC calls.</span></span>

## <a name="in-pipe"></a><span data-ttu-id="9c100-105">IN Pipe</span><span class="sxs-lookup"><span data-stu-id="9c100-105">IN Pipe</span></span>

<span data-ttu-id="9c100-106">Client Verhalten</span><span class="sxs-lookup"><span data-stu-id="9c100-106">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c100-107">State</span><span class="sxs-lookup"><span data-stu-id="9c100-107">State</span></span></th>
<th><span data-ttu-id="9c100-108">Name des Staats</span><span class="sxs-lookup"><span data-stu-id="9c100-108">State Name</span></span></th>
<th><span data-ttu-id="9c100-109">Aktion</span><span class="sxs-lookup"><span data-stu-id="9c100-109">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c100-110">C</span><span class="sxs-lookup"><span data-stu-id="9c100-110">C</span></span></td>
<td><span data-ttu-id="9c100-111">Ausführen des Aufrufes</span><span class="sxs-lookup"><span data-stu-id="9c100-111">Make the call</span></span></td>
<td><span data-ttu-id="9c100-112">Erstellen des RPC</span><span class="sxs-lookup"><span data-stu-id="9c100-112">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="9c100-113">Bei Erfolg gehe zu Status WS</span><span class="sxs-lookup"><span data-stu-id="9c100-113">On success go to state WS</span></span></li>
<li><span data-ttu-id="9c100-114">Bei Ausnahme gehe zu Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-114">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="9c100-115">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="9c100-115">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-116">P</span><span class="sxs-lookup"><span data-stu-id="9c100-116">P</span></span></td>
<td><span data-ttu-id="9c100-117">Push</span><span class="sxs-lookup"><span data-stu-id="9c100-117">Push</span></span></td>
<td><span data-ttu-id="9c100-118">Push tätigen</span><span class="sxs-lookup"><span data-stu-id="9c100-118">Make a push</span></span>
<ul>
<li><span data-ttu-id="9c100-119">Bei Fehler "Gehe zu Ende"</span><span class="sxs-lookup"><span data-stu-id="9c100-119">On failure go to End</span></span></li>
<li><span data-ttu-id="9c100-120">Bei Erfolg gehe zu WS</span><span class="sxs-lookup"><span data-stu-id="9c100-120">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="9c100-121">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="9c100-121">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-122">WS</span><span class="sxs-lookup"><span data-stu-id="9c100-122">WS</span></span></td>
<td><span data-ttu-id="9c100-123">Auf senden warten</span><span class="sxs-lookup"><span data-stu-id="9c100-123">Wait for Send</span></span></td>
<td><span data-ttu-id="9c100-124">Auf Benachrichtigung warten</span><span class="sxs-lookup"><span data-stu-id="9c100-124">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="9c100-125">Wenn Sie eine Benachrichtigung erhalten, gehen Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-125">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="9c100-126">Wenn ein Erfolg von <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> empfangen wird und weitere Daten gesendet werden müssen, gehen Sie zu P.</span><span class="sxs-lookup"><span data-stu-id="9c100-126">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="9c100-127">Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> -Vorgang empfangen wird und weitere Daten nicht gesendet werden müssen, gehen Sie zu NP.</span><span class="sxs-lookup"><span data-stu-id="9c100-127">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="9c100-128">Wenn ein Fehler " <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpccallcomplete</strong></a> " empfangen wird, gehen Sie zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-128">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="9c100-129">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="9c100-129">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-130">NP</span><span class="sxs-lookup"><span data-stu-id="9c100-130">NP</span></span></td>
<td><span data-ttu-id="9c100-131">NULL-Push</span><span class="sxs-lookup"><span data-stu-id="9c100-131">Null Push</span></span></td>
<td><span data-ttu-id="9c100-132">Push 0 bytes (null Push)</span><span class="sxs-lookup"><span data-stu-id="9c100-132">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="9c100-133">Bei Fehler "Gehe zu Ende"</span><span class="sxs-lookup"><span data-stu-id="9c100-133">On failure go to End</span></span></li>
<li><span data-ttu-id="9c100-134">Bei Erfolg gehe zu wcomp</span><span class="sxs-lookup"><span data-stu-id="9c100-134">On success go to WComp</span></span></li>
</ul>
<span data-ttu-id="9c100-135">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="9c100-135">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-136">Kann</span><span class="sxs-lookup"><span data-stu-id="9c100-136">Can</span></span></td>
<td><span data-ttu-id="9c100-137">Abbrechen des Aufrufes</span><span class="sxs-lookup"><span data-stu-id="9c100-137">Cancel the Call</span></span></td>
<td><span data-ttu-id="9c100-138">Aufrufen von <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>rpcasynccancelcallgo</strong></a>zu wcomp</span><span class="sxs-lookup"><span data-stu-id="9c100-138">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-139">Wcomp</span><span class="sxs-lookup"><span data-stu-id="9c100-139">WComp</span></span></td>
<td><span data-ttu-id="9c100-140">Auf Abschluss warten</span><span class="sxs-lookup"><span data-stu-id="9c100-140">Wait for Completion</span></span></td>
<td><span data-ttu-id="9c100-141">Warten Sie, bis eine notificationcallbenachrichtigung gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="9c100-141">Wait for notificationCall-complete notification should be received.</span></span><br/> <span data-ttu-id="9c100-142">Gehe zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-142">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-143">Zuschreiben</span><span class="sxs-lookup"><span data-stu-id="9c100-143">Comp</span></span></td>
<td><span data-ttu-id="9c100-144">Completion</span><span class="sxs-lookup"><span data-stu-id="9c100-144">Completion</span></span></td>
<td><span data-ttu-id="9c100-145">Problem " <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcasynccompletecallgo</strong></a>to End"</span><span class="sxs-lookup"><span data-stu-id="9c100-145">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-146">Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-146">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="9c100-147">Server Verhalten</span><span class="sxs-lookup"><span data-stu-id="9c100-147">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c100-148">State</span><span class="sxs-lookup"><span data-stu-id="9c100-148">State</span></span></th>
<th><span data-ttu-id="9c100-149">Name des Staats</span><span class="sxs-lookup"><span data-stu-id="9c100-149">State Name</span></span></th>
<th><span data-ttu-id="9c100-150">Aktion</span><span class="sxs-lookup"><span data-stu-id="9c100-150">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c100-151">D</span><span class="sxs-lookup"><span data-stu-id="9c100-151">D</span></span></td>
<td><span data-ttu-id="9c100-152">Dispatch</span><span class="sxs-lookup"><span data-stu-id="9c100-152">Dispatch</span></span></td>
<td><span data-ttu-id="9c100-153">Der Aufruf wird von der RPC-Laufzeit an "P" gesendet.</span><span class="sxs-lookup"><span data-stu-id="9c100-153">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="9c100-154">So führen Sie einen fehlerhaften Fehler (während der Ausführung im RPC-Thread) aus: Ausnahme auslösen; Gehe zu Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-154">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="9c100-155">So führen Sie einen fehlerhaften Fehler aus: Gehe zu A</span><span class="sxs-lookup"><span data-stu-id="9c100-155">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-156">P</span><span class="sxs-lookup"><span data-stu-id="9c100-156">P</span></span></td>
<td><span data-ttu-id="9c100-157">Pull</span><span class="sxs-lookup"><span data-stu-id="9c100-157">Pull</span></span></td>
<td><span data-ttu-id="9c100-158">Pull erstellen</span><span class="sxs-lookup"><span data-stu-id="9c100-158">Make a pull</span></span>
<ul>
<li><span data-ttu-id="9c100-159">Bei Fehler "Gehe zu Ende"</span><span class="sxs-lookup"><span data-stu-id="9c100-159">On failure go to End</span></span></li>
<li><span data-ttu-id="9c100-160">Bei Erfolg und synchrone Vervollständigung mit bytes, die ungleich NULL sind, wechseln Sie zu P.</span><span class="sxs-lookup"><span data-stu-id="9c100-160">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="9c100-161">Bei Erfolg und synchroner Abschluss mit NULL gelesenen Bytes (null-Pull) gehe zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-161">On success and synchronous completion with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="9c100-162">Bei Erfolg und asynchroner Beendigung (ERROR_IO_PENDING wird zurückgegeben) gehe zu WP</span><span class="sxs-lookup"><span data-stu-id="9c100-162">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="9c100-163">Fehler: Wechseln Sie zu einem</span><span class="sxs-lookup"><span data-stu-id="9c100-163">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-164">WP</span><span class="sxs-lookup"><span data-stu-id="9c100-164">WP</span></span></td>
<td><span data-ttu-id="9c100-165">Auf Pull warten</span><span class="sxs-lookup"><span data-stu-id="9c100-165">Wait for Pull</span></span></td>
<td><span data-ttu-id="9c100-166">Auf Benachrichtigung warten</span><span class="sxs-lookup"><span data-stu-id="9c100-166">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="9c100-167">Wenn Sie einen Abschluss erhalten, wechseln Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-167">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="9c100-168">Wenn ein Fehler " <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> " empfangen wird, wechseln Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-168">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="9c100-169">Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit Bytes ungleich 0 (null) empfangen wird, gehen Sie zu "P".</span><span class="sxs-lookup"><span data-stu-id="9c100-169">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="9c100-170">Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit 0 (null) Bytes empfangen wird (null-Pull), wechseln Sie zu comp.</span><span class="sxs-lookup"><span data-stu-id="9c100-170">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="9c100-171">Wenn ein Fehler aufgetreten ist, wechseln Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-171">If a failure is received go to A</span></span></li>
</ul>
<span data-ttu-id="9c100-172">Fehler: Wechseln Sie zu einem</span><span class="sxs-lookup"><span data-stu-id="9c100-172">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-173">A</span><span class="sxs-lookup"><span data-stu-id="9c100-173">A</span></span></td>
<td><span data-ttu-id="9c100-174">Abbrechen des Aufrufes</span><span class="sxs-lookup"><span data-stu-id="9c100-174">Abort the Call</span></span></td>
<td><span data-ttu-id="9c100-175">Aufrufen von <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>rpcasyncabortcallgo</strong></a>zum Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-175">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-176">Zuschreiben</span><span class="sxs-lookup"><span data-stu-id="9c100-176">Comp</span></span></td>
<td><span data-ttu-id="9c100-177">Completion</span><span class="sxs-lookup"><span data-stu-id="9c100-177">Completion</span></span></td>
<td><span data-ttu-id="9c100-178">Aufrufen von <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcasynccompletecallgo</strong></a>zum Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-178">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-179">Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-179">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a><span data-ttu-id="9c100-180">Out-Pipe</span><span class="sxs-lookup"><span data-stu-id="9c100-180">OUT Pipe</span></span>

<span data-ttu-id="9c100-181">Client Verhalten</span><span class="sxs-lookup"><span data-stu-id="9c100-181">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c100-182">State</span><span class="sxs-lookup"><span data-stu-id="9c100-182">State</span></span></th>
<th><span data-ttu-id="9c100-183">Name des Staats</span><span class="sxs-lookup"><span data-stu-id="9c100-183">State Name</span></span></th>
<th><span data-ttu-id="9c100-184">Aktion</span><span class="sxs-lookup"><span data-stu-id="9c100-184">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c100-185">C</span><span class="sxs-lookup"><span data-stu-id="9c100-185">C</span></span></td>
<td><span data-ttu-id="9c100-186">Ausführen des Aufrufes</span><span class="sxs-lookup"><span data-stu-id="9c100-186">Make the call</span></span></td>
<td><span data-ttu-id="9c100-187">Erstellen des RPC</span><span class="sxs-lookup"><span data-stu-id="9c100-187">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="9c100-188">Bei Erfolg gehe zu P</span><span class="sxs-lookup"><span data-stu-id="9c100-188">On success go to P</span></span></li>
<li><span data-ttu-id="9c100-189">Bei Fehler wechseln Sie zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-189">On failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="9c100-190">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="9c100-190">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-191">P</span><span class="sxs-lookup"><span data-stu-id="9c100-191">P</span></span></td>
<td><span data-ttu-id="9c100-192">Pull</span><span class="sxs-lookup"><span data-stu-id="9c100-192">Pull</span></span></td>
<td><span data-ttu-id="9c100-193">Pull erstellen</span><span class="sxs-lookup"><span data-stu-id="9c100-193">Make a pull</span></span>
<ul>
<li><span data-ttu-id="9c100-194">Bei Fehler "Gehe zu Ende"</span><span class="sxs-lookup"><span data-stu-id="9c100-194">On failure go to End</span></span></li>
<li><span data-ttu-id="9c100-195">Bei Erfolg und synchrone Vervollständigung mit bytes, die ungleich NULL sind, wechseln Sie zu P.</span><span class="sxs-lookup"><span data-stu-id="9c100-195">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="9c100-196">Bei Erfolg und synchronen Abschluss mit NULL gelesenen Bytes (null-Pull) gehe zu wcomp</span><span class="sxs-lookup"><span data-stu-id="9c100-196">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="9c100-197">Bei Erfolg und asynchroner Beendigung (ERROR_IO_PENDING wird zurückgegeben) gehe zu WP</span><span class="sxs-lookup"><span data-stu-id="9c100-197">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="9c100-198">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="9c100-198">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-199">WP</span><span class="sxs-lookup"><span data-stu-id="9c100-199">WP</span></span></td>
<td><span data-ttu-id="9c100-200">Auf Pull warten</span><span class="sxs-lookup"><span data-stu-id="9c100-200">Wait for Pull</span></span></td>
<td><span data-ttu-id="9c100-201">Auf Benachrichtigung warten</span><span class="sxs-lookup"><span data-stu-id="9c100-201">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="9c100-202">Bei einem Fehler, der abgeschlossen werden kann, gehen Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-202">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="9c100-203">Wenn ein Fehler " <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> " empfangen wird, gehen Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-203">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="9c100-204">Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit Bytes ungleich 0 (null) empfangen wird, gehen Sie zu "P".</span><span class="sxs-lookup"><span data-stu-id="9c100-204">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="9c100-205">Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit 0 (null) Bytes empfangen wird (null-Pull), wechseln Sie zu comp.</span><span class="sxs-lookup"><span data-stu-id="9c100-205">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="9c100-206">Wenn ein Fehler aufgetreten ist, können Sie</span><span class="sxs-lookup"><span data-stu-id="9c100-206">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="9c100-207">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="9c100-207">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-208">Kann</span><span class="sxs-lookup"><span data-stu-id="9c100-208">Can</span></span></td>
<td><span data-ttu-id="9c100-209">Abbrechen des Aufrufes</span><span class="sxs-lookup"><span data-stu-id="9c100-209">Cancel the Call</span></span></td>
<td><span data-ttu-id="9c100-210">Aufrufen von <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>rpcasynccancelcallgo</strong></a>zu wcomp</span><span class="sxs-lookup"><span data-stu-id="9c100-210">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-211">Wcomp</span><span class="sxs-lookup"><span data-stu-id="9c100-211">WComp</span></span></td>
<td><span data-ttu-id="9c100-212">Auf Abschluss warten</span><span class="sxs-lookup"><span data-stu-id="9c100-212">Wait for Completion</span></span></td>
<td><span data-ttu-id="9c100-213">Warten Sie auf eine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="9c100-213">Wait for notification.</span></span> <span data-ttu-id="9c100-214">Eine Benachrichtigung zum Abschluss des Aufrufes sollte empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="9c100-214">Call-complete notification should be received.</span></span><br/> <span data-ttu-id="9c100-215">Gehe zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-215">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-216">Zuschreiben</span><span class="sxs-lookup"><span data-stu-id="9c100-216">Comp</span></span></td>
<td><span data-ttu-id="9c100-217">Completion</span><span class="sxs-lookup"><span data-stu-id="9c100-217">Completion</span></span></td>
<td><span data-ttu-id="9c100-218">Problem " <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcasynccompletecallgo</strong></a>to End"</span><span class="sxs-lookup"><span data-stu-id="9c100-218">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-219">Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-219">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="9c100-220">Server Verhalten</span><span class="sxs-lookup"><span data-stu-id="9c100-220">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c100-221">State</span><span class="sxs-lookup"><span data-stu-id="9c100-221">State</span></span></th>
<th><span data-ttu-id="9c100-222">Name des Staats</span><span class="sxs-lookup"><span data-stu-id="9c100-222">State Name</span></span></th>
<th><span data-ttu-id="9c100-223">Aktion</span><span class="sxs-lookup"><span data-stu-id="9c100-223">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c100-224">D</span><span class="sxs-lookup"><span data-stu-id="9c100-224">D</span></span></td>
<td><span data-ttu-id="9c100-225">Dispatch</span><span class="sxs-lookup"><span data-stu-id="9c100-225">Dispatch</span></span></td>
<td><span data-ttu-id="9c100-226">Der Aufruf wird von der RPC-Laufzeit an "P" gesendet.</span><span class="sxs-lookup"><span data-stu-id="9c100-226">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="9c100-227">So führen Sie einen fehlerhaften Fehler (während der Ausführung im RPC-Thread) aus: Ausnahme auslösen; Gehe zu Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-227">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="9c100-228">So führen Sie einen fehlerhaften Fehler aus: Gehe zu A</span><span class="sxs-lookup"><span data-stu-id="9c100-228">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-229">P</span><span class="sxs-lookup"><span data-stu-id="9c100-229">P</span></span></td>
<td><span data-ttu-id="9c100-230">Push</span><span class="sxs-lookup"><span data-stu-id="9c100-230">Push</span></span></td>
<td><span data-ttu-id="9c100-231">Push tätigen</span><span class="sxs-lookup"><span data-stu-id="9c100-231">Make a push</span></span>
<ul>
<li><span data-ttu-id="9c100-232">Bei Erfolg gehe zu WP</span><span class="sxs-lookup"><span data-stu-id="9c100-232">On success go to WP</span></span></li>
<li><span data-ttu-id="9c100-233">Bei Fehler "Gehe zu Ende"</span><span class="sxs-lookup"><span data-stu-id="9c100-233">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="9c100-234">Fehler: Wechseln Sie zu einem</span><span class="sxs-lookup"><span data-stu-id="9c100-234">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-235">WP</span><span class="sxs-lookup"><span data-stu-id="9c100-235">WP</span></span></td>
<td><span data-ttu-id="9c100-236">Auf Push warten</span><span class="sxs-lookup"><span data-stu-id="9c100-236">Wait for Push</span></span></td>
<td><span data-ttu-id="9c100-237">Auf Benachrichtigung warten</span><span class="sxs-lookup"><span data-stu-id="9c100-237">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="9c100-238">Wenn Sie einen Abschluss erhalten, wechseln Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-238">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="9c100-239">Wenn ein Erfolg von <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> empfangen wird und weitere Daten gesendet werden müssen, gehen Sie zu P.</span><span class="sxs-lookup"><span data-stu-id="9c100-239">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="9c100-240">Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> -Vorgang empfangen wird und weitere Daten nicht gesendet werden müssen, gehen Sie zu NP.</span><span class="sxs-lookup"><span data-stu-id="9c100-240">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="9c100-241">Wenn ein Fehler auftritt, gehen Sie zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-241">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="9c100-242">Fehler: Wechseln Sie zu einem</span><span class="sxs-lookup"><span data-stu-id="9c100-242">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-243">NP</span><span class="sxs-lookup"><span data-stu-id="9c100-243">NP</span></span></td>
<td><span data-ttu-id="9c100-244">NULL-Push</span><span class="sxs-lookup"><span data-stu-id="9c100-244">Null Push</span></span></td>
<td><span data-ttu-id="9c100-245">Push 0 Bytes</span><span class="sxs-lookup"><span data-stu-id="9c100-245">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="9c100-246">bei Erfolg gehe zu wnp</span><span class="sxs-lookup"><span data-stu-id="9c100-246">on success go to WNP</span></span></li>
<li><span data-ttu-id="9c100-247">bei Fehler wechseln Sie zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-247">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="9c100-248">Fehler: Wechseln Sie zu einem</span><span class="sxs-lookup"><span data-stu-id="9c100-248">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-249">Wnp</span><span class="sxs-lookup"><span data-stu-id="9c100-249">WNP</span></span></td>
<td><span data-ttu-id="9c100-250">Auf NULL-Push warten</span><span class="sxs-lookup"><span data-stu-id="9c100-250">Wait for Null Push</span></span></td>
<td><span data-ttu-id="9c100-251">Auf Benachrichtigung warten</span><span class="sxs-lookup"><span data-stu-id="9c100-251">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="9c100-252">Wenn Sie einen Abschluss erhalten, wechseln Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-252">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="9c100-253">Wenn ein Fehler auftritt, gehen Sie zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-253">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="9c100-254">Wenn eine Erfolgsmeldung empfangen wird, gehen Sie zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-254">If a success is received go Comp</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-255">A</span><span class="sxs-lookup"><span data-stu-id="9c100-255">A</span></span></td>
<td><span data-ttu-id="9c100-256">Abbrechen des Aufrufes</span><span class="sxs-lookup"><span data-stu-id="9c100-256">Abort the Call</span></span></td>
<td><span data-ttu-id="9c100-257"><a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>Rpcasyncabortcall;</strong></a>aufzurufen Gehe zu Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-257">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-258">Zuschreiben</span><span class="sxs-lookup"><span data-stu-id="9c100-258">Comp</span></span></td>
<td><span data-ttu-id="9c100-259">Completion</span><span class="sxs-lookup"><span data-stu-id="9c100-259">Completion</span></span></td>
<td><span data-ttu-id="9c100-260">Problem " <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall;</strong></a>" Gehe zu Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-260">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-261">Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-261">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a><span data-ttu-id="9c100-262">IN-Out-Pipe</span><span class="sxs-lookup"><span data-stu-id="9c100-262">IN-OUT Pipe</span></span>

<span data-ttu-id="9c100-263">Client Verhalten</span><span class="sxs-lookup"><span data-stu-id="9c100-263">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c100-264">State</span><span class="sxs-lookup"><span data-stu-id="9c100-264">State</span></span></th>
<th><span data-ttu-id="9c100-265">Name des Staats</span><span class="sxs-lookup"><span data-stu-id="9c100-265">State Name</span></span></th>
<th><span data-ttu-id="9c100-266">Aktion</span><span class="sxs-lookup"><span data-stu-id="9c100-266">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c100-267">C</span><span class="sxs-lookup"><span data-stu-id="9c100-267">C</span></span></td>
<td><span data-ttu-id="9c100-268">Ausführen des Aufrufes</span><span class="sxs-lookup"><span data-stu-id="9c100-268">Make the call</span></span></td>
<td><span data-ttu-id="9c100-269">Erstellen des RPC</span><span class="sxs-lookup"><span data-stu-id="9c100-269">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="9c100-270">Bei Erfolg gehe zu WS</span><span class="sxs-lookup"><span data-stu-id="9c100-270">On success go to WS</span></span></li>
<li><span data-ttu-id="9c100-271">Bei Ausnahme gehe zu Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-271">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="9c100-272">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="9c100-272">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-273">PS</span><span class="sxs-lookup"><span data-stu-id="9c100-273">PS</span></span></td>
<td><span data-ttu-id="9c100-274">Push</span><span class="sxs-lookup"><span data-stu-id="9c100-274">Push</span></span></td>
<td><span data-ttu-id="9c100-275">Push tätigen</span><span class="sxs-lookup"><span data-stu-id="9c100-275">Make a push</span></span>
<ul>
<li><span data-ttu-id="9c100-276">Bei Fehler "Gehe zu Ende"</span><span class="sxs-lookup"><span data-stu-id="9c100-276">On failure go to End</span></span></li>
<li><span data-ttu-id="9c100-277">Bei Erfolg gehe zu WS</span><span class="sxs-lookup"><span data-stu-id="9c100-277">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="9c100-278">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="9c100-278">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-279">WS</span><span class="sxs-lookup"><span data-stu-id="9c100-279">WS</span></span></td>
<td><span data-ttu-id="9c100-280">Auf senden warten</span><span class="sxs-lookup"><span data-stu-id="9c100-280">Wait for Send</span></span></td>
<td><span data-ttu-id="9c100-281">Auf Benachrichtigung warten</span><span class="sxs-lookup"><span data-stu-id="9c100-281">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="9c100-282">Wenn Sie eine Benachrichtigung erhalten, gehen Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-282">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="9c100-283">Wenn ein Erfolg von <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> empfangen wird und weitere Daten gesendet werden müssen, gehen Sie zu PS</span><span class="sxs-lookup"><span data-stu-id="9c100-283">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="9c100-284">Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> -Vorgang empfangen wird und weitere Daten nicht gesendet werden müssen, gehen Sie zu NP.</span><span class="sxs-lookup"><span data-stu-id="9c100-284">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="9c100-285">Wenn ein Fehler " <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpccallcomplete</strong></a> " empfangen wird, gehen Sie zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-285">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="9c100-286">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="9c100-286">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-287">NP</span><span class="sxs-lookup"><span data-stu-id="9c100-287">NP</span></span></td>
<td><span data-ttu-id="9c100-288">NULL-Push</span><span class="sxs-lookup"><span data-stu-id="9c100-288">Null Push</span></span></td>
<td><span data-ttu-id="9c100-289">Push 0 bytes (null Push)</span><span class="sxs-lookup"><span data-stu-id="9c100-289">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="9c100-290">Bei Fehler "Gehe zu Ende"</span><span class="sxs-lookup"><span data-stu-id="9c100-290">On failure go to End</span></span></li>
<li><span data-ttu-id="9c100-291">Bei Erfolg gehe zu PL</span><span class="sxs-lookup"><span data-stu-id="9c100-291">On success go to PL</span></span></li>
</ul>
<span data-ttu-id="9c100-292">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="9c100-292">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-293">PL</span><span class="sxs-lookup"><span data-stu-id="9c100-293">PL</span></span></td>
<td><span data-ttu-id="9c100-294">Pull</span><span class="sxs-lookup"><span data-stu-id="9c100-294">Pull</span></span></td>
<td><span data-ttu-id="9c100-295">Pull erstellen</span><span class="sxs-lookup"><span data-stu-id="9c100-295">Make a pull</span></span>
<ul>
<li><span data-ttu-id="9c100-296">Bei Fehler "Gehe zu Ende"</span><span class="sxs-lookup"><span data-stu-id="9c100-296">On failure go to End</span></span></li>
<li><span data-ttu-id="9c100-297">Bei Erfolg und synchroner Abschluss mit bytes, die ungleich 0 (null) sind, gehe zu PL</span><span class="sxs-lookup"><span data-stu-id="9c100-297">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="9c100-298">Bei Erfolg und synchronen Abschluss mit NULL gelesenen Bytes (null-Pull) gehe zu wcomp</span><span class="sxs-lookup"><span data-stu-id="9c100-298">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="9c100-299">Bei Erfolg und asynchroner Beendigung (ERROR_IO_PENDING wird zurückgegeben) wechseln Sie zu WPL.</span><span class="sxs-lookup"><span data-stu-id="9c100-299">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="9c100-300">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="9c100-300">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-301">WPL</span><span class="sxs-lookup"><span data-stu-id="9c100-301">WPL</span></span></td>
<td><span data-ttu-id="9c100-302">Auf Pull warten</span><span class="sxs-lookup"><span data-stu-id="9c100-302">Wait for Pull</span></span></td>
<td><span data-ttu-id="9c100-303">Auf Benachrichtigung warten</span><span class="sxs-lookup"><span data-stu-id="9c100-303">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="9c100-304">Bei einem Fehler, der abgeschlossen werden kann, gehen Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-304">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="9c100-305">Wenn ein Fehler " <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> " empfangen wird, gehen Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-305">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="9c100-306">Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit Bytes ungleich 0 (null) empfangen wird, gehen Sie zu pl.</span><span class="sxs-lookup"><span data-stu-id="9c100-306">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="9c100-307">Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit 0 (null) Bytes empfangen wird, gehen Sie zu comp.</span><span class="sxs-lookup"><span data-stu-id="9c100-307">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to Comp</span></span></li>
<li><span data-ttu-id="9c100-308">Wenn ein Fehler aufgetreten ist, können Sie</span><span class="sxs-lookup"><span data-stu-id="9c100-308">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="9c100-309">Fehler: Gehe zu</span><span class="sxs-lookup"><span data-stu-id="9c100-309">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-310">Kann</span><span class="sxs-lookup"><span data-stu-id="9c100-310">Can</span></span></td>
<td><span data-ttu-id="9c100-311">Abbrechen des Aufrufes</span><span class="sxs-lookup"><span data-stu-id="9c100-311">Cancel the Call</span></span></td>
<td><span data-ttu-id="9c100-312">Aufrufen von <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>rpcasynccancelcallgo</strong></a>zu wcomp</span><span class="sxs-lookup"><span data-stu-id="9c100-312">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-313">Wcomp</span><span class="sxs-lookup"><span data-stu-id="9c100-313">WComp</span></span></td>
<td><span data-ttu-id="9c100-314">Auf Abschluss warten</span><span class="sxs-lookup"><span data-stu-id="9c100-314">Wait for Completion</span></span></td>
<td><span data-ttu-id="9c100-315">Warten Sie auf eine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="9c100-315">Wait for notification.</span></span> <span data-ttu-id="9c100-316">Die callcomplete-Benachrichtigung sollte empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="9c100-316">CallComplete notification should be received.</span></span><br/> <span data-ttu-id="9c100-317">Gehe zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-317">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-318">Zuschreiben</span><span class="sxs-lookup"><span data-stu-id="9c100-318">Comp</span></span></td>
<td><span data-ttu-id="9c100-319">Completion</span><span class="sxs-lookup"><span data-stu-id="9c100-319">Completion</span></span></td>
<td><span data-ttu-id="9c100-320">Problem " <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>rpcasynccompletecallgo</strong></a>to End"</span><span class="sxs-lookup"><span data-stu-id="9c100-320">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-321">Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-321">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="9c100-322">Server Verhalten</span><span class="sxs-lookup"><span data-stu-id="9c100-322">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c100-323">State</span><span class="sxs-lookup"><span data-stu-id="9c100-323">State</span></span></th>
<th><span data-ttu-id="9c100-324">Name des Staats</span><span class="sxs-lookup"><span data-stu-id="9c100-324">State Name</span></span></th>
<th><span data-ttu-id="9c100-325">Aktion</span><span class="sxs-lookup"><span data-stu-id="9c100-325">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c100-326">D</span><span class="sxs-lookup"><span data-stu-id="9c100-326">D</span></span></td>
<td><span data-ttu-id="9c100-327">Dispatch</span><span class="sxs-lookup"><span data-stu-id="9c100-327">Dispatch</span></span></td>
<td><span data-ttu-id="9c100-328">Der Aufruf wird vom RPC-runtimego an pl gesendet.</span><span class="sxs-lookup"><span data-stu-id="9c100-328">The call is dispatched by the RPC runtimeGo to PL</span></span><br/> <span data-ttu-id="9c100-329">So führen Sie einen fehlerhaften Fehler (während der Ausführung im RPC-Thread) aus: Ausnahme auslösen; Gehe zu Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-329">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="9c100-330">So führen Sie einen fehlerhaften Fehler aus: Gehe zu A</span><span class="sxs-lookup"><span data-stu-id="9c100-330">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-331">PL</span><span class="sxs-lookup"><span data-stu-id="9c100-331">PL</span></span></td>
<td><span data-ttu-id="9c100-332">Pull</span><span class="sxs-lookup"><span data-stu-id="9c100-332">Pull</span></span></td>
<td><span data-ttu-id="9c100-333">Pull erstellen</span><span class="sxs-lookup"><span data-stu-id="9c100-333">Make a pull</span></span>
<ul>
<li><span data-ttu-id="9c100-334">Bei Fehler "Gehe zu Ende"</span><span class="sxs-lookup"><span data-stu-id="9c100-334">On failure go to End</span></span></li>
<li><span data-ttu-id="9c100-335">Bei Erfolg und synchroner Abschluss mit bytes, die ungleich 0 (null) sind, gehe zu PL</span><span class="sxs-lookup"><span data-stu-id="9c100-335">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="9c100-336">Bei Erfolg und synchroner Abschluss mit NULL gelesenen Bytes (null-Pull) gehe zu PS</span><span class="sxs-lookup"><span data-stu-id="9c100-336">On success and synchronous completion with zero bytes read (null pull) go to PS</span></span></li>
<li><span data-ttu-id="9c100-337">Bei Erfolg und asynchroner Beendigung (ERROR_IO_PENDING wird zurückgegeben) wechseln Sie zu WPL.</span><span class="sxs-lookup"><span data-stu-id="9c100-337">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="9c100-338">Fehler: Wechseln Sie zu einem</span><span class="sxs-lookup"><span data-stu-id="9c100-338">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-339">WPL</span><span class="sxs-lookup"><span data-stu-id="9c100-339">WPL</span></span></td>
<td><span data-ttu-id="9c100-340">Auf Pull warten</span><span class="sxs-lookup"><span data-stu-id="9c100-340">Wait for Pull</span></span></td>
<td><span data-ttu-id="9c100-341">Auf Benachrichtigung warten</span><span class="sxs-lookup"><span data-stu-id="9c100-341">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="9c100-342">Wenn Sie einen Abschluss erhalten, wechseln Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-342">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="9c100-343">Wenn ein Fehler " <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> " empfangen wird, wechseln Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-343">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="9c100-344">Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit Bytes ungleich 0 (null) empfangen wird, gehen Sie zu pl.</span><span class="sxs-lookup"><span data-stu-id="9c100-344">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="9c100-345">Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcreceivecomplete</strong></a> -Vorgang mit 0 (null) Bytes empfangen wird, gehen Sie zu PS</span><span class="sxs-lookup"><span data-stu-id="9c100-345">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to PS</span></span></li>
<li><span data-ttu-id="9c100-346">Wenn ein Fehler auftritt, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="9c100-346">If a failure is received go A</span></span></li>
</ul>
<span data-ttu-id="9c100-347">Fehler: Wechseln Sie zu einem</span><span class="sxs-lookup"><span data-stu-id="9c100-347">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-348">PS</span><span class="sxs-lookup"><span data-stu-id="9c100-348">PS</span></span></td>
<td><span data-ttu-id="9c100-349">Push</span><span class="sxs-lookup"><span data-stu-id="9c100-349">Push</span></span></td>
<td><span data-ttu-id="9c100-350">Push tätigen</span><span class="sxs-lookup"><span data-stu-id="9c100-350">Make a push</span></span>
<ul>
<li><span data-ttu-id="9c100-351">Bei Erfolg gehe zu WPS</span><span class="sxs-lookup"><span data-stu-id="9c100-351">On success go to WPS</span></span></li>
<li><span data-ttu-id="9c100-352">Bei Fehler "Gehe zu Ende"</span><span class="sxs-lookup"><span data-stu-id="9c100-352">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="9c100-353">Fehler: Wechseln Sie zu einem</span><span class="sxs-lookup"><span data-stu-id="9c100-353">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-354">WPS</span><span class="sxs-lookup"><span data-stu-id="9c100-354">WPS</span></span></td>
<td><span data-ttu-id="9c100-355">Auf Push warten</span><span class="sxs-lookup"><span data-stu-id="9c100-355">Wait for Push</span></span></td>
<td><span data-ttu-id="9c100-356">Auf Benachrichtigung warten</span><span class="sxs-lookup"><span data-stu-id="9c100-356">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="9c100-357">Wenn Sie einen Abschluss erhalten, wechseln Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-357">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="9c100-358">Wenn ein Erfolg von <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> empfangen wird und weitere Daten gesendet werden müssen, gehen Sie zu PS</span><span class="sxs-lookup"><span data-stu-id="9c100-358">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="9c100-359">Wenn ein erfolgreicher <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcsendcomplete</strong></a> -Vorgang empfangen wird und weitere Daten nicht gesendet werden müssen, gehen Sie zu NP.</span><span class="sxs-lookup"><span data-stu-id="9c100-359">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="9c100-360">Wenn ein Fehler auftritt, gehen Sie zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-360">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="9c100-361">Fehler: Wechseln Sie zu einem</span><span class="sxs-lookup"><span data-stu-id="9c100-361">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-362">NP</span><span class="sxs-lookup"><span data-stu-id="9c100-362">NP</span></span></td>
<td><span data-ttu-id="9c100-363">NULL-Push</span><span class="sxs-lookup"><span data-stu-id="9c100-363">Null Push</span></span></td>
<td><span data-ttu-id="9c100-364">Push 0 Bytes</span><span class="sxs-lookup"><span data-stu-id="9c100-364">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="9c100-365">bei Erfolg gehe zu wnp</span><span class="sxs-lookup"><span data-stu-id="9c100-365">on success go to WNP</span></span></li>
<li><span data-ttu-id="9c100-366">bei Fehler wechseln Sie zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-366">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="9c100-367">Fehler: Wechseln Sie zu einem</span><span class="sxs-lookup"><span data-stu-id="9c100-367">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-368">Wnp</span><span class="sxs-lookup"><span data-stu-id="9c100-368">WNP</span></span></td>
<td><span data-ttu-id="9c100-369">Auf NULL-Push warten</span><span class="sxs-lookup"><span data-stu-id="9c100-369">Wait for Null Push</span></span></td>
<td><span data-ttu-id="9c100-370">Auf Benachrichtigung warten</span><span class="sxs-lookup"><span data-stu-id="9c100-370">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="9c100-371">Wenn Sie einen Abschluss erhalten, wechseln Sie zu</span><span class="sxs-lookup"><span data-stu-id="9c100-371">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="9c100-372">Wenn ein Fehler auftritt, gehen Sie zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-372">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="9c100-373">Wenn eine Erfolgsmeldung empfangen wird, gehen Sie zu Comp</span><span class="sxs-lookup"><span data-stu-id="9c100-373">If a success is received go Comp</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-374">A</span><span class="sxs-lookup"><span data-stu-id="9c100-374">A</span></span></td>
<td><span data-ttu-id="9c100-375">Abbrechen des Aufrufes</span><span class="sxs-lookup"><span data-stu-id="9c100-375">Abort the Call</span></span></td>
<td><span data-ttu-id="9c100-376"><a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>Rpcasyncabortcall;</strong></a>aufzurufen Gehe zu Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-376">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c100-377">Zuschreiben</span><span class="sxs-lookup"><span data-stu-id="9c100-377">Comp</span></span></td>
<td><span data-ttu-id="9c100-378">Completion</span><span class="sxs-lookup"><span data-stu-id="9c100-378">Completion</span></span></td>
<td><span data-ttu-id="9c100-379">Problem " <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall;</strong></a>" Gehe zu Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-379">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c100-380">Ende</span><span class="sxs-lookup"><span data-stu-id="9c100-380">End</span></span></td>


</tr>
</tbody>
</table>



 

 

 





