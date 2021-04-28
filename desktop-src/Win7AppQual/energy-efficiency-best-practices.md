---
description: Bewährte Methoden für die Energieeffizienz
ms.assetid: 355abd0e-928e-442e-a724-855d9dd946fc
title: Bewährte Methoden für die Energieeffizienz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d9a348b9df49531358de2db50acc0936622c36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088388"
---
# <a name="best-practices-for-energy-efficiency"></a>Bewährte Methoden für die Energieeffizienz

## <a name="platform"></a>Plattform

 **Clients** – Windows XP \| Windows Vista Windows \| 7  

## <a name="description"></a>BESCHREIBUNG

Windows-basierte Laptops müssen gesetzliche Anforderungen an die Energieeffizienz erfüllen, z. B. die anforderungen des Energy Star-Programms der USA Environmental Protection Agency (WPA). Darüber hinaus haben Umfragen ergeben, dass die längere Akkulaufzeit weiterhin das ist, was Die Verbraucher am meisten wünschen und in Laptops benötigen. Um die Verbraucheranforderungen zu erfüllen, müssen Windows-Laptops in den folgenden Bereichen kontinuierlich weiterentwickelt werden:

-   Energieeffizienz in allen Nutzungsszenarien, einschließlich Leerlauf, Produktivitätsworkloads, DVD- und Medienwiedergabe und Branchenbenchmarks
-   Akkulebensdauer mobiler PCs – für Hardwareplattformen und für Windows

Die Windows-Plattform ist äußerst zuverlässig und ermöglicht eine schnelle Ein- und Aus-Leistung. Erweiterungen, die mit mobilen PC-Systemen wie Diensten, Taskleisten-Applets, Treibern und anderer Software bereitgestellt werden, können sich jedoch erheblich auf Leistung, Zuverlässigkeit und Energieeffizienz auswirken.

Energieeffizienz ist ein komplexes Problem mit Faktoren, die von allen Elementen des PC-Ökosystems betroffen sind und sich darauf auswirken. Kleine Verbesserungen in mehreren Szenarien können die Energieeffizienz verbessern, aber eine einzelne schlecht leistungsfähige Anwendung, ein Gerät oder ein Systemfeature kann den Energieverbrauch erheblich erhöhen.

Hardware und Geräte bilden die Grundlage für die Energieeffizienz. Anwendungs- und Dienstsoftware muss jedoch auch effizient sein, damit das System eine optimale Akkulebensdauer erzielen kann. Jede Softwarekomponente im System, einschließlich des Betriebssystems und mehrwertige Anwendungen und Dienste, muss den grundlegenden Effizienzrichtlinien entsprechen. Eine einzelne fehlerhafte Anwendung oder ein einzelner Dienst kann jegliche Energieeffizienzsteigerungen beseitigen, die der neueste Prozessor, die neuesten Geräte oder die neueste Plattformhardware erzielt hat. Ausführlichere Informationen zur Akkulebensdauer und Energieeffizienz finden Sie im Handbuch zu Lösungen für die [Akkulebensdauer.](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)

Die Hauptprobleme und Komponenten, die sich auf die Akkulaufzeit auf einem mobilen PC auswirken, sind:

**Akkumerkmale**

-   Größe, Typ und Qualität der Akkukapazität wirken sich auf die Akkulebensdauer aus
-   Je größer der Akku, desto größer die Stromversorgung
-   Größere Akkus sind teurer und umfangreicher. Benutzer bevorzugen einfachere Systeme

**Hardwarekomponenten**

-   Häufigkeit und Tiefe, mit der Hardware in niedrigere Leistungszustände gelangen kann
-   Hardwareunterstützung für niedrigere Leistungszustände
-   Treiberoptimierung für Energieeffizienz

**Vom Betriebssystem gesteuerte Energieverwaltung**

-   Effizienz von Windows-Code während einer Auslastung im Vergleich zu im Leerlauf
-   Zusammenarbeitsebene aller Komponenten mit windowsgesteuerter Energieverwaltung
-   Ordnungsgemäße Konfiguration des Betriebssystems zur Optimierung der Energieverwaltung durch Energierichtlinieneinstellungen

**Anwendungssoftware und -dienste**

-   Effizienz von Anwendungen, Treibern und Diensten bei einer Last im Vergleich zum Leerlauf
-   Zusammenarbeitsebene von Anwendungen mit windowsgesteuerter Energieverwaltung
-   Softwarezutritt des Systems oder der Geräte in den Leerlaufzustand mit geringer Leistung

Eine einzelne Anwendung oder Dienstkomponente kann verhindern, dass ein System eine optimale Akkulaufzeit realisiert. Obwohl Windows viele Energiekonfigurationsoptionen bietet, sind vorinstallierte Software- oder Energierichtlinieneinstellungen auf vielen Systemen nicht für die Hosthardwareplattform optimiert.

Eine gängige Methode zum Auswerten der Auswirkungen vorinstallierter Software auf die Akkulebensdauer ist der Vergleich des Energieverbrauchs des Systems mit einer Neuinstallation von Windows im Vergleich zu einer Windows-Installation, die Mehrwertsoftware und -dienste umfasst. Obwohl eine Neuinstallation nicht die typische Plattform darstellt, die OEMs an Kunden liefern, kann der Vergleich des Stromverbrauchs Einblicke in die Energieeffizienz von vorinstallierten Software bieten.

## <a name="best-practices"></a>Bewährte Methoden

Um sicherzustellen, dass Ihre Anwendung auf Windows-Plattformen optimiert ist, befolgen Sie beim Entwerfen von Anwendungen oder Diensten die folgenden bewährten Methoden:

-   **Vermeiden der Verwendung von periodischen Zeitgebern mit hoher Auflösung**

<dl> Verwenden von periodischen Zeitgebern mit hoher Auflösung (<10 ms) reduces the efficiency of processor power-management technologies.  
</dl>

-   **Investitionen in Leistungsoptimierungen**

<dl> Jede Leistungsoptimierung ist eine Optimierung der Akkulebensdauer. Reduzierung der erforderlichen Ressourcen, z. B. durch weniger Prozessorzeit oder Batchverarbeitung/Clustering von Datenträgerlesedaten, ermöglicht es, dass die Systemhardware in den Leerlauf versetzt wird und in den Energiesparmodus versetzt wird.  
</dl>

-   **Anpassen an die Benutzerleistungsrichtlinie**

<dl> Windows Vista und höher erleichtern dem Benutzer die Auswahl des gesamten Energiespar- oder Leistungsverhaltens des Systems. Ihre Anwendung sollte auf Änderungen in der Energierichtlinie reagieren und die Ressourcennutzung reduzieren oder die Leistung entsprechend erhöhen. Beispielsweise sollte eine Anwendung Hintergrundaktivitäten wie Indizierung oder Systemüberprüfung deaktivieren, wenn der Benutzer einen Energiesparplan ausgewählt hat.  
</dl>

-   **Reduzieren des Ressourcenverbrauchs, wenn das System im Akkubetrieb ist**

<dl> Ihre Anwendung sollte die Ressourcennutzung reduzieren , z. B. die Aktualisierungshäufigkeit im Hintergrund, wenn das System im Akkubetrieb ist.  
</dl>

-   **Nicht in der Anzeige rendern, wenn sie deaktiviert ist**

<dl> Die Systemanzeige kann aus Gründen der Stromeinsparung deaktiviert sein. Ihre Anwendung sollte kein unnötiges Grafikrendering durchführen, wenn die Anzeige ausgeschaltet ist, da dadurch Systemressourcen und Energie verschwendet werden.  
</dl>

-   **Vermeiden von Abruf und Spinnen in engen Schleifen**

<dl> Eine hohe Prozessorauslastung reduziert die Effektivität von Technologien zur Prozessorleistungsverwaltung, z. B. Prozessor-Leerlaufzustände und Prozessorleistungszustände.  
</dl>

-   **Verhindern Sie nicht, dass das System die Anzeige ausschalten oder in den Ruhezustand versetzt wird.**

<dl> Ihre Anwendung sollte mit der SetThreadExecutionState-API mit vorsichtsvollen Power Requests vorgehen. Das System sollte diese Anforderungen nur stellen, wenn kritische Vorgänge das System am Ausschalten der Anzeige oder am automatischen Eintritt in den Ruhezustand verzögern müssen.  
</dl>

-   **Reagieren auf allgemeine Energieverwaltungsereignisse**

<dl> Ihre Anwendung sollte sich für allgemeine Energieverwaltungsereignisse registrieren und darauf reagieren, z. B. Änderungen an der Systemstromquelle und Ein- und Ausschalten-Benachrichtigungen für die Anzeige.  
</dl>

-   **Aktivieren Sie die Debugprotokollierung nicht standardmäßig. Verwenden Sie stattdessen die Ereignisablaufverfolgung für Windows.**

<dl> Die regelmäßige Debugprotokollierung kann das Herunterspinnen von Datenträgern verhindern.  
</dl>

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Leitfaden für Akkulebensdauerlösungen](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)
-   [Energieeffizienzportal](https://www.microsoft.com/whdc/system/pnppwr/mobilepwr.mspx)
-   [Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)

 

 



