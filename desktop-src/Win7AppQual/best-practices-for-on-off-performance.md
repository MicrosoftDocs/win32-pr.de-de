---
description: .
ms.assetid: 872c2a33-327e-41a8-81db-905c46673f13
title: Bewährte Methoden für ein-/ausschalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda45cb1ec7fb66b8afdcdebab7c92bdb071a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373351"
---
# <a name="best-practices-for-onoff-performance"></a>Bewährte Methoden für ein-/ausschalten

## <a name="platform"></a>Plattform

**Clients:** Windows Vista \| Windows 7  
**Server:** Windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>BESCHREIBUNG

Die System Energiezustände (oder S-Zustände), wie in der Advanced Computer Power Interface (ACPI)-Spezifikation definiert, werden als ein-/ausschalten bezeichnet, da es sich bei dem gängigsten Übergang des s-Zustands um einen Computer handelt, der ein-und ausgeschaltet. Bei einem System, auf dem Windows Vista oder Windows 7 ausgeführt wird, gibt es unterschiedliche on/off-Zustandsübergänge: Boot, Standby (ACPI S3), Ruhezustand (ACPI S4) und Shutdown.

Eine gute Leistung während dieser on/off-Übergänge verbessert nicht nur die wahrgenommene Qualität eines Computers, sondern wirkt sich auch stark auf die täglichen Computer Verwendungs Muster und die Systemzuverlässigkeit aus. Kunden können durch Systeme, die zu lange zum Starten oder Herunterfahren benötigen, frustriert werden. Mobile Systeme mit langen Standby-und Ruhe Zustands Übergängen können die Akku Lebensdauer unnötig erschöpft werden. Längere Beendigungs Zeiten können sich auch negativ auf die Zuverlässigkeit mobiler Systeme auswirken. Beispielsweise erhöhen Sie das Risiko unerwarteter Strom Ausschnitten.

System Erweiterungen, wie z. b. Treiber, Anwendungen und Dienste, können erhebliche Auswirkungen auf die Übergangszeiten für ein/aus haben. In diesem Abschnitt werden einige bewährte Methoden erläutert, die Anwendungs-und Dienst Entwickler befolgen können, um Verzögerungen beim Starten, Standbymodus und Herunterfahren zu vermeiden und eine reaktionsfähige Benutzerfunktion nach dem Start und nach dem fortsetzen sicherzustellen. Weitere Informationen zum Ermitteln von Leistungsproblemen mit dem Windows Performance Toolkit und zum Implementieren der unten aufgeführten Empfehlungen für Ihre Anwendung oder ihren Dienst finden Sie in den Whitepaper im Abschnitt "Links zu anderen Ressourcen".

## <a name="best-practices"></a>Bewährte Methoden

-   Verwenden Sie das Windows Performance Toolkit, um die Leistung während aller ein-/aus-Übergänge zu messen.
-   Führen Sie Tests auf kontrollierte Weise durch, und treffen Sie Vergleiche mit einer gültigen Baseline:
    -   Abrufen einer grundlegenden Messung auf einem System mit möglichst wenigen Systemerweiterungen
    -   Anwendungen und Dienste einzeln hinzufügen
    -   Testen auf unannehmbare Regressionen bei on/off-Übergangszeiten
-   Vermeiden Sie die Verwendung von verwaltetem Code für Anwendungen auf dem kritischen Start Pfad.
-   Stellen Sie sicher, dass alle Anwendungen schnell auf Benachrichtigungen zum Herunterfahren Antworten (WM \_ queryendsession und WM \_ EndSession Messages).
-   Verringern Sie die Verzögerungen beim Herunterfahren von Diensten und Anwendungen, indem Sie die CPU-, Datenträger-und Netzwerkaktivität als Reaktion auf Benachrichtigungen zum Herunterfahren minimieren.
-   Vermeiden von Verzögerungen bei der Verarbeitung der Suspend-Benachrichtigung (WM- \_ powerbroadcast-Nachricht).
-   Reagieren Sie schnell auf das Fortsetzen von Ereignissen, und minimieren Sie die CPU-, Datenträger-und Netzwerk Auslastung nach
-   Reduzieren Sie den Verbrauch von Anwendungs Ressourcen nach dem Start.
-   Starten Sie bei jedem Start keine Anwendungen von der RunOnce-Taste.
-   Konvertieren Sie alle nicht wichtigen Dienste so, dass der Start oder der Start des Starts gestartet wird, um Systemressourcen während des Starts verfügbar zu machen.
-   Vermeiden Sie die Verwendung von Lade Auftrags Gruppen zum Ausdrücken von Dienst Abhängigkeiten.
-   Stellen Sie sicher, dass alle laufenden Dienste diesen Status während des Starts so schnell wie möglich melden, um zu verhindern, dass der Dienststeuerungs-Manager blockiert wird.
-   Vermeiden Sie die Verwendung von verwaltetem Code für Dienste im Startpfad.
-   Erlauben Sie nicht, dass sich Dienste für den Empfang von Benachrichtigungen vor dem Herunterfahren und Herunterfahren entscheiden (Dienst \_ Kontrolle \_ : vorshutdown und \_ Dienststeuerungs- \_ Steuerungs Codes), sofern dies nicht unbedingt erforderlich ist.
-   Stellen Sie sicher, dass alle Dienste, die sich für den Empfang von Shutdown-Benachrichtigungen entschieden haben, schnell auf den SCM
-   Vergewissern Sie sich, dass sich die Dienste nicht für das Empfangen von Suspend-Benachrichtigungen entscheiden, es sei denn,
-   Stellen Sie sicher, dass alle Dienste schnell reagieren, um Ereignisse wieder aufzunehmen, und minimieren Sie die CPU-, Datenträger-und Netzwerk Auslastung nach

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   -   [Lösungs Handbuch zum Windows on/off-Übergänge](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Übertragung der Übergangs Leistung von Windows Vista](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Windows-Leistungsanalyse](https://msdn.microsoft.com/performance/default.aspx)
-   [Dokumentation zu Windows Performance Toolkit auf MSDN](/previous-versions/windows/desktop/xperf/windows-performance-analyzer--wpa-)
-   [Forum zur Windows-Leistungsanalyse](https://social.msdn.microsoft.com/Forums/wptk_v4/threads/)
-   [Ereignis Ablauf Verfolgung für Windows auf MSDN](../etw/event-tracing-portal.md)

 

 
