---
description: Bewährte Methoden für die Ein-/Aus-Leistung
ms.assetid: 872c2a33-327e-41a8-81db-905c46673f13
title: Bewährte Methoden für die Ein-/Aus-Leistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef9e10b0a6fc82be138951d45f811ce1ccf0dbe2222b620cf73d0c272570c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031050"
---
# <a name="best-practices-for-onoff-performance"></a>Bewährte Methoden für die Ein-/Aus-Leistung

## <a name="platform"></a>Plattform

**Clients –** Windows Vista \| Windows 7  
**Server –** Windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>BESCHREIBUNG

Die Systemleistungszustände (oder S-Zustände), wie in der Spezifikation advanced Computer Power Interface (ACPI) definiert, werden umgangssprachlich als Ein-/Aus-Zustände bezeichnet, da der gängigste S-Zustandsübergang ein Computer ist, der ein- und ausgeschaltet wird. Die verschiedenen Ein-/Aus-Zustandsübergänge auf einem System, auf dem Windows Vista oder Windows 7 ausgeführt wird, sind Start, Ruhezustand (ACPI S3), Ruhezustand (ACPI S4) und Herunterfahren.

Eine gute Leistung während dieser Ein-/Aus-Übergänge verbessert nicht nur die wahrgenommene Qualität eines Computers, sondern wirkt sich auch erheblich auf die täglichen Computernutzungsmuster und die Systemzuverlässigkeit aus. Kunden können von Systemen frustriert werden, die zu lange zum Starten oder Herunterfahren dauern. Mobile Systeme mit langen Ruhezustands- und Ruhezustandsübergängen können die Akkulebensdauer unnötigerweise versappen. Längere Herunterfahrenszeiten können sich auch negativ auf die Zuverlässigkeit mobiler Systeme auswirken. Beispielsweise erhöhen sie das Risiko unerwarteter Stromabschaltungen.

Systemerweiterungen wie Treiber, Anwendungen und Dienste können erhebliche Auswirkungen auf die Ein-/Aus-Übergangszeiten haben. In diesem Abschnitt werden einige der bewährten Methoden erläutert, die Anwendungs- und Dienstentwickler befolgen können, um Verzögerungen beim Starten, Standby und Herunterfahren zu vermeiden und eine reaktionsfähige Benutzererfahrung nach dem Start und nach dem Fortsetzen sicherzustellen. Weitere Informationen zum Identifizieren von Ein-/Aus-Leistungsproblemen mit dem Windows Performance Toolkit und zum Implementieren der folgenden Empfehlungen für Ihre Anwendung oder Ihren Dienst finden Sie in den Whitepapers im Abschnitt "Links zu anderen Ressourcen".

## <a name="best-practices"></a>Empfehlungen

-   Verwenden Sie das Windows Performance Toolkit, um die Leistung während aller Ein-/Aus-Übergänge zu messen.
-   Führen Sie Tests kontrolliert durch, und führen Sie Vergleiche mit einer gültigen Baseline durch:
    -   Abrufen einer Baselinemessung auf einem System mit so wenigen Systemerweiterungen wie möglich
    -   Hinzufügen von Anwendungen und Diensten nach dem anderen
    -   Testen auf inakzeptable Regressionen bei Ein-/Aus-Übergangszeiten
-   Vermeiden Sie die Verwendung von verwaltetem Code für Anwendungen auf dem kritischen Startpfad.
-   Stellen Sie sicher, dass alle Anwendungen schnell auf Benachrichtigungen zum Herunterfahren reagieren (WM \_ QUERYENDSESSION- und WM \_ ENDSESSION-Meldungen).
-   Verringern Sie Verzögerungen beim Herunterfahren von Diensten und Anwendungen, indem Sie die CPU-, Datenträger- und Netzwerkaktivität als Reaktion auf Benachrichtigungen zum Herunterfahren minimieren.
-   Vermeiden Sie Verzögerungen bei der Verarbeitung der Suspend-Benachrichtigung (WM \_ POWERBROADCAST-Nachricht).
-   Reagieren Sie schnell, um Ereignisse wieder aufzunehmen und die CPU-, Datenträger- und Netzwerkauslastung nach dem Fortsetzen zu minimieren.
-   Reduzieren Sie den Verbrauch von Anwendungsressourcen nach dem Start.
-   Starten Sie Anwendungen nicht bei jedem Start über den RunOnce-Schlüssel.
-   Konvertieren Sie alle nicht unwesentlichen Dienste in den start- oder trigger-Start nach Bedarf, um Systemressourcen während des Startvorgangs verfügbar zu machen.
-   Vermeiden Sie die Verwendung von Lastenausgleichsgruppen, um Dienstabhängigkeiten auszudrücken.
-   Stellen Sie sicher, dass alle ausgeführten Dienste diesen Status so bald wie möglich während des Startvorgangs melden, um zu vermeiden, dass der Dienststeuerungs-Manager (Service Control Manager, SCM) blockiert wird.
-   Vermeiden Sie die Verwendung von verwaltetem Code für Dienste im Startpfad.
-   Lassen Sie nicht zu, dass Dienste sich für den Empfang von Benachrichtigungen vor dem Herunter- und Herunterfahren (SERVICE \_ CONTROL \_ PRESHUTDOWN- und SERVICE \_ CONTROL SHUTDOWN-Steuerungscodes) entscheiden, es sei denn, dies \_ ist unbedingt erforderlich.
-   Stellen Sie sicher, dass alle Dienste, die sich für den Empfang von Benachrichtigungen zum Herunterfahren entschieden haben, schnell auf den SCM reagieren.
-   Vergewissern Sie sich, dass Dienste nicht den Empfang von Benachrichtigungen zum Angehaltenen aktivieren, es sei denn, dies ist unbedingt erforderlich.
-   Stellen Sie sicher, dass alle Dienste schnell reagieren, um Ereignisse wieder aufzunehmen und die CPU-, Datenträger- und Netzwerkauslastung nach dem Fortsetzen zu minimieren.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   -   [Windows Lösungshandbuch für Ein/Aus-Übergänge](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Leistungsanalyse des Ein/Aus-Übergangs von Windows Vista](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Windows Leistungsanalyse](https://msdn.microsoft.com/performance/default.aspx)
-   [Windows Dokumentation zum Performance Toolkit auf MSDN](/previous-versions/windows/desktop/xperf/windows-performance-analyzer--wpa-)
-   [Windows Forum zur Leistungsanalyse](https://social.msdn.microsoft.com/Forums/wptk_v4/threads/)
-   [Ereignisablaufverfolgung für Windows auf MSDN](../etw/event-tracing-portal.md)

 

 
