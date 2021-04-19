---
description: Komponenten Fehler in der Warteschlange
ms.assetid: 29a1bf52-7252-4f8a-bdb7-61b152fb907e
title: Komponenten Fehler in der Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422ea9c7ff77f2d69633d6db8b8d48c63fabc071
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346447"
---
# <a name="queued-components-errors"></a><span data-ttu-id="4899b-103">Komponenten Fehler in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="4899b-103">Queued Components Errors</span></span>

<span data-ttu-id="4899b-104">Wenn ein Aufruf an eine in der Warteschlange befindliche Komponente fehlschlägt, weil Sie entweder nicht an den Server übertragen werden konnte (ein Client seitiger Fehler) oder weil Sie beim Eintreffen (serverseitiger Fehler) nicht ausgeführt werden konnte, wird die entsprechende [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Meldung als nicht verarbeitbare *Nachricht* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4899b-104">When a call to a queued component fails, either because it could not be transmitted to the server (a client-side failure) or because it failed to execute when it arrived (a server-side failure), the corresponding [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) message is called a *poison message*.</span></span>

<span data-ttu-id="4899b-105">Der Dienst "com+-Warteschlangen Komponenten" verarbeitet nicht verarbeitbare Nachrichten mithilfe einer Reihe von Wiederholungs Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="4899b-105">The COM+ queued components service handles poison messages by using a series of retry queues.</span></span> <span data-ttu-id="4899b-106">Nach mehreren Wiederholungs versuchen wird die Nachricht in eine letzte Warteschlange verschoben.</span><span class="sxs-lookup"><span data-stu-id="4899b-106">After several retries, the message is moved to a final resting queue.</span></span> <span data-ttu-id="4899b-107">Nachrichten bleiben in der ruhenden Warteschlange, bis Sie manuell mithilfe des Nachrichten verschiebungshilfsprogramms in der Warteschlange eingereiht werden.</span><span class="sxs-lookup"><span data-stu-id="4899b-107">Messages stay in the resting queue until they are moved manually by using the queued components message mover utility.</span></span> <span data-ttu-id="4899b-108">Weitere Informationen zur Verwendung des Nachrichten Verschiebungsvorgangs finden Sie unter [Behandeln von Fehlern](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="4899b-108">For more information about using the message mover, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

<span data-ttu-id="4899b-109">Ausführliche Beschreibungen der Ereignis Sequenz, die für verschiedene Arten von Fehlern auftritt, finden Sie in den Themen, die in der folgenden Tabelle beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4899b-109">Detailed descriptions of the sequence of events that occurs for various sorts of errors can be found in the topics described in the following table.</span></span>



| <span data-ttu-id="4899b-110">Thema</span><span class="sxs-lookup"><span data-stu-id="4899b-110">Topic</span></span>                                                                             | <span data-ttu-id="4899b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4899b-111">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4899b-112">Server seitige Fehler</span><span class="sxs-lookup"><span data-stu-id="4899b-112">Server-Side Errors</span></span>](server-side-errors.md)<br/>                           | <span data-ttu-id="4899b-113">Beschreibt ausführlich die Antwort des Dienstanbieter der com+-Warteschlange auf einen serverseitigen Fehler.</span><span class="sxs-lookup"><span data-stu-id="4899b-113">Describes in detail the response of the COM+ queued components service to a server-side failure.</span></span><br/>             |
| [<span data-ttu-id="4899b-114">Client seitige Fehler</span><span class="sxs-lookup"><span data-stu-id="4899b-114">Client-Side Errors</span></span>](client-side-errors.md)<br/>                           | <span data-ttu-id="4899b-115">Beschreibt ausführlich die Antwort des Dienstanbieter der com+-Warteschlange auf einen Client seitigen Fehler.</span><span class="sxs-lookup"><span data-stu-id="4899b-115">Describes in detail the response of the COM+ queued components service to a client-side failure.</span></span><br/>             |
| [<span data-ttu-id="4899b-116">Persistente Client-Side Fehler</span><span class="sxs-lookup"><span data-stu-id="4899b-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)<br/> | <span data-ttu-id="4899b-117">Beschreibt im Detail die Antwort des com+-Dienstanbieter für die Warteschlange auf wiederholte Client seitige Fehler.</span><span class="sxs-lookup"><span data-stu-id="4899b-117">Describes in the detail the response of the COM+ queued components service to repeated client-side failures.</span></span><br/> |



 

 

 




