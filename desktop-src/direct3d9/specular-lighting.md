---
description: Das Modellieren von Glanz Reflektion erfordert, dass das System nicht nur weiß, in welcher Richtung das Licht unterwegs ist, sondern auch die Richtung des Viewers.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Glanz Beleuchtung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab378d4ca3f00ef81c5048e6ad6cc85eaeb18ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569457"
---
# <a name="specular-lighting-direct3d-9"></a>Glanz Beleuchtung (Direct3D 9)

Das Modellieren von Glanz Reflektion erfordert, dass das System nicht nur weiß, in welcher Richtung das Licht unterwegs ist, sondern auch die Richtung des Viewers. Das System verwendet eine vereinfachte Version des Phong-reflektionsmodells, das einen halben Vektor verwendet, um die Intensität der Glanz Reflektion zu annähern.

Der Standard Beleuchtungs Zustand berechnet keine Glanzlichter. Um die Glanz Beleuchtung zu aktivieren, stellen Sie sicher, dass D3DRS \_ specularenable auf **true** festgelegt ist.

## <a name="specular-lighting-equation"></a>Glanzlicht Gleichung

Die Glanz Beleuchtung wird durch die folgende Gleichung beschrieben.



|                                                                             |
|-----------------------------------------------------------------------------|
| Glanz Beleuchtung = CS \* Sum \[ ls \* (N) H)<sup>P</sup> \* - \* Punkt-Punkt\] |



 

In der folgenden Tabelle werden die Variablen, ihre Typen und ihre Bereiche aufgeführt.



| Parameter    | Standardwert | type          | BESCHREIBUNG                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| CS           | (0, 0, 0, 0)     | D3DCOLORVALUE | Glanz Farbe.                                                                                                     |
| Sum          | –           | –           | Sumpunktions Zeichen für die Glanz Komponente der einzelnen Leuchten.                                                                       |
| N            | –           | D3DVECTOR     | Vertex normal.                                                                                                      |
| H            | –           | D3DVECTOR     | Halber-Wege-Vektor. Weitere Informationen finden Sie im Abschnitt zum halben Vektor.                                                             |
| <sup>P</sup> | 0,0           | GLEITKOMMAZAHL         | Glanz Fähigkeit der Reflektion. Der Bereich liegt zwischen 0 und + unendlich.                                                                  |
| Ls           | (0, 0, 0, 0)     | D3DCOLORVALUE | Helle Glanz Farbe.                                                                                               |
| Ratte        | –           | GLEITKOMMAZAHL         | Heller Dämpfungswert. Siehe [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| Sofortige Zahlung         | –           | GLEITKOMMAZAHL         | Spotlight-Faktor. Siehe [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md).        |



 

Der Wert für CS lautet wie folgt:


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   Vertex color1, wenn die Glanz materialquelle D3DMCS \_ color1 und die erste Scheitelpunkt Farbe in der Scheitelpunkt Deklaration angegeben wird.
-   Vertex color2, wenn die Glanz materialquelle D3DMCS \_ color2 ist, und die zweite Scheitelpunkt Farbe in der Vertex-Deklaration angegeben wird.
-   Material Glanz Farbe

> [!Note]  
> Wenn eine der beiden Optionen für die Quell Text Quelle verwendet wird und die Scheitelpunkt Farbe nicht angegeben wird, wird die Glanz Farbe für das Material verwendet.

 

Glanz Komponenten werden an einen Wert zwischen 0 und 255 gebunden, nachdem alle Lichter separat verarbeitet und interpoliert wurden.

## <a name="the-halfway-vector"></a>Der halbe Vektor

Der halbe Vektor (H) ist in der Mitte zwischen zwei Vektoren vorhanden: der Vektor von einem Objekt Scheitelpunkt zur hellen Quelle und der Vektor von einem Objekt Scheitelpunkt bis zur Kameraposition. Direct3D bietet zwei Möglichkeiten, den halbvektor zu berechnen. Wenn D3DRS \_ localviewer auf **true** festgelegt ist, berechnet das System den halben Vektor mithilfe der Position der Kamera und der Position des Scheitel Punkts, zusammen mit dem Richtungsvektor des Lichts. Dies wird in der folgenden Formel veranschaulicht.



|                                           |
|-------------------------------------------|
| H = Norm (Norm (CP-VP) + L-<sub>dir</sub>) |



 



| Parameter       | Standardwert | type      | BESCHREIBUNG                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| Erfolgen              | –           | D3DVECTOR | Kameraposition.                                             |
| Füttern              | –           | D3DVECTOR | Vertex-Position.                                             |
| L-<sub>dir</sub> | –           | D3DVECTOR | Richtung Vektor von Scheitelpunkt Position zur hellen Position. |



 

Die Bestimmung des halb möglichen Vektors auf diese Weise kann Rechen intensiv sein. Alternativ \_ weist das Festlegen von D3DRS localviewer = **false** das System an, so zu agieren, als ob der Standpunkt auf der z-Achse unendlich weit entfernt ist. Dies wird in der folgenden Formel dargestellt.



|                                     |
|-------------------------------------|
| H = Norm ((0,0) + L-<sub>dir</sub>) |



 

Diese Einstellung ist weniger Rechen intensiv, aber weitaus weniger genau. Sie wird daher am besten von Anwendungen verwendet, die eine orthogonale Projektion verwenden.

## <a name="example"></a>Beispiel

In diesem Beispiel wird das-Objekt mithilfe der Glanzlicht Farbe der Szene und einer hellen Glanz Farbe gefärbt. Der Code wird unten dargestellt.


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



Gemäß der Gleichung ist die resultierende Farbe für die Objekt Vertices eine Kombination aus der Material Farbe und der hellen Farbe.

Die folgende Abbildung zeigt die Glanz Farbe, die grau ist, und die helle helle Farbe, die weiß ist.

![Abbildung einer grauen Kugel](images/amb1.jpg)![Abbildung einer weißen Kugel](images/lightwhite.jpg)

Die sich ergebende Glanz Markierung wird in der folgenden Abbildung dargestellt.

![Abbildung der Glanz Markierung](images/lights.jpg)

Die Kombination der Glanz Markierung mit der Ambient-und diffuse Beleuchtung ergibt die folgende Abbildung. Wenn alle drei Arten von Beleuchtung angewendet werden, ähnelt dies deutlich einem realistischen Objekt.

![Darstellung der Kombination der Glanz Markierung, der Umgebungsbeleuchtung und der diffusen Beleuchtung](images/lightads.jpg)

Die Glanz Beleuchtung ist intensiver zu berechnen als diffuses Beleuchtung. Sie wird in der Regel verwendet, um visuelle Hinweise zum Oberflächenmaterial bereitzustellen. Die Glanz Markierung variiert in Größe und Farbe mit dem Material der-Oberfläche.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mathematik der Beleuchtung](mathematics-of-lighting.md)
</dt> </dl>

 

 



