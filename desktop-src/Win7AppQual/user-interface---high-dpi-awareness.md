---
description: 'Benutzeroberfläche: Hohe DPI-Werte'
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: 'Benutzeroberfläche: Hohe DPI-Werte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52c2bb42ad2c54fc1d23e44edf54e4bc88f8ab40a3f3a04f9dbc57b484b55173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994580"
---
# <a name="user-interface---high-dpi-awareness"></a>Benutzeroberfläche: Hohe DPI-Werte

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients** – Windows XP \| Windows Vista \| Windows 7  

## <a name="feature-impact"></a>Auswirkungen auf Features

**Schweregrad –** Mittel  
**Frequency** - Medium  

## <a name="description"></a>BESCHREIBUNG

Das Ziel besteht darin, Endbenutzer zu ermutigen, ihre Anzeigen auf eine native Auflösung festzulegen und DPI anstelle der Bildschirmauflösung zu verwenden, um die Größe des angezeigten Texts und der Bilder zu ändern. Windows 7 kann einen Standard-DPI bei Neuinstallationen auf Computern automatisch erkennen und konfigurieren, die von ihren OEMs mithilfe von DPI-Einstellungen konfiguriert wurden. Es gibt Tools, mit denen Sie Anwendungen entwerfen können, die hohe DPI-Werte unterstützen, um die lesbarsten Ergebnisse sicherzustellen.

Wir haben Windows 7 zwei neue Features mit hohem DPI-Anteil hinzugefügt:

-   DPI-Einstellung pro Benutzer (bisher pro Computer)
-   DPI ohne Neustart ändern (Abmeldung/Anmeldung ist weiterhin erforderlich)

## <a name="manifestation-of-impact"></a>Auswirkungen

Anwendungen, die den hohen DPI-Fall nicht verarbeiten, weisen wahrscheinlich visuelle Artefakte auf, z. B.:

-   Beschneiden der Benutzeroberfläche oder des Texts durch andere Benutzeroberflächenelemente
-   Inkonsistente Schriftgrade
-   Off-Screen-UIs
-   Weichzeichnen von Text oder Benutzeroberfläche
-   Fehlerhafte Drag & Drop-Eingaben oder andere Eingaben
-   Rendering von DX-Vollbildanwendungen teilweise außerhalb des Bildschirms

## <a name="solution"></a>Lösung

So sorgen Sie für DPI-fähige Anwendungen:

1.  Führen Sie einen funktionsbezogenen Testdurchlauf auf hoher Ebene durch, einschließlich der Installation und Deinstallation mit den folgenden Einstellungen:

    | Einstellung                                              | Suchen nach                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1024 x 768 mit 120 DPI (Skalierung von 125 %)                    | Dies ist eine effektive Lösung von ca. 800 x 600. Suchen Sie also nach Problemen mit der Benutzeroberfläche, die vom Bildschirm abgeschnitten wurden, oder nach Layoutproblemen. Suchen Sie auch nach pixilatierten Bitmaps & Symbolen.                         |
    | 1600 x 1200 @144 DPI (Skalierung von 150 %)                    | Unscharfe Benutzeroberfläche. Vergewissern Sie sich, dass alle Mausvorgänge funktionieren, insbesondere drag & Drop-Vorgänge. Überprüfen Sie auch, ob die Vollbildmodi ordnungsgemäß funktionieren.                                     |
    | 1600x1200 @ 144 DPI mit deaktivierter DPI-Virtualisierung | Häufig werden Schaltflächen und die Benutzeroberfläche nicht in Bezug auf größeren Text skaliert, & es zu erheblichen Textausschnitten kommt. Suchen Sie im Allgemeinen nach Layoutproblemen & pixilatierten Bitmatten & Symbolen. |

    

     

2.  Notieren Sie sich alle gefundenen Probleme, einschließlich Speicherort, Bildschirmauflösung und DPI-Einstellungen, sowie das Verhalten der Anwendung in den anderen DPI-/Auflösungskonfigurationen zur Vollständigkeit.
3.  Überprüfen Sie jedes Problem anhand der allgemeinen DPI-Codierungsprobleme.
4.  Bewerten der Kosten für die vollständige DPI-Fähige Nutzung der Anwendung
5.  Erstellen Sie eine Liste der erforderlichen Objekte mit hohem DPI-Wert (z. B. Schaltflächen, Symbole).
6.  Durcharbeiten und Beheben der Liste der in Schritt 1 gefundenen DPI-Probleme
7.  Integrieren der neuen Ressourcen aus Schritt 5
8.  Deklarieren der DPI-fähigen Anwendungsdaten

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests

Führen Sie die DPI Awareness-Bewertung erneut aus, und überprüfen Sie, ob die Probleme behoben wurden.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Desktopanwendungsentwicklung mit hohem DPI-Windows](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   **Kontakt für technische Fragen:**<disup@microsoft.com>

 

 
