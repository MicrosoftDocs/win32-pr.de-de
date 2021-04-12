---
description: Das Direct3D Light-Modell deckt Ambient-, diffuse, Glanz-und selbst leuchtendes-Beleuchtung ab.
ms.assetid: cf870c89-4be0-4b95-92aa-ec7bcdc6d9dd
title: Mathematik der Beleuchtung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683e320788d720883702ebfa56941b1a3a5cf090
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481094"
---
# <a name="mathematics-of-lighting-direct3d-9"></a>Mathematik der Beleuchtung (Direct3D 9)

Das Direct3D Light-Modell deckt Ambient-, diffuse, Glanz-und selbst leuchtendes-Beleuchtung ab. Dies ist ausreichend Flexibilität, um eine breite Palette von Beleuchtungssituationen zu lösen. Sie verweisen auf die Gesamtmenge des Lichts in einer Szene als globale Beleuchtung und berechnen Sie mithilfe der folgenden Gleichung.


```
Global Illumination = Ambient Light + Diffuse Light + Specular Light + Emissive Light 
```



[Ambient-Beleuchtung (Direct3D 9)](ambient-lighting.md) ist eine konstante Beleuchtung. Er ist in allen Richtungen konstant und färbt alle Pixel eines Objekts gleich. Es ist schnell zu berechnen, die Objekte werden jedoch flach und unrealistisch angezeigt. Informationen zur Berechnung der Umgebungsbeleuchtung durch Direct3D finden Sie unter Ambient-Beleuchtung (Direct3D 9).

[Diffuse Beleuchtung (Direct3D 9)](diffuse-lighting.md) hängt sowohl von der Lichtrichtung als auch von der Objekt Oberfläche ab. Sie variiert auf der Oberfläche eines Objekts als Ergebnis der sich ändernden Lichtrichtung und des sich ändernden Oberflächen numerischen Vektors. Die Berechnung der diffusen Beleuchtung dauert länger, da Sie sich für jeden Objekt Scheitelpunkt ändert. der Vorteil der Verwendung besteht jedoch darin, dass Sie Objekte schattiert und dreidimensionale (3D) Tiefe liefert. Informationen zur Berechnung der diffusen Beleuchtung in Direct3D finden Sie unter diffuse Beleuchtung (Direct3D 9).

Glanz [Beleuchtung (Direct3D 9)](specular-lighting.md) identifiziert die hellen Glanzlichter, die auftreten, wenn Light auf eine Objekt Oberfläche trifft und sich wieder auf die Kamera auswirkt. Es ist intensiver als diffuses Licht und wird schneller über die Objekt Oberfläche hinweg entfernt. Die Berechnung der Glanz Beleuchtung dauert länger als bei der diffusen Beleuchtung, aber der Vorteil der Verwendung besteht darin, dass Sie einer Oberfläche deutliche Details hinzufügt. Informationen zur Berechnung der Glanz Beleuchtung in Direct3D finden Sie unter Glanz Beleuchtung (Direct3D 9).

[Emissive Beleuchtung (Direct3D 9)](emissive-lighting.md) ist ein Licht, das von einem Objekt ausgegeben wird. beispielsweise ein Glanz. Informationen zur Berechnung der selbst leuchtendes-Beleuchtung in Direct3D finden Sie unter selbst leuchtendes Beleuchtung (Direct3D 9).

Eine realistische Beleuchtung kann durch Anwenden dieser Art von Beleuchtung auf eine 3D-Szene erreicht werden. Die Werte, die für Ambient-, emissive-und diffuse-Komponenten berechnet werden, werden als diffuses Scheitelpunkt Farben ausgegeben. der Wert für die Glanzlicht Komponente wird als Glanz Farbe für Scheitel Punkte ausgegeben. Umgebungs-, diffusen und Glanz leichte Werte können von der Dämpfung und dem Spotlight-Faktor eines bestimmten Lichts beeinflusst werden. Weitere Informationen zur Funktionsweise der Dämpfung finden Sie unter [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md).

Um einen realistischeren Beleuchtungs Effekt zu erzielen, fügen Sie weitere Beleuchtung hinzu. das Rendering der Szene dauert jedoch länger. Um alle Auswirkungen eines Designers zu erzielen, verbrauchen einige Spiele mehr CPU-Leistung, als allgemein verfügbar ist. In diesem Fall ist es üblich, die Anzahl der Beleuchtungsberechnungen auf ein Mindestmaß zu reduzieren, indem Beleuchtungs Zuordnungen und Umgebungs Zuordnungen verwendet werden, um bei der Verwendung von Textur Karten Beleuchtung zu einer Szene hinzuzufügen.

Beleuchtung wird im Kamerabereich berechnet. Informationen zur Berechnung von Beleuchtungs Transformationen finden Sie unter [Kamera Raum Transformationen (Direct3D 9)](camera-space-transformations.md). Optimierte Beleuchtung kann im Modellbereich berechnet werden, wenn besondere Bedingungen vorliegen: normale Vektoren sind bereits normalisiert (D3DRS \_ normalizenormals ist true), Vertex-Blending ist nicht erforderlich, Transformations Matrizen sind orthogonal und so weiter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beleuchtung und Materialien](lights-and-materials.md)
</dt> </dl>

 

 



