---
title: Timer-Ereignis Vorgänge
description: Timer-Ereignis Vorgänge
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- Multimedia-Timer, Veranstaltungen
- Timer, Ereignisse
- timesetevent-Funktion
- timekillevent-Funktion
- Starten von Timer-Ereignissen
- Ereignisse mit nur einem Timer
- periodische Timer-Ereignisse
- Abbrechen von Zeit Geber Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d4329a6d6c55e9e8dd6c56fab5d1e3ca938833
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724800"
---
# <a name="timer-event-operations"></a><span data-ttu-id="bf423-111">Timer-Ereignis Vorgänge</span><span class="sxs-lookup"><span data-stu-id="bf423-111">Timer Event Operations</span></span>

<span data-ttu-id="bf423-112">Nachdem Sie die Zeit Geber Auflösung Ihrer Anwendung festgelegt haben, können Sie Timer-Ereignisse mithilfe der [**timesetevent**](/previous-versions//dd757634(v=vs.85)) -Funktion starten.</span><span class="sxs-lookup"><span data-stu-id="bf423-112">After you have established your application's timer resolution, you can start timer events by using the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function.</span></span> <span data-ttu-id="bf423-113">Diese Funktion gibt einen Zeit Geber Bezeichner zurück, der verwendet werden kann, um Zeit Geber Ereignisse anzuhalten oder zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bf423-113">This function returns a timer identifier that can be used to stop or identify timer events.</span></span> <span data-ttu-id="bf423-114">Einer der Parameter der Funktion ist die Adresse einer [**timeproc**](/previous-versions//dd757631(v=vs.85)) -Rückruffunktion, die aufgerufen wird, wenn das Timer-Ereignis stattfindet.</span><span class="sxs-lookup"><span data-stu-id="bf423-114">One of the function's parameters is the address of a [**TimeProc**](/previous-versions//dd757631(v=vs.85)) callback function that is called when the timer event takes place.</span></span>

<span data-ttu-id="bf423-115">Es gibt zwei Arten von Timer-Ereignissen: *Single* und *periodisch*.</span><span class="sxs-lookup"><span data-stu-id="bf423-115">There are two types of timer events: *single* and *periodic*.</span></span> <span data-ttu-id="bf423-116">Ein einzelnes Timer-Ereignis tritt einmal nach einer angegebenen Anzahl von Millisekunden auf.</span><span class="sxs-lookup"><span data-stu-id="bf423-116">A single timer event occurs once, after a specified number of milliseconds.</span></span> <span data-ttu-id="bf423-117">Jedes Mal, wenn eine angegebene Anzahl von Millisekunden verstrichen ist, tritt ein regelmäßiges Timer-Ereignis auf.</span><span class="sxs-lookup"><span data-stu-id="bf423-117">A periodic timer event occurs every time a specified number of milliseconds elapses.</span></span> <span data-ttu-id="bf423-118">Das Intervall zwischen periodischen Ereignissen wird als *Ereignis Verzögerung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf423-118">The interval between periodic events is called an *event delay*.</span></span> <span data-ttu-id="bf423-119">Periodische Timer-Ereignisse mit einer Ereignis Verzögerung von 10 Millisekunden oder weniger belegen einen erheblichen Anteil der CPU-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="bf423-119">Periodic timer events with an event delay of 10 milliseconds or less consume a significant portion of CPU resources.</span></span>

<span data-ttu-id="bf423-120">Die Beziehung zwischen der Auflösung eines Zeit Geber Ereignisses und der Länge der Ereignis Verzögerung ist in Zeit Geber Ereignissen wichtig.</span><span class="sxs-lookup"><span data-stu-id="bf423-120">The relationship between the resolution of a timer event and the length of the event delay is important in timer events.</span></span> <span data-ttu-id="bf423-121">Wenn Sie z. b. eine Auflösung von 5 und eine Ereignis Verzögerung von 100 angeben, benachrichtigen die Timer-Dienste die Rückruffunktion nach einem Intervall zwischen 95 und 105 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="bf423-121">For example, if you specify a resolution of 5 and an event delay of 100, the timer services notify the callback function after an interval ranging from 95 to 105 milliseconds.</span></span>

<span data-ttu-id="bf423-122">Sie können ein aktives Timer-Ereignis jederzeit mithilfe der [**timekillevent**](/previous-versions//dd757630(v=vs.85)) -Funktion abbrechen.</span><span class="sxs-lookup"><span data-stu-id="bf423-122">You can cancel an active timer event at any time by using the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function.</span></span> <span data-ttu-id="bf423-123">Stellen Sie sicher, dass Sie alle ausstehenden Timer abbrechen, bevor Sie den Speicher freigeben, der die Rückruffunktion enthält.</span><span class="sxs-lookup"><span data-stu-id="bf423-123">Be sure to cancel any outstanding timers before freeing the memory containing the callback function.</span></span>

> [!Note]  
> <span data-ttu-id="bf423-124">Der Multimedia-Timer wird in einem eigenen Thread ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf423-124">The multimedia timer runs in its own thread.</span></span>

 

 

 