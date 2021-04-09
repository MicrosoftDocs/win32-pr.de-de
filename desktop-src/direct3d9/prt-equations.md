---
description: Um einen Shader, der PRT implementiert, vollständig zu verstehen, ist es hilfreich, die Formel abzuleiten, die der Shader zum Berechnen der Ausgangs Strahlung verwendet.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: PRT-Gleichungen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65559fada82fda7f7eed1c7d05543883a06a19e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124819"
---
# <a name="prt-equations-direct3d-9"></a>PRT-Gleichungen (Direct3D 9)

Um einen Shader, der PRT implementiert, vollständig zu verstehen, ist es hilfreich, die Formel abzuleiten, die der Shader zum Berechnen der Ausgangs Strahlung verwendet.

Um zu beginnen, ist die folgende Gleichung die allgemeine Gleichung zur Berechnung der Beendigungs Strahlen, die sich aus der direkten Beleuchtung eines diffusen Objekts mit willkürlicher, entfernter Beleuchtung ergibt.

![Gleichung der Beendigungs Strahlung, die sich aus der direkten Beleuchtung eines diffusen Objekts mit willkürlicher, entfernter Beleuchtung ergibt](images/prt-theory-eq1.png)

Dabei gilt Folgendes:



| Parameter     | BESCHREIBUNG                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| Neutraler            | Der Ausgangs Glanz bei Scheitelpunkt p. Ausgewertet an jedem Scheitelpunkt im Mesh.                                   |
| p<sub>d</sub> | Die Albedo der Oberfläche.                                                                              |
| pi            | Eine Konstante, die als normalisierungs Faktor für die Energieeinsparung verwendet wird.                                        |
| L (s)          | Die Beleuchtungs Umgebung (Quell Ausstrahlung).                                                             |
| VP ₍ s ₎         | Eine binäre Sichtbarkeits Funktion für Punkt p. Der Wert ist 1, wenn der Punkt das Licht sehen kann, andernfalls 0.             |
| HNP ₍ s ₎        | Der Kosinus Begriff von Lambert-Gesetz. Gleich max ((NP = s), 0), wobei NP die Oberflächen normale an Punkt p ist. |
| s             | Die Variable, die in die Kugel integriert ist.                                                           |



 

Durch die Verwendung von sphärischen Basisfunktionen, wie z. b. sphärischen Harmonics, gleicht die folgende Gleichung der Beleuchtungs Umgebung

![Gleichung der Beleuchtungs Umgebung](images/prt-theory-eq2.png)

Dabei gilt Folgendes:



| Parameter        | BESCHREIBUNG                                              |
|------------------|----------------------------------------------------------|
| L (s)             | Die Beleuchtungs Umgebung (Quell Ausstrahlung).              |
| i                | Eine ganze Zahl, die die Anzahl der Basisfunktionen summiert. |
| O                | Die Reihenfolge der sphärischen Harmonics.                        |
| l<sub>i</sub>    | Ein Koeffizient.                                           |
| Y<sub>i (s)</sub> | Eine Basis Funktion über der Kugel.                     |



 

Die Auflistung dieser Koeffizienten, L ", bietet die optimale Näherung für die Funktion l (s) mit den Basisfunktionen Y (s). Durch ersetzen und verteilen ergibt sich die folgende Gleichung.

![Gleichung der Beendigungs Strahlung nach dem Ersetzen von l (s) und verteilen](images/prt-theory-eq3.png)

Der integrale Wert von Y<sub>i (s)</sub>VP ₍ s ₎ HNP ₍ s ₎ ist ein Transfer Koeffizienten t<sub>Pi</sub> , den der Simulator für jeden Scheitelpunkt im Mesh vorberechnet. Wenn Sie ersetzen, wird die folgende Gleichung erzeugt.

![Gleichung der Beendigungs Glanz, nachdem der Übertragungskoeffizienten ersetzt wurde.](images/prt-theory-eq4.png)

Wenn Sie dies in eine Vektor Notation ändern, ergibt sich die folgende nicht komprimierte Gleichung, um die Ausgangs Glanz für jeden Kanal zu berechnen

![Gleichung der Beendigungs Strahlung nach dem Wechsel zur Vektor Notation](images/prt-theory-eq5.png)

Dabei gilt Folgendes:



| Parameter     | BESCHREIBUNG                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Neutraler            | Der Ausgangs Glanz bei Scheitelpunkt p.                                                                                                                                                      |
| p<sub>d</sub> | Die Albedo der Oberfläche.                                                                                                                                                          |
| Int            | Der Vektor von l<sub>i</sub>und ist die Projektion der Quell Ausstrahlung in die kugelförmigen harmonischen Basisfunktionen. Dies ist ein Order ²-Vektor mit sphärischen harmonischen Koeffizient. |
| TP            | Ein "Order ²"-Übertragungs Vektor für Vertex p. Der Simulator dividiert die Übertragungskoeffizienten durch p.                                                                                       |



 

Beide Vektoren sind ein Order ²-Vektor mit sphärischen harmonischen Koeffizienten. Beachten Sie, dass es sich hierbei einfach um ein Punktprodukt handelt. Abhängig von der Bestellung kann der Punkt teuer sein, sodass die Komprimierung verwendet werden kann. Mit einem Algorithmus namens "Clustered Principal Component Analysis (CPCA)" werden die Daten effizient komprimiert. Dies ermöglicht die Verwendung einer sphärischen harmonischen Näherung höherer Ordnung, was zu schärferen Schatten führt.

CPCA stellt die folgende Gleichung bereit, um den Übertragungs Vektor anzugleichen.

![Gleichung des ungefäckten Übertragungs Vektors](images/prt-theory-eq6.png)

Dabei gilt Folgendes:



| Parameter      | BESCHREIBUNG                                          |
|----------------|------------------------------------------------------|
| TP             | Der Übertragungs Vektor für Scheitelpunkt p.                    |
| Gegründete             | Der Mittelwert für Cluster k.                              |
| j              | Eine ganze Zahl, die die Anzahl der PCA-Vektoren summiert. |
| N              | Die Anzahl der PCA-Vektoren.                           |
| w-<sub>PJ</sub> | Die Jth-PCA-Gewichtung für Punkt p.                      |
| B-<sub>kJ</sub> | Der Jth PCA-Basis Vektor für Cluster k.              |



 

Ein Cluster ist einfach eine bestimmte Anzahl von Vertices, die denselben Mittel Vektor verwenden. Im folgenden wird erläutert, wie der Cluster Mittelwert, die PCA-Gewichtungen, die PCA-Basis Vektoren und die Cluster-IDs für die Scheitel Punkte erläutert werden.

Durch diese beiden Gleichungen ergibt sich Folgendes:

![Gleichung der Beendigungs Glanz, nachdem der Übertragungs Vektor ersetzt wurde.](images/prt-theory-eq7.png)

Anschließend ergibt die Verteilung des Punkt Produkts die folgende Gleichung.

![Gleichung der Beendigungs Glanz nach der Verteilung des Punkt Produkts](images/prt-theory-eq8.png)

Da beide (MK) L ') und (B<sub>kJ</sub>) L ') sind konstant pro Scheitelpunkt. das Beispiel berechnet diese Werte mit der CPU und übergibt sie als Konstanten an den Vertexshader. Da sich w<sub>PJ</sub> für jeden Scheitelpunkt ändert, speichert das Beispiel diese pro-Vertex-Daten im Scheitelpunkt Puffer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Voraus berechnete Strahlungs Übertragung](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



