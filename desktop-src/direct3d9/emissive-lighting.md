---
description: Die emissive-Beleuchtung wird durch einen einzelnen Begriff beschrieben.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Emissive-Beleuchtung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb0566d2409fb68e5fbbdca1cc609c31120e95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343119"
---
# <a name="emissive-lighting-direct3d-9"></a>Emissive-Beleuchtung (Direct3D 9)

Die emissive-Beleuchtung wird durch einen einzelnen Begriff beschrieben.

Emissive Beleuchtung = c ₑ

Hierbei gilt:



| Parameter | Standardwert | type          | BESCHREIBUNG     |
|-----------|---------------|---------------|-----------------|
| C ₑ        | (0, 0, 0, 0)     | D3DCOLORVALUE | Emissive-Farbe. |



 

Der Wert für c ₑ lautet wie folgt:

-   Vertex color1, wenn emissivematerialsource = D3DMCS \_ color1 und die erste Scheitelpunkt Farbe in der Vertex-Deklaration angegeben wird.
-   Vertex color2, wenn emissivematerialsource = D3DMCS \_ color2 und die zweite Scheitelpunkt Farbe in der Vertex-Deklaration angegeben wird.
-   Material-selbst leuchtendes-Farbe

> [!Note]  
> Wenn eine der Optionen "emissivematerialsource" verwendet wird und die Scheitelpunkt Farbe nicht angegeben wird, wird die selbst leuchtendes-Farbe des Materials verwendet.

 

## <a name="example"></a>Beispiel

In diesem Beispiel wird das-Objekt mithilfe der Szene Ambient Light und einer Material Ambient-Farbe gefärbt. Der Code wird unten dargestellt.


```
// create material
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );
mtrl.Emissive.r = 0.0f;
mtrl.Emissive.g = 0.75f;
mtrl.Emissive.b = 0.0f;
mtrl.Emissive.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_EMISSIVEMATERIALSOURCE, D3DMCS_MATERIAL);
```



Gemäß der Gleichung ist die resultierende Farbe für die Objekt Vertices die Material Farbe.

In der folgenden Abbildung wird die Material Farbe angezeigt, die grün ist. Emissive Light beleuchtet alle Objekt Scheitel Punkte mit der gleichen Farbe. Er ist nicht abhängig von der Scheitelpunkt normalen oder der Lichtrichtung. Folglich sieht die Kugel wie ein 2D-Kreis aus, da es keinen Unterschied gibt, um die Oberfläche des Objekts zu schattieren.

![Abbildung einer grünen Kugel](images/lighte.jpg)

In der folgenden Abbildung wird gezeigt, wie das selbst leuchtendes-Licht mit den anderen drei Arten von Lichtern in den vorherigen Beispielen kombiniert werden kann. Auf der rechten Seite der Kugel gibt es eine Mischung aus dem grünen selbst leuchtendes-und dem roten Ambient-Licht. Auf der linken Seite der Kugel wird das grüne Rand Licht mit rotem Ambient und diffuses Licht kombiniert, das einen roten Farbverlauf erzeugt. Die Glanz Markierung ist weiß in der Mitte und erstellt einen gelben Ring, da der Glanz helle Wert stark abfällt, wodurch sich die Umgebungs-, diffusen und abzurufenden hellen Werte, die miteinander verknüpft sind, hervorgehoben lassen.

![Abbildung einer grünen Kugel mit selbst leuchtendes Light](images/lightadse.jpg)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mathematik der Beleuchtung](mathematics-of-lighting.md)
</dt> </dl>

 

 



