---
title: Zeit Geber Auflösung
description: Zeit Geber Auflösung
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
keywords:
- Multimedia-Timer, Lösung
- Timer, Auflösung
- minimale Zeit Geber Auflösung
- maximale Zeit Geber Auflösung
- Multimedia-Timer, maximale Auflösung
- Timer, maximale Auflösung
- Multimedia-Timer, minimale Auflösung
- Timer, minimale Auflösung
- timegetdevcaps-Funktion
- TimeBeginPeriod-Funktion
- timeendperiod-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e96f1b410f2e18203af794ea124bb6b83bccce
ms.sourcegitcommit: a0b531d335bc691100149830b256d5af7e136c24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/28/2019
ms.locfileid: "103706990"
---
# <a name="timer-resolution"></a><span data-ttu-id="64fdc-114">Zeit Geber Auflösung</span><span class="sxs-lookup"><span data-stu-id="64fdc-114">Timer Resolution</span></span>

<span data-ttu-id="64fdc-115">Um die minimalen und maximalen Zeit Geber Auflösungen zu ermitteln, die von den Timer-Diensten unterstützt werden, verwenden Sie die Funktion [**timegetdevcaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="64fdc-115">To determine the minimum and maximum timer resolutions supported by the timer services, use the [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) function.</span></span> <span data-ttu-id="64fdc-116">Diese Funktion füllt die **Member wperiodmin** und **wperiodmax** der [**timecaps**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) -Struktur mit der minimalen und maximalen Auflösung aus.</span><span class="sxs-lookup"><span data-stu-id="64fdc-116">This function fills the **wPeriodMin** and **wPeriodMax** members of the [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) structure with the minimum and maximum resolutions.</span></span> <span data-ttu-id="64fdc-117">Dieser Bereich kann sich zwischen Computern und Windows-Plattformen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="64fdc-117">This range can vary across computers and Windows platforms.</span></span>

<span data-ttu-id="64fdc-118">Nachdem Sie die minimale und die maximale Anzahl verfügbarer Zeit Geber Auflösungen festgelegt haben, müssen Sie die minimale Auflösung einrichten, die von der Anwendung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="64fdc-118">After you determine the minimum and maximum available timer resolutions, you must establish the minimum resolution you want your application to use.</span></span> <span data-ttu-id="64fdc-119">Verwenden Sie die [**TimeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) -und [**timeendperiod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) -Funktionen, um diese Auflösung festzulegen und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="64fdc-119">Use the [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) functions to set and clear this resolution.</span></span> <span data-ttu-id="64fdc-120">Sie müssen jeden Aufruf von **TimeBeginPeriod** mit einem Aufruf von **timeendperiod** vergleichen und dabei dieselbe minimale Auflösung in beiden Aufrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="64fdc-120">You must match each call to **timeBeginPeriod** with a call to **timeEndPeriod**, specifying the same minimum resolution in both calls.</span></span> <span data-ttu-id="64fdc-121">Eine Anwendung kann mehrere **TimeBeginPeriod** -Aufrufe durchführen, solange jeder Aufruf mit einem Aufruf von **timeendperiod** übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="64fdc-121">An application can make multiple **timeBeginPeriod** calls, as long as each call is matched with a call to **timeEndPeriod**.</span></span>

<span data-ttu-id="64fdc-122">In [**TimeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) und [**timeendperiod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod)gibt der *uperiod* -Parameter die minimale Zeit Geber Auflösung in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="64fdc-122">In both [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod), the *uPeriod* parameter indicates the minimum timer resolution, in milliseconds.</span></span> <span data-ttu-id="64fdc-123">Sie können einen beliebigen Zeit Geber Auflösungswert innerhalb des Bereichs angeben, der vom Timer unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="64fdc-123">You can specify any timer resolution value within the range supported by the timer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64fdc-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64fdc-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64fdc-125">Informationen zu multimeditimern</span><span class="sxs-lookup"><span data-stu-id="64fdc-125">About Multimedia Timers</span></span>](about-multimedia-timers.md)
</dt> </dl>

 

 




