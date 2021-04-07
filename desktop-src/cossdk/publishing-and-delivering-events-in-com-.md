---
description: Zum Veröffentlichen eines Ereignisses instanziieren Sie einfach ein Ereignis Klassenobjekt, und rufen Sie die gewünschte Methode auf. Ausführliche Anweisungen dazu, wie Sie dies in Code tun, finden Sie unter Veröffentlichen eines Ereignisses.
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: Veröffentlichen und Bereitstellung von Ereignissen in com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a444b64501156191590c115d6000f4c0bda153
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748856"
---
# <a name="publishing-and-delivering-events-in-com"></a><span data-ttu-id="555b6-103">Veröffentlichen und Bereitstellung von Ereignissen in com+</span><span class="sxs-lookup"><span data-stu-id="555b6-103">Publishing and Delivering Events in COM+</span></span>

<span data-ttu-id="555b6-104">Zum Veröffentlichen eines Ereignisses instanziieren Sie einfach ein [Ereignis Klassen](the-com--event-class-object.md) Objekt, und rufen Sie die gewünschte Methode auf. Ausführliche Anweisungen dazu, wie Sie dies in Code tun, finden Sie unter [Veröffentlichen eines Ereignisses](publishing-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="555b6-104">To publish an event, simply instantiate an [event class](the-com--event-class-object.md) object and invoke the desired method; for detailed instructions on how to do this in code, see [Publishing an Event](publishing-an-event.md).</span></span>

<span data-ttu-id="555b6-105">Wenn ein Verleger ein Ereignis auslöst, durchsucht der com+-Ereignis Dienst die Abonnement Datenbank, um alle Abonnenten zu suchen, die Abonnements für die instanziierte Ereignisklasse registriert haben.</span><span class="sxs-lookup"><span data-stu-id="555b6-105">When a publisher fires an event, the COM+ Events service searches the subscription database to find all the subscribers who have registered subscriptions to the instantiated event class.</span></span> <span data-ttu-id="555b6-106">Sie stellt eine Verbindung mit diesen Abonnenten her (durch direkte Erstellung, Moniker oder in der Warteschlange befindliche Komponenten) und ruft die-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="555b6-106">It connects to those subscribers (by direct creation, monikers, or queued components) and calls the method.</span></span> <span data-ttu-id="555b6-107">Um mehr als eine Abonnenten Benachrichtigung für ein Ereignis zu unterstützen, können-Methoden nur in-Parameter enthalten und dürfen nur Erfolgs-oder Fehler- **HRESULT** -Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="555b6-107">To support more than one subscriber notification for an event, methods can contain only in parameters and must return only success or failure **HRESULT** values.</span></span>

> [!Note]  
> <span data-ttu-id="555b6-108">Diese Version von COM+-Ereignissen unterstützt keinen verteilten Ereignisspeicher.</span><span class="sxs-lookup"><span data-stu-id="555b6-108">This version of COM+ events does not support a distributed event store.</span></span> <span data-ttu-id="555b6-109">Ein Abonnent muss ein Ereignis auf jedem Computer abonnieren, von dem aus eine Benachrichtigung empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="555b6-109">A subscriber must subscribe to an event on each computer from which it wants to receive notification.</span></span> <span data-ttu-id="555b6-110">Als Alternative können Sie das Ereignis Klassenobjekt und die Abonnements auf einem zentralen Computer registrieren und dieses Ereignis Klassenobjekt von den Remote Computern, auf denen Ereignisse veröffentlicht werden, instanziieren.</span><span class="sxs-lookup"><span data-stu-id="555b6-110">As an alternative, you can register the event class object and subscriptions on a central computer and instantiate this event class object from the remote computers on which you publish events.</span></span> <span data-ttu-id="555b6-111">Die Übermittlung von Ereignissen wird entweder durch DCOM oder durch den com+-Dienst in der Warteschlange bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="555b6-111">Delivery of events is provided either by DCOM or by the COM+ queued components service.</span></span> <span data-ttu-id="555b6-112">Weitere Informationen zur Verwendung des-Dienstanbieter für die com+-Warteschlange finden Sie unter [Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange](using-com--events-with-com--queued-components.md)</span><span class="sxs-lookup"><span data-stu-id="555b6-112">For more information about using the COM+ queued components service, see [Using COM+ Events with COM+ Queued Components](using-com--events-with-com--queued-components.md).</span></span>

 

<span data-ttu-id="555b6-113">Standardmäßig löst der com+-Ereignis Dienst Ereignisse nacheinander in einer nicht ermittelten oder wiederholbaren Reihenfolge auf.</span><span class="sxs-lookup"><span data-stu-id="555b6-113">By default, the COM+ events service fires events one at a time, in no determined or repeatable order.</span></span> <span data-ttu-id="555b6-114">Herausgeber, die die Reihenfolge steuern müssen, in der Abonnenten ein Ereignis empfangen, können einen Herausgeber Filter implementieren.</span><span class="sxs-lookup"><span data-stu-id="555b6-114">Publishers that need to control the order in which subscribers receive an event can implement a publisher filter.</span></span> <span data-ttu-id="555b6-115">(Weitere Informationen finden Sie unter [Filtern von Ereignissen in com+](filtering-events-in-com-.md).)</span><span class="sxs-lookup"><span data-stu-id="555b6-115">(For more information, see [Filtering Events in COM+](filtering-events-in-com-.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="555b6-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="555b6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="555b6-117">Filtern von Ereignissen in com+</span><span class="sxs-lookup"><span data-stu-id="555b6-117">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="555b6-118">Abonnements</span><span class="sxs-lookup"><span data-stu-id="555b6-118">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="555b6-119">Das com+-Ereignis Klassenobjekt</span><span class="sxs-lookup"><span data-stu-id="555b6-119">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="555b6-120">Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="555b6-120">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



