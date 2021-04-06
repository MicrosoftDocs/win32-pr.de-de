---
description: Grundlagen der Light-Aware Benutzeroberflächen
ms.assetid: 7ea391cb-f72b-4ac1-99be-c957d4ccc8af
title: Grundlagen der Light-Aware Benutzeroberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ce71ab67e11684d14b188fef7ae73500edb7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758754"
---
# <a name="fundamentals-of-light-aware-user-interfaces"></a>Grundlagen der Light-Aware Benutzeroberflächen

Der Begriff " *Light-Aware UI* " bezieht sich auf ein Programm, das Lichtsensor Daten verwendet, um seinen Inhalt, Steuerelemente und andere Grafiken zu optimieren, um eine optimale Benutzeroberfläche in vielen Beleuchtungsbedingungen zu erzielen, von der Dunkelheit bis hin zum direkten Sonnenlicht. Die wichtigsten Optimierungen sind z. b. Lesbarkeit, Lesbarkeit und Interaktionen bei direkter Sonneneinstrahlung, da Bildschirme in den folgenden Situationen normalerweise nicht gut funktionieren. In diesem Abschnitt konzentrieren wir uns auf drei Eigenschaften der Benutzeroberfläche: Skalierung, Kontrast und Farbe. Diese Eigenschaften können geändert werden, um die visuelle Benutzer Leistung zu optimieren.

## <a name="scale-and-brightness"></a>Skalierung und Helligkeit

Im Allgemeinen sind größere Objekte leichter zu erkennen. Wenn sich der Computer in einer nachteiligen Beleuchtung befindet (z. b. bei direkter Sonneneinstrahlung), kann das Verbessern der Lesbarkeit und Interoperabilität dieser Inhalte helfen.

In den folgenden Fotos wird ein Laptop in direktem Sonnenlicht mit typischer Bildschirmhelligkeit und Zoomstufe für einen Laptop mit einer einfachen Benutzeroberfläche verglichen. Das erste Foto zeigt, dass die Anzeige auf 40% Helligkeit mit normalen Zoomstufen festgelegt ist. Die zweite Abbildung zeigt, dass die Anzeige auf 100% Helligkeit mit erhöhter Zoomstufe festgelegt ist.

![Laptop Anzeige mit einer Helligkeit von 40% mit normalen Zoomstufen](images/laptop-40.png)![Laptop Anzeige bei einer Helligkeit von 100% mit erhöhter Zoomstufe](images/laptop-100.png)

### <a name="varying-font-size"></a>Veränderliche Schriftgröße

Wenn Sie die Schriftart vergrößern, die zum Anzeigen von Text verwendet wird, ist der Text in den negativen Beleuchtungs Zuständen besser lesbar. Schriftart Stil, Schriftart und andere Merkmale können auch unterschiedlich sein, um Lesbarkeit und Lesbarkeit zu optimieren. Sans Serif-Schriftarten sind z. b. in der Regel leichter zu lesen als Serif-Schriftarten.

![Sans-Serif-Schriftart im Vergleich zur Serif-Schriftart](images/fonts.png)

### <a name="zooming-content"></a>Zoomen von Inhalten

Wenn das Programm Zoom implementiert, kann es zum Skalieren des Inhalts verwendet werden. Durch Zoomen in wird die Lesbarkeit verbessert, während Sie vergrößert werden, sodass das Programm mehr Inhalte anzeigen kann.

### <a name="altering-vector-graphic-rendering-properties"></a>Ändern der Eigenschaften von Vektorgrafik Rendering

Wenn das Programm Vektorgrafik primitive (z. b. Linien, Kreise usw.) rendert, können die Merkmale des Renderings geändert werden, um die Lesbarkeit zu optimieren. Wenn das Programm z. b. Rechtecke rendert, kann die Breite der Linien, die zum Rendern der Rechtecke verwendet werden, skaliert werden (für die zwischen-und schmaler), um das Erscheinungsbild und die Lesbarkeit des Vektorgrafik Inhalts zu optimieren.

## <a name="contrast"></a>Vergleichen Sie

Wenn LCD-Bildschirme in hellen Beleuchtungs Zuständen verwendet werden, wird der Bildschirm insgesamt reduziert. Wenn der Bildschirm mit Licht (z. b. von der Sonne) überflutet wird, wird die Wahrnehmung von dunklen Bereichen auf dem Bildschirm reduziert. Im Allgemeinen ist es wichtig, den Kontrast von Inhalten und der Benutzeroberfläche zu vergrößern, wenn das Ambiente hell hell ist. Es kann wünschenswert sein, ein monochromes Farbschema zu verwenden, um Kontrast in diesen Beleuchtungsbedingungen zu maximieren. Eine weitere Möglichkeit, den Kontrast zu erhöhen, besteht darin, Inhalte mit geringem Kontrast (z. b. ein Luftbild Modus in einem Mapping-Programm) durch Elemente mit hohem Kontrast (z. b. der schwarz-auf-weißen Straßen Vektor-Grafikmodus) zu ersetzen.

## <a name="color"></a>Color

Die Farben, die ein Programm zum Anzeigen seiner Inhalte verwendet, können sich drastisch auf die gesamte Benutzerumgebung und die Lesbarkeit gerenderter Inhalte auswirken. Durch Ändern des Farb Kontrasts basierend auf Ambient Light können Sie Inhalte besser lesbar machen, wenn Sie sich gegenseitig besser lesbar machen, z. b. helle oder dunkle innen Leuchten.

Eine Möglichkeit, den Farbkontrast zu erhöhen, ist die Farbsättigung. Eine andere Möglichkeit ist die Verwendung von Komplement Ellen Farben anstelle von angrenzenden Farben, um eine bessere Lesbarkeit zu erzielen. Ergänzende Farben sind Paare von Farben, die gegenüberliegenden Farbton sind, wie z. b. blau und gelb. Im folgenden Beispiel wird gezeigt, wie Sie mit ergänzenden Farben den Farbkontrast verbessern können.

![Beispiel für die Auswirkungen der Textfarbe auf die Lesbarkeit.](images/color.png)

 

 



