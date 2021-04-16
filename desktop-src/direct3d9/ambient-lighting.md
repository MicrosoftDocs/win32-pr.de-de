---
description: Ambient-Beleuchtung bietet eine konstante Beleuchtung für eine Szene.
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: Umgebungsbeleuchtung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991981a9c1d7d24714e7014d08cefeaa94fe20f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523840"
---
# <a name="ambient-lighting-direct3d-9"></a>Umgebungsbeleuchtung (Direct3D 9)

Ambient-Beleuchtung bietet eine konstante Beleuchtung für eine Szene. Alle Objekt Scheitel Punkte werden gleich angezeigt, da Sie nicht von anderen Beleuchtungs Faktoren abhängen, wie z. b. Vertex-normalen, Lichtrichtung, Lichtposition, Bereich oder Dämpfung. Dies ist die schnellste Art von Beleuchtung, liefert jedoch die wenigsten realistischen Ergebnisse. Direct3D enthält eine einzelne globale Ambient-Light-Eigenschaft, die Sie verwenden können, ohne dass ein Licht erstellt werden kann. Alternativ können Sie ein beliebiges helles Objekt festlegen, um Umgebungsbeleuchtung bereitzustellen. Die Umgebungsbeleuchtung für eine Szene wird durch die folgende Gleichung beschrieben.

Ambient lighting = c ₐ \* \[ g ₐ + Sum (Atten<sub>i</sub> \* Spot<sub>i</sub> \* L<sub>AI</sub>)\]

Hierbei gilt:



| Parameter         | Standardwert | type          | BESCHREIBUNG                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| C ₐ                | (0, 0, 0, 0)     | D3DCOLORVALUE | Material Ambient-Farbe                                                                                                         |
| G ₐ                | (0, 0, 0, 0)     | D3DCOLORVALUE | Globale Ambient-Farbe                                                                                                           |
| Atten<sub>i</sub> | (0, 0, 0, 0)     | D3DCOLORVALUE | Helle Dämpfung des ITH-Lichts. Siehe [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| Stelle<sub>ich</sub>  | (0, 0, 0, 0)     | D3DVECTOR     | Der Spotlight-Faktor des ITH-Lichts. Siehe [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md).  |
| Sum               | –           | –           | Summe der Umgebungsbeleuchtung                                                                                                       |
| L<sub>AI</sub>    | (0, 0, 0, 0)     | D3DVECTOR     | Helle Ambient-Farbe des ITH-Lichts                                                                                           |



 

Der Wert für c ₐ lautet wie folgt:

-   Vertex color1, wenn AmbientMaterialSource = D3DMCS \_ color1 und die erste Scheitelpunkt Farbe in der Vertex-Deklaration angegeben wird.
-   Vertex color2, wenn AmbientMaterialSource = D3DMCS \_ color2 und die zweite Scheitelpunkt Farbe in der Scheitelpunkt Deklaration angegeben wird.
-   Material Ambient-Farbe.

> [!Note]  
> Wenn eine der beiden Optionen "AmbientMaterialSource" verwendet wird und die Scheitelpunkt Farbe nicht angegeben wird, wird die Umgebungs Farbe für das Material verwendet.

 

Verwenden Sie setmaterial, um die Material Ambient-Farbe zu verwenden, wie im folgenden Beispielcode gezeigt.

G ₐ ist die globale Umgebungs Farbe. Sie wird mithilfe von setrenderstate (D3DRS \_ AMBIENT) festgelegt. In einer Direct3D-Szene gibt es eine globale Umgebungs Farbe. Dieser Parameter ist keinem Direct3D Light-Objekt zugeordnet.

L<sub>AI</sub> ist die Ambiente-Farbe des ITH-Lichts in der Szene. Jedes Direct3D Light verfügt über eine Reihe von Eigenschaften, von denen eine die Umgebungs Farbe ist. Der Begriff Sum (L<sub>AI</sub>) ist eine Summe aller Ambient-Farben in der Szene.

## <a name="example"></a>Beispiel

In diesem Beispiel wird das-Objekt mithilfe der Szene Ambient Light und einer Material Ambient-Farbe gefärbt.


```
#define GRAY_COLOR  0x00bfbfbf

// create material
D3DMATERIAL9 mtrl;
ZeroMemory(&mtrl, sizeof(mtrl));
mtrl.Ambient.r = 0.75f;
mtrl.Ambient.g = 0.0f;
mtrl.Ambient.b = 0.0f;
mtrl.Ambient.a = 0.0f;
m_pd3dDevice->SetMaterial(&mtrl);
m_pd3dDevice->SetRenderState(D3DRS_AMBIENT, GRAY_COLOR);
```



Gemäß der Gleichung ist die resultierende Farbe für die Objekt Vertices eine Kombination aus der Material Farbe und der hellen Farbe.

Die beiden folgenden Abbildungen zeigen die Material Farbe, die grau ist, und die helle Farbe, die hell rot ist.

![Abbildung einer grauen Kugel](images/amb1.jpg)![Abbildung einer roten Kugel](images/lightred.jpg)

Die resultierende Szene wird in der folgenden Abbildung dargestellt. Das einzige Objekt in der Szene ist eine Kugel. Ambient Light beleuchtet alle Objekt Scheitel Punkte mit der gleichen Farbe. Er ist nicht abhängig von der Scheitelpunkt normalen oder der Lichtrichtung. Folglich sieht die Kugel wie ein 2D-Kreis aus, da es keinen Unterschied gibt, um die Oberfläche des Objekts zu schattieren.

![Abbildung einer Kugel mit Umgebungsbeleuchtung](images/lighta.jpg)

Um Objekten einen realistischeren Einblick zu verschaffen, wenden Sie zusätzlich zur Umgebungsbeleuchtung diffuse oder Glanzlichter an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mathematik der Beleuchtung](mathematics-of-lighting.md)
</dt> </dl>

 

 



