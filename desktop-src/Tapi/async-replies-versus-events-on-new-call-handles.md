---
description: TSPI umfasst eine Reihe von Vorgängen, mit denen die Lebensdauer eines Rückruf Handles gestartet wird.
ms.assetid: 28e171a3-db47-40fd-9c5a-d7b76d834a99
title: Asynchrone Antworten und Ereignisse bei neuen aufrufshandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02511a083c318afb227e3e172191d3ab84a69fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866603"
---
# <a name="async-replies-versus-events-on-new-call-handles"></a><span data-ttu-id="b617f-103">Asynchrone Antworten und Ereignisse bei neuen aufrufshandles</span><span class="sxs-lookup"><span data-stu-id="b617f-103">Async Replies versus Events on New Call Handles</span></span>

<span data-ttu-id="b617f-104">TSPI umfasst eine Reihe von Vorgängen, mit denen die Lebensdauer eines Rückruf Handles gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b617f-104">TSPI includes a number of operations that start the lifetime of a call handle.</span></span> <span data-ttu-id="b617f-105">Wenn der Dienstanbieter einen Erfolg für einen solchen Vorgang zurückgibt, muss er den nicht transparenten Handle des Typs " **hdrvcall"** ausfüllen, der für den neuen-Befehl verwendet wird, bevor er zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b617f-105">If the service provider returns SUCCESS for such an operation, it must fill in the opaque handle of type **HDRVCALL**, which it uses for the new call before it returns.</span></span> <span data-ttu-id="b617f-106">TAPI führt niemals Vorgänge für den-Befehl aus, bevor die entsprechende Abschluss Prozedur empfangen wurde. [*\_*](/windows/win32/api/tspi/nc-tspi-async_completion)</span><span class="sxs-lookup"><span data-stu-id="b617f-106">TAPI never performs operations on the call before the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) has been received.</span></span> <span data-ttu-id="b617f-107">Wenn der Dienstanbieter einen Fehler zurückgibt, wird das Handle automatisch ungültig (d. h. ohne [**TSPI \_ lineclosecall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)).</span><span class="sxs-lookup"><span data-stu-id="b617f-107">If the service provider returns FAILURE, the handle automatically becomes invalid (that is, without [**TSPI\_lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)).</span></span> <span data-ttu-id="b617f-108">In der Tat behandelt TAPI das Handle als "noch nicht gültig", bis der asynchrone Abschluss abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b617f-108">In effect, TAPI treats the handle as "not yet valid" until the asynchronous completion.</span></span>

<span data-ttu-id="b617f-109">Der Dienstanbieter muss das Handle auch als "noch nicht gültig" behandeln, bis der entsprechende [*Abschluss \_ proc*](/windows/win32/api/tspi/nc-tspi-async_completion) -Prozess empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="b617f-109">The service provider must also treat the handle as "not yet valid" until after the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) is received.</span></span> <span data-ttu-id="b617f-110">Anders ausgedrückt: Es darf keine [*Zeilen \_ Ereignis*](/windows/win32/api/tspi/nc-tspi-lineevent) Funktionen für den neuen-Befehl ausgeben oder in die Anzahl von Aufrufen in Nachrichten oder Statusdaten Strukturen für die Zeile einschließen.</span><span class="sxs-lookup"><span data-stu-id="b617f-110">In other words, it must not issue any [*Line\_Event*](/windows/win32/api/tspi/nc-tspi-lineevent) functions for the new call or include it in call counts in messages or status data structures for the line.</span></span>

<span data-ttu-id="b617f-111">Die TAPI-Ebene entspricht auch diesen Lebenszyklus Einschränkungen. ein neues-Rückruf Handle wird erst zurückgegeben oder gültig, wenn die übereinstimmende [**Zeilen \_ Antwort**](./line-reply.md) Nachricht und keine Ereignisse für den neuen-Befehl an die Anwendung übermittelt werden, bis die Zeilen \_ Antwortnachricht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b617f-111">The TAPI level also conforms to these life cycle restrictions; a new call handle is not returned or valid until the matching [**LINE\_REPLY**](./line-reply.md) message, and no events for the new call are delivered to the application until after the LINE\_REPLY message.</span></span>

<span data-ttu-id="b617f-112">Die TSPI-Vorgänge, auf die das Prinzip "Start Lebensdauer" angewendet wird, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b617f-112">The TSPI operations to which this "start lifetime" principle applies are the following:</span></span>

-   [<span data-ttu-id="b617f-113">**TSPI \_ linecompletetransfer**</span><span class="sxs-lookup"><span data-stu-id="b617f-113">**TSPI\_lineCompleteTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [<span data-ttu-id="b617f-114">**TSPI ( \_ lineforward)**</span><span class="sxs-lookup"><span data-stu-id="b617f-114">**TSPI\_lineForward**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [<span data-ttu-id="b617f-115">**TSPI \_ linemakecall**</span><span class="sxs-lookup"><span data-stu-id="b617f-115">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [<span data-ttu-id="b617f-116">**TSPI- \_ linepickup**</span><span class="sxs-lookup"><span data-stu-id="b617f-116">**TSPI\_linePickup**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [<span data-ttu-id="b617f-117">**TSPI \_ lineprepareaddumconference**</span><span class="sxs-lookup"><span data-stu-id="b617f-117">**TSPI\_linePrepareAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [<span data-ttu-id="b617f-118">**TSPI \_ linesetupconference**</span><span class="sxs-lookup"><span data-stu-id="b617f-118">**TSPI\_lineSetupConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [<span data-ttu-id="b617f-119">**TSPI \_ lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="b617f-119">**TSPI\_lineSetupTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [<span data-ttu-id="b617f-120">**TSPI \_ lineunpark**</span><span class="sxs-lookup"><span data-stu-id="b617f-120">**TSPI\_lineUnpark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
