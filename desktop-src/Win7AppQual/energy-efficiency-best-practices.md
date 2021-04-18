---
description: .
ms.assetid: 355abd0e-928e-442e-a724-855d9dd946fc
title: Bewährte Methoden für die Energieeffizienz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a9980d199e2d95c6dbd01c642a1f00f45e584c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352577"
---
# <a name="best-practices-for-energy-efficiency"></a>Bewährte Methoden für die Energieeffizienz

## <a name="platform"></a>Plattform

 **Clients** – Windows XP Windows \| Vista \| Windows 7  

## <a name="description"></a>BESCHREIBUNG

Windows-basierte Laptops müssen die gesetzlichen Anforderungen an die Energieeffizienz erfüllen, wie z. b. die der USA Umweltschutzbehörde (EPA) Energy Star Program. Außerdem haben Umfragen ergeben, dass die Dauer der Dauer des Akkus länger dauert als die meisten Kunden, die in Laptops benötigt werden. Um Kundenanforderungen gerecht zu werden, müssen Windows-Laptops ständig in den folgenden Bereichen fortfahren:

-   Energieeffizienz in allen Verwendungs Szenarien, einschließlich Leerlauf, produktionsworkloads, DVD-und Medienwiedergabe und Branchen Benchmarks
-   Akku Lebensdauer für mobile PCs – für Hardwareplattformen und für Windows

Die Windows-Plattform ist äußerst zuverlässig und ermöglicht eine schnelle und leistungsfähige Leistung. Erweiterungen, die für mobile PC-Systeme bereitgestellt werden, wie z. b. Dienste, System Steuerungs Applets, Treiber und andere Software, können sich jedoch erheblich auf die Leistung, Zuverlässigkeit und Energieeffizienz auswirken.

Energieeffizienz ist ein komplexes Problem, bei dem Faktoren betroffen sind, die sich auf alle Elemente des PC-Ökosystems auswirken. Kleinere Verbesserungen in mehreren Szenarien können die Energieeffizienz verbessern, aber eine einzelne Anwendung, ein leistungsfähiges Gerät oder ein Feature mit schlechter Leistung kann den Energieverbrauch erheblich steigern.

Hardware und Geräte bilden die Grundlage für die Energieeffizienz. Anwendungs-und Dienst Software müssen jedoch auch effizient sein, damit das System eine optimale Akku Lebensdauer erzielen kann. Jede Softwarekomponente im System, einschließlich des Betriebssystems und der durch den Wert hinzugefügten Anwendungen und Dienste, muss den grundlegenden Effizienz Richtlinien entsprechen. Eine einzelne Anwendung oder ein fehlerhafter Dienst kann jegliche Energieeffizienz erzielen, die der neueste Prozessor, die Geräte oder die Platt Form Hardware erreicht hat. Ausführlichere Informationen zur Akku Lebensdauer und Energieeffizienz finden Sie im [Handbuch zur Akku Lebensdauer](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#).

Die wichtigsten Probleme und Komponenten, die sich auf die Akku Lebensdauer auf einem mobilen PC auswirken, sind folgende:

**Akku Merkmale**

-   Größe, Typ und Qualität der Akkukapazität wirken sich auf die Akku Lebensdauer aus
-   Je größer der Akku, desto größer das Netzteil.
-   Größere Akkus sind teurer und schwerer. Benutzer bevorzugen leichtere Systeme

**Hardwarekomponenten**

-   Häufigkeit und Tiefe der Hardware in niedrigere Energiezustände
-   Hardware Unterstützung von niedrigeren Energiezuständen
-   Treiber Optimierung für Energieeffizienz

**Betriebs System – gesteuerte Energie Verwaltung**

-   Effizienz von Windows-Code im Vergleich zur Auslastung im Leerlauf
-   Die Zusammenarbeit aller Komponenten mit Windows-gesteuerter Energie Verwaltung
-   Ordnungsgemäße Konfiguration des Betriebssystems zur Optimierung der Energie Verwaltung durch Energierichtlinien Einstellungen

**Anwendungs Software und-Dienste**

-   Effizienz von Anwendungen, Treibern und Diensten im Vergleich zum Leerlauf
-   Anwendungsebene der Anwendungen mit Windows – gesteuerte Energie Verwaltung
-   Software Gewährung des Systems oder der Geräte, die in den Energiespar Zustand "Leerlauf" eingegeben werden sollen

Eine einzelne Anwendung oder Dienst Komponente kann verhindern, dass ein System die optimale Akku Lebensdauer erkennt. Obwohl Windows viele Energie Konfigurationsoptionen bereitstellt, sind vorinstallierte Software-oder Energierichtlinien Einstellungen auf vielen Systemen nicht für die Host Hardwareplattform optimiert.

Eine gängige Methode zum Auswerten der Akku Lebensdauer von vorinstallierter Software besteht darin, den Stromverbrauch des Systems mit einer Neuinstallation von Windows im Vergleich zu einer Windows-Installation zu vergleichen, die zusätzliche Software und Dienste umfasst. Obwohl es sich bei einer Neuinstallation nicht um die typische Plattform handelt, die von OEMs an Kunden ausgeliefert wird, kann der Stromverbrauchs Vergleich einen Einblick in die Energieeffizienz der vorinstallierten Software bieten.

## <a name="best-practices"></a>Bewährte Methoden

Um sicherzustellen, dass Ihre Anwendung auf Windows-Plattformen optimiert ist, befolgen Sie die folgenden bewährten Methoden, wenn Sie Anwendungen oder Dienste entwerfen:

-   **Vermeiden Sie die Verwendung von periodischen Zeit Gebern mit hoher Auflösung.**

<dl> Verwenden von periodischen Zeit Gebern mit hoher Auflösung (<10 ms) reduces the efficiency of processor power-management technologies.  
</dl>

-   **In Leistungsoptimierungen investieren**

<dl> Jede Leistungsoptimierung ist eine Optimierung der Akku Lebensdauer. Durch die Reduzierung der erforderlichen Ressourcen, z. b. die Verwendung der geringeren Prozessorzeit oder der Datenträger Lesevorgänge bei der Batch Verarbeitung/Cluster Verarbeitung, kann sich die System Hardware in den Leerlauf versetzen und in den Modus  
</dl>

-   **Anpassen an die Benutzer Energierichtlinie**

<dl> Windows Vista und höher erleichtern es dem Benutzer, die Gesamtenergieeinsparung oder das Leistungsverhalten des Systems auszuwählen. Ihre Anwendung sollte auf Änderungen der Energierichtlinie reagieren und die Ressourcennutzung reduzieren oder die Leistung entsprechend steigern. Beispielsweise sollte eine Anwendung Hintergrund Aktivitäten wie z. b. Indizierung oder Systemüberprüfung deaktivieren, wenn der Benutzer einen Energiespar Energie Sparplan ausgewählt hat.  
</dl>

-   **Reduzieren der Ressourcennutzung, wenn sich das System im Akku Betrieb befindet**

<dl> Ihre Anwendung sollte den Ressourcenverbrauch reduzieren, z. b. die Häufigkeit des Aktualisierungs Intervalls, wenn sich das System in der Akkuleistung befindet.  
</dl>

-   **Nicht in der angezeigten Anzeige Rendering**

<dl> Die System Anzeige ist möglicherweise deaktiviert, um Energieeinsparungen zu erzielen. Die Anwendung sollte keine unnötige Grafik Rendering durchführen, wenn die Anzeige deaktiviert ist, da dadurch Systemressourcen und eine Stromversorgung verschwendet werden.  
</dl>

-   **Vermeiden von Abfragen und Gliederung in engen Schleifen**

<dl> Hohe Prozessorauslastung reduziert die Effektivität von Technologien zur Prozessor Energie Verwaltung, wie z. b. Prozessor-Leerlauf Zustände und Prozessor Leistungszustände.  
</dl>

-   **Verhindern, dass das System die Anzeige oder die Leerlaufzeit in den Standbymodus schaltet**

<dl> Die Anwendung sollte mit der SetThreadExecutionState-API über die SetThreadExecutionState-API verfügen. Das System sollte diese Anforderungen nur dann stellen, wenn kritische Vorgänge das System vor dem Ausschalten der Anzeige oder dem automatischen Wechsel in den Standbymodus verzögern müssen.  
</dl>

-   **Antworten auf häufige Ereignisse der Energie Verwaltung**

<dl> Die Anwendung sollte sich für allgemeine Energie Verwaltungs Ereignisse registrieren und auf diese reagieren, wie z. b. Änderungen an der System Energiequelle und Einschalt-und Ausschalten von Benachrichtigungen für die Anzeige.  
</dl>

-   **Aktivieren Sie die Debugprotokollierung nicht standardmäßig. Verwenden Sie stattdessen die Ereignis Ablauf Verfolgung für Windows.**

<dl> Eine regelmäßige Debugprotokollierung kann die Datenträger-Spin-Down  
</dl>

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Leitfaden zu den Akku lebenslösungen](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)
-   [Energieeffizienz Portal](https://www.microsoft.com/whdc/system/pnppwr/mobilepwr.mspx)
-   [Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)

 

 



