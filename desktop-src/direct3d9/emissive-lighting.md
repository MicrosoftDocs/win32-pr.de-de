---
description: Die freizügige Beleuchtung wird durch einen einzigen Begriff beschrieben.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Emissive Lighting (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3200486118e6b44efc3be31f01b3a10e62c876d673c687619a4e6c8445f0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802930"
---
# <a name="emissive-lighting-direct3d-9"></a>Emissive Lighting (Direct3D 9)

Die freizügige Beleuchtung wird durch einen einzigen Begriff beschrieben.

Emissive Lighting = Cₑ

Hierbei gilt:



| Parameter | Standardwert | type          | BESCHREIBUNG     |
|-----------|---------------|---------------|-----------------|
| Cₑ        | (0,0,0,0)     | D3DCOLORVALUE | Freizügige Farbe. |



 

Der Wert für Cₑ ist:

-   vertex color1, wenn EMISSIVEMATERIALSOURCE = D3DMCS \_ COLOR1, und die erste Scheitelpunktfarbe in der Scheitelpunktdeklaration angegeben wird.
-   vertex color2, wenn EMISSIVEMATERIALSOURCE = D3DMCS \_ COLOR2, und die zweite Scheitelpunktfarbe in der Scheitelpunktdeklaration angegeben wird.
-   material emissive color

> [!Note]  
> Wenn eine der Beiden EMISSIVEMATERIALSOURCE-Optionen verwendet wird und die Scheitelpunktfarbe nicht angegeben wird, wird die materialemissive Farbe verwendet.

 

## <a name="example"></a>Beispiel

In diesem Beispiel wird das -Objekt mithilfe des Umgebungslichts der Szene und einer materialen Umgebungsfarbe farbig dargestellt. Der Code ist unten dargestellt.


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



Gemäß der Gleichung ist die resultierende Farbe für die Objektvertices die Materialfarbe.

Die folgende Abbildung zeigt die Materialfarbe grün. Das freizügige Licht leuchtet alle Objektvertices mit der gleichen Farbe. Sie ist nicht von der Scheitelpunktnormale oder der Lichtrichtung abhängig. Daher sieht die Kugel wie ein 2D-Kreis aus, da es keinen Unterschied in der Schattierung um die Oberfläche des Objekts gibt.

![Abbildung einer grünen Kugel](images/lighte.jpg)

Die folgende Abbildung zeigt, wie sich das freizügige Licht mit den anderen drei Lichttypen aus den vorherigen Beispielen verbindet. Auf der rechten Seite der Kugel befindet sich eine Mischung aus grünem und rotem Umgebungslicht. Auf der linken Seite der Kugel wird das grüne, freizügige Licht mit rotem Umgebungslicht und diffusem Licht kombiniert, wodurch ein roter Farbverlauf entsteht. Das Glanzlicht ist in der Mitte weiß und erstellt einen gelben Ring, wenn der Glanzlichtwert abfällt und die Umgebungs-, diffusen und freizügigen Lichtwerte, die sich zu Gelb vermischen, stark verlässt.

![Abbildung einer grünen Kugel mit freizügigem Licht](images/lightadse.jpg)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mathematik der Beleuchtung](mathematics-of-lighting.md)
</dt> </dl>

 

 



