---
title: Farbverwaltungseffekt
description: Verwenden Sie den Farbverwaltungseffekt, um ein Bild von einem FARBPROFIL (International Color Consortium) in ein anderes zu transformieren. Der Effekt transformiert das Bild gemäß der SPEZIFIKATION VON DER-Spezifikation.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- Farbverwaltungseffekt
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 274591312ab110a24fb315d01f72d23a22a938ad41f380620d94a865602e82a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826698"
---
# <a name="color-management-effect"></a>Farbverwaltungseffekt

Verwenden Sie den Farbverwaltungseffekt, um ein Bild von einem FARBPROFIL (International Color Consortium) in ein anderes zu transformieren. Der Effekt transformiert das Bild gemäß der [SPEZIFIKATION DER -Spezifikation.](https://www.color.org)

Die CLSID für diesen Effekt ist CLSID \_ D2D1ColorManagement.

- [Effect-Eigenschaften](#effect-properties)
- [Renderingabsichtsmodi](#rendering-intent-modes)
- [Alphamodi des Eingabebilds](#input-image-alpha-modes)
- [Konformität mit der SPEZIFIKATION FÜR DIE ANFORDERUNG](#compliance-with-icc-specification)
- [Alphakanalverhalten](#alpha-channel-behavior)
- [Qualitätsmodi](#quality-modes)
- [Beispielcode](#sample-code)
- [Requirements](#requirements)
- [Zugehörige Themen](#related-topics)

## <a name="effect-properties"></a>Effect-Eigenschaften

| Anzeigename und Indexenumeration | Beschreibung |
|-|-|
| SourceContext<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ SOURCE \_ COLOR \_ CONTEXT<br/> | Die Informationen zum Quellfarbraum. Der Typ ist [**ID2D1ColorContext.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)<br/> Der Standardwert ist NULL.<br/> |
| SourceIntent<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ SOURCE \_ RENDERING \_ INTENT<br/> | Die zu verwendende RENDERINGabsicht VON RENDERING. Der Typ ist D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT.<br/> Der Standardwert ist D2D1 \_ COLORMANAGEMENT \_ RENDERING INTENT \_ \_ PERCEPTUAL.<br/> |
| DestinationContext<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ \_ ZIELFARBKONTEXT \_<br/> | Die Informationen zum Zielfarbraum. Der Typ ist [**ID2D1ColorContext.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)<br/> Der Standardwert ist NULL.<br/> |
| DestinationIntent<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ DESTINATION \_ RENDERING \_ INTENT<br/> | Die zu verwendende RENDERINGabsicht VON RENDERING. Der Typ ist D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT.<br/> Der Standardwert ist D2D1 \_ COLORMANAGEMENT \_ RENDERING INTENT \_ \_ PERCEPTUAL.<br/> |
| AlphaMode<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ ALPHA \_ MODE<br/> | Interpretieren von Alphadaten, die im Eingabebild enthalten sind. Der Typ ist D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ MODE.<br/> Der Standardwert ist D2D1 \_ COLORMANAGEMENT \_ ALPHA MODE \_ \_ PREMULTIPLIED.<br/> |
| Qualität<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ QUALITY<br/> | Die Qualitätsstufe der Transformation. Der Typ ist D2D1 \_ COLORMANAGEMENT \_ QUALITY.<br/> Der Standardwert ist D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ NORMAL.<br/> |

## <a name="rendering-intent-modes"></a>Renderingabsichtsmodi

| Enumeration | Beschreibung |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT \_ PERCEPTUAL | Der Effekt komprimiert oder erweitert die vollständige Farbskala des Bilds, um die Farb gamut des Geräts zu füllen, sodass der Graustand beibehalten wird, die farbmetrische Genauigkeit jedoch möglicherweise nicht beibehalten wird. |
| D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT \_ RELATIVE \_ COLORIMETRIC | Der Effekt behält die Farben im Bild auf mögliche Kosten von Farbton und Lichtart bei. |
| D2D1 \_ COLORMANAGEMENT RENDERING \_ INTENT \_ \_ SÄTTIGUNG | Der Effekt passt Farben an, die außerhalb des Farbbereichs liegen, den das Ausgabegerät rendert, um die nächste verfügbare Farbe zu erhalten. Der Weißpunkt wird nicht beibehalten. |
| D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT \_ ABSOLUTE \_ COLORIMETRIC | Der Effekt passt alle Farben an, die außerhalb des Bereichs liegen, den das Ausgabegerät rendern kann, um die nächstgelegene Farbe anzupassen, die gerendert werden kann. Der Effekt ändert nicht die anderen Farben und behält den Weißen Punkt bei. |

## <a name="input-image-alpha-modes"></a>Alphamodi des Eingabebilds

| Enumeration | Beschreibung |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ MODE \_ PREMULTIPLIED | Der Effekt setzt voraus, dass der Alphamodus prämultipliiert ist. |
| D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ MODE \_ STRAIGHT | Der Effekt geht davon aus, dass der Alphamodus gerade ist. |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a>D2D1_GAMMA1_G2084 Verhaltensänderungen
    
Wenn Ihre Anwendung den [D2D1_GAMMA1_G2084-Raum](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) oder einen der [DXGI_COLOR_SPACE_TYPE-Enumerationswerte](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) verwendet, die den Farbraum SMPTE ST.2084 (Perceptual Quantizer) verwenden, beabsichtigt die Anwendung, mit HDR-Daten zu arbeiten.

Die [**APIs ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) und [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) berücksichtigen dies nicht. Stattdessen wird der HDR-Inhalt so skaliert, dass er während des G2084-DeGamma-Vorgangs in den Bereich 0-1 passt.

In der Praxis wird für Inhalte, die in diesem Gammaraum codiert sind, ein WhiteLevel-Verweis von 10.000 Bissen verwendet, der normalerweise als 10.000 /80 = 125,0 in DEN -Codierungen dargestellt wird. Um Ihre App besser zu vereinfachen, ist es also am einfachsten, bei dieser Gammakonvertierung auch die Leuchtdichte um den Faktor 125 zu skalieren. Ab Windows 10, Version 1809 (10.0; Build 17763), ist das Verhalten des Farbverwaltungseffekts so, dass diese Skalierung angewendet wird. Das bedeutet, dass Sie als Entwickler keinen zweiten Anpassungseffekt auf weißer Ebene auf [die](white-level-adjustment-effect.md) Pipeline anwenden müssen.

## <a name="compliance-with-icc-specification"></a>Konformität mit der SPEZIFIKATION FÜR DIE ANFORDERUNG

Der Farbverwaltungseffekt ist mit der SPEZIFIKATION FÜR DIE V4.3-Spezifikation kompatibel, mit den folgenden Einschränkungen:

- Der Effekt unterstützt Farbräume mit 1, 3 und 4 Kanälen.
- Der Effekt unterstützt keine ColorSpace- oder Named Color-Profile.

## <a name="alpha-channel-behavior"></a>Alphakanalverhalten

Im Allgemeinen legt der Effekt alpha auf 1 (nicht transparent) fest, wenn im Quellbild keine Alphadaten sind und die Alphadaten verworfen werden, wenn im Zielbild kein Platz ist. In der folgenden Tabelle wird das Alphaverhalten beschrieben.

<table>
<thead>
<tr class="header">
<th>Quellfarbraum, Pixelformat</th>
<th>Zielfarbraum, Pixelformat</th>
<th>Alphaverhalten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">1 Kanal, R-Pixelformat ${REMOVE}$<br />
</td>
<td>1 Kanal, R-Pixelformat</td>
<td>(Keine Alphadaten)</td>
</tr>
<tr class="even">
<td>1 Kanal, RGBA-Pixelformat</td>
<td>Alphadaten sind auf 1 (nicht transparent) festgelegt.</td>

</tr>
<tr class="odd">
<td>3 Kanal, RGBA-Pixelformat</td>
<td>Alphadaten sind auf 1 (nicht transparent) festgelegt.</td>

</tr>
<tr class="even">
<td>4 Kanal, RGBA-Pixelformat</td>
<td>(Keine Alphadaten)</td>

</tr>
<tr class="odd">
<td rowspan="4">1 Kanal, RGBA-Pixelformat ${REMOVE}$<br />
</td>
<td>1 Kanal, R-Pixelformat</td>
<td>Alphadaten werden verworfen</td>
</tr>
<tr class="even">
<td>1 Kanal, RGBA-Pixelformat</td>
<td>Alphadaten werden übergeben</td>

</tr>
<tr class="odd">
<td>3 Kanal, RGBA-Pixelformat</td>
<td>Alphadaten werden übergeben</td>

</tr>
<tr class="even">
<td>4 Kanal, RGBA-Pixelformat</td>
<td>Alphadaten werden verworfen</td>

</tr>
<tr class="odd">
<td rowspan="4">3 Kanal, RGBA-Pixelformat ${REMOVE}$<br />
</td>
<td>1 Kanal, R-Pixelformat</td>
<td>Alphadaten werden verworfen</td>
</tr>
<tr class="even">
<td>1 Kanal, RGBA-Pixelformat</td>
<td>Alphadaten werden übergeben</td>

</tr>
<tr class="odd">
<td>3 Kanal, RGBA-Pixelformat</td>
<td>Alphadaten werden übergeben</td>

</tr>
<tr class="even">
<td>4 Kanal, RGBA-Pixelformat</td>
<td>Alphadaten werden verworfen</td>

</tr>
<tr class="odd">
<td rowspan="4">4 Kanal, RGBA-Pixelformat ${REMOVE}$<br />
</td>
<td>1 Kanal, R-Pixelformat</td>
<td>(Keine Alphadaten)</td>
</tr>
<tr class="even">
<td>1 Kanal, RGBA-Pixelformat</td>
<td>Alphadaten sind auf 1 (nicht transparent) festgelegt.</td>

</tr>
<tr class="odd">
<td>3 Kanal, RGBA-Pixelformat</td>
<td>Alphadaten sind auf 1 (nicht transparent) festgelegt.</td>

</tr>
<tr class="even">
<td>4 Kanal, RGBA-Pixelformat</td>
<td>(Keine Alphadaten)</td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a>Qualitätsmodi

| Mode | BESCHREIBUNG |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ PROOF | Der Modus mit der niedrigsten Qualität. Für diesen Modus ist die Funktionsebene 9 \_ 1 oder höher erforderlich. |
| D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ NORMAL | Normaler Qualitätsmodus. Für diesen Modus ist die Funktionsebene 9 \_ 1 oder höher erforderlich. |
| D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ BEST | Der Modus mit der besten Qualität. Dieser Modus erfordert die Featureebene 10 0 oder höher sowie Puffer \_ mit Gleitkommagenauigkeit. Dieser Modus unterstützt die Gleitkommagenauigkeit sowie den erweiterten Bereich, wie in der SPEZIFIKATION FÜR DIE Version 4.3 definiert. |

Der Farbverwaltungseffekt schlägt beim Zeichnen fehl, wenn die Anwendung einen Qualitätsmodus an fordert, der von der Hardware nicht unterstützt wird. Sie können die Funktionsebene bestimmen, wenn Sie [**D3D11CreateDevice aufrufen.**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) Sie können die Gleitkommapufferunterstützung überprüfen, indem Sie [**ID2D1EffectContext::IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) mit dem Wert [**D2D1 \_ BUFFER PRECISION \_ \_ 32BPC \_ FLOAT aufrufen.**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision)

## <a name="sample-code"></a>Beispielcode

Ein Beispiel für diesen Effekt finden Sie im Beispiel zur Anpassung von [Direct2D-Effekten](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)und unter Lektion 4 des Beispiels.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Header | d2d1effects.h |
| Bibliothek | d2d1.lib, dxguid.lib |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
