---
title: Weißtonzuordnungseffekt
description: Dieser Effekt ermöglicht das lineare Skalieren der weißen Ebene eines Bilds. Dies ist besonders hilfreich, wenn Sie zwischen anzeigespezifischem Luminanzraum und szenenspezifischem Luminanzraum oder umgekehrt konvertieren.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 646ad47ad671618f29d1691878de93b5e5141855787c53fdad44025487835ad4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292630"
---
# <a name="white-level-adjustment-effect"></a>Auswirkung der Anpassung auf weißer Ebene

Dieser Effekt ermöglicht das lineare Skalieren der weißen Ebene eines Bilds. Dies ist besonders hilfreich, wenn Sie zwischen anzeigespezifischem Luminanzraum und szenenspezifischem Luminanzraum oder umgekehrt konvertieren.

Die Eigenschaften für diesen Effekt werden durch die [**D2D1_WHITELEVELADJUSTMENT_PROP-Enumeration**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)identifiziert, und die CLSID wird **CLSID_D2D1WhiteLevelAdjustment.**

## <a name="effect-properties"></a>Effect-Eigenschaften

| Anzeigename und Indexenumeration | Typ und Standardwert | Beschreibung |
|-|-|-|
| InputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL | GLEITKOMMAZAHL | Die weiße Ebene des Eingabebilds in 30 Grad. |
| OutputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL | GLEITKOMMAZAHL | Die weiße Ebene des Ausgabebilds in 30 Prozent. |

## <a name="remarks"></a>Hinweise
Dieser Effekt soll mit dem [HDR-Ton](hdr-tone-map-effect.md) map-Effekt kombiniert werden, damit Sie HDR-Bilder in Direct2D mit ordnungsgemäßer Farbverwaltung und Tonzuordnung rendern können. Weitere Informationen finden Sie **in den Anmerkungen** zu diesem Thema. Die Effekte sind auf jedes Framework ausgerichtet, das eine erstklassige HDR-Bildanzeige bereitstellen möchte, die alle Windows HDR-Bildformate verarbeitet und sich an die Funktionen der Anzeige anpasst (unabhängig davon, ob es sich um HDR oder WCG/SDR handelt).

Bei Windows wird davon ausgegangen, dass sich alle SDR-/WCG-Inhalte in einem anzeigespezifischen Leuchtdichtebereich befindet. Dies bedeutet, dass die weiße Ebene des Inhalts auf die weiße Ebene der Anzeige hochskaliert werden sollte, bevor sie letztendlich angezeigt wird. Es liegt jedoch nicht immer in der Verantwortung Ihrer Anwendung, dies zu tun. Im Gegensatz dazu wird davon ausgegangen, dass sich HDR-Inhalte in einem szenenspezifischen Leuchtdichtebereich befindet, was bedeutet, dass sie letztendlich nicht so skaliert werden sollten, dass sie der weißen Ebene der Anzeige passen. Ihre Anwendung muss jedoch unter bestimmten Umständen beim Rendern von HDR-Inhalten eine Skalierung durchführen, um sicherzustellen, dass dies das Nettoergebnis ist.

Wenn sich Windows Desktop im SDR- oder WCG-Modus befindet, besteht der Desktop in einem anzeigespezifischen Leuchtdichtebereich. Wenn sich der Windows desktop jedoch im HDR-Modus befindet, erfolgt die Desktopkomposition im szenenspezifischen Leuchtdichteraum. Das bedeutet, dass das Desktopfenster-Manager (DWM) selbst Leuchtdichteanpassungen (häufig als SDRBoost bezeichnet) für 8-Bit-Kompositionsoberflächen durchführt, was Ihre Anwendung für diesen Fall vereinfacht. Dennoch bedeutet die automatische Verstärkung, dass die Rolle Ihrer Anwendung bei der Konvertierung von einem Leuchtdichteraum in einen anderen vom Kompositionsformat abhängig ist, das Ihre Anwendung verwendet, um ihren Inhalt zu präsentieren.

In der folgenden Tabelle werden die Fälle beschrieben, in denen Ihre Anwendung eine Anpassung auf weißer Ebene durchführen sollte und was diese Anpassung sein sollte. Im Allgemeinen hängt die Anpassung von drei Faktoren ab.

1. Eingabeinhaltsfarbraum. Gibt an, ob Ihr Eingabeinhalt HDR-Luminanzwerte (High Dynamic Range) enthält oder nicht. WCG-Inhalt verhält sich für das Leuchtdichteverhalten genauso wie SDR.
2. Kompositionsformat. Das Pixelformat der Zieloberfläche, das dem DWM angezeigt wird, z. B. eine Austauschkette &mdash; oder eine [Kompositionsoberfläche.](/uwp/api/Windows.UI.Composition.ICompositionSurface) [](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) Beim Rendern mit Direct2D ist dies **entweder UINT8** oder **FP16.**
3. Erweiterter Desktopfarbmodus. Gibt an, ob das DWM für die aktuelle Anzeige im SDR-, WCG- oder HDR-Modus ausgeführt wird. Diese Informationen erhalten Sie [**über DXGI_OUTPUT_DESC1::ColorSpace**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) oder [**AdvancedColorInfo.CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind).

Basierend auf diesen drei Faktoren sollten Sie die entsprechenden Werte für die Eigenschaften `InputWhiteLevel` und `OutputWhiteLevel` festlegen.

|Eingabeinhalt|Kompositionsformat|Erweiterter Farbmodus|InputWhiteLevel|OutputWhiteLevel|
|-|-|-|-|-|
|SDR/WCG|**UINT8**|Any|–|Nicht zutreffend|
|SDR/WCG|**FP16**|SDR/WCG|Nicht zutreffend|Nicht zutreffend|
|SDR/WCG|**FP16**|Hdr|SDRWhite|80|
|Hdr|Beliebig|SDR/WCG|80|[**DXGI_OUTPUT_DESC1::MaxLudominanz**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)|
|Hdr|**UINT8**|Hdr|80|SDRWhite|
|Hdr|**FP16**|Hdr|Nicht zutreffend|Nicht zutreffend|

In der Tabelle ist der Wert 80 der Verweis-White-Level für sRGB- oder scRGB-Inhalt in Tafeln. Hierzu können Sie die Konstante D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL [**verwenden,**](/windows/desktop/direct2d/direct2d-constants)die in definiert `d2d1effects_2.h` ist. Der Wert ist die Anzahl der 3000-000-Daten, die die Anzeige verwenden soll, um weißen `SDRWhite` sRGB-Inhalt anzuzeigen. Sie können diesen Wert abrufen, indem Sie auf die [**AdvancedColorInfo.SdrWhiteLevelInNits-Eigenschaft**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits) zugreifen. Der Wert N/A bedeutet, dass in diesem Szenario keine Anpassung auf weißer Ebene verwendet wird. Sie können entweder den Effekt aus dem Diagramm entfernen oder Werte für einen No-Op festlegen.

Beachten Sie, dass das DWM oder die Anzeige in Fällen, in denen die Anwendung keine Anpassung des Leerraums benötigt, möglicherweise die Konvertierung vom anzeigebewöhnten Leuchtdichteraum in den auf die Szene verwiesenen Ludominanzraum umtauscht.

- Im SDR/WCG-Modus erfolgt die Konvertierung nach der DWM-Komposition und gilt für alle Inhalte, die dieser Anzeige angezeigt werden. Die Anzeige führt diese Konvertierung implizit aus.
- Im HDR-Modus wird die Konvertierung automatisch vom DWM vor der Komposition durchgeführt, solange die Kompositionsoberfläche Ihrer Anwendung SDR ist.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 10, Version 1809 (10.0; Build 17763) \[ Desktop-Apps \| UWP-Apps\] |
| Header | d2d1effects \_ 2.h |
| Bibliothek | d2d1.lib, dxguid.lib |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [D2D1_WHITELEVELADJUSTMENT_PROP Enumeration](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)
