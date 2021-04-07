---
description: Abrufen von Auflistungen im com+-Katalog
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Abrufen von Auflistungen im com+-Katalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cbf81bfedd4ba37b74b36e5ad9a8ad320e9c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748032"
---
# <a name="retrieving-collections-on-the-com-catalog"></a><span data-ttu-id="bc7d9-103">Abrufen von Auflistungen im com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="bc7d9-103">Retrieving Collections on the COM+ Catalog</span></span>

<span data-ttu-id="bc7d9-104">Daten im com+-Katalog werden in einer Hierarchie von Sammlungen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-104">Data on the COM+ catalog is stored within a hierarchy of collections.</span></span> <span data-ttu-id="bc7d9-105">Im Verwaltungs Programmkomponenten Dienste werden viele dieser Sammlungen als Ordner in der Konsolen Struktur angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-105">In the Component Services administrative tool, many of these collections appear as folders in the console tree.</span></span> <span data-ttu-id="bc7d9-106">Sammlungen, die nicht als Ordner angezeigt werden, können nur Programm gesteuert aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-106">Collections that don't appear as folders can be accessed only programmatically.</span></span> <span data-ttu-id="bc7d9-107">Sammlungen dienen als Container für Elemente.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-107">Collections serve as containers for items.</span></span> <span data-ttu-id="bc7d9-108">Die Elemente in einer bestimmten Auflistung sind von einem konsistenten Typ. Das heißt, dass alle die gleiche Art von Element darstellen und eine beliebige Anzahl von Elementen in einer Auflistung vorhanden sein kann.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-108">The items in a given collection are all of a consistent type; that is, they all represent the same kind of element, and there can be an arbitrary number of items in a collection.</span></span> <span data-ttu-id="bc7d9-109">Beispielsweise enthält die [**Anwendungs**](applications.md) Auflistung ein Element für jede com+-Anwendung, die auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-109">For example, the [**Applications**](applications.md) collection contains an item for each COM+ application that is installed on the machine.</span></span> <span data-ttu-id="bc7d9-110">Diese Sammlung wird im Verwaltungs Tool als **com+-Anwendungs** Ordner angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-110">This collection appears in the administrative tool as the **COM+ Applications** folder.</span></span>

<span data-ttu-id="bc7d9-111">Die Auflistungen treten in einer hierarchischen Struktur auf, da die darin enthaltenen Elemente einer angeborenen Reihenfolge der Einfügung folgen.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-111">The collections occur in a hierarchical structure because the elements they contain follow an innate order of inclusion.</span></span> <span data-ttu-id="bc7d9-112">Da z. b. Komponenten in einer COM+-Anwendung installiert werden, wird die [**Komponenten**](components.md) Auflistung logisch unter der [**Anwendungs**](applications.md) Sammlung unterteilt.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-112">For example, because components are installed into a COM+ application, the [**Components**](components.md) collection is logically subsumed under the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="bc7d9-113">Vor allem, um die Komponenten zu speichern, die in dieser speziellen Anwendung installiert sind, gibt es für jedes Element in der **Anwendungs** Auflistung eine eindeutige **Komponenten** Sammlung.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-113">More particularly, to hold the components installed into that particular application, there is a distinct **Components** collection for each item in the **Applications** collection.</span></span>

<span data-ttu-id="bc7d9-114">Sie müssen immer dann eine Auflistung im Katalog abrufen, wenn Sie ein Element abrufen und Eigenschaften für dieses Element festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-114">You must get a collection on the catalog whenever you want to retrieve an item and set properties on it.</span></span> <span data-ttu-id="bc7d9-115">Im Allgemeinen müssen Sie mehrere Sammlungen schrittweise durchlaufen, um das gewünschte Element zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-115">In the general case, you need to step through several collections to get to the element you want.</span></span> <span data-ttu-id="bc7d9-116">Die Vorgehensweise hierzu finden Sie unter [Navigieren in der com+](navigating-the-com--collection-hierarchy.md)-Auflistungs Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-116">For the procedure for doing this, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="bc7d9-117">Nachdem Sie eine Sammlung abgerufen haben und bevor Sie direkt mit den darin enthaltenen Elementen arbeiten können, müssen Sie die Sammlung auffüllen, die Daten für den Inhalt der Sammlung aus dem com+-Katalog abruft.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-117">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection, which fetches data for the collection's contents from the COM+ catalog.</span></span> <span data-ttu-id="bc7d9-118">Weitere Informationen finden Sie unter Auffüllen von [com+](populating-com--collections.md)-Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-118">For details, see [Populating COM+ Collections](populating-com--collections.md).</span></span>

<span data-ttu-id="bc7d9-119">Außerdem gibt es eine Möglichkeit, die Sie verwenden können, mit der Sie dynamisch Abfragen können, um festzustellen, welche verwandten Sammlungen von einer bestimmten Sammlung verfügbar sind, die Sie halten.</span><span class="sxs-lookup"><span data-stu-id="bc7d9-119">Additionally, there is a facility you can use that enables you to dynamically query to see what related collections are available from a given collection you are holding.</span></span> <span data-ttu-id="bc7d9-120">Weitere Informationen finden Sie unter [Abfragen von verfügbaren verwandten Sammlungen](querying-for-available-related-collections.md).</span><span class="sxs-lookup"><span data-stu-id="bc7d9-120">For details, see [Querying for Available Related Collections](querying-for-available-related-collections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc7d9-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bc7d9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc7d9-122">Com+-Verwaltungsvorgänge in Transaktionen</span><span class="sxs-lookup"><span data-stu-id="bc7d9-122">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="bc7d9-123">Behandeln von com+-Verwaltungsfehlern</span><span class="sxs-lookup"><span data-stu-id="bc7d9-123">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="bc7d9-124">Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog</span><span class="sxs-lookup"><span data-stu-id="bc7d9-124">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="bc7d9-125">Übersicht über die COMAdmin-Objekte</span><span class="sxs-lookup"><span data-stu-id="bc7d9-125">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="bc7d9-126">Festlegen von Eigenschaften und Speichern von Änderungen am com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="bc7d9-126">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



