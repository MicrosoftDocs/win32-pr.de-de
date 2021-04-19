---
description: Enthält eine Übersicht über die Einführung der Indizierungs Priorisierung und der rowsetereignisse für Windows 7.
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: Indizieren von Priorisierungs-und rowsetereignissen in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6610500a3c2fcd359f346e5239507fb15ad896d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106366357"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a><span data-ttu-id="35c7e-103">Indizieren von Priorisierungs-und rowsetereignissen in Windows 7</span><span class="sxs-lookup"><span data-stu-id="35c7e-103">Indexing Prioritization and Rowset Events in Windows 7</span></span>

<span data-ttu-id="35c7e-104">In diesem Thema wird die Einführung der Indizierungs Priorisierung und der rowsetereignisse für Windows 7 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="35c7e-104">This topic outlines the introduction of indexing prioritization and rowset events for Windows 7.</span></span>

<span data-ttu-id="35c7e-105">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="35c7e-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="35c7e-106">Indizieren von Priorisierung und rowsetereignissen</span><span class="sxs-lookup"><span data-stu-id="35c7e-106">Indexing Prioritization and Rowset Events</span></span>](#indexing-prioritization-and-rowset-events)
    -   [<span data-ttu-id="35c7e-107">Irowsetpriorization-Beispiele</span><span class="sxs-lookup"><span data-stu-id="35c7e-107">IRowsetPriorization Examples</span></span>](#irowsetpriorization-examples)
    -   [<span data-ttu-id="35c7e-108">Irowsetpriorisierungsereignisse</span><span class="sxs-lookup"><span data-stu-id="35c7e-108">IRowsetPrioritization Events</span></span>](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [<span data-ttu-id="35c7e-109">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="35c7e-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="35c7e-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="35c7e-110">Related topics</span></span>](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a><span data-ttu-id="35c7e-111">Indizieren von Priorisierung und rowsetereignissen</span><span class="sxs-lookup"><span data-stu-id="35c7e-111">Indexing Prioritization and Rowset Events</span></span>

<span data-ttu-id="35c7e-112">In Windows 7? und höher gibt es einen Prioritäts Stapel, in dem der Kontext einer bestimmten Abfrage den Client anfordern kann, dass die in dieser Abfrage verwendeten Bereiche priorisiert werden, die mit den normalen Elementen priorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="35c7e-112">In Windows 7?and later, there is a priority stack within which the context of any particular query, the client can request that the scopes used in that query be prioritized above that of normal items.</span></span>

<span data-ttu-id="35c7e-113">Dieser Priorisierungs Stapel hat die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="35c7e-113">This prioritization stack has the following characteristics:</span></span>

-   <span data-ttu-id="35c7e-114">Elemente im Stapel können die Priorität "Vordergrund", "hoch" oder "niedrig" aufweisen:</span><span class="sxs-lookup"><span data-stu-id="35c7e-114">Items in the stack can have foreground, high, or low priority:</span></span>
    -   <span data-ttu-id="35c7e-115">**Vordergrund**: Backoff-Logik wird übersprungen, und die Indizierung verläuft so schnell, wie der Computer zulässt.</span><span class="sxs-lookup"><span data-stu-id="35c7e-115">**Foreground**: Backoff logic is skipped and indexing proceeds as fast as the machine allows.</span></span>
    -   <span data-ttu-id="35c7e-116">**Hoch**: Priorisierung wurde mit Backoff angefordert.</span><span class="sxs-lookup"><span data-stu-id="35c7e-116">**High**: Prioritization has been requested with backoff.</span></span>
    -   <span data-ttu-id="35c7e-117">**Niedrig**: Es wurde eine Priorisierung angefordert, nicht auf Kosten anderer Bereiche im Stapel, sondern oberhalb der Indizierung ohne Priorität.</span><span class="sxs-lookup"><span data-stu-id="35c7e-117">**Low**: Prioritization has been requested, not at the expense of other scopes on the stack, but above non-prioritized indexing.</span></span>
-   <span data-ttu-id="35c7e-118">Jede Anforderung für hohe oder Vordergrund Priorität bestößt die anfordernde Abfrage automatisch am Anfang des Stapels.</span><span class="sxs-lookup"><span data-stu-id="35c7e-118">Any request for high or foreground priority bumps the requesting query to the top of the stack automatically.</span></span>
-   <span data-ttu-id="35c7e-119">Nur das Element oben im Stapel kann eine Vordergrund Priorität haben.</span><span class="sxs-lookup"><span data-stu-id="35c7e-119">Only the item on top of the stack can have foreground priority.</span></span>
-   <span data-ttu-id="35c7e-120">Eine Abfrage mit Vordergrund Priorität, die bei Priorität nach unten gesetzt wird, empfängt ein Ereignis, das die Vordergrund Priorität verliert und mit einem Backoff zu einer hohen Priorität geworden ist.</span><span class="sxs-lookup"><span data-stu-id="35c7e-120">A query with foreground priority that is bumped down in priority receives an event notifying it that it has lost foreground priority and has become a high priority with backoff.</span></span>

<span data-ttu-id="35c7e-121">Der Prioritäts Stapel legt eine Gesamt Priorität von Elementen fest, die im Indexer wie folgt verarbeitet werden:</span><span class="sxs-lookup"><span data-stu-id="35c7e-121">The priority stack sets an overall priority of items that are processed in the indexer as follows:</span></span>

-   <span data-ttu-id="35c7e-122">Benachrichtigungen mit hoher Priorität verfügen über keinen Backoff und werden in der Regel nur für eine kleine Anzahl von Elementen gesendet.</span><span class="sxs-lookup"><span data-stu-id="35c7e-122">High Priority notifications have no backoff, and are typically sent only for a small number of items.</span></span> <span data-ttu-id="35c7e-123">Windows-Explorer verwendet diese Priorität z. b. bei kleinen Kopier-Engine-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="35c7e-123">For example, Windows Explorer uses this priority for small copy engine operations.</span></span>
-   <span data-ttu-id="35c7e-124">Der Prioritäts Stapel ist der obere Rand des Stapels, verfügt über einen Backoff und ist die zuletzt angeforderte Prioritäts Abfrage.</span><span class="sxs-lookup"><span data-stu-id="35c7e-124">Priority Stack is top of the stack, has backoff, and is the last requested priority query.</span></span>
-   <span data-ttu-id="35c7e-125">Zweite Abfrage im Stapel.</span><span class="sxs-lookup"><span data-stu-id="35c7e-125">Second query in the stack.</span></span>
-   <span data-ttu-id="35c7e-126">Dritte Abfrage im Stapel.</span><span class="sxs-lookup"><span data-stu-id="35c7e-126">Third query in the stack.</span></span>
-   <span data-ttu-id="35c7e-127">Vierte Abfrage im Stapel usw.</span><span class="sxs-lookup"><span data-stu-id="35c7e-127">Fourth query in the stack, and so forth.</span></span>
-   <span data-ttu-id="35c7e-128">Elemente mit normaler Priorität.</span><span class="sxs-lookup"><span data-stu-id="35c7e-128">Normal Priority items.</span></span>
-   <span data-ttu-id="35c7e-129">Gelöschte Elemente.</span><span class="sxs-lookup"><span data-stu-id="35c7e-129">Deleted items.</span></span>
    > [!Note]  
    > <span data-ttu-id="35c7e-130">Elemente in jeder Gruppe werden intern durch die ältere Semantik pro Element priorisiert.</span><span class="sxs-lookup"><span data-stu-id="35c7e-130">Items within each group are prioritized internally through the older per-item semantics.</span></span>

     

### <a name="irowsetpriorization-examples"></a><span data-ttu-id="35c7e-131">Irowsetpriorization-Beispiele</span><span class="sxs-lookup"><span data-stu-id="35c7e-131">IRowsetPriorization Examples</span></span>

<span data-ttu-id="35c7e-132">Die primäre API für Priorisierungs arbeiten ist über die folgende Schnittstelle verfügbar, die durch Abfragen des zurückgegebenen Rowsets aufgerufen werden kann:</span><span class="sxs-lookup"><span data-stu-id="35c7e-132">The primary API for prioritization work is available through the following interface, which can be called by querying the returned rowset:</span></span>


```
typedef [v1_enum] enum
{
    PRIORITY_LEVEL_FOREGROUND           = 0,    // process items in the scope first as quickly as possible
    PRIORITY_LEVEL_HIGH                 = 1,    // process items in the scope first at the normal rate
    PRIORITY_LEVEL_LOW                  = 2,    // process items in this scope before those at the normal rate, but after any other prioritization requests
    PRIORITY_LEVEL_DEFAULT              = 3     // process items at the normal indexer rate
} PRIORITY_LEVEL;


[
    object,
    uuid(IRowsetPrioritization_GUID),
    pointer_default(unique)
]
interface IRowsetPrioritization : IUnknown
{
    // Sets or retrieves the current indexer prioritization level for the scope specified by
    // this query.

    HRESULT SetScopePriority( [in] PRIORITY_LEVEL priority, [in] DWORD scopeStatisticsEventFrequency );
    HRESULT GetScopePriority( [out] PRIORITY_LEVEL * priority, [out] DWORD * scopeStatisticsEventFrequency );

    // Gets information describing the scope specified by this query:
    // indexedDocumentCount     -   The total number of documents currently indexed in the scope
    // oustandingAddCount       -   The total number of documents yet to be indexed in the scope (those not yet included in indexedDocumentCount)
    // oustandingModifyCount    -   The total number of documents indexed in the scope that need to be re-indexed (included in indexedDocumentCount)
    
    HRESULT GetScopeStatistics( [out] DWORD * indexedDocumentCount, [out] DWORD * oustandingAddCount, [out] DWORD * oustandingModifyCount );
};
```



<span data-ttu-id="35c7e-133">Die rowsetpriorisierung funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="35c7e-133">Rowset prioritization works as follows:</span></span>

1.  <span data-ttu-id="35c7e-134">[**Irowsetpriorisierung**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) wird mit der [IUnknown:: QueryInterface-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für ein Indexer-Rowset abgerufen.</span><span class="sxs-lookup"><span data-stu-id="35c7e-134">[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) is acquired with [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an indexer rowset.</span></span> <span data-ttu-id="35c7e-135">**DBPROP \_ Enablerowsetevents** muss mit der OLE DB [ICommandProperties:: SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) -Methode auf " **true** " festgelegt werden, bevor die Abfrage ausgeführt wird, um die rowsetpriorisierung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="35c7e-135">**DBPROP\_ENABLEROWSETEVENTS** must be set to **TRUE** with the OLE DB [ICommandProperties::SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) method prior to executing the query in order to use rowset prioritization.</span></span>
2.  <span data-ttu-id="35c7e-136">[**Irowsetprioritisierung:: setscopepriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) legt die Priorisierung für die Bereiche fest, die der Abfrage angehören, und das Intervall, das das Bereichs Statistik Ereignis ausgelöst wird, wenn ausstehende Dokumente innerhalb der Abfrage Bereiche indiziert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="35c7e-136">[**IRowsetPrioritization::SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) sets the prioritization for the scopes belonging to the query, and the interval the scope statistics event is raised when there are outstanding documents to be indexed within the query scopes.</span></span> <span data-ttu-id="35c7e-137">Dieses Ereignis wird ausgelöst, wenn die Prioritätsstufe auf Default festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="35c7e-137">This event is raised if the priority level is set to default.</span></span>
3.  <span data-ttu-id="35c7e-138">[**Irowsetprioritisierung:: getscopestatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) kann verwendet werden, um die Anzahl der indizierten Elemente im Bereich, die Anzahl der ausstehenden Dokumente, die dem Bereich hinzugefügt werden sollen, und die Anzahl der Dokumente, die in diesem Bereich neu indiziert werden müssen, zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="35c7e-138">[**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) can be used to get the number of indexed items in the scope, the number of outstanding documents to be added in the scope, and the number of documents that need to be re-indexed within this scope.</span></span>

### <a name="irowsetprioritization-events"></a><span data-ttu-id="35c7e-139">Irowsetpriorisierungsereignisse</span><span class="sxs-lookup"><span data-stu-id="35c7e-139">IRowsetPrioritization Events</span></span>

<span data-ttu-id="35c7e-140">Es gibt drei rowsetereignisse in [**irowsetevents:: onrowsetevent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) in der [**RowSetEvent- \_ Typenumeration**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) :</span><span class="sxs-lookup"><span data-stu-id="35c7e-140">There are three rowset events in [**IRowsetEvents::OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) in the [**ROWSETEVENT\_TYPE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) enumeration:</span></span>


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



<span data-ttu-id="35c7e-141">Die rowsetereignisse lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="35c7e-141">The rowset events are as follows:</span></span>

-   <span data-ttu-id="35c7e-142">Das Ereignis **RowSetEvent \_ Type \_ dataabgelaufgibt** an, dass Daten, die das Rowset unterstützen, abgelaufen sind und dass ein neues Rowset angefordert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="35c7e-142">The **ROWSETEVENT\_TYPE\_DATAEXPIRED** event indicates that data backing the rowset has expired, and that a new rowset should be requested.</span></span>
-   <span data-ttu-id="35c7e-143">Das Ereignis " **\_ \_ foregroundlost" des rowsettyps** gibt an, dass ein Element mit der Vordergrund Priorität im Priorisierungs Stapel herabgestuft wurde, da sich eine andere Person vor dieser Abfrage selbst priorisiert hat.</span><span class="sxs-lookup"><span data-stu-id="35c7e-143">The **ROWSET\_TYPE\_FOREGROUNDLOST** event indicates that an item that did have foreground priority in the prioritization stack has been demoted, because someone else prioritized themselves ahead of this query.</span></span>
-   <span data-ttu-id="35c7e-144">Das Ereignis **RowSetEvent \_ Type \_ scopestatistics** bietet Ihnen die gleichen Informationen, die über den [**irowsetprioritisierung:: getscopestatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) -Methodenaufrufe verfügbar sind, aber über einen Push-Mechaniker wie folgt:</span><span class="sxs-lookup"><span data-stu-id="35c7e-144">The **ROWSETEVENT\_TYPE\_SCOPESTATISTICS** event gives you the same information available from the [**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) method call, but through a push mechanic, as follows:</span></span>
    -   <span data-ttu-id="35c7e-145">Das Ereignis tritt auf, wenn die Priorisierungs-API verwendet wurde, um eine nicht standardmäßige Priorisierungs Ebene und eine Statistik Ereignis Häufigkeit ungleich NULL anzufordern.</span><span class="sxs-lookup"><span data-stu-id="35c7e-145">The event arises if the prioritization API has been used to request a non-default prioritization level, and a non-zero statistics event frequency.</span></span>
    -   <span data-ttu-id="35c7e-146">Das Ereignis tritt nur auf, wenn Statistiken tatsächlich geändert werden und das in [**irowsetpriorisierung**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) angegebene Intervall abgelaufen ist (das Intervall garantiert nicht die Häufigkeit des Ereignisses).</span><span class="sxs-lookup"><span data-stu-id="35c7e-146">The event arises only when statistics actually change, and the interval specified in the [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) has elapsed (the interval does not guarantee the frequency of the event).</span></span>
    -   <span data-ttu-id="35c7e-147">Dieses Ereignis stellt sicher, dass der Status "Sprung 0" (null Elemente, die noch nicht hinzugefügt werden müssen, 0 verbleibende modifizierungwerte) nicht ausgelöst wird, vorausgesetzt, dass ein Ereignis ungleich NULL ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="35c7e-147">This event is guaranteed to raise a "bounce zero" state (zero items remaining to be added, zero modifies remaining), provided that a non-zero event has been raised.</span></span>
    -   <span data-ttu-id="35c7e-148">Der Indexer kann Elemente verarbeiten, ohne dieses Ereignis zu senden, wenn die Warteschlange vor der Statistik Ereignis Häufigkeit entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="35c7e-148">The indexer may process items without sending this event, if the queue empties before the statistics event frequency.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35c7e-149">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="35c7e-149">Additional Resources</span></span>

<span data-ttu-id="35c7e-150">Sehen Sie sich die folgenden Ressourcen im Zusammenhang mit Priorisierung und Rowsets an:</span><span class="sxs-lookup"><span data-stu-id="35c7e-150">See the following resources related to prioritization and rowsets:</span></span>

-   <span data-ttu-id="35c7e-151">Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="35c7e-151">Interfaces:</span></span>
    -   [<span data-ttu-id="35c7e-152">**IRow-tevents**</span><span class="sxs-lookup"><span data-stu-id="35c7e-152">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [<span data-ttu-id="35c7e-153">**Irowsetpriorisierung**</span><span class="sxs-lookup"><span data-stu-id="35c7e-153">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   <span data-ttu-id="35c7e-154">Aufzählungen:</span><span class="sxs-lookup"><span data-stu-id="35c7e-154">Enumerations:</span></span>
    -   [<span data-ttu-id="35c7e-155">**Priorisieren von \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="35c7e-155">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [<span data-ttu-id="35c7e-156">**Prioritäts \_ Stufe**</span><span class="sxs-lookup"><span data-stu-id="35c7e-156">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [<span data-ttu-id="35c7e-157">**rowevent- \_ Ausdruck ItemState**</span><span class="sxs-lookup"><span data-stu-id="35c7e-157">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [<span data-ttu-id="35c7e-158">**rowsertevent- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="35c7e-158">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a><span data-ttu-id="35c7e-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="35c7e-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35c7e-160">Windows 7-Suche</span><span class="sxs-lookup"><span data-stu-id="35c7e-160">Windows 7 Search</span></span>](./-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="35c7e-161">Neu bei der Windows 7-Suche</span><span class="sxs-lookup"><span data-stu-id="35c7e-161">New for Windows 7 Search</span></span>](new-for-windows-7-search.md)
</dt> <dt>

[<span data-ttu-id="35c7e-162">Windows Shell-Bibliotheken in Windows 7</span><span class="sxs-lookup"><span data-stu-id="35c7e-162">Windows Shell Libraries in Windows 7</span></span>](-search-win7-development-scenarios.md)
</dt> </dl>

 

 