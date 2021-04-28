---
description: 'Benutzeroberfläche: Hohe DPI-Werte'
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: 'Benutzeroberfläche: Hohe DPI-Werte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118b566d35f753a77f6cfd9706c2e69819f3fbaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116068"
---
# <a name="user-interface---high-dpi-awareness"></a>Benutzeroberfläche: Hohe DPI-Werte

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients** : Windows XP \| Windows Vista Windows \| 7  

## <a name="feature-impact"></a>Auswirkungen auf Das Feature

**Schweregrad –** Mittel  
**Häufigkeit** – Mittel  

## <a name="description"></a>BESCHREIBUNG

Das Ziel besteht darin, Endbenutzer zu ermutigen, ihre Anzeigen auf eine native Auflösung festzulegen und DPI anstelle der Bildschirmauflösung zu verwenden, um die Größe des angezeigten Texts und der Bilder zu ändern. Windows 7 kann einen Standard-DPI auf Neuinstallationen auf Computern automatisch erkennen und konfigurieren, die von ihren OEMs mithilfe von DPI-Einstellungen konfiguriert wurden. Es gibt Tools, mit denen Sie Anwendungen entwerfen können, die hohe DPI-Werte unterstützen, um die lesbarsten Ergebnisse sicherzustellen.

Windows 7 wurde um zwei neue Features mit hohem DPI-Anteil erweitert:

-   DPI-Einstellung pro Benutzer (bisher pro Computer)
-   DPI ohne Neustart ändern (Abmeldung/Anmeldung ist weiterhin erforderlich)

## <a name="manifestation-of-impact"></a>Wirkungserz weiter

Anwendungen, die den hohen DPI-Fall nicht verarbeiten, weisen wahrscheinlich visuelle Artefakte auf, z. B.:

-   Beschneiden der Benutzeroberfläche oder des Texts durch andere Benutzeroberflächenelemente
-   Inkonsistente Schriftgrade
-   Off-Screen-UIs
-   Weichzeichnen von Text oder Benutzeroberfläche
-   Fehlerhafte Drag &amp; Drop-Eingaben oder andere Eingaben
-   Rendering von DX-Vollbildanwendungen teilweise außerhalb des Bildschirms

## <a name="solution"></a>Lösung

So sorgen Sie für DPI-fähige Anwendungen:

1.  Führen Sie einen funktionstüchtigen Testlauf auf hoher Ebene durch, einschließlich Installation und Deinstallation in den folgenden Einstellungen:

    | Einstellung                                              | Worauf Sie achten müssen                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1024 x 768 bei 120 DPI (125 % Skalierung)                    | Dies ist eine effektive Auflösung von ca. 800 x 600. Suchen Sie daher nach Benutzeroberflächenproblemen, die vom Bildschirm abgeschnitten wurden. Suchen Sie auch nach pixilierten Bitmaps & Symbolen.                         |
    | 1600 x 1200 @144 DPI (150 % Skalierung)                    | Unscharfe Benutzeroberfläche. Stellen Sie sicher, dass alle Mausvorgänge funktionieren, insbesondere drag & Drop-Vorgänge. Überprüfen Sie außerdem, ob die Vollbildmodi ordnungsgemäß funktionieren.                                     |
    | 1600x1200 @ 144 DPI mit deaktivierter DPI-Virtualisierung | Häufig werden Schaltflächen und die Benutzeroberfläche nicht im Verhältnis zu größerem Text skaliert& es zu erheblichen Textausschneidefechen kommt. Suchen Sie im Allgemeinen nach Layoutproblemen & pixilierten Bitmaten & Symbolen. |

    

     

2.  Notieren Sie sich alle gefundenen Probleme, einschließlich Standort, Bildschirmauflösung und DPI-Einstellungen, sowie das Verhalten der Anwendung in den anderen DPI-/Auflösungskonfigurationen aus Vollständigkeits-
3.  Überprüfen Sie jedes Problem mit den allgemeinen DPI-Codierungsproblemen.
4.  Bewerten der Kosten für die vollständige DPI-Wertung der Anwendung
5.  Erstellen Sie eine Liste der erforderlichen Objekte mit hohem DPI-Werte (z. B. Schaltflächen, Symbole).
6.  Arbeiten Sie die Liste der in Schritt 1 gefundenen DPI-Probleme durch, und beheben Sie sie.
7.  Integrieren der neuen Ressourcen aus Schritt 5
8.  Deklarieren Der DPI-bewusste Anwendung

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Nutzbarkeitstests

Führen Sie die DPI Awareness-Bewertung erneut aus, und überprüfen Sie, ob die Probleme behoben wurden.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Desktopanwendungsentwicklung mit hohem DPI-Anteil unter Windows](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   **Kontakt für technische Fragen:**<disup@microsoft.com>

 

 
