---
description: Um einen Shader, der PRT implementiert, vollständig zu verstehen, ist es hilfreich, die Formel zu leiten, die der Shader zum Berechnen der Beendigungsausdance verwendet.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: PRT-Gleichungen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd3dc716349ce46d4e678f0e408e5c964eb5f01d633649e3d512db6115c0267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798171"
---
# <a name="prt-equations-direct3d-9"></a>PRT-Gleichungen (Direct3D 9)

Um einen Shader, der PRT implementiert, vollständig zu verstehen, ist es hilfreich, die Formel zu leiten, die der Shader zum Berechnen der Beendigungsausdance verwendet.

Zu Beginn ist die folgende Gleichung die allgemeine Gleichung, um die Exitauslösung zu berechnen, die sich aus der direkten Beleuchtung eines diffusen Objekts mit beliebiger entfernter Beleuchtung ergibt.

![Gleichung der Exit-Radiance, die sich aus der direkten Beleuchtung auf einem diffusen Objekt mit beliebiger entfernter Beleuchtung ergibt](images/prt-theory-eq1.png)

Dabei gilt Folgendes:



| Parameter     | Beschreibung                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| Rp            | Die Beendigungsausdance am Scheitelpunkt p. Wird an jedem Scheitelpunkt im Gitternetz ausgewertet.                                   |
| p<sub>d</sub> | Der Albedo der Oberfläche.                                                                              |
| pi            | Eine Konstante, die als Energienormalisierungsfaktor verwendet wird.                                        |
| L(s)          | Die Beleuchtungsumgebung (Quelllicht).                                                             |
| Vp₍s₎         | Eine binäre Sichtbarkeitsfunktion für Punkt p. Es ist 1, wenn der Punkt das Licht sehen kann, 0, wenn nicht.             |
| Hnp₍s₎        | Der Kosinusbegriff aus lamberts Gesetz. Entspricht max((Np· s), 0, wobei Np die Normale Oberfläche an Punkt p ist. |
| s             | Die Variable, die über die Kugel integriert wird.                                                           |



 

Mithilfe von pherischen Basisfunktionen, z. B. pherischen Kugeln, entspricht die folgende Gleichung der Beleuchtungsumgebung.

![Gleichung der Beleuchtungsumgebung](images/prt-theory-eq2.png)

Dabei gilt Folgendes:



| Parameter        | Beschreibung                                              |
|------------------|----------------------------------------------------------|
| L(s)             | Die Beleuchtungsumgebung (Quelllicht).              |
| i                | Eine ganze Zahl, die die Anzahl der Basisfunktionen summiert. |
| O                | Die Reihenfolge der pherischen Trophäen.                        |
| l<sub>i</sub>    | Ein Koeffizient.                                           |
| Y<sub>i(s)</sub> | Eine Basisfunktion über der Kugel.                     |



 

Die Auflistung dieser Koeffizienten, L', stellt die optimale Näherung für Funktion L(s) mit den Basisfunktionen Y(s) zur Verfügung. Das Durchsubstituieren und Verteilen ergibt die folgende Gleichung.

![Gleichung der Exit-Radiance nach dem Ersatz von l(s) und der Verteilung](images/prt-theory-eq3.png)

Das Integral von Y<sub>i(s)</sub>Vp₍s₎Hnp₍s₎ ist ein Übertragungskoeffizient t<sub>pi,</sub> der vom Simulator für jeden Scheitelpunkt im Netz vorbesetzt wird. Durch Dies wird die folgende Gleichung ergeben.

![Gleichung der Beendigungsausdehnung nach dem Ersatz des Übertragungskoeffizienten](images/prt-theory-eq4.png)

Wenn Sie dies in Vektor notation ändern, ergibt sich die folgende unkomprimierte Gleichung, um die Beendigungsausdance für jeden Kanal zu berechnen.

![Gleichung der Exit-Radiance nach dem Wechsel zur Vektor notation](images/prt-theory-eq5.png)

Dabei gilt Folgendes:



| Parameter     | Beschreibung                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rp            | Die Beendigungsausdance am Scheitelpunkt p.                                                                                                                                                      |
| p<sub>d</sub> | Der Albedo der Oberfläche.                                                                                                                                                          |
| L'            | Der Vektor von l<sub>i</sub>und ist die Projektion der Quellauslassung in die pherischen Basisfunktionen der Tropen. Dies ist ein Order-2-Vektor aus pherischen Koeffizienten. |
| Tp            | Ein Order 2-Übertragungsvektor für Scheitelpunkt p. Der Simulator dividiert die Übertragungskoeffizienten durch p.                                                                                       |



 

Beide Vektoren sind ein Order-2-Vektor aus pherischen Koeffizienten. Beachten Sie daher, dass es sich hierbei einfach um ein Punktprodukt handelt. Je nach Reihenfolge kann der Punkt teuer sein, sodass die Komprimierung verwendet werden kann. Ein Algorithmus namens Clustered Principal Component Analysis (CPCA) komprimiert die Daten effizient. Dies ermöglicht die Verwendung einer pherischen näherungsförmigen Näherung höherer Ordnung, was zu schärferen Schatten führt.

CPCA stellt die folgende Gleichung zur Ungefährung des Übertragungsvektors zur Folge.

![Gleichung des ungefähren Übertragungsvektors](images/prt-theory-eq6.png)

Dabei gilt Folgendes:



| Parameter      | Beschreibung                                          |
|----------------|------------------------------------------------------|
| Tp             | Der Übertragungsvektor für Scheitelpunkt p.                    |
| Mk             | Der Mittelwert für Cluster k.                              |
| j              | Eine ganze Zahl, die die Anzahl der PCA-Vektoren summiert. |
| N              | Die Anzahl der PCA-Vektoren.                           |
| w<sub>pj</sub> | Die jth PCA-Gewichtung für Punkt p.                      |
| B<sub>kj</sub> | Der jth PCA-Basisvektor für Cluster k.              |



 

Ein Cluster ist einfach eine Reihe von Scheitelzeichen, die denselben mittleren Vektor verwenden. Im Folgenden wird erläutert, wie Sie den Mittelwert des Clusters, die PCA-Gewichtungen, die PCA-Basisvektoren und die Cluster-IDs für die Scheitelungen erhalten.

Durch die Ersetzung dieser beiden Gleichungen ergibt sich Folgendes:

![Gleichung des Exit-Bogens nach dem Ersatz des Übertragungsvektors](images/prt-theory-eq7.png)

Anschließend ergibt die Verteilung des Punktprodukts die folgende Gleichung.

![Gleichung der Beendigungsausdance nach der Verteilung des Punktprodukts](images/prt-theory-eq8.png)

Da beides (Mk· L') und (B<sub>kj</sub>· L') sind konstant pro Scheitelpunkt. Im Beispiel werden diese Werte mit der CPU berechnet und als Konstanten an den Vertex-Shader übergibt. Da sich<sub>w pj</sub> für jeden Scheitelpunkt ändert, speichert das Beispiel diese Pro-Scheitelpunkt-Daten im Scheitelpunktpuffer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorausberechnungsübertragung der Radiance](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



