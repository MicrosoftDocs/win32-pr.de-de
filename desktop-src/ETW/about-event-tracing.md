---
description: Ereignisablaufverfolgung für Windows (ETW) ist eine effiziente Ablaufverfolgungsfunktion auf Kernelebene, mit der Sie kernel- oder anwendungsdefinierte Ereignisse in einer Protokolldatei protokollieren können.
ms.assetid: 0eaa7bd3-8537-483a-b0d6-db3b790a6f3d
title: Informationen zur Ereignisablaufverfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5004ada6d0d11d9c232a6fda1553ea24de5a59fb1d03e46728084f84f0e79de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086430"
---
# <a name="about-event-tracing"></a>Informationen zur Ereignisablaufverfolgung

Ereignisablaufverfolgung für Windows (ETW) ist eine effiziente Ablaufverfolgungsfunktion auf Kernelebene, mit der Sie kernel- oder anwendungsdefinierte Ereignisse in einer Protokolldatei protokollieren können. Sie können die Ereignisse in Echtzeit oder aus einer Protokolldatei nutzen und sie verwenden, um eine Anwendung zu debuggen oder zu bestimmen, wo Leistungsprobleme in der Anwendung auftreten.

Mit ETW können Sie die Ereignisablaufverfolgung dynamisch aktivieren oder deaktivieren, sodass Sie eine detaillierte Ablaufverfolgung in einer Produktionsumgebung ausführen können, ohne dass ein Neustart des Computers oder der Anwendung erforderlich ist.

Die Ereignisablaufverfolgungs-API ist in drei verschiedene Komponenten zerbrochen:

-   [Controller](#controllers), die eine Ereignisablaufverfolgungssitzung starten und beenden und Anbieter aktivieren
-   [Anbieter,](#providers)die die Ereignisse bereitstellen
-   [Consumers](#consumers), die die Ereignisse nutzen

Das folgende Diagramm zeigt das Ereignisablaufverfolgungsmodell.

![Ereignisablaufverfolgungsmodell](images/etdiag2.png)

## <a name="controllers"></a>Controller

Controller sind Anwendungen, die die Größe und den Speicherort der Protokolldatei definieren, Ereignisablaufverfolgungssitzungen starten und [beenden,](event-tracing-sessions.md)Anbieter aktivieren, damit sie Ereignisse in der Sitzung protokollieren, die Größe des Pufferpools verwalten und Ausführungsstatistiken für Sitzungen abrufen können. Sitzungsstatistiken umfassen die Anzahl der verwendeten Puffer, die Anzahl der übermittelten Puffer und die Anzahl der verloren gegangenen Ereignisse und Puffer. 

Weitere Informationen finden Sie unter [Steuern von Ereignisablaufverfolgungssitzungen.](controlling-event-tracing-sessions.md)

## <a name="providers"></a>Anbieter

Anbieter sind Anwendungen, die die Instrumentierung der Ereignisablaufverfolgung enthalten. Nachdem sich ein Anbieter registriert hat, kann ein Controller die Ereignisablaufverfolgung im Anbieter aktivieren oder deaktivieren. Der Anbieter definiert seine Interpretation, ob er aktiviert oder deaktiviert ist. Im Allgemeinen generiert ein aktivierter Anbieter Ereignisse, während ein deaktivierter Anbieter dies nicht tut. Auf diese Weise können Sie ihrer Anwendung ereignisablaufverfolgung hinzufügen, ohne dass sie immer Ereignisse generieren muss. 

Obwohl das ETW-Modell controller und Anbieter in separate Anwendungen trennt, kann eine Anwendung beide Komponenten enthalten.

Weitere Informationen finden Sie unter [Bereitstellen von Ereignissen.](providing-events.md)

### <a name="types-of-providers"></a>Anbietertypen

Es gibt vier Haupttypen von Anbietern: MOF-Anbieter (klassisch), WPP-Anbieter, manifestbasierte Anbieter und TraceLogging-Anbieter. Sie sollten einen manifestbasierten Anbieter oder einen TraceLogging-Anbieter verwenden, wenn Sie Anwendungen für Windows Vista oder höher schreiben, die keine Legacysysteme unterstützen müssen.

#### <a name="mof-classic-providers"></a>MOF-Anbieter (klassisch):

-   Verwenden Sie die [Funktionen RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) [und TraceEvent,](/windows/win32/api/evntrace/nf-evntrace-traceevent) um Ereignisse zu registrieren und zu schreiben.
-   Verwenden Sie MOF-Klassen, um Ereignisse zu definieren, damit Die Verbraucher wissen, wie sie sie verwenden.
-   Kann nur von einer Ablaufverfolgungssitzung gleichzeitig aktiviert werden.

#### <a name="wpp-providers"></a>WPP-Anbieter:

-   Verwenden Sie die [Funktionen RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) [und TraceEvent,](/windows/win32/api/evntrace/nf-evntrace-traceevent) um Ereignisse zu registrieren und zu schreiben.
-   Verfügen Sie über zugeordnete TMF-Dateien (kompiliert in die PDB-Datei einer Binärdatei), die Decodierungsinformationen enthalten, die aus dem Scan der WPP-Instrumentierung im Quellcode des Präprozessors abgeleitet wurden.
-   Kann nur von einer Ablaufverfolgungssitzung gleichzeitig aktiviert werden.

#### <a name="manifest-based-providers"></a>Manifestbasierte Anbieter:

-   Verwenden [Sie EventRegister](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) und [EventWrite,](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) um Ereignisse zu registrieren und zu schreiben.
-   Verwenden Sie ein Manifest, um Ereignisse zu definieren, damit die Kunden wissen, wie sie sie verwenden.
-   Kann durch bis zu acht Ablaufverfolgungssitzungen gleichzeitig aktiviert werden.

#### <a name="tracelogging-providers"></a>[TraceLogging-Anbieter:](/windows/desktop/tracelogging/trace-logging-about)

-   Verwenden [Sie TraceLoggingRegister und](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) [TraceLoggingWrite,](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) um Ereignisse zu registrieren und zu schreiben.
-   Verwenden Sie selbstbeschreibende Ereignisse, damit die Ereignisse selbst alle erforderlichen Informationen für deren Nutzung enthalten.
-   Kann durch bis zu acht Ablaufverfolgungssitzungen gleichzeitig aktiviert werden.

Alle Ereignisanbieter verwenden im Wesentlichen die Ereignisablaufverfolgungsfamilie von APIs ([TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) für Legacytechnologien und [](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) / [EventWrite EventWriteEx](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) für neuere). Ereignisanbieter unterscheiden sich einfach in den Feldtypen, die sie in Ereignisnutzlasten speichern, und dem Ort, an dem sie die zugehörigen Ereignisdecodierungsinformationen speichern.

## <a name="consumers"></a>Consumer

Consumers sind Anwendungen, die eine oder mehrere Ereignisablaufverfolgungssitzungen als Ereignisquelle auswählen. Ein Consumer kann Ereignisse von mehreren Ereignisablaufverfolgungssitzungen gleichzeitig anfordern. das System übermittelt die Ereignisse in chronologischer Reihenfolge. Benutzer können Ereignisse empfangen, die in Protokolldateien gespeichert sind, oder von Sitzungen, die Ereignisse in Echtzeit liefern. Bei der Verarbeitung von Ereignissen kann ein Consumer Start- und Endzeiten angeben, und nur Ereignisse, die im angegebenen Zeitrahmen auftreten, werden übermittelt. 

Weitere Informationen finden Sie unter [Verwenden von Ereignissen.](consuming-events.md)

## <a name="missing-events"></a>Fehlende Ereignisse

Perfmon, Systemdiagnose und andere Systemtools melden möglicherweise fehlende Ereignisse im Ereignisprotokoll und geben an, dass die Einstellungen für die Ereignisablaufverfolgung für Windows (ETW) möglicherweise nicht optimal sind. Ereignisse können aus verschiedenen Gründen verloren gehen:

-   Die Gesamtereignisgröße ist größer als 64.000. Dies schließt den ETW-Header sowie die Daten oder Nutzlast ein. Ein Benutzer hat keine Kontrolle über diese fehlenden Ereignisse, da die Ereignisgröße von der Anwendung konfiguriert wird.

-   Die ETW-Puffergröße ist kleiner als die Gesamtereignisgröße. Ein Benutzer hat keine Kontrolle über diese fehlenden Ereignisse, da die Ereignisgröße von der Anwendung konfiguriert wird, die die Ereignisse protokolliert.

-   Für die Echtzeitprotokollierung verwendet der Echtzeit-Consumer Ereignisse nicht schnell genug oder ist nicht vollständig vorhanden, und dann füllt sich die Hintergrunddatei. Dies kann dazu führen, dass der Ereignisprotokolldienst beendet und gestartet wird, wenn Ereignisse protokolliert werden. Ein Benutzer hat keine Kontrolle über diese fehlenden Ereignisse.

-   Bei der Protokollierung in einer Datei ist der Datenträger zu langsam, um mit der Protokollierungsrate mithalten zu können.

Melden Sie diese Probleme aus jedem dieser Gründe an den Anbieter der Anwendung oder des Diensts, die die Ereignisse generiert. Diese Probleme können nur vom Anwendungsentwickler oder vom Dienst behoben werden, der die Ereignisse protokollieren. Wenn die fehlenden Ereignisse im Ereignisprotokolldienst gemeldet werden, kann dies auf ein Problem mit der Konfiguration des Ereignisprotokolldiensts hinweisen. Der Benutzer hat möglicherweise eingeschränkte Möglichkeiten, den maximalen Speicherplatz zu erhöhen, der vom Ereignisprotokolldienst verwendet werden soll, wodurch die Anzahl der fehlenden Ereignisse reduziert werden kann.

 

 
