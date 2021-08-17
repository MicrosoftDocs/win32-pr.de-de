---
description: Das Direct3D-Lichtmodell deckt die Umgebungs-, Diffusen-, Specular- und Glühbirnenbeleuchtung ab.
ms.assetid: cf870c89-4be0-4b95-92aa-ec7bcdc6d9dd
title: Mathematik der Beleuchtung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1c6ffa8a1142c1be40993dcd8130b4708f2b509c8a5a1f05e234d0231c3bdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728335"
---
# <a name="mathematics-of-lighting-direct3d-9"></a>Mathematik der Beleuchtung (Direct3D 9)

Das Direct3D-Lichtmodell deckt die Umgebungs-, Diffusen-, Specular- und Glühbirnenbeleuchtung ab. Dies ist ausreichend Flexibilität, um eine Vielzahl von Beleuchtungssituationen zu lösen. Sie bezeichnen die Gesamtmenge des Lichts in einer Szene als die globale Gleichung und berechnen sie mithilfe der folgenden Gleichung.


```
Global Illumination = Ambient Light + Diffuse Light + Specular Light + Emissive Light 
```



[Umgebungsbeleuchtung (Direct3D 9) ist](ambient-lighting.md) eine konstante Beleuchtung. Sie ist in alle Richtungen konstant und färbt alle Pixel eines Objekts gleich. Es ist schnell zu berechnen, aber Objekte sehen flach und unrealistisch aus. Informationen zur Berechnung der Umgebungsbeleuchtung durch Direct3D finden Sie unter Ambient Lighting (Direct3D 9).

[Diffuse Beleuchtung (Direct3D 9)](diffuse-lighting.md) hängt sowohl von der Lichtrichtung als auch von der normalen Objektoberfläche ab. Sie variiert auf der Oberfläche eines Objekts durch die sich ändernde Lichtrichtung und den sich ändernden Oberflächenzählervektor. Die Berechnung der diffusen Beleuchtung dauert länger, da sie sich für jeden Objektvertex ändert. Der Vorteil der Verwendung besteht jedoch in der Schattierung von Objekten und deren dreidimensionaler Tiefe (3D). Informationen zur Berechnung der diffusen Beleuchtung in Direct3D finden Sie unter Diffuse Beleuchtung (Direct3D 9).

[Specular Lighting (Direct3D 9)](specular-lighting.md) identifiziert die hellen Glanzlichter, die auftreten, wenn Licht auf eine Objektoberfläche trifft und zurück zur Kamera reflektiert wird. Es ist intensiver als diffuses Licht und fällt schneller über die Objektoberfläche ab. Es dauert länger, die lichtförmige Beleuchtung als die diffuse Beleuchtung zu berechnen. Der Vorteil der Verwendung ist jedoch, dass sie einer Oberfläche erhebliche Details hinzufügt. Informationen zur Berechnung der Lichtqualität in Direct3D finden Sie unter Specular Lighting (Direct3D 9).

[Die beleuchtende Beleuchtung (Direct3D 9)](emissive-lighting.md) ist ein Licht, das von einem Objekt ausgegeben wird. z. B. ein Leuchter. Informationen dazu, wie Diessive Beleuchtung in Direct3D berechnet wird, finden Sie unter Leuchtlicht (Direct3D 9).

Eine realistische Beleuchtung kann erreicht werden, indem jede dieser Beleuchtungstypen auf eine 3D-Szene anwendungiert wird. Die werte, die für Umgebungs-, Gewinde- und diffuse Komponenten berechnet werden, werden als diffuse Scheitelpunktfarbe ausgegeben. Der Wert für die Specular-Beleuchtungskomponente wird als specular vertex color ausgegeben. Umgebungs-, diffuse und speculare Lichtwerte können durch die Dämpfung und den Spotlightfaktor eines bestimmten Lichts beeinflusst werden. Weitere Informationen zur Funktionsweise der Dämpfung finden Sie unter [Attenuation and Spotlight Factor (Direct3D 9) (Dämpfung und Spotlight-Faktor (Direct3D 9)).](attenuation-and-spotlight-factor.md)

Um einen realistischeren Beleuchtungseffekt zu erzielen, fügen Sie weitere Beleuchtung hinzu. Das Rendern der Szene dauert jedoch länger. Um alle von einem Designer erzielten Effekte zu erzielen, verwenden einige Spiele mehr CPU-Leistung, als allgemein verfügbar ist. In diesem Fall ist es typisch, die Anzahl von Beleuchtungsberechnungen mithilfe von Beleuchtungskarten und Umgebungszuordnungen auf ein Minimum zu reduzieren, um eine Beleuchtung zu einer Szene hinzuzufügen, während Texturkarten verwendet werden.

Die Beleuchtung wird im Kameraraum berechnet. Informationen zur Berechnung von Beleuchtungstransformationen finden Sie unter [Kameraraumtransformationen (Direct3D 9).](camera-space-transformations.md) Optimierte Beleuchtung kann im Modellraum berechnet werden, wenn besondere Bedingungen vorliegen: normale Vektoren sind bereits normalisiert (D3DRS NORMALIZENORMALS ist True), Vertexblending ist nicht erforderlich, Transformationsmatrizen sind \_ orthogonal usw.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Licht und Materialien](lights-and-materials.md)
</dt> </dl>

 

 



