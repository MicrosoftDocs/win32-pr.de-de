---
description: Windows stellt APIs bereit, mit denen Sie Zeitstempel mit hoher Auflösung abrufen oder Zeitintervalle messen können.
ms.assetid: D66E0FC2-3AF2-489B-B4B5-78648905B77B
title: Abrufen von Zeitstempeln mit hoher Auflösung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9a1300967738b717ab8d8c822bf2af3f6a4a7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960997"
---
# <a name="acquiring-high-resolution-time-stamps"></a>Abrufen von Zeitstempeln mit hoher Auflösung

Windows stellt APIs bereit, mit denen Sie Zeitstempel mit hoher Auflösung abrufen oder Zeitintervalle messen können. Die primäre API für nativen Code ist " [**QueryPerformanceCounter" (QPC)**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Für Gerätetreiber ist die [**kernelmodusapi KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter). Bei verwaltetem Code verwendet die [**System. Diagnostics. Stopwatch**](/previous-versions/windows/) -Klasse **QPC** als genaue Zeit.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) ist unabhängig von und wird nicht mit einem externen Zeit Verweis synchronisiert. Zum Abrufen von Zeitstempeln, die mit einem externen Zeit Verweis synchronisiert werden können, z. b. koordinierte Weltzeit (UTC) zur Verwendung in zeitgesteuerten Messungen mit hoher Auflösung, verwenden Sie [**getsystemtimepreciseasfiletime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

Zeitstempel und Zeitintervall Messungen sind ein wesentlicher Bestandteil der Leistungsmessungen für Computer und Netzwerk. Zu diesen Leistungs Messungs Vorgängen zählen die Berechnung der Antwortzeit, des Durchsatzes und der Latenz sowie die Profilerstellung für Code. Jeder dieser Vorgänge umfasst eine Messung von Aktivitäten, die während eines Zeitintervalls auftreten, das von einem Start-und einem End-Ereignis definiert wird, das unabhängig von einem externen uhrzeitverweis sein kann.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) ist in der Regel die beste Methode zum Zeitstempel von Ereignissen und zum Messen kleiner Zeitintervalle, die auf dem gleichen System oder virtuellen Computer auftreten. Sie sollten [**getsystemtimepreciseasfiletime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) verwenden, wenn Sie Zeitstempel Ereignisse auf mehreren Computern verwenden möchten, vorausgesetzt, dass jeder Computer an einem Zeit Synchronisierungs Schema wie z. b. Network Time Protocol (NTP) teilnimmt. **QPC** hilft Ihnen, Probleme zu vermeiden, die bei anderen Zeit Messungs Ansätzen auftreten können, z. b. das direkte Lesen des Zeitstempel Zählers ("Zeitstempel") des Prozessors.

-   [QPC-Unterstützung in Windows-Versionen](#qpc-support-in-windows-versions)
-   [Leitfaden zum Abrufen von Zeitstempeln](#guidance-for-acquiring-time-stamps)
    -   [Virtualisierung](#virtualization)
    -   [Direkte Verwendung von TSC](#direct-tsc-usage)
    -   [Beispiele für das Abrufen von Zeitstempeln](#examples-for-acquiring-time-stamps)
-   [Allgemeine häufig gestellte Fragen zu QPC und TSC](#general-faq-about-qpc-and-tsc)
-   [Häufig gestellte Fragen zum Programmieren mit QPC und TSC](#faq-about-programming-with-qpc-and-tsc)
-   [Hardware Takt Merkmale auf niedriger Ebene](#low-level-hardware-clock-characteristics)
    -   [Absolute Uhren und Differenz Uhren](#absolute-clocks-and-difference-clocks)
    -   [Auflösung, Genauigkeit, Genauigkeit und Stabilität](#resolution-precision-accuracy-and-stability)
-   [Informationen zum Hardware-Timer](#hardware-timer-info)

## <a name="qpc-support-in-windows-versions"></a>QPC-Unterstützung in Windows-Versionen

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) wurde in Windows 2000 und Windows XP eingeführt und wurde entwickelt, um die Verbesserungen an der Hardwareplattform und den Prozessoren zu nutzen. Hier beschreiben wir die Merkmale von **QPC** unter verschiedenen Windows-Versionen, die Sie bei der Wartung von Software unterstützen, die auf diesen Windows-Versionen ausgeführt wird.

### <a name="windows-xp-and-windows-2000"></a>Windows XP und Windows 2000

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) ist unter Windows XP und Windows 2000 verfügbar und funktioniert auf den meisten Systemen gut. Allerdings haben einige Hardwaresystem-BIOS keine ordnungsgemäße Hardware-CPU-Merkmale (ein nicht invarianter TSC) angegeben, und einige Multikern-oder Multiprozessorsysteme verwendeten Prozessoren mit TSCs, die nicht über Kerne synchronisiert werden konnten. Systeme mit einer fehlerhaften Firmware, die diese Versionen von Windows ausführen, bieten möglicherweise nicht denselben **QPC** -Lesevorgang auf unterschiedlichen Kernen, wenn Sie den TSC als Grundlage für **QPC** verwendet haben.

### <a name="windows-vista-and-windows-server-2008"></a>Windows Vista und Windows Server 2008

Auf allen Computern, die mit Windows Vista und Windows Server 2008 ausgeliefert wurden, wurde ein Platt Form Zähler (HPET) oder der ACPI-Energie Verwaltungszeit Geber (PM-Timer) als Grundlage für [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)verwendet. Solche Platt Form Timer haben eine höhere Zugriffs Latenz als der TSC und werden von mehreren Prozessoren gemeinsam genutzt. Dadurch wird die Skalierbarkeit von **QPC** eingeschränkt, wenn Sie gleichzeitig von mehreren Prozessoren aufgerufen wird.

### <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 und Windows Server 2008 R2

Die meisten Windows 7-und Windows Server 2008 R2-Computer verfügen über Prozessoren mit konstantem TSCs und verwenden diese Leistungsindikatoren als Grundlage für [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). TSCs sind Hardware Indikatoren mit hoher Auflösung pro Prozessor, auf die mit sehr geringer Latenz und mehr Aufwand (je nach Prozessortyp) zugegriffen werden kann. Windows 7 und Windows Server 2008 R2 verwenden TSCs als Grundlage von **QPC** auf Einzel-Uhr-Domänen Systemen, in denen das Betriebssystem (oder der Hypervisor) die einzelnen TSCs während der Systeminitialisierung eng auf alle Prozessoren synchronisieren kann. Auf solchen Systemen sind die Kosten für das Lesen des Leistungs Zählers deutlich niedriger als die Systeme, die einen Platt Form Leistungstest verwenden. Außerdem gibt es keinen zusätzlichen mehr Aufwand für gleichzeitige Aufrufe, und im benutzermodusabfragen werden häufig Systemaufrufe umgangen, was den Aufwand weiter reduziert. Auf Systemen, auf denen sich der TSC nicht für die Zeit Aufbewahrung eignet, wählt Windows automatisch einen Platt Form Zähler (entweder den HPET-Timer oder den ACPI-pm-Timer) als Grundlage für **QPC** aus.

### <a name="windows-8-windows-81-windows-server-2012-and-windows-server-2012-r2"></a>Windows 8, Windows 8.1, Windows Server 2012 und Windows Server 2012 R2

Windows 8, Windows 8.1, Windows Server 2012 und Windows Server 2012 R2 verwenden TSCs als Grundlage für den Leistungs Leistungstest. Der TSC-Synchronisierungs Algorithmus wurde erheblich verbessert, um große Systeme mit vielen Prozessoren besser zu unterstützen. Außerdem wurde die Unterstützung für die neue präzise Tages-API hinzugefügt, die das Abrufen präziser Zeitstempel für die Zeit des Betriebssystems ermöglicht. Weitere Informationen finden Sie unter [**getsystemtimepreciseasfiletime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). Auf Windows RT-PC-Plattformen basiert der Leistungs Zähler entweder auf einem proprietären Platt Form Zähler oder auf dem System Zähler, der vom generischen Timer für Windows RT-PCs bereitgestellt wird, wenn die Plattform so ausgestattet ist.

## <a name="guidance-for-acquiring-time-stamps"></a>Leitfaden zum Abrufen von Zeitstempeln

Windows verfügt über und wird weiterhin in die Bereitstellung eines zuverlässigen und effizienten Leistungs Zählers investieren. Wenn Sie Zeitstempel mit einer Auflösung von 1 Mikrosekunden oder besser benötigen und die Zeitstempel nicht mit einem externen Zeit Verweis synchronisiert werden müssen, wählen Sie [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter), [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter)oder [**kequeryinterrupttimepräzisen**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise)aus. Wenn Sie UTC-synchronisierte Zeitstempel mit einer Auflösung von 1 Mikrosekunden oder besser benötigen, wählen Sie [**getsystemtimepreciseasfiletime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) oder [**kequerysystemtimeprecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequerysystemtimeprecise)aus.

Auf einer relativ kleinen Anzahl von Plattformen, die das TSC-Register nicht als [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) verwenden können, z. b. aus den in Hardware Zeit Geber [Informationen](#hardware-timer-info)erläuterten Gründen, kann das Abrufen von Zeitstempeln mit hoher Auflösung erheblich teurer sein als das Abrufen von Zeitstempeln mit niedrigerer Auflösung. Wenn die Auflösung von 10 bis 16 Millisekunden ausreichend ist, können Sie mit [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64), [**queryinterrupttime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**queryunbiasedinterrupttime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), [**kequeryinterrupttime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttime)oder [**kequeryunbiasedinterrupttime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryunbiasedinterrupttime) Zeitstempel abrufen, die nicht mit einem externen Zeit Verweis synchronisiert werden. Verwenden Sie für UTC-synchronisierte Zeitstempel [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) oder [**kequerysystemtime**](/windows-hardware/drivers/ddi/wdm/nf-wdm-kequerysystemtime~r1). Wenn eine höhere Auflösung erforderlich ist, können Sie stattdessen " [**queryinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)", " [**queryunbiasedinterrupttimepräzisen**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)" oder " [**kequeryinterrupttimepräzisen**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) " verwenden, um stattdessen Zeitstempel zu erhalten.

Im Allgemeinen sind die Ergebnisse des Leistungs Zählers für alle Prozessoren in Multikern-und Multiprozessorsystemen konsistent, auch wenn Sie in verschiedenen Threads oder Prozessen gemessen werden. Hier sind einige Ausnahmen zu dieser Regel:

-   Betriebssysteme vor Windows Vista, die auf bestimmten Prozessoren ausgeführt werden, können aufgrund eines der folgenden Gründe gegen diese Konsistenz verstoßen:

    -   Die Hardware Prozessoren verfügen über einen nicht invarianten TSC, und das BIOS zeigt diese Bedingung nicht ordnungsgemäß an.
    -   Der verwendete TSC-Synchronisierungs Algorithmus war nicht für Systeme mit einer großen Anzahl von Prozessoren geeignet.

-   Wenn Sie Leistungs Zähler Ergebnisse vergleichen, die aus unterschiedlichen Threads abgerufen werden, sollten Sie Werte, die sich durch einen Takt von ± 1 unterscheiden, auf eine mehrdeutige Reihenfolge Wenn die Zeitstempel aus demselben Thread entnommen werden, trifft diese Ungewissheit nicht zu. In diesem Kontext bezieht sich der Begriff Tick auf einen Zeitrahmen von 1 bis (die Häufigkeit des Leistungs Zählers, der von [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)abgerufen wird).

Wenn Sie den Leistungswert für große Serversysteme mit Multi-Clock-Domänen verwenden, die nicht in der Hardware synchronisiert werden, stellt Windows fest, dass der TSC nicht zu Zeit Steuerungs Zwecken verwendet werden kann [](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Obwohl dieses Szenario weiterhin zuverlässige Zeitstempel liefert, wirkt sich dies negativ auf die Zugriffs Latenz und die Skalierbarkeit aus. Verwenden Sie daher, wie bereits im vorherigen Leitfaden erläutert, nur die APIs, die eine Mikrosekunde oder eine bessere Auflösung bieten, wenn eine derartige Lösung erforderlich ist. Der TSC wird als Grundlage für **QPC** auf Multi-Clock-Domänen Systemen verwendet, die die Hardware Synchronisierung aller prozessortaksdomänen umfassen, da diese effektiv als ein einzelnes Takt-Domänen System fungieren.

Die Häufigkeit des Leistungs Zählers wird beim Systemstart korrigiert und ist für alle Prozessoren konsistent, sodass Sie nur die Häufigkeit von [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) Abfragen müssen, wenn die Anwendung initialisiert wird, und dann das Ergebnis Zwischenspeichern.

### <a name="virtualization"></a>Virtualisierung

Es wird erwartet, dass der Leistungs Zähler auf allen virtuellen Gast Computern, die auf ordnungsgemäß implementierten Hypervisoren ausgeführt werden, zuverlässig funktioniert. Hypervisoren, die die Schnittstelle der Hypervisor-Version 1,0 erfüllen und die Referenzzeit-Erleuchtung zur Verfügung stellen, können jedoch einen erheblich geringeren Aufwand bieten. Weitere Informationen zu Hypervisor-Schnittstellen und-Implementierungen finden Sie unter [Hypervisor-Spezifikationen](/virtualization/hyper-v-on-windows/reference/tlfs).

### <a name="direct-tsc-usage"></a>Direkte Verwendung von TSC

Wir raten dringend davon ab, die Prozessor Anweisung **RDTSC** oder **rdtscp** zu verwenden, um den TSC direkt abzufragen, da Sie bei einigen Versionen von Windows, bei Live Migrationen von virtuellen Computern und bei Hardwaresystemen ohne Invarianz oder eng synchronisierten TSCs keine zuverlässigen Ergebnisse erhalten. Stattdessen empfehlen wir Ihnen, [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) zu verwenden, um die Abstraktion, Konsistenz und Portabilität zu nutzen, die es bietet.

### <a name="examples-for-acquiring-time-stamps"></a>Beispiele für das Abrufen von Zeitstempeln

In den verschiedenen Codebeispielen in diesen Abschnitten wird gezeigt, wie Sie Zeitstempel erhalten.

### <a name="using-qpc-in-native-code"></a>Verwenden von QPC in nativem Code

In diesem Beispiel wird gezeigt, wie Sie [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) in nativem C-und C++-Code verwenden.


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

Dieses Beispiel zeigt die Verwendung der [**System. Diagnostics. Stopwatch**](/previous-versions/windows/) -Klasse von Managed Code.


```CSharp
using System.Diagnostics;

long StartingTime = Stopwatch.GetTimestamp();

// Activity to be timed

long EndingTime  = Stopwatch.GetTimestamp();
long ElapsedTime = EndingTime - StartingTime;

double ElapsedSeconds = ElapsedTime * (1.0 / Stopwatch.Frequency);
```



Die [**System. Diagnostics. Stopwatch**](/previous-versions/windows/) -Klasse bietet auch mehrere praktische Methoden zum Durchführen von Zeitintervall Messungen.

### <a name="using-qpc-from-kernel-mode"></a>Verwenden von QPC aus dem Kernel Modus

Der Windows-Kernel ermöglicht den kernelmoduszugriff auf den Leistungsdaten Träger über [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) , von dem sowohl der Leistungs-als auch die Leistungs Häufigkeit abgerufen werden kann. **KeQueryPerformanceCounter** ist nur im Kernel Modus verfügbar und wird für Writer von Gerätetreibern und anderen Kernelmoduskomponenten bereitgestellt.

In diesem Beispiel wird gezeigt, wie [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) im C-und C++-Kernelmodus verwendet wird.


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

<span id="Is_QueryPerformanceCounter___the_same_as_the_Win32_GetTickCount___or_________GetTickCount64___function_"></span><span id="is_queryperformancecounter___the_same_as_the_win32_gettickcount___or_________gettickcount64___function_"></span><span id="IS_QUERYPERFORMANCECOUNTER___THE_SAME_AS_THE_WIN32_GETTICKCOUNT___OR_________GETTICKCOUNT64___FUNCTION_"></span>**Ist QueryPerformanceCounter () identisch mit der Win32-Funktion GetTickCount () oder GetTickCount64 ()?**
</dt> <dd>

Nein. " [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) " und " [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) " sind nicht mit [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)verknüpft. **GetTickCount** und **GetTickCount64** geben die Anzahl der Millisekunden seit dem Start des Systems zurück.

</dd> <dt>

<span id="Should_I_use_QPC_or_call_the_RDTSC__RDTSCP_instructions_directly_"></span><span id="should_i_use_qpc_or_call_the_rdtsc__rdtscp_instructions_directly_"></span><span id="SHOULD_I_USE_QPC_OR_CALL_THE_RDTSC__RDTSCP_INSTRUCTIONS_DIRECTLY_"></span>**Sollte QPC verwendet oder die RDTSC-/rdtscp-Anweisungen direkt aufgerufen werden?**
</dt> <dd>

Um Unrichtigkeit und Portabilitäts Probleme zu vermeiden, empfehlen wir Ihnen dringend, [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) zu verwenden, anstatt das TSC-Register oder **RDTSC** -oder **rdtscp** -Prozessor Anweisungen zu verwenden.

</dd> <dt>

<span id="What_is_QPC_s_relation_to_an_external_time_epoch__Can_it_be_synchronized_to_an_________external_epoch_such_as_UTC_"></span><span id="what_is_qpc_s_relation_to_an_external_time_epoch__can_it_be_synchronized_to_an_________external_epoch_such_as_utc_"></span><span id="WHAT_IS_QPC_S_RELATION_TO_AN_EXTERNAL_TIME_EPOCH__CAN_IT_BE_SYNCHRONIZED_TO_AN_________EXTERNAL_EPOCH_SUCH_AS_UTC_"></span>**Was ist QPC in Bezug auf eine externe Zeitepoche? Kann die Synchronisierung mit einer externen Epoche wie UTC erfolgen?**
</dt> <dd>

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) basiert auf einem Hardware-Counter, der nicht mit einem externen Zeit Verweis (z. b. UTC) synchronisiert werden kann. Verwenden Sie für genaue Zeitstempel, die mit einem externen UTC-Verweis synchronisiert werden können, [**getsystemtimepreciseasfiletime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

</dd> <dt>

<span id="Is_QPC_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="is_qpc_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="IS_QPC_AFFECTED_BY_DAYLIGHT_SAVINGS_TIME__LEAP_SECONDS__TIME_ZONES__OR_SYSTEM_________TIME_CHANGES_MADE_BY_THE_ADMINISTRATOR_"></span>**Ist QPC von der Sommerzeit, von Schaltsekunden, Zeitzonen oder vom Administrator vorgenommenen Systemzeit Änderungen betroffen?**
</dt> <dd>

Nein. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) ist vollständig unabhängig von der Systemzeit und der UTC.

</dd> <dt>

<span id="Is_QPC_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_Turbo_Boost_technology_"></span><span id="is_qpc_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_turbo_boost_technology_"></span><span id="IS_QPC_ACCURACY_AFFECTED_BY_PROCESSOR_FREQUENCY_CHANGES_CAUSED_BY_POWER_________MANAGEMENT_OR_TURBO_BOOST_TECHNOLOGY_"></span>**Wirkt sich die QPC-Genauigkeit auf die von der Energie Verwaltung oder Turbo Boost-Technologie verursachten Änderungen der Prozessorfrequenz aus?**
</dt> <dd>

Nein. Wenn der Prozessor über eine invariante TSC verfügt, ist der [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) von diesen Änderungen nicht betroffen. Wenn der Prozessor nicht über eine invariante TSC verfügt, kehrt **QPC** auf einen Platt Form Hardware-Timer zurück, der nicht von den Änderungen an der Prozessorfrequenz oder der Turbo Boost-Technologie betroffen ist.

</dd> <dt>

<span id="Does_QPC_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="does_qpc_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="DOES_QPC_RELIABLY_WORK_ON_MULTI-PROCESSOR_SYSTEMS__MULTI-CORE_SYSTEM__AND_________SYSTEMS_WITH_HYPER-THREADING_"></span>**Funktioniert QPC zuverlässig mit Multiprozessorsystemen, Multikernsystem und Systemen mit Hyperthreading?**
</dt> <dd>

Ja

</dd> <dt>

<span id="How_do_I_determine_and_validate_that_QPC_works_on_my_machine_"></span><span id="how_do_i_determine_and_validate_that_qpc_works_on_my_machine_"></span><span id="HOW_DO_I_DETERMINE_AND_VALIDATE_THAT_QPC_WORKS_ON_MY_MACHINE_"></span>**Gewusst wie Sie ermitteln und überprüfen, ob QPC auf meinem Computer funktioniert?**
</dt> <dd>

Diese Überprüfungen müssen nicht durchgeführt werden.

</dd> <dt>

<span id="Which_processors_have_non-invariant_TSCs__How_can_I_check_if_my_system_has_a_________non-invariant_TSC_"></span><span id="which_processors_have_non-invariant_tscs__how_can_i_check_if_my_system_has_a_________non-invariant_tsc_"></span><span id="WHICH_PROCESSORS_HAVE_NON-INVARIANT_TSCS__HOW_CAN_I_CHECK_IF_MY_SYSTEM_HAS_A_________NON-INVARIANT_TSC_"></span>**Welche Prozessoren haben nicht invariante TSCs? Wie kann ich überprüfen, ob mein System einen nicht invarianten TSC hat?**
</dt> <dd>

Sie müssen diese Überprüfung nicht selbst durchführen. Windows-Betriebssysteme führen bei der Systeminitialisierung mehrere Überprüfungen durch, um zu bestimmen, ob der TSC als Grundlage für [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)geeignet ist. Zu Referenzzwecken können Sie jedoch ermitteln, ob Ihr Prozessor über eine invariante TSC verfügt, indem Sie eine der folgenden Funktionen verwenden:

-   Das Coreinfo.exe-Hilfsprogramm von Windows Sysinternals
-   Überprüfen der Werte, die von der CPUID-Anweisung bezüglich der TSC-Merkmale zurückgegeben werden
-   Dokumentation des Prozessor Herstellers

Im folgenden werden die von Windows Sysinternals Coreinfo.exe Utility ([www.sysInternals.com](https://www.sysinternals.com)) bereitgestellten TSC-invarianten Informationen angezeigt. Ein Sternchen bedeutet "true".

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

<span id="Does_QPC_work_reliably_on__hardware_platforms_"></span><span id="does_qpc_work_reliably_on__hardware_platforms_"></span><span id="DOES_QPC_WORK_RELIABLY_ON__HARDWARE_PLATFORMS_"></span>**Funktioniert QPC zuverlässig auf Windows RT-PC-Hardwareplattformen?**
</dt> <dd>

Ja

</dd> <dt>

<span id="How_often_does_QPC_roll_over_"></span><span id="how_often_does_qpc_roll_over_"></span><span id="HOW_OFTEN_DOES_QPC_ROLL_OVER_"></span>**Wie oft führt der QPC einen Rollover durch?**
</dt> <dd>

Nicht weniger als 100 Jahre ab dem aktuellen Systemstart und möglicherweise länger, basierend auf dem verwendeten Hardware-Timer. Bei den meisten Anwendungen ist das Rollover nicht von Bedeutung.

</dd> <dt>

<span id="What_is_the_computational_cost_of_calling_QPC_"></span><span id="what_is_the_computational_cost_of_calling_qpc_"></span><span id="WHAT_IS_THE_COMPUTATIONAL_COST_OF_CALLING_QPC_"></span>**Was sind die berechnungskosten für das Aufrufen von QPC?**
</dt> <dd>

Die berechnungskosten von [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) werden primär durch die zugrunde liegende Hardwareplattform bestimmt. Wenn das TSC-Register als Grundlage für QPC verwendet wird, werden die berechnungskosten primär dadurch bestimmt, wie lange der Prozessor die Verarbeitung einer **RDTSC** -Anweisung dauert. Diese Zeitspanne liegt zwischen 10E CPU-Zyklen und mehreren hundert CPU-Zyklen, je nach verwendetem Prozessor. Wenn der TSC nicht verwendet werden kann, wählt das System eine andere Hardware Zeit aus. Da sich diese Zeit Basen auf der Hauptplatine (z. b. auf der PCI-Süd-Bridge oder im PCH) befinden, sind die Kosten pro Aufruf der Gebühr höher als der TSC und liegen häufig in der Nähe von 0,8-1,0 Mikrosekunden, je nach Prozessorgeschwindigkeit und anderen Hardware Faktoren. Diese Kosten sind von der Zeit, die für den Zugriff auf das Hardware Gerät auf dem Motherboard erforderlich ist, geprägt.

</dd> <dt>

<span id="Does_QPC_require_a_kernel_transition__system_call__"></span><span id="does_qpc_require_a_kernel_transition__system_call__"></span><span id="DOES_QPC_REQUIRE_A_KERNEL_TRANSITION__SYSTEM_CALL__"></span>**Erfordert QPC einen Kernel Übergang (Systemaufrufe)?**
</dt> <dd>

Ein Kernel Übergang ist nicht erforderlich, wenn das-System das TSC-Register als Grundlage für [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)verwenden kann. Wenn das System eine andere Zeitbasis verwenden muss, z. b. den HPET oder den pm-Timer, ist ein Systemaufruf erforderlich.

</dd> <dt>

<span id="Is_the_performance_counter_monotonic__non-decreasing__"></span><span id="is_the_performance_counter_monotonic__non-decreasing__"></span><span id="IS_THE_PERFORMANCE_COUNTER_MONOTONIC__NON-DECREASING__"></span>**Ist der Leistungswert monoton (nicht absteigend)?**
</dt> <dd>

Ja

</dd> <dt>

<span id="Can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="CAN_THE_PERFORMANCE_COUNTER_BE_USED_TO_ORDER_EVENTS_IN_TIME_"></span>**Kann der Leistungs Bewert verwendet werden, um Ereignisse zeitlich zu sortieren?**
</dt> <dd>

Ja. Wenn Sie jedoch Leistungs Zähler Ergebnisse vergleichen, die aus unterschiedlichen Threads abgerufen werden, weisen Werte, die sich durch den Takt von ± 1 unterscheiden, eine mehrdeutige Reihenfolge auf, als hätten Sie einen identischen Zeitstempel.

</dd> <dt>

<span id="How_accurate_is_the_performance_counter_"></span><span id="how_accurate_is_the_performance_counter_"></span><span id="HOW_ACCURATE_IS_THE_PERFORMANCE_COUNTER_"></span>**Wie genau ist der Leistungswert?**
</dt> <dd>

Die Antwort hängt von einer Vielzahl von Faktoren ab. Weitere Informationen finden Sie unter [Eigenschaften von Hardware Uhren auf niedriger Ebene](#low-level-hardware-clock-characteristics).

</dd> </dl>

## <a name="faq-about-programming-with-qpc-and-tsc"></a>Häufig gestellte Fragen zum Programmieren mit QPC und TSC

Hier finden Sie Antworten auf häufig gestellte Fragen zum Programmieren mit [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) und TSCs.

<dl> <dt>

<span id="I_need_to_convert_the_QPC_output_to_milliseconds._How_can_I_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="i_need_to_convert_the_qpc_output_to_milliseconds._how_can_i_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="I_NEED_TO_CONVERT_THE_QPC_OUTPUT_TO_MILLISECONDS._HOW_CAN_I_AVOID_LOSS_OF_________PRECISION_WITH_CONVERTING_TO_DOUBLE_OR_FLOAT_"></span>**Ich muss die QPC-Ausgabe in Millisekunden konvertieren. Wie kann ich den Genauigkeits Verlust bei der Umstellung auf Double oder float vermeiden?**
</dt> <dd>

Beim Durchführen von Berechnungen für ganzzahlige Leistungsindikatoren sind einige Punkte zu beachten:

-   Die ganzzahlige Division verliert den Rest. Dies kann in einigen Fällen zu einem Genauigkeits Verlust führen.
-   Die Konvertierung zwischen 64-Bit-Ganzzahlen und Gleit Komma Zahlen (Double) kann zu einem Genauigkeits Verlust führen, da die Gleit Komma-Mantisse nicht alle möglichen integralen Werte darstellen kann.
-   Multiplikation von 64-Bit-Ganzzahlen kann zu einem ganzzahligen Überlauf führen.

Im Allgemeinen können diese Berechnungen und Konvertierungen so lange wie möglich verzögert werden, um die Zusammensetzung der aufgetretenen Fehler zu vermeiden.

</dd> <dt>

<span id="How_can_I_convert_QPC_to_100_nanosecond_ticks_so_I_can_add_it_to_a_________FILETIME_"></span><span id="how_can_i_convert_qpc_to_100_nanosecond_ticks_so_i_can_add_it_to_a_________filetime_"></span><span id="HOW_CAN_I_CONVERT_QPC_TO_100_NANOSECOND_TICKS_SO_I_CAN_ADD_IT_TO_A_________FILETIME_"></span>**Wie kann ich QPC in 100 Nanosekunden-Ticks konvertieren, damit ich Sie einem FILETIME-Wert hinzufügen kann?**
</dt> <dd>

Eine Dateizeit ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosekunden-Intervalle darstellt, die seit 12:00 Uhr vergangen sind. 1. Januar 1601 koordinierte Weltzeit (UTC). Datei Zeiten werden von Win32-API-Aufrufen verwendet, die eine Tageszeit zurückgeben, z. b. [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) und [**getsystemtimepreciseasfiletime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). Im Gegensatz dazu gibt [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Werte zurück, die die Uhrzeit in Einheiten von 1/(die Häufigkeit des Leistungs Zählers, der von [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)abgerufen wurde) darstellen. Bei der Konvertierung zwischen den beiden muss das Verhältnis zwischen dem **QPC** -Intervall und 100-Nanosekunden-Intervallen berechnet werden. Achten Sie darauf, die Genauigkeit zu vermeiden, da die Werte klein sein können (0,0000001/0,000000340).

</dd> <dt>

<span id="Why_is_the_time_stamp_that_is_returned_from_QPC_a_signed_integer_"></span><span id="why_is_the_time_stamp_that_is_returned_from_qpc_a_signed_integer_"></span><span id="WHY_IS_THE_TIME_STAMP_THAT_IS_RETURNED_FROM_QPC_A_SIGNED_INTEGER_"></span>**Warum ist der Zeitstempel, der von QPC zurückgegeben wird, eine ganze Zahl mit Vorzeichen?**
</dt> <dd>

Berechnungen, die [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) -Zeitstempel einschließen, können Subtraktion einschließen. Mithilfe eines signierten Werts können Sie Berechnungen verarbeiten, die möglicherweise negative Werte liefern.

</dd> <dt>

<span id="How_can_I_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="how_can_i_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="HOW_CAN_I_OBTAIN_HIGH_RESOLUTION_TIME_STAMPS_FROM_MANAGED_CODE_"></span>**Wie kann ich Zeitstempel mit hoher Auflösung aus verwaltetem Code abrufen?**
</dt> <dd>

Aufrufen der [**Stopwatch. getTimestamp**](/previous-versions/windows/) -Methode aus der [**System. Diagnostics. Stopwatch**](/previous-versions/windows/) -Klasse. Ein Beispiel für die Verwendung von **Stopwatch. getTimestamp** finden Sie unter Abrufen [von Zeitstempeln mit hoher Auflösung aus verwaltetem Code](#acquiring-high-resolution-time-stamps-from-managed-code).

</dd> <dt>

<span id="Under_what_circumstances_does_QueryPerformanceFrequency_return_FALSE__or_________QueryPerformanceCounter_return_zero_"></span><span id="under_what_circumstances_does_queryperformancefrequency_return_false__or_________queryperformancecounter_return_zero_"></span><span id="UNDER_WHAT_CIRCUMSTANCES_DOES_QUERYPERFORMANCEFREQUENCY_RETURN_FALSE__OR_________QUERYPERFORMANCECOUNTER_RETURN_ZERO_"></span>**Unter welchen Umständen gibt QueryPerformanceFrequency "false" zurück, oder QueryPerformanceCounter gibt "Null" zurück?**
</dt> <dd>

Dies tritt nicht auf einem System auf, auf dem Windows XP oder höher ausgeführt wird.

</dd> <dt>

<span id="Do_I_need_to_set_the_thread_affinity_to_a_single_core_to_use_QPC_"></span><span id="do_i_need_to_set_the_thread_affinity_to_a_single_core_to_use_qpc_"></span><span id="DO_I_NEED_TO_SET_THE_THREAD_AFFINITY_TO_A_SINGLE_CORE_TO_USE_QPC_"></span>**Muss ich die Thread Affinität auf einen einzelnen Kern festlegen, damit QPC verwendet werden kann?**
</dt> <dd>

Nein. Weitere Informationen finden Sie unter [Leitfaden zum Abrufen von Zeitstempeln](#guidance-for-acquiring-time-stamps). Dieses Szenario ist weder erforderlich noch erwünscht. Das Ausführen dieses Szenarios kann sich negativ auf die Leistung Ihrer Anwendung auswirken, indem die Verarbeitung auf einen Kern beschränkt wird, oder indem ein Engpass für einen einzelnen Kern entsteht, wenn mehrere Threads ihre Affinität beim Aufrufen von [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)auf denselben Kern festgelegt haben.

</dd> </dl>

## <a name="low-level-hardware-clock-characteristics"></a>Hardware Takt Merkmale auf niedriger Ebene

In diesen Abschnitten werden die Hardware Takt Merkmale auf niedriger Ebene dargestellt.

### <a name="absolute-clocks-and-difference-clocks"></a>Absolute Uhren und Differenz Uhren

Absolute Uhren bieten exakte Tages Messungen. Sie basieren in der Regel auf der koordinierten Weltzeit (UTC). Folglich hängt ihre Genauigkeit davon ab, wie gut Sie mit einem externen Zeit Verweis synchronisiert werden. Differenz Uhren Messen Zeitintervalle und basieren in der Regel nicht auf einer externen Zeitepoche. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) ist eine Differenz Uhr und wird nicht mit einer externen Zeitepoche oder einem anderen Verweis synchronisiert. Wenn Sie **QPC** für Zeitintervall Messungen verwenden, erhalten Sie in der Regel eine bessere Genauigkeit als bei der Verwendung von Zeitstempeln, die von einer absoluten Uhr abgeleitet werden. Dies liegt daran, dass die Synchronisierung der Zeit einer absoluten Uhr Phasen-und Häufigkeits Verschiebungen zur Erhöhung der Ungewissheit von kurzfristigen Zeitintervall Messungen verursachen kann.

### <a name="resolution-precision-accuracy-and-stability"></a>Auflösung, Genauigkeit, Genauigkeit und Stabilität

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) verwendet einen Hardware-Counter als Grundlage. Hardwartimer bestehen aus drei Teilen: einem Tick-Generator, einem Zähler, der die Ticks zählt, und einem Mittel zum Abrufen des Zähler Werts. Die Merkmale dieser drei Komponenten legen die Auflösung, Genauigkeit, Genauigkeit und Stabilität von **QPC** fest.

Wenn ein Hardware Generator Ticks mit konstanter Geschwindigkeit bereitstellt, können Zeitintervalle durch einfaches zählen dieser Ticks gemessen werden. Die Rate, mit der die Ticks generiert werden, wird als Häufigkeit bezeichnet und in Hertz (Hz) ausgedrückt. Die gegenseitige Häufigkeit wird als Zeitraum oder Takt Intervall bezeichnet und wird in einem entsprechenden internationalen System der Einheiten (SI) Time Unit (z. b. Second, millisecond, Mikro Second oder nanosecond) ausgedrückt.

![Zeitintervall](images/tick-interval.png)

Die Auflösung des Timers ist gleich dem Zeitraum. Die Auflösung bestimmt die Möglichkeit, zwischen zwei beliebigen Zeitstempeln zu unterscheiden, und legt eine untere Grenze für die kleinsten Zeitintervalle fest, die gemessen werden können. Dies wird manchmal als Takt Auflösung bezeichnet.

Die digitale Zeitmessung führt zu einer Messung der Ungewissheit von ± 1, da der digitale Zähler in separaten Schritten fortschreitet, während die Zeit kontinuierlich voranschreitet. Diese Ungewissheit wird als quantifisierungsfehler bezeichnet. Bei typischen Zeitintervall Messungen kann dieser Effekt häufig ignoriert werden, da der quantifizierungfehler wesentlich kleiner ist als das Zeitintervall, das gemessen wird.

![digitale Zeitmessung](images/digital-time-measure.png)

Wenn der gemessene Zeitraum jedoch klein ist und die Auflösung des Timers erreicht, müssen Sie diesen quantifisierungsfehler in Erwägung gezogen. Die Größe des eingeführten Fehlers liegt im Zeitraum von einer Uhr.

Die folgenden beiden Diagramme veranschaulichen die Auswirkung der Beeinträchtigung der Beeinträchtigung von ± 1 mithilfe eines Timers mit einer Auflösung von 1 Zeiteinheit.

![Tick-Ungewissheit](images/tick-uncertainty.png)

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) gibt die Häufigkeit von [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)zurück, und der Zeitraum und die Auflösung sind gleich der gegen übereinwirkung dieses Werts. Die Häufigkeit, mit der **QueryPerformanceFrequency** zurückgegeben wird, wird während der Systeminitialisierung bestimmt und ändert sich nicht, während das System ausgeführt wird.

> [!Note]  
> Möglicherweise gibt es Fälle, in denen [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) nicht die tatsächliche Häufigkeit des Hardware Tick-Generators zurückgibt. In vielen Fällen gibt **QueryPerformanceFrequency** z. b. die TSC-Häufigkeit dividiert durch 1024 zurück. und bei Hyper-V beträgt die Häufigkeit des Leistungs Zählers immer 10 MHz, wenn der virtuelle Gastcomputer unter einem [Hypervisor](https://msdn.microsoft.com/library/Ff542584(v=VS.85).aspx) ausgeführt wird, der die [Schnittstelle der Hypervisor-Version 1,0](https://msdn.microsoft.com/library/Ff541458(v=VS.85).aspx)implementiert. Nehmen Sie daher nicht an, dass **QueryPerformanceFrequency** die genaue TSC-Häufigkeit zurückgibt.

 

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) liest den Leistungswert und gibt die Gesamtanzahl der Ticks zurück, die seit dem Start des Windows-Betriebssystems aufgetreten sind, einschließlich der Zeit, zu der sich der Computer im Standbymodus befand, z. b. Standby, Ruhezustand oder verbundener Standbymodus.

In diesen Beispielen wird gezeigt, wie Sie das Takt Intervall und die Auflösung berechnen und die Takt Anzahl in einen Uhrzeitwert konvertieren.

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Beispiel 1**
</dt> <dd>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) gibt den Wert 3.125.000 auf einem bestimmten Computer zurück. Was ist das Takt Intervall und die Auflösung von [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) -Messungen auf diesem Computer? Das Takt Intervall bzw. der Zeitraum ist die gegenseitige 3.125.000, d. h. 0,000000320 (320 nanoseconds). Daher stellt jedes Tick die Übergabe von 320 Nanosekunden dar. Zeiträume, die kleiner als 320 Nanosekunden sind, können auf diesem Computer nicht gemessen werden.

Takt Intervall = 1/(Leistungs Häufigkeit)

Tick-Intervall = 1/3125000 = 320 NS

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Beispiel 2**
</dt> <dd>

Auf demselben Computer wie im vorherigen Beispiel ist der Unterschied zwischen den Werten, die von zwei aufeinander folgenden Aufrufen an [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) zurückgegeben werden, 5. Wie viel Zeit ist zwischen den beiden Aufrufen vergangen? 5 Ticks multipliziert mit 320 Nanosekunden ergeben 1,6 Mikrosekunden.

Verstrichen Zeit = Ticks Takt \* Intervall

Abgelaufenen Zeit = 5 \* 320 NS = 1,6.

</dd> </dl>

Der Zugriff (Lesevorgang) auf den Tick-Zähler der Software dauert eine Weile, und diese Zugriffszeit kann die Genauigkeit der Zeitmessung verringern. Dies liegt daran, dass die minimale Intervallzeit (das kleinste Zeitintervall, das gemessen werden kann) die größere Auflösung und die Zugriffszeit ist.

Precision = Max \[ Resolution, ACCESSTIME\]

Stellen Sie sich beispielsweise einen hypothetischen Hardware Timer mit einer 100 Nanosekunden-Auflösung und einer 800 Nanosekunden-Zugriffszeit vor. Dies kann der Fall sein, wenn der Platt formtimer anstelle des TSC-Registers als Basis von [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)verwendet wurde. Folglich ist die Genauigkeit 800 Nanosekunden nicht 100 Nanosekunden, wie in dieser Berechnung gezeigt.

Genauigkeit = max. \[ 800 NS, 100 NS \] = 800 NS

Diese beiden Abbildungen stellen diesen Effekt dar.

![QPC-Zugriffszeit](images/qpc-access-time.png)

Wenn die Zugriffszeit größer als die Auflösung ist, versuchen Sie nicht, die Genauigkeit zu verbessern, indem Sie erraten. Anders ausgedrückt: Es ist ein Fehler, wenn Sie davon ausgehen, dass der Zeitstempel genau in der Mitte oder am Anfang oder Ende des Aufrufes verwendet wird.

Im Gegensatz dazu sollten Sie das folgende Beispiel beachten, bei dem die [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) -Zugriffszeit nur 20 Nanosekunden und die hardwaretaktsauflösung 100 Nanosekunden beträgt. Dies kann der Fall sein, wenn das TSC-Register als Grundlage für **QPC** verwendet wurde. Hier ist die Genauigkeit durch die Takt Auflösung beschränkt.

![QPC-Genauigkeit](images/qpc-precision.png)

In der Praxis können Sie Zeitquellen suchen, für die die zum Lesen des Zählers benötigte Zeit größer oder kleiner als die Auflösung ist. In beiden Fällen ist die Genauigkeit die größere der beiden.

Diese Tabelle enthält Informationen über die ungefähre Auflösung, die Zugriffszeit und die Genauigkeit einer Vielzahl von Uhren. Beachten Sie, dass einige der Werte sich von den verschiedenen Prozessoren, Hardwareplattformen und Prozessor Geschwindigkeiten unterscheiden.



| Uhrquelle                                                      | Nominale Taktfrequenz | Takt Auflösung    | Zugriffszeit (typisch) | Genauigkeit       |
|-------------------------------------------------------------------|-------------------------|---------------------|-----------------------|-----------------|
| PC-RTC                                                            | 64 Hz                   | 15,625 Millisekunden | –                   | –             |
| Abfragen des Leistungs Zählers mithilfe von TSC mit einer Prozessorzeit von 3 GHz  | 3 MHz                   | 333 Nanosekunden     | 30 Nanosekunden        | 333 Nanosekunden |
| **RDTSC** -Machine-Anweisung auf einem System mit einer Dauer von 3 GHz | 3 GHz                   | 333 picoseconds     | 30 Nanosekunden        | 30 Nanosekunden  |



 

Da [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) einen Hardware Zähler verwendet, können Sie, wenn Sie einige grundlegende Merkmale von Hardware Indikatoren verstehen, sich über die Funktionen und Einschränkungen von **QPC** informieren.

Der am häufigsten verwendete Hardware Taktgenerator ist ein Crystal-Oszillator. Der Crystal ist ein kleines Stück von Quarz oder anderem Keramikmaterial, das Piezoelectric-Merkmale aufzeigt, die einen preisgünstigen Frequenz Verweis mit hervorragender Stabilität und Genauigkeit bieten. Diese Häufigkeit wird verwendet, um die Ticks zu generieren, die von der Uhr gezählt werden.

Die Genauigkeit eines Timers bezieht sich auf den Grad der Konformität auf einen true-oder Standard-Wert. Dies hängt in erster Linie davon ab, ob die Möglichkeit besteht, Ticks mit der angegebenen Häufigkeit bereitzustellen. Wenn die Häufigkeit der osziierung zu hoch ist, wird die Uhr schnell ausgeführt, und gemessene Intervalle werden länger angezeigt, als Sie tatsächlich sind. Wenn die Häufigkeit zu niedrig ist, wird die Uhr langsam ausgeführt, und gemessene Intervalle werden kürzer angezeigt als Sie tatsächlich sind.

Für typische Zeitintervall Messungen für kurze Dauer (z. b. Antwortzeit Messungen, Messungen der Netzwerk Latenz usw.) ist die Genauigkeit des Hardware Oszillators in der Regel ausreichend. Bei manchen Messungen ist die Genauigkeit der Oszillatorfrequenz jedoch wichtig, insbesondere für lange Zeitintervalle oder wenn Sie Messungen vergleichen möchten, die auf verschiedenen Computern durchgeführt werden. Im restlichen Teil dieses Abschnitts werden die Auswirkungen der oszillatorgenauigkeit untersucht.

Die Häufigkeit der Kristalle der Kristalle wird während des Herstellungsprozesses festgelegt und vom Hersteller in Bezug auf eine angegebene Frequenz zuzüglich oder abzüglich einer Fertigungstoleranz in "parts per Million" (ppm) angegeben, die als maximaler Häufigkeits Offset bezeichnet wird. Ein Glas mit einer angegebenen Häufigkeit von 1 Million Hz und ein maximaler Frequenz Offset von ± 10 ppm liegen innerhalb von Spezifikations Limits, wenn die tatsächliche Häufigkeit zwischen 999.990 Hz und 1.000.010 Hz liegt.

Wenn Sie die Ausdrucks Teile pro Million durch die Mikrosekunden pro Sekunde ersetzen, können wir diesen Frequency Offset-Fehler auf Zeitintervall Messungen anwenden. Ein Oszillator mit dem Offset + 10 ppm würde einen Fehler von 10 Mikrosekunden pro Sekunde aufweisen. Wenn ein 1-Sekunden-Intervall gemessen wird, wird es daher schnell ausgeführt, und es wird ein 1-Sekunden-Intervall als 0,999990 Sekunden gemessen.

Eine bequeme Referenz ist, dass ein Häufigkeits Fehler von 100 ppm einen Fehler von 8,64 Sekunden nach 24 Stunden verursacht. In dieser Tabelle wird die Messunsicherheit aufgrund des gesammelten Fehlers für längere Zeitintervalle dargestellt.



| Dauer des Zeitintervalls | Maß an Ungewissheit aufgrund eines akkumulierten Fehlers mit +/-10 ppm-Frequenztoleranz |
|------------------------|--------------------------------------------------------------------------------------|
| 1 Mikrosekunde          | ± 10 picoseconds (10-12)                                                             |
| 1 Millisekunde          | ± 10 Nanosekunden (10-9)                                                              |
| 1 Sekunde               | ± 10 Mikrosekunden                                                                    |
| 1 Stunde                 | ± 60 Mikrosekunden                                                                    |
| 1 Tag                  | ± 0,86 Sekunden                                                                       |
| 1 Woche                 | ± 6,08 Sekunden                                                                       |



 

Die obige Tabelle zeigt, dass der Häufigkeits Offset Fehler in kurzen Zeitintervallen häufig ignoriert werden kann. Bei langen Zeitintervallen kann auch ein kleiner Häufigkeits Offset zu einer erheblichen gewissen Maß an Ungewissheit führen.

Bei den in PCs und Servern verwendeten Crystal-Oszillatoren wird in der Regel eine Frequenztoleranz von ± 30 bis 50 Teilen pro Million hergestellt, und in seltenen Fällen können Kristalle um bis zu 500 ppm ausgeschaltet werden. Obwohl Kristalle mit erheblich engeren Frequenz Offset-Toleranzen verfügbar sind, sind Sie teurer und werden daher auf den meisten Computern nicht verwendet.

Um die negativen Auswirkungen dieses Fehlers bei der Frequenz Abweichung zu reduzieren, verwenden neuere Versionen von Windows, insbesondere Windows 8, mehrere Hardwaretimer, um den Frequenz Offset zu erkennen und diesen so weit wie möglich auszugleichen. Dieser Kalibrierungsvorgang wird ausgeführt, wenn Windows gestartet wird.

Wie in den folgenden Beispielen gezeigt, wirkt sich der Häufigkeits Offset Fehler einer Hardwareuhr auf die erreichbare Genauigkeit aus, und die Auflösung der Uhr kann weniger wichtig sein.

![Häufigkeits Offset-Fehler beeinflussen erreichbare Genauigkeit](images/freq-offset-error.png)

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Beispiel 1**
</dt> <dd>

Angenommen, Sie führen Zeitintervall Messungen mithilfe eines 1-MHz-Oszillators aus, der eine Auflösung von 1 Mikrosekunden und einem maximalen Frequency-Offset-Fehler von ± 50 ppm aufweist. Nehmen wir nun an, dass der Offset genau + 50 ppm ist. Dies bedeutet, dass die tatsächliche Häufigkeit 1.000.050 Hz betragen würde. Wenn wir ein Zeitintervall von 24 Stunden gemessen haben, ist unser Maß 4,3 Sekunden zu kurz (23:59:55.700000 gemessen im Vergleich zu 24:00:00.000000 actual).

Sekunden an einem Tag = 86400

Fehler bei Frequenz Offset = 50 ppm = 0,00005

86.400 Sekunden \* 0,00005 = 4,3 Sekunden

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Beispiel 2**
</dt> <dd>

Angenommen, die TSC-Zeit des Prozessors wird von einem Crystal-Oszillator gesteuert und hat eine Frequenz von 3 GHz festgelegt. Dies bedeutet, dass die Auflösung 1/3000000000 oder ungefähr 333 picoseconds betragen würde. Angenommen, der zum Steuern der Prozessoruhr verwendete Crystal hat eine Frequenztoleranz von ± 50 ppm und ist tatsächlich + 50 ppm. Trotz der beeindruckenden Auflösung ist eine Zeitintervall Messung von 24 Stunden nach wie vor 4,3 Sekunden zu kurz. (23:59:55.7000000000 gemessen im Vergleich zu 24:00:00.0000000000 actual).

Sekunden an einem Tag = 86400

Fehler bei Frequenz Offset = 50 ppm = 0,00005

86.400 Sekunden \* 0,00005 = 4,3 Sekunden

Dies zeigt, dass eine hochauflösende TSC-Uhr nicht notwendigerweise genauere Messungen als eine niedrigere Auflösungszeit bereitstellt.

</dd> <dt>

<span id="Example_3"></span><span id="example_3"></span><span id="EXAMPLE_3"></span>**Beispiel 3**
</dt> <dd>

Sie können zwei verschiedene Computer verwenden, um das gleiche 24-Stunden-Zeitintervall zu messen. Beide Computer verfügen über einen Oszillator mit einem maximalen Frequenz Offset von ± 50 ppm. Wie weit ist die Messung des gleichen Zeitintervalls für diese beiden Systeme gleich? Wie in den vorherigen Beispielen ergibt ± 50 ppm einen maximalen Fehler von ± 4,3 Sekunden nach 24 Stunden. Wenn ein System schnell 4,3 Sekunden und die anderen 4,3 Sekunden langsam ausgeführt werden, kann der maximale Fehler nach 24 Stunden 8,6 Sekunden betragen.

Sekunden an einem Tag = 86400

Frequency Offset Error = ± 50 ppm = ± 0,00005

± (86.400 Sekunden \* 0,00005) = ± 4,3 Sekunden

Maximaler Offset zwischen den beiden Systemen = 8,6 Sekunden

Zusammenfassend wird der Fehler bei der Frequenz Abweichung immer wichtiger, wenn lange Zeitintervalle gemessen werden und Messungen zwischen verschiedenen Systemen verglichen werden.

Die Stabilität eines Timers beschreibt, ob sich die Taktfrequenz im Laufe der Zeit ändert, z. b. aufgrund von Temperaturänderungen. Als Takt Generatoren auf Computern verwendete Quarzkristalle zeigen kleine Änderungen in der Häufigkeit als Temperatur Funktion an. Der von der thermischen Abweichung verursachte Fehler ist in der Regel gering, verglichen mit dem Fehler "Frequency Offset" für allgemeine Temperaturbereiche. Entwickler von Software für tragbare Geräte oder Geräte, die große Temperaturschwankungen unterliegen, müssen diesen Effekt jedoch möglicherweise in Erwägung ziehen.

</dd> </dl>

## <a name="hardware-timer-info"></a>Informationen zum Hardware-Timer

<dl> <dt>

<span id="TSC_Register"></span><span id="tsc_register"></span><span id="TSC_REGISTER"></span>**TSC-Register**
</dt> <dd>

Einige Intel-und AMD-Prozessoren enthalten ein TSC-Register, bei dem es sich um ein 64-Bit-Register handelt, das sich zu einem hohen Preis erhöht, in der Regel gleich der Prozessor Der Wert dieses Leistungs Zählers kann durch die Anweisungen **RDTSC** oder **rdtscp** Machine gelesen werden. er bietet eine sehr geringe Zugriffszeit und berechnungskosten in der Reihenfolge von Dutzenden oder Hunderten von Computer Zyklen, je nach Prozessor.

Obwohl es sich bei dem TSC-Register um einen idealen Zeitstempel Mechanismus handelt, gibt es hier Situationen, in denen er nicht zuverlässig für die Zeit Aufbewahrung funktionieren kann:

-   Nicht alle Prozessoren verfügen über TSC-Register, sodass das TSC-Register in Software direkt ein Portabilitäts Problem verursacht. (In diesem Fall wählt Windows eine Alternative Zeit Quelle für [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) aus, wodurch das Portabilitäts Problem vermieden wird.)
-   Einige Prozessoren können die Häufigkeit der TSC-Uhr variieren oder die Weiterentwicklung des TSC-Registers verhindern, sodass der TSC für die zeitliche Steuerung auf diesen Prozessoren ungeeignet ist. Diese Prozessoren werden als nicht invariante TSC-Register bezeichnet. (Dies wird von Windows automatisch erkannt, und Sie wählen eine Alternative Zeit Quelle für [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)aus.)
-   Auf Systemen mit mehreren Prozessoren oder mehreren Kernen können einige Prozessoren und Systeme die Uhren der einzelnen Kerne nicht mit demselben Wert synchronisieren. (Dies wird von Windows automatisch erkannt, und Sie wählen eine Alternative Zeit Quelle für [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)aus.)
-   Bei einigen großen Multiprozessorsystemen können Sie die Prozessor Uhren möglicherweise nicht mit demselben Wert synchronisieren, auch wenn der Prozessor über einen invarianten TSC verfügt. (Dies wird von Windows automatisch erkannt, und Sie wählen eine Alternative Zeit Quelle für [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)aus.)
-   Einige Prozessoren führen Anweisungen außerhalb der Reihenfolge aus. Dies kann zu einer falschen Anzahl von Zyklen führen, wenn **RDTSC** zum Zeitpunkt der Anweisungs Sequenzen verwendet wird, da die **RDTSC** -Anweisung möglicherweise zu einem anderen Zeitpunkt ausgeführt wird, als im Programm angegeben ist. Die **rdtscp** -Anweisung wurde auf einigen Prozessoren als Reaktion auf dieses Problem eingeführt.

Wie bei anderen Timern basiert der TSC auf einem Crystal-Oszillator, dessen Häufigkeit im Voraus nicht bekannt ist und für den ein Frequency-Offset-Fehler vorliegt. Daher muss Sie, bevor Sie verwendet werden kann, mithilfe eines anderen Zeit Steuerungs Verweises kalibriert werden.

Während der Systeminitialisierung überprüft Windows, ob der TSC zu Zeit Steuerungs Zwecken geeignet ist, und führt die erforderliche Häufigkeits-und Kern Synchronisierung durch.

</dd> <dt>

<span id="PM_Clock"></span><span id="pm_clock"></span><span id="PM_CLOCK"></span>**PM-Uhr**
</dt> <dd>

Der ACPI-Timer, auch als PM-Uhr bezeichnet, wurde der Systemarchitektur hinzugefügt, um zuverlässige Zeitstempel unabhängig von der Geschwindigkeit der Prozessoren bereitzustellen. Da dies das einzige Ziel dieses Timers war, stellt es einen Zeitstempel in einem einzelnen Takt Intervall bereit, bietet aber keine andere Funktionalität.

</dd> <dt>

<span id="HPET_Timer"></span><span id="hpet_timer"></span><span id="HPET_TIMER"></span>**HPET-Timer**
</dt> <dd>

Der Ereignis Timer mit hoher Genauigkeit (HPET) wurde von Intel und Microsoft zusammen entwickelt, um die zeitlichen Anforderungen von Multimedia-und anderen zeitsensiblen Anwendungen zu erfüllen. HPET-Unterstützung ist seit Windows Vista in Windows und Windows 7-und Windows 8-Hardware Logo Zertifizierung erfordert HPET-Unterstützung in der Hardwareplattform.

</dd> </dl>

 

 
