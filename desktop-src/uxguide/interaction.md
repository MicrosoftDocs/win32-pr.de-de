---
title: Interaktion
description: Interaktion ist die Vielzahl von Möglichkeiten, wie Benutzer mit Ihrer App interagieren, einschließlich Toucheingabe, Tastatur, Maus usw. Verwenden Sie diese Richtlinien, um intuitive und einzigartige Benutzeroberflächen zu erstellen, die für die Toucheingabe optimiert sind, aber über Eingabegeräte hinweg konsistent funktionieren.
ms.assetid: 1509c885-f4dc-4cf9-86a3-cc6754d3b4a0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 869034e8d7cc8b9d7023e1511482dae203c14b49
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524174"
---
# <a name="interaction"></a>Interaktion

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Interaktion ist die Vielzahl von Möglichkeiten, wie Benutzer mit Ihrer App interagieren, einschließlich Toucheingabe, Tastatur, Maus usw. Verwenden Sie diese Richtlinien, um intuitive und einzigartige Benutzeroberflächen zu erstellen, die für die Toucheingabe optimiert sind, aber über Eingabegeräte hinweg konsistent funktionieren.

## <a name="design-for-a-touch-first-experience"></a>Entwurf für eine Touch-First-Erfahrung

Am wichtigsten ist, dass Sie beim Entwerfen Ihrer App davon ausgehen, dass die Benutzer in erster Linie die Fingereingabe als Eingabemethode verwenden. Wenn Sie die Plattformsteuerelemente verwenden, erfordert die Unterstützung für Touchpad, Maus und Stift/Stift keine zusätzliche Programmierung, da Windows dies kostenlos bereitstellt.

Bedenken Sie dabei jedoch, dass eine für Toucheingaben optimierte Benutzeroberfläche einer herkömmlichen Benutzeroberfläche nicht in jedem Fall überlegen ist. Beide bieten Vor- und Nachteile, die sich auf die Technologie und die Anwendung auskennen. Bei der Umstellung auf eine Touch-First-Benutzeroberfläche ist es wichtig, die grundlegenden Unterschiede zwischen Toucheingabe (einschließlich Touchpad), Stift/Stift, Maus und Tastatureingabe zu verstehen. Nehmen Sie keine vertrauten Eingabegeräteeigenschaften und -verhaltensweisen als selbstverständlich an, da touch in Windows 8 mehr als nur diese Funktionalität emuliert.

Wie Sie bald feststellen werden, erfordert die Toucheingabe einen anderen Ansatz für den Benutzeroberflächenentwurf.

**Vergleich der Anforderungen für Toucheingabe-Interaktionen**

Diese Tabelle zeigt einige der Unterschiede zwischen Eingabegeräten, die Sie beim Entwerfen touchoptimierter Windows Store-Apps berücksichtigen sollten.



| Faktor          | Toucheingabe-Interaktionen   | Interaktionen über Maus, Tastatur oder Zeichen- bzw. Eingabestift | Touchpad  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
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

Wir stellen hier einige allgemeine Richtlinien für die Benutzerinteraktion bereit und behandeln gerätespezifische Richtlinien in diesen Themen.

-   [Toucheingabe](/windows/desktop/uxguide/inter-touch)
-   [Maus](/windows/desktop/uxguide/inter-mouse)
-   [Stift](/windows/desktop/uxguide/inter-pen)
-   [Tastatur](/windows/desktop/uxguide/inter-keyboard)
-   [Bedienungshilfen](/windows/desktop/uxguide/inter-accessibility)

## <a name="visuals-for-feedback"></a>Visuals für Feedback

Geeignetes visuelles Feedback bei Interaktionen mit Ihrer App hilft Benutzern dabei, zu erkennen, zu lernen und anzupassen, wie ihre Interaktionen sowohl von der App interpretiert werden, als auch das visuelle Feedback von Windows kann auf erfolgreiche Interaktionen hinweisen, den Systemstatus weiterleiten, das Gefühl der Kontrolle verbessern, Fehler reduzieren, Benutzern helfen, das System und das Eingabegerät zu verstehen und die Interaktion zu fördern.

Visuelles Feedback ist wichtig, wenn der Benutzer die Fingereingabe für Aktivitäten verwendet, bei denen Positionsgenauigkeit gefragt ist. Zeigen Sie immer Feedback an, wenn Toucheingabe erkannt wird, damit der Benutzer die von der App und den Steuerelementen definierten angepassten Zielbestimmungsregeln versteht.

## <a name="optimize-for-accuracy"></a>Optimieren der Genauigkeit

Die Toucheingabe umfasst den gesamten Kontaktbereich des Fingers. Diese Kontaktgeometrie wird verwendet, um das wahrscheinlichste Zielobjekt zu bestimmen. Dimensionieren Sie Ihre Steuerelemente, um eine komfortable Benutzeroberfläche mit Objekten und Steuerelementen sicherzustellen, die einfach und sicher als Ziel verwendet werden können.

Größe, Platz und Position ihrer Steuerelemente, um finger- und handverdeckung zu beseitigen, wobei die Benutzeroberfläche durch die Benutzerinteraktion selbst verdeckt wird.

Positionieren Sie nach Möglichkeit Menüs, Popups und QuickInfos über dem Kontaktbereich.

## <a name="constrain-for-confidence"></a>Einschränken der Zuverlässigkeit

Vermeiden oder minimieren Sie Disketteninteraktionen mithilfe von Benutzeroberflächeneinschränkungen.

-   Andockpunkte können das Anhalten an gewünschten Stellen vereinfachen. Mit Andockpunkten werden logische Stopps im App-Inhalt festgelegt. Kognitiv fungieren Ausrichtungspunkte als Auslagerungsmechanismus für den Benutzer und minimieren die Ermüdung durch übermäßiges Gleiten, Wischen oder Drehen. Mit ihnen können Sie unpräzise Benutzereingaben verarbeiten und sicherstellen, dass eine bestimmte Teilmenge von Inhalten oder Schlüsselinformationen angezeigt wird.
-   Direktionale "Schienen", die die Bewegungsachse (vertikal oder horizontal) hervorheben.

## <a name="avoid-timed-interactions"></a>Vermeiden von zeitlichen Interaktionen

Die Interaktionen sollten nicht anhand der Zeit unterschieden werden. Eine Interaktion sollte unabhängig von der Ausführungsdauer immer zum gleichen Ergebnis führen. Zeitbasierte Aktivierungen führen zu obligatorischen Verzögerungen für Benutzer und beeinträchtigen die immersive Natur der direkten Manipulation und die Wahrnehmung der Reaktion des Systems.

Zeitlich festgelegte Interaktionen bestimmen normalerweise abhängig von unsichtbaren Schwellenwerten wie Zeit, Entfernung oder Geschwindigkeit, welcher Befehl ausgeführt werden soll. Zeitabhängige Interaktionen haben kein visuelles Feedback, bis das System die Aktion ausführt und Benutzer willkürliche und unsichtbare Schwellenwerte erreichen müssen, um ein Ergebnis zu erzielen. Sofortiges visuelles Feedback bei Interaktionen weckt die Aufmerksamkeit der Benutzer und vermittelt ihnen ein Gefühl von Sicherheit und Kontrolle.

Interaktionen, die direkte Auswirkungen auf Objekte haben und reale Interaktionen nachahmen, sind intuitiver und leichter zu finden und zu merken. Sie sind nicht auf schwer verständliche oder abstrakte Interaktionen angewiesen.

**Hinweis:** Eine Ausnahme besteht darin, dass Sie bestimmte zeitlich festgelegte Interaktionen verwenden, um beim Lernen und Untersuchen zu helfen (z. B. drücken und halten). Die Verwendung geeigneter Beschreibungen und visueller Hinweise hat einen großen Einfluss auf die Verwendung erweiterter Interaktionen.

