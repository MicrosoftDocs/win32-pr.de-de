---
title: Ereignis Sperrung
description: Ereignis Sperrung
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e403448d53949c263b8e146961690de1200436c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856044"
---
# <a name="event-freezing"></a><span data-ttu-id="c4318-103">Ereignis Sperrung</span><span class="sxs-lookup"><span data-stu-id="c4318-103">Event Freezing</span></span>

<span data-ttu-id="c4318-104">Ein Container kann ein Steuerelement benachrichtigen, dass er nicht bereit ist, auf Ereignisse zu reagieren, indem er [**IOleControl:: frezeevents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) mit **true** aufruft.</span><span class="sxs-lookup"><span data-stu-id="c4318-104">A container can notify a control that it is not ready to respond to events by calling [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE**.</span></span> <span data-ttu-id="c4318-105">Das Einfrieren der Ereignisse kann durch Aufrufen von " **frezeevents** mit **false**" aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="c4318-105">It can unfreeze the events by calling **FreezeEvents** with **FALSE**.</span></span> <span data-ttu-id="c4318-106">Wenn ein Container Ereignisse friert, wird die Ereignisverarbeitung eingefroren, und es wird kein Ereignis empfangen. Das heißt, ein Container kann weiterhin Ereignisse empfangen, während Ereignisse eingefroren werden.</span><span class="sxs-lookup"><span data-stu-id="c4318-106">When a container freezes events, it is freezing event processing, not event receiving; that is, a container can still receive events while events are frozen.</span></span> <span data-ttu-id="c4318-107">Wenn ein Container eine Ereignis Benachrichtigung empfängt, während seine Ereignisse eingefroren sind, sollte der Container das Ereignis ignorieren.</span><span class="sxs-lookup"><span data-stu-id="c4318-107">If a container receives an event notification while its events are frozen, the container should ignore the event.</span></span> <span data-ttu-id="c4318-108">Es ist keine weitere Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4318-108">No other action is appropriate.</span></span>

<span data-ttu-id="c4318-109">Ein Steuerelement sollte den Aufrufen von " [**frezeevents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) " eines Containers mit " **true** " notieren, wenn es für das Steuerelement wichtig ist, dass ein Ereignis nicht übersehen wird.</span><span class="sxs-lookup"><span data-stu-id="c4318-109">A control should take note of a container's call to [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE** if it is important to the control that an event is not missed.</span></span> <span data-ttu-id="c4318-110">Während die Ereignisverarbeitung eines Containers eingefroren ist, sollte ein Steuerelement eine der folgenden Techniken implementieren:</span><span class="sxs-lookup"><span data-stu-id="c4318-110">While a container's event processing is frozen, a control should implement one of the following techniques:</span></span>

-   <span data-ttu-id="c4318-111">Lösen Sie die Ereignisse in den vollständigen Kenntnissen aus, dass der Container keine Aktion durchführt.</span><span class="sxs-lookup"><span data-stu-id="c4318-111">Fire the events in the full knowledge that the container will take no action.</span></span>
-   <span data-ttu-id="c4318-112">Verwerfen Sie alle Ereignisse, die das Steuerelement ausgelöst hätte.</span><span class="sxs-lookup"><span data-stu-id="c4318-112">Discard all events that the control would have fired.</span></span>
-   <span data-ttu-id="c4318-113">Richten Sie alle ausstehenden Ereignisse in die Warteschlange ein, und lösen Sie Sie aus, nachdem der Container " [**frezeevents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) " mit **false**</span><span class="sxs-lookup"><span data-stu-id="c4318-113">Queue up all pending events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>
-   <span data-ttu-id="c4318-114">Richten Sie nur relevante oder wichtige Ereignisse in die Warteschlange ein, und lösen Sie Sie aus, nachdem der Container " [**frezeevents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) " mit **false**</span><span class="sxs-lookup"><span data-stu-id="c4318-114">Queue up only relevant or important events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>

<span data-ttu-id="c4318-115">Jede Technik ist akzeptabel und in unterschiedlichen Situationen angemessen.</span><span class="sxs-lookup"><span data-stu-id="c4318-115">Each technique is acceptable and appropriate in different circumstances.</span></span> <span data-ttu-id="c4318-116">Der Entwickler des Steuer Elements ist verantwortlich für die Bestimmung und Implementierung der entsprechenden Technik für die Funktionalität des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="c4318-116">The control developer is responsible for determining and implementing the appropriate technique for the control's functionality.</span></span>

 

 




