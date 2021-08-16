---
description: Das Modellieren von Glanzreflektion erfordert, dass das System nicht nur weiß, in welche Richtung Licht bewegt wird, sondern auch die Richtung zum Auge des Betrachters.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Glanzlicht (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84597b63ebd064fbe27ae90b673e9c91166be96f6f45b039ba29a16de9011054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520181"
---
# <a name="specular-lighting-direct3d-9"></a>Glanzlicht (Direct3D 9)

Das Modellieren von Glanzreflektion erfordert, dass das System nicht nur weiß, in welche Richtung Licht bewegt wird, sondern auch die Richtung zum Auge des Betrachters. Das System verwendet eine vereinfachte Version des Phong-Spiegelungsmodells, das einen Halbvektor verwendet, um die Intensität der Glanzreflektion anzunähern.

Der Standardlichtzustand berechnet keine Glanzlichter. Um die Glanzlichterung zu aktivieren, stellen Sie sicher, dass D3DRS \_ SPECULARENABLE auf TRUE festgelegt **ist.**

## <a name="specular-lighting-equation"></a>Glanzlichtgleichung

Specular Lighting wird durch die folgende Gleichung beschrieben:

**Specular Lighting = Cs \* sum \[ Ls \* (N · H)<sup>P</sup> \* Atten \* Spot\]**



 

In der folgenden Tabelle sind die Variablen, ihre Typen und ihre Bereiche aufgeführt.



| Parameter    | Standardwert | Typ          | Beschreibung                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| Cs           | (0,0,0,0)     | D3DCOLORVALUE | Glanzfarbe.                                                                                                     |
| Sum          | Nicht zutreffend           | Nicht zutreffend           | Summierung der Glanzkomponente jedes Lichts.                                                                       |
| N            | Nicht zutreffend           | D3DVECTOR     | Scheitelpunktnorm normal.                                                                                                      |
| H            | Nicht zutreffend           | D3DVECTOR     | Halber Vektor. Weitere Informationen finden Sie im Abschnitt zur Hälfte des Vektors.                                                             |
| <sup>P</sup> | 0,0           | GLEITKOMMAZAHL         | Glanzreflektionsleistung. Der Bereich ist 0 bis +unendlich.                                                                  |
| Ls           | (0,0,0,0)     | D3DCOLORVALUE | Helle Glanzfarbe.                                                                                               |
| Atten        | Nicht zutreffend           | GLEITKOMMAZAHL         | Leichter Dämpfungswert. Weitere Informationen finden Sie [unter Dämpfung und Spotlight-Faktor (Direct3D 9).](attenuation-and-spotlight-factor.md) |
| Sofortige Zahlung         | Nicht zutreffend           | GLEITKOMMAZAHL         | Spotlight-Faktor. Weitere Informationen finden Sie [unter Dämpfung und Spotlight-Faktor (Direct3D 9).](attenuation-and-spotlight-factor.md)        |



 

Der Wert für Cs lautet:


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   vertex color1, wenn die Spiegelmaterialquelle D3DMCS COLOR1 ist \_ und die erste Scheitelpunktfarbe in der Scheitelpunktdeklaration angegeben wird.
-   vertex color2, wenn die Spiegelmaterialquelle D3DMCS COLOR2 ist \_ und die zweite Scheitelpunktfarbe in der Scheitelpunktdeklaration angegeben wird.
-   material specular color (Materialspekularfarbe)

> [!Note]  
> Wenn eine der beiden Quelloptionen für Glanzmaterialien verwendet wird und die Scheitelpunktfarbe nicht angegeben wird, wird die Materialspekularfarbe verwendet.

 

Glanzkomponenten werden so klammert, dass sie von 0 bis 255 liegen, nachdem alle Beleuchtungen separat verarbeitet und interpoliert wurden.

## <a name="the-halfway-vector"></a>Der Halbwegvektor

Der halbe Vektor (H) befindet sich in der Mitte zwischen zwei Vektoren: der Vektor von einem Objektvertex zur Lichtquelle und der Vektor von einem Objektvertex zur Kameraposition. Direct3D bietet zwei Möglichkeiten, den Halbvektor zu berechnen. Wenn D3DRS \_ LOCALVIEWER auf **TRUE** festgelegt ist, berechnet das System den Halbvektor anhand der Position der Kamera und der Position des Scheitelpunkts zusammen mit dem Richtungsvektor des Lichts. Die folgende Formel veranschaulicht dies.

**H = norm(norm(Cp - Vp) + L <sub>dir</sub>)**



 



| Parameter       | Standardwert | Typ      | Beschreibung                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| Cp              | Nicht zutreffend           | D3DVECTOR | Kameraposition.                                             |
| Vp              | Nicht zutreffend           | D3DVECTOR | Vertexposition.                                             |
| L<sub>dir</sub> | Nicht zutreffend           | D3DVECTOR | Richtungsvektor von der Scheitelpunktposition zur Lichtposition. |



 

Die Bestimmung des Halbvektors auf diese Weise kann rechenintensiv sein. Alternativ dazu weist das Festlegen von D3DRS \_ LOCALVIEWER = **FALSE** das System an, so zu handeln, als ob der Blickpunkt auf der Z-Achse unendlich weit entfernt ist. Dies wird in der folgenden Formel widergespiegelt.

**H = norm((0,0,1) + L <sub>dir</sub>)**



 

Diese Einstellung ist weniger rechenintensiv, aber viel weniger genau, daher wird sie am besten von Anwendungen verwendet, die eine orthogonale Projektion verwenden.

## <a name="example"></a>Beispiel

In diesem Beispiel wird das Objekt mithilfe der Szenen-Glanzlichtfarbe und einer materialen Glanzfarbe farbig farbig dargestellt. Der Code ist unten dargestellt.


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

light.Specular.r = 1.0f;
light.Specular.g = 1.0f;
light.Specular.b = 1.0f;
light.Specular.a = 1.0f;

light.Range = 1000;
light.Falloff = 0;
light.Attenuation0 = 1;
light.Attenuation1 = 0;
light.Attenuation2 = 0;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );
m_pd3dDevice->SetRenderState( D3DRS_SPECULARENABLE, TRUE );

mtrl.Specular.r = 0.5f;
mtrl.Specular.g = 0.5f;
mtrl.Specular.b = 0.5f;
mtrl.Specular.a = 0.5f;
mtrl.Power = 20;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_SPECULARMATERIALSOURCE, D3DMCS_MATERIAL);
```



Gemäß der Gleichung ist die resultierende Farbe für die Objektvertices eine Kombination aus der Materialfarbe und der hellen Farbe.

Die folgenden beiden Abbildungen zeigen die Farbe des Glanzmaterials , die grau ist, und die Glanzlichtfarbe, die weiß ist.

![Abbildung einer grauen Kugel](images/amb1.jpg)![Abbildung einer weißen Kugel](images/lightwhite.jpg)

Die resultierende Glanzlichtermarkerung wird in der folgenden Abbildung dargestellt.

![Abbildung des Glanzlichts](images/lights.jpg)

Die Kombination des Glanzlichts mit der Umgebungs- und diffusen Beleuchtung erzeugt die folgende Abbildung. Wenn alle drei Arten von Beleuchtung angewendet werden, ähnelt dies eindeutiger einem realistischen Objekt.

![Abbildung der Kombination von Glanzlicht, Umgebungslicht und diffuser Beleuchtung](images/lightads.jpg)

Die Berechnung der Glanzlichter ist aufwendiger als die diffuse Beleuchtung. Es wird in der Regel verwendet, um visuelle Hinweise zum Oberflächenmaterial bereitzustellen. Die Glanzlichter unterscheiden sich in Größe und Farbe mit dem Material der Oberfläche.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mathematik der Beleuchtung](mathematics-of-lighting.md)
</dt> </dl>

 

 



