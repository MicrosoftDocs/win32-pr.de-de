---
description: Der Dienst "com+-Warteschlangen Komponenten" unterstützt das Konzept der Partitionen vollständig. Das heißt, wenn eine in einer Warteschlange befindliche Komponente innerhalb einer Partition ausgeführt wird, wird die Nachricht in die Warteschlange eingereiht, und die Komponente wird schließlich innerhalb der Komponenten Partition ausgeführt.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Komponenten und Partitionen in der com+-Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589d7cb7c3e61be8ef53a248f990cde65447cf9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523283"
---
# <a name="com-queued-components-and-partitions"></a><span data-ttu-id="f78d0-104">Komponenten und Partitionen in der com+-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="f78d0-104">COM+ Queued Components and Partitions</span></span>

<span data-ttu-id="f78d0-105">Der Dienst "com+-Warteschlangen Komponenten" unterstützt das Konzept der Partitionen vollständig.</span><span class="sxs-lookup"><span data-stu-id="f78d0-105">The COM+ queued components service fully supports the concept of partitions.</span></span> <span data-ttu-id="f78d0-106">Das heißt, wenn eine in einer Warteschlange befindliche Komponente innerhalb einer Partition ausgeführt wird, wird die Nachricht in die Warteschlange eingereiht, und die Komponente wird schließlich innerhalb der Partition der Komponente ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f78d0-106">That is, when a queued component within a partition is executed, the message is queued and the component is eventually executed within the component's partition.</span></span>

## <a name="queue-names-for-partitioned-components"></a><span data-ttu-id="f78d0-107">Warteschlangen Namen für partitionierte Komponenten</span><span class="sxs-lookup"><span data-stu-id="f78d0-107">Queue Names for Partitioned Components</span></span>

<span data-ttu-id="f78d0-108">In der Regel verwendet der Dienst für in der Warteschlange befindliche Komponenten den Anwendungsnamen als Warteschlangen Namen.</span><span class="sxs-lookup"><span data-stu-id="f78d0-108">Traditionally, the queued components service uses the application name as the queue name.</span></span> <span data-ttu-id="f78d0-109">Dies bedeutet, dass in einem Szenario ohne Partitionen, in dem nur eine Instanz eines Anwendungs namens auf einem Computer vorhanden ist, jeder Anwendungsname eine eigene Nachrichten Warteschlange aufweist.</span><span class="sxs-lookup"><span data-stu-id="f78d0-109">This means that in a non-partitions scenario, where only one instance of an application name exists on a computer, each application name has its own message queue.</span></span>

<span data-ttu-id="f78d0-110">Wenn jedoch mehrere Instanzen desselben Anwendungs namens auf einem Computer vorhanden sein können, verwendet der Dienst für in der Warteschlange befindliche Komponenten für alle in der Warteschlange befindlichen Komponenten, die denselben Anwendungsnamen haben, dieselbe Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="f78d0-110">In the case of partitions, however, where multiple instances of the same application name can exist on a computer, the queued components service uses the same queue for any queued components that share the same application name.</span></span>

## <a name="activating-queued-components"></a><span data-ttu-id="f78d0-111">Aktivieren von Komponenten in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="f78d0-111">Activating Queued Components</span></span>

<span data-ttu-id="f78d0-112">Die gleichen Regeln, wie die Partitions-ID zum Aktivieren einer nicht in der Warteschlange befindlichen Komponente verwendet wird, gelten für eine in der Warteschlange befindliche Komponente wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f78d0-112">The same rules for how the partition ID is used to activate a non-queued component applies to a queued component, as follows:</span></span>

-   <span data-ttu-id="f78d0-113">Wenn ein Moniker zum Aktivieren der in der Warteschlange befindlichen Komponente verwendet wird und eine Partitions-ID enthalten ist, wird diese Partitions-ID verwendet, um die Partition zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f78d0-113">If a moniker is used to activate the queued component and a partition ID is included, this partition ID is used to locate the partition.</span></span> <span data-ttu-id="f78d0-114">Diese Partitions-ID hat Vorrang vor allen Partitions-IDs, die im Kontext für die aktivierte Komponente vorhanden sein könnten.</span><span class="sxs-lookup"><span data-stu-id="f78d0-114">This partition ID takes precedence over any partition ID that might exist in the context for the component being activated.</span></span>
-   <span data-ttu-id="f78d0-115">Wenn kein Moniker zum Aktivieren der Komponente verwendet wird, wird die Partitions-ID verwendet, die im Kontext des Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f78d0-115">If no moniker is being used to activate the component, the partition ID that is in the object's context is used.</span></span>
-   <span data-ttu-id="f78d0-116">Wenn im Kontext des Objekts keine Partitions-ID vorhanden ist, wird die Standard Zuordnung zwischen Benutzern und Partitionen in Active Directory verwendet.</span><span class="sxs-lookup"><span data-stu-id="f78d0-116">If no partition ID exists in the object's context, the default user-to-partition mapping within Active Directory is used.</span></span>

> [!Note]  
> <span data-ttu-id="f78d0-117">Wenn ein Server Computer vom Netzwerk getrennt ist und die Zuordnung zwischen Benutzer und Partition geändert wird, während der Server getrennt wird, kann der Partitions Cache eine veraltete Zuordnung zwischen Benutzern und Partitionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f78d0-117">If a server computer is disconnected from the network and if the user-to-partition set mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition set mapping.</span></span> <span data-ttu-id="f78d0-118">Dies kann zu einem Aktivierungs Fehler führen, wenn die Zuordnung von Benutzer zu Partition zum Aktivieren einer Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f78d0-118">This could result in an activation error if user-to-partition set mapping is the mechanism used to activate a component.</span></span>

 

<span data-ttu-id="f78d0-119">Com+-Ereignisse sind vollständig in Partitionen integriert.</span><span class="sxs-lookup"><span data-stu-id="f78d0-119">COM+ events are fully integrated into partitions.</span></span> <span data-ttu-id="f78d0-120">Dies bedeutet, dass ein Abonnent einen Verleger abonnieren kann, dessen Anwendung sich innerhalb einer Partition befindet.</span><span class="sxs-lookup"><span data-stu-id="f78d0-120">This means that a subscriber can subscribe to a publisher whose application resides within a partition.</span></span> <span data-ttu-id="f78d0-121">Um dieses Abonnement zuzulassen, enthält die Auflistung der Abonnenten Klassen zwei Partitions bezogene Eigenschaften – eine Partitions-ID der Ereignisklasse und eine Anwendungs-ID der Ereignisklasse.</span><span class="sxs-lookup"><span data-stu-id="f78d0-121">To allow this subscription, the subscriber class collection includes two partition-related properties—an event class partition ID and an event class application ID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f78d0-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f78d0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f78d0-123">Einschränkungen beim Anwendungs Entwurf</span><span class="sxs-lookup"><span data-stu-id="f78d0-123">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="f78d0-124">Partitions Implementierung</span><span class="sxs-lookup"><span data-stu-id="f78d0-124">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="f78d0-125">Registrieren und Aktivieren von Komponenten in Partitionen</span><span class="sxs-lookup"><span data-stu-id="f78d0-125">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="f78d0-126">Was sind COM+-Partitionen?</span><span class="sxs-lookup"><span data-stu-id="f78d0-126">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



