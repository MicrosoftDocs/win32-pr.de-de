---
description: In diesem Thema werden Timer erläutert. Ein Timer ist eine interne Routine, die wiederholt ein angegebenes Intervall in Millisekunden misst.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa44be05acc09eafed550a200ed6bc61f79daa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362711"
---
# <a name="timers"></a><span data-ttu-id="8dfa3-104">Timer</span><span class="sxs-lookup"><span data-stu-id="8dfa3-104">Timers</span></span>

<span data-ttu-id="8dfa3-105">Ein Timer ist eine interne Routine, die wiederholt ein angegebenes Intervall in Millisekunden misst.</span><span class="sxs-lookup"><span data-stu-id="8dfa3-105">A timer is an internal routine that repeatedly measures a specified interval, in milliseconds.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="8dfa3-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="8dfa3-106">In This Section</span></span>



| <span data-ttu-id="8dfa3-107">Name</span><span class="sxs-lookup"><span data-stu-id="8dfa3-107">Name</span></span>                                   | <span data-ttu-id="8dfa3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8dfa3-108">Description</span></span>                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8dfa3-109">Informationen zu Timern</span><span class="sxs-lookup"><span data-stu-id="8dfa3-109">About Timers</span></span>](about-timers.md)       | <span data-ttu-id="8dfa3-110">Beschreibt, wie Timer erstellt, identifiziert, festgelegt und gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="8dfa3-110">Describes how to create, identify, set, and delete timers.</span></span><br/>                                                     |
| [<span data-ttu-id="8dfa3-111">Verwenden von Timern</span><span class="sxs-lookup"><span data-stu-id="8dfa3-111">Using Timers</span></span>](using-timers.md)       | <span data-ttu-id="8dfa3-112">Erläutert, wie Timer erstellt und zerstört werden und wie ein Timer verwendet wird, um Maus Eingaben in angegebenen Intervallen abzufangen.</span><span class="sxs-lookup"><span data-stu-id="8dfa3-112">Discusses how to create and destroy timers, and how to use a timer to trap mouse input at specified intervals.</span></span><br/> |
| [<span data-ttu-id="8dfa3-113">Timer-Verweis</span><span class="sxs-lookup"><span data-stu-id="8dfa3-113">Timer Reference</span></span>](timer-reference.md) | <span data-ttu-id="8dfa3-114">Enthält die API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="8dfa3-114">Contains the API reference.</span></span><br/>                                                                                    |



 

### <a name="timer-functions"></a><span data-ttu-id="8dfa3-115">Timer-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8dfa3-115">Timer Functions</span></span>



| <span data-ttu-id="8dfa3-116">Name</span><span class="sxs-lookup"><span data-stu-id="8dfa3-116">Name</span></span>                           | <span data-ttu-id="8dfa3-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8dfa3-117">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8dfa3-118">**Killtimer Memberfunktion**</span><span class="sxs-lookup"><span data-stu-id="8dfa3-118">**KillTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-killtimer) | <span data-ttu-id="8dfa3-119">Zerstört den angegebenen Timer.</span><span class="sxs-lookup"><span data-stu-id="8dfa3-119">Destroys the specified timer.</span></span> <br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="8dfa3-120">**Ziel**</span><span class="sxs-lookup"><span data-stu-id="8dfa3-120">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)   | <span data-ttu-id="8dfa3-121">Erstellt einen Timer mit dem angegebenen Timeout Wert.</span><span class="sxs-lookup"><span data-stu-id="8dfa3-121">Creates a timer with the specified time-out value.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="8dfa3-122">*Timerproc*</span><span class="sxs-lookup"><span data-stu-id="8dfa3-122">*TimerProc*</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)   | <span data-ttu-id="8dfa3-123">Eine Anwendungs definierte Rückruffunktion, die [**WM- \_**](wm-timer.md) Zeit Geber Nachrichten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8dfa3-123">An application-defined callback function that processes [**WM\_TIMER**](wm-timer.md) messages.</span></span> <span data-ttu-id="8dfa3-124">Der **timerproc** -Typ definiert einen Zeiger auf diese Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="8dfa3-124">The **TIMERPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="8dfa3-125">[*Timerproc*](/windows/win32/api/winuser/nc-winuser-timerproc) ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="8dfa3-125">[*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) is a placeholder for the application-defined function name.</span></span> <br/> |



 

### <a name="timer-notifications"></a><span data-ttu-id="8dfa3-126">Timer-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="8dfa3-126">Timer Notifications</span></span>



| <span data-ttu-id="8dfa3-127">Name</span><span class="sxs-lookup"><span data-stu-id="8dfa3-127">Name</span></span>                          | <span data-ttu-id="8dfa3-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8dfa3-128">Description</span></span>                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8dfa3-129">**WM- \_ Timer**</span><span class="sxs-lookup"><span data-stu-id="8dfa3-129">**WM\_TIMER**</span></span>](wm-timer.md) | <span data-ttu-id="8dfa3-130">Wird in der Meldungs Warteschlange des Installations Threads gepostet, wenn ein Timer abläuft.</span><span class="sxs-lookup"><span data-stu-id="8dfa3-130">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="8dfa3-131">Die Nachricht wird von der [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion oder der [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) -Funktion gepostet.</span><span class="sxs-lookup"><span data-stu-id="8dfa3-131">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span> <br/> |



 

 

 
