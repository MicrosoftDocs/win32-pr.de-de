---
description: Interruptzeit ist die Zeitspanne seit dem letzten Start des Systems in Intervallen von 100 Nanosekunden.
ms.assetid: 56fe322e-53ea-4186-9b5e-352f69b09109
title: Interruptzeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0da8fa92fc51cdceef6f0052dda7a2cd27d7b21b24d11bd8ec7b1ea4aff18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885510"
---
# <a name="interrupt-time"></a>Interruptzeit

*Interruptzeit* ist die Zeitspanne seit dem letzten Start des Systems in Intervallen von 100 Nanosekunden. Die Anzahl der Interruptzeit beginnt bei 0 (null), wenn das System gestartet wird, und wird bei jedem Uhrunterbrechungsschritt um die Länge eines Takts erhöht. Die genaue Länge eines Takts hängt von der zugrunde liegenden Hardware ab und kann je nach System variieren.

Im [Gegensatz zur Systemzeit](system-time.md)unterliegt die Anzahl der Interruptzeiten keinen Anpassungen durch Benutzer oder den Windows-Zeitdienst. Dies ist eine bessere Wahl für die Messung kurzer Zeitdauern. Anwendungen, die eine höhere Genauigkeit als die Anzahl der Interruptzeit erfordern, sollten einen [timer mit hoher Auflösung verwenden.](../winmsg/about-timers.md) Verwenden Sie [**die QueryPerformanceFrequency-Funktion,**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) um die Häufigkeit des timer mit hoher Auflösung und die [**QueryPerformanceCounter-Funktion**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) abzurufen, um den Wert des Indikators abzurufen.

Die [**Funktionen QueryInterruptTime,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) [**QueryInterruptTimePrecise,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise) [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)und [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) können verwendet werden, um die Interruptzeitanzahl abzurufen. Unvoreingenommene Interruptzeit bedeutet, dass nur die Zeit gezählt wird, in der sich das System im Arbeitszustand befindet. Daher wird die Anzahl der Interruptzeit nicht durch die Zeit "verzerrt", die das System im Ruhezustand oder Ruhezustand verbringt.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP/2000:** Die [**QueryUnbiasedInterruptTime-Funktion**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) ist ab Windows 7 und Windows Server 2008 R2 verfügbar.

Die von den [**timeBeginPeriod-**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) und [**timeEndPeriod-Funktionen**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) festgelegte Timerauflösung wirkt sich auf die Auflösung der [**Funktionen QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) und [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) aus. Es wird jedoch nicht empfohlen, die Timerauflösung zu erhöhen, da dies die Gesamtleistung des Systems verringern und den Energieverbrauch erhöhen kann, indem verhindert wird, dass der Prozessor energiesparende Zustände einnimmt. Stattdessen sollten Anwendungen einen timer mit hoher Auflösung verwenden.

> [!Note]  
> Die [**Funktionen QueryInterruptTime,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) [**QueryInterruptTimePrecise,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise) [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)und [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) erzeugen unterschiedliche Ergebnisse bei Debugbuilds ("überprüft") von Windows, da die Anzahl der Interruptzeiten und Ticks um ca. 49 Tage erweitert wird. Dadurch können Fehler identifiziert werden, die möglicherweise erst auftreten, wenn das System lange ausgeführt wurde. Der überprüfte Build steht MSDN-Abonnenten über die MSDN-Website [(Microsoft-Entwickler Network)](https://msdn.microsoft.com/default.aspx) zur Verfügung.

 

Das folgende Beispiel zeigt, wie die Interruptzeitanzahl durch Aufrufen der Funktionen [**QueryInterruptTime,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) [**QueryInterruptTimePrecise,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise) [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)und [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) abgerufen wird. Link zur Bibliothek OneCore.lib, wenn Sie eine Konsolenanwendung erstellen, die diese Funktionen aufruft.


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



Verwenden Sie die [**GetTickCount-**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) oder [**GetTickCount64-Funktion,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) oder verwenden Sie den System up Time-Leistungsindikator, um die verstrichene Zeit abzurufen, die für den Ruhezustand oder Ruhezustand verwendet wird. Dieser Leistungsindikator kann aus den Leistungsdaten im Registrierungsschlüssel **HKEY \_ PERFORMANCE DATA abgerufen \_ werden.** Der zurückgegebene Wert ist ein 8-Byte-Wert. Weitere Informationen finden Sie unter [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
