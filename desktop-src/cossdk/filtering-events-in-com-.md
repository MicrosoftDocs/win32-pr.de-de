---
description: 'Com+-Ereignisse bieten zwei Möglichkeiten, um zu steuern, welche Ereignisse die folgenden Abonnenten erreichen: Herausgeber Filterung und Parameter Filterung.'
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: Filtern von Ereignissen in com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748864"
---
# <a name="filtering-events-in-com"></a><span data-ttu-id="d9af1-103">Filtern von Ereignissen in com+</span><span class="sxs-lookup"><span data-stu-id="d9af1-103">Filtering Events in COM+</span></span>

<span data-ttu-id="d9af1-104">Com+-Ereignisse bieten zwei Möglichkeiten, um zu steuern, welche Ereignisse die folgenden Abonnenten erreichen: *Herausgeber Filterung* und *Parameter Filterung*.</span><span class="sxs-lookup"><span data-stu-id="d9af1-104">COM+ Events provides two ways to control which events reach which subscribers: *publisher filtering* and *parameter filtering*.</span></span>

## <a name="publisher-filtering"></a><span data-ttu-id="d9af1-105">Herausgeber Filterung</span><span class="sxs-lookup"><span data-stu-id="d9af1-105">Publisher Filtering</span></span>

<span data-ttu-id="d9af1-106">Die Herausgeber Filterung steuert die Reihenfolge und das Auslösen einer Ereignismethode durch ein [Ereignis Klassen](the-com--event-class-object.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="d9af1-106">Publisher filtering controls the order and firing of an event method by an [event class](the-com--event-class-object.md) object.</span></span> <span data-ttu-id="d9af1-107">Die Herausgeber Filterung ermöglicht dem Verleger, zu bestimmen, welche Abonnenten ein bestimmtes Ereignis erhalten.</span><span class="sxs-lookup"><span data-stu-id="d9af1-107">Publisher filtering allows the publisher to determine which subscribers receive a particular event.</span></span>

<span data-ttu-id="d9af1-108">Ein Beispiel für die effektive Verwendung der Herausgeber Filterung ist die von einem Aktien Austausch.</span><span class="sxs-lookup"><span data-stu-id="d9af1-108">An example of effective use of publisher filtering is that of a stock exchange.</span></span> <span data-ttu-id="d9af1-109">Die meisten Abonnenten möchten wissen, wann ein neuer bestand hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d9af1-109">Most subscribers want to know when a new stock is added.</span></span> <span data-ttu-id="d9af1-110">Viele dieser Abonnenten möchten jedoch möglicherweise nicht wissen, wann jeder Aktienkurs geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d9af1-110">However, many of these same subscribers may not want to know whenever each stock price changes.</span></span> <span data-ttu-id="d9af1-111">Die Herausgeber Filterung bietet die Granularität, die für die effektive Bereitstellung von Ereignissen an die Abonnenten erforderlich ist, die diese Informationen wünschen</span><span class="sxs-lookup"><span data-stu-id="d9af1-111">Publisher filtering provides the granularity required to effectively deliver events to only the subscribers who want this information.</span></span>

<span data-ttu-id="d9af1-112">Wenn eine Methode für das instanziierte Ereignis Klassenobjekt aufgerufen wird, sammelt Sie alle Verleger Filter für diese Methode.</span><span class="sxs-lookup"><span data-stu-id="d9af1-112">When a method is invoked on the instantiated event class object, it collects any publisher filters on that method.</span></span> <span data-ttu-id="d9af1-113">Der Filter erzwingt, dass das Ereignis Objekt die Ereignismethode für einen bestimmten Abonnenten auslöst.</span><span class="sxs-lookup"><span data-stu-id="d9af1-113">The filter forces the event object to fire the event method to a specific subscriber.</span></span> <span data-ttu-id="d9af1-114">Der Filter bestimmt, welche Abonnements ausgelöst werden und in welcher Reihenfolge Sie ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="d9af1-114">The filter determines which subscriptions to fire and in which order to fire them.</span></span> <span data-ttu-id="d9af1-115">Beispielsweise könnte der Filter die Abonnementliste lesen und die Reihenfolge basierend auf einigen Anwendungskriterien erstellen und dann die Abonnenten in dieser Reihenfolge aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d9af1-115">For example, the filter could read the subscription list and create the order based on some application criteria and then call the subscribers in that order.</span></span>

<span data-ttu-id="d9af1-116">Ausführliche Anweisungen zum Erstellen eines Herausgeber Filters finden Sie unter [Erstellen eines Herausgeber Filters](creating-a-publisher-filter.md).</span><span class="sxs-lookup"><span data-stu-id="d9af1-116">For detailed instructions on creating a publisher filter, see [Creating a Publisher Filter](creating-a-publisher-filter.md).</span></span>

## <a name="parameter-filtering"></a><span data-ttu-id="d9af1-117">Parameterfilterung</span><span class="sxs-lookup"><span data-stu-id="d9af1-117">Parameter Filtering</span></span>

<span data-ttu-id="d9af1-118">Anders als bei der Herausgeber Filterung bietet der com+-Ereignis Dienst eine optionale Filterung von Abonnenten Parametern für jedes Abonnement und jeden Aufruf der Ereignismethode.</span><span class="sxs-lookup"><span data-stu-id="d9af1-118">In contrast to publisher filtering, the COM+ Events service provides an optional subscriber parameter filtering for each subscription and each event method invocation.</span></span> <span data-ttu-id="d9af1-119">Durch die Parameter Filterung wird die Eigenschaft "filterCriteria" des Abonnements mit den Parametern der Ereignismethode ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="d9af1-119">Parameter filtering evaluates the subscription FilterCriteria property against the parameters of the event method.</span></span> <span data-ttu-id="d9af1-120">Dieser Filtertyp wird pro Methode und pro Abonnement verwendet und bietet eine Ebene der Abonnenten Filterung an der Ereignis Quelle.</span><span class="sxs-lookup"><span data-stu-id="d9af1-120">This type of filtering is used on a per-method, per-subscription basis and provides a level of subscriber filtering at the event source.</span></span> <span data-ttu-id="d9af1-121">Die Filter Kriterienzeichenfolge erkennt relationale Operatoren zum Überprüfen von Gleichheit (=, = =,!,! =, ~, ~ =,  <>), geschachtelten Klammern und logischen Schlüsselwörtern **und**, **or** oder **Not**.</span><span class="sxs-lookup"><span data-stu-id="d9af1-121">The filter criteria string recognizes relational operators for checking equality (=, ==, !, !=, ~, ~=, <>), nested parentheses, and logical keywords **AND**, **OR**, or **NOT**.</span></span>

<span data-ttu-id="d9af1-122">Die Parameter Filterung erfolgt nach dem Filtern aller Verleger und beim Auslösen des Standard Ereignis Objekts für ein bestimmtes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9af1-122">Parameter filtering occurs after any publisher filtering and when the standard event object is fired for a given subscription.</span></span> <span data-ttu-id="d9af1-123">Wenn die Herausgeber Filterung verwendet wird, erfolgt die Parameter Filterung nur, wenn der Verleger Filter [**ifiringcontrol:: fireabonnement**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription)aufruft.</span><span class="sxs-lookup"><span data-stu-id="d9af1-123">If publisher filtering is used, parameter filtering occurs only when the publisher filter invokes [**IFiringControl::FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription).</span></span> <span data-ttu-id="d9af1-124">Aus diesem Grund können Herausgeber Filterung und Parameter Filterung zusammen verfasst werden, aber die Herausgeber Filterung hat Vorrang.</span><span class="sxs-lookup"><span data-stu-id="d9af1-124">Because of this, publisher filtering and parameter filtering can compose together but publisher filtering takes precedence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9af1-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d9af1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9af1-126">Veröffentlichen und Bereitstellung von Ereignissen in com+</span><span class="sxs-lookup"><span data-stu-id="d9af1-126">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="d9af1-127">Abonnements</span><span class="sxs-lookup"><span data-stu-id="d9af1-127">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="d9af1-128">Das com+-Ereignis Klassenobjekt</span><span class="sxs-lookup"><span data-stu-id="d9af1-128">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="d9af1-129">Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="d9af1-129">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



