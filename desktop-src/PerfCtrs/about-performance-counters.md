---
description: Leistungsindikatoren werden verwendet, um Informationen zur Leistung des Betriebssystems oder einer Anwendung, eines Diensts oder Treibers zu liefern.
ms.assetid: d172a131-61d3-4fc1-8e0c-b07b2bd34f80
title: Informationen zu Leistungsindikatoren
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8a80ac907ef842e4564f0e67daa173fee165bc93d8fa568920df8ffc24b8c9a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978914"
---
# <a name="about-performance-counters"></a>Informationen zu Leistungsindikatoren

Windows Leistungsindikatoren bieten eine abstraktionsschicht auf hoher Ebene mit einer konsistenten Schnittstelle zum Sammeln verschiedener Arten von Systemdaten wie CPU-, Arbeitsspeicher- und Datenträgernutzungsstatistiken. Systemadministratoren verwenden Leistungsindikatoren, um Leistungs- oder Verhaltensprobleme zu überwachen. Softwareentwickler verwenden Leistungsindikatoren, um die Ressourcennutzung ihrer Komponenten zu überprüfen.

> [!IMPORTANT]
> Windows Leistungsindikatoren sind für die Ermittlung und Sammlung administrativer/diagnoser Daten optimiert. Sie sind nicht für die Sammlung von Daten mit hoher Häufigkeit oder für die Profilerstellung von Anwendungen geeignet, da sie nicht so konzipiert sind, dass sie mehr als einmal pro Sekunde gesammelt werden. Für den Zugriff auf Systeminformationen mit geringerem Mehraufwand bevorzugen Sie möglicherweise direktere APIs wie Process [**Status Helper,**](../psapi/process-status-helper.md) [**GlobalMemoryStatusEx,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)oder [**GetProcessTimes.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes) Für die Profilerstellung können Sie ETW-Protokolle mit [**Systemprofilerstellungsdaten**](/windows-hardware/drivers/devtest/tracelog) sammeln, indem Sietracelog.exe-, -, - oder -Optionen verwenden, oder Sie können `-critsec` `-dpcisr` die `-eflag` `-ProfileSource` [**Hardwareindikatorprofilerstellung verwenden.**](/previous-versions/windows/desktop/hcp/hcp-reference)

> [!NOTE]
> Verwechseln Sie Windows Leistungsindikatoren nicht mit der [**QueryPerformanceCounter-API.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Windows Leistungsindikatoren bieten eine abstraktion auf hoher Ebene für viele Arten von Systeminformationen. Die QueryPerformanceCounter-Funktion bietet optimierten Zugriff auf einen Zeitstempel mit hoher Genauigkeit.

## <a name="getting-started"></a>Erste Schritte

- Verwenden [Sie Leistungsindikatortools,](performance-counters-tools.md) wenn Sie die Leistungsdaten eines Systems sammeln oder anzeigen möchten.
- Verwenden [Sie Leistungsindikatorsammlungs-APIs,](consuming-counter-data.md) wenn Sie ein Skript oder ein Programm schreiben möchten, das Leistungsdaten aus dem lokalen System sammelt.
- Verwenden [Sie WMI-Leistungsindikatorklassen,](/windows/desktop/WmiSdk/monitoring-performance-data) wenn Sie Leistungsdaten von einem lokalen oder Remotesystem mithilfe von WMI sammeln möchten.
- Verwenden [Sie Leistungsindikatoranbieter-APIs,](providing-counter-data.md) wenn Sie Leistungsdaten aus Ihrer Softwarekomponente veröffentlichen möchten.

## <a name="concepts"></a>Konzepte

Das Windows System des **Leistungsindikators** ist in **Verbraucher,** **Anbieter,** **Countersets,** Leistungsindikatoren, Instanzen und **Leistungsindikatorwerte organisiert.** 

Ein **Consumer** ist eine Softwarekomponente, die Leistungsdaten nutzt. Windows enthält mehrere [integrierte Tools,](performance-counters-tools.md) die Leistungsdaten nutzen. Dazu gehören Task-Manager, Ressourcenmonitor, Leistungsmonitor, typeperf.exe, logman.exe und relog.exe. Entwickler können Skripts und Anwendungen schreiben, die über Leistungsindikator-APIs auf [Leistungsindikatoren zugreifen.](consuming-counter-data.md)

Ein **Anbieter ist** eine Softwarekomponente, die [Leistungsdaten generiert und veröffentlicht.](providing-counter-data.md) Ein Anbieter veröffentlicht Daten für einen oder *mehrere Countersets.* Ein Datenbanksystem kann sich beispielsweise selbst als Leistungsdatenanbieter registrieren.

- Ein **V1-Anbieter** ist eine Softwarekomponente, die Leistungsdaten über eine [Leistungs-DLL veröffentlicht,](providing-counter-data-using-a-performance-dll.md) die im Prozess des Consumers ausgeführt wird. Ein V1-Anbieter wird über eine Datei auf einem System `.ini` installiert. Die Architektur des V1-Anbieters ist veraltet. Neue Anbieter sollten die V2-Anbieterarchitektur verwenden.
- Ein **V2-Anbieter** ist eine Softwarekomponente, die Leistungsdaten über die [Leistungsindikatoranbieter-APIs veröffentlicht.](providing-counter-data-using-version-2-0.md) Ein V2-Anbieter wird über eine `.man` (XML-Manifest)-Datei auf einem System installiert.

Ein **Counterset** ist eine Gruppierung von Leistungsdaten innerhalb eines Anbieters. Ein Counterset verfügt über einen Namen und einen oder *mehrere Leistungsindikatoren.* Das Sammeln der Daten aus einem Counterset gibt eine Reihe von *-Instanzen zurück.* In einigen Windows-APIs werden Leistungsindikatoren als **Leistungsobjekte bezeichnet.** Beispielsweise kann ein Leistungsdatenanbieter für ein Datenbanksystem einen Indikatorsatz für datenbankspezifische Statistiken bereitstellen.

Ein **Leistungsindikator** ist die Definition einzelner Leistungsdaten. Ein Indikator verfügt über einen Namen und einen Typ. Beispielsweise kann ein Indikatorsatz für "Statistiken pro Datenbank" einen Zähler namens "Transaktionen pro Sekunde" mit dem Typ `PERF_COUNTER_COUNTER` enthalten.

Eine **Instanz ist** eine Entität, über die Leistungsdaten gemeldet werden. Eine -Instanz verfügt über einen Namen (Zeichenfolge) und mindestens einen *Indikatorwert.* Ein Indikatorsatz für "Statistiken pro Datenbank" kann z. B. eine Instanz pro Datenbank enthalten. Der Instanzname wäre der Datenbankname, und jede Instanz würde Leistungsindikatorwerte für die Leistungsindikatoren "Transaktionen pro Sekunde", "Speicherauslastung" und "Datenträgerauslastung" enthalten.

Ein **Leistungsindikatorwert** ist der Wert eines einzelnen Leistungsindikatordaten. Ein Indikatorwert ist eine ganze Zahl ohne Vorzeichen, je nach Typ des entsprechenden Leistungsindikators entweder 32-Bit oder 64 Bit. Wenn von einer -Instanz *gesprochen wird,* kann *ein Zählerwert* manchmal als Zähler *oder* als Wert *bezeichnet werden.*

> [!TIP]
> Es kann hilfreich sein, Leistungsindikatorbegriffe mit vertrauteren Tabellenbegriffen in Beziehung zu stehen. Ein **Counterset** ist wie eine Tabelle. Ein **Zähler** ist wie eine Spalte. Eine **-Instanz** ist wie eine Zeile. Ein **Indikatorwert** ist wie eine Zelle in der Tabelle.

**Einzelinstanz-Countersets** enthalten immer Daten für genau eine Instanz. Dies ist häufig bei Countersets der Fall, die system globale Statistiken melden. Beispielsweise verfügt Windows über einen integrierten Indikatorsatz mit einer einzelnen Instanz namens "Memory", der über die globale Speicherauslastung berichtet.

**Countersets mit mehreren Instanzen enthalten** Daten für eine variable Anzahl von Instanzen. Dies ist häufig bei Countersets der Fall, die über Entitäten innerhalb des Systems berichten. Beispielsweise verfügt Windows über einen integrierten Indikatorsatz mit mehreren Instanzen namens "Prozessorinformationen", der eine Instanz für jede installierte CPU meldet.

Verbraucher sammeln und zeichnen die Daten in regelmäßigen Abständen aus dem Counterset eines Anbieters auf. Beispielsweise kann der Consumer Daten einmal pro Sekunde oder einmal pro Minute sammeln. Die gesammelten Daten werden als Beispiel **bezeichnet.** Ein Beispiel besteht aus Zeitstempeln zusammen mit den Daten für Instanzen des Countersets. Die Daten für jede Instanz enthalten den Instanznamen (Zeichenfolge) und einen Satz von Indikatorwerten (ganze Zahlen, einen Wert für jeden Indikator im Counterset).

Instanznamen sollten normalerweise innerhalb eines Beispiels eindeutig sein, d. h., ein Anbieter sollte nicht zwei Instanzen mit demselben Namen als Teil eines einzelnen Beispiels zurückgeben. Einige ältere Anbieter befolgen diese Regel nicht, daher müssen Verbraucher in der Lage sein, nicht [eindeutige Instanznamen zu tolerieren.](handling-duplicate-instance-names.md) Bei Instanznamen wird die Schreibung nicht beachtet, sodass Instanzen keine Namen haben sollten, die sich nur in der Kleinschreibung unterscheiden.

> [!NOTE]
> Aus Gründen der Abwärtskompatibilität gibt das Counterset "Process" nicht eindeutige Instanznamen basierend auf dem EXE-Dateinamen zurück. Dies kann zu verwirrenden Ergebnissen führen, insbesondere wenn ein Prozess mit einem nicht eindeutigen Namen gestartet oder heruntergefahren wird, da dies in der Regel zu Datenverwechslungen aufgrund eines falschen Abgleichs von Instanznamen zwischen Stichproben führt. Die Verbraucher des "Process"-Countersets müssen in der Lage sein, diese nicht eindeutigen Instanznamen und die daraus resultierenden Datenschiebe zu tolerieren.

Instanznamen müssen stichprobenübergreifend stabil sein, d. h., ein Anbieter sollte bei jeder Zählermenge denselben Instanznamen für dieselbe Entität verwenden.

Jeder Indikator verfügt über einen Typ. Der Indikatortyp gibt den Typ des Rohwerts des Indikators **an** (32-Bit-Ganzzahl ohne Vorzeichen oder 64-Bit-Ganzzahl ohne Vorzeichen). Der Indikatortyp gibt auch an, was der Rohwert des Indikators darstellt, der bestimmt, wie der Rohwert verarbeitet werden soll, um nützliche Statistiken zu generieren.

Während einige Indikatortypen einfach sind und einen Rohwert haben, [](calculating-counter-values.md) der direkt nützlich ist, erfordern viele Indikatortypen zusätzliche Verarbeitung, um einen nützlichen **formatierten Wert zu erstellen.** Um den formatierten Wert zu erzeugen, erfordern einige Indikatortypen Rohwerte aus zwei Stichproben, einige Indikatortypen erfordern Zeitstempel, und einige Indikatortypen erfordern Rohwerte von mehreren Leistungsindikatoren. Beispiel:

- `PERF_COUNTER_LARGE_RAWCOUNT` ist ein 64-Bit-Rohwert, der keine Verarbeitung erfordert, um nützlich zu sein. Sie ist für Zeitpunktwerte geeignet, z. B. "Verwendete Bytes arbeitsspeicher".
- `PERF_COUNTER_RAWCOUNT_HEX` ist ein 32-Bit-Rohwert, der nur einfache hexadezimale Formatierung erfordert, um nützlich zu sein. Sie ist für Zeitpunkte oder zur Identifizierung von Informationen wie "Flags" oder "Basisadresse" geeignet.
- `PERF_COUNTER_BULK_COUNT` ist ein 64-Bit-Rohwert, der die Anzahl der Ereignisse angibt und verwendet wird, um die Rate zu berechnen, mit der die Ereignisse auftreten. Um nützlich zu sein, erfordert dieser Indikatortyp zwei Stichproben, die zeitgetrennt sind. Der formatierte Wert ist die Ereignisrate, d. h., wie oft das Ereignis pro Sekunde im Intervall zwischen den beiden Stichproben aufgetreten ist. Bei zwei Stichproben `s0` und `s1` wird der formatierte Wert (Ereignisrate) als `(s1.EventCount - s0.EventCount)/(s1.TimestampInSeconds - s0.TimestampInSeconds)` berechnet.

Von Anbietern wird erwartet, dass sie sich wie zustandslos verhalten, d. h., das Sammeln von Daten aus einem Counterset sollte sich nicht sichtbar auf den Zustand des Anbieters auswirken. Beispielsweise sollte ein Anbieter die Indikatorwerte nicht auf 0 zurücksetzen, wenn ein Counterset erfasst wird, und er sollte nicht den Zeitstempel einer vorherigen Auflistung verwenden, um die Werte in der aktuellen Auflistung anzupassen. Stattdessen sollten einfache rohe Indikatorwerte mit genauen Typen angegeben werden, damit der Consumer nützliche Statistiken basierend auf den Rohwerten und ihren Zeitstempeln berechnen kann.

## <a name="performance-api-architecture"></a>Architektur der Leistungs-API

![Leistungsindikatoranwendungen rufen Windows APIs auf, die Anbieter aufrufen, um Leistungsdaten zu erhalten.](images/architecture.png)

Leistungsindikatorverbraucher umfassen Folgendes:

- [Von Microsoft bereitgestellte](performance-counters-tools.md) Anwendungen wie Task-Manager, Ressourcenmonitor, Leistungsmonitor und typeperf.exe.
- Von Microsoft bereitgestellte api-Oberflächen auf hoher Ebene, die Leistungsindikatordaten wie [WMI-Leistungsklassen verfügbar machen.](/windows/desktop/WmiSdk/monitoring-performance-data)
- Ihre eigenen Anwendungen oder Skripts, die [Leistungsindikator-Consumer-APIs verwenden.](consuming-counter-data.md)

Die meisten Leistungsindikatorverbraucher verwenden APIs aus [PDH.dll, ](using-the-pdh-functions-to-consume-counter-data.md) um Leistungsdaten zu sammeln. PDH verwaltet viele komplexe Aspekte der Erfassung von Leistungsindikatoren, z. B. das Analyse von Abfragen, das Abgleichen von Instanzen über mehrere Stichproben hinweg und das Berechnen von formatierten Werten aus den rohen Indikatordaten. Die PDH-Implementierung verwendet die Registrierungs-APIs, wenn Daten von einem V1-Anbieter verwendet werden, und die V2-Consumer-APIs, wenn Daten von einem V2-Anbieter verwendet werden.

Einige ältere Leistungsindikatorverbraucher verwenden die [Registrierungs-APIs,](using-the-registry-functions-to-consume-counter-data.md) um Leistungsdaten aus dem speziellen `HKEY_PERFORMANCE_DATA` Registrierungsschlüssel zu sammeln. Dies wird für neuen Code nicht empfohlen, da die Verarbeitung der Daten aus der Registrierung komplex und fehleranfällig ist. Die Implementierung der Registrierungs-API unterstützt das Sammeln von Daten von V1-Anbietern direkt. Sie unterstützt indirekt das Sammeln von Daten von V2-Anbietern über eine Übersetzungsebene, die die V2-Consumer-APIs verwendet.

Einige Leistungsindikator-Consumer verwenden die [PerfLib V2-Consumerfunktionen,](using-the-perflib-functions-to-consume-counter-data.md) um direkt auf Daten von V2-Anbietern zuzugreifen. Dies ist komplexer als die Nutzung von Daten mithilfe der PDH-APIs. Dieser Ansatz kann jedoch nützlich sein, wenn PDH-APIs aufgrund von Leistungs- oder Abhängigkeitsproblemen nicht verwendet werden können. Die PerfLib V2-Implementierung unterstützt direkt das Sammeln von Daten von V2-Anbietern. Das Sammeln von Daten von V1-Anbietern wird nicht unterstützt.

> [!NOTE]
> Windows OneCore enthält keine PDH.dll und keine Unterstützung für die Erfassung von Leistungsindikatordaten über die Registrierungs-APIs. Consumer, die auf OneCore ausgeführt werden, müssen die PerfLib V2-Consumerfunktionen verwenden.

V1-Anbieter werden als Anbieter-DLL implementiert, die in den Consumerprozess geladen wird. Die Implementierung der Registrierungs-API verwaltet das Laden der Anbieter-DLL, das Aufrufen in die DLL zum Sammeln von Leistungsdaten und das Entladen der DLL nach Bedarf. Die Anbieter-DLL ist für das Sammeln von [Leistungsdaten nach Bedarf](communicating-with-your-application.md)verantwortlich, z. B. mithilfe normaler Windows-APIs, RPC, Named Pipes, freigegebenem Arbeitsspeicher oder anderer prozessübergreifender Kommunikationsmechanismen.

V2-Anbieter werden entweder als Benutzermodusprogramm (häufig ein Windows Dienst) oder als Kernelmodustreiber implementiert. In der Regel wird der Code des Leistungsdatenanbieters direkt in eine vorhandene Komponente integriert (d. h. der Treiber oder Dienst meldet Statistiken über sich selbst). Die PerfLib V2-Implementierung verwaltet Anforderungen und Antworten über die PCW.sys Kernelerweiterung, sodass der Anbieter normalerweise keine prozessübergreifende Kommunikation implementieren muss, um die Leistungsdaten bereitzustellen.

> [!NOTE]
> Windows Leistungsindikator-APIs und -Tools bieten eingeschränkte Unterstützung für den Zugriff auf Leistungsindikatoren von anderen Computern über die Remoteregistrierung (für V1-Anbieter) und RPC (für V2-Anbieter). Diese Unterstützung ist in Bezug auf die Authentifizierungssteuerelemente (die Tools und APIs können sich nur als aktueller Benutzer authentifizieren) sowie in Bezug auf die [Systemkonfiguration](accessing-remote-counter-data.md) (die erforderlichen Endpunkte und Dienste sind standardmäßig deaktiviert) schwierig zu verwenden. In vielen Fällen ist es besser, über [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) auf die Leistungsindikatoren von Remotesystemen zuzugreifen, anstatt über die integrierte Remotezugriffsunterstützung.

## <a name="developer-audience"></a>Entwicklergruppe

Leistungsindikatoren werden häufig von Administratoren genutzt, um Leistungsprobleme oder ungewöhnliches Verhalten von Systemen zu identifizieren, von Entwicklern, um die Ressourcennutzung von Softwarekomponenten zu untersuchen, und von einzelnen Benutzern, um zu verstehen, wie sich Programme auf ihrem System verhalten. Die Verwendung kann über GUI-Tools wie Task-Manager oder Leistungsmonitor, Befehlszeilentools wie typeperf.exe oder logman.exe, über Skripts über WMI und PowerShell oder über C/C++ und .NET-APIs erfolgen.

Leistungsindikatoranbieter werden in der Regel als Kernelmodustreiber oder Benutzermodusdienste implementiert. Leistungsindikatoranbieter werden in der Regel in C oder C++ geschrieben.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Informationen zu Laufzeitanforderungen für ein bestimmtes Programmierelement finden Sie im Abschnitt Anforderungen der Referenzseite für dieses Element.

Informationen zum Versionsverlauf finden Sie unter [Neuerungen.](performance-counters-what-s-new.md)

## <a name="see-also"></a>Siehe auch

[Verwenden von Leistungsindikatoren](using-performance-counters.md)

[Referenz zu Leistungsindikatoren](performance-counters-reference.md)
