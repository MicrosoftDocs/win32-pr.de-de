---
description: Windows apis, die Sie verwenden können, um zeitstempel mit hoher Auflösung zu erhalten oder Zeitintervalle zu messen.
ms.assetid: D66E0FC2-3AF2-489B-B4B5-78648905B77B
title: Abrufen von Zeitstempeln mit hoher Auflösung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e25c50cb602dd7e5c53c967c12321ec02a6ea68613767f4019b2def7f5793b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764624"
---
# <a name="acquiring-high-resolution-time-stamps"></a>Abrufen von Zeitstempeln mit hoher Auflösung

Windows apis, die Sie verwenden können, um zeitstempel mit hoher Auflösung zu erhalten oder Zeitintervalle zu messen. Die primäre API für nativen Code ist [**QueryPerformanceCounter (QPC).**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Für Gerätetreiber ist die Kernelmodus-API [**KeQueryPerformanceCounter.**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) Für verwalteten Code verwendet die [**System.Diagnostics.Stopwatch-Klasse**](/previous-versions/windows/) **QPC** als genaue Zeitbasis.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) ist unabhängig von und wird nicht mit externen Zeitverweisen synchronisiert. Verwenden Sie [**GetSystemTimePreciseAsFileTime,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime)um Zeitstempel abzurufen, die mit einem externen Zeitverweis synchronisiert werden können, z. B. koordinierte Weltzeit (UTC) für die Verwendung in messungen mit hoher Auflösung zur Tageszeit.

Zeitstempel und Zeitintervallmessungen sind ein wesentlicher Bestandteil von Computer- und Netzwerkleistungsmessungen. Zu diesen Leistungsmessungsvorgängen gehören die Berechnung der Antwortzeit, des Durchsatzes und der Latenz sowie die Codeausführung für die Profilerstellung. Jeder dieser Vorgänge umfasst eine Messung der Aktivitäten, die während eines Zeitintervalls auftreten, das durch ein Start- und ein Endereignis definiert wird, das unabhängig von externen Zeitverweisen sein kann.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) ist in der Regel die beste Methode, um Zeitstempelereignisse zu stempeln und kleine Zeitintervalle zu messen, die auf demselben System oder virtuellen Computer auftreten. Erwägen Sie die Verwendung [**von GetSystemTimePreciseAsFileTime,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) wenn Sie Ereignisse auf mehreren Computern zeitstempeln möchten, vorausgesetzt, dass jeder Computer an einem Zeitsynchronisierungsschema wie Network Time Protocol (NTP) beteiligt ist. **Mit QPC** können Sie Schwierigkeiten vermeiden, die bei anderen Zeitmessungsansätzen auftreten können, z. B. das direkte Lesen des Zeitstempelzählers (Time Stamp Counter, TSC) des Prozessors.

-   [QPC-Unterstützung in Windows Versionen](#qpc-support-in-windows-versions)
-   [Leitfaden zum Abrufen von Zeitstempeln](#guidance-for-acquiring-time-stamps)
    -   [Virtualisierung](#virtualization)
    -   [Direkte TSC-Nutzung](#direct-tsc-usage)
    -   [Beispiele für das Abrufen von Zeitstempeln](#examples-for-acquiring-time-stamps)
-   [Allgemeine häufig gestellte Fragen zu QPC und TSC](#general-faq-about-qpc-and-tsc)
-   [Häufig gestellte Fragen zur Programmierung mit QPC und TSC](#faq-about-programming-with-qpc-and-tsc)
-   [Merkmale der Hardwareuhr auf niedriger Ebene](#low-level-hardware-clock-characteristics)
    -   [Absolute Uhren und Differenzuhren](#absolute-clocks-and-difference-clocks)
    -   [Auflösung, Genauigkeit, Genauigkeit und Stabilität](#resolution-precision-accuracy-and-stability)
-   [Hardware-Timerinformationen](#hardware-timer-info)

## <a name="qpc-support-in-windows-versions"></a>QPC-Unterstützung in Windows Versionen

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) wurde in Windows 2000 und Windows XP eingeführt und hat sich weiterentwickelt, um die Verbesserungen der Hardwareplattform und der Prozessoren zu nutzen. Hier werden die Merkmale von **QPC** in verschiedenen Windows beschrieben, um Sie bei der Wartung von Software zu unterstützen, die auf diesen Windows wird.

### <a name="windows-xp-and-windows-2000"></a>Windows XP und Windows 2000

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) ist auf Windows XP und Windows 2000 verfügbar und funktioniert auf den meisten Systemen gut. Das BIOS einiger Hardwaresysteme gibt jedoch die CPU-Merkmale der Hardware (ein nicht invariantes TSC) nicht richtig an, und einige Systeme mit mehreren Kernen oder mehreren Prozessoren verwendeten Prozessoren mit TSCs, die nicht kernübergreifend synchronisiert werden konnten. Systeme mit fehlerhafter Firmware, auf denen diese Versionen von Windows ausgeführt werden, bieten möglicherweise nicht denselben **QPC-Leseschutz** auf verschiedenen Kernen, wenn sie TSC als Grundlage für **QPC verwenden.**

### <a name="windows-vista-and-windows-server-2008"></a>Windows Vista und Windows Server 2008

Alle Computer, die mit Windows Vista und Windows Server 2008 ausgeliefert wurden, verwendeten einen Plattformzähler (High Precision Event Timer (HPET)) oder den ACPI Power Management Timer (PM-Timer) als Grundlage für [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Solche Plattformzeiter haben eine höhere Zugriffslatenz als der TSC und werden von mehreren Prozessoren gemeinsam genutzt. Dies schränkt die Skalierbarkeit **von QPC** ein, wenn es von mehreren Prozessoren gleichzeitig aufgerufen wird.

### <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 und Windows Server 2008 R2

Die meisten Windows 7- und Windows Server 2008 R2-Computer verfügen über Prozessoren mit konstanten TSCs und verwenden diese Leistungsindikatoren als Grundlage für [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). TSCs sind hardwareleistungsbasierte Leistungsindikatoren mit hoher Auflösung pro Prozessor, auf die mit sehr geringer Latenz und geringem Mehraufwand zugegriffen werden kann (je nach Prozessortyp in der Reihenfolge von 10 oder 100Ern von Computerzyklen). Windows 7 und Windows Server 2008 R2 verwenden TSCs als Grundlage für **QPC** auf Domänensystemen mit nur einer Uhr, bei denen das Betriebssystem (oder der Hypervisor) die einzelnen TSCs während der Systemin initialisierung über alle Prozessoren hinweg eng synchronisieren kann. In solchen Systemen sind die Kosten für das Lesen des Leistungsindikators im Vergleich zu Systemen, die einen Plattformzähler verwenden, erheblich niedriger. Darüber hinaus gibt es keinen zusätzlichen Mehraufwand für gleichzeitige Aufrufe, und Benutzermodusabfragen umgehen häufig Systemaufrufe, wodurch der Mehraufwand weiter reduziert wird. Auf Systemen, in denen der TSC nicht für die Zeitmessung geeignet ist, wählt Windows automatisch einen Plattformzähler (entweder den HPET-Timer oder den ACPI PM-Timer) als Grundlage für **QPC aus.**

### <a name="windows-8-windows-81-windows-server-2012-and-windows-server-2012-r2"></a>Windows 8, Windows 8.1, Windows Server 2012 und Windows Server 2012 R2

Windows 8, Windows 8.1, Windows Server 2012 und Windows Server 2012 R2 verwenden TSCs als Grundlage für den Leistungsindikator. Der TSC-Synchronisierungsalgorithmus wurde erheblich verbessert, um große Systeme mit vielen Prozessoren besser aufnehmen zu können. Darüber hinaus wurde Unterstützung für die neue API für die genaue Tageszeit hinzugefügt, die das Abrufen präziser Zeitstempel für die Wanduhr vom Betriebssystem ermöglicht. Weitere Informationen finden Sie unter [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). Auf Windows RT PC-Plattformen basiert der Leistungsindikator entweder auf einem proprietären Plattformzähler oder auf dem Systemzähler, der vom generischen Windows RT-PC-Timer bereitgestellt wird, wenn die Plattform so ausgestattet ist.

## <a name="guidance-for-acquiring-time-stamps"></a>Leitfaden zum Abrufen von Zeitstempeln

Windows verfügt über und wird weiterhin in die Bereitstellung eines zuverlässigen und effizienten Leistungsindikators investieren. Wenn Sie Zeitstempel mit einer Auflösung von 1 Mikrosekunde oder besser benötigen und die Zeitstempel nicht mit einem externen Zeitverweis synchronisiert werden müssen, wählen Sie [**QueryPerformanceCounter,**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter)oder [**KeQueryInterruptTimePrecise aus.**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) Wenn Sie UTC-synchronisierte Zeitstempel mit einer Auflösung von 1 Mikrosekunde oder besser benötigen, wählen Sie [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) oder [**KeQuerySystemTimePrecise aus.**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequerysystemtimeprecise)

Auf einer relativ kleinen Anzahl von Plattformen, die das TSC-Register nicht als [**QPC-Basis**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) verwenden können, z. B. aus Gründen, die unter [Hardware-Timerinformationen](#hardware-timer-info)erläutert werden, kann das Abrufen von Zeitstempeln mit hoher Auflösung erheblich teurer sein als das Abrufen von Zeitstempeln mit geringerer Auflösung. Wenn eine Auflösung von 10 bis 16 Millisekunden ausreicht, können Sie [**GetTickCount64,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) [**QueryInterruptTime,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) [**QueryUnbiasedInterruptTime,**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) [**KeQueryInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttime)oder [**KeQueryUnbiasedInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryunbiasedinterrupttime) verwenden, um Zeitstempel zu erhalten, die nicht mit einem externen Zeitverweis synchronisiert werden. Verwenden Sie für UTC-synchronisierte Zeitstempel [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) oder [**KeQuerySystemTime.**](/windows-hardware/drivers/ddi/wdm/nf-wdm-kequerysystemtime~r1) Wenn eine höhere Auflösung erforderlich ist, können Sie stattdessen [**QueryInterruptTimePrecise,**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise) [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)oder [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) verwenden, um Zeitstempel zu erhalten.

Im Allgemeinen sind die Leistungsindikatorergebnisse für alle Prozessoren in Systemen mit mehreren Kernen und mehreren Prozessoren konsistent, auch wenn sie in verschiedenen Threads oder Prozessen gemessen werden. Hier sind einige Ausnahmen von dieser Regel:

-   Vor der Windows Vista-Betriebssysteme, die auf bestimmten Prozessoren ausgeführt werden, kann diese Konsistenz aus einem der folgenden Gründe verletzen:

    -   Die Hardwareprozessoren verfügen über ein nicht invariantes TSC, und das BIOS gibt diese Bedingung nicht ordnungsgemäß an.
    -   Der verwendete TSC-Synchronisierungsalgorithmus eignete sich nicht für Systeme mit einer großen Anzahl von Prozessoren.

-   Wenn Sie Leistungsindikatorergebnisse vergleichen, die von verschiedenen Threads erfasst werden, sollten Sie Werte berücksichtigen, die sich um einen ± 1 Tick unterscheiden, um eine mehrdeutige Reihenfolge zu erhalten. Wenn die Zeitstempel aus demselben Thread genommen werden, gilt ± 1 Tick-Unsicherheit nicht. In diesem Kontext bezieht sich der Begriff Tick auf einen Zeitraum, der gleich 1 ÷ ist (die Häufigkeit des Leistungsindikators, der von [**QueryPerformanceFrequency ermittelt wird).**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)

Wenn Sie den Leistungsindikator auf großen Serversystemen mit Domänen mit mehreren Takten verwenden, die nicht in der Hardware synchronisiert sind, ermittelt Windows, dass der TSC nicht zu Zeitsteuerungszwecken verwendet werden kann, und wählt einen Plattformzähler als Grundlage für [**QPC aus.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Obwohl dieses Szenario weiterhin zuverlässige Zeitstempel liefert, werden die Zugriffslatenz und Skalierbarkeit beeinträchtigt. Verwenden Sie daher, wie bereits in der vorherigen Verwendungsanleitung erwähnt, nur die APIs, die eine Auflösung von 1 Mikrosekunden oder eine bessere Auflösung bereitstellen, wenn eine solche Auflösung erforderlich ist. Das TSC wird als Grundlage für **QPC** auf Domänensystemen mit mehreren Uhren verwendet, die die Hardwaresynchronisierung aller Prozessoruhrdomänen umfassen, da sie dadurch effektiv als einzelnes Uhrdomänensystem funktionieren.

Die Häufigkeit des Leistungsindikators wird beim Systemstart festgelegt und ist für alle Prozessoren konsistent, sodass Sie nur die Häufigkeit von [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) abfragen müssen, während die Anwendung initialisiert wird, und dann das Ergebnis zwischenspeichern müssen.

### <a name="virtualization"></a>Virtualisierung

Es wird erwartet, dass der Leistungsindikator zuverlässig auf allen virtuellen Gastcomputern funktioniert, die auf ordnungsgemäß implementierten Hypervisoren ausgeführt werden. Hypervisoren, die der Schnittstelle der Hypervisorversion 1.0 entsprechen und die Referenzzeitreferenz zur Oberfläche machen, können jedoch einen erheblich geringeren Mehraufwand bieten. Weitere Informationen zu Hypervisorschnittstellen und -benutzeroberflächen finden Sie unter [Hypervisorspezifikationen](/virtualization/hyper-v-on-windows/reference/tlfs).

### <a name="direct-tsc-usage"></a>Direkte TSC-Nutzung

Es wird dringend davon abgeraten, die **RDTSC-** oder **RDTSCP-Prozessoranweisung** zum direkten Abfragen des TSC zu verwenden, da Sie bei einigen Versionen von Windows, bei Livemigrationen virtueller Computer und auf Hardwaresystemen ohne invariante oder eng synchronisierte TSCs keine zuverlässigen Ergebnisse erhalten. Stattdessen empfehlen wir Ihnen, [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) zu verwenden, um die Abstraktion, Konsistenz und Portabilität zu nutzen, die es bietet.

### <a name="examples-for-acquiring-time-stamps"></a>Beispiele für das Abrufen von Zeitstempeln

Die verschiedenen Codebeispiele in diesen Abschnitten zeigen, wie Zeitstempel erhalten werden.

### <a name="using-qpc-in-native-code"></a>Verwenden von QPC in nativem Code

In diesem Beispiel wird gezeigt, wie [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) in nativem C- und C++-Code verwendet wird.


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

QueryPerformanceFrequency(&Frequency); 
QueryPerformanceCounter(&StartingTime);

// Activity to be timed

QueryPerformanceCounter(&EndingTime);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;


//
// We now have the elapsed number of ticks, along with the
// number of ticks-per-second. We use these values
// to convert to the number of elapsed microseconds.
// To guard against loss-of-precision, we convert
// to microseconds *before* dividing by ticks-per-second.
//

ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



### <a name="acquiring-high-resolution-time-stamps-from-managed-code"></a>Abrufen von Zeitstempeln mit hoher Auflösung aus verwaltetem Code

In diesem Beispiel wird die Verwendung der [**System.Diagnostics.Stopwatch-Klasse für verwalteten Code**](/previous-versions/windows/) veranschaulicht.


```CSharp
using System.Diagnostics;

long StartingTime = Stopwatch.GetTimestamp();

// Activity to be timed

long EndingTime  = Stopwatch.GetTimestamp();
long ElapsedTime = EndingTime - StartingTime;

double ElapsedSeconds = ElapsedTime * (1.0 / Stopwatch.Frequency);
```



Die [**System.Diagnostics.Stopwatch-Klasse**](/previous-versions/windows/) bietet auch mehrere praktische Methoden zum Durchführen von Zeitintervallmessungen.

### <a name="using-qpc-from-kernel-mode"></a>Verwenden von QPC aus dem Kernelmodus

Der Windows-Kernel ermöglicht den Zugriff auf den Leistungsindikator im Kernelmodus über [**KeQueryPerformanceCounter,**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) von dem sowohl der Leistungsindikator als auch die Leistungshäufigkeit ermittelt werden können. **KeQueryPerformanceCounter** ist nur im Kernelmodus verfügbar und wird für Writer von Gerätetreibern und anderen Kernelmoduskomponenten bereitgestellt.

In diesem Beispiel wird die Verwendung von [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) im C- und C++-Kernelmodus veranschaulicht.


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

StartingTime = KeQueryPerformanceCounter(&Frequency);

// Activity to be timed

EndingTime = KeQueryPerformanceCounter(NULL);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;
ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



## <a name="general-faq-about-qpc-and-tsc"></a>Allgemeine häufig gestellte Fragen zu QPC und TSC

Hier finden Sie Antworten auf häufig gestellte Fragen zu [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) und TSCs im Allgemeinen.

<dl> <dt>

<span id="Is_QueryPerformanceCounter___the_same_as_the_Win32_GetTickCount___or_________GetTickCount64___function_"></span><span id="is_queryperformancecounter___the_same_as_the_win32_gettickcount___or_________gettickcount64___function_"></span><span id="IS_QUERYPERFORMANCECOUNTER___THE_SAME_AS_THE_WIN32_GETTICKCOUNT___OR_________GETTICKCOUNT64___FUNCTION_"></span>**Ist QueryPerformanceCounter() mit der Win32-Funktion GetTickCount() oder GetTickCount64() identisch?**
</dt> <dd>

Nein. [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) und [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) stehen nicht im Zusammenhang mit [**QPC.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) **GetTickCount** und **GetTickCount64 geben** die Anzahl von Millisekunden seit dem Start des Systems zurück.

</dd> <dt>

<span id="Should_I_use_QPC_or_call_the_RDTSC__RDTSCP_instructions_directly_"></span><span id="should_i_use_qpc_or_call_the_rdtsc__rdtscp_instructions_directly_"></span><span id="SHOULD_I_USE_QPC_OR_CALL_THE_RDTSC__RDTSCP_INSTRUCTIONS_DIRECTLY_"></span>**Sollte ich QPC verwenden oder die RDTSC/RDTSCP-Anweisungen direkt aufrufen?**
</dt> <dd>

Um Richtigkeits- und Portabilitätsprobleme zu vermeiden, wird dringend empfohlen, [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) anstelle des TSC-Registers oder der **RDTSC-** oder **RDTSCP-Prozessoranweisungen** zu verwenden.

</dd> <dt>

<span id="What_is_QPC_s_relation_to_an_external_time_epoch__Can_it_be_synchronized_to_an_________external_epoch_such_as_UTC_"></span><span id="what_is_qpc_s_relation_to_an_external_time_epoch__can_it_be_synchronized_to_an_________external_epoch_such_as_utc_"></span><span id="WHAT_IS_QPC_S_RELATION_TO_AN_EXTERNAL_TIME_EPOCH__CAN_IT_BE_SYNCHRONIZED_TO_AN_________EXTERNAL_EPOCH_SUCH_AS_UTC_"></span>**Was ist die Beziehung von QPC zu einer externen Zeitepoche? Kann sie mit einer externen Epoche wie UTC synchronisiert werden?**
</dt> <dd>

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) basiert auf einem Hardwarezähler, der nicht mit einem externen Zeitverweis wie UTC synchronisiert werden kann. Verwenden Sie [**GetSystemTimePreciseAsFileTime,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime)um genaue Zeitstempel für die Tageszeit zu erhalten, die mit einem externen UTC-Verweis synchronisiert werden können.

</dd> <dt>

<span id="Is_QPC_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="is_qpc_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="IS_QPC_AFFECTED_BY_DAYLIGHT_SAVINGS_TIME__LEAP_SECONDS__TIME_ZONES__OR_SYSTEM_________TIME_CHANGES_MADE_BY_THE_ADMINISTRATOR_"></span>**Ist QPC von Sommerzeit, Schaltsekunden, Zeitzonen oder Systemzeitänderungen betroffen, die vom Administrator vorgenommen wurden?**
</dt> <dd>

Nein. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) ist vollständig unabhängig von systemzeit und UTC.

</dd> <dt>

<span id="Is_QPC_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_Turbo_Boost_technology_"></span><span id="is_qpc_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_turbo_boost_technology_"></span><span id="IS_QPC_ACCURACY_AFFECTED_BY_PROCESSOR_FREQUENCY_CHANGES_CAUSED_BY_POWER_________MANAGEMENT_OR_TURBO_BOOST_TECHNOLOGY_"></span>**Wird die QPC-Genauigkeit durch Änderungen der Prozessorhäufigkeit beeinflusst, die durch die Energieverwaltung oder Turbo Boost-Technologie verursacht werden?**
</dt> <dd>

Nein. Wenn der Prozessor über einen invarianten TSC verfügt, wirkt sich diese Art von Änderungen nicht auf den [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) aus. Wenn der Prozessor nicht über einen invarianten TSC verfügt, wird **QPC** auf einen Plattformhardwaretimer zurückgesetzt, der von Änderungen der Prozessorhäufigkeit oder turbo Boost-Technologie nicht betroffen ist.

</dd> <dt>

<span id="Does_QPC_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="does_qpc_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="DOES_QPC_RELIABLY_WORK_ON_MULTI-PROCESSOR_SYSTEMS__MULTI-CORE_SYSTEM__AND_________SYSTEMS_WITH_HYPER-THREADING_"></span>**Funktioniert QPC zuverlässig auf Systemen mit mehreren Prozessoren, auf Systemen mit mehreren Kernen und auf Systemen mit Hyperthreading?**
</dt> <dd>

Ja

</dd> <dt>

<span id="How_do_I_determine_and_validate_that_QPC_works_on_my_machine_"></span><span id="how_do_i_determine_and_validate_that_qpc_works_on_my_machine_"></span><span id="HOW_DO_I_DETERMINE_AND_VALIDATE_THAT_QPC_WORKS_ON_MY_MACHINE_"></span>**Gewusst wie ermitteln und überprüfen, ob QPC auf meinem Computer funktioniert?**
</dt> <dd>

Sie müssen solche Überprüfungen nicht durchführen.

</dd> <dt>

<span id="Which_processors_have_non-invariant_TSCs__How_can_I_check_if_my_system_has_a_________non-invariant_TSC_"></span><span id="which_processors_have_non-invariant_tscs__how_can_i_check_if_my_system_has_a_________non-invariant_tsc_"></span><span id="WHICH_PROCESSORS_HAVE_NON-INVARIANT_TSCS__HOW_CAN_I_CHECK_IF_MY_SYSTEM_HAS_A_________NON-INVARIANT_TSC_"></span>**Welche Prozessoren verfügen über nicht invariante TSCs? Wie kann ich überprüfen, ob mein System über ein nicht invariantes TSC verfügt?**
</dt> <dd>

Sie müssen diese Überprüfung nicht selbst durchführen. Windows Betriebssysteme führen bei der Systeminitialisierung mehrere Überprüfungen durch, um zu ermitteln, ob TSC als Grundlage für [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)geeignet ist. Zu Referenzzwecken können Sie jedoch ermitteln, ob Ihr Prozessor über eine invariante TSC verfügt, indem Sie eine der folgenden Verfahren verwenden:

-   das hilfsprogramm Coreinfo.exe aus Windows Sysinternals
-   Überprüfen der von der CPUID-Anweisung zurückgegebenen Werte für die TSC-Merkmale
-   Dokumentation des Prozessorherstellers

Im Folgenden werden die TSC-INVARIANT-Informationen angezeigt, die vom hilfsprogramm sysinternals Coreinfo.exe Windows ([www.sysinternals.com](https://www.sysinternals.com)) bereitgestellt werden. Ein Sternchen bedeutet "True".

``` syntax
> Coreinfo.exe 

Coreinfo v3.2 - Dump information on system CPU and memory topology
Copyright (C) 2008-2012 Mark Russinovich
Sysinternals - www.sysinternals.com

 <unrelated text removed>

RDTSCP          * Supports RDTSCP instruction
TSC             * Supports RDTSC instruction
TSC-DEADLINE    - Local APIC supports one-shot deadline timer
TSC-INVARIANT   * TSC runs at constant rate
```

</dd> <dt>

<span id="Does_QPC_work_reliably_on__hardware_platforms_"></span><span id="does_qpc_work_reliably_on__hardware_platforms_"></span><span id="DOES_QPC_WORK_RELIABLY_ON__HARDWARE_PLATFORMS_"></span>**Funktioniert QPC zuverlässig auf Windows RT PC-Hardwareplattformen?**
</dt> <dd>

Ja

</dd> <dt>

<span id="How_often_does_QPC_roll_over_"></span><span id="how_often_does_qpc_roll_over_"></span><span id="HOW_OFTEN_DOES_QPC_ROLL_OVER_"></span>**Wie oft führt QPC ein Rollup aus?**
</dt> <dd>

Nicht weniger als 100 Jahre nach dem letzten Systemstart und möglicherweise länger basierend auf dem zugrunde liegenden verwendeten Hardwaretimer. Bei den meisten Anwendungen ist ein Rollover kein Problem.

</dd> <dt>

<span id="What_is_the_computational_cost_of_calling_QPC_"></span><span id="what_is_the_computational_cost_of_calling_qpc_"></span><span id="WHAT_IS_THE_COMPUTATIONAL_COST_OF_CALLING_QPC_"></span>**Wie sind die Berechnungskosten für den Aufruf von QPC?**
</dt> <dd>

Die Computeaufrufkosten von [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) werden in erster Linie von der zugrunde liegenden Hardwareplattform bestimmt. Wenn das TSC-Register als Grundlage für QPC verwendet wird, werden die Berechnungskosten in erster Linie davon bestimmt, wie lange der Prozessor zum Verarbeiten einer **RDTSC-Anweisung** benötigt. Diese Zeit reicht von 10 cpu-Zyklen bis hin zu mehreren hundert CPU-Zyklen, abhängig vom verwendeten Prozessor. Wenn der TSC nicht verwendet werden kann, wählt das System eine andere Hardwarezeitbasis aus. Da sich diese Zeitbasen auf der Hauptplatine befinden (z. B. auf der PCI South Bridge oder PCH), sind die Rechenkosten pro Aufruf höher als der TSC und liegen häufig in der Nähe von 0,8 bis 1,0 Mikrosekunden, je nach Prozessorgeschwindigkeit und anderen Hardwarefaktoren. Diese Kosten hängen von der Zeit ab, die für den Zugriff auf das Hardwaregerät auf der Hauptplatine erforderlich ist.

</dd> <dt>

<span id="Does_QPC_require_a_kernel_transition__system_call__"></span><span id="does_qpc_require_a_kernel_transition__system_call__"></span><span id="DOES_QPC_REQUIRE_A_KERNEL_TRANSITION__SYSTEM_CALL__"></span>**Erfordert QPC einen Kernelübergang (Systemaufruf)?**
</dt> <dd>

Ein Kernelübergang ist nicht erforderlich, wenn das System das TSC-Register als Grundlage für [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)verwenden kann. Wenn das System eine andere Zeitbasis verwenden muss, z. B. den HPET- oder PM-Timer, ist ein Systemaufruf erforderlich.

</dd> <dt>

<span id="Is_the_performance_counter_monotonic__non-decreasing__"></span><span id="is_the_performance_counter_monotonic__non-decreasing__"></span><span id="IS_THE_PERFORMANCE_COUNTER_MONOTONIC__NON-DECREASING__"></span>**Ist der Leistungsindikator monoton (nicht absteigend)?**
</dt> <dd>

Ja

</dd> <dt>

<span id="Can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="CAN_THE_PERFORMANCE_COUNTER_BE_USED_TO_ORDER_EVENTS_IN_TIME_"></span>**Kann der Leistungsindikator verwendet werden, um Ereignisse zeitlich zu ordnen?**
</dt> <dd>

Ja. Beim Vergleich von Leistungsindikatorergebnissen, die von verschiedenen Threads bezogen werden, weisen Werte, die sich durch ± 1 Tick unterscheiden, eine mehrdeutige Reihenfolge auf, als ob sie einen identischen Zeitstempel hätten.

</dd> <dt>

<span id="How_accurate_is_the_performance_counter_"></span><span id="how_accurate_is_the_performance_counter_"></span><span id="HOW_ACCURATE_IS_THE_PERFORMANCE_COUNTER_"></span>**Wie genau ist der Leistungsindikator?**
</dt> <dd>

Die Antwort hängt von einer Vielzahl von Faktoren ab. Weitere Informationen finden Sie unter Eigenschaften der Hardwareuhr auf [niedriger Ebene.](#low-level-hardware-clock-characteristics)

</dd> </dl>

## <a name="faq-about-programming-with-qpc-and-tsc"></a>Häufig gestellte Fragen zum Programmieren mit QPC und TSC

Hier finden Sie Antworten auf häufig gestellte Fragen zur Programmierung mit [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) und TSCs.

<dl> <dt>

<span id="I_need_to_convert_the_QPC_output_to_milliseconds._How_can_I_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="i_need_to_convert_the_qpc_output_to_milliseconds._how_can_i_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="I_NEED_TO_CONVERT_THE_QPC_OUTPUT_TO_MILLISECONDS._HOW_CAN_I_AVOID_LOSS_OF_________PRECISION_WITH_CONVERTING_TO_DOUBLE_OR_FLOAT_"></span>**Ich muss die QPC-Ausgabe in Millisekunden konvertieren. Wie kann ich Genauigkeitsverluste bei der Konvertierung in double oder float vermeiden?**
</dt> <dd>

Beim Ausführen von Berechnungen für ganzzahlige Leistungsindikatoren sind mehrere Punkte zu beachten:

-   Die Ganzzahldivision verliert den Rest. Dies kann in einigen Fällen zu Genauigkeitsverlusten führen.
-   Die Konvertierung zwischen 64-Bit-Ganzzahlen und Gleitkommawerten (double) kann zu Genauigkeitsverlusten führen, da die Gleitkomma-Mantisse nicht alle möglichen ganzzahligen Werte darstellen kann.
-   Die Multiplikation von 64-Bit-Ganzzahlen kann zu einem Ganzzahlüberlauf führen.

Grundsätzlich verzögern Sie diese Berechnungen und Konvertierungen so lange wie möglich, um eine Verschleierung der eingeführten Fehler zu vermeiden.

</dd> <dt>

<span id="How_can_I_convert_QPC_to_100_nanosecond_ticks_so_I_can_add_it_to_a_________FILETIME_"></span><span id="how_can_i_convert_qpc_to_100_nanosecond_ticks_so_i_can_add_it_to_a_________filetime_"></span><span id="HOW_CAN_I_CONVERT_QPC_TO_100_NANOSECOND_TICKS_SO_I_CAN_ADD_IT_TO_A_________FILETIME_"></span>**Wie kann ich QPC in 100 Nanosekunden-Ticks konvertieren, damit ich es einem FILETIME-Wert hinzufügen kann?**
</dt> <dd>

Eine Dateizeit ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen darstellt, die seit 12:00 Uhr verstrichen sind. 1. Januar 1601 koordinierte Weltzeit (UTC). Dateizeiten werden von Win32-API-Aufrufen verwendet, die die Tageszeit zurückgeben, z. B. [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) und [**GetSystemTimePreciseAsFileTime.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) Im Gegensatz dazu gibt [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Werte zurück, die die Zeit in Einheiten von 1/(die Häufigkeit des Von [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)abgerufenen Leistungsindikators) darstellen. Für die Konvertierung zwischen den  beiden Intervallen muss das Verhältnis des QPC-Intervalls und der Intervalle von 100 Nanosekunden berechnet werden. Achten Sie darauf, die Genauigkeit zu verlieren, da die Werte klein sein können (0,0000001 / 0,0000000340).

</dd> <dt>

<span id="Why_is_the_time_stamp_that_is_returned_from_QPC_a_signed_integer_"></span><span id="why_is_the_time_stamp_that_is_returned_from_qpc_a_signed_integer_"></span><span id="WHY_IS_THE_TIME_STAMP_THAT_IS_RETURNED_FROM_QPC_A_SIGNED_INTEGER_"></span>**Warum ist der zeitstempel, der von QPC zurückgegeben wird, eine ganze Zahl mit Vorzeichen?**
</dt> <dd>

Berechnungen [](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) mit QPC-Zeitstempeln können eine Subtraktion beinhalten. Mithilfe eines Vorzeichenwerts können Sie Berechnungen verarbeiten, die negative Werte liefern können.

</dd> <dt>

<span id="How_can_I_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="how_can_i_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="HOW_CAN_I_OBTAIN_HIGH_RESOLUTION_TIME_STAMPS_FROM_MANAGED_CODE_"></span>**Wie kann ich Zeitstempel mit hoher Auflösung aus verwaltetem Code abrufen?**
</dt> <dd>

Rufen Sie die [**Stopwatch.GetTimeStamp-Methode**](/previous-versions/windows/) aus der [**System.Diagnostics.Stopwatch-Klasse**](/previous-versions/windows/) auf. Ein Beispiel zur Verwendung von **Stopwatch.GetTimeStamp** finden Sie unter [Abrufen von Zeitstempeln mit hoher Auflösung aus verwaltetem Code.](#acquiring-high-resolution-time-stamps-from-managed-code)

</dd> <dt>

<span id="Under_what_circumstances_does_QueryPerformanceFrequency_return_FALSE__or_________QueryPerformanceCounter_return_zero_"></span><span id="under_what_circumstances_does_queryperformancefrequency_return_false__or_________queryperformancecounter_return_zero_"></span><span id="UNDER_WHAT_CIRCUMSTANCES_DOES_QUERYPERFORMANCEFREQUENCY_RETURN_FALSE__OR_________QUERYPERFORMANCECOUNTER_RETURN_ZERO_"></span>**Unter welchen Umständen gibt QueryPerformanceFrequency FALSE oder QueryPerformanceCounter 0 (null) zurück?**
</dt> <dd>

Dies geschieht auf keinem System, auf dem Windows XP oder höher ausgeführt wird.

</dd> <dt>

<span id="Do_I_need_to_set_the_thread_affinity_to_a_single_core_to_use_QPC_"></span><span id="do_i_need_to_set_the_thread_affinity_to_a_single_core_to_use_qpc_"></span><span id="DO_I_NEED_TO_SET_THE_THREAD_AFFINITY_TO_A_SINGLE_CORE_TO_USE_QPC_"></span>**Muss ich die Threadaffinität auf einen einzelnen Kern festlegen, um QPC zu verwenden?**
</dt> <dd>

Nein. Weitere Informationen finden Sie unter [Leitfaden zum Abrufen von Zeitstempeln.](#guidance-for-acquiring-time-stamps) Dieses Szenario ist weder notwendig noch wünschenswert. Die Ausführung dieses Szenarios kann sich negativ auf die Leistung Ihrer Anwendung auswirken, indem die Verarbeitung auf einen Kern beschränkt wird oder ein Engpass auf einem einzelnen Kern entsteht, wenn mehrere Threads ihre Affinität auf denselben Kern festlegen, wenn [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)aufgerufen wird.

</dd> </dl>

## <a name="low-level-hardware-clock-characteristics"></a>Merkmale der Hardwareuhr auf niedriger Ebene

In diesen Abschnitten werden die Merkmale der Hardwareuhr auf niedriger Ebene erläutert.

### <a name="absolute-clocks-and-difference-clocks"></a>Absolute Uhren und Differenzuhren

Absolute Uhren bieten genaue Tageszeitwerte. Sie basieren in der Regel auf koordinierte Weltzeit (UTC), und daher hängt ihre Genauigkeit teilweise davon ab, wie gut sie mit einem externen Zeitverweis synchronisiert werden. Differenzuhren messen Zeitintervalle und basieren in der Regel nicht auf einer externen Zeitepoche. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) ist eine Differenzuhr und wird nicht mit einer externen Zeitepoche oder einem externen Verweis synchronisiert. Wenn Sie **QPC** für Zeitintervallmessungen verwenden, erhalten Sie in der Regel eine bessere Genauigkeit als durch die Verwendung von Zeitstempeln, die von einer absoluten Uhr abgeleitet werden. Dies liegt daran, dass der Prozess der Synchronisierung der Zeit einer absoluten Uhr Phasen- und Häufigkeitsverschiebungen einführen kann, die die Unsicherheit bei kurzfristigen Zeitintervallmessungen erhöhen.

### <a name="resolution-precision-accuracy-and-stability"></a>Auflösung, Genauigkeit, Genauigkeit und Stabilität

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) verwendet einen Hardwarezähler als Grundlage. Hardwaretimer bestehen aus drei Teilen: einem Tick-Generator, einem Zähler, der die Takte zählt, und einem Mittel zum Abrufen des Indikatorwerts. Die Merkmale dieser drei Komponenten bestimmen die Auflösung, Genauigkeit, Genauigkeit und Stabilität von **QPC.**

Wenn ein Hardwaregenerator Ticks mit konstanter Geschwindigkeit bereitstellt, können Zeitintervalle gemessen werden, indem diese Ticks einfach gezählt werden. Die Rate, mit der die Takte generiert werden, wird als Häufigkeit bezeichnet und in Hertz (Hz) ausgedrückt. Der Kehrwert der Häufigkeit wird als Zeitraum oder Taktintervall bezeichnet und in einer entsprechenden SI-Zeiteinheit (International System of Units) ausgedrückt (z. B. Sekunde, Millisekunde, Mikrosekunde oder Nanosekunde).

![Zeitintervall](images/tick-interval.png)

Die Auflösung des Timers entspricht dem Zeitraum. Die Auflösung bestimmt die Fähigkeit, zwischen zwei beliebigen Zeitstempeln zu unterscheiden, und legt eine Untergrenze in den kleinsten Zeitintervallen fest, die gemessen werden können. Dies wird manchmal als Teilstrichauflösung bezeichnet.

Die digitale Zeitmessung führt zu einer Ungenauigkeit von ± 1 Tick, da sich der digitale Indikator in diskreten Schritten fortschreitet, während die Zeit kontinuierlich weiterentwickelt wird. Diese Unsicherheit wird als Quantisierungsfehler bezeichnet. Bei typischen Zeitintervallmessungen kann dieser Effekt häufig ignoriert werden, da der Quantisierungsfehler viel kleiner als das gemessene Zeitintervall ist.

![Digitale Zeitmessung](images/digital-time-measure.png)

Wenn der gemessene Zeitraum jedoch klein ist und sich der Auflösung des Timers nähert, müssen Sie diesen Quantisierungsfehler berücksichtigen. Die Größe des eingeführten Fehlers ist die eines Uhrzeitraums.

Die folgenden beiden Diagramme veranschaulichen die Auswirkungen der ± 1-Teilstrich-Unsicherheit mithilfe eines Timers mit einer Auflösung von 1 Zeiteinheit.

![Tickunsicherheit](images/tick-uncertainty.png)

[**QueryPerformanceFrequency gibt**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) die Häufigkeit von [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)zurück, und der Punkt und die Auflösung entsprechen dem Kehrwert dieses Werts. Die Häufigkeit des Leistungsindikators, die **QueryPerformanceFrequency** zurückgibt, wird während der Systemin initialisierung bestimmt und ändert sich nicht, während das System ausgeführt wird.

> [!Note]  
> Möglicherweise gibt es [**Fälle, in denen QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) nicht die tatsächliche Frequenz des Hardware-Tick-Generators zurücksendet. Beispielsweise gibt **QueryPerformanceFrequency** in vielen Fällen die TSC-Häufigkeit dividiert durch 1024 zurück. und bei Hyper-V beträgt die Frequenz des Leistungsindikators immer 10 MHz, wenn der virtuelle Gastcomputer unter einem [Hypervisor](https://msdn.microsoft.com/library/Ff542584(v=VS.85).aspx) ausgeführt wird, der die [Hypervisor-Schnittstelle version 1.0 implementiert.](https://msdn.microsoft.com/library/Ff541458(v=VS.85).aspx) Gehen Sie daher nicht davon aus, dass **QueryPerformanceFrequency** die genaue TSC-Häufigkeit zurück gibt.

 

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) liest den Leistungsindikator und gibt die Gesamtzahl der Ticks zurück, die seit dem Start des Windows-Betriebssystems aufgetreten sind, einschließlich der Zeit, zu der sich der Computer im Standbymodus, Ruhezustand oder verbundener Standbymodus befindet.

In diesen Beispielen wird gezeigt, wie Sie das Taktintervall und die Auflösung berechnen und die Taktanzahl in einen Zeitwert konvertieren.

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Beispiel 1**
</dt> <dd>

[**QueryPerformanceFrequency gibt**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) den Wert 3.125.000 auf einem bestimmten Computer zurück. Wie sieht das Taktintervall und die Auflösung von [**QPC-Messungen**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) auf diesem Computer aus? Das Taktintervall oder der Zeitraum ist der Kehrzeitraum von 3.125.000, was 0,000000320 (320 Nanosekunden) ist. Daher stellt jeder Teilstrich die Übergabe von 320 Nanosekunden dar. Zeitintervalle, die kleiner als 320 Nanosekunden sind, können auf diesem Computer nicht gemessen werden.

Taktintervall = 1/(Leistungshäufigkeit)

Taktintervall = 1/3.125.000 = 320 ns

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Beispiel 2**
</dt> <dd>

Auf demselben Computer wie im vorherigen Beispiel beträgt der Unterschied zwischen den Werten, die von zwei aufeinander folgenden Aufrufen von [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) zurückgegeben werden, 5. Wie viel Zeit ist zwischen den beiden Aufrufen verstrichen? 5 Ticks multipliziert mit 320 Nanosekunden ergeben 1,6 Mikrosekunden.

ElapsedTime = Ticks \* Tick Interval

ElapsedTime = 5 \* 320 ns = 1,6 μs

</dd> </dl>

Es dauert eine Weile, bis der Zugriff auf den Teilstrichzähler aus der Software erfolgt (gelesen), und diese Zugriffszeit kann die Genauigkeit der Zeitmessung verringern. Dies liegt daran, dass die minimale Intervallzeit (das kleinste Zeitintervall, das gemessen werden kann) die größere Auflösung und die Zugriffszeit ist.

Precision = MAX \[ Resolution, AccessTime\]

Betrachten Sie beispielsweise einen hypothetischen Hardwarezeitler mit einer Auflösung von 100 Nanosekunden und einer Zugriffszeit von 800 Nanosekunden. Dies kann der Fall sein, wenn der Plattformzeiter anstelle des TSC-Registers als Grundlage für [**QPC verwendet wurde.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Daher beträgt die Genauigkeit 800 Nanosekunden und nicht 100 Nanosekunden, wie in dieser Berechnung dargestellt.

Genauigkeit = MAX \[ 800 ns,100 ns \] = 800 ns

Diese beiden Abbildungen zeigen diesen Effekt.

![qpc-Zugriffszeit](images/qpc-access-time.png)

Wenn die Zugriffszeit größer als die Auflösung ist, versuchen Sie nicht, die Genauigkeit durch Erraten zu verbessern. Anders ausgedrückt: Es ist ein Fehler, davon auszugehen, dass der Zeitstempel genau in der Mitte oder am Anfang oder Ende des Aufrufs genommen wird.

Betrachten Sie im Gegensatz dazu das folgende Beispiel, in dem die [**QPC-Zugriffszeit**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) nur 20 Nanosekunden und die Hardwareuhrauflösung 100 Nanosekunden beträgt. Dies kann der Fall sein, wenn das TSC-Register als Grundlage für **QPC verwendet wurde.** Hier wird die Genauigkeit durch die Uhrauflösung eingeschränkt.

![qpc precision](images/qpc-precision.png)

In der Praxis finden Sie Zeitquellen, deren Zeit zum Lesen des Leistungsindikators größer oder kleiner als die Auflösung ist. In beiden Fällen ist die Genauigkeit die größere der beiden.

Diese Tabelle enthält Informationen zur ungefähren Auflösung, Zugriffszeit und Genauigkeit einer Vielzahl von Uhren. Beachten Sie, dass einige der Werte je nach Prozessor, Hardwareplattformen und Prozessorgeschwindigkeit variieren.



| Clock Source                                                      | Nominale Taktfrequenz | Uhrauflösung    | Zugriffszeit (typisch) | Genauigkeit       |
|-------------------------------------------------------------------|-------------------------|---------------------|-----------------------|-----------------|
| PC RTC                                                            | 64 Hz                   | 15,625 Millisekunden | Nicht zutreffend                   | Nicht zutreffend             |
| Abfrageleistungsindikator mit TSC mit einer Prozessoruhr mit 3 GHz  | 3 MHz                   | 333 Nanosekunden     | 30 Nanosekunden        | 333 Nanosekunden |
| **RDTSC-Computeranweisung** auf einem System mit einer Zykluszeit von 3 GHz | 3 GHz                   | 333 Millisekunden     | 30 Nanosekunden        | 30 Nanosekunden  |



 

Da [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) einen Hardwarezähler verwendet, können Sie sich mit den Funktionen und Einschränkungen von QPC auskennen, wenn Sie sich mit einigen grundlegenden Merkmalen von **Hardwareindikatoren auskennen.**

Der am häufigsten verwendete Hardware-Tick-Generator ist ein Oszillator. Bei dem Eis ist es sich um ein kleines Stück Bzw. anderes Material aus Bzw. mit Material aus Demos, das eine kostengünstige Häufigkeitsreferenz mit hervorragender Stabilität und Genauigkeit bietet. Diese Häufigkeit wird verwendet, um die Ticks zu generieren, die von der Uhr gezählt werden.

Die Genauigkeit eines Timers bezieht sich auf den Grad der Übereinstimmung mit einem TRUE- oder Standardwert. Dies hängt in erster Linie davon ab, ob der Oszillator Ticks mit der angegebenen Häufigkeit bereitstellen kann. Wenn die Häufigkeit der Oszillation zu hoch ist, wird die Uhr "schnell ausgeführt", und gemessene Intervalle werden länger angezeigt, als sie tatsächlich sind. Und wenn die Häufigkeit zu niedrig ist, wird die Uhr langsam ausgeführt, und die gemessenen Intervalle erscheinen kürzer als tatsächlich.

Bei typischen Zeitintervallmessungen für kurze Dauer (z. B. Antwortzeitmessungen, Netzwerklatenzmessungen und so weiter) ist die Genauigkeit des Hardwareoszillators in der Regel ausreichend. Bei einigen Messungen wird die Genauigkeit der Oszillatorfrequenz jedoch wichtig, insbesondere für lange Zeitintervalle oder wenn Sie Messungen vergleichen möchten, die auf verschiedenen Computern durchgeführt wurden. Im restlichen Teil dieses Abschnitts werden die Auswirkungen der Oszillatorgenauigkeit untersucht.

Die Oszillationshäufigkeit der Eiskugeln wird während des Fertigungsprozesses festgelegt und vom Hersteller als angegebene Häufigkeit plus oder minus einer in "Parts per Million" (ppm) ausgedrückten Fertigungstoleranz angegeben, die als maximale Häufigkeitsoffset bezeichnet wird. Ein Eis mit einer angegebenen Frequenz von 1.000.000 Hz und einem maximalen Frequenzoffset von ± 10 ppm würde innerhalb der Spezifikationsgrenzwerte liegen, wenn die tatsächliche Frequenz zwischen 999.990 Hz und 1.000.010 Hz liegt.

Indem wir die Ausdrucksteile pro Million durch Mikrosekunden pro Sekunde substituieren, können wir diesen Häufigkeitsoffsetfehler auf Zeitintervallmessungen anwenden. Ein Oszillator mit einem Offset von + 10 ppm würde einen Fehler von 10 Mikrosekunden pro Sekunde haben. Entsprechend wird beim Messen eines Intervalls von 1 Sekunde schnell und ein Intervall von 1 Sekunde als 0,999990 Sekunden gemessen.

Ein praktischer Verweis ist, dass ein Häufigkeitsfehler von 100 ppm nach 24 Stunden einen Fehler von 8,64 Sekunden verursacht. In dieser Tabelle wird die Ungenauigkeit der Messung aufgrund des akkumulierten Fehlers für längere Zeitintervalle dargestellt.



| Dauer des Zeitintervalls | Messungsungenauigkeit aufgrund eines akkumulierten Fehlers mit +/- 10 PPM Häufigkeitstoleranz |
|------------------------|--------------------------------------------------------------------------------------|
| 1 Mikrosekunde          | ± 10 Millisekunden (10-12)                                                             |
| 1 Millisekunde          | ± 10 Nanosekunden (10-9)                                                              |
| 1 Sekunde               | ± 10 Mikrosekunden                                                                    |
| 1 Stunde                 | ± 60 Mikrosekunden                                                                    |
| 1 Tag                  | ± 0,86 Sekunden                                                                       |
| 1 Woche                 | ± 6,08 Sekunden                                                                       |



 

Die obige Tabelle zeigt, dass der Frequency Offset-Fehler bei kleinen Zeitintervallen häufig ignoriert werden kann. Bei langen Zeitintervallen kann jedoch selbst ein kleiner Frequenzoffset zu einer erheblichen Verunsicherung der Messung führen.

Die in Personalcomputern und Servern verwendeten Oszillatoren werden in der Regel mit einer Frequenztoleranz von ± 30 bis 50 Teilen pro Million hergestellt, und selten können Dies bis zu 500 ppm betragen. Obwohl Bänder mit viel engeren Frequenzoffsettoleranzen verfügbar sind, sind sie teurer und werden daher auf den meisten Computern nicht verwendet.

Um die negativen Auswirkungen dieses Häufigkeitsoffsetfehlers zu reduzieren, verwenden aktuelle Versionen von Windows, insbesondere Windows 8, mehrere Hardware-Timer, um den Frequenzoffset zu erkennen und so weit wie möglich zu kompensieren. Dieser Kalibrierungsprozess wird ausgeführt, wenn Windows gestartet wird.

Wie die folgenden Beispiele zeigen, wirkt sich der Frequenzoffsetfehler einer Hardwareuhr auf die erreichbare Genauigkeit aus, und die Auflösung der Uhr kann weniger wichtig sein.

![Häufigkeitsoffsetfehler beeinflusst erreichbare Genauigkeit](images/freq-offset-error.png)

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Beispiel 1**
</dt> <dd>

Angenommen, Sie führen Zeitintervallmessungen durch, indem Sie einen 1-MHz-Oszillator mit einer Auflösung von 1 Mikrosekunde und einen maximalen Frequency Offset-Fehler von ±50 ppm verwenden. Nehmen wir nun an, dass der Offset genau +50 ppm beträgt. Dies bedeutet, dass die tatsächliche Frequenz 1.000.050 Hz beträgt. Wenn wir ein Zeitintervall von 24 Stunden gemessen haben, wäre unsere Messung 4,3 Sekunden zu kurz (23:59:55.700.0000 im Vergleich zu 24:00:00.000000 tatsächlich).

Sekunden pro Tag = 86400

Frequency offset error = 50 ppm = 0.00005

86.400 Sekunden \* 0,00005 = 4,3 Sekunden

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Beispiel 2**
</dt> <dd>

Angenommen, die TSC-Prozessoruhr wird von einem Oszillator gesteuert und hat eine Frequenz von 3 GHz angegeben. Dies bedeutet, dass die Auflösung 1/3.000.000.000 oder etwa 333 Millisekunden beträgt. Angenommen, der zur Steuerung der Prozessoruhr verwendete 100000000 hat eine Frequenztoleranz von ±50 ppm und beträgt tatsächlich +50 ppm. Trotz der beeindruckenden Auflösung ist eine Zeitintervallmessung von 24 Stunden immer noch 4,3 Sekunden zu kurz. (23:59:55.7000000000 im Vergleich zu 24:00:00.0000000000 tatsächlich).

Sekunden pro Tag = 86400

Frequency offset error = 50 ppm = 0.00005

86.400 Sekunden \* 0,00005 = 4,3 Sekunden

Dies zeigt, dass eine TSC-Uhr mit hoher Auflösung nicht notwendigerweise genauere Messungen als eine Uhr mit niedrigerer Auflösung bietet.

</dd> <dt>

<span id="Example_3"></span><span id="example_3"></span><span id="EXAMPLE_3"></span>**Beispiel 3**
</dt> <dd>

Erwägen Sie die Verwendung von zwei verschiedenen Computern, um das gleiche 24-Stunden-Zeitintervall zu messen. Beide Computer verfügen über einen Oszillator mit einem maximalen Frequenzoffset von ± 50 ppm. Wie weit ist die Messung des gleichen Zeitintervalls auf diesen beiden Systemen voneinander entfernt? Wie in den vorherigen Beispielen ergibt ± 50 ppm einen maximalen Fehler von ± 4,3 Sekunden nach 24 Stunden. Wenn ein System 4,3 Sekunden schnell und das andere 4,3 Sekunden langsam ausgeführt wird, kann der maximale Fehler nach 24 Stunden 8,6 Sekunden beträgt.

Sekunden pro Tag = 86400

Frequency offset error = ±50 ppm = ±0.00005

±(86.400 Sekunden \* 0,00005) = ±4,3 Sekunden

Maximaler Offset zwischen den beiden Systemen = 8,6 Sekunden

Zusammenfassend wird der Häufigkeitsoffsetfehler immer wichtiger, wenn lange Zeitintervalle gemessen und Messungen zwischen verschiedenen Systemen verglichen werden.

Die Stabilität eines Timers beschreibt, ob sich die Taktfrequenz im Laufe der Zeit ändert, z. B. als Ergebnis von Temperaturänderungen. Die Als Tick-Generatoren auf Computern verwendeten Eiskugeln weisen kleine Änderungen an der Frequenz als Funktion der Temperatur auf. Der durch eine driftbedingte Abweichung verursachte Fehler ist im Vergleich zum Frequenzoffsetfehler für allgemeine Temperaturbereiche in der Regel klein. Designer von Software für tragbare Geräte oder Geräte, die großen Temperaturschwankungen ausgesetzt sind, müssen diesen Effekt jedoch möglicherweise berücksichtigen.

</dd> </dl>

## <a name="hardware-timer-info"></a>Hardware-Timerinformationen

<dl> <dt>

<span id="TSC_Register"></span><span id="tsc_register"></span><span id="TSC_REGISTER"></span>**TSC-Registrierung**
</dt> <dd>

Einige Intel- und AMD-Prozessoren enthalten ein TSC-Register, bei dem es sich um ein 64-Bit-Register handelt, das sich mit einer hohen Rate erhöht, in der Regel gleich der Prozessoruhr. Der Wert dieses Leistungsindikators kann durch die **RDTSC-** oder **RDTSCP-Computeranweisungen** gelesen werden, was je nach Prozessor eine sehr geringe Zugriffszeit und Rechenkosten in der Reihenfolge von Dutzenden oder Hunderten von Computerzyklen bietet.

Obwohl das TSC-Register wie ein idealer Zeitstempelmechanismus aussieht, gibt es hier Situationen, in denen es zu Zeitmessungszwecken nicht zuverlässig funktionieren kann:

-   Nicht alle Prozessoren verfügen über TSC-Register, sodass die direkte Verwendung des TSC-Registers in software ein Portabilitätsproblem verursacht. (Windows wählt in diesem Fall eine alternative Zeitquelle für [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) aus, wodurch das Portabilitätsproblem vermieden wird.)
-   Einige Prozessoren können die Häufigkeit der TSC-Uhr ändern oder die Weiterentwicklung des TSC-Registers beenden, wodurch der TSC für Zeitsteuerungszwecke auf diesen Prozessoren nicht geeignet ist. Diese Prozessoren verfügen über nicht invariante TSC-Register. (Windows erkennt dies automatisch und wählt eine alternative Zeitquelle für [**QPC aus.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
-   Auf Systemen mit mehreren Prozessoren oder mit mehreren Kernen können einige Prozessoren und Systeme die Uhren auf jedem Kern nicht mit demselben Wert synchronisieren. (Windows erkennt dies automatisch und wählt eine alternative Zeitquelle für [**QPC aus.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
-   Bei einigen großen Systemen mit mehreren Prozessoren können Sie die Prozessoruhren möglicherweise nicht mit demselben Wert synchronisieren, auch wenn der Prozessor über einen invarianten TSC verfügt. (Windows erkennt dies automatisch und wählt eine alternative Zeitquelle für [**QPC aus.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
-   Einige Prozessoren führen Anweisungen nicht in der angegebenen Reihenfolge aus. Dies kann zu falschen Zykluszahlen führen, wenn **RDTSC** verwendet wird, um Anweisungssequenzen zu zeitverfolgen, da die **RDTSC-Anweisung** möglicherweise zu einem anderen Zeitpunkt als im Programm angegeben ausgeführt wird. Die **RDTSCP-Anweisung** wurde auf einigen Prozessoren als Reaktion auf dieses Problem eingeführt.

Wie andere Timer basiert der TSC auf einem Oszillator, dessen genaue Häufigkeit nicht im Voraus bekannt ist und der einen Frequency Offset-Fehler auft. Bevor sie verwendet werden kann, muss sie daher mithilfe eines anderen Zeitsteuerungsverweises kalibriert werden.

Während der Systemin initialisierung überprüft Windows, ob der TSC für zeitliche Steuerungszwecke geeignet ist, und führt die erforderliche Häufigkeits- und Kernsynchronisierung durch.

</dd> <dt>

<span id="PM_Clock"></span><span id="pm_clock"></span><span id="PM_CLOCK"></span>**PM-Uhr**
</dt> <dd>

Der ACPI-Timer, auch als PM-Uhr bezeichnet, wurde der Systemarchitektur hinzugefügt, um zuverlässige Zeitstempel unabhängig von der Prozessorgeschwindigkeit zu bieten. Da dies das einzige Ziel dieses Timers war, stellt er einen Zeitstempel in einem einzelnen Uhrzyklus zur Verfügung, bietet jedoch keine anderen Funktionen.

</dd> <dt>

<span id="HPET_Timer"></span><span id="hpet_timer"></span><span id="HPET_TIMER"></span>**HPET-Timer**
</dt> <dd>

Der High Precision Event Timer (HPET) wurde gemeinsam von Intel und Microsoft entwickelt, um die Zeitanforderungen von Multimedia und anderen zeitempfindlichen Anwendungen zu erfüllen. DIE HPET-Unterstützung ist seit Windows Vista Windows verfügbar, und Windows 7- und Windows 8-Hardwarelogo-Zertifizierung erfordert HPET-Unterstützung auf der Hardwareplattform.

</dd> </dl>

 

 
