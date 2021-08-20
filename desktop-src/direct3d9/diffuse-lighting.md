---
description: Nachdem die Lichtstärke auf Dämpfungseffekte angepasst wurde, berechnet das Beleuchtungsmodul, wie viel des verbleibenden Lichts von einem Scheitelpunkt reflektiert wird, angesichts des Winkels der Scheitelpunktnormale und der Richtung des Vorfalllichts.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Diffuse Beleuchtung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9906742b47b959336fd882748388a2f10776b6adb06eb98bc23effb6576793be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675764"
---
# <a name="diffuse-lighting-direct3d-9"></a>Diffuse Beleuchtung (Direct3D 9)

Nachdem die Lichtstärke auf Dämpfungseffekte angepasst wurde, berechnet das Beleuchtungsmodul, wie viel des verbleibenden Lichts von einem Scheitelpunkt reflektiert wird, angesichts des Winkels der Scheitelpunktnormale und der Richtung des Vorfalllichts. Das Beleuchtungsmodul springt zu diesem Schritt für Richtungslichter, da sie nicht über die Entfernung dämpfen. Das System berücksichtigt zwei Reflektionstypen, diffus und specular, und verwendet eine andere Formel, um zu bestimmen, wie viel Licht für jeden reflektiert wird. Nach der Berechnung der reflektierten Lichtmengen wendet Direct3D diese neuen Werte auf die diffusen und glanzförmigen Reflektoreigenschaften des aktuellen Materials an. Die resultierenden Farbwerte sind die diffusen und specular-Komponenten, die der Rasterizer verwendet, um gouraud shading und specular highlighting zu erzeugen.

Die diffuse Beleuchtung wird durch die folgende Gleichung beschrieben.

Diffuse Beleuchtung = Summe \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>.</sup> L<sub>dir</sub>) \* Atten \* Spot\]



| Parameter       | Standardwert | Typ          | Beschreibung                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| Sum             | Nicht zutreffend           | Nicht zutreffend           | Summierung der diffusen Komponente jedes Lichts.                                                                  |
| C<sub>d</sub>   | (0,0,0,0)     | D3DCOLORVALUE | Diffuse Farbe.                                                                                                |
| L<sub>d</sub>   | (0,0,0,0)     | D3DCOLORVALUE | Helle diffuse Farbe.                                                                                          |
| N               | Nicht zutreffend           | D3DVECTOR     | Scheitelpunkt normal                                                                                                 |
| L<sub>dir</sub> | Nicht zutreffend           | D3DVECTOR     | Richtungsvektor vom Objektvertex zum Licht.                                                             |
| Atten           | Nicht zutreffend           | GLEITKOMMAZAHL         | Lichtdämpfung. Weitere Informationen [finden Sie unter Attenuation and Spotlight Factor (Direct3D 9) (Dämpfung und Spotlight-Faktor (Direct3D 9)).](attenuation-and-spotlight-factor.md) |
| Sofortige Zahlung            | Nicht zutreffend           | GLEITKOMMAZAHL         | Spotlight-Faktor. Weitere Informationen [finden Sie unter Attenuation and Spotlight Factor (Direct3D 9) (Dämpfung und Spotlight-Faktor (Direct3D 9)).](attenuation-and-spotlight-factor.md)  |



 

Der Wert für C<sub>d</sub> ist entweder:

-   Scheitelpunktfarbe1, wenn DIFFUSEMATERIALSOURCE = D3DMCS COLOR1, und die erste Scheitelpunktfarbe \_ in der Scheitelpunktdeklaration angegeben wird.
-   vertex color2, wenn DIFFUSEMATERIALSOURCE = D3DMCS COLOR2, und die zweite Scheitelpunktfarbe \_ in der Scheitelpunktdeklaration angegeben wird.
-   Material – diffuse Farbe

> [!Note]  
> Wenn eine der BEIDEN DIFFUSEMATERIALSOURCE-Optionen verwendet wird und die Scheitelpunktfarbe nicht angegeben wird, wird die diffuse Materialfarbe verwendet.

 

Informationen zum Berechnen der Dämpfung (Atten) oder der Spotlight-Merkmale (Spot) finden Sie unter [Attenuation and Spotlight Factor (Direct3D 9) (Dämpfung und Spotlight-Faktor (Direct3D 9)).](attenuation-and-spotlight-factor.md)

Diffuse Komponenten werden mit 0 bis 255 klammert, nachdem alle Lichtlichter separat verarbeitet und interpoliert wurden. Der resultierende diffuse Beleuchtungswert ist eine Kombination der Umgebungs-, Diffusen- und Glühbirnenlichtwerte.

## <a name="example"></a>Beispiel

In diesem Beispiel wird das -Objekt mit der hell diffusen Farbe und einer material diffusen Farbe farbig dargestellt. Der Code ist unten dargestellt.


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



Gemäß der Gleichung ist die resultierende Farbe für die Objektvertices eine Kombination aus der Materialfarbe und der hellfarbenen Farbe.

Die folgenden beiden Abbildungen zeigen die Materialfarbe , die grau ist, und die helle Farbe, die hell rot ist.

![Abbildung einer grauen Kugel](images/amb1.jpg)![Abbildung einer roten Kugel](images/lightred.jpg)

Die resultierende Szene wird in der folgenden Abbildung dargestellt. Das einzige Objekt in der Szene ist eine Kugel. Bei der Berechnung der diffusen Beleuchtung werden das Material und die hell diffuse Farbe verwendet und mithilfe des Punktprodukts um den Winkel zwischen der Lichtrichtung und der Scheitelpunktnormale verändert. Infolgedessen wird die Rückseite der Kugel dunkler, da die Oberfläche der Kugel vom Licht abtrünnt.

![Abbildung einer Kugel mit diffuser Beleuchtung](images/lightd.jpg)

Wenn Sie die diffuse Beleuchtung mit der Umgebungsbeleuchtung aus dem vorherigen Beispiel kombinieren, wird die gesamte Oberfläche des Objekts schattiert. Das Umgebungslicht schattiert die gesamte Oberfläche, und das diffuse Licht hilft dabei, die 3D-Form des Objekts zu zeigen, wie in der folgenden Abbildung dargestellt.

![Abbildung einer Kugel mit diffuser Beleuchtung und Umgebungslicht](images/lightad.jpg)

Die Berechnung der diffusen Beleuchtung ist schwieriger als die Umgebungsbeleuchtung. Da dies von den Scheitelpunktnormale und der Lichtrichtung abhängt, können Sie die Objektgeometrie im 3D-Raum sehen, wodurch eine realistischere Beleuchtung als eine Umgebungsbeleuchtung erzeugt wird. Sie können Glanzlichter verwenden, um ein realistischeres Aussehen zu erzielen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mathematik der Beleuchtung](mathematics-of-lighting.md)
</dt> </dl>

 

 



