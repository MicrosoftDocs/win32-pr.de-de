---
description: Der com+-Ereignis Dienst wird verwendet, um die Übermittlung von Ereignissen von Verlegern an Abonnenten zu verwalten.
ms.assetid: 0945163b-1276-47f6-ae7f-9d932a1b586d
title: Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be31dd1088b720902295738c23173c28145cef2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346862"
---
# <a name="using-com-events-with-com-queued-components"></a><span data-ttu-id="75b46-103">Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="75b46-103">Using COM+ Events with COM+ Queued Components</span></span>

<span data-ttu-id="75b46-104">Der com+-Ereignis Dienst wird verwendet, um die Übermittlung von Ereignissen von Verlegern an Abonnenten zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="75b46-104">The COM+ events service is used to manage the delivery of events from publishers to subscribers.</span></span> <span data-ttu-id="75b46-105">Der Dienst "com+-Warteschlangen Komponenten" kann verwendet werden, um die Verarbeitungszeit des Verlegers und des Abonnenten unabhängig voneinander zu machen, indem die Verleger Nachricht in die Warteschlange eingereiht wird</span><span class="sxs-lookup"><span data-stu-id="75b46-105">The COM+ queued components service can be used to make the publisher and subscriber processing time independent by queuing the publisher's message and later replaying it to the subscriber.</span></span> <span data-ttu-id="75b46-106">Ob Sie den Dienst für die Warteschlangen Dienste verwenden müssen, hängt von der zugrunde liegenden Geschäftslogik Ihrer Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="75b46-106">Whether or not you need to use the queued components service depends on the underlying business logic of your application.</span></span> <span data-ttu-id="75b46-107">Wenn Sie Ereignisse haben müssen, die Zeit unabhängig sind, können Sie diese mithilfe des com+-Ereignis Dienstanbieter mit den COM+-Diensten in der Warteschlange erstellen.</span><span class="sxs-lookup"><span data-stu-id="75b46-107">If you need to have events that are time independent, you can create them by using the COM+ events service with COM+ queued components service.</span></span>

> [!Note]  
> <span data-ttu-id="75b46-108">Weitere Informationen zur Verwendung des-Dienstanbieter für die com+-Warteschlange finden Sie unter [com+-Komponenten in der Warteschlange](com--queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="75b46-108">For additional information about using the COM+ queued components service, see [COM+ Queued Components](com--queued-components.md).</span></span>

 

<span data-ttu-id="75b46-109">Der Dienst für in der Warteschlange befindliche Komponenten verwaltet den Aufruf der Aufruf Reihenfolge in einer einzelnen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="75b46-109">The queued components service maintains order-of-method invocation within a single message.</span></span> <span data-ttu-id="75b46-110">Der Recorder fasst alle Methodenaufrufe in eine Nachricht um. Anschließend ruft der Player diese Methoden in der Reihenfolge auf, in der die Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="75b46-110">The recorder batches all method invocations into a message, and then the player invokes those methods in order when the message is processed.</span></span>

<span data-ttu-id="75b46-111">Eine in der Warteschlange befindliche Komponenten Aufzeichnung und ein Player können an einem der beiden folgenden Stellen positioniert werden:</span><span class="sxs-lookup"><span data-stu-id="75b46-111">A queued components recorder and player can be positioned in either of the following two places:</span></span>

-   <span data-ttu-id="75b46-112">Zwischen dem Verleger und dem Ereignis Objekt</span><span class="sxs-lookup"><span data-stu-id="75b46-112">Between the publisher and event object</span></span>
-   <span data-ttu-id="75b46-113">Zwischen dem Ereignis Objekt und dem Abonnenten</span><span class="sxs-lookup"><span data-stu-id="75b46-113">Between the event object and subscriber</span></span>

<span data-ttu-id="75b46-114">Wenn Sie die Aufzeichnung und den Player zwischen dem Verleger und dem Ereignis Objekt positionieren, stellen Sie die [Ereignis Klassen](the-com--event-class-object.md) Komponente in die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="75b46-114">If you position the recorder and player between the publisher and event object, you are making the [event class](the-com--event-class-object.md) component queuable.</span></span> <span data-ttu-id="75b46-115">Die Ereignis Klassen Komponente muss für die Warteschlange markiert und vom Player in einem Prozess aktiviert werden, der vom Verleger getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="75b46-115">The event class component must be marked for queuing and be activated by the player in a process that is separate from the publisher.</span></span>

<span data-ttu-id="75b46-116">Um Ereignisse asynchron zu übermitteln, verfassen Sie den Recorder und den Player zwischen dem Ereignis Objekt und dem Abonnenten, und legen Sie das Attribut in der Warteschlange des Abonnement Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="75b46-116">To deliver events asynchronously, compose the recorder and player between the event object and subscriber and set the Queued attribute of the subscription object.</span></span> <span data-ttu-id="75b46-117">Hierdurch wird der Abonnement Name wie folgt festgelegt: "Queue:/New:/ {12345678-1234-1234-1234-123456789012} ".</span><span class="sxs-lookup"><span data-stu-id="75b46-117">This sets SubscriberMoniker as follows: "queue:/new:/{12345678-1234-1234-1234-123456789012}".</span></span>

<span data-ttu-id="75b46-118">Bei der Verwendung von in der Warteschlange befindlichen Komponenten in einer Ereignis Situation ist eine Reihenfolge der Übermittlungs Implikation zu beachten.</span><span class="sxs-lookup"><span data-stu-id="75b46-118">There is an order of delivery implication to consider when using queued components in an event situation.</span></span> <span data-ttu-id="75b46-119">Da die in der Warteschlange befindlichen Komponenten alle Aufrufe innerhalb der Lebensdauer eines einzelnen Objekts in einer Nachricht aufzeichnet und wieder gibt, werden alle Aufrufe in der Reihenfolge wiedergegeben, in der Sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="75b46-119">Because the queued components service records and plays back all calls within the lifetime of a single object in one message, all calls are replayed in the order in which they were made.</span></span> <span data-ttu-id="75b46-120">Wenn jedoch mehr als eine Sitzung mit mehreren Objekten vorhanden ist, kann die Reihenfolge nicht garantiert werden.</span><span class="sxs-lookup"><span data-stu-id="75b46-120">However, if there is more than one session with more than one object, order cannot be guaranteed.</span></span> <span data-ttu-id="75b46-121">Wenn die Reihenfolge wichtig ist, stellen Sie sicher, dass Aufrufe, die in der Reihenfolge wiedergegeben werden müssen, sich in derselben Objektinstanz befinden.</span><span class="sxs-lookup"><span data-stu-id="75b46-121">If order is important, make sure that calls that need to be played back in order reside on the same object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75b46-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75b46-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75b46-123">Filtern von Ereignissen in com+</span><span class="sxs-lookup"><span data-stu-id="75b46-123">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="75b46-124">Veröffentlichen und Bereitstellung von Ereignissen in com+</span><span class="sxs-lookup"><span data-stu-id="75b46-124">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="75b46-125">Abonnements</span><span class="sxs-lookup"><span data-stu-id="75b46-125">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="75b46-126">Das com+-Ereignis Klassenobjekt</span><span class="sxs-lookup"><span data-stu-id="75b46-126">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



