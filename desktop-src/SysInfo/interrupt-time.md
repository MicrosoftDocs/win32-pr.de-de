---
description: Die Interruptzeit ist die Zeitspanne seit dem letzten Start des Systems in 100-Nanosekunden-Intervallen.
ms.assetid: 56fe322e-53ea-4186-9b5e-352f69b09109
title: Interruptzeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6018d97ab0eecd1182c02b734357ca13fbe12632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348448"
---
# <a name="interrupt-time"></a><span data-ttu-id="71b56-103">Interruptzeit</span><span class="sxs-lookup"><span data-stu-id="71b56-103">Interrupt Time</span></span>

<span data-ttu-id="71b56-104">Die *Interruptzeit* ist die Zeitspanne seit dem letzten Start des Systems in 100-Nanosekunden-Intervallen.</span><span class="sxs-lookup"><span data-stu-id="71b56-104">*Interrupt time* is the amount of time since the system was last started, in 100-nanosecond intervals.</span></span> <span data-ttu-id="71b56-105">Der Wert für die Interruptzeit beginnt bei 0 (null), wenn das System gestartet wird, und wird bei jeder Uhr Unterbrechung um die Länge eines Takt zeitakts erhöht.</span><span class="sxs-lookup"><span data-stu-id="71b56-105">The interrupt-time count begins at zero when the system starts and is incremented at each clock interrupt by the length of a clock tick.</span></span> <span data-ttu-id="71b56-106">Die genaue Länge eines Takt zeitachs hängt von der zugrunde liegenden Hardware ab und kann je nach System variieren.</span><span class="sxs-lookup"><span data-stu-id="71b56-106">The exact length of a clock tick depends on underlying hardware and can vary between systems.</span></span>

<span data-ttu-id="71b56-107">Im Unterschied zur [Systemzeit](system-time.md)unterliegt die Anzahl der Interrupt-Zeiten nicht den Anpassungen durch Benutzer oder den Windows-Zeit Dienst, sodass Sie eine bessere Wahl für die Messung kurzer Dauer haben.</span><span class="sxs-lookup"><span data-stu-id="71b56-107">Unlike [system time](system-time.md), the interrupt-time count is not subject to adjustments by users or the Windows time service, making it a better choice for measuring short durations.</span></span> <span data-ttu-id="71b56-108">Anwendungen, die eine höhere Genauigkeit benötigen als die Anzahl der Interruptzeit, sollten einen Zeit Geber mit [hoher Auflösung](../winmsg/about-timers.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="71b56-108">Applications that require greater precision than the interrupt-time count should use a [high-resolution timer](../winmsg/about-timers.md).</span></span> <span data-ttu-id="71b56-109">Verwenden Sie die Funktion [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) , um die Häufigkeit des hochauflösenden Timers abzurufen, und die [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) -Funktion, um den Wert des Zählers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="71b56-109">Use the [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) function to retrieve the frequency of the high-resolution timer and the [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) function to retrieve the counter's value.</span></span>

<span data-ttu-id="71b56-110">Die Funktionen [**queryinterrupttime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**queryinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)und [**queryunbiasedinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) können verwendet werden, um die Anzahl der Interrupt-Zeiten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="71b56-110">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions can be used to retrieve the interrupt-time count.</span></span> <span data-ttu-id="71b56-111">Eine unausgewogene Interruptzeit bedeutet, dass nur die Zeit gezählt wird, in der sich das System im Arbeitszustand befindet – daher ist die Anzahl der Interrupt-Zeit nicht "verzerrt", wenn das System im Standbymodus oder Ruhezustand verbringt.</span><span class="sxs-lookup"><span data-stu-id="71b56-111">Unbiased interrupt-time means that only time that the system is in the working state is counted—therefore, the interrupt-time count is not "biased" by time the system spends in sleep or hibernation.</span></span>

<span data-ttu-id="71b56-112">**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP/2000:** Die [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) -Funktion ist ab Windows 7 und Windows Server 2008 R2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="71b56-112">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:** The [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) function is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="71b56-113">Die von den Funktionen [**TimeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) und [**timeendperiod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) festgelegte Zeit Geber Auflösung wirkt sich auf die Auflösung der Funktionen [**queryinterrupttime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) und [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) aus.</span><span class="sxs-lookup"><span data-stu-id="71b56-113">The timer resolution set by the [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) functions affects the resolution of the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) and [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) functions.</span></span> <span data-ttu-id="71b56-114">Das Erhöhen der Zeit Geber Auflösung wird jedoch nicht empfohlen, da dadurch die Gesamtsystemleistung reduziert und der Stromverbrauch erhöht werden kann, da der Prozessor nicht in den Energiesparmodus wechselt.</span><span class="sxs-lookup"><span data-stu-id="71b56-114">However, increasing the timer resolution is not recommended because it can reduce overall system performance and increase power consumption by preventing the processor from entering power-saving states.</span></span> <span data-ttu-id="71b56-115">Stattdessen sollten Anwendungen einen hochauflösenden Timer verwenden.</span><span class="sxs-lookup"><span data-stu-id="71b56-115">Instead, applications should use a high-resolution timer.</span></span>

> [!Note]  
> <span data-ttu-id="71b56-116">Die Funktionen " [**queryinterrupttime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)", " [**queryinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)", " [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)" und " [**queryunbiasedinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) " erzeugen unterschiedliche Ergebnisse beim Debuggen ("aktivierte") Builds von Windows, da die Anzahl der Interruptzeit und die Takt Anzahl um ungefähr 49 Tage erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="71b56-116">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days.</span></span> <span data-ttu-id="71b56-117">Dies hilft, Fehler zu identifizieren, die möglicherweise erst auftreten, wenn das System über einen längeren Zeitraum ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71b56-117">This helps to identify bugs that might not occur until the system has been running for a long time.</span></span> <span data-ttu-id="71b56-118">Der überprüfte Build steht MSDN-Abonnenten über die [MSDN-Website (Microsoft Developer Network)](https://msdn.microsoft.com/default.aspx) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="71b56-118">The checked build is available to MSDN subscribers through the [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) Web site.</span></span>

 

<span data-ttu-id="71b56-119">Im folgenden Beispiel wird gezeigt, wie die Interruptzeit-Anzahl abgerufen wird, indem die Funktionen [**queryinterrupttime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**queryinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)und [**queryunbiasedinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="71b56-119">The following example shows how to retrieve the interrupt-time count by calling the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions.</span></span> <span data-ttu-id="71b56-120">Verknüpfung mit der onecore. lib-Bibliothek, wenn Sie eine Konsolenanwendung erstellen, die diese Funktionen aufruft.</span><span class="sxs-lookup"><span data-stu-id="71b56-120">Link to the OneCore.lib library when you build a console application that calls these functions.</span></span>


```C++
#include "stdafx.h"
#include <windows.h>
#include <realtimeapiset.h>

void InterruptTimeTest()
{
    ULONGLONG InterruptTime;
    ULONGLONG PreciseInterruptTime;
    ULONGLONG UnbiasedInterruptTime;
    ULONGLONG PreciseUnbiasedInterruptTime;

        // The interrupt time that QueryInterruptTime reports is based on the 
        // latest tick of the system clock timer. The system clock timer is 
        // the hardware timer that periodically generates interrupts for the 
        // system clock. The uniform period between system clock timer 
        // interrupts is referred to as a system clock tick, and is typically 
        // in the range of 0.5 milliseconds to 15.625 milliseconds, depending 
        // on the hardware platform. The interrupt time value retrieved by 
        // QueryInterruptTime is accurate within a system clock tick.

    QueryInterruptTime(&InterruptTime);
    printf("Interrupt time: %.7f seconds\n", 
            (double)InterruptTime/(double)10000000);

        // Precise interrupt time is more precise than the interrupt time that
        // QueryInterruptTime reports because the functions that report  
        // precise interrupt time read the timer hardware directly.

    QueryInterruptTimePrecise(&PreciseInterruptTime);
    printf("Precise interrupt time: %.7f seconds\n", 
            (double)PreciseInterruptTime/(double)10000000);

        // Unbiased interrupt time means that only time that the system is in 
        // the working state is counted. Therefore, the interrupt-time count 
        // is not biased by time the system spends in sleep or hibernation.

    QueryUnbiasedInterruptTime(&UnbiasedInterruptTime);
    printf("Unbiased interrupt time: %.7f seconds\n", 
            (double)UnbiasedInterruptTime/(double)10000000);

        // QueryUnbiasedInterruptTimePrecise gets an interrupt-time count
        // that is both unbiased and precise, as defined in the comments
        // included earlier in this example.

    QueryUnbiasedInterruptTimePrecise(&PreciseUnbiasedInterruptTime);
    printf("Precise unbiased interrupt time: %.7f seconds\n", 
            (double)PreciseUnbiasedInterruptTime/(double)10000000);

}

int main(void)
{
    void InterruptTimeTime();

    InterruptTimeTest();
    return(0);
}
```



<span data-ttu-id="71b56-121">Um die verstrichene Zeit für den Standbymodus oder den Ruhezustand abzurufen, verwenden Sie die Funktion [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) oder [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) , oder verwenden Sie den Leistungs Zähler System Betriebszeit.</span><span class="sxs-lookup"><span data-stu-id="71b56-121">To retrieve elapsed time that accounts for sleep or hibernation, use the [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) or [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) function, or use the System Up Time performance counter.</span></span> <span data-ttu-id="71b56-122">Dieser Leistungswert kann aus den Leistungsdaten in den **HKEY- \_ Leistungs \_ Daten** des Registrierungsschlüssels abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="71b56-122">This performance counter can be retrieved from the performance data in the registry key **HKEY\_PERFORMANCE\_DATA**.</span></span> <span data-ttu-id="71b56-123">Der zurückgegebene Wert ist ein 8-Byte-Wert.</span><span class="sxs-lookup"><span data-stu-id="71b56-123">The value returned is an 8-byte value.</span></span> <span data-ttu-id="71b56-124">Weitere Informationen finden Sie unter [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="71b56-124">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

## <a name="related-topics"></a><span data-ttu-id="71b56-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="71b56-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71b56-126">**Queryinterrupttime**</span><span class="sxs-lookup"><span data-stu-id="71b56-126">**QueryInterruptTime**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[<span data-ttu-id="71b56-127">**Queryinterrupttimepräzisen**</span><span class="sxs-lookup"><span data-stu-id="71b56-127">**QueryInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="71b56-128">**Queryunbiasedinterrupttime**</span><span class="sxs-lookup"><span data-stu-id="71b56-128">**QueryUnbiasedInterruptTime**</span></span>](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[<span data-ttu-id="71b56-129">**Queryunbiasedinterrupttimepräzisen**</span><span class="sxs-lookup"><span data-stu-id="71b56-129">**QueryUnbiasedInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="71b56-130">**TimeBeginPeriod**</span><span class="sxs-lookup"><span data-stu-id="71b56-130">**timeBeginPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[<span data-ttu-id="71b56-131">**timeendperiod**</span><span class="sxs-lookup"><span data-stu-id="71b56-131">**timeEndPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
