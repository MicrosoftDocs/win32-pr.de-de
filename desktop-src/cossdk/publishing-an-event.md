---
description: Veröffentlichen eines Ereignisses
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Veröffentlichen eines Ereignisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344212"
---
# <a name="publishing-an-event"></a><span data-ttu-id="bf6b9-103">Veröffentlichen eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="bf6b9-103">Publishing an Event</span></span>

<span data-ttu-id="bf6b9-104">Zum Veröffentlichen eines Ereignisses instanziieren Sie einfach ein Ereignis Objekt, indem Sie [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder die Microsoft Visual Basic **CreateObject** -Methode mithilfe von eventclassid oder EventClassName als Argument aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bf6b9-104">To publish an event, just instantiate an event object by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or the Microsoft Visual Basic **CreateObject** method using EventClassID or EventClassName as an argument.</span></span> <span data-ttu-id="bf6b9-105">Der Verleger ruft [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das Ereignis Objekt auf, um die vom Ereignis Klassenobjekt unterstützten Schnittstellen zu erhalten, und ruft eine Methode für das Ereignis Objekt über die-Schnittstelle auf, um das Ereignis zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="bf6b9-105">The publisher calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the event object to obtain the interfaces supported by the event class object and invokes a method on the event object through the interface to publish the event.</span></span> <span data-ttu-id="bf6b9-106">Das Ereignis System veröffentlicht dann Ereignisse in der Ereignisklasse CLSID \_ eventobjectchange mit der Schnittstellen-ID IID \_ ieventobjectchange.</span><span class="sxs-lookup"><span data-stu-id="bf6b9-106">The event system then publishes events on the event class CLSID\_EventObjectChange with the interface ID IID\_IEventObjectChange.</span></span>

<span data-ttu-id="bf6b9-107">Um die Übermittlung von Ereignissen an mehrere Abonnenten zu unterstützen, sollten Ereignis Klassen Methoden nur in-Parametern enthalten.</span><span class="sxs-lookup"><span data-stu-id="bf6b9-107">To support delivery of events to multiple subscribers, event class methods should contain only in parameters.</span></span>

<span data-ttu-id="bf6b9-108">Mithilfe der Eigenschaft "freinparallel" des Objekts " [Event Class](the-com--event-class-object.md) " können Verleger anfordern, dass das Ereignis System mehrere Threads verwendet, um ein Ereignis an mehr als einen Abonnenten zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="bf6b9-108">By using the FireInParallel property of the [event class](the-com--event-class-object.md) object, publishers can request that the event system use multiple threads to deliver an event to more than one subscriber.</span></span> <span data-ttu-id="bf6b9-109">Die Auswahl eines parallelen Übermittlungs Mechanismus garantiert nicht die gleichzeitige Übermittlung des Ereignisses an mehrere Abonnenten, sondern weist den com+-Ereignis Dienst an, dies zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="bf6b9-109">Selecting an in-parallel delivery mechanism does not guarantee simultaneous delivery of the event to multiple subscribers, but it instructs the COM+ events service to permit this to happen.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf6b9-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bf6b9-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf6b9-111">Veröffentlichen und Bereitstellung von Ereignissen in com+</span><span class="sxs-lookup"><span data-stu-id="bf6b9-111">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
