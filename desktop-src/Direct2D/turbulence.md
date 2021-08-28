---
title: Auswirkung "Effekt"
description: Verwenden Sie den Effekt "Rauschen", um eine Bitmap basierend auf der Perlin-Rauschfunktion zu generieren.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- Wirkung von "effect"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f2aa58be48c759956fe3522812d7ad6c3e9989
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468597"
---
# <a name="turbulence-effect"></a>Auswirkung "Effekt"

Verwenden Sie den Effekt "Rauschen", um eine Bitmap basierend auf der Perlin-Rauschfunktion zu generieren.

Der Effekt hat kein Eingabebild.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Turbulence.

-   [Beispielbild](#example-image)
-   [Effekteigenschaften](#effect-properties)
-   [Rauschmodi](#noise-modes)
-   [Ausgabebitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

![Screenshot des Effektbeispiels, der die Ausgabe des Effekts "Wirkung" zeigt.](images/32-turbulence.png)

Der Effekt "Rauschen" berechnet die Summe eines oder mehrerer Oktaven der Perlin-Rauschfunktion. Perlinrauschen ist eine pseudozufällige Funktion, deren Wert von häufigkeit, Position und Ausgangswert abhängt. Der Effekt generiert die RGBA-Werte mithilfe einer dieser Gleichungen.

Wenn Sie den D2D1 \_ NOISE \_ NOISE \_ FRACTAL \_ SUM-Rauschmodus auswählen, verwendet der Effekt diese Gleichung.

![Screenshot, der die Funktion "1" zeigt, die zum Generieren einer Bitmap verwendet wird.](images/turbulence-equation1.png)

Wenn Sie den D2D1 \_ NOISE \_ NOISE \_ NOISE-Rauschmodus auswählen, verwendet der Effekt diese Gleichung.

![die zum Generieren einer Bitmap verwendete Funktionsfunktion.](images/turbulence-equation2.png)

> [!Note]  
> Die `PerlinNoise` Funktion hat einen Bereich von \[ -1, 1 \] .

 

Dieser Effekt gibt Pixelwerte in prämultiplizieren alpha aus.

## <a name="effect-properties"></a>Effekteigenschaften




| Anzeigename und Indexenumeration | BESCHREIBUNG | 
|------------------------------------|-------------|
| Offset<br /> D2D1_TURBULENCE_PROP_OFFSET<br /> | Die Koordinaten, an denen die Ausgabe der Ausgabe generiert wird.<br /> Der Algorithmus, der zum Generieren des Perlin-Rauschens verwendet wird, ist positionsabhängig, sodass ein anderer Offset zu einer anderen Ausgabe führt. Diese Eigenschaft ist nicht begrenzt, und die Einheiten werden in DIPs angegeben. <br /><blockquote>[!Note]<br />Der Offset hat nicht die gleiche Auswirkung wie eine Übersetzung, da die Ausgabe der Rauschfunktion unendlich ist und die Funktion die Kachel umschließt.</blockquote><br /> Der Typ ist D2D1_VECTOR_2F.<br /> Der Standardwert ist {0.0f, 0.0f}.<br /> | 
| Size<br /> D2D1_TURBULENCE_PROP_SIZE<br /> | Die Größe der Ausgabe der Ausgabe.<br /> Diese Eigenschaft ist nicht begrenzt, und die Einheiten werden in DIPs angegeben. <br /><br /> Der Typ ist D2D1_VECTOR_2F.<br /> Der Standardwert ist {0.0f, 0.0f}.<br /> | 
| BaseFrequency<br /> D2D1_TURBULENCE_PROP_BASE_FREQUENCY<br /> | Die Basisfrequenzen in X- und Y-Richtung. Diese Eigenschaft ist float und muss größer als 0 sein. Die Einheiten werden in 1/DIPs angegeben. <br /> Der Wert 1 (1/DIPs) für die Basisfrequenz führt dazu, dass das Perlin-Rauschen einen gesamten Zyklus zwischen zwei Pixeln abschließt. Die einfache Interpolation für diese Pixel führt zu vollständig zufälligen Pixeln, da es keine Korrelation zwischen den Pixeln gibt.<br /> Der Wert 0,1 (1/DIPs) für die Basisfrequenz, die Perlin-Rauschfunktion wiederholt alle 10 DIPs. Dies führt zu einer Korrelation zwischen Pixeln, und der typische Effekt ist sichtbar.<br /> Der Typ ist D2D1_VECTOR_2F.<br /> Der Standardwert ist {0.01f, 0.01f}.<br /> | 
| NumOctaves<br /> D2D1_TURBULENCE_PROP_NUM_OCTAVES<br /> | Die Anzahl der Oktaven für die Rauschfunktion. Diese Eigenschaft ist ein UINT32 und muss größer als 0 sein.<br /> Der Typ ist UINT32.<br /> Der Standardwert ist 1.<br /> | 
| Seed<br /> D2D1_TURBULENCE_PROP_SEED<br /> | Der Ausgangswert für den Pseudo-Zufallsgenerator. Diese Eigenschaft ist nicht gebunden.<br /> Der Typ ist UINT32.<br /> Der Standardwert ist 0.<br /> | 
| Stördatenverkehr<br /> D2D1_TURBULENCE_PROP_NOISE<br /> | Der Rauschmodus "Rauschen". Bei dieser Eigenschaft kann es sich um <em>eine fraktale Summe</em> oder um <em>eine unausgeknüpfte</em>Eigenschaft () handelt. Gibt an, ob eine Bitmap basierend auf fraktalen Rauschen oder der Funktion "Rauschen" generiert werden soll. Weitere Informationen finden Sie unter <a href="#noise-modes">Rauschmodi.</a> <br /> Der Typ ist D2D1_TURBULENCE_NOISE.<br /> Der Standardwert ist D2D1_TURBULENCE_NOISE_FRACTAL_SUM.<br /> | 
| Zusammenfügen<br /> D2D1_TURBULENCE_PROP_STITCHABLE<br /> | Aktiviert oder deaktiviert das Zusammenfügen. Die Basisfrequenz wird so angepasst, dass die Ausgabebitmap zusammengefügt werden kann. Dies ist nützlich, wenn Sie mehrere Kopien der Ausgabe der Effektauswirkung kacheln möchten.<ul><li>True Die Ausgabebitmap kann (mithilfe des Kacheleffekts) ohne die Darstellung von Nahten gekachelt werden. Die Basisfrequenz wird so angepasst, dass die Ausgabebitmap zusammengefügt werden kann.</li><li>False Die Basishäufigkeit wird nicht angepasst, sodass Nahten zwischen Kacheln angezeigt werden können, wenn die Bitmap gekachelt wird.</li></ul><br /> Der Typ ist BOOL.<br /> Der Standardwert ist FALSE.<br /> | 




 

## <a name="noise-modes"></a>Rauschmodi



| Enumeration                           | Beschreibung                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| D2D1 \_ TURBULENCE \_ NOISE \_ FRACTAL \_ SUM | Berechnet eine Summe der Oktaven und verschiebt den Ausgabebereich von \[ -1, 1 \] auf \[ 0, \] 1. |
| \_D2D1-RAUSCHRAUSCHEN IN DER \_ \_ RAUSCHUNTERDRÜCKUNG   | Berechnet eine Summe des absoluten Werts jeder Oktave.                                  |



 

> [!Note]  
> Keiner der Modi enthält eine explizite Klammer der Ausgabewerte.

 

## <a name="output-bitmap"></a>Ausgabebitmap

Dieser Effekt generiert eine logisch unendlich große Bitmap.

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

 

