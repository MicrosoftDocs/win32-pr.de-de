---
title: Interaktion
description: Interaktion ist die unterschiedliche Art und Weise, wie Benutzer mit Ihrer APP interagieren, einschließlich berühren, Tastatur, Maus und so weiter. Verwenden Sie diese Richtlinien, um intuitive und differenzierte Benutzeroberflächen zu erstellen, die für die Berührungs Optimierung optimiert sind, aber konsistent auf Eingabegeräten funktionieren
ms.assetid: 1509c885-f4dc-4cf9-86a3-cc6754d3b4a0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: fbbbed55bbee1b1b0a028bada4e9d97682d9c293
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106366540"
---
# <a name="interaction"></a>Interaktion

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Interaktion ist die unterschiedliche Art und Weise, wie Benutzer mit Ihrer APP interagieren, einschließlich berühren, Tastatur, Maus und so weiter. Verwenden Sie diese Richtlinien, um intuitive und differenzierte Benutzeroberflächen zu erstellen, die für die Berührungs Optimierung optimiert sind, aber konsistent auf Eingabegeräten funktionieren

## <a name="design-for-a-touch-first-experience"></a>Entwurf für eine Berührungs basierte Interaktion

Am wichtigsten ist, dass Sie beim Entwerfen Ihrer App davon ausgehen, dass die Benutzer in erster Linie die Fingereingabe als Eingabemethode verwenden. Wenn Sie die Platt Form Steuerelemente verwenden, ist für die Unterstützung von Touchpad, Maus und Stift/Tablettstift keine zusätzliche Programmierung erforderlich, da Windows dies kostenlos bereitstellt.

Bedenken Sie dabei jedoch, dass eine für Toucheingaben optimierte Benutzeroberfläche einer herkömmlichen Benutzeroberfläche nicht in jedem Fall überlegen ist. Beide bieten vor-und Nachteile, die für die Technologie und die Anwendung eindeutig sind. Bei der Umstellung auf eine Touch-First-Benutzeroberfläche ist es wichtig, die wesentlichen Unterschiede zwischen Touch (einschließlich Touchpad), Stift/Tablettstift, Maus und Tastatureingaben zu verstehen. Nehmen Sie keine vertrauten Eingabegeräte Eigenschaften und Verhaltensweisen für die Gewährung vor, da die Interaktion in Windows 8 mehr als einfach nur diese Funktionalität emuliert.

Wie Sie bald erkennen, erfordert die Berührungs Eingabe einen anderen Ansatz für den Entwurf der Benutzeroberfläche.

**Vergleich der Anforderungen für Toucheingabe-Interaktionen**

In dieser Tabelle werden einige der Unterschiede zwischen Eingabegeräten angezeigt, die Sie beim Entwerfen von Touchscreen-optimierten Windows Store-Apps berücksichtigen sollten.



|                                 |                                                                                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                 |                                                     |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| **Aspekt**<br/>           | **Interaktionen per Toucheingabe**<br/>                                                                                                                                                                                | **Interaktionen über Maus, Tastatur oder Zeichen- bzw. Eingabestift**<br/>                                                                                                                                                                                                                                                         | **Touchpad**<br/>                             |
| **Genauigkeit**<br/>        | Der Kontaktbereich einer Fingerspitze ist größer als eine einzige xy-Koordinate. Dadurch erhöht sich die Wahrscheinlichkeit, dass Befehle unbeabsichtigt aktiviert werden.<br/>                                                               | Maus und Zeichen- oder Eingabestift liefern eine präzise xy-Koordinate.<br/>                                                                                                                                                                                                                                            | Identisch mit der Maus.<br/>                           |
|                                 | Die Form des Kontaktbereichs ändert sich während der Bewegung. <br/>                                                                                                                                       | Mausbewegungen und Striche mit Zeichen- oder Eingabestift liefern eine präzise xy-Koordinate. Die Tastatur hat einen expliziten Fokus.<br/>                                                                                                                                                                                                   | Identisch mit der Maus.<br/>                           |
|                                 | Es gibt keinen Mauscursor, der die Zielbestimmung unterstützt.<br/>                                                                                                                                                    | Der Fokus von Mauscursor, Zeichen- oder Eingabestiftcursor und Tastatur unterstützt die Zielbestimmung.<br/>                                                                                                                                                                                                                   | Identisch mit der Maus.<br/>                           |
| **Menschliche Anatomie**<br/>    | Bewegungen mit den Fingerspitzen sind ungenau, da es schwierig ist, mit den Fingern eine lineare Bewegung auszuführen. Dies liegt an der Krümmung der Handgelenke und der Anzahl der an der Bewegung beteiligten Gelenke.<br/> | Es ist leichter, mit der Maus oder mit einem Zeichen- oder Eingabestift eine Bewegung in gerader Linie auszuführen, da die Hand, die diese Geräte steuert, eine kürzere physische Strecke zurücklegen muss als der Cursor auf dem Bildschirm.<br/>                                                                                                                    | Identisch mit der Maus.<br/>                           |
|                                 | Manche Bereiche der für die Fingereingabe vorgesehenen Oberfläche eines Anzeigegeräts sind aufgrund der Fingerhaltung und der Tatsache, dass der Benutzer das Gerät halten muss, möglicherweise schwer zu erreichen.<br/>                                                                | Maus und Zeichen- oder Eingabestift können alle Bereiche des Bildschirms erreichen, während über die Aktivierreihenfolge der Zugriff auf alle Steuerelemente möglich sein sollte. <br/>                                                                                                                                                                 | Haltung und Druck der Finger spielen dabei eventuell auch eine Rolle.<br/> |
|                                 | Objekte werden möglicherweise durch mindestens eine Fingerspitze oder die Hand des Benutzers verdeckt. Dies wird als Okklusion bezeichnet.<br/>                                                                                                   | Indirekte Eingabegeräte verursachen keine Okklusion.<br/>                                                                                                                                                                                                                                                       | Identisch mit der Maus.<br/>                           |
| **Objektstatus**<br/>     | Bei der Fingereingabe wird ein Modell mit zwei Zuständen verwendet: Die für die Fingereingabe vorgesehene Oberfläche eines Anzeigegeräts wird entweder berührt (ein) oder nicht berührt (aus). Es gibt keinen Zeigezustand, der zusätzliches visuelles Feedback auslösen kann.<br/>                         | Maus, Zeichen- oder Eingabestift und Tastatur machen ein Modell mit drei Zuständen verfügbar: oben (aus), unten (ein) und Zeigen (Fokus).<br/> Mit Zeigen können Benutzer QuickInfos zu UI-Elementen erforschen und kennenlernen. Zeigen und Fokus können vermitteln, welche Objekte interaktiv sind, und außerdem die Zielbestimmung erleichtern. <br/> | Identisch mit der Maus.<br/>                           |
| **Umfangreiche Interaktionen**<br/> | Unterstützt die Mehrfingereingabe: mehrere Eingabepunkte (Fingerspitzen) auf einer für die Fingereingabe vorgesehenen Oberfläche.<br/>                                                                                                                          | Unterstützt einen einzigen Eingabepunkt.<br/>                                                                                                                                                                                                                                                                       | Identisch mit der Fingereingabe.<br/>                           |
|                                 | Unterstützt die direkte Manipulation von Objekten durch Bewegungen wie beispielsweise Tippen, Ziehen, Zusammendrücken und Drehen.<br/>                                                                                  | Keine Unterstützung für die direkte Manipulation, da Maus, Zeichen- oder Eingabestift und Tastatur indirekte Eingabegeräte sind.<br/>                                                                                                                                                                                                    | Identisch mit der Maus.<br/>                           |



 

**Hinweis**

Die indirekte Eingabe hat den Vorteil, dass sie über 25 Jahre optimiert wurde. Features wie durch Zeigen ausgelöste QuickInfos wurden als Lösung für die Erforschung der UI speziell für die Eingabe über Touchpad, Maus, Zeichen- oder Eingabestift und Tastatur entworfen. Solche UI-Funktionen wurden neu entworfen, um der umfassenden Toucheingabefunktion gerecht zu werden, ohne die Benutzererfahrung auf den anderen Geräten zu beeinträchtigen.

Wir stellen hier einige allgemeine Richtlinien für die Benutzerinteraktion bereit und decken gerätespezifische Richtlinien in diesen Themen ab.

-   [Toucheingabe](/windows/desktop/uxguide/inter-touch)
-   [Maus](/windows/desktop/uxguide/inter-mouse)
-   [Stift](/windows/desktop/uxguide/inter-pen)
-   [Tastatur](/windows/desktop/uxguide/inter-keyboard)
-   [Bedienungshilfen](/windows/desktop/uxguide/inter-accessibility)

## <a name="visuals-for-feedback"></a>Visuelle Elemente für Feedback

Durch entsprechendes visuelles Feedback bei Interaktionen mit ihrer App können Benutzer ihre Interaktionen erkennen, erlernen und anpassen, wie ihre Interaktionen sowohl von der App als auch von dem visuellen Windows-Feedback interpretiert werden, können auf erfolgreiche Interaktionen, den Status des relaysystems, das Verbessern der Steuerung, das Verringern von Fehlern, das verstehen des System-und Eingabe Geräts und das fördern der Interaktion hinweisen.

Visuelles Feedback ist wichtig, wenn der Benutzer die Fingereingabe für Aktivitäten verwendet, bei denen Positionsgenauigkeit gefragt ist. Zeigen Sie immer Feedback an, wenn Toucheingabe erkannt wird, damit der Benutzer die von der App und den Steuerelementen definierten angepassten Zielbestimmungsregeln versteht.

## <a name="optimize-for-accuracy"></a>Optimieren der Genauigkeit

Touch-Eingaben betreffen den gesamten Kontaktbereich des Fingers. Diese Kontakt Geometrie wird verwendet, um das wahrscheinlichste Zielobjekt zu ermitteln. Größe Ihrer Steuerelemente, um eine bequeme Benutzeroberfläche mit Objekten und Steuerelementen zu gewährleisten, die einfach und sicher für das Ziel sind.

Größe, Leerraum und Position Ihrer Steuerelemente, um die Finger-und Handzeichen-oksion zu eliminieren, bei der die Benutzeroberfläche durch die Benutzerinteraktion selbst verdeckt wird.

Positions Menüs, Popups und Quick Infos über dem Kontaktbereich, wann immer dies möglich ist.

## <a name="constrain-for-confidence"></a>Vertrauen einschränken

Vermeiden oder minimieren Sie schlampigen-Interaktionen mithilfe von Benutzeroberflächen Einschränkungen.

-   Andockpunkte können das Ende an den gewünschten Orten vereinfachen. Mit Andockpunkten werden logische Stopps im App-Inhalt festgelegt. Reaktions Punkte fungieren als Auslagerungs Mechanismus für den Benutzer und minimieren die Ermüdung durch übermäßige gleitende, Striping-oder rotieren. Mit Ihnen können Sie unpräzise Benutzereingaben behandeln und sicherstellen, dass eine bestimmte Teilmenge von Inhalts-oder Schlüsselinformationen angezeigt wird.
-   Direktionale "Rails", die die Achse der Bewegung (vertikal oder horizontal) hervorheben.

## <a name="avoid-timed-interactions"></a>Vermeiden von zeitgesteuerten Interaktionen

Die Interaktionen sollten nicht anhand der Zeit unterschieden werden. Eine Interaktion sollte unabhängig von der Ausführungsdauer immer zum gleichen Ergebnis führen. Zeitbasierte Aktivierungen führen zu obligatorischen Verzögerungen für Benutzer und beeinträchtigen die immersive Natur der direkten Manipulation und die Wahrnehmung der Reaktion des Systems.

Zeitlich festgelegte Interaktionen bestimmen normalerweise abhängig von unsichtbaren Schwellenwerten wie Zeit, Entfernung oder Geschwindigkeit, welcher Befehl ausgeführt werden soll. Zeitgesteuerte Interaktionen haben kein visuelles Feedback, bis das System die Aktion ausführt und Benutzer beliebige und unsichtbare Schwellenwerte erreichen müssen, um ein Ergebnis zu erzielen. Sofortiges visuelles Feedback bei Interaktionen weckt die Aufmerksamkeit der Benutzer und vermittelt ihnen ein Gefühl von Sicherheit und Kontrolle.

Interaktionen, die direkte Auswirkungen auf Objekte haben und reale Interaktionen nachahmen, sind intuitiver und leichter zu finden und zu merken. Sie sind nicht auf schwer verständliche oder abstrakte Interaktionen angewiesen.

**Hinweis:** Eine Ausnahme besteht darin, dass Sie bestimmte zeitgesteuerte Interaktionen verwenden, um das Erlernen und durchsuchen zu unterstützen (z. b. Drücken und halten). Die Verwendung von geeigneten Beschreibungen und visuellen Cues hat eine große Auswirkung auf die Verwendung von erweiterten Interaktionen.

