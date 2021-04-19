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
# <a name="interrupt-time"></a>Interruptzeit

Die *Interruptzeit* ist die Zeitspanne seit dem letzten Start des Systems in 100-Nanosekunden-Intervallen. Der Wert für die Interruptzeit beginnt bei 0 (null), wenn das System gestartet wird, und wird bei jeder Uhr Unterbrechung um die Länge eines Takt zeitakts erhöht. Die genaue Länge eines Takt zeitachs hängt von der zugrunde liegenden Hardware ab und kann je nach System variieren.

Im Unterschied zur [Systemzeit](system-time.md)unterliegt die Anzahl der Interrupt-Zeiten nicht den Anpassungen durch Benutzer oder den Windows-Zeit Dienst, sodass Sie eine bessere Wahl für die Messung kurzer Dauer haben. Anwendungen, die eine höhere Genauigkeit benötigen als die Anzahl der Interruptzeit, sollten einen Zeit Geber mit [hoher Auflösung](../winmsg/about-timers.md)verwenden. Verwenden Sie die Funktion [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) , um die Häufigkeit des hochauflösenden Timers abzurufen, und die [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) -Funktion, um den Wert des Zählers abzurufen.

Die Funktionen [**queryinterrupttime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**queryinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)und [**queryunbiasedinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) können verwendet werden, um die Anzahl der Interrupt-Zeiten abzurufen. Eine unausgewogene Interruptzeit bedeutet, dass nur die Zeit gezählt wird, in der sich das System im Arbeitszustand befindet – daher ist die Anzahl der Interrupt-Zeit nicht "verzerrt", wenn das System im Standbymodus oder Ruhezustand verbringt.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP/2000:** Die [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) -Funktion ist ab Windows 7 und Windows Server 2008 R2 verfügbar.

Die von den Funktionen [**TimeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) und [**timeendperiod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) festgelegte Zeit Geber Auflösung wirkt sich auf die Auflösung der Funktionen [**queryinterrupttime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) und [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) aus. Das Erhöhen der Zeit Geber Auflösung wird jedoch nicht empfohlen, da dadurch die Gesamtsystemleistung reduziert und der Stromverbrauch erhöht werden kann, da der Prozessor nicht in den Energiesparmodus wechselt. Stattdessen sollten Anwendungen einen hochauflösenden Timer verwenden.

> [!Note]  
> Die Funktionen " [**queryinterrupttime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)", " [**queryinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)", " [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)" und " [**queryunbiasedinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) " erzeugen unterschiedliche Ergebnisse beim Debuggen ("aktivierte") Builds von Windows, da die Anzahl der Interruptzeit und die Takt Anzahl um ungefähr 49 Tage erweitert werden. Dies hilft, Fehler zu identifizieren, die möglicherweise erst auftreten, wenn das System über einen längeren Zeitraum ausgeführt wird. Der überprüfte Build steht MSDN-Abonnenten über die [MSDN-Website (Microsoft Developer Network)](https://msdn.microsoft.com/default.aspx) zur Verfügung.

 

Im folgenden Beispiel wird gezeigt, wie die Interruptzeit-Anzahl abgerufen wird, indem die Funktionen [**queryinterrupttime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**queryinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)und [**queryunbiasedinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) aufgerufen werden. Verknüpfung mit der onecore. lib-Bibliothek, wenn Sie eine Konsolenanwendung erstellen, die diese Funktionen aufruft.


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



Um die verstrichene Zeit für den Standbymodus oder den Ruhezustand abzurufen, verwenden Sie die Funktion [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) oder [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) , oder verwenden Sie den Leistungs Zähler System Betriebszeit. Dieser Leistungswert kann aus den Leistungsdaten in den **HKEY- \_ Leistungs \_ Daten** des Registrierungsschlüssels abgerufen werden. Der zurückgegebene Wert ist ein 8-Byte-Wert. Weitere Informationen finden Sie unter [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Queryinterrupttime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[**Queryinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[**Queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[**Queryunbiasedinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[**TimeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[**timeendperiod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
