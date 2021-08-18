---
description: Grundlagen Light-Aware Benutzeroberflächen
ms.assetid: 7ea391cb-f72b-4ac1-99be-c957d4ccc8af
title: Grundlagen Light-Aware Benutzeroberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8955180dfc57219d3b640c6463f2ee2025f22500d3d29b688bc4b0c154895f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890206"
---
# <a name="fundamentals-of-light-aware-user-interfaces"></a>Grundlagen Light-Aware Benutzeroberflächen

Der Begriff *lichtfähige Benutzeroberfläche* bezieht sich auf ein Programm, das Lichtsensordaten verwendet, um seinen Inhalt, Steuerelemente und andere Grafiken für eine optimale Benutzererfahrung bei vielen Beleuchtungsbedingungen zu optimieren, von Dern zu direkt wirkenden Menschen. Die wichtigsten Optimierungen sind möglicherweise Lesbarkeit, Lesbarkeit und Interaktionen bei direkter Empfindlichkeit, da Bildschirme unter diesen Bedingungen in der Regel nicht gut funktionieren. In diesem Abschnitt konzentrieren wir uns auf drei Benutzeroberflächeneigenschaften: Skalierung, Kontrast und Farbe. Diese Eigenschaften können geändert werden, um die visuelle Benutzeroberfläche zu optimieren.

## <a name="scale-and-brightness"></a>Skalierung und Helligkeit

Im Allgemeinen sind größere Objekte leichter zu erkennen. Wenn sich der Computer unter schädlichen Beleuchtungsbedingungen befindet (z. B. bei direkter Vergrößerung), kann das Vergrößern von Inhalten dazu beitragen, die Lesbarkeit und Interaktivität dieses Inhalts zu verbessern.

Die folgenden Fotos vergleichen einen Laptop in direkter Strahlkraft mit typischer Bildschirmstärke und Zoomstufe mit einem Laptop unter den gleichen Beleuchtungsbedingungen mit lichtbewusster Benutzeroberfläche. Das erste Foto zeigt die Anzeige, die auf 40 % Helligkeit bei normalen Zoomstufen festgelegt ist. Das zweite Foto zeigt die Anzeige, die auf eine Helligkeit von 100 % mit erhöhten Zoomwerten festgelegt ist.

![Laptopanzeige bei 40 % Helligkeit mit normalem Zoomfaktor](images/laptop-40.png)![Laptopanzeige bei einer Helligkeit von 100 % mit erhöhten Zoomwerten](images/laptop-100.png)

### <a name="varying-font-size"></a>Variierender Schriftgrad

Wenn Sie die Schriftgröße erhöhen, die zum Anzeigen von Text verwendet wird, ist der Text bei beeinträchtigungen Beleuchtungsbedingungen lesbarer. Der Schriftschnitt, die Schriftart und andere Merkmale können ebenfalls geändert werden, um lesbarkeit und Lesbarkeit zu optimieren. Beispielsweise sind sans serif-Schriftarten in der Regel einfacher zu lesen als Serifschriftarten.

![sans serif font im Vergleich zur Serifenschriftart](images/fonts.png)

### <a name="zooming-content"></a>Zoomen von Inhalten

Wenn Ihr Programm Zoomen implementiert, kann es zum Skalieren des Inhalts verwendet werden. Das Vergrößern verbessert die Lesbarkeit, während das Verkleinern dem Programm ermöglicht, mehr Inhalt anzuzeigen.

### <a name="altering-vector-graphic-rendering-properties"></a>Ändern von Vektorgrafik-Renderingeigenschaften

Wenn Ihr Programm Vektorgrafikprimitiven (z. B. Linien, Kreise usw.) rendert, können die Merkmale des Renderings geändert werden, um die Lesbarkeit zu optimieren. Wenn Ihr Programm beispielsweise Rechtecke rendert, kann die Breite der Linien, die zum Rendern der Rechtecke verwendet werden, skaliert werden (breiter für Außenanlagen und schmaler für Gebäude), um die Darstellung und Lesbarkeit des Vektorgrafikinhalts zu optimieren.

## <a name="contrast"></a>Vergleichen Sie

Bei Verwendung von DISPLAYS-Bildschirmen bei hellem Licht wird der Gesamtkontrast des Bildschirms reduziert. Wenn der Bildschirm mit Licht überflutet wird (z. B. von der So scheint), wird die Wahrnehmung von dunklen Bereichen auf dem Bildschirm reduziert. Im Allgemeinen ist es wichtig, den Kontrast von Inhalt und Benutzeroberfläche zu erhöhen, wenn das Umgebungslicht hell ist. Es kann wünschenswert sein, ein monocolores Farbschema zu verwenden, um den Kontrast in diesen Beleuchtungsbedingungen zu maximieren. Eine weitere Möglichkeit, den Kontrast zu erhöhen, besteht darin, Inhalte mit geringem Kontrast (z. B. einen Luftfotomodus in einem Zuordnungsprogramm) durch Elemente mit hohem Kontrast (z. B. den Grafikmodus "Schwarz auf Weiß" für Straßenvektoren) zu ersetzen.

## <a name="color"></a>Color

Die Farben, die ein Programm zum Anzeigen seines Inhalts verwendet, können sich drastisch auf die Allgemeine Benutzerfreundlichkeit und Lesbarkeit gerenderten Inhalts auswirken. Indem Sie den Farbkontrast basierend auf Umgebungslicht ändern, können Sie Inhalte bei schädlichen Beleuchtungsbedingungen besser lesbar machen, z. B. helles Außenlicht oder dunkles inneres Licht.

Eine Möglichkeit, den Farbkontrast zu erhöhen, ist die Farbsättigung. Eine andere Möglichkeit besteht darin, ergänzende Farben anstelle benachbarter Farben zu verwenden, um die Lesbarkeit zu verbessern. Ergänzende Farben sind Farbpaare mit entgegengesetztem Farbton, z. B. Blau und Gelb. Das folgende parallele Beispiel zeigt, wie die Verwendung von ergänzenden Farben zur Verbesserung des Farbkontrasts beitragen kann.

![Beispiel für die Auswirkungen der Textfarbe auf die Lesbarkeit.](images/color.png)

 

 



