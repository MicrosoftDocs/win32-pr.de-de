---
description: Nach der Anpassung der Lichtintensität für alle Dämpfungseffekte berechnet die Beleuchtungs-Engine, wie viel von dem verbleibenden Licht von einem Scheitelpunkt reflektiert wird, wenn der Winkel des Scheitel Punkts normal und die Richtung des Vorfall Lichts angezeigt wird.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Diffuse Beleuchtung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51e45093786348aaa115ec38c420acec471f718
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123374"
---
# <a name="diffuse-lighting-direct3d-9"></a>Diffuse Beleuchtung (Direct3D 9)

Nach der Anpassung der Lichtintensität für alle Dämpfungseffekte berechnet die Beleuchtungs-Engine, wie viel von dem verbleibenden Licht von einem Scheitelpunkt reflektiert wird, wenn der Winkel des Scheitel Punkts normal und die Richtung des Vorfall Lichts angezeigt wird. Die Beleuchtungs-Engine überspringt diesen Schritt für direktionale Lichter, da Sie nicht über die Entfernung gedämpft werden. Das System berücksichtigt zwei reflektionstypen (diffuses und Glanz) und verwendet eine andere Formel, um zu bestimmen, wie viel Licht für jede reflektiert wird. Nach dem Berechnen der Menge an Licht, die reflektiert wird, wendet Direct3D diese neuen Werte auf die diffusen und Glanz enden Reflectance-Eigenschaften des aktuellen Materials an. Die sich ergebenden Farbwerte sind die diffusen und Glanz baren Komponenten, die vom Raster verwendet werden, um die Schattierung und Glanz Markierung von Gouraud zu schaffen.

Diffuses Beleuchtung wird durch die folgende Gleichung beschrieben.

Diffuse Beleuchtung = Sum \[ C<sub>d</sub> \* L<sub>d</sub> \* (N)<sup>.</sup> L<sub>dir</sub>) \* \* Punktposition\]



| Parameter       | Standardwert | type          | BESCHREIBUNG                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| Sum             | –           | –           | Sumdieren der diffusen Komponente jeder Beleuchtung.                                                                  |
| C<sub>d</sub>   | (0, 0, 0, 0)     | D3DCOLORVALUE | Diffuse Farbe.                                                                                                |
| L<sub>d</sub>   | (0, 0, 0, 0)     | D3DCOLORVALUE | Helle diffuse Farbe.                                                                                          |
| N               | –           | D3DVECTOR     | Scheitelpunkt normal                                                                                                 |
| L-<sub>dir</sub> | –           | D3DVECTOR     | Richtung Vektor von Objekt Scheitelpunkt zu Licht.                                                             |
| Ratte           | –           | GLEITKOMMAZAHL         | Licht Dämpfung. Siehe [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| Sofortige Zahlung            | –           | GLEITKOMMAZAHL         | Spotlight-Faktor. Siehe [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md).  |



 

Der Wert für C<sub>d</sub> ist entweder:

-   Vertex color1, wenn DiffuseMaterialSource = D3DMCS \_ color1 und die erste Scheitelpunkt Farbe in der Vertex-Deklaration angegeben wird.
-   Vertex color2, wenn DiffuseMaterialSource = D3DMCS \_ color2 und die zweite Scheitelpunkt Farbe in der Vertex-Deklaration angegeben wird.
-   Material diffuse Farbe

> [!Note]  
> Wenn eine der beiden Optionen DiffuseMaterialSource verwendet wird und die Scheitelpunkt Farbe nicht angegeben wird, wird die diffuse Farbe des Materials verwendet.

 

Informationen zum Berechnen der Dämpfungs-oder Spotlight-Merkmale (Spot) finden Sie unter [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md).

Bei diffusen Komponenten wird der Wert zwischen 0 und 255 gebunden, nachdem alle Lichter separat verarbeitet und interpoliert wurden. Der resultierende diffuses Beleuchtungs Wert ist eine Kombination aus Ambient-, diff-und selbst leuchtendes-hellen Werten.

## <a name="example"></a>Beispiel

In diesem Beispiel wird das-Objekt mithilfe der hellen diffusen Farbe und einer Material diffusen Farbe gefärbt. Der Code wird unten dargestellt.


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

// set directional light diffuse color
light.Diffuse.r = 1.0f;
light.Diffuse.g = 1.0f;
light.Diffuse.b = 1.0f;
light.Diffuse.a = 1.0f;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );

// if a material is used, SetRenderState must be used
// vertex color = light diffuse color * material diffuse color
mtrl.Diffuse.r = 0.75f;
mtrl.Diffuse.g = 0.0f;
mtrl.Diffuse.b = 0.0f;
mtrl.Diffuse.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL);
```



Gemäß der Gleichung ist die resultierende Farbe für die Objekt Vertices eine Kombination aus der Material Farbe und der hellen Farbe.

Die beiden folgenden Abbildungen zeigen die Material Farbe, die grau ist, und die helle Farbe, die hell rot ist.

![Abbildung einer grauen Kugel](images/amb1.jpg)![Abbildung einer roten Kugel](images/lightred.jpg)

Die resultierende Szene wird in der folgenden Abbildung dargestellt. Das einzige Objekt in der Szene ist eine Kugel. Bei der Berechnung der diffusen Beleuchtung werden das Material und die helle diffuse Farbe geändert und mit dem Punktprodukt um den Winkel zwischen der Lichtrichtung und dem Scheitelpunkt (Scheitelpunkt) geändert. Folglich wird die Rückseite der Kugel dunkler, wenn sich die Oberfläche der Kugel von der Lichtfläche Weg lässt.

![Abbildung einer Kugel mit diffuses Beleuchtung](images/lightd.jpg)

Durch die Kombination der diffusen Beleuchtung mit der Ambient-Beleuchtung aus dem vorherigen Beispiel wird die gesamte Oberfläche des Objekts schattiert. Die Umgebungsbeleuchtung schattiert die gesamte Oberfläche, und das diffuse Licht trägt dazu bei, die 3D-Form des Objekts zu verdeutlichen, wie in der folgenden Abbildung dargestellt.

![Abbildung einer Kugel mit diffuses Beleuchtung und Umgebungsbeleuchtung](images/lightad.jpg)

Die Berechnung der diffusen Beleuchtung ist intensiver als Umgebungsbeleuchtung. Da es von den Scheitelpunkt normalen und der Lichtrichtung abhängt, können Sie die Objekte Geometrie im 3D-Raum sehen, was eine realistischere Beleuchtung als Umgebungsbeleuchtung erzeugt. Sie können Glanzlichter verwenden, um ein realistischeres Aussehen zu erzielen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mathematik der Beleuchtung](mathematics-of-lighting.md)
</dt> </dl>

 

 



