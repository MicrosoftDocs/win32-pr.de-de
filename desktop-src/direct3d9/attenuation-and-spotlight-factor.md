---
description: Die diffusen und Glanzlicht Komponenten der globalen Beleuchtungs Gleichung enthalten Begriffe, die die Licht Dämpfung und den Spotlight-Kegel beschreiben. Diese Begriffe werden unten beschrieben.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Dämpfung und Spotlight-Faktor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bb3cb2b1c2a3ee9e0e5d9419ff71dd9a303b6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550282"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a>Dämpfung und Spotlight-Faktor (Direct3D 9)

Die diffusen und Glanzlicht Komponenten der globalen Beleuchtungs Gleichung enthalten Begriffe, die die Licht Dämpfung und den Spotlight-Kegel beschreiben. Diese Begriffe werden unten beschrieben.

## <a name="attenuation"></a>Dämpfung

Die Dämpfung eines Lichts hängt von der Art des Lichts und der Entfernung zwischen dem Licht und der Scheitelpunkt Position ab. Verwenden Sie zum Berechnen der Dämpfung eine der folgenden Gleichungen.

Atten = 1/(att0<sub>i</sub> + Att1<sub>i</sub> \* d + att2<sub>i</sub> \* d ²)

Hierbei gilt:



| Parameter        | Standardwert | type  | BESCHREIBUNG                                     | Range          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| att0<sub>i</sub> | 0,0           | GLEITKOMMAZAHL | Faktor für konstante Dämpfung                     | 0 bis + unendlich |
| Att1<sub>i</sub> | 0,0           | GLEITKOMMAZAHL | Faktor für lineare Dämpfung                       | 0 bis + unendlich |
| att2<sub>i</sub> | 0,0           | GLEITKOMMAZAHL | Faktor für die quadratische Dämpfung                    | 0 bis + unendlich |
| d                | –           | GLEITKOMMAZAHL | Abstand zwischen Scheitelpunkt Position und heller Position | –            |



 

-   Atten = 1, wenn das Licht ein Direktionales Licht ist.
-   Atten = 0, wenn der Abstand zwischen dem Licht und dem Scheitelpunkt den hellen Bereich überschreitet.

Die att0-, Att1-, att2-Werte werden von den Attenuation0-, Attenuation1-und Attenuation2-Membern von [**D3DLIGHT9**](d3dlight9.md)angegeben.

Der Abstand zwischen dem Licht und der Scheitelpunkt Position ist immer positiv.

d = \| L-<sub>dir</sub>\|

Hierbei gilt:



| Parameter       | Standardwert | type      | BESCHREIBUNG                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| L-<sub>dir</sub> | –           | D3DVECTOR | Richtung Vektor von Scheitelpunkt Position zur hellen Position |



 

Wenn d größer ist als der Bereich des Lichts, d. h. der Bereichs Member einer [**D3DLIGHT9**](d3dlight9.md) -Struktur, führt Direct3D keine weiteren Dämpfung-Berechnungen durch und wendet keine Auswirkungen vom Licht auf den Scheitelpunkt an.

Die Dämpfungs Konstanten fungieren als Koeffizienten in der Formel. Sie können eine Vielzahl von Dämpfungs Kurven erstellen, indem Sie einfache Anpassungen vornehmen. Sie können Attenuation1 auf 1,0 festlegen, um ein Licht zu erstellen, das nicht abgeschwächt wird, aber weiterhin durch den Bereich beschränkt ist, oder Sie können mit verschiedenen Werten experimentieren, um verschiedene Dämpfungseffekte zu erzielen.

Die Dämpfung im maximalen Bereich des Lichts ist nicht 0,0. Um zu verhindern, dass Glühbirnen plötzlich angezeigt werden, wenn Sie sich im hellen Bereich befinden, kann eine Anwendung den hellen Bereich vergrößern. Oder die Anwendung kann Dämpfungs Konstanten einrichten, sodass der Faktor für die Dämpfung fast 0,0 am hellen Bereich liegt. Der Wert für die Dämpfung wird mit den roten, grünen und blauen Komponenten der hellen Farbe multipliziert, um die Intensität des Lichts als Faktor der Entfernung zu einem Scheitelpunkt zu skalieren.

## <a name="spotlight-factor"></a>Spotlight-Faktor

Die folgende Gleichung gibt den Spotlight-Faktor an.

![Gleichung des Spotlight-Faktors](images/dx8light9.png)



| Parameter         | Standardwert | type  | BESCHREIBUNG                              | Range                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| Rho<sub>i</sub>   | –           | GLEITKOMMAZAHL | Kosinus (Winkel) für Spotlight i            | –                      |
| Phi<sub>i</sub>   | 0,0           | GLEITKOMMAZAHL | Pendel Winkel von Spotlight i im Bogenmaße | \[-TA<sub>i</sub>, PI) |
| die<sub>i</sub> | 0,0           | GLEITKOMMAZAHL | Der Umschlag Winkel von Spotlight i im Bogenmaße    | \[0, PI)                 |
| Übergang           | 0,0           | GLEITKOMMAZAHL | Zuordnung der Rolle                           | (-unendlich, + unendlich)   |



 

Hierbei gilt:

Rho = Norm (L<sub>DCS</sub>)<sup>.</sup> Norm (L-<sub>dir</sub>)

und:



| Parameter       | Standardwert | type      | BESCHREIBUNG                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| L-<sub>DCS</sub> | –           | D3DVECTOR | Das negative der Lichtrichtung im Kamerabereich         |
| L-<sub>dir</sub> | –           | D3DVECTOR | Richtung Vektor von Scheitelpunkt Position zur hellen Position |



 

Nach dem Berechnen der Licht Dämpfung werden bei Direct3D auch Spotlight-Effekte berücksichtigt, der Winkel, den das Licht von einer Oberfläche reflektiert, und die Reflektion des aktuellen Materials, um die diffusen und Glanz Komponenten für diesen Scheitelpunkt zu berechnen. Weitere Informationen finden Sie unter [Spotlight](light-types.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mathematik der Beleuchtung](mathematics-of-lighting.md)
</dt> </dl>

 

 



