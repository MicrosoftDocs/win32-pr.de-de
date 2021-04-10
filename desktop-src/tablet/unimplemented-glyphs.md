---
description: Im folgenden finden Sie eine Liste von Gesten Symbolen, die Microsoft in Zukunft als Teil der Microsoft Gestenerkennung unterstützen möchte.
ms.assetid: 4d504140-ff48-4a07-9bf7-a36913e44426
title: Nicht implementierte Symbole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d479c6f3b486706b9e8d063ae2bc46daf5a0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214554"
---
# <a name="unimplemented-glyphs"></a>Nicht implementierte Symbole

Im folgenden finden Sie eine Liste von Gesten Symbolen, die Microsoft in Zukunft als Teil der *Microsoft Gestenerkennung* unterstützen möchte. Es wird zurzeit gearbeitet, um sicherzustellen, dass die Erkennungsgenauigkeit für diese Symbole hoch ist (um eine versehentliche Aktivierung zu vermeiden) und dass Sie den entsprechenden Vorgängen zugeordnet werden.

Um die Konsistenz von *Gesten* sicherzustellen, die für häufige *Aktionen* zwischen Anwendungen verwendet werden, sollten Sie die folgenden Vorschläge befolgen:

-   Die *Aktion* ist das vorgeschlagene Semantik Verhalten, das mit der Geste verknüpft ist.
-   Für die Gesten in der folgenden Tabelle wird empfohlen, das empfohlene Semantik Verhalten *nicht zu ändern* . Wenn für eine Anwendung das angegebene Semantik Verhalten nicht erforderlich ist, wird empfohlen, die Geste für eine andere Aktion oder Semantik nicht wiederzuverwenden.
-   Sie sollten das relevante Semantik Verhalten allen anderen Gesten zuordnen können. Diese Gesten werden als *anwendungsspezifisch* bezeichnet. Für Gesten mit einem empfohlenen Semantik Verhalten wird empfohlen, dass Sie die Geste der vorgeschlagenen Semantik verwenden, wenn die entsprechende Funktionalität in Ihrer Anwendung vorhanden ist.
-   Der heiße Punkt einer Geste ist ein Erkennungs Punkt in der Geometrie der Bewegung. Der Hotspot kann verwendet werden, um zu bestimmen, an welcher Stelle die Geste durchgeführt wurde. Die Gesten-API ermöglicht es, den Hotspot für eine bestimmte Geste zu ermitteln. Allerdings haben nicht alle Gesten einen bestimmten Unterscheidungs-Hot Point. Für diejenigen, die keinen bestimmten Unterscheidungs-Hot-Punkt aufweisen, wird der Ausgangspunkt als Hot Point gemeldet.

> [!Note]  
> Einige der Gesten haben einen Unterschied, dass es sich um den Ausgangspunkt handelt. Diese werden in der Tabelle unterschieden.

 



| Gesten Name                      | Aktion                                         | Fest                           | Hotspot                                                           |
|-----------------------------------|------------------------------------------------|---------------------------------|---------------------------------------------------------------------|
| Unendlich<br/>               | Wechseln in den und aus dem Gesten Modus<br/> | Fest<br/>                | Startpunkt<br/>                                           |
| Cross<br/>                  | Löschen<br/>                              | Anwendungsspezifisch<br/> | Schnittmenge der Striche<br/>                              |
| Absatz Markierung<br/>         | Neuer Absatz<br/>                       | Fest<br/>                | Startpunkt<br/>                                           |
| `Section`<br/>                | Neuer Abschnitt<br/>                         | Fest<br/>                | Startpunkt<br/>                                           |
| Streif<br/>                 | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Kugel-Kreuz<br/>           | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Wellenlinie<br/>               | Fett<br/>                                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Swap<br/>                   | Exchange-Inhalt<br/>                    | Anwendungsspezifisch<br/> | Mitte des aufwärts Strichs<br/>                                  |
| OpenUp<br/>                 | Leerzeichen zwischen Wörtern öffnen<br/>         | Anwendungsspezifisch<br/> | Mitte des nach-unten-Strichs<br/>                                |
| Nahaufnahme<br/>                | Zusätzlichen Speicherplatz schließen<br/>                | Anwendungsspezifisch<br/> | Mitte des vertikalen Leerraums zwischen den beiden Klammern<br/> |
| Rechteck<br/>              | Eingeschlossene Inhalte auswählen<br/>            | Fest<br/>                | Startpunkt<br/>                                           |
| Kreis-tippen<br/>             | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Tippen<br/>                                                      |
| Kreis-Kreis<br/>          | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Kreis-Kreuz<br/>           | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Zirkel Linie-vertikal<br/>   | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Zirkel Linie Horizontal<br/> | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Doppelpfeil nach oben<br/>        | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeil Kopfes<br/>                                   |
| Doppelpfeil nach unten<br/>      | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeil Kopfes<br/>                                   |
| Doppelpfeil-Links<br/>      | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeil Kopfes<br/>                                   |
| Doppelpfeil nach rechts<br/>     | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeil Kopfes<br/>                                   |
| Nach-oben-nach-links<br/>          | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeil Kopfes<br/>                                   |
| Nach-rechts-Taste<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeil Kopfes<br/>                                   |
| Nach-unten-nach-links<br/>        | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeil Kopfes<br/>                                   |
| Nach-rechts-Taste<br/>       | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeil Kopfes<br/>                                   |
| Pfeil nach links nach oben<br/>          | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Die Spitze des Pfeil Kopfes.<br/>                               |
| Pfeil nach links nach unten<br/>        | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeil Kopfes<br/>                                   |
| Rechter Pfeil nach oben<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeil Kopfes<br/>                                   |
| Nach-rechts-Pfeil nach unten<br/>       | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeil Kopfes<br/>                                   |
| Diagonal-linkstup<br/>        | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Diagonal-right-right<br/>       | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Diagonal-Links unten<br/>      | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Diagonal-rechts unten<br/>     | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-A<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-B<br/>         | Fett<br/>                                | Fest<br/>                | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-C<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-D<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-E<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-F<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-G<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-H<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-I<br/>         | Kursiv<br/>                              | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-J<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-K<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-L<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-M<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-N<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-O<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-P<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-Q<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-R<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-S<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-T<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-U<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-V<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-W<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-X<br/>         | Ausschneiden<br/>                                 | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-Y<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-Z<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer-0<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer-1<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer-2<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer-3<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer-4<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer-5<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer-6<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer-7<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer-8<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer 9<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Fragezeichen<br/>          | Hilfe<br/>                                | Fest<br/>                | Zentriert entlang der Höhe der Kurve<br/>                     |
| Scharfer<br/>                  | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ausgegebenen<br/>                 | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Asterisk<br/>               | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Zentrum<br/>                                                   |
| Plus<br/>                   | Einfügen<br/>                               | Fest<br/>                | Schnittmenge der Striche<br/>                              |
| Double-Up<br/>              | Bildlauf nach oben<br/>                           | Fest<br/>                | Startpunkt<br/>                                           |
| Doppel unten<br/>            | Bildlauf nach unten<br/>                         | Fest<br/>                | Startpunkt<br/>                                           |
| Doppel Links<br/>            | Bildlauf nach links<br/>                         | Fest<br/>                | Startpunkt<br/>                                           |
| Double-right<br/>           | Bildlauf nach rechts<br/>                        | Fest<br/>                | Startpunkt<br/>                                           |
| Dreimal hoch<br/>              | Bild auf<br/>                             | Fest<br/>                | Startpunkt<br/>                                           |
| Triple-Down<br/>            | Bild ab<br/>                           | Fest<br/>                | Startpunkt<br/>                                           |
| Dreimal Links<br/>            | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Triple-right<br/>           | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Klammer-over<br/>           | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Midpoint<br/>                                                 |
| Klammer-unter<br/>          | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Midpoint<br/>                                                 |
| Eckige Klammer links<br/>           | Auswahl Beginn<br/>                  | Fest<br/>                | Midpoint<br/>                                                 |
| Klammer-rechts<br/>          | Ende der Auswahl<br/>                    | Fest<br/>                | Midpoint<br/>                                                 |
| Geschweifter Klammer<br/>             | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Midpoint<br/>                                                 |
| Geschweifter Klammer unter<br/>            | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Midpoint<br/>                                                 |
| Geschweifter Klammer links<br/>             | Beginn der diskontinuierlichen Auswahl<br/>    | Fest<br/>                | Midpoint<br/>                                                 |
| Geschweifter Klammer rechts<br/>            | Ende der diskontinuierlichen Auswahl<br/>      | Fest<br/>                | Midpoint<br/>                                                 |
| Triple-Tap<br/>             | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Der Ausgangspunkt unterscheidet sich als Hot Point.<br/>               |
| Viereck tippen<br/>          | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Der Ausgangspunkt unterscheidet sich als Hot Point.<br/>               |



 

 

 




