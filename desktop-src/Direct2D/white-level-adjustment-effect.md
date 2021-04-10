---
title: Effekt der weißen Tonkarte
description: Dieser Effekt ermöglicht die Lineare Skalierung der weißen Ebene eines Bilds. Dies ist besonders hilfreich, wenn Sie zwischen einem Anzeigebereich und einem von der Szene bezeichneten Glanz Bereich wechseln, oder umgekehrt.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 70a38f37f5a5461b968099bebe4be120a727c053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956706"
---
# <a name="white-level-adjustment-effect"></a>Anpassungs Effekt auf weißer Ebene

Dieser Effekt ermöglicht die Lineare Skalierung der weißen Ebene eines Bilds. Dies ist besonders hilfreich, wenn Sie zwischen einem Anzeigebereich und einem von der Szene bezeichneten Glanz Bereich wechseln, oder umgekehrt.

Die Eigenschaften für diesen Effekt werden durch die [**D2D1_WHITELEVELADJUSTMENT_PROP-Enumeration**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)identifiziert, und die CLSID ist **CLSID_D2D1WhiteLevelAdjustment**.

## <a name="effect-properties"></a>Effekt Eigenschaften

| Anzeige Name und indexenumeration | Typ und Standardwert | BESCHREIBUNG |
|-|-|-|
| Inputwhitelevel, D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL | GLEITKOMMAZAHL | Die weiße Ebene des Eingabe Bilds in Nits. |
| Outputwhitelevel, D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL | GLEITKOMMAZAHL | Die weiße Ebene des Ausgabe Bilds in Nits. |

## <a name="remarks"></a>Bemerkungen
Dieser Effekt soll mit dem Code der HDR- [tonmap](hdr-tone-map-effect.md) kombiniert werden, damit Sie HDR-Bilder in Direct2D mit entsprechender Farbverwaltung und Ton Zuordnung Rendering können. Weitere Informationen finden Sie in den **Anmerkungen** zu diesem Thema. Die Auswirkungen sind auf jedes Framework ausgerichtet, das eine erstklassige HDR-Bild Anzeige bietet, die alle Windows HDR-Bildformate verarbeitet, und sich an die Funktionen der Anzeige anpasst (ob HDR oder WCG/SDR).

Unter Windows wird davon ausgegangen, dass sich der Inhalt von "SDR/WCG" in einem von der Anzeige referenzierten Glanz Bereich befindet. Dies bedeutet, dass die weiß Ebene des Inhalts auf die weiße Ebene der Anzeige hochskaliert werden soll, bevor Sie letztendlich angezeigt wird. Es ist jedoch nicht immer die Aufgabe Ihrer Anwendung, dies zu tun. Im Gegensatz dazu wird davon ausgegangen, dass sich der HDR-Inhalt in einem in der Szene bezeichneten Glanz Bereich befindet. Dies bedeutet, dass er letztlich nicht so skaliert werden kann, dass er der weißen Ebene der Anzeige entspricht Dies bedeutet, dass Ihre Anwendung in einigen Fällen die Skalierung durchführen muss, wenn HDR-Inhalte gerendert werden, um sicherzustellen, dass dies das Ergebnis ist.

Wenn sich der Windows-Desktop im SDR-oder WCG-Modus befindet, wird der Desktop in einem von der Anzeige bezeichneten Glanz Bereich zusammengesetzt. Wenn sich der Windows-Desktop jedoch im HDR-Modus befindet, erfolgt die Desktop Komposition in einem von der Szene bezeichneten Glanz Bereich. Dies bedeutet, dass der Desktopfenster-Manager (DWM) selbst für 8-Bit-Kompositions Oberflächen Beleuchtungs Anpassungen durchführt (oftmals "sdrboost" genannt), die Ihre Anwendung in diesem Fall vereinfachen. Dies bedeutet, dass die automatische Verstärkung bedeutet, dass die Rolle Ihrer Anwendung bei der Umstellung von einem Lichtbereich in einen anderen von dem Kompositions Format abhängt, das Ihre Anwendung zur Darstellung des Inhalts verwendet.

In der folgenden Tabelle werden die Fälle beschrieben, in denen Ihre Anwendung eine Anpassung auf der weißen Ebene ausführen sollte und sollte, und was diese Anpassung sein sollte. Im Allgemeinen hängt die Anpassung von drei Faktoren ab.

1. Eingabe Inhalt colorspace. Gibt an, ob die Eingabe Inhalte hohe Werte für den dynamischen Bereich (HDR) enthalten. WCG-Inhalt verhält sich mit dem Verhalten von "SDR" für das Verhalten der Beleuchtung.
2. Kompositions Format. Das Pixel Format der dem DWM dargestellten Ziel Oberfläche &mdash; , z. b. eine [Swapkette](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) oder eine [Kompositions Oberfläche](/uwp/api/Windows.UI.Composition.ICompositionSurface). Wenn Sie mit Direct2D rendern, ist dies entweder **Uint8** oder **FP16**.
3. Modus für erweiterte Desktop Farben. Gibt an, ob die DWM für die aktuelle Anzeige im Modus "SZR", "WCG" oder "HDR" ausgeführt wird. Rufen Sie diese Informationen über [**DXGI_OUTPUT_DESC1:: colorspace**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) oder [**advancedcolorinfo. currentadvancedcolorkind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind)ab.

Basierend auf diesen drei Faktoren sollten Sie die entsprechenden Werte für die-Eigenschaft `InputWhiteLevel` und die-Eigenschaft festlegen `OutputWhiteLevel` .

|Eingabe Inhalt|Kompositions Format|Erweiterter Farbmodus|Input whitelevel|Outputwhitelevel|
|-|-|-|-|-|
|SZR/WCG|**UINT8**|Any|–|–|
|SZR/WCG|**FP16**|SZR/WCG|–|–|
|SZR/WCG|**FP16**|HDR|Sdrwhite|80|
|HDR|Any|SZR/WCG|80|[**DXGI_OUTPUT_DESC1:: maxluminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)|
|HDR|**UINT8**|HDR|80|Sdrwhite|
|HDR|**FP16**|HDR|–|–|

In der Tabelle ist der Wert 80 die Referenz-weißen Ebene in Nits für sRGB-oder ScRGB-Inhalt. Hierfür können Sie die Konstante [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](/windows/desktop/direct2d/direct2d-constants)verwenden, die in definiert ist `d2d1effects_2.h` . Der Wert `SDRWhite` ist die Anzahl der Nits, die die Anzeige zum Anzeigen von weißem sRGB-Inhalt verwenden soll. Sie können diesen Wert abrufen, indem Sie auf die [**advancedcolorinfo. sdrwhitelevelinnits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits) -Eigenschaft zugreifen. Der Wert "N/A" bedeutet, dass die Anpassung der weißen Ebene in diesem Szenario nicht verwendet wird. Sie können den Effekt entweder aus dem Diagramm entfernen oder Werte für einen No-op-Wert festlegen.

Beachten Sie, dass in Fällen, in denen eine Anpassung der weißen Ebene von der Anwendung nicht benötigt wird, die DWM-oder die-Anzeige möglicherweise die Konvertierung von einem Anzeigebereich in den Glanz Bereich in den hell Bereich verarbeitet.

- Im Modus "SZR/WCG" erfolgt die Konvertierung nach der DWM-Komposition und gilt für alle Inhalte, die dieser Anzeige angezeigt werden. Diese Konvertierung wird von der Anzeige implizit durchführt.
- Im HDR-Modus wird die Konvertierung automatisch von der DWM vor der Komposition durchgeführt, solange die Kompositions Oberfläche Ihrer Anwendung SZR ist.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 10, Version 1809 (10,0; Build 17763) \[ Desktop-Apps \| UWP-apps\] |
| Header | d2d1effects \_ 2. h |
| Bibliothek | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [D2D1_WHITELEVELADJUSTMENT_PROP-Enumeration](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)
