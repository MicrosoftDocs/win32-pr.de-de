---
description: Es gibt mehrere Typen von Abfragen, die zum Abfragen des Status von Ressourcen entworfen wurden.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Abfragen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859974"
---
# <a name="queries-direct3d-9"></a><span data-ttu-id="fc654-103">Abfragen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fc654-103">Queries (Direct3D 9)</span></span>

<span data-ttu-id="fc654-104">Es gibt mehrere Typen von Abfragen, die zum Abfragen des Status von Ressourcen entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="fc654-104">There are several types of queries which are designed to query the status of resources.</span></span> <span data-ttu-id="fc654-105">Der Status einer bestimmten Ressource umfasst den GPU-Status (Graphics Processing Unit), den Treiber Status oder den Lauf Zeit Status.</span><span class="sxs-lookup"><span data-stu-id="fc654-105">The status of a given resource includes graphics processing unit (GPU) status, driver status, or runtime status.</span></span> <span data-ttu-id="fc654-106">Um den Unterschied zwischen den unterschiedlichen Abfrage Typen zu verstehen, müssen Sie die Abfrage Zustände verstehen.</span><span class="sxs-lookup"><span data-stu-id="fc654-106">To understand the difference between the different query types, you need to understand the query states.</span></span> <span data-ttu-id="fc654-107">Im folgenden Zustands Übergangs Diagramm werden die einzelnen Abfrage Zustände erläutert.</span><span class="sxs-lookup"><span data-stu-id="fc654-107">The following state transition diagram explains each of the query states.</span></span>

![Diagramm zur Darstellung von Übergängen zwischen Abfrage Zuständen](images/queries.png)

<span data-ttu-id="fc654-109">Das Diagramm zeigt drei Zustände, die jeweils durch Kreise definiert werden.</span><span class="sxs-lookup"><span data-stu-id="fc654-109">The diagram shows three states, each defined by circles.</span></span> <span data-ttu-id="fc654-110">Jede der vollwertigen Linien sind Anwendungs gesteuerte Ereignisse, die einen Zustandsübergang verursachen.</span><span class="sxs-lookup"><span data-stu-id="fc654-110">Each of the solid lines are application-driven events that cause a state transition.</span></span> <span data-ttu-id="fc654-111">Die gestrichelte Linie ist ein Ressourcen gesteuertes Ereignis, das eine Abfrage aus dem ausgestellten Zustand in den signalisierten Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="fc654-111">The dashed line is a resource-driven event that switches a query from the issued state to the signaled state.</span></span> <span data-ttu-id="fc654-112">Jeder dieser Zustände hat einen anderen Zweck:</span><span class="sxs-lookup"><span data-stu-id="fc654-112">Each of these states has a different purpose:</span></span>

-   <span data-ttu-id="fc654-113">Der Status "signalisiert" ähnelt einem Leerlaufzustand.</span><span class="sxs-lookup"><span data-stu-id="fc654-113">The signaled state is like an idle state.</span></span> <span data-ttu-id="fc654-114">Das Query-Objekt wurde generiert und wartet darauf, dass die Anwendung die Abfrage ausgibt.</span><span class="sxs-lookup"><span data-stu-id="fc654-114">The query object has been generated and is waiting for the application to issue the query.</span></span> <span data-ttu-id="fc654-115">Nachdem eine Abfrage abgeschlossen und in den signalisierten Zustand umgestellt wurde, kann die Antwort auf die Abfrage abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fc654-115">Once a query has completed and transitioned back to the signaled state, the answer to the query can be retrieved.</span></span>
-   <span data-ttu-id="fc654-116">Der erstellungstatus ist wie ein Stagingbereich für eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="fc654-116">The building state is like a staging area for a query.</span></span> <span data-ttu-id="fc654-117">Aus dem Erteilungs Status wurde eine Abfrage ausgegeben (durch Aufrufen von [**D3DISSUE \_ Begin**](d3dissue-begin.md)), hat sich jedoch noch nicht in den ausgestellten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="fc654-117">From the building state, a query has been issued (by calling [**D3DISSUE\_BEGIN**](d3dissue-begin.md)) but has not yet transitioned to the issued state.</span></span> <span data-ttu-id="fc654-118">Wenn eine Anwendung ein Abfrage Ende ausgibt (durch Aufrufen von [**D3DISSUE \_ End**](d3dissue-end.md)), wechselt die Abfrage in den ausgegebene Zustand.</span><span class="sxs-lookup"><span data-stu-id="fc654-118">When an application issues a query end (by calling [**D3DISSUE\_END**](d3dissue-end.md)), the query transitions to the issued state.</span></span>
-   <span data-ttu-id="fc654-119">Der ausgegebene Zustand bedeutet, dass die Abfrage, die abgefragt wird, die Abfrage steuert.</span><span class="sxs-lookup"><span data-stu-id="fc654-119">The issued state means that the resource being queried has control of the query.</span></span> <span data-ttu-id="fc654-120">Sobald die Ressource abgeschlossen ist, überträgt die Ressource den Zustands Automat in den signalisierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="fc654-120">Once the resource finishes its work, the resource transitions the state machine to the signaled state.</span></span> <span data-ttu-id="fc654-121">Während des ausgestellten Zustands muss die Anwendung Abfragen, um den Übergang in den signalisierten Zustand zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="fc654-121">During the issued state, the application must poll to detect the transition to the signaled state.</span></span> <span data-ttu-id="fc654-122">Nachdem der Übergang in den signalisierten Zustand erfolgt ist, gibt [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) das Abfrageergebnis (über ein Argument) an die Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="fc654-122">Once the transition to the signaled state occurs, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns the query result (through an argument) to the application.</span></span>

<span data-ttu-id="fc654-123">In der folgenden Tabelle sind die verfügbaren Abfrage Typen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fc654-123">The following table lists the available query types.</span></span>



| <span data-ttu-id="fc654-124">Abfragetyp</span><span class="sxs-lookup"><span data-stu-id="fc654-124">Query Type</span></span>        | <span data-ttu-id="fc654-125">Problem Ereignis</span><span class="sxs-lookup"><span data-stu-id="fc654-125">Issue Event</span></span>                                                                      | <span data-ttu-id="fc654-126">GetData-Puffer</span><span class="sxs-lookup"><span data-stu-id="fc654-126">GetData buffer</span></span>                                                              | <span data-ttu-id="fc654-127">Typ</span><span class="sxs-lookup"><span data-stu-id="fc654-127">Runtime</span></span>      | <span data-ttu-id="fc654-128">Impliziter Beginn der Abfrage</span><span class="sxs-lookup"><span data-stu-id="fc654-128">Implicit beginning of query</span></span>                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| <span data-ttu-id="fc654-129">Bandwidthtimings</span><span class="sxs-lookup"><span data-stu-id="fc654-129">BANDWIDTHTIMINGS</span></span>  | <span data-ttu-id="fc654-130">[**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="fc654-130">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="fc654-131">**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="fc654-131">**D3DDEVINFO\_D3D9BANDWIDTHTIMINGS**</span></span>](d3ddevinfo-d3d9bandwidthtimings.md) | <span data-ttu-id="fc654-132">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="fc654-132">Retail/Debug</span></span> | <span data-ttu-id="fc654-133">–</span><span class="sxs-lookup"><span data-stu-id="fc654-133">N/A</span></span>                                              |
| <span data-ttu-id="fc654-134">Cacheutilization</span><span class="sxs-lookup"><span data-stu-id="fc654-134">CACHEUTILIZATION</span></span>  | <span data-ttu-id="fc654-135">[**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="fc654-135">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="fc654-136">**D3DDEVINFO \_ D3D9CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="fc654-136">**D3DDEVINFO\_D3D9CACHEUTILIZATION**</span></span>](d3ddevinfo-d3d9cacheutilization.md) | <span data-ttu-id="fc654-137">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="fc654-137">Retail/Debug</span></span> | <span data-ttu-id="fc654-138">–</span><span class="sxs-lookup"><span data-stu-id="fc654-138">N/A</span></span>                                              |
| <span data-ttu-id="fc654-139">EREIGNIS</span><span class="sxs-lookup"><span data-stu-id="fc654-139">EVENT</span></span>             | [<span data-ttu-id="fc654-140">**D3DISSUE \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="fc654-140">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="fc654-141">BOOL</span><span class="sxs-lookup"><span data-stu-id="fc654-141">BOOL</span></span>                                                                        | <span data-ttu-id="fc654-142">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="fc654-142">Retail/Debug</span></span> | [<span data-ttu-id="fc654-143">**"Kreatedevice"**</span><span class="sxs-lookup"><span data-stu-id="fc654-143">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="fc654-144">Interfacetimings</span><span class="sxs-lookup"><span data-stu-id="fc654-144">INTERFACETIMINGS</span></span>  | <span data-ttu-id="fc654-145">[**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="fc654-145">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="fc654-146">**D3DDEVINFO \_ D3D9INTERFACETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="fc654-146">**D3DDEVINFO\_D3D9INTERFACETIMINGS**</span></span>](d3ddevinfo-d3d9interfacetimings.md) | <span data-ttu-id="fc654-147">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="fc654-147">Retail/Debug</span></span> | <span data-ttu-id="fc654-148">–</span><span class="sxs-lookup"><span data-stu-id="fc654-148">N/A</span></span>                                              |
| <span data-ttu-id="fc654-149">Okklusions</span><span class="sxs-lookup"><span data-stu-id="fc654-149">OCCLUSION</span></span>         | <span data-ttu-id="fc654-150">[**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="fc654-150">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="fc654-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="fc654-151">DWORD</span></span>                                                                       | <span data-ttu-id="fc654-152">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="fc654-152">Retail/Debug</span></span> | <span data-ttu-id="fc654-153">–</span><span class="sxs-lookup"><span data-stu-id="fc654-153">N/A</span></span>                                              |
| <span data-ttu-id="fc654-154">Pipelinetimings</span><span class="sxs-lookup"><span data-stu-id="fc654-154">PIPELINETIMINGS</span></span>   | <span data-ttu-id="fc654-155">[**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="fc654-155">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="fc654-156">**D3DDEVINFO \_ D3D9PIPELINETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="fc654-156">**D3DDEVINFO\_D3D9PIPELINETIMINGS**</span></span>](d3ddevinfo-d3d9pipelinetimings.md)   | <span data-ttu-id="fc654-157">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="fc654-157">Retail/Debug</span></span> | <span data-ttu-id="fc654-158">–</span><span class="sxs-lookup"><span data-stu-id="fc654-158">N/A</span></span>                                              |
| <span data-ttu-id="fc654-159">RESOURCEMANAGER</span><span class="sxs-lookup"><span data-stu-id="fc654-159">RESOURCEMANAGER</span></span>   | [<span data-ttu-id="fc654-160">**D3DISSUE \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="fc654-160">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="fc654-161">**D3DDEVINFO \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="fc654-161">**D3DDEVINFO\_ResourceManager**</span></span>](d3ddevinfo-resourcemanager.md)           | <span data-ttu-id="fc654-162">Nur Debuggen</span><span class="sxs-lookup"><span data-stu-id="fc654-162">Debug only</span></span>   | [<span data-ttu-id="fc654-163">**Anzahl**</span><span class="sxs-lookup"><span data-stu-id="fc654-163">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="fc654-164">timestamp</span><span class="sxs-lookup"><span data-stu-id="fc654-164">TIMESTAMP</span></span>         | [<span data-ttu-id="fc654-165">**D3DISSUE \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="fc654-165">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="fc654-166">UINT64</span><span class="sxs-lookup"><span data-stu-id="fc654-166">UINT64</span></span>                                                                      | <span data-ttu-id="fc654-167">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="fc654-167">Retail/Debug</span></span> | <span data-ttu-id="fc654-168">–</span><span class="sxs-lookup"><span data-stu-id="fc654-168">N/A</span></span>                                              |
| <span data-ttu-id="fc654-169">Timestampdisjoint</span><span class="sxs-lookup"><span data-stu-id="fc654-169">TIMESTAMPDISJOINT</span></span> | <span data-ttu-id="fc654-170">[**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="fc654-170">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="fc654-171">BOOL</span><span class="sxs-lookup"><span data-stu-id="fc654-171">BOOL</span></span>                                                                        | <span data-ttu-id="fc654-172">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="fc654-172">Retail/Debug</span></span> | <span data-ttu-id="fc654-173">–</span><span class="sxs-lookup"><span data-stu-id="fc654-173">N/A</span></span>                                              |
| <span data-ttu-id="fc654-174">Timestampfreq</span><span class="sxs-lookup"><span data-stu-id="fc654-174">TIMESTAMPFREQ</span></span>     | [<span data-ttu-id="fc654-175">**D3DISSUE \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="fc654-175">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="fc654-176">UINT64</span><span class="sxs-lookup"><span data-stu-id="fc654-176">UINT64</span></span>                                                                      | <span data-ttu-id="fc654-177">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="fc654-177">Retail/Debug</span></span> | <span data-ttu-id="fc654-178">–</span><span class="sxs-lookup"><span data-stu-id="fc654-178">N/A</span></span>                                              |
| <span data-ttu-id="fc654-179">VCACHE</span><span class="sxs-lookup"><span data-stu-id="fc654-179">VCACHE</span></span>            | [<span data-ttu-id="fc654-180">**D3DISSUE \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="fc654-180">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="fc654-181">**D3DDEVINFO \_ VCACHE**</span><span class="sxs-lookup"><span data-stu-id="fc654-181">**D3DDEVINFO\_VCACHE**</span></span>](d3ddevinfo-vcache.md)                             | <span data-ttu-id="fc654-182">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="fc654-182">Retail/Debug</span></span> | [<span data-ttu-id="fc654-183">**"Kreatedevice"**</span><span class="sxs-lookup"><span data-stu-id="fc654-183">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="fc654-184">Vertexstats</span><span class="sxs-lookup"><span data-stu-id="fc654-184">VERTEXSTATS</span></span>       | [<span data-ttu-id="fc654-185">**D3DISSUE \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="fc654-185">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="fc654-186">**D3DDEVINFO \_ D3DVERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="fc654-186">**D3DDEVINFO\_D3DVERTEXSTATS**</span></span>](d3ddevinfo-d3dvertexstats.md)             | <span data-ttu-id="fc654-187">Nur Debuggen</span><span class="sxs-lookup"><span data-stu-id="fc654-187">Debug only</span></span>   | [<span data-ttu-id="fc654-188">**Anzahl**</span><span class="sxs-lookup"><span data-stu-id="fc654-188">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="fc654-189">Vertextierungen</span><span class="sxs-lookup"><span data-stu-id="fc654-189">VERTEXTIMINGS</span></span>     | <span data-ttu-id="fc654-190">[**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="fc654-190">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="fc654-191">**D3DDEVINFO \_ D3D9STAGETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="fc654-191">**D3DDEVINFO\_D3D9STAGETIMINGS**</span></span>](d3ddevinfo-d3d9stagetimings.md)         | <span data-ttu-id="fc654-192">Retail/Debug</span><span class="sxs-lookup"><span data-stu-id="fc654-192">Retail/Debug</span></span> | <span data-ttu-id="fc654-193">–</span><span class="sxs-lookup"><span data-stu-id="fc654-193">N/A</span></span>                                              |



 

<span data-ttu-id="fc654-194">Einige Abfragen erfordern ein Begin-und End-Ereignis, während andere nur ein End-Ereignis benötigen.</span><span class="sxs-lookup"><span data-stu-id="fc654-194">Some of the queries require a begin and end event, while others only require an end event.</span></span> <span data-ttu-id="fc654-195">Die Abfragen, die nur ein End-Ereignis erfordern, beginnen, wenn ein anderes impliziertes Ereignis auftritt (das in der Tabelle aufgelistet ist).</span><span class="sxs-lookup"><span data-stu-id="fc654-195">The queries that only require an end event begin when another implicit event occurs (which is listed in the table).</span></span> <span data-ttu-id="fc654-196">Alle Abfragen geben eine Antwort zurück, mit Ausnahme der Ereignis Abfrage, deren Antwort immer " **true**" ist.</span><span class="sxs-lookup"><span data-stu-id="fc654-196">All queries return an answer, except the event query whose answer is always **TRUE**.</span></span> <span data-ttu-id="fc654-197">Eine Anwendung verwendet entweder den Status der Abfrage oder den Rückgabecode von [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="fc654-197">An application uses either the state of the query or the return code of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>

## <a name="create-a-query"></a><span data-ttu-id="fc654-198">Erstellen einer Abfrage</span><span class="sxs-lookup"><span data-stu-id="fc654-198">Create a Query</span></span>

<span data-ttu-id="fc654-199">Bevor Sie eine Abfrage erstellen, können Sie überprüfen, ob die Laufzeit Abfragen unterstützt, indem Sie [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) mit einem **null** -Zeiger wie dem folgenden aufrufen:</span><span class="sxs-lookup"><span data-stu-id="fc654-199">Before you create a query, you can check to see if the runtime supports queries by calling [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) with a **NULL** pointer like this:</span></span>


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



<span data-ttu-id="fc654-200">Diese Methode gibt einen Erfolgs Code zurück, wenn eine Abfrage erstellt werden kann. Andernfalls wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fc654-200">This method returns a success code if a query can be created; otherwise it returns an error code.</span></span> <span data-ttu-id="fc654-201">Nach erfolgreicher Ausführung von " [**kreatequery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) " können Sie ein Abfrageobjekt wie folgt erstellen:</span><span class="sxs-lookup"><span data-stu-id="fc654-201">Once [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) succeeds, you can create a query object like this:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



<span data-ttu-id="fc654-202">Wenn dieser Befehl erfolgreich ausgeführt wird, wird ein Abfrageobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc654-202">If this call succeeds, a query object is created.</span></span> <span data-ttu-id="fc654-203">Die Abfrage befindet sich im Wesentlichen im Zustand "signalisiert" im Zustand "signalisiert" (mit einer nicht initialisierten Antwort) und wartet auf die Ausstellung.</span><span class="sxs-lookup"><span data-stu-id="fc654-203">The query is essentially idle in the signaled state (with an uninitialized answer) waiting to be issued.</span></span> <span data-ttu-id="fc654-204">Wenn Sie mit der Abfrage fertig sind, geben Sie Sie wie jede andere Schnittstelle frei.</span><span class="sxs-lookup"><span data-stu-id="fc654-204">When you are finished with the query, release it like any other interface.</span></span>

## <a name="issue-a-query"></a><span data-ttu-id="fc654-205">Ausstellen einer Abfrage</span><span class="sxs-lookup"><span data-stu-id="fc654-205">Issue a Query</span></span>

<span data-ttu-id="fc654-206">Eine Anwendung ändert einen Abfrage Zustand, indem eine Abfrage ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fc654-206">An application changes a query state by issuing a query.</span></span> <span data-ttu-id="fc654-207">Im folgenden finden Sie ein Beispiel für die Ausgabe einer Abfrage:</span><span class="sxs-lookup"><span data-stu-id="fc654-207">Here is an example of issuing a query:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



<span data-ttu-id="fc654-208">Eine Abfrage im signalisierten Zustand geht wie folgt vor, wenn Sie ausgestellt wird:</span><span class="sxs-lookup"><span data-stu-id="fc654-208">A query in the signaled state will transition like this when issued:</span></span>



| <span data-ttu-id="fc654-209">Problemtyp</span><span class="sxs-lookup"><span data-stu-id="fc654-209">Issue Type</span></span>                                | <span data-ttu-id="fc654-210">Die Abfrage wechselt zum.</span><span class="sxs-lookup"><span data-stu-id="fc654-210">Query Transitions to the .</span></span> <span data-ttu-id="fc654-211">.</span><span class="sxs-lookup"><span data-stu-id="fc654-211">.</span></span> <span data-ttu-id="fc654-212">.</span><span class="sxs-lookup"><span data-stu-id="fc654-212">.</span></span> |
|-------------------------------------------|--------------------------------|
| [<span data-ttu-id="fc654-213">**D3DISSUE \_ Begin**</span><span class="sxs-lookup"><span data-stu-id="fc654-213">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="fc654-214">Der Status wird aufgebaut.</span><span class="sxs-lookup"><span data-stu-id="fc654-214">Building state.</span></span>                |
| [<span data-ttu-id="fc654-215">**D3DISSUE \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="fc654-215">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="fc654-216">Ausgegebener Zustand.</span><span class="sxs-lookup"><span data-stu-id="fc654-216">Issued state.</span></span>                  |



 

<span data-ttu-id="fc654-217">Eine Abfrage im Erstellungs Status geht wie folgt vor, wenn Sie ausgestellt wird:</span><span class="sxs-lookup"><span data-stu-id="fc654-217">A query in the building state will transition like this when issued:</span></span>



| <span data-ttu-id="fc654-218">Problemtyp</span><span class="sxs-lookup"><span data-stu-id="fc654-218">Issue Type</span></span>                                | <span data-ttu-id="fc654-219">Die Abfrage wechselt zum.</span><span class="sxs-lookup"><span data-stu-id="fc654-219">Query Transitions to the .</span></span> <span data-ttu-id="fc654-220">.</span><span class="sxs-lookup"><span data-stu-id="fc654-220">.</span></span> <span data-ttu-id="fc654-221">.</span><span class="sxs-lookup"><span data-stu-id="fc654-221">.</span></span>                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="fc654-222">**D3DISSUE \_ Begin**</span><span class="sxs-lookup"><span data-stu-id="fc654-222">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="fc654-223">(Kein Übergang, bleibt im Erstellungs Status.</span><span class="sxs-lookup"><span data-stu-id="fc654-223">(No transition, stays in the building state.</span></span> <span data-ttu-id="fc654-224">Startet die Abfrage Klammer neu.)</span><span class="sxs-lookup"><span data-stu-id="fc654-224">Restarts the query bracket.)</span></span> |
| [<span data-ttu-id="fc654-225">**D3DISSUE \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="fc654-225">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="fc654-226">Ausgegebener Zustand.</span><span class="sxs-lookup"><span data-stu-id="fc654-226">Issued state.</span></span>                                                             |



 

<span data-ttu-id="fc654-227">Eine Abfrage im ausgestellten Status wird wie folgt ausgeführt, wenn Sie ausgestellt wird:</span><span class="sxs-lookup"><span data-stu-id="fc654-227">A query in the issued state will transition like this when issued:</span></span>



| <span data-ttu-id="fc654-228">Problemtyp</span><span class="sxs-lookup"><span data-stu-id="fc654-228">Issue Type</span></span>                                | <span data-ttu-id="fc654-229">Die Abfrage wechselt zum.</span><span class="sxs-lookup"><span data-stu-id="fc654-229">Query Transitions to the .</span></span> <span data-ttu-id="fc654-230">.</span><span class="sxs-lookup"><span data-stu-id="fc654-230">.</span></span> <span data-ttu-id="fc654-231">.</span><span class="sxs-lookup"><span data-stu-id="fc654-231">.</span></span>                    |
|-------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="fc654-232">**D3DISSUE \_ Begin**</span><span class="sxs-lookup"><span data-stu-id="fc654-232">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="fc654-233">Der Status wird erstellt, und die Abfrage Klammer wird neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="fc654-233">Building state and restarts the query bracket.</span></span>    |
| [<span data-ttu-id="fc654-234">**D3DISSUE \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="fc654-234">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="fc654-235">Der Status wird nach dem verwerfen der vorhandenen Abfrage ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="fc654-235">Issued state after abandoning the existing query.</span></span> |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a><span data-ttu-id="fc654-236">Überprüfen Sie den Abfrage Status, und erhalten Sie die Antwort auf die Abfrage.</span><span class="sxs-lookup"><span data-stu-id="fc654-236">Check the Query State and Get the Answer to the Query</span></span>

<span data-ttu-id="fc654-237">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) führt zwei Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="fc654-237">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) does two things:</span></span>

1.  <span data-ttu-id="fc654-238">Gibt den Abfrage Status im Rückgabecode zurück.</span><span class="sxs-lookup"><span data-stu-id="fc654-238">Returns the query state in the return code.</span></span>
2.  <span data-ttu-id="fc654-239">Gibt die Antwort auf die Abfrage in *pData* zurück.</span><span class="sxs-lookup"><span data-stu-id="fc654-239">Returns the answer to the query in *pData*.</span></span>

<span data-ttu-id="fc654-240">Im folgenden werden die [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) -Rückgabecodes von den drei Abfrage Zuständen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="fc654-240">From each of the three query states, here are the [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) return codes:</span></span>



| <span data-ttu-id="fc654-241">Abfragestatus</span><span class="sxs-lookup"><span data-stu-id="fc654-241">Query State</span></span> | <span data-ttu-id="fc654-242">GetData-Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fc654-242">GetData return code</span></span> |
|-------------|---------------------|
| <span data-ttu-id="fc654-243">Ausgeschil</span><span class="sxs-lookup"><span data-stu-id="fc654-243">Signaled</span></span>    | <span data-ttu-id="fc654-244">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="fc654-244">S\_OK</span></span>               |
| <span data-ttu-id="fc654-245">Erstellen</span><span class="sxs-lookup"><span data-stu-id="fc654-245">Building</span></span>    | <span data-ttu-id="fc654-246">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="fc654-246">Error code</span></span>          |
| <span data-ttu-id="fc654-247">Ausgestellt</span><span class="sxs-lookup"><span data-stu-id="fc654-247">Issued</span></span>      | <span data-ttu-id="fc654-248">S \_ false</span><span class="sxs-lookup"><span data-stu-id="fc654-248">S\_FALSE</span></span>            |



 

<span data-ttu-id="fc654-249">Wenn eine Abfrage z. b. den ausgegebene Status aufweist und die Antwort auf die Abfrage nicht verfügbar ist, gibt [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) den Wert "false" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="fc654-249">For example, when a query is in the issued state and the answer to the query is not available, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns S\_FALSE.</span></span> <span data-ttu-id="fc654-250">Wenn die Ressource die Arbeit beendet und die Anwendung ein Abfrage Ende ausgegeben hat, überträgt die Ressource die Abfrage in den signalisierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="fc654-250">When the resource finishes its work and the application has issued a query end, the resource transitions the query to the signaled state.</span></span> <span data-ttu-id="fc654-251">Im signalisierten Zustand gibt **GetData** "S \_ OK" zurück. Dies bedeutet, dass die Antwort auf die Abfrage auch in " *pData*" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fc654-251">From the signaled state, **GetData** returns S\_OK which means that the answer to the query is also returned in *pData*.</span></span> <span data-ttu-id="fc654-252">Hier ist beispielsweise die Sequenz von Ereignissen, die die Anzahl der in einer Rendering-Sequenz gezeichneten Pixel zurückgibt:</span><span class="sxs-lookup"><span data-stu-id="fc654-252">For instance, here is the sequence of events to return the number of pixels drawn in a render sequence:</span></span>

-   <span data-ttu-id="fc654-253">Erstellen der Abfrage</span><span class="sxs-lookup"><span data-stu-id="fc654-253">Create the query.</span></span>
-   <span data-ttu-id="fc654-254">Geben Sie ein Begin-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="fc654-254">Issue a begin event.</span></span>
-   <span data-ttu-id="fc654-255">Zeichnen Sie etwas.</span><span class="sxs-lookup"><span data-stu-id="fc654-255">Draw something.</span></span>
-   <span data-ttu-id="fc654-256">Geben Sie ein End-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="fc654-256">Issue an end event.</span></span>

<span data-ttu-id="fc654-257">Im folgenden finden Sie die entsprechende Code Sequenz:</span><span class="sxs-lookup"><span data-stu-id="fc654-257">The following is the corresponding sequence of code:</span></span>


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="fc654-258">Diese Codezeilen führen verschiedene Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="fc654-258">These lines of code do several things:</span></span>

-   <span data-ttu-id="fc654-259">Ruft [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) auf, um die Anzahl der gezeichneten Pixel zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="fc654-259">Call [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to return the number of pixels drawn.</span></span>
-   <span data-ttu-id="fc654-260">Geben Sie [**D3DGETDATA \_ Flush**](d3dgetdata-flush.md) an, damit die Ressource die Abfrage in den signalisierten Zustand versetzen kann.</span><span class="sxs-lookup"><span data-stu-id="fc654-260">Specify [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md) to enable the resource to transition the query to the signaled state.</span></span>
-   <span data-ttu-id="fc654-261">Rufen Sie die Abfrage Ressource durch Aufrufen von [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) aus einer-Schleife ab.</span><span class="sxs-lookup"><span data-stu-id="fc654-261">Poll the query resource by calling [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) from a loop.</span></span> <span data-ttu-id="fc654-262">Solange **GetData** "S false" zurückgibt \_ , bedeutet dies, dass die Ressource die Antwort noch nicht zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="fc654-262">As long as **GetData** returns S\_FALSE, this means the resource has not returned the answer yet.</span></span>

<span data-ttu-id="fc654-263">Der Rückgabewert von " [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) " weist im Wesentlichen darauf hin, in welchem Zustand die Abfrage ist.</span><span class="sxs-lookup"><span data-stu-id="fc654-263">The return value of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) essentially tells you in what state the query is.</span></span> <span data-ttu-id="fc654-264">Mögliche Werte sind s \_ OK, s \_ false und ein Fehler.</span><span class="sxs-lookup"><span data-stu-id="fc654-264">Possible values are S\_OK, S\_FALSE, and an error.</span></span> <span data-ttu-id="fc654-265">Ruft **GetData** nicht für eine Abfrage auf, die sich im Erstellungs Status befindet.</span><span class="sxs-lookup"><span data-stu-id="fc654-265">Do not call **GetData** on a query that is in the building state.</span></span>

-   <span data-ttu-id="fc654-266">S \_ OK bedeutet, dass die Ressource (GPU oder Treiber oder Laufzeit) abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fc654-266">S\_OK means the resource (GPU or driver, or runtime) is finished.</span></span> <span data-ttu-id="fc654-267">Die Abfrage wird in den signalisierten Zustand zurückversetzt.</span><span class="sxs-lookup"><span data-stu-id="fc654-267">The query is returning to the signaled state.</span></span> <span data-ttu-id="fc654-268">Die Antwort (sofern vorhanden) wird von [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fc654-268">The answer (if any) is being returned by [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>
-   <span data-ttu-id="fc654-269">' \_ False ' bedeutet, dass die Ressource (GPU oder Treiber oder Runtime) noch keine Antwort zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="fc654-269">S\_FALSE means the resource (GPU or driver, or runtime) cannot return an answer yet.</span></span> <span data-ttu-id="fc654-270">Dies kann daran liegen, dass die GPU noch nicht abgeschlossen wurde oder die Arbeit noch nicht gesehen hat.</span><span class="sxs-lookup"><span data-stu-id="fc654-270">This could be because the GPU is not finished or has not seen the work yet.</span></span>
-   <span data-ttu-id="fc654-271">Ein Fehler bedeutet, dass die Abfrage einen Fehler generiert hat, von dem Sie nicht wieder hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="fc654-271">An error means that the query has generated an error from which it cannot recover.</span></span> <span data-ttu-id="fc654-272">Dies kann der Fall sein, wenn das Gerät während einer Abfrage verloren geht.</span><span class="sxs-lookup"><span data-stu-id="fc654-272">This could be the case if the device is lost during a query.</span></span> <span data-ttu-id="fc654-273">Nachdem eine Abfrage einen Fehler generiert hat (außer S \_ false), muss die Abfrage neu erstellt werden, wodurch die Abfrage Sequenz aus dem signalisierten Zustand neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="fc654-273">Once a query has generated an error (other than S\_FALSE), the query must be recreated which will restart the query sequence from the signaled state.</span></span>

<span data-ttu-id="fc654-274">Anstatt [**D3DGETDATA \_ Flush**](d3dgetdata-flush.md)anzugeben, das aktuellere Informationen bereitstellt, können Sie NULL angeben. Dies ist eine genauere Überprüfung, wenn sich die Abfrage im ausgeführten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="fc654-274">Instead of specifying [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md), which provides more up-to-date information, you could supply zero which is a more light-weight check if the query is in the issued state.</span></span> <span data-ttu-id="fc654-275">Die Angabe von 0 (null) bewirkt, dass [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) den Befehls Puffer nicht leert.</span><span class="sxs-lookup"><span data-stu-id="fc654-275">Supplying zero will cause [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to not flush the command buffer.</span></span> <span data-ttu-id="fc654-276">Aus diesem Grund muss sorgfältig vorgegangen werden, um die Endlosschleifen zu vermeiden (Weitere Informationen finden Sie unter **GetData** ).</span><span class="sxs-lookup"><span data-stu-id="fc654-276">For this reason, care must be taken to avoid infinate loops (see **GetData** for details).</span></span> <span data-ttu-id="fc654-277">Da die Laufzeit im Befehls Puffer Aufgaben in die Warteschlange einreiht, ist **D3DGETDATA \_ Flush** ein Mechanismus zum Leeren des Befehls Puffers für den Treiber (und somit die GPU; siehe [exakte Profilerstellung Direct3D API-Aufrufe (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="fc654-277">Since the runtime queues up work in the command buffer, **D3DGETDATA\_FLUSH** is a mechanism for flushing the command buffer to the driver (and hence the GPU; see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="fc654-278">Während der Leerung des Befehls Puffers kann eine Abfrage in den signalisierten Zustand übergehen.</span><span class="sxs-lookup"><span data-stu-id="fc654-278">During the command buffer flush, a query may transition to the signaled state.</span></span>

## <a name="example-an-event-query"></a><span data-ttu-id="fc654-279">Beispiel: eine Ereignis Abfrage</span><span class="sxs-lookup"><span data-stu-id="fc654-279">Example: An Event Query</span></span>

<span data-ttu-id="fc654-280">Ein Begin-Ereignis wird von einer Ereignis Abfrage nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fc654-280">An event query does not support a begin event.</span></span>

-   <span data-ttu-id="fc654-281">Erstellen der Abfrage</span><span class="sxs-lookup"><span data-stu-id="fc654-281">Create the query.</span></span>
-   <span data-ttu-id="fc654-282">Geben Sie ein End-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="fc654-282">Issue an end event.</span></span>
-   <span data-ttu-id="fc654-283">Ruft ab, bis sich die GPU im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="fc654-283">Poll until the GPU is idle.</span></span>
-   <span data-ttu-id="fc654-284">Geben Sie ein End-Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="fc654-284">Issue an end event.</span></span>


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="fc654-285">Dies ist die Sequenz von Befehlen, die von einer Ereignis Abfrage zum Erstellen von Profilen für API-Aufrufe (Application Programming Interface) verwendet werden (siehe [exakte Profilerstellung Direct3D API-Aufrufe (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="fc654-285">This is the sequence of commands an event query uses to profile application programming interface (API) calls (see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="fc654-286">Diese Sequenz verwendet Marker, um den Arbeitsaufwand im Befehls Puffer zu steuern.</span><span class="sxs-lookup"><span data-stu-id="fc654-286">This sequence uses markers to help control the amount of work in the command buffer.</span></span>

<span data-ttu-id="fc654-287">Beachten Sie, dass Anwendungen besonders auf die großen Kosten achten müssen, die mit dem leeren des Befehls Puffers verbunden sind, da dies dazu veranlasst, dass das Betriebssystem in den Kernel Modus wechselt und somit eine beträchtliche Leistungs Einbuße auftritt.</span><span class="sxs-lookup"><span data-stu-id="fc654-287">Note that applications should pay special attention to the large cost associated with flushing the command buffer because this causes the operating system to switch into kernel mode, thus incurring a sizeable performance penalty.</span></span> <span data-ttu-id="fc654-288">Anwendungen sollten auch wissen, dass CPU-Zyklen verschwendet werden, indem auf den Abschluss von Abfragen gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="fc654-288">Applications should also be aware of wasting CPU cycles by waiting for queries to complete.</span></span>

<span data-ttu-id="fc654-289">Abfragen sind eine Optimierung, die beim Rendern verwendet wird, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="fc654-289">Queries are an optimization to be used during rendering to increase performance.</span></span> <span data-ttu-id="fc654-290">Daher ist es nicht vorteilhaft, Zeit mit dem warten auf den Abschluss einer Abfrage zu warten.</span><span class="sxs-lookup"><span data-stu-id="fc654-290">Therefore, it is not beneficial to spend time waiting for a query to finish.</span></span> <span data-ttu-id="fc654-291">Wenn eine Abfrage ausgegeben wird und die Ergebnisse zu dem Zeitpunkt, zu dem Sie von der Anwendung überprüft wird, noch nicht bereit sind, konnte der Optimierungs Versuch nicht erfolgreich ausgeführt werden, und das Rendering sollte wie gewohnt fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="fc654-291">If a query is issued and if the results are not yet ready by the time the application checks for them, the attempt at optimizing did not succeed and rendering should continue as normal.</span></span>

<span data-ttu-id="fc654-292">Das klassische Beispiel hierfür ist die Okklusion.</span><span class="sxs-lookup"><span data-stu-id="fc654-292">The classic example of this is during Occlusion Culling.</span></span> <span data-ttu-id="fc654-293">Anstelle der obigen **while** -Schleife kann eine Anwendung, die Abfragen verwendet, die Okklusions-culsierung implementieren, um zu überprüfen, ob eine Abfrage zu dem Zeitpunkt abgeschlossen ist, zu dem das Ergebnis benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="fc654-293">Instead of the **while** loop above, an application using queries can implement occlusion culling to check to see if a query had finished by the time it needs the result.</span></span> <span data-ttu-id="fc654-294">Wenn die Abfrage noch nicht abgeschlossen wurde, fahren Sie (als Ungünstigster Fall Szenario) fort, als ob das Objekt, für das getestet wird, nicht verdeckt (d.h. sichtbar) ist, und Rendering Sie es.</span><span class="sxs-lookup"><span data-stu-id="fc654-294">If the query has not finished, continue (as a worst-case scenario) as if the object being tested against is not occluded (i.e. it is visible) and render it.</span></span> <span data-ttu-id="fc654-295">Der Code würde etwa wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="fc654-295">The code would look similar to the following.</span></span>


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a><span data-ttu-id="fc654-296">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fc654-296">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc654-297">Erweiterte Themen</span><span class="sxs-lookup"><span data-stu-id="fc654-297">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
