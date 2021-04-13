---
title: Farb Verwaltungs Effekt
description: Verwenden Sie den Farb Verwaltungs Effekt, um ein Bild von einem "ICC"-Farbprofil (International Color Consortium) in ein anderes zu transformieren. Der Effekt wandelt das Bild entsprechend der ICC-Spezifikation um.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- Farb Verwaltungs Effekt
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 5f3783132e0e2af511a99fd8c44d5f899e577a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391832"
---
# <a name="color-management-effect"></a>Farb Verwaltungs Effekt

Verwenden Sie den Farb Verwaltungs Effekt, um ein Bild von einem "ICC"-Farbprofil (International Color Consortium) in ein anderes zu transformieren. Der Effekt wandelt das Bild entsprechend der [ICC-Spezifikation](https://www.color.org)um.

Die CLSID für diesen Effekt ist CLSID \_ D2D1ColorManagement.

- [Effekt Eigenschaften](#effect-properties)
- [Renderintent-Modi](#rendering-intent-modes)
- [Eingabebild-Alpha-Modi](#input-image-alpha-modes)
- [Konformität mit der ICC-Spezifikation](#compliance-with-icc-specification)
- [Alpha Kanal Verhalten](#alpha-channel-behavior)
- [Qualitäts Modi](#quality-modes)
- [Beispielcode](#sample-code)
- [Anforderungen](#requirements)
- [Zugehörige Themen](#related-topics)

## <a name="effect-properties"></a>Effekt Eigenschaften

| Anzeige Name und indexenumeration | BESCHREIBUNG |
|-|-|
| SourceContext<br/> D2D1 \_ Colormanagement- \_ Prop- \_ Quell \_ Farb \_ Kontext<br/> | Die Quell Farbraum-Informationen. Der Typ ist " [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)".<br/> Der Standardwert ist NULL.<br/> |
| Sourceinztent<br/> D2D1 \_ Colormanagement- \_ Prop- \_ Quell \_ \_ renderabsicht<br/> | Die zu verwendende ICC-renderingabsicht. Der Typ ist "D2D1 \_ Colormanagement \_ RENDERING \_ INTENT".<br/> Der Standardwert ist D2D1 \_ Colormanagement \_ RENDERING \_ INTENT INTENT \_ .<br/> |
| Destinationcontext<br/> D2D1 \_ Colormanagement- \_ Prop- \_ Ziel \_ Farb \_ Kontext<br/> | Die Informationen zum Ziel Farbraum. Der Typ ist " [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)".<br/> Der Standardwert ist NULL.<br/> |
| Destinationintent<br/> D2D1 \_ Colormanagement- \_ Prop- \_ Ziel \_ \_ renderabsicht<br/> | Die zu verwendende ICC-renderingabsicht. Der Typ ist "D2D1 \_ Colormanagement \_ RENDERING \_ INTENT".<br/> Der Standardwert ist D2D1 \_ Colormanagement \_ RENDERING \_ INTENT INTENT \_ .<br/> |
| Alpha AMODE<br/> D2D1 \_ Colormanagement- \_ Prop- \_ alpha- \_ Modus<br/> | Interpretieren von Alpha-Daten, die im Eingabebild enthalten sind. Der Typ ist der D2D1 \_ Colormanagement \_ alpha- \_ Modus.<br/> Der Standardwert ist "D2D1 \_ Colormanagement \_ Alpha Mode" ( \_ \_ vorab multipliziert).<br/> |
| Qualität<br/> D2D1 \_ Colormanagement- \_ Prop- \_ Qualität<br/> | Die Qualitätsstufe der Transformation. Der Typ ist "D2D1 \_ Colormanagement \_ Quality".<br/> Der Standardwert ist D2D1 \_ Colormanagement \_ Quality \_ Normal.<br/> |

## <a name="rendering-intent-modes"></a>Renderintent-Modi

| Enumeration | Beschreibung |
|-|-|
| D2D1 \_ Colormanagement- \_ RENDERING \_ INTENT INTENT \_ | Der Effekt komprimiert oder erweitert den vollständigen Farb Umfang des Bilds, um den Farb Umfang des Geräts zu füllen, sodass das graue Gleichgewicht beibehalten wird, die farbige metrikgenauigkeit jedoch möglicherweise nicht beibehalten wird. |
| D2D1 \_ Colormanagement \_ - \_ renderabsicht \_ relative \_ farbige Metrik | Der Effekt bewahrt den Chroma der Farben im Bild auf mögliche Kosten von Hue und Helligkeit. |
| D2D1 \_ Colormanagement- \_ renderingabsicht \_ \_ | Der Effekt passt Farben an, die außerhalb des Bereichs von Farben liegen, die das Ausgabegerät rendert, bis zur nächstgelegenen verfügbaren Farbe. Der weiße Punkt wird nicht beibehalten. |
| D2D1 \_ Colormanagement \_ - \_ renderabsicht \_ absolute \_ farbige Metrik | Der Effekt passt alle Farben an, die außerhalb des Bereichs liegen, den das Ausgabegerät rendern kann, bis zur nächstgelegenen Farbe, die gerendert werden kann. Der Effekt ändert nicht die anderen Farben und behält den weißen Punkt bei. |

## <a name="input-image-alpha-modes"></a>Eingabebild-Alpha-Modi

| Enumeration | Beschreibung |
|-|-|
| D2D1 \_ Colormanagement- \_ alpha \_ Modus ist \_ vorab multipliziert | Der Effekt geht davon aus, dass der Alpha-Modus vorab multipliziert ist. |
| D2D1 \_ Colormanagement \_ alpha \_ Modus \_ direkt | Der Effekt geht davon aus, dass der Alpha-Modus gerade ist. |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a>D2D1_GAMMA1_G2084 Verhaltensänderungen
    
Wenn Ihre Anwendung den [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) Raum oder einen der [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) Enumerationswerte verwendet, die den SMPTE St. 2084-Farbraum (perzeptive Quantizer) verwenden, beabsichtigt die Anwendung, mit HDR-Daten zu arbeiten.

Die [**ID2D1DeviceContext5:::: | atecolorcontextfromsimplecolorprofile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) -und [**ID2D1DeviceContext5:: roatecolorcontextfromdxgicolorspace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) -APIs berücksichtigen das nicht. Stattdessen wird der HDR-Inhalt so skaliert, dass er während des G2084 Degamma-Vorgangs in den Bereich 0-1 passt.

In der Praxis verwendet der in diesem Gamma Bereich codierte Inhalt eine Verweis whitelevel von 10.000 Nits, die normalerweise in CCCS als 10.000/80 = 125,0 dargestellt werden. Um Ihre APP besser zu vereinfachen, ist es am einfachsten, dass diese Gamma Konvertierung auch die Helligkeit um den Faktor 125 skaliert. Ab Windows 10, Version 1809 (10,0; Build 17763), das Verhalten des Farb Verwaltungs Effekts bewirkt, dass diese Skalierung angewendet wird. Dies bedeutet, dass Sie als Entwickler keinen zweiten [Anpassungs Effekt in der weißen Ebene](white-level-adjustment-effect.md) auf die Pipeline anwenden müssen.

## <a name="compliance-with-icc-specification"></a>Konformität mit der ICC-Spezifikation

Der Effekt der Farbverwaltung ist mit den folgenden Einschränkungen mit der Spezifikation von "ICC v 4.3" kompatibel:

- Der Effekt unterstützt 1, 3 und 4 Kanal Farbräume.
- Der Effekt unterstützt keine colorspace-oder Named Color-Profile.

## <a name="alpha-channel-behavior"></a>Alpha Kanal Verhalten

Im Allgemeinen legt der Effekt Alpha auf 1 (nicht transparent) fest, wenn keine Alpha Daten im Quell Abbild vorhanden sind und die Alpha Daten verworfen werden, wenn das Ziel Image keinen Platz hat. In der folgenden Tabelle wird das Alpha Verhalten beschrieben.

<table>
<thead>
<tr class="header">
<th>Color Space-Quelle, Pixel Format</th>
<th>Color Space-Ziel, Pixel Format</th>
<th>Alpha-Verhalten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">1 Channel, R-Pixel-Format $ {Remove} $<br />
</td>
<td>1 Channel, R-Pixel-Format</td>
<td>(Keine Alpha Daten)</td>
</tr>
<tr class="even">
<td>1 Kanal, RGBA-Pixel Format</td>
<td>Alpha Daten sind auf 1 (nicht transparent) festgelegt.</td>

</tr>
<tr class="odd">
<td>3 Channel, RGBA-Pixel Format</td>
<td>Alpha Daten sind auf 1 (nicht transparent) festgelegt.</td>

</tr>
<tr class="even">
<td>4 Channel, RGBA-Pixel Format</td>
<td>(Keine Alpha Daten)</td>

</tr>
<tr class="odd">
<td rowspan="4">1 Channel, RGBA-Pixel Format $ {Remove} $<br />
</td>
<td>1 Channel, R-Pixel-Format</td>
<td>Alpha Daten werden verworfen.</td>
</tr>
<tr class="even">
<td>1 Kanal, RGBA-Pixel Format</td>
<td>Alpha Daten werden durchlaufen</td>

</tr>
<tr class="odd">
<td>3 Channel, RGBA-Pixel Format</td>
<td>Alpha Daten werden durchlaufen</td>

</tr>
<tr class="even">
<td>4 Channel, RGBA-Pixel Format</td>
<td>Alpha Daten werden verworfen.</td>

</tr>
<tr class="odd">
<td rowspan="4">3 Channel, RGBA-Pixel Format $ {Remove} $<br />
</td>
<td>1 Channel, R-Pixel-Format</td>
<td>Alpha Daten werden verworfen.</td>
</tr>
<tr class="even">
<td>1 Kanal, RGBA-Pixel Format</td>
<td>Alpha Daten werden durchlaufen</td>

</tr>
<tr class="odd">
<td>3 Channel, RGBA-Pixel Format</td>
<td>Alpha Daten werden durchlaufen</td>

</tr>
<tr class="even">
<td>4 Channel, RGBA-Pixel Format</td>
<td>Alpha Daten werden verworfen.</td>

</tr>
<tr class="odd">
<td rowspan="4">4 Channel, RGBA-Pixel Format $ {Remove} $<br />
</td>
<td>1 Channel, R-Pixel-Format</td>
<td>(Keine Alpha Daten)</td>
</tr>
<tr class="even">
<td>1 Kanal, RGBA-Pixel Format</td>
<td>Alpha Daten sind auf 1 (nicht transparent) festgelegt.</td>

</tr>
<tr class="odd">
<td>3 Channel, RGBA-Pixel Format</td>
<td>Alpha Daten sind auf 1 (nicht transparent) festgelegt.</td>

</tr>
<tr class="even">
<td>4 Channel, RGBA-Pixel Format</td>
<td>(Keine Alpha Daten)</td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a>Qualitäts Modi

| Mode | BESCHREIBUNG |
|-|-|
| D2D1 \_ Colormanagement- \_ Qualitäts \_ Nachweis | Der Modus mit der niedrigsten Qualität. Für diesen Modus ist die Featureebene 9 \_ 1 oder höher erforderlich. |
| D2D1 \_ Colormanagement- \_ Qualität \_ Normal | Normaler Qualitäts Modus. Für diesen Modus ist die Featureebene 9 \_ 1 oder höher erforderlich. |
| D2D1 \_ Colormanagement- \_ Qualität \_ am besten | Der Modus für die beste Qualität. Für diesen Modus sind die Featureebene 10 \_ 0 oder höher sowie die Puffer für Gleit Komma Genauigkeit erforderlich. Dieser Modus unterstützt die Genauigkeit von Gleit Komma Werten und den erweiterten Bereich, wie in der Spezifikation von "ICC v 4.3" definiert. |

Der Farb Verwaltungs Effekt schlägt fehl, wenn die Anwendung einen Qualitäts Modus anfordert, der von der Hardware nicht unterstützt wird. Sie können die Featureebene ermitteln, wenn Sie [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice)aufgerufen haben. Sie können die Unterstützung für Gleit Komma Puffer überprüfen, indem Sie [**ID2D1EffectContext:: isbufferprecisionsupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) mit dem Wert [**D2D1 \_ buffer \_ Precision \_ 32bpc \_ float**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision)aufrufen.

## <a name="sample-code"></a>Beispielcode

Ein Beispiel für diesen Effekt finden Sie unter Beispiel für die [Photo-Anpassung Direct2D Effects](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)und in Lektion 4 des Beispiels.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Header | d2d1effects. h |
| Bibliothek | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
