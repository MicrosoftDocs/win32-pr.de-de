---
title: Informationen zu multimeditimern
description: Informationen zu multimeditimern
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Windows-Multimedia, Timer
- Multimedia, Timer
- Multimedia-Eingabe, Timer
- Multimedia-Timer, Informationen zu
- Timer, Info
- Multimedia-Timer, Planungs Ereignisse
- Timer, Zeit Planungs Ereignisse
- Planen von Zeit Geber Ereignissen
- Zeitüberschreitung bei hoher Auflösung
- Funktion "Funktion"
- Funktion "kreatewaitabletimer"
- WM_TIMER Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c36e5f19a92b6b47a3b1976bd85aadef88ab3ec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038927"
---
# <a name="about-multimedia-timers"></a><span data-ttu-id="548d8-115">Informationen zu multimeditimern</span><span class="sxs-lookup"><span data-stu-id="548d8-115">About Multimedia Timers</span></span>

<span data-ttu-id="548d8-116">Multimedietdienste ermöglichen es Anwendungen, Zeit Geber Ereignisse mit der größtmöglichen Auflösung (oder Genauigkeit) für die Hardwareplattform zu planen.</span><span class="sxs-lookup"><span data-stu-id="548d8-116">Multimedia timer services allow applications to schedule timer events with the greatest resolution (or accuracy) possible for the hardware platform.</span></span> <span data-ttu-id="548d8-117">Diese Multimedia-Timer-Dienste ermöglichen es Ihnen, Zeit Geber Ereignisse in einer höheren Auflösung als andere Zeit Geber Dienste zu planen.</span><span class="sxs-lookup"><span data-stu-id="548d8-117">These multimedia timer services allow you to schedule timer events at a higher resolution than other timer services.</span></span>

<span data-ttu-id="548d8-118">Diese Timer-Dienste sind für Anwendungen nützlich, die eine Zeitüberschreitung mit hoher Auflösung erfordern.</span><span class="sxs-lookup"><span data-stu-id="548d8-118">These timer services are useful for applications that demand high-resolution timing.</span></span> <span data-ttu-id="548d8-119">Beispielsweise erfordert ein "MIDI Sequencer" einen Zeit Geber mit hoher Auflösung, da er die Geschwindigkeit von "MIDI"-Ereignissen innerhalb einer Auflösung von 1 Millisekunden aufrechterhalten muss.</span><span class="sxs-lookup"><span data-stu-id="548d8-119">For example, a MIDI sequencer requires a high-resolution timer because it must maintain the pace of MIDI events within a resolution of 1 millisecond.</span></span>

<span data-ttu-id="548d8-120">Anwendungen, die keine Zeitüberschreitung mit hoher Auflösung verwenden, sollten [die Funktion](/windows/win32/api/winuser/nf-winuser-settimer) "-Funktion" anstelle von Multimedia-Timer-Diensten verwenden.</span><span class="sxs-lookup"><span data-stu-id="548d8-120">Applications that do not use high-resolution timing should use the [SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) function instead of multimedia timer services.</span></span> <span data-ttu-id="548d8-121">Die **von "** " bereitgestellten Timer-Dienste stellen Zeit Geber Nachrichten in einer Nachrichten Warteschlange bereit, während die Multimediatimer-Dienste eine Rückruffunktion aufzurufen. [ \_](../winmsg/wm-timer.md)</span><span class="sxs-lookup"><span data-stu-id="548d8-121">The timer services provided by **SetTimer** post [WM\_TIMER](../winmsg/wm-timer.md) messages to a message queue, while the multimedia timer services call a callback function.</span></span> <span data-ttu-id="548d8-122">Anwendungen, die einen aktivierbaren Timer benötigen, sollten die Funktion " [kreatewaitabletimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="548d8-122">Applications that want a waitable timer should use the [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) function.</span></span>

 

 