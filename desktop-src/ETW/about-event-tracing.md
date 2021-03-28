---
description: Ereignisablaufverfolgung für Windows (ETW) ist eine effiziente Ablaufverfolgungsfunktion auf Kernelebene, mit der Sie kernel- oder anwendungsdefinierte Ereignisse in einer Protokolldatei protokollieren können.
ms.assetid: 0eaa7bd3-8537-483a-b0d6-db3b790a6f3d
title: Informationen zur Ereignis Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2f13284cec1d9300c23241fafe154f277f72a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959085"
---
# <a name="about-event-tracing"></a>Informationen zur Ereignis Ablauf Verfolgung

Ereignisablaufverfolgung für Windows (ETW) ist eine effiziente Ablaufverfolgungsfunktion auf Kernelebene, mit der Sie kernel- oder anwendungsdefinierte Ereignisse in einer Protokolldatei protokollieren können. Sie können die Ereignisse in Echtzeit oder über eine Protokolldatei nutzen und zum Debuggen einer Anwendung verwenden oder um zu bestimmen, wo Leistungsprobleme in der Anwendung auftreten.

Mit etw können Sie die Ereignis Ablauf Verfolgung dynamisch aktivieren bzw. deaktivieren, sodass Sie eine ausführliche Ablauf Verfolgung in einer Produktionsumgebung ausführen können, ohne dass Computer-oder Anwendungs Neustarts erforderlich sind.

Die Ereignis Ablauf Verfolgungs-API ist in drei unterschiedliche Komponenten unterteilt:

-   [Controller](#controllers), die eine Ereignis Ablauf Verfolgungs Sitzung starten und beenden und Anbieter aktivieren
-   [Anbieter](#providers), die die Ereignisse bereitstellen
-   Consumer [, die](#consumers)die Ereignisse nutzen

Das folgende Diagramm zeigt das Ereignis Ablauf Verfolgungs Modell.

![Ereignis Ablauf Verfolgungs Modell](images/etdiag2.png)

## <a name="controllers"></a>Controller

Bei Controllern handelt es sich um Anwendungen, die die Größe und den Speicherort der Protokolldatei definieren, [Ereignis Ablauf Verfolgungs Sitzungen](event-tracing-sessions.md)starten und Abbrechen, Anbieter aktivieren, damit Sie Ereignisse in der Sitzung protokollieren, die Größe des Pufferpools verwalten und Ausführungs Statistiken für Sitzungen abrufen können. Sitzungs Statistiken enthalten die Anzahl der verwendeten Puffer, die Anzahl der übermittelten Puffer und die Anzahl der verlorenen Ereignisse und Puffer. 

Weitere Informationen finden Sie unter [Steuern von Ereignis Ablauf Verfolgungs Sitzungen](controlling-event-tracing-sessions.md).

## <a name="providers"></a>Anbieter

Anbieter sind Anwendungen, die die Ereignis Ablauf Verfolgungs Instrumentation enthalten. Nachdem sich ein Anbieter registriert hat, kann ein Controller die Ereignis Ablauf Verfolgung im Anbieter aktivieren bzw. deaktivieren. Der Anbieter definiert seine Interpretation, dass er aktiviert oder deaktiviert wird. Im allgemeinen generiert ein aktivierter Anbieter Ereignisse, während dies bei einem deaktivierten Anbieter nicht der Fall ist. Auf diese Weise können Sie der Anwendung die Ereignis Ablauf Verfolgung hinzufügen, ohne dass die Ereignisse immer generiert werden müssen. 

Obwohl das ETW-Modell den Controller und den Anbieter in separate Anwendungen trennt, kann eine Anwendung beide Komponenten enthalten.

Weitere Informationen finden Sie unter [Bereitstellen von Ereignissen](providing-events.md).

### <a name="types-of-providers"></a>Anbietertypen

Es gibt vier Haupttypen von Anbietern: MOF (Classic)-Anbieter, WPP-Anbieter, Manifest-basierte Anbieter und tracelogging-Anbieter. Wenn Sie Anwendungen für Windows Vista oder höher schreiben, die keine Legacy Systeme unterstützen müssen, sollten Sie einen manifestressourcenbasierten Anbieter oder einen tracelogging-Anbieter verwenden.

#### <a name="mof-classic-providers"></a>MOF (Classic)-Anbieter:

-   Verwenden Sie die Funktionen [registertraceguids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) und [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) , um Ereignisse zu registrieren und zu schreiben.
-   Verwenden Sie MOF-Klassen, um Ereignisse zu definieren, damit Consumer wissen, wie Sie Sie nutzen können.
-   Kann jeweils nur von einer Ablauf Verfolgungs Sitzung aktiviert werden.

#### <a name="wpp-providers"></a>WPP-Anbieter:

-   Verwenden Sie die Funktionen [registertraceguids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) und [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) , um Ereignisse zu registrieren und zu schreiben.
-   Mit zugeordneten TMF-Dateien (kompiliert in eine PDB-Datei) mit Decodierungs Informationen, die aus der Überprüfung der WPP-Instrumentation des präprozessorcodes im Quellcode abgeleitet wurden.
-   Kann jeweils nur von einer Ablauf Verfolgungs Sitzung aktiviert werden.

#### <a name="manifest-based-providers"></a>Manifestressourcenbasierte Anbieter:

-   Verwenden Sie [EventRegister](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) und [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) , um Ereignisse zu registrieren und zu schreiben.
-   Verwenden Sie ein Manifest, um Ereignisse zu definieren, damit Consumer wissen, wie Sie Sie nutzen können.
-   Kann bis zu acht Ablauf Verfolgungs Sitzungen gleichzeitig aktiviert werden.

#### <a name="tracelogging-providers"></a>[Tracelogging](/windows/desktop/tracelogging/trace-logging-about) -Anbieter:

-   Verwenden Sie " [traceloggingregister](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) " und " [traceloggingwrite](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) ", um Ereignisse zu registrieren und zu schreiben.
-   Verwenden Sie selbst beschreibende Ereignisse, sodass die Ereignisse selbst alle erforderlichen Informationen enthalten, um Sie zu verarbeiten.
-   Kann bis zu acht Ablauf Verfolgungs Sitzungen gleichzeitig aktiviert werden.

Alle Ereignis Anbieter verwenden grundsätzlich die Ereignis-Ablauf Verfolgungs Familie der APIs ([TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) für Legacy Technologien und [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) / [EventWrite-Ex](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) für neuere Technologien). Ereignis Anbieter unterscheiden sich einfach in den Feldtypen, die Sie in Ereignis Nutzlasten speichern, und wo Sie die zugehörigen ereignisdecodierinformationen speichern.

## <a name="consumers"></a>Consumer

Consumer sind Anwendungen, die eine oder mehrere Ereignis Ablauf Verfolgungs Sitzungen als Quelle für Ereignisse auswählen. Ein Consumer kann Ereignisse von mehreren Ereignis Ablauf Verfolgungs Sitzungen gleichzeitig anfordern. Das System liefert die Ereignisse in chronologischer Reihenfolge. Consumer können Ereignisse empfangen, die in Protokolldateien gespeichert werden, oder von Sitzungen, die Ereignisse in Echtzeit bereitzustellen. Beim Verarbeiten von Ereignissen kann ein Consumer Start-und Endzeiten angeben, und nur Ereignisse, die im angegebenen Zeitrahmen auftreten, werden übermittelt. 

Weitere Informationen finden Sie unter Verwenden von [Ereignissen](consuming-events.md).

## <a name="missing-events"></a>Fehlende Ereignisse

Perfmon, Systemdiagnose und andere System Tools melden möglicherweise fehlende Ereignisse im Ereignisprotokoll und geben an, dass die Einstellungen für die Ereignis Ablauf Verfolgung für Windows (ETW) möglicherweise nicht optimal sind. Ereignisse können aus verschiedenen Gründen verloren gehen:

-   Die Gesamt Ereignis Größe ist größer als 64K. Dazu gehört der etw-Header sowie die Daten oder die Nutzlast. Ein Benutzer hat keine Kontrolle über diese fehlenden Ereignisse, da die Ereignis Größe von der Anwendung konfiguriert wird.

-   Die ETW-Puffergröße ist kleiner als die Gesamt Ereignis Größe. Ein Benutzer hat keine Kontrolle über diese fehlenden Ereignisse, da die Ereignis Größe von der Anwendung konfiguriert wird, die die Ereignisse protokolliert.

-   Bei der Echt Zeit Protokollierung beansprucht der Echt Zeit Consumer Ereignisse nicht schnell genug oder ist nicht vollständig vorhanden, und die Sicherungsdatei wird aufgefüllt. Dies kann der Fall sein, wenn der Ereignisprotokoll Dienst beendet und gestartet wird, wenn Ereignisse protokolliert werden. Ein Benutzer hat keine Kontrolle über diese fehlenden Ereignisse.

-   Bei der Protokollierung in einer Datei ist der Datenträger zu langsam, um die Protokollierungs Rate zu behalten.

Aus diesen Gründen melden Sie diese Probleme dem Anbieter der Anwendung oder des Dienstanbieters, der die Ereignisse erzeugt. Diese Probleme können nur vom Anwendungsentwickler oder vom Dienst behoben werden, der die Ereignisse protokolliert. Wenn die fehlenden Ereignisse im Ereignisprotokoll Dienst gemeldet werden, deutet dies möglicherweise auf ein Problem mit der Konfiguration des Ereignisprotokoll Dienstanbieter hin. Der Benutzer kann den maximalen Speicherplatz erhöhen, der vom Ereignisprotokoll Dienst verwendet werden kann, wodurch die Anzahl der fehlenden Ereignisse reduziert werden kann.

 

 
