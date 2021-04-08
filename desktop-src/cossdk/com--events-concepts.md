---
description: Konzepte der com+-Ereignisse
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: Konzepte der com+-Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749088"
---
# <a name="com-events-concepts"></a><span data-ttu-id="8eeda-103">Konzepte der com+-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8eeda-103">COM+ Events Concepts</span></span>

<span data-ttu-id="8eeda-104">Der com+-Ereignis Dienst ist ein automatisiertes, *locker gekoppeltes Ereignis* System, das Ereignis Informationen von verschiedenen Verlegern im com+-Katalog speichert.</span><span class="sxs-lookup"><span data-stu-id="8eeda-104">The COM+ events service is an automated, *loosely coupled event* system that stores event information from different publishers in the COM+ catalog.</span></span> <span data-ttu-id="8eeda-105">Abonnenten können diesen Ereignisspeicher Abfragen und die Ereignisse auswählen, über die Sie hören möchten.</span><span class="sxs-lookup"><span data-stu-id="8eeda-105">Subscribers can query this event store and select the events that they want to hear about.</span></span>

> [!Note]  
> <span data-ttu-id="8eeda-106">Ein *Ereignis* wird durch eine Methode in einer COM+-Schnittstelle identifiziert, die als *Ereignismethode* bezeichnet wird und von einem Verleger stammt und über den com+-Ereignis Dienst an die richtigen Abonnenten oder Abonnenten gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="8eeda-106">An *event* is identified by a method in a COM+ interface, known as an *event method*, and is originated by a publisher and dispatched to the correct subscriber or subscribers through the COM+ events service.</span></span> <span data-ttu-id="8eeda-107">Ereignis Methoden müssen eindeutig benannt werden und dürfen nur Eingabeparameter (keine Ausgabe-oder Eingabe-/Ausgabeparameter) enthalten.</span><span class="sxs-lookup"><span data-stu-id="8eeda-107">Event methods must be uniquely named and can contain only input parameters (no output or input/output parameters).</span></span> <span data-ttu-id="8eeda-108">Der Rückgabewert muss ein **HRESULT** sein.</span><span class="sxs-lookup"><span data-stu-id="8eeda-108">The return value must be an **HRESULT**.</span></span>

 

<span data-ttu-id="8eeda-109">Der com+-Ereignis Dienst verarbeitet den größten Teil der Ereignis Semantik für den Verleger und den Abonnenten.</span><span class="sxs-lookup"><span data-stu-id="8eeda-109">The COM+ events service handles most of the event semantics for the publisher and subscriber.</span></span> <span data-ttu-id="8eeda-110">Herausgeber bieten die Veröffentlichung von Ereignis Typen, und Abonnenten fordern Ereignis Typen von Verlegern an.</span><span class="sxs-lookup"><span data-stu-id="8eeda-110">Publishers offer to publish event types, and subscribers request event types from publishers.</span></span> <span data-ttu-id="8eeda-111">Anders als bei einem *eng verknüpften Ereignis* System, bei dem Herausgeber den mehr Aufwand für das direkte Aufrufen von Abonnenten behandeln müssen, verwaltet der com+-Ereignis Dienst Abonnement Daten im com+-Katalog unabhängig vom Verleger und dem Abonnenten.</span><span class="sxs-lookup"><span data-stu-id="8eeda-111">Unlike a *tightly coupled event* system, where publishers must handle the overhead of calling subscribers directly, the COM+ events service maintains subscription data in the COM+ catalog, independent of the publisher and subscriber.</span></span> <span data-ttu-id="8eeda-112">Dadurch wird das Programmiermodell für den Verleger und den Abonnenten vereinfacht, da die com+-Abonnenten Komponente nicht die Logik zum Aufbauen von Abonnements enthalten muss.</span><span class="sxs-lookup"><span data-stu-id="8eeda-112">This simplifies the programming model for the publisher and subscriber because the COM+ subscriber component does not need to contain the logic for building subscriptions.</span></span>

<span data-ttu-id="8eeda-113">Da der Lebenszyklus der com+-Ereignis Abonnement Daten vom Verleger oder Abonnenten getrennt ist, können Abonnements erstellt werden, bevor entweder der Abonnent oder die Verleger Anwendungen aktiv werden.</span><span class="sxs-lookup"><span data-stu-id="8eeda-113">Because the life cycle of the COM+ events subscription data is separate from that of either the publisher or the subscriber, subscriptions can be built prior to either the subscriber or the publisher applications being active.</span></span> <span data-ttu-id="8eeda-114">Dies bedeutet auch, dass Verleger und Abonnenten separat entwickelt und bereitgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="8eeda-114">This also means that publishers and subscribers can be developed and deployed separately.</span></span> <span data-ttu-id="8eeda-115">Der Verleger kann ohne Kenntnis der Anzahl und des Speicher Orts der Abonnenten geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8eeda-115">The publisher can be written without knowledge of the number and location of the subscribers.</span></span> <span data-ttu-id="8eeda-116">Die Abonnenten verwenden den com+-Ereignis Dienst, um nach dem Verleger zu suchen und seine Abonnements zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="8eeda-116">The subscribers use the COM+ Events service to find the publisher and manage their subscriptions.</span></span>

<span data-ttu-id="8eeda-117">Die folgenden Themen in diesem Abschnitt enthalten ausführliche Informationen zu den Kernelementen des com+-Ereignis Dienstanbieter und deren Verwendung.</span><span class="sxs-lookup"><span data-stu-id="8eeda-117">The following topics in this section provide detailed information about the core elements of the COM+ events service and how to use them.</span></span>

-   [<span data-ttu-id="8eeda-118">Das com+-Ereignis Klassenobjekt</span><span class="sxs-lookup"><span data-stu-id="8eeda-118">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
-   [<span data-ttu-id="8eeda-119">Abonnements</span><span class="sxs-lookup"><span data-stu-id="8eeda-119">Subscriptions</span></span>](subscriptions.md)
-   [<span data-ttu-id="8eeda-120">Veröffentlichen und Bereitstellung von Ereignissen in com+</span><span class="sxs-lookup"><span data-stu-id="8eeda-120">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
-   [<span data-ttu-id="8eeda-121">Filtern von Ereignissen in com+</span><span class="sxs-lookup"><span data-stu-id="8eeda-121">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
-   [<span data-ttu-id="8eeda-122">Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="8eeda-122">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a><span data-ttu-id="8eeda-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8eeda-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eeda-124">Sicherheitsüberlegungen für COM+-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8eeda-124">COM+ Events Security Considerations</span></span>](com--events-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="8eeda-125">Aufgaben für COM+-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8eeda-125">COM+ Events Tasks</span></span>](com--events-tasks.md)
</dt> </dl>

 

 



