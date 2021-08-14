---
title: HDR-Tonzuordnungseffekt
description: Dieser Effekt passt den dynamischen Bereich eines Bilds an, um seinen Inhalt besser an die Funktion der Ausgabeanzeige anzupassen.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: ce47159abe4bdf0615a76960c4c5e2db289156e89989012f659e437e93727cca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260063"
---
# <a name="hdr-tone-map-effect"></a>HDR-Tonzuordnungseffekt

Dieser Effekt passt den dynamischen Bereich eines Bilds an, um seinen Inhalt besser an die Funktion der Ausgabeanzeige anzupassen.

Die Eigenschaften für diesen Effekt werden durch die [**D2D1_HDRTONEMAP_PROP-Enumeration**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)identifiziert, und die CLSID wird **CLSID_D2D1HdrToneMap.**

## <a name="effect-properties"></a>Effect-Eigenschaften

| Anzeigename und Indexenumeration | Typ und Standardwert | BESCHREIBUNG |
|-|-|-|
| InputMaxLuminance, D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE | GLEITKOMMAZAHL | Der maximale Lichtpegel (oder MaxCLL) des Bilds in Glühbirnen. |
| OutputMaxLuminance, D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE | GLEITKOMMAZAHL | Der vom Ausgabeziel unterstützte MaxCLL-Besatz in Der Regel ist auf &mdash; maxCLL der Anzeige festgelegt. |
| DisplayMode, D2D1_HDRTONEMAP_PROP_DISPLAY_MODE | [**D2D1_HDRTONEMAP_DISPLAY_MODE**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_display_mode) | Wenn auf **_HDR** festgelegt ist, wird die Tonzuordnungskurve angepasst, um besser an das Verhalten gängiger HDR-Displays anzupassen. |

## <a name="remarks"></a>Hinweise
Der Wert für `InputMaxLuminance` wird in der Regel von den Bildmetadaten abgeleitet. In Fällen, in denen die Metadaten nicht vorhanden sind, können Sie die **D2DAdvancedColorImagesRenderer::ComputeHdrMetadata-Funktion** (im [Erweiterten Direct2D-Farbbildrenderingbeispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)) verwenden, um den maximalen Lichtpegel (MaxCLL) eines Bilds in Glühbirnen zu berechnen.

Der Wert für `OutputMaxLuminance` ist so konzipiert, dass er mithilfe von [**DXGI_OUTPUT_DESC1::MaxLudomanz**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)von der Anzeige abgeleitet wird.

Der HDR-Tonzuordnungseffekt hat unterschiedliche Tonzuordnungskurven, je nachdem, ob es sich bei der Anzeige um eine HDR-Anzeige oder eine SDR/WCG-Anzeige handelt.

Dieser Effekt soll mit dem Anpassungseffekt white [level](white-level-adjustment-effect.md) kombiniert werden, damit Sie HDR-Bilder in Direct2D mit ordnungsgemäßer Farbverwaltung und Tonzuordnung rendern können. Sie richtet sich an jedes Framework, das eine erstklassige HDR-Bildanzeige bereitstellen möchte, die alle Windows HDR-Bildformate verarbeitet und sich an die Funktionen der Anzeige anpasst (ob HDR oder WCG/SDR). Die Auswirkungen sollen wie unten beschrieben nacheinander verkettet werden.

- Nehmen Sie das Eingabebild, dessen Farbraum durch seinen Codec definiert wird. Metadaten können whitePoint angeben. Metadaten können die Eingabedominanzstufe angeben.
- Wenden Sie den Farbverwaltungseffekt an. Konvertieren sie in scRGB-Speicherplatz (SCRGB).
- Wenden Sie den HDR-Tonzuordnungseffekt an. Senken Sie den Lichtpegel des Bilds auf die gewünschte Ebene.
- Wenden Sie den Anpassungseffekt auf weißer Ebene an. Skalieren Sie die weiß-Ebene des Bilds auf die weiß-Ebene, die für die Austauschkette erforderlich ist.
- Wenden Sie den Farbverwaltungseffekt erneut an. Wenn Sie zu 8bpc rendern, konvertieren Sie in sRGB.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 10, Version 1809 (10.0; Build 17763) \[ Desktop-Apps \| UWP-Apps\] |
| Header | d2d1effects \_ 2.h |
| Bibliothek | d2d1.lib, dxguid.lib |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [D2D1_HDRTONEMAP_PROP Enumeration](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)
