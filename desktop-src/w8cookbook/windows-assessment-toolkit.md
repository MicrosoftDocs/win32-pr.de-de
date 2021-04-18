---
title: Windows-Bewertungstoolkit
description: Windows-Bewertungstoolkit
ms.assetid: 9D0A4F42-F027-4032-8297-045937BD2B6E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38d75aa02757acb54083e005d67a10e0fa42efec
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "106337885"
---
# <a name="windows-assessment-toolkit"></a>Windows-Bewertungstoolkit

## <a name="platforms"></a>Plattformen

**Clients** -Windows 7 \| Windows 8  

## <a name="description"></a>BESCHREIBUNG

Das Windows Assessment Toolkit und das Windows Performance Toolkit bilden das Windows Assessment and Deployment Kit (ADK). Diese stellen eine umfassende Lösung zum Auswerten der gesamten Computerleistung und zur Automatisierung der Bereitstellung des Windows-Betriebssystems auf neuen Computern bereit.

Dieses Thema konzentriert sich auf das **Assessment Toolkit**. Die Bewertungsergebnisse werden verwendet, um potenzielle Probleme zu diagnostizieren, sodass die von Ihnen entwickelte Hardware und Software beide reaktionsfähig sind und eine minimale Auswirkung auf die Akku Lebensdauer, die Startleistung und das Herunterfahren haben. Die gleichen Bewertungen sind für OEM-Partner, ISV/IHV-Partner, Enthusiasten und andere Mitglieder der Community verfügbar, um ein gemeinsames Framework zum Messen, vergleichen und Überprüfen von Qualitätsaspekten einzurichten.

Mithilfe der Windows Assessment-Tools können Sie verschiedene Aspekte der Leistung in einer Vielzahl von Szenarios Messen, von der Startzeit bis hin zur Akku Lebensleistung bis hin zu Video Streaming mit hoher Definition. Anhand von Bewertungen können potenzielle Probleme, ein inkonsistentes Verhalten und die zu untersuchenden Bereiche aufgezeigt werden.

In früheren Windows-Versionen waren mehrere Tools zum Messen der Qualität verfügbar, einschließlich der Velocity-Test Sammlung (VTS/Vos), der grundlegenden Quality Tool Suite (fqts) und der System Leistung und Leistungs Tools Suite (sppts). Das Assessment Toolkit kombiniert die Funktionalität dieser Leistungs Diagnosetools zu einem integrierten Satz von Tools, der einfacher zu verwenden ist und breitere, aussagekräftigere Ergebnisse bietet.

Das Windows Assessment Toolkit maximiert die Zufriedenheit der Consumer durch:

-   Unterstützung der Bewertung der Gesamtleistung von Fenstern, Mehrwert Software und-Treibern und Hardware Konfigurationen
-   Bereitstellen detaillierter Systemdaten, die Ihnen helfen können, die Ursachen von Qualitätsproblemen zu identifizieren
-   Senken der Kosten durch Offenlegen von Problemen während der Entwicklung
-   Erstellen von Vergleichen der Ergebnisse von verschiedenen Computern oder derselben Gruppe von Computern im Zeitverlauf durch das Erstellen von Vergleichs Diagrammen aus mehreren Resultsets
-   Erstellen von Feedback in einem standardisierten Format, das Sie verwenden können, um die Qualität ihrer Produkte zu verbessern

Wichtige Geschäftsziele können mithilfe des Assessment Toolkit erreicht werden:

-   **Messen & vergleichen** : Sie können die Daten verwenden, um Komponenten (Software, Treiber oder beides) mit anderen ähnlichen Komponenten zu vergleichen, um ihre Entscheidungsfindung, Empfehlungen und Wettbewerbs-Bench-Markierung zu vereinfachen.
-   **Qualität verbessern** : Sie können unabhängig oder mit beteiligten Partnern arbeiten, um eine Komponente (Software, Treiber oder beides) gemäß den vordefinierten Qualitätskriterien zu erstellen.
-   **Qualität nachverfolgen**   Sie können einen Prozess für die effiziente Nachverfolgung der Qualität von Komponenten Versionen und das Erkennen von Regressionen nach jeder Iterationen erstellen.

## <a name="usage-and-best-practices"></a>Verwendung und bewährte Methoden

Bei den Bewertungen handelt es sich um eine Kombination aus XML-und Binärdateien, die auf einem Computer einen bestimmten Satz von Zuständen auslösen, die Aktivität messen und aufzeichnen und die aufgezeichneten Ergebnisse erhalten. Ein Auftrag ist eine Sammlung von einer oder mehreren Bewertungen und deren Einstellungen, die gleichzeitig auf einem Computer ausgeführt werden. Die Bewertungsplattform stellt die Infrastruktur für das konsistente ausführen und Anzeigen von Aufträgen, BEWERTUNGEN und Ergebnissen bereit. Die Ergebnisse enthalten häufig Diagnose-und Wiederherstellungs Informationen, mit deren Hilfe Sie Bereiche ermitteln können, die zusätzliche Untersuchungen und Korrekturmaßnahmen erfordern. Ihre Möglichkeiten:

-   Ausführen von Bewertungen für einen einzelnen Computer oder eine kleine Sammlung von Computern mit der **Windows Assessment Console** (Windows AC) <dl> Dieses Szenario ist für Benutzer gedacht, die Leistungsmerkmale für eine oder mehrere verschiedene Computerkonfigurationen anzeigen möchten. Windows AC ist eine grafische Benutzeroberfläche (GUI), die verwendet wird, um die Bewertungen zu gruppieren, einen Auftrag zu erstellen, einen Auftrag zu verpacken, den Auftrag auszuführen und die Auftrags Ergebnisse zu verwalten. Zu den Ergebnissen zählen häufig Empfohlene Aktionen.  
    </dl>
-   Run assessments against multiple computers in a lab environment with **Windows Assessment Services** (Windows AS) <dl> Dieses Szenario richtet sich hauptsächlich an Benutzer, die eine Reihe von qualitativen Bewertungen für eine komplette Reihe von Desktops, Laptops oder Tablet PCs in einer Entwicklungsumgebung ausführen möchten.  
    </dl>

Das Assessment Toolkit bietet folgende Features:

-   Eine einfache grafische Benutzeroberfläche (GUI) und Bewertungen, die zur Bewertung eines Computers ohne umfassende technische Kenntnisse des Systems verwendet werden können
-   Bewertungsergebnisse, die in der-Konsole oder der Benutzeroberfläche angezeigt werden und häufig Empfehlungen enthalten, die Ihnen helfen, das System zu verbessern
-   Die Möglichkeit, einen vorkonfigurierten Auftrag mit einem Mausklick auszuführen.
-   Vordefinierte Bewertungs Einstellungen in jeder vorkonfigurierten Auftrags Bewertung, sodass Sie einen Auftrag auf mehreren Computern ausführen und sicher sein können, dass die Ergebnisse vergleichbar sind
-   Aufträge, die angepasst werden können, um die zu verwendenden Bewertungen und die gewünschten Einstellungen einzuschließen
-   Bewertungsplattform-Befehlszeilen Syntax für die Skripterstellung und Automatisierung von Aufträgen
-   Die Möglichkeit zum Ausführen eines Auftrags, zum Anzeigen der Ergebnisse, zum Ausführen von Wiederherstellungs Schritten, um das System zu verbessern, und zum anschließenden erneuten Ausführen des Auftrags und Vergleichen der neuen Ergebnisse mit den alten Ergebnissen, um zu sehen, wie sich das System verbessert hat

Das Assessment Toolkit wird in der Regel in folgenden Szenarien verwendet:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Szenario</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Schwarzes Feld&quot;</td>
<td>Führen Sie einen vordefinierten Auftrag aus, und untersuchen Sie die Ergebnisse auf ungewöhnliche Werte oder Anzeichen für Probleme mit Treibern, der Speicherauslastung oder anderen Bereichen, die von den Bewertungen behandelt werden.</td>
</tr>
<tr class="even">
<td>Vergleichen von Ergebnissen</td>
<td><ol>
<li>Führen Sie eine einzelne Bewertung mithilfe der empfohlenen Einstellungen auf allen Computern aus, auf denen ein unterstütztes Betriebssystem ausgeführt wird.</li>
<li>Verwenden Sie Windows AC, um den Auftrag zum Ausführen auf einem anderen Computer zu verpacken.</li>
<li>Speichern Sie die Ergebnisse in einer Freigabe, damit Sie die Ergebnisse vergleichen können.</li>
<li>Vergleichen Sie die Ergebnisse von einem beliebigen Windows-Computer mit denen eines beliebigen anderen unterstützten Betriebssystems, um Unterschiede zu ermitteln.</li>
</ol>
<br/></td>
</tr>
<tr class="odd">
<td>Computer bereinigen</td>
<td>Führen Sie Bewertungen auf einem sauberen Computer aus, der nur das Betriebssystem enthält, um grundlegende System Ergebnisse zu erzielen.</td>
</tr>
<tr class="even">
<td>Computer mit hinzugefügter Hardware oder Softwarekomponenten</td>
<td>Fügen Sie dem System für saubere Computer neue Hardware oder Software hinzu, und führen Sie dann die Bewertungen erneut aus, um die Ergebnisse mit den Ergebnissen für saubere Computer zu vergleichen.</td>
</tr>
<tr class="odd">
<td>Erstellen von Bewertungen</td>
<td>Verwenden Sie öffentliche APIs, um eine Bewertung zu entwickeln oder zu erweitern, oder integrieren Sie Bewertungen in ihre Tools und ihre Infrastruktur.</td>
</tr>
</tbody>
</table>



 

Diese Bewertungen können verwendet werden:



| Bewertung                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorab Validierung der Treiber Zertifizierung          | Die Bewertung der vorab Überprüfung der **Treiber Zertifizierung** überprüft, ob die Treiber auf einem laufenden Windows-Betriebssystem für das Windows-Zertifizierungsprogramm qualifiziert sind. Die Ergebnisse enthalten Empfehlungen, mit denen Sie Probleme beheben können, die von der Bewertung gefunden werden, z. b. nicht signierte Treiber oder abgelaufene Signaturen.                                                                                                                                                                                                                                                            |
| Treiberüberprüfung                          | Bei der über **Prüfung der Treiber Überprüfung** wird überprüft, ob ein Offline-Windows-Abbild oder ein Betriebssystem unter Windows die richtigen Treiber Gruppe enthält. Die Ergebnisse enthalten Empfehlungen, mit deren Hilfe Sie Probleme beheben können, die von der Bewertung gefunden werden. Diese Probleme können fehlende, doppelte, ältere oder unnötige Treiber umfassen.                                                                                                                                                                                                                                         |
| Dateibehandlung                                | Die **Datei Behandlungs** Bewertung bietet eine automatisierte Möglichkeit zum Ausführen allgemeiner Datei Vorgänge und zum Erfassen von Metriken. Die Metriken Messen Dauer und Durchsatz, damit Sie besser verstehen können, wie gut ein Computer in Szenarios für die Datei Behandlung durch Endbenutzer arbeitet. Die Datei Behandlungs Bewertung verwendet einen Satz von Arbeits Auslastungen, um einen Benutzer zu simulieren, der Dateien und Ordner auf Client Systemen kopiert, verschiebt, komprimiert, komprimiert und löscht.                                                                                                                                       |
| Foto Behandlung                               | Die Bewertung der **Fotobearbeitung** misst die Leistung und die Akku Lebensdauer von Computern, indem ein Endbenutzer simuliert wird, der Fotos anzeigen und bearbeiten soll.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Internet Explorer Launch/Tab-Taste erstellen          | Mit der Leistungsbewertung für den **Internet Explorer-Start** können Sie Komponenten identifizieren, die sich auf die zum Starten von Internet Explorer benötigte Zeit auswirken können Die Bewertung misst die Zeit zum vollständigen Rendering einer leeren Seite, einschließlich der Ladezeit des IExplore.exe Prozesses sowie der Intervalle für Frame Erstellung und Registerkarten Erstellung. Außerdem werden die Auswirkungen aller Erweiterungen, Add-Ins und Symbolleisten gemessen, die auf dem System installiert sind. Die Leistung von Netzwerk-oder Browsen wird nicht gemessen.                                                                                         |
| Ein/Aus                                       | **Mit der on/off-Übergangs** Bewertung wird die Leistung von Windows 8-Leistungs Szenarios für Start, Standby und Ruhe Zustands gemessen.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Internet Explorer-Browser Leistung       | Die Leistungsbewertung für das durch **Suchen von Internet Explorer** misst die Qualität der Browser Darstellung in Internet Explorer und wertet CPU-und grafische Hardwarefunktionen aus. Es werden drei separate browserworkloads bereitgestellt, um den Computer auf unterschiedliche Weise zu belasten.                                                                                                                                                                                                                                                                                                  |
| Medientranscodierungsleistung                | Die **transcode-Video** Bewertung misst den Prozess der Änderung einer Video Datei in ein anderes Format oder eine andere Bitrate. Diese Bewertung führt eine Reihe von transcodieren-Vorgängen mit allgemeinen Eingabe-und Ausgabedatei Formaten und Auflösungen aus.                                                                                                                                                                                                                                                                                                                                           |
| Windows-Benutzeroberflächen Leistung                       | Die **Leistungs** Bewertung der Windows-Benutzeroberfläche wertet die Leistung einiger grundlegender Erfahrungen innerhalb der Windows-Benutzeroberfläche aus. Bei der Bewertung werden Reaktionsfähigkeit und renderingqualität gemessen, während die Bewertung Workloads ausführt, die Benutzeraktivitäten simulieren, z. b. die Verwendung von suchen und wechseln von der Windows Store-App-Umgebung zum Desktop Die Reaktionsfähigkeit der Ergebnisse wird in Millisekunden gemessen. Niedrige Anzahl bedeutet, dass der Computer schneller und reaktionsfähiger ist. Zum Rendern zeigen die Ergebnisse die Framerate und die Anzahl der auftretenden Fehler an. |
| Speicherbedarf                             | Mithilfe der Bewertung für den **Speicherbedarf** können Sie ein Baseline-Betriebssystem Abbild mit einem anderen Betriebssystem Abbild in quantitativer Art vergleichen. Anschließend können Sie die spezifischen Komponenten identifizieren, die sich auf den Speicherbedarf des physischen Systems auswirken. Diese Komponenten können Treiber, Add-in-apps, vorab geladene Softwarepakete und Antivirenprogramme enthalten.                                                                                                                                                                                                           |
| Erste Startleistung                       | Die **erste Start Leistungs** Bewertung identifiziert Probleme, die sich darauf auswirken, wie lange Windows gestartet werden muss, und zeigt den Start Bildschirm an, wenn der Computer zum ersten Mal gestartet wird. Die Ergebnisse helfen OEMs bei der Diagnose von Verzögerungen und bieten Empfehlungen zur Verbesserung der Leistung.                                                                                                                                                                                                                                                                                      |
| Medien Streaming                              | Mithilfe der Leistungsbewertung für **Streamingmedien** können Sie die Leistung einer Computerkonfiguration beurteilen, wenn Sie Medien mithilfe von Internet Explorer streamen. Mit den Bewertungsergebnissen können Sie das Streaming von Medien verstehen, vergleichen und verbessern.                                                                                                                                                                                                                                                                                                                 |
| WinSAT-umfassend                         | Die **Windows-Systembewertung (WinSAT)** wird verwendet, um die Leistung eines Computers in mehreren System Komponenten, einschließlich CPU, Arbeitsspeicher, Datenträger und Grafiken, zu bewerten und zu verbessern. Durch die umfassenden Ergebnisse der WinSAT-Bewertung wird die Fähigkeit der Hardwarekonfiguration eines Computers in Zahlen ausgedrückt. Höhere Ergebnisse bedeuten im Allgemeinen, dass der bewertete Computer besser und schneller als ein Computer mit niedrigerer Bewertung funktioniert.                                                                                                                                                        |
| Energieeffizienz                            | Der **Energieeffizienz** Auftrag bietet eine automatisierte Möglichkeit, um die Akku Lebensdauer eines Computers zu bewerten. Mithilfe von Arbeits Auslastungen führt der Energieeffizienz Auftrag auch Diagnose durch, die bewerten, ob Systemkomponenten Strom verwenden, wenn Sie sich im Leerlauf befinden.                                                                                                                                                                                                                                                                                                               |
| Mini Filter-Diagnose Einstellungen               | Die **Minifilter-Diagnose** Option wird innerhalb der Leistungsbewertung für den Internet Explorer, die Datei Behandlungs Bewertung und die Start Leistungsbewertung (Windows 8) ausgeführt. Das Auswählen dieser Option in den Bewertungen, die die Mini Filter-Diagnose Option bieten, erzeugt Metriken, mit denen Sie die Auswirkungen von Minifilter-Vorgängen auf verschiedene Bewertungs Szenarien auswerten können.                                                                                                                                                                                  |
| Leistung und Qualität des Windows Media Players | Mit der **Leistungs-und Qualitätsbewertung von Windows Media Player** wird WMP gestartet, und es werden mehrere Medienclips nacheinander abgespielt, um Leistungs-und Qualitäts Metriken in Bezug auf die Medienwiedergabe aufzuzeichnen.                                                                                                                                                                                                                                                                                                                                                                          |



 

Andere Tools, wie z. b. das Windows Performance Toolkit, sind im ADK enthalten. Diese Tools bieten detaillierte Informationen, mit denen Sie die System-und App-Leistung analysieren und verfolgen können. Weitere Informationen finden Sie im Abschnitt Ressourcen weiter unten.

## <a name="resources"></a>Ressourcen

**Video**

-   [Channel9 Erstellen von ADK-Videos](https://channel9.msdn.com/Events/BUILD/BUILD2011?sort=status&direction=asc&term=&t=assessment+and+deployment+kit)

  
**Dokumentation**

-   [Windows Assessment and Deployment Kit](/previous-versions/windows/hh825420(v=win.10))
-   [Technische Referenz zum Windows-Bewertungstoolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh825508(v=win.10))
-   [Bewertungsausführungsmodul](/previous-versions/windows/desktop/axe/axe-access-portal)
-   [Windows-Leistungsanalyse](https://msdn.microsoft.com/performance/default.aspx)

  


 

