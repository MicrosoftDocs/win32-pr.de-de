---
description: Es folgt eine Liste der Gestenglyphen, die Microsoft in Zukunft als Teil der Microsoft-Gestenerkennung unterstützen möchte.
ms.assetid: 4d504140-ff48-4a07-9bf7-a36913e44426
title: Nicht implementierte Glyphen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f3966ef2e4bec268bc4b45b65b6778abd434f4169ec1e2aa971703032f07ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966709"
---
# <a name="unimplemented-glyphs"></a>Nicht implementierte Glyphen

Im Folgenden ist eine Liste der Gestenglyphen aufgeführt, die Microsoft in Zukunft als Teil der *Microsoft-Gestenerkennung* unterstützen möchte. Es wird daran gearbeitet, sicherzustellen, dass die Erkennungsgenauigkeit für diese Glyphen hoch ist (um eine versehentliche Aktivierung zu vermeiden), und dass sie den entsprechenden Vorgängen zugeordnet werden.

Um die Konsistenz der *Gesten* sicherzustellen, die für allgemeine *Aktionen* zwischen Anwendungen verwendet werden, sollten Sie die folgenden Vorschläge befolgen:

-   Die *Aktion* ist das vorgeschlagene semantische Verhalten, das der Geste zugeordnet ist.
-   Für gesten mit der Bezeichnung *Fixed* in der folgenden Tabelle wird empfohlen, das vorgeschlagene semantische Verhalten nicht zu ändern. Wenn eine Anwendung das angegebene semantische Verhalten nicht benötigt, wird empfohlen, die Geste nicht für eine andere Aktion oder Semantik wiederzuverwenden.
-   Sie sollten allen anderen Gesten relevante semantische Verhaltensweisen zuordnen können. Diese Gesten werden als *Anwendungsspezifisch* bezeichnet. Für Gesten, die ein vorgeschlagenes semantisches Verhalten aufweisen, wird empfohlen, die Geste für die vorgeschlagene Semantik zu verwenden, wenn die entsprechende Funktionalität in Ihrer Anwendung vorhanden ist.
-   Der Heiße Punkt einer Geste ist ein Unterscheidungspunkt in der Geometrie der Geste. Der Heiße Punkt kann verwendet werden, um zu bestimmen, wo die Geste vorgenommen wurde. Die Gesten-API ermöglicht es, den heißen Punkt für eine bestimmte Geste zu bestimmen. Allerdings haben nicht alle Gesten einen bestimmten Unterscheidungspunkt. Für Diejenigen, die keinen bestimmten Unterscheidungspunkt aufweisen, wird der Startpunkt als Heißpunkt gemeldet.

> [!Note]  
> Einige der Gesten verfügen über einen unterscheidenden Heißenpunkt, der nur der Ausgangspunkt ist. Diese werden in der Tabelle unterschieden.

 



| Gestenname                      | Aktion                                         | Fest                           | Heißer Punkt                                                           |
|-----------------------------------|------------------------------------------------|---------------------------------|---------------------------------------------------------------------|
| Unendlich<br/>               | Ein- und Ausschalten des Gestenmodus<br/> | Fest<br/>                | Startpunkt<br/>                                           |
| Cross<br/>                  | Löschen<br/>                              | Anwendungsspezifisch<br/> | Schnittmenge der Striche<br/>                              |
| Absatzmarke<br/>         | Neuer Absatz<br/>                       | Fest<br/>                | Startpunkt<br/>                                           |
| `Section`<br/>                | Neuer Abschnitt<br/>                         | Fest<br/>                | Startpunkt<br/>                                           |
| Kugel<br/>                 | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Aufzählungszeichen übergreifend<br/>           | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Wellenlinie<br/>               | Fett<br/>                                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Swap<br/>                   | Exchange Inhalt<br/>                    | Anwendungsspezifisch<br/> | Mitte des Nach-oben-Strichs<br/>                                  |
| Öffnen<br/>                 | Leerzeichen zwischen Wörtern öffnen<br/>         | Anwendungsspezifisch<br/> | Mitte des Abwärtsstrichs<br/>                                |
| Closeup<br/>                | Schließen Sie zusätzlichen Speicherplatz.<br/>                | Anwendungsspezifisch<br/> | Mittelpunkt des vertikalen Abstands zwischen den beiden Klammern<br/> |
| Rechteck<br/>              | Wählt eingeschlossenen Inhalt aus.<br/>            | Fest<br/>                | Startpunkt<br/>                                           |
| Kreis tippen<br/>             | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Tippen<br/>                                                      |
| Kreiskreis<br/>          | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Kreisübergreifend<br/>           | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Kreislinie-vertikal<br/>   | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Kreislinie horizontal<br/> | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Doppelpfeil nach oben<br/>        | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeilkopfs<br/>                                   |
| Doppelpfeil nach unten<br/>      | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeilkopfs<br/>                                   |
| Doppelpfeil nach links<br/>      | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeilkopfs<br/>                                   |
| Doppelpfeil nach rechts<br/>     | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeilkopfs<br/>                                   |
| Nach oben nach links<br/>          | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeilkopfs<br/>                                   |
| Nach oben nach rechts<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeilkopfs<br/>                                   |
| Nach unten nach links<br/>        | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeilkopfs<br/>                                   |
| Nach unten nach rechts<br/>       | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeilkopfs<br/>                                   |
| Nach links nach oben<br/>          | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Die Spitze des Pfeilkopfs<br/>                               |
| Nach links nach unten<br/>        | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeilkopfs<br/>                                   |
| Nach rechts nach oben<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeilkopfs<br/>                                   |
| Nach unten nach rechts<br/>       | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Spitze des Pfeilkopfs<br/>                                   |
| Diagonale Linke<br/>        | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Diagonale Nach rechts<br/>       | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Diagonale Nach-Links-Abdrückung<br/>      | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Diagonaler Rechtsdown<br/>     | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe A<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe B<br/>         | Fett<br/>                                | Fest<br/>                | Startpunkt<br/>                                           |
| Lateinischer Buchstabe C<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe D<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe E<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-F<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe G<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe H<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe I<br/>         | Kursiv<br/>                              | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe J<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe K<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe L<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe M<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe N<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe O<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe P<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Latin-Letter-Q<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe R<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe S<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe T<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe U<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe V<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe W<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe X<br/>         | Ausschneiden<br/>                                 | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinischer Buchstabe Y<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Lateinisch-Buchstabe-Z<br/>         | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer 0<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer 1<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer 2<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer 3<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer 4<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer 5<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer 6<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer 7<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer 8<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Ziffer 9<br/>                | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Fragezeichen<br/>          | Hilfe<br/>                                | Fest<br/>                | Zenträr entlang der Höhe der Kurve<br/>                     |
| Scharf<br/>                  | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Dollar<br/>                 | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Asterisk<br/>               | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Zentrum<br/>                                                   |
| Plus<br/>                   | Einfügen<br/>                               | Fest<br/>                | Schnittmenge der Striche<br/>                              |
| Double-up<br/>              | Bildlauf nach oben<br/>                           | Fest<br/>                | Startpunkt<br/>                                           |
| Double-down<br/>            | Bildlauf nach unten<br/>                         | Fest<br/>                | Startpunkt<br/>                                           |
| Doppelt links<br/>            | Nach links scrollen<br/>                         | Fest<br/>                | Startpunkt<br/>                                           |
| Doppelt rechts<br/>           | Nach rechts scrollen<br/>                        | Fest<br/>                | Startpunkt<br/>                                           |
| Triple-up<br/>              | Bild auf<br/>                             | Fest<br/>                | Startpunkt<br/>                                           |
| Triple-down<br/>            | Bild ab<br/>                           | Fest<br/>                | Startpunkt<br/>                                           |
| Triple-left<br/>            | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Triple-right<br/>           | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Startpunkt<br/>                                           |
| Eckige Klammer<br/>           | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Midpoint<br/>                                                 |
| Eckige Klammer unter<br/>          | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Midpoint<br/>                                                 |
| Eckige Klammer links<br/>           | Start der Auswahl<br/>                  | Fest<br/>                | Midpoint<br/>                                                 |
| Eckige Klammer rechts<br/>          | Ende der Auswahl<br/>                    | Fest<br/>                | Midpoint<br/>                                                 |
| Geschweifte Klammer<br/>             | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Midpoint<br/>                                                 |
| Geschweifte Klammer unter<br/>            | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Midpoint<br/>                                                 |
| Geschweifte Klammer links<br/>             | Start der diskontinuierlich ausgewählten Auswahl<br/>    | Fest<br/>                | Midpoint<br/>                                                 |
| Geschweifte Klammer rechts<br/>            | Ende der diskontinuierlich ausgewählten Auswahl<br/>      | Fest<br/>                | Midpoint<br/>                                                 |
| Dreifaches Tippen<br/>             | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Ausgangspunkt ist die Unterscheidung nach "Heißer Punkt"<br/>               |
| Vierfach tippen<br/>          | Anwendungsspezifisch<br/>                | Anwendungsspezifisch<br/> | Ausgangspunkt ist die Unterscheidung nach "Heißer Punkt"<br/>               |



 

 

 




