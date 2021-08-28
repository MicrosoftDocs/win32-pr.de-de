---
title: Windows-Bewertungstoolkit
description: Windows-Bewertungstoolkit
ms.assetid: 9D0A4F42-F027-4032-8297-045937BD2B6E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6eff172a59a7f0ee00f85a0cd8f237387aaa78
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482676"
---
# <a name="windows-assessment-toolkit"></a>Windows-Bewertungstoolkit

## <a name="platforms"></a>Plattformen

**Clients** – Windows 7 \| Windows 8  

## <a name="description"></a>BESCHREIBUNG

Das Windows Assessment Toolkit und das Windows Performance Toolkit bilden das Windows Assessment and Deployment Kit (ADK). Zusammen bieten sie eine vollständige Lösung zum Auswerten der gesamten Computerleistung und automatisieren die Bereitstellung des Windows Betriebssystems auf neuen Computern.

In diesem Thema liegt der Schwerpunkt auf dem **Assessment Toolkit.** Die Bewertungsergebnisse werden verwendet, um potenzielle Probleme zu diagnostizieren, sodass die Hardware und Software, die Sie entwickeln, reaktionsfähig sind und sich minimal auf die Akkulaufzeit, die Startleistung und die Herunterfahrenszeit auswirken. Die gleichen Bewertungen sind für OEM-Partner, ISV-/IHV-Partner, Fans und andere Mitglieder der Community verfügbar, um ein gemeinsames Framework zum Messen, Vergleichen und Überprüfen von Qualitätsaspekten einzurichten.

Mithilfe der Windows Bewertungstools können Sie verschiedene Leistungsaspekte in einer Vielzahl von Szenarien messen– von der Startzeit über die Akkulebensdauer bis hin zum High-Definition-Videostreaming. Bewertungen können potenzielle Probleme, inkonsistentes Verhalten und zu untersuchende Bereiche identifizieren.

In vorherigen Windows-Versionen waren mehrere Tools zum Messen der Qualität verfügbar, einschließlich Der Geschwindigkeitstestsuite (VTS/VOS), Fundamental Quality Tools Suite (FQTS) und System Power and Performance Tools Suite (SPPTS). Das Assessment Toolkit kombiniert die Funktionen dieser Leistungsdiagnosetools in einem integrierten Satz von Tools, die einfacher zu verwenden sind und umfassendere, aussagekräftige ergebnisse liefert.

Das Windows Assessment Toolkit maximiert die Zufriedenheit der Kunden durch Folgendes:

-   Unterstützung bei der Bewertung der Gesamterfahrung von Windows, Mehrwertsoftware und Treibern sowie Hardwarekonfigurationen
-   Bereitstellen detaillierter Systemdaten, die Ihnen helfen können, die Grundursachen von Qualitätsproblemen zu identifizieren
-   Senken Ihrer Kosten durch Aufdecken von Problemen während der Entwicklung
-   Generieren von Vergleichen von Ergebnissen von verschiedenen Computern oder derselben Gruppe von Computern im Zeitverlauf durch Erstellen von Vergleichsdiagrammen aus mehreren Resultsets
-   Generieren von Feedback in einem standardisierten Format, mit dem Sie die Qualität Ihrer Produkte verbessern können

Wichtige Geschäftsziele können mit dem Assessment Toolkit erreicht werden:

-   **Messen & Vergleichen:** Sie können die Daten verwenden, um Komponenten (Software, Treiber oder beides) mit anderen ähnlichen Komponenten zu vergleichen, um Ihre Entscheidungsfindung, Empfehlungen und die Kennzeichnung von Wehen zu erleichtern.
-   **Verbessern der Qualität:** Sie können unabhängig oder mit beteiligten Partnern zusammenarbeiten, um eine Komponente (Software, Treiber oder beides) gemäß vordefinierten Qualitätskriterien zu erstellen.
-   **Nachverfolgen der Qualität**   Sie können einen Prozess zum effizienten Nachverfolgen der Qualität von Komponentenversionen erstellen und Regressionen nach jeder Iteration erkennen.

## <a name="usage-and-best-practices"></a>Verwendung und bewährte Methoden

Bewertungen sind eine Kombination aus XML- und Binärdateien, die einen bestimmten Satz von Zuständen auf einem Computer auslösen, die Aktivität messen und aufzeichnen und die aufgezeichneten Ergebnisse beibehalten. Ein Auftrag ist eine Sammlung von bewertungen und deren Einstellungen, die gleichzeitig auf einem Computer ausgeführt werden. Die Bewertungsplattform bietet die Infrastruktur für die konsistente Ausführung und Anzeige von Aufträgen, Bewertungen und Ergebnissen. Die Ergebnisse enthalten häufig Diagnose- und Korrekturinformationen, mit denen Sie Bereiche ermitteln können, die zusätzliche Untersuchungen und Korrekturmaßnahmen erfordern. Ihre Möglichkeiten:

-   Ausführen von Bewertungen für einen einzelnen Computer oder eine kleine Sammlung von Computern mit der **Windows Assessment Console** (Windows AC) <dl> Dieses Szenario richtet sich an Benutzer, die Leistungsmerkmale in einer oder mehreren verschiedenen Computerkonfigurationen anzeigen möchten. Windows AC ist eine grafische Benutzeroberfläche (GUI), die zum Gruppieren der Bewertungen, Erstellen eines Auftrags, Packen eines Auftrags, Ausführen des Auftrags und Verwalten der Auftragsergebnisse verwendet wird. Die Ergebnisse enthalten häufig empfohlene Aktionen.  
    </dl>
-   Run assessments against multiple computers in a lab environment with **Windows Assessment Services** (Windows AS) <dl> Dieses Szenario richtet sich in erster Linie an Benutzer, die eine Sammlung von qualitativen Bewertungen für eine vollständige Zeile von Desktops, Laptops oder Tabletcomputern in einer Entwicklungsumgebung durchführen möchten.  
    </dl>

Das Assessment Toolkit bietet folgende Features:

-   Eine einfache grafische Benutzeroberfläche (GUI) und Bewertungen, die verwendet werden können, um einen Computer ohne detaillierte technische Kenntnisse des Systems zu bewerten.
-   Bewertungsergebnisse, die in der Konsole oder Benutzeroberfläche angezeigt werden und häufig Empfehlungen enthalten, die Ihnen helfen, das System zu verbessern
-   Die Möglichkeit, einen vorkonfigurierten Auftrag mit einem Klick auszuführen
-   Vordefinierte Bewertungseinstellungen in jeder vorkonfigurierten Auftragsbewertung, sodass Sie einen Auftrag auf mehreren Computern ausführen und sicher sein können, dass die Ergebnisse vergleichbar sind
-   Aufträge, die angepasst werden können, um die bewertungen, die Sie verwenden möchten, und die Einstellungen, die Sie verwenden möchten, einzubeziehen
-   Befehlszeilensyntax der Bewertungsplattform für die Skripterstellung und Automatisierung von Aufträgen
-   Die Möglichkeit, einen Auftrag auszuführen, die Ergebnisse anzuzeigen, Korrekturschritte zur Verbesserung des Systems auszuführen, den Auftrag dann erneut auszuführen und die neuen Ergebnisse nebeneinander mit den alten Ergebnissen zu vergleichen, um zu sehen, wie sich das System verbessert hat.

Das Assessment Toolkit wird in der Regel in folgenden Szenarien verwendet:




| Szenario | BESCHREIBUNG | 
|----------|-------------|
| "Black box" | Führen Sie einen vordefinierten Auftrag aus, und untersuchen Sie die Ergebnisse auf ungewöhnliche Werte oder Anzeichen von Problemen mit Treibern, Speicherauslastung oder anderen Bereichen, die von den Bewertungen behandelt werden. | 
| Vergleichen von Ergebnissen | <ol><li>Führen Sie eine einzelne Bewertung mit den empfohlenen Einstellungen auf jedem Computer aus, auf dem ein unterstütztes Betriebssystem ausgeführt wird.</li><li>Verwenden Sie die Windows AC, um den Auftrag für die Ausführung auf einem anderen Computer zu packen.</li><li>Speichern Sie die Ergebnisse in einer Freigabe, damit Sie die Ergebnisse vergleichen können.</li><li>Vergleichen Sie die Ergebnisse eines beliebigen Windows Computers mit denen eines anderen unterstützten Betriebssystems, um Unterschiede zu identifizieren.</li></ol><br /> | 
| Bereinigen des Computers | Führen Sie Bewertungen auf einem bereinigten Computer aus, der nur das Betriebssystem enthält, um Baselinesystemergebnisse festzulegen. | 
| Computer mit hinzugefügter Hardware oder Softwarekomponenten | Fügen Sie dem sauberen Computersystem neue Hardware oder Software hinzu, und führen Sie dann die Bewertungen erneut aus, um die Ergebnisse mit den Ergebnissen des bereinigten Computers zu vergleichen. | 
| Erstellen von Bewertungen | Verwenden Sie öffentliche APIs, um eine Bewertung zu entwickeln oder zu erweitern, oder integrieren Sie Bewertungen in Ihre Tools und Infrastruktur. | 




 

Diese Bewertungen können verwendet werden:



| Bewertung                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorüberprüfung der Treiberzertifizierung          | Bei der **Vorvalidierungsbewertung** der Treiberzertifizierung wird überprüft, ob die Treiber auf einem ausgeführten Windows Betriebssystem für das Windows Certification Program qualifiziert sind. Die Ergebnisse enthalten Empfehlungen, die Sie bei der Behebung von Problemen unterstützen, die von der Bewertung gefunden werden, z. B. nicht signierte Treiber oder abgelaufene Signaturen.                                                                                                                                                                                                                                                            |
| Treiberüberprüfung                          | Bei der **Überprüfung des Treibers** wird überprüft, ob ein Offline-Windows Image oder ein ausgeführtes Windows Betriebssystem den richtigen Treibersatz enthält. Die Ergebnisse enthalten Empfehlungen, die Sie bei der Behebung von Problemen unterstützen, die von der Bewertung gefunden werden. Zu diesen Problemen können fehlende, doppelte, ältere oder unnötige Treiber gehören.                                                                                                                                                                                                                                         |
| Dateibehandlung                                | Die **Dateibehandlungsbewertung** bietet eine automatisierte Möglichkeit, allgemeine Dateivorgänge durchzuführen und Metriken zu erfassen. Die Metriken messen die Dauer und den Durchsatz, damit Sie besser verstehen können, wie gut ein Computer in Szenarien für die Dateiverarbeitung von Endbenutzern abschneidet. Die Dateibehandlungsbewertung verwendet eine Reihe von Workloads, um einen Benutzer zu simulieren, der Dateien und Ordner auf Clientsystemen kopiert, verschoben, komprimiert, dekomprimiert und löscht.                                                                                                                                       |
| Fotobehandlung                               | Die **Fotobehandlungsbewertung** misst die Computerleistung und Akkulaufzeit, indem ein Endbenutzer simuliert wird, der Fotos anzeigt und bearbeitet.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Internet Explorer Starten/Erstellen von Registerkarten          | Die **Internet Explorer Startleistungsbewertung** hilft bei der Identifizierung von Komponenten, die sich auf die Zeit auswirken können, die zum Starten Internet Explorer erforderlich ist. Die Bewertung misst die Zeit zum vollständigen Rendern einer leeren Seite, einschließlich der Ladezeit des IExplore.exe Prozesses und der Intervalle für die Frameerstellung und die Tabstopperstellung. Außerdem werden die Auswirkungen aller Erweiterungen, Add-Ins und Symbolleisten, die auf dem System installiert sind, misst. Die Netzwerk- oder Browserleistung wird nicht gemessen.                                                                                         |
| Ein/Aus                                       | Die Bewertung **"On/Off Transition"** misst die Leistung Windows 8 Leistungsszenarien "Start", "Standby" und "Ruhezustand".                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Internet Explorer Browserleistung       | Die Internet Explorer Bewertung der **Browserleistung** misst die Qualität der Browsererfahrung in Internet Explorer und wertet CPU- und Grafikhardwarefunktionen aus. Drei separate Browserworkloads werden bereitgestellt, um den Computer auf verschiedene Weise zu belastungen.                                                                                                                                                                                                                                                                                                  |
| Medientranscodierungsleistung                | Die **Videobewertung transcodieren** misst den Prozess der Änderung einer Videodatei in ein anderes Format oder eine andere Bitrate. Diese Bewertung führt eine Reihe von Transcodierungsvorgängen mit gängigen Eingabe- und Ausgabedateiformaten und -auflösungen aus.                                                                                                                                                                                                                                                                                                                                           |
| Windows Benutzeroberflächenleistung                       | Die **Windows-Benutzeroberflächenleistungsbewertung** wertet die Leistung einiger grundlegender Benutzeroberflächen innerhalb der Windows Benutzeroberfläche aus. Die Bewertung misst die Reaktionsfähigkeit und Renderingqualität, während die Bewertung Workloads durchsetzt, die Benutzeraktivitäten simulieren, z. B. die Suche und den Übergang von Windows Store App-Umgebung zum Desktop. Die Ergebnisse der Reaktionsfähigkeit werden in Millisekunden gemessen. Niedrige Zahlen bedeuten, dass der Computer schneller und reaktionsfähiger ist. Für das Rendering zeigen die Ergebnisse die Bildfrequenz und die Anzahl der auftretenden Störungen an. |
| Speicherbedarf                             | Sie können die **Speicherbedarfsbewertung** verwenden, um ein Basisbetriebssystemimage quantitativ mit einem anderen Betriebssystemimage zu vergleichen. Anschließend können Sie die spezifischen Komponenten identifizieren, die sich auf den Speicherbedarf des physischen Systems auswirken. Diese Komponenten können Treiber, Add-In-Apps, vorab geladene Softwarepakete und Antivirenprogramme umfassen.                                                                                                                                                                                                           |
| Leistung beim ersten Start                       | In **der Bewertung** der Ersten Startleistung werden Probleme identifiziert, die sich darauf auswirken, wie lange Windows starten und die Startbildschirm beim ersten Starten des Computers anzeigen. Die Ergebnisse helfen OEMs bei der Diagnose der Ursachen von Verzögerungen und bei der Bereitstellung von Empfehlungen zur Verbesserung der Benutzererfahrung.                                                                                                                                                                                                                                                                                      |
| Medienstreaming                              | Mit **der Bewertung der Leistung von Streamingmedien** können Sie die Leistung einer Computerkonfiguration bewerten, wenn Sie Medien mithilfe von Internet Explorer. Sie können die Bewertungsergebnisse verwenden, um die Streamingmedienerfahrung zu verstehen, zu vergleichen und zu verbessern.                                                                                                                                                                                                                                                                                                                 |
| WinSAT – umfassend                         | Die **Windows System Assessment (WinSAT)** wird verwendet, um die Leistung eines Computers in mehreren Systemkomponenten zu bewerten und zu verbessern, einschließlich CPU, Arbeitsspeicher, Datenträger und Grafiken. Die Ergebnisse der umfassenden WinSAT-Bewertung ausdrücken die Leistungsfähigkeit der Hardwarekonfiguration eines Computers in Zahlen. Höhere Bewertungen bedeuten im Allgemeinen, dass der bewertete Computer eine bessere und schnellere Leistung erzielt als ein Computer mit einer niedrigeren Bewertung.                                                                                                                                                        |
| Energieeffizienz                            | Der **Auftrag Energieeffizienz** bietet Ihnen eine automatisierte Möglichkeit, die Akkulaufzeit eines Computers zu bewerten. Mithilfe von Workloads führt der Auftrag Energieeffizienz auch Diagnosen durch, die bewerten, ob Systemkomponenten Energie nutzen, wenn sie sich im Leerlauf befinden sollten.                                                                                                                                                                                                                                                                                                               |
| MiniFilter-Einstellungen               | Die **MiniFilter-Diagnoseoption** wird in der Internet Explorer-Startleistungsbewertung, der Dateibehandlungsbewertung und der Startleistungsbewertung (Windows 8) ausgeführt. Wenn Sie diese Option innerhalb der Bewertungen auswählen, die die Diagnoseoption MiniFilter bieten, werden Metriken erstellt, mit denen Sie die Auswirkungen von MiniFilter-Vorgängen auf verschiedene Bewertungsszenarien bewerten können.                                                                                                                                                                                  |
| Leistung und Qualität des Windows Media Players | Die **Windows Media Player Leistungs- und Qualitätsbewertung** startet WMP und gibt mehrere Medienclips nacheinander wieder, um Leistungs- und Qualitätsmetriken im Zusammenhang mit der Medienwiedergabe zu erfassen.                                                                                                                                                                                                                                                                                                                                                                          |



 

Andere Tools wie das Windows Performance Toolkit sind im ADK enthalten. Diese Tools bieten detaillierte Informationen, mit denen Sie die System- und App-Leistung analysieren und nachverfolgen können. Weitere Informationen finden Sie weiter unten im Abschnitt Ressourcen.

## <a name="resources"></a>Ressourcen

**Video:**

-   [Channel9 BUILD ADK-Videos](https://channel9.msdn.com/Events/BUILD/BUILD2011?sort=status&direction=asc&term=&t=assessment+and+deployment+kit)

  
**Dokumentation:**

-   [Windows Assessment and Deployment Kit](/previous-versions/windows/hh825420(v=win.10))
-   [Technische Referenz zum Windows-Bewertungstoolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh825508(v=win.10))
-   [Bewertungsausführungsmodul](/previous-versions/windows/desktop/axe/axe-access-portal)
-   [Windows Leistungsanalyse](https://msdn.microsoft.com/performance/default.aspx)

  


 

