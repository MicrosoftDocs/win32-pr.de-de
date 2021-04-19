---
description: .
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: 'Benutzeroberfläche: Hohe DPI-Werte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e93aeed452f421e8e38df8d6d75f6bbe1f97cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354025"
---
# <a name="user-interface---high-dpi-awareness"></a>Benutzeroberfläche: Hohe DPI-Werte

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients** -Windows XP \| Windows Vista \| Windows 7  

## <a name="feature-impact"></a>Auswirkungen von Features

**Schweregrad** -Mittel  
**Frequency** -Medium  

## <a name="description"></a>BESCHREIBUNG

Ziel ist es, Endbenutzern zu empfehlen, Ihre Anzeige auf die systemeigene Auflösung festzulegen und dpi anstelle der Bildschirmauflösung zu verwenden, um die Größe von angezeigter Text und Bilder zu ändern. Windows 7 kann eine Standard-dpi bei Neuinstallationen auf Computern, die von ihren OEMs mithilfe der DPI-Einstellungen konfiguriert wurden, automatisch erkennen und konfigurieren. Es gibt Tools, die Sie verwenden können, um Anwendungen zu entwerfen, die hoch dpi-fähig sind, um die gängigsten Ergebnisse sicherzustellen.

Wir haben Windows 7 zwei neue High-dpi-Features hinzugefügt:

-   DPI-Einstellung pro Benutzer (zuvor pro Computer)
-   DPI ohne Neustart ändern (Abmeldung/Anmeldung ist noch erforderlich)

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

Anwendungen, die die Groß-/Kleinschreibung nicht verarbeiten, weisen wahrscheinlich visuelle Artefakte auf, einschließlich:

-   Clipping von Benutzeroberfläche oder Text durch andere Benutzeroberflächen Elemente
-   Inkonsistente Schriftart Größen
-   Benutzerdefinierte Benutzeroberflächen
-   Verwischt von Text oder UI
-   Unterbrochene Drag & Drop-Eingaben oder andere Eingaben
-   Rendering von voll Bild-DX-Anwendungen teilweise aus dem Bildschirm

## <a name="solution"></a>Lösung

So machen Sie Ihre Anwendungen mit dpi-Werten kompatibel:

1.  Führen Sie einen Funktions Testdurchlauf auf hoher Ebene aus, einschließlich der Installation und Deinstallation unter den folgenden Einstellungen:

    | Einstellung                                              | Was Sie suchen müssen                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1024 x 768 @ 120 dpi (125% Skalierung)                    | Dies ist eine effektive Auflösung von ~ 800X600. Achten Sie also auf die Benutzeroberfläche, die auf dem Bildschirm oder auf Layoutprobleme abgeschnitten wurde. Suchen Sie auch nach pixilen Bitmaps & Symbolen.                         |
    | 1600x1200 @144 dpi (150% Skalierung)                    | Blurry-Benutzeroberfläche. Überprüfen Sie, ob alle Maus Vorgänge funktionieren, insbesondere ziehen Sie & Drop-Vorgänge. Überprüfen Sie auch, ob die Vollbildmodi ordnungsgemäß funktionieren.                                     |
    | 1600x1200 @ 144 dpi mit deaktivierter dpi-Virtualisierung | Häufig werden Schaltflächen und die Benutzeroberfläche nicht in Relation zu größerem Text skaliert, & ein signifikanter Text Clipping vorhanden ist. Suchen Sie im Allgemeinen nach Layoutproblemen, & & Symbolen Symbolen. |

    

     

2.  Notieren Sie sich alle gefundenen Probleme, einschließlich des Speicher Orts, der Bildschirmauflösung und der DPI-Einstellungen. Außerdem wird erläutert, wie sich die Anwendung in den anderen dpi/Resolution-Konfigurationen aus Gründen der Vollständigkeit verhält.
3.  Überprüfen der einzelnen Probleme gegen häufige dpi-Codierungs Probleme
4.  Bewerten der Kosten für die vollständige dpi-Erkennung der Anwendung
5.  Erstellen Sie eine Liste der erforderlichen hohen dpi-Objekte (z. b. Schaltflächen, Symbole).
6.  Arbeiten Sie durch, und korrigieren Sie die Liste der in Schritt 1 gefundenen dpi-Probleme.
7.  Integrieren der neuen Assets aus Schritt 5
8.  Deklarieren Sie Ihre Anwendung dpi-fähig

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit

Führen Sie die dpi-Bewertung erneut aus, und überprüfen Sie, ob die Probleme behoben wurden.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Hohe dpi-Entwicklung für Desktop Anwendungen unter Windows](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   **Wenden Sie sich für technische Fragen an:**<disup@microsoft.com>

 

 
