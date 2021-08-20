---
description: Die diffusen und specularen Beleuchtungskomponenten der globalen Gleichung enthalten Begriffe, die die Lichtdämpfung und den Spotlight-Kegel beschreiben. Diese Begriffe werden unten beschrieben.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Dämpfung und Spotlight-Faktor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80fff287749e2979a89f2e20c830fdad3961d90ec05bf90a4ee2f6a51f8bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850615"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a>Dämpfung und Spotlight-Faktor (Direct3D 9)

Die diffusen und specularen Beleuchtungskomponenten der globalen Gleichung enthalten Begriffe, die die Lichtdämpfung und den Spotlight-Kegel beschreiben. Diese Begriffe werden unten beschrieben.

## <a name="attenuation"></a>Dämpfung

Die Dämpfung eines Lichts hängt vom Lichttyp und dem Abstand zwischen dem Licht und der Scheitelpunktposition ab. Verwenden Sie eine der folgenden Gleichungen, um die Dämpfung zu berechnen.

Atten = 1/( att0<sub>i</sub> + att1<sub>i</sub> \* d + att2<sub>i</sub> \* d);

Hierbei gilt:



| Parameter        | Standardwert | type  | BESCHREIBUNG                                     | Range          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| att0<sub>i</sub> | 0,0           | GLEITKOMMAZAHL | Konstanter Dämpfungsfaktor                     | 0 bis +unendlich |
| att1<sub>i</sub> | 0,0           | GLEITKOMMAZAHL | Linearer Dämpfungsfaktor                       | 0 bis +unendlich |
| att2<sub>i</sub> | 0,0           | GLEITKOMMAZAHL | Quadratischer Dämpfungsfaktor                    | 0 bis +unendlich |
| d                | Nicht zutreffend           | GLEITKOMMAZAHL | Abstand zwischen Scheitelpunktposition und Lichtposition | Nicht zutreffend            |



 

-   Atten = 1, wenn das Licht ein direktionales Licht ist.
-   Atten = 0, wenn der Abstand zwischen dem Licht und dem Scheitelpunkt den Bereich des Lichts überschreitet.

Die att0-, att1- und att2-Werte werden durch die Attenuation0-, Attenuation1- und Attenuation2-Member von [**D3DLIGHT9 angegeben.**](d3dlight9.md)

Der Abstand zwischen dem Licht und der Scheitelpunktposition ist immer positiv.

d = \| L<sub>dir</sub>\|

Hierbei gilt:



| Parameter       | Standardwert | type      | BESCHREIBUNG                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| L<sub>dir</sub> | Nicht zutreffend           | D3DVECTOR | Richtungsvektor von der Scheitelpunktposition zur Lichtposition |



 

If d is greater than the light's range, that is, the Range member of a [**D3DLIGHT9**](d3dlight9.md) structure, Direct3D makes no further attenuation calculations and applies no effects from the light to the vertex.

Die Dämpfungskonstationen fungieren als Koeffizienten in der Formel. Sie können eine Vielzahl von Dämpfungskurven erzeugen, indem Sie einfache Anpassungen an ihnen vornehmen. Sie können Attenuation1 auf 1.0 festlegen, um ein Licht zu erstellen, das nicht dämpft, aber immer noch durch den Bereich begrenzt ist, oder Sie können mit verschiedenen Werten experimentieren, um verschiedene Dämpfungseffekte zu erzielen.

Die Dämpfung im maximalen Bereich des Lichts ist nicht 0,0. Um zu verhindern, dass Licht plötzlich angezeigt wird, wenn sie sich im Lichtbereich befinden, kann eine Anwendung den Lichtbereich erhöhen. Oder die Anwendung kann Dämpfungskonstationen einrichten, sodass der Dämpfungsfaktor im Lichtbereich nahe bei 0,0 liegt. Der Dämpfungswert wird mit den roten, grünen und blauen Komponenten der Farbe des Lichts multipliziert, um die Intensität des Lichts als Faktor der Entfernung zu einem Scheitelpunkt zu skalieren.

## <a name="spotlight-factor"></a>Spotlight-Faktor

Die folgende Gleichung gibt den Blickpunktfaktor an.

![Gleichung des Blickpunktfaktors](images/dx8light9.png)



| Parameter         | Standardwert | type  | BESCHREIBUNG                              | Range                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| i<sub></sub>   | Nicht zutreffend           | GLEITKOMMAZAHL | Kosinus (Winkel) für Spotlight i            | Nicht zutreffend                      |
| phi<sub>i</sub>   | 0,0           | GLEITKOMMAZAHL | Penumbra-Winkel von Spotlight i im Bogenmaß | \[theta<sub>i</sub>, pi) |
| theta<sub>i</sub> | 0,0           | GLEITKOMMAZAHL | Umbra-Winkel von Spotlight i im Bogenmaß    | \[0, pi)                 |
| Abfall           | 0,0           | GLEITKOMMAZAHL | Fallofffaktor                           | (-infinity, +infinity)   |



 

Hierbei gilt:

gleich = norm(L<sub>dcs</sub>)<sup>.</sup> norm(L<sub>dir</sub>)

und:



| Parameter       | Standardwert | type      | BESCHREIBUNG                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| L<sub>dcs</sub> | Nicht zutreffend           | D3DVECTOR | Das Negative der Lichtrichtung im Kameraraum         |
| L<sub>dir</sub> | Nicht zutreffend           | D3DVECTOR | Richtungsvektor von der Scheitelpunktposition zur Lichtposition |



 

Nach dem Berechnen der Lichtdämpfung berücksichtigt Direct3D ggf. auch Spotlighteffekte, den Winkel, den das Licht von einer Oberfläche reflektiert, und die Reflexion des aktuellen Materials, um die diffusen und specularen Komponenten für diesen Scheitelpunkt zu berechnen. Weitere Informationen finden Sie unter [SpotLight](light-types.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mathematik der Beleuchtung](mathematics-of-lighting.md)
</dt> </dl>

 

 



