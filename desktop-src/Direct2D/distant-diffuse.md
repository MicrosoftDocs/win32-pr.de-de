---
title: Beleuchtungseffekt „Entfernt-Diffus“
description: Verwenden Sie den fernen diffusen Beleuchtungseffekt, um ein Bild zu erstellen, das eine nicht reflektierende Oberfläche zu sein scheint, bei der die Lichtquelle aus einer langen Entfernung (z. B. die Sonnen- oder Overheadlichter) zu stammen scheint und das Licht in alle Richtungen verteilt ist.
ms.assetid: 981FD58B-0565-4D0E-957C-3ED81BA8A6EB
keywords:
- ferner diffuser Beleuchtungseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f1860f196685c3d7dc0dcc30ae575cee70bc1eb0fcc29e8da7709c1174ee411
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260404"
---
# <a name="distant-diffuse-lighting-effect"></a>Beleuchtungseffekt „Entfernt-Diffus“

Verwenden Sie den fernen diffusen Beleuchtungseffekt, um ein Bild zu erstellen, das eine nicht reflektierende Oberfläche zu sein scheint, bei der die Lichtquelle aus einer langen Entfernung (z. B. die Sonnen- oder Overheadlichter) zu stammen scheint und das Licht in alle Richtungen verteilt ist. Dieser Effekt verwendet den Alphakanal als Höhenkarte und strahlt das Bild mit einer entfernten Lichtquelle aus.

Die Farbe der Ausgabebitmap ist das Ergebnis von Lichtfarbe, Lichtposition und Oberflächengeometrie des Bilds. Die Alphakanalausgabe für jedes Pixel mit diffuser Beleuchtung ist immer 1,0.

Die CLSID für diesen Effekt ist CLSID \_ D2D1DistantDiffuse.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Skalierungsmodi](#scale-modes)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das folgende Beispiel zeigt die Ein- und Ausgabebilder des entfernt-diffusen Beleuchtungseffekts.

![Effect-Beispielscreenshot der Ein- und Ausgabebilder des entfernten diffusen Beleuchtungseffekts.](images/distant-diffuse-example.png)

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azimut<br/> D2D1 \_ DISTANTDIFFUSE \_ PROP \_ AZIAKUS<br/>                       | Der Richtungswinkel der Lichtquelle in der XY-Ebene relativ zur X-Achse in der Indikatoruhrrichtung. Die Einheiten sind in Grad und müssen zwischen 0 und 360 Grad liegen.<br/> Der Typ ist FLOAT.<br/> Der Standardwert ist 0,0f.<br/>                                                                                                                                                                                                                                                            |
| Elevation<br/> D2D1 \_ ENTFERNTEDIFFUSE \_ PROP \_ ELEVATION<br/>                   | Der Richtungswinkel der Lichtquelle in der YZ-Ebene relativ zur Y-Achse in der taktweisen Richtung des Indikators. Die Einheiten sind in Grad und müssen zwischen 0 und 360 Grad liegen. <br/> Der Typ ist FLOAT.<br/> Der Standardwert ist 0,0f.<br/>                                                                                                                                                                                                                                                           |
| DiffuseConstant<br/> D2D1 \_ DISTANTDIFFUSE \_ PROP \_ \_ DIFFUSE-KONSTANTE<br/>     | Das Verhältnis der diffusen Reflektion zu der Menge des eingehenden Lichts. Diese Eigenschaft muss zwischen 0 und 10.000 liegen und ist einheitenlos. <br/> Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                                                                                                                                                      |
| SurfaceScale<br/> D2D1 \_ \_ ENTFERNTEIFFUSE-PROP-OBERFLÄCHENSKALA \_ \_<br/>           | Der Skalierungsfaktor in Z-Richtung. Die Oberflächenskala ist einheitenlos und muss zwischen 0 und 10.000 sein.<br/> Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                                                                                                                                                                           |
| Color<br/> D2D1 \_ FARDIFFUSE \_ PROP \_ COLOR<br/>                           | Die Farbe des eingehenden Lichts. Diese Eigenschaft wird als D2D1 \_ VECTOR \_ 3F (R, G, B) verfügbar gemacht und zum Berechnen von L<sub>R,</sub>L<sub>G,</sub>L<sub>B</sub>verwendet. <br/> Der Typ ist D2D1 \_ VECTOR \_ 3F.<br/> Der Standardwert ist {1.0f, 1.0f, 1.0f}.<br/>                                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> D2D1 \_ DISTANTDIFFUSE \_ PROP \_ KERNEL \_ UNIT \_ LENGTH<br/> | Die Größe eines Elements im Sobel-Kernel, das verwendet wird, um die Oberflächennormale in X- und Y-Richtung zu generieren. Diese Eigenschaft wird den Dx- und Dy-Werten im Sobel-Farbverlauf zugeordnet. Diese Eigenschaft ist ein D2D1 \_ VECTOR \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) und wird in (geräteunabhängige Pixel (DIPs)/Kernel Unit) definiert. Der Effekt verwendet die bilineare Interpolation, um die Bitmap entsprechend der Größe von Kernelelementen zu skalieren. <br/> Der Typ ist D2D1 \_ VECTOR \_ 2F.<br/> Der Standardwert ist {1.0f, 1.0f}.<br/> |
| Scalemode<br/> D2D1 \_ - ENTFERNTEIFFUSE-PROP-SKALIERUNGSMODUS \_ \_ \_<br/>                 | Der Interpolationsmodus, den der Effekt verwendet, um das Bild auf die entsprechende Kerneleinheitlänge zu skalieren. Es gibt sechs Skalierungsmodi, die in Qualität und Geschwindigkeit reichen.<br/> Der Typ ist D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE.<br/> Der Standardwert ist D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                                                                                                                 |



 

## <a name="scale-modes"></a>Skalierungsmodi



| Enumeration                                              | Beschreibung                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ \_ ENTFERNTERDIFFUSE-SKALIERUNGSMODUS NÄCHSTER \_ \_ \_ NACHBAR     | Probieren Sie den nächstgelegenen einzelnen Punkt aus, und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das Bild mit der niedrigsten Qualität aus.                                                                           |
| D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE \_ LINEAR                | Verwendet eine Vier-Punkt-Stichprobe und lineare Interpolation. Dieser Modus gibt ein Bild mit höherer Qualität als der nächste Nachbar aus.                                                                                   |
| D2D1 \_ DISTANTDIFFUSE \_ SCALE MODE \_ \_ KUBISCH                 | Verwendet einen kubischen Kernel mit 16 Beispielen für die Interpolation. Dieser Modus verwendet die meiste Verarbeitungszeit, gibt jedoch ein Bild höherer Qualität aus.                                                                        |
| D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für ein gutes Edge-Antialiasing. Dieser Modus eignet sich gut für das Herunterskalierung um kleine Mengen auf Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ \_ ENTFERNTEDIFFUSE-SKALIERUNGSMODUS \_ \_ ANISOTROPE           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap abzubilden.                                                                                                     |
| D2D1 \_ - ENTFERNTEIFFUSE-SKALIERUNGSMODUS \_ MIT HOHER \_ \_ \_ \_ KUBISCHER QUALITÄT  | Verwendet einen kubischen Kernel variabler Größe, um das Bild vorab herunterzuskalieren, wenn die Transformationsmatrix eine Downskalierung umfasst. Verwendet dann den kubischen Interpolationsmodus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird standardmäßig D2D1 \_ DISTANTDIFFUSE \_ SCALE MODE LINEAR \_ \_ verwendet.

 
## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects.h                                                                      |
| Bibliothek                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

