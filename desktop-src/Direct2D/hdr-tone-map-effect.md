---
title: HDR-Ton Zuordnungs Effekt
description: Dadurch wird der dynamische Bereich eines Bilds so angepasst, dass es seinen Inhalt besser an die Funktion der Ausgabe Anzeige anpasst.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 4c9234e1b50e155173630a2ff7d94756c5be6130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858988"
---
# <a name="hdr-tone-map-effect"></a>HDR-Ton Zuordnungs Effekt

Dadurch wird der dynamische Bereich eines Bilds so angepasst, dass es seinen Inhalt besser an die Funktion der Ausgabe Anzeige anpasst.

Die Eigenschaften für diesen Effekt werden durch die [**D2D1_HDRTONEMAP_PROP-Enumeration**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)identifiziert, und die CLSID ist **CLSID_D2D1HdrToneMap**.

## <a name="effect-properties"></a>Effekt Eigenschaften

| Anzeige Name und indexenumeration | Typ und Standardwert | BESCHREIBUNG |
|-|-|-|
| Inputmaxluminance, D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE | GLEITKOMMAZAHL | Die maximale helle Ebene (oder maxcll) des Bilds in Nits. |
| Outputmaxluminance, D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE | GLEITKOMMAZAHL | Das vom Ausgabeziel unterstützte maxcll in Nits, das in der &mdash; Regel auf die maxcll der Anzeige festgelegt ist. |
| Display Mode, D2D1_HDRTONEMAP_PROP_DISPLAY_MODE | [**D2D1_HDRTONEMAP_DISPLAY_MODE**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_display_mode) | Wenn diese Einstellung auf **_HDR** festgelegt ist, wird die tonzuordnungskurve angepasst, um das Verhalten von gängigen HDR-anzeigen besser anzupassen. |

## <a name="remarks"></a>Bemerkungen
Der Wert für `InputMaxLuminance` wird in der Regel von den Bild Metadaten abgeleitet. In Fällen, in denen die Metadaten nicht vorhanden sind, können Sie die Funktion **D2DAdvancedColorImagesRenderer:: computehdrmetadata** (im [Beispiel Direct2D Advanced Color Image Rendering](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)) verwenden, um die maximale Lichtebene (maxcll) eines Bilds in Nits zu berechnen.

Der Wert für `OutputMaxLuminance` ist so konzipiert, dass er von der Anzeige mithilfe von [**DXGI_OUTPUT_DESC1:: maxluminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)abgeleitet wird.

Der HDR-Ton Zuordnungs Effekt hat unterschiedliche Karten Kurven, abhängig davon, ob es sich um eine HDR-Anzeige oder eine SZR-/WCG-Anzeige handelt.

Dieser Effekt ist dafür vorgesehen, mit dem [Anpassungs Effekt auf der weißen Ebene](white-level-adjustment-effect.md) kombiniert zu werden, damit Sie HDR-Bilder in Direct2D mit entsprechender Farbverwaltung und Ton Zuordnung Rendering können. Es richtet sich an jedes Framework, das eine erstklassige HDR-Bild Anzeige bietet, das alle Windows HDR-Bildformate verarbeitet und sich an die Funktionen der Anzeige anpasst (ob HDR oder WCG/SDR). Die Effekte sind so ausgerichtet, dass Sie nacheinander verkettet werden, wie unten beschrieben.

- Nehmen Sie das Eingabebild, dessen Farbraum durch seinen Codec definiert ist. Metadaten können einen WhitePoint angeben. Metadaten können die Eingabe-Leuchtkraft Ebene angeben.
- Anwenden des Farb Verwaltungs Effekts. In ScRGB-Speicher (CCCS) konvertieren.
- Anwenden des HDR-Ton Zuordnungs Effekts. Verringern Sie die helle Ebene des Bilds auf die gewünschte Ebene.
- Anwenden des Anpassungs Effekts auf der weißen Ebene. Skalieren Sie die weiße Ebene des Bilds auf die für die Swapkette erforderliche weiße Ebene.
- Wenden Sie den Farb Verwaltungs Effekt erneut an. Wenn Sie in 8bpc rendern, konvertieren Sie in sRGB.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 10, Version 1809 (10,0; Build 17763) \[ Desktop-Apps \| UWP-apps\] |
| Header | d2d1effects \_ 2. h |
| Bibliothek | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [D2D1_HDRTONEMAP_PROP-Enumeration](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)
