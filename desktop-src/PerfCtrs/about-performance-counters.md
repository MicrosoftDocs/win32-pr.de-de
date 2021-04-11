---
description: Leistungsindikatoren werden verwendet, um Informationen darüber bereitzustellen, wie gut das Betriebssystem, die Anwendung, der Dienst oder der Treiber ausgeführt wird.
ms.assetid: d172a131-61d3-4fc1-8e0c-b07b2bd34f80
title: Informationen zu Leistungsindikatoren
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dec7c71e99ab614ee64e3d1e8c9620f0be78c14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865136"
---
# <a name="about-performance-counters"></a>Informationen zu Leistungsindikatoren

Windows-Leistungsindikatoren stellen eine Abstraktions Ebene auf hoher Ebene mit einer konsistenten Schnittstelle zum Erfassen verschiedener Arten von Systemdaten bereit, wie z. b. CPU, Arbeitsspeicher und Datenträger Verwendungs Statistiken. System Administratoren verwenden Leistungsindikatoren, um Probleme mit der Leistung oder dem Verhalten zu überwachen. Software Entwickler verwenden Leistungsindikatoren, um die Ressourcenverwendung ihrer Komponenten zu überprüfen.

> [!IMPORTANT]
> Windows-Leistungsindikatoren sind für die Ermittlung und Erfassung von Verwaltungs-und Diagnosedaten optimiert. Sie sind nicht für die Datensammlung mit hoher Häufigkeit oder für die Anwendungsprofil Erstellung geeignet, da Sie nicht für die mehrmalige Erfassung pro Sekunde entwickelt wurden. Für den Zugriff auf Systeminformationen mit niedrigerem Verwaltungsaufwand bevorzugen Sie möglicherweise direktere APIs, wie z. b. [**Process-Status**](../psapi/process-status-helper.md)-Hilfsobjekt, [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex), [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)oder [**GetProcessTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes). Bei der Profilerstellung können Sie etw-Protokolle mit Systemprofil Erstellungs Daten sammeln, indem Sie [**tracelog.exe**](/windows-hardware/drivers/devtest/tracelog) mit den `-critsec` `-dpcisr` Optionen,, `-eflag` oder `-ProfileSource` verwenden, oder Sie können die [**Hardware Counter-Profilerstellung**](/previous-versions/windows/desktop/hcp/hcp-reference)verwenden.

> [!NOTE]
> Verwechseln Sie Windows-Leistungsindikatoren nicht mit der [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) -API. Windows-Leistungsindikatoren stellen eine Abstraktion auf hoher Ebene für viele Arten von Systeminformationen dar. Die QueryPerformanceCounter-Funktion ermöglicht optimierten Zugriff auf einen Zeitstempel mit hoher Genauigkeit.

## <a name="getting-started"></a>Erste Schritte

- Verwenden Sie [Leistungs Tool Tools](performance-counters-tools.md) , wenn Sie die Leistungsdaten von einem System erfassen oder anzeigen möchten.
- Verwenden Sie [Leistungs befassungs-APIs](consuming-counter-data.md) , wenn Sie ein Skript oder ein Programm schreiben möchten, das Leistungsdaten vom lokalen System sammelt.
- Verwenden Sie [WMI-Leistungs Leistungs Zählers](/windows/desktop/WmiSdk/monitoring-performance-data) , wenn Sie Leistungsdaten von einem lokalen System oder Remote System mithilfe von WMI sammeln möchten.
- Verwenden Sie [Leistungs Anbieter-APIs](providing-counter-data.md) , wenn Sie Leistungsdaten von der Softwarekomponente veröffentlichen möchten.

## <a name="concepts"></a>Konzepte

Das Windows-Leistungsindikator System **ist in Consumer**, **Anbieter**, **countersets**, **Indikatoren**, **Instanzen** und Indikator **Werte** organisiert.

Ein **Consumer** ist eine Softwarekomponente, die Leistungsdaten nutzt. Windows umfasst mehrere [integrierte Tools](performance-counters-tools.md) , die Leistungsdaten nutzen. Hierzu gehören Task-Manager, Ressourcenmonitor, System Monitor, typeperf.exe, logman.exe und relog.exe. Entwickler können Skripts und Anwendungen schreiben, die über Leistungsindikator- [APIs](consuming-counter-data.md)auf Leistungsindikatoren zugreifen.

Ein **Anbieter** ist eine Softwarekomponente, mit der [Leistungsdaten generiert und veröffentlicht](providing-counter-data.md)werden. Ein Anbieter veröffentlicht Daten für eine oder mehrere *Gegensätze*. Ein Datenbanksystem kann sich z. b. als Leistungsdaten Anbieter registrieren.

- Ein **v1-Anbieter** ist eine Softwarekomponente, die Leistungsdaten über eine [Leistungs-DLL](providing-counter-data-using-a-performance-dll.md) veröffentlicht, die im Prozess des Consumers ausgeführt wird. Ein v1-Anbieter wird über eine-Datei auf einem System installiert `.ini` . Die v1-Anbieter Architektur ist veraltet. Neue Anbieter sollten die V2-Anbieter Architektur verwenden.
- Ein **v2-Anbieter** ist eine Softwarekomponente, die Leistungsdaten über die [Leistungs Anbieter-APIs](providing-counter-data-using-version-2-0.md)veröffentlicht. Ein v2-Anbieter wird über eine- `.man` Datei (XML-Manifest) auf einem System installiert.

Ein **CounterSet** ist eine Gruppierung von Leistungsdaten innerhalb eines Anbieters. Ein CounterSet weist einen Namen und einen *oder mehrere Indikatoren* auf. Beim Erfassen der Daten aus einer gegen Menge werden mehrere *Instanzen* zurückgegeben. In einigen Windows-APIs werden countersets als **Leistungs Objekte** bezeichnet. Beispielsweise kann ein Leistungsdaten Anbieter für ein Datenbanksystem einen gegen Satz für Statistiken pro Datenbank bereitstellen.

Ein **Leistungs** starker Wert ist die Definition von einzelnen Leistungsdaten. Ein-Counter hat einen Namen und einen Typ. Beispielsweise kann eine "Statistiken pro Datenbank"-CounterSet einen Indikator mit dem Namen "Transaktionen pro Sekunde" mit dem Typ enthalten `PERF_COUNTER_COUNTER` .

Eine **Instanz** ist eine Entität, in der Leistungsdaten gemeldet werden. Eine Instanz hat einen Namen (String) und einen oder mehrere *Werte für den Zählers*. Beispielsweise kann eine "Statistiken pro Datenbank"-CounterSet eine Instanz pro Datenbank enthalten. Der Instanzname ist der Datenbankname, und jede Instanz würde Zählerwerte für die Leistungsindikatoren "Transaktionen pro Sekunde", "Speicherauslastung" und "Datenträger Verwendung" enthalten.

Der Wert eines **Leistungs Zählers ist der** Wert eines einzelnen Leistungsdaten Zählers. Ein Leistungswert ist eine Ganzzahl ohne Vorzeichen, entweder 32-Bit oder 64-Bit, abhängig vom Typ des entsprechenden Zählers. Wenn Sie über eine- *Instanz* sprechen, kann es vorkommen, *dass ein Leistungs* *Zählers* auch als Leistungs-oder *Wert* bezeichnet wird.

> [!TIP]
> Es ist möglicherweise hilfreich, die Leistungsdaten des Leistungs Zählers mit den vertrauten Tabellen Begriffen zu verknüpfen. Ein **CounterSet** ist wie eine Tabelle. Ein- **Wert ist wie eine-** Spalte. Eine **Instanz** ist wie eine Zeile. Ein **Leistungswert** ist wie eine Zelle in der Tabelle.

**Einzelinstanzcountersets** enthalten immer Daten für genau eine Instanz. Dies kommt häufig bei countersets vor, die System globale Statistiken melden. Windows verfügt beispielsweise über eine integrierte einzelinstanzcountermenge mit dem Namen "Memory", die die globale Speicherauslastung meldet.

**Gegensätze mit mehreren** Instanzen enthalten Daten für eine Variable Anzahl von Instanzen. Dies kommt häufig bei countersets vor, die über Entitäten im System Berichten. Windows verfügt beispielsweise über eine integrierte gegen Menge mit mehreren Instanzen mit dem Namen "Prozessor Informationen", die eine Instanz für jede installierte CPU meldet.

Consumer erfassen und erfassen in regelmäßigen Abständen die Daten aus dem CounterSet eines Anbieters. Der Consumer kann z. b. einmal pro Sekunde oder einmal pro Minute Daten sammeln. Die gesammelten Daten werden als **Beispiel** bezeichnet. Ein Beispiel besteht aus Zeitstempeln und den Daten für Instanzen des countersets. Die Daten für jede Instanz enthalten den Instanznamen (Zeichenfolge) und einen Satz von Indikator Werten (ganze Zahlen, einen Wert für jeden Indikator im CounterSet).

Instanznamen sollten normalerweise innerhalb eines Beispiels eindeutig sein, d. h., ein Anbieter sollte nicht zwei Instanzen mit dem gleichen Namen als Teil eines einzelnen Beispiels zurückgeben. Einige ältere Anbieter befolgen diese Regel nicht, sodass Consumer [nicht eindeutige Instanznamen tolerieren müssen](handling-duplicate-instance-names.md). Bei Instanznamen wird die Groß-/Kleinschreibung nicht beachtet

> [!NOTE]
> Aus Gründen der Abwärtskompatibilität gibt das CounterSet "Process" nicht eindeutige Instanznamen basierend auf dem Dateinamen der exe-Datei zurück. Dies kann zu verwirrenden Ergebnissen führen, insbesondere dann, wenn ein Prozess mit einem nicht eindeutigen Namen gestartet oder heruntergefahren wird, da dies in der Regel zu Datenfehlern führt, weil die Instanznamen zwischen den Beispielen falsch abgeglichen werden. Consumer des "Process"-Gegensatzes müssen diese nicht eindeutigen Instanznamen und die resultierenden Datenfehler tolerieren können.

Instanznamen müssen über mehrere Stichproben hinweg stabil sein, d. h. ein Anbieter sollte bei jeder Erfassung des countersets denselben Instanznamen für dieselbe Entität verwenden.

Jeder Counter hat einen Typ. Der zähtertyp gibt den Typ des **Rohwerts** des Zählers an (entweder ganze Zahl 32 ohne Vorzeichen oder eine 64-Bit-Ganzzahl ohne Vorzeichen). Der zähtertyp gibt auch an, was der Rohwert des Zählers darstellt, der bestimmt, wie der Rohwert verarbeitet werden soll, um nützliche Statistiken zu generieren.

Einige Leistungstypen sind einfach und weisen einen Rohdaten Wert auf, der direkt nützlich ist. viele Leistungstypen erfordern [zusätzliche Verarbeitungs](calculating-counter-values.md) Schritte, um einen nützlichen **formatierten Wert** zu erstellen. Um den formatierten Wert zu erhalten, benötigen einige Indikator Typen Rohwerte aus zwei Beispielen, einige Indikator Typen erfordern Zeitstempel, und einige Indikator Typen erfordern Rohwerte aus mehreren Leistungsindikatoren. Beispiel:

- `PERF_COUNTER_LARGE_RAWCOUNT` ist ein 64-Bit-Rohwert, der keine Verarbeitung erfordert. Sie eignet sich für Zeit Punktwerte, wie z. b. "verwendete Bytes des Speichers".
- `PERF_COUNTER_RAWCOUNT_HEX` ist ein 32-Bit-Rohwert, der nur eine einfache hexadezimale Formatierung erfordert, um nützlich zu sein. Sie eignet sich für Zeit Punkt-oder identifizierende Informationen, wie z. b. "Flags" oder "Basisadresse".
- `PERF_COUNTER_BULK_COUNT` ein 64-Bit-Rohwert, der die Anzahl von Ereignissen angibt und verwendet wird, um die Rate zu berechnen, mit der die Ereignisse auftreten. Um nützlich zu sein, erfordert dieser Kontotyp zwei Beispiele, die zeitlich voneinander getrennt sind. Der formatierte Wert ist die Ereignisrate, d. h. die Häufigkeit, mit der das Ereignis pro Sekunde im Intervall zwischen den beiden Beispielen aufgetreten ist. Bei zwei Beispielen `s0` und `s1` würde der formatierte Wert (Ereignisrate) als berechnet werden `(s1.EventCount - s0.EventCount)/(s1.TimestampInSeconds - s0.TimestampInSeconds)` .

Es wird erwartet, dass sich die Anbieter so Verhalten, als wären Sie zustandslos, d. h. das Sammeln von Daten aus einer gegen Menge sollte sich nicht sichtbar auf den Status des Anbieters Ein Anbieter sollte z. b. die Indikatorwerte nicht auf 0 zurücksetzen, wenn ein CounterSet gesammelt wird, und der Zeitstempel einer vorherigen Auflistung nicht zum Anpassen der Werte in der aktuellen Auflistung verwendet werden soll. Stattdessen sollte Sie einfache Rohdaten von Leistungswerten mit exakten Typen bereitstellen, damit der Consumer nützliche Statistiken auf der Grundlage der Rohwerte und der zugehörigen Zeitstempel berechnen kann.

## <a name="performance-api-architecture"></a>Leistungs-API-Architektur

![Performance Counter-Anwendungen rufen Windows-APIs auf, die Anbieter aufrufen, um Leistungsdaten zu erhalten.](images/architecture.png)

Zu den Consumer von Leistungs Zählern gehören:

- Von [Microsoft bereitgestellte Anwendungen](performance-counters-tools.md) , wie z. b. Task-Manager, Ressourcenmonitor, Leistungs Monitor und typeperf.exe.
- Von Microsoft bereitgestellte API-Oberflächen, mit denen Leistungsdaten wie z. b. [WMI-Leistungsklassen](/windows/desktop/WmiSdk/monitoring-performance-data)verfügbar gemacht werden.
- Ihre eigenen Anwendungen oder Skripts, die [Leistungs Zählers-Consumer-APIs](consuming-counter-data.md)verwenden.

Die meisten leistungsindikatorenconsumer verwenden APIs aus [PDH.dll](using-the-pdh-functions-to-consume-counter-data.md) zum Erfassen von Leistungsdaten. PDH verwaltet viele komplexe Aspekte der Erfassung von Leistungsindikatoren, wie z. b. das Abfragen von Abfragen, das Zuordnen von Instanzen über mehrere Stichproben und das berechnen formatierter Werte aus den unformatierten Indikator Daten. Die PDH-Implementierung verwendet die Registrierungs-APIs bei der Nutzung von Daten von einem v1-Anbieter und verwendet die V2-Consumer-APIs, wenn Daten von einem v2-Anbieter verwendet werden.

Einige ältere leistungsindikatorenconsumer verwenden die [Registrierungs-APIs](using-the-registry-functions-to-consume-counter-data.md) , um Leistungsdaten aus dem speziellen `HKEY_PERFORMANCE_DATA` Registrierungsschlüssel zu erfassen. Dies wird für neuen Code nicht empfohlen, da die Verarbeitung der Daten aus der Registrierung komplex und fehleranfällig ist. Die Implementierung der Registrierungs-API unterstützt das Sammeln von Daten von v1-Anbietern direkt. Es unterstützt indirekt das Sammeln von Daten von V2-Anbietern über eine Übersetzungs Schicht, die die V2-Consumer-APIs verwendet.

Einige leistungsindikatorenconsumer verwenden die [Perflib v2-consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md) , um direkt auf Daten von V2-Anbietern zuzugreifen. Dies ist komplexer als das Verarbeiten von Daten mithilfe der PDH-APIs. diese Vorgehensweise kann jedoch nützlich sein, wenn PDH-APIs aufgrund von Leistungs-oder Abhängigkeitsproblemen nicht verwendet werden können. Die Perflib v2-Implementierung unterstützt das Sammeln von Daten von V2-Anbietern direkt. Das Sammeln von Daten von v1-Anbietern wird nicht unterstützt.

> [!NOTE]
> Windows onecore umfasst nicht PDH.dll und bietet keine Unterstützung für die Nutzung von Leistungsdaten für Leistungsdaten über die Registrierungs-APIs. Consumer, die auf onecore ausgeführt werden, müssen die Perflib v2-consumerfunktionen verwenden.

V1-Anbieter werden als Anbieter-DLL implementiert, die in den consumerprozess geladen wird. Die Implementierung der Registrierungs-API verwaltet das Laden der Anbieter-DLL, das Aufrufen der dll zum Sammeln von Leistungsdaten und das Entladen der DLL nach Bedarf. Die Anbieter-dll ist für die [Erfassung von Leistungsdaten](communicating-with-your-application.md)verantwortlich, z. b. durch die Verwendung normaler Windows-APIs, RPC, Named Pipes, Shared Memory oder anderer prozessübergreifende Kommunikationsmechanismen.

V2-Anbieter werden entweder als benutzermodusprogramm (häufig als Windows-Dienst) oder als Kernelmodustreiber implementiert. Normalerweise ist der Leistungsdaten Anbieter Code direkt in eine vorhandene Komponente integriert (d. h. der Treiber oder Dienst meldet Statistiken über sich selbst). Die Perflib v2-Implementierung verwaltet Anforderungen und Antworten über die PCW.sys Kernel Erweiterung, damit der Anbieter in der Regel keine prozessübergreifende Kommunikation implementieren muss, um die Leistungsdaten bereitzustellen.

> [!NOTE]
> Zu den Windows-Leistungsindikator-APIs und-Tools gehören eingeschränkte Unterstützung für den Zugriff auf Leistungsindikatoren von anderen Computern über Remote Registrierung (für v1-Anbieter) und RPC (für V2-Anbieter). Diese Unterstützung ist in Bezug auf Authentifizierungs Steuerelemente (die Tools und APIs können nur als aktueller Benutzer authentifiziert werden) und in Bezug auf die [Systemkonfiguration](accessing-remote-counter-data.md) häufig schwer zu verwenden (die erforderlichen Endpunkte und Dienste sind standardmäßig deaktiviert). In vielen Fällen ist es besser, auf die Leistungsindikatoren von Remote Systemen über [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) zuzugreifen, anstatt über die integrierte Remote Zugriffs Unterstützung.

## <a name="developer-audience"></a>Entwicklergruppe

Leistungsindikatoren werden oft von Administratoren genutzt, um Leistungsprobleme oder nicht normales Verhalten von Systemen zu ermitteln, von Entwicklern, die Ressourcennutzung von Softwarekomponenten zu untersuchen, und von einzelnen Benutzern, um zu verstehen, wie Programme sich auf Ihrem Systemverhalten. Die Verwendung erfolgt möglicherweise über GUI-Tools wie den Task-Manager oder den System Monitor, Befehlszeilen Tools wie typeperf.exe oder logman.exe, über die Skripterstellung über WMI und PowerShell oder über C/C++-und .NET-APIs.

Leistungsindikatorenanbieter werden normalerweise als Kernelmodustreiber oder benutzermodusdienste implementiert. Leistungsindikatorenanbieter werden normalerweise in C oder C++ geschrieben.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.

[Den](performance-counters-what-s-new.md)Versionsverlauf finden Sie unter Neuigkeiten.

## <a name="see-also"></a>Siehe auch

[Verwenden von Leistungsindikatoren](using-performance-counters.md)

[Leistungsindikator Referenz](performance-counters-reference.md)
