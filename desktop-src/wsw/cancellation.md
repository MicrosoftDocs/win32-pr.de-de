---
title: Abbruch
description: Die meisten Vorgänge in der wwsapi können während der Ausführung abgebrochen werden.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Abbrechen von Webdiensten für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e979455e898922dfb7c81381c1f1aafd455274
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316850"
---
# <a name="cancellation"></a><span data-ttu-id="1ee7f-106">Abbruch</span><span class="sxs-lookup"><span data-stu-id="1ee7f-106">Cancellation</span></span>

<span data-ttu-id="1ee7f-107">Die meisten Vorgänge in der wwsapi können während der Ausführung abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-107">Most of operations in the WWSAPI can be canceled during execution.</span></span>

<span data-ttu-id="1ee7f-108">Die Funktion, mit der ein Vorgang abgebrochen wird, hängt vom betroffenen Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-108">Which function you use to cancel an operation depends on the object affected.</span></span>

| <span data-ttu-id="1ee7f-109">Funktion</span><span class="sxs-lookup"><span data-stu-id="1ee7f-109">Function</span></span>                                           | <span data-ttu-id="1ee7f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ee7f-110">Description</span></span>                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ee7f-111">**Wsabortchannel**</span><span class="sxs-lookup"><span data-stu-id="1ee7f-111">**WsAbortChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | <span data-ttu-id="1ee7f-112">Bricht alle ausstehenden Eingaben und Ausgaben für einen angegebenen Kanal ab und legt den Kanal Zustand auf den WS- \_ Kanalstatus Fehler fest \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1ee7f-112">Cancels all pending input and output on a specified channel and sets the channel state to WS\_CHANNEL\_STATE\_FAULTED.</span></span> |
| [<span data-ttu-id="1ee7f-113">**Wsabortlistener**</span><span class="sxs-lookup"><span data-stu-id="1ee7f-113">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | <span data-ttu-id="1ee7f-114">Bricht alle ausstehenden Eingaben und Ausgaben für einen angegebenen Listener ab.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-114">Cancels all pending input and output on a specified listener.</span></span>                                                          |
| [<span data-ttu-id="1ee7f-115">**Wsabortserviceproxy**</span><span class="sxs-lookup"><span data-stu-id="1ee7f-115">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | <span data-ttu-id="1ee7f-116">Bricht alle ausstehenden Eingaben und Ausgaben für einen angegebenen Dienst Proxy ab.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-116">Cancels all pending input and output on a specified service proxy.</span></span>                                                     |
| [<span data-ttu-id="1ee7f-117">**Wsabortservicehost**</span><span class="sxs-lookup"><span data-stu-id="1ee7f-117">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | <span data-ttu-id="1ee7f-118">Unterbricht und beendet die aktuellen Vorgänge auf dem Dienst Host.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-118">Interrupts and discontinues current operations on the service host.</span></span>                                                    |
| [<span data-ttu-id="1ee7f-119">**Wsabandoncall**</span><span class="sxs-lookup"><span data-stu-id="1ee7f-119">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | <span data-ttu-id="1ee7f-120">Bricht einen-Befehl ab, einen angegebenen-Rückruf für einen angegebenen Dienst Proxy.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-120">Abandons a call, a specified call on a specified service proxy.</span></span>                                                        |



 

<span data-ttu-id="1ee7f-121">Informationen zu Stornierungen, die [serverseitige Dienst Vorgänge](server-side-service-operations.md) und Dienstmodell Rückrufe betreffen, finden Sie unter [Aufruf Abbruch](call-cancellation.md).</span><span class="sxs-lookup"><span data-stu-id="1ee7f-121">For information on cancellations that affect [server side service operations](server-side-service-operations.md) and service-model callbacks, see [Call Cancellation](call-cancellation.md).</span></span>


 

 




