---
title: Effekt der Verschiebungszuordnung
description: Verwenden Sie den Verschiebungszuordnungseffekt, um die Pixel des Eingabebilds durch die Intensitätswerte eines zweiten Eingabebilds zu verfängigen.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- Verschiebungszuordnungseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73888d8168e411bf0f8daee1f2e04801353ee8358d27ba4d5cc9b1f71630a762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833014"
---
# <a name="displacement-map-effect"></a>Effekt der Verschiebungszuordnung

Verwenden Sie den Verschiebungszuordnungseffekt, um die Pixel des Eingabebilds durch die Intensitätswerte eines zweiten Eingabebilds zu verfängigen.

Die CLSID für diesen Effekt ist CLSID \_ D2D1DisplacementMap.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Farbkanäle](#color-channels)
-   [Ausgabebitmap](#output-bitmap)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                           |
|------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)       |
| Danach                                                            |
| ![das Bild nach der Transformation.](images/19-displacementmap.png) |



 


```C++
ComPtr<ID2D1Effect> displacementMapEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DisplacementMap, &displacementMapEffect);

displacementMapEffect->SetInput(0, bitmap);
displacementMapEffect->SetValue(D2D1_DISPLACEMENTMAP_PROP_SCALE, 100.0f);

// The second input of the displacement effect determines how the input image is transformed.
// For this example, we will use a turbulence effect as the second input to randomly distort the image.
ComPtr<ID2D1Effect> turbulenceEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Turbulence, &turbulenceEffect);
displacementMapEffect->SetInputEffect(1, turbulenceEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(displacementMapEffect.Get());
m_d2dContext->EndDraw();
```



Die Positionen der Pixel in der Ausgabe werden mithilfe dieser Formel bestimmt:

C' (x,y)=C(x+ scale \* (XChannelSelector(Bitmap für Verschiebung (x,y))-0,5),y+ scale \* (YChannelSelector(Bitmap für Verschiebung (x,y))-0.5))

Hierbei gilt:<dl> *C (x, y)* ist das Ausgabepixel bei (x, y).  
*C (x, y)* ist das Eingabepixel bei (x, y).  
*Verschiebungsbitmap (x, y)* ist die Intensität des Verschiebungspixels an den angegebenen Koordinaten.  
*XChannelSelector die* Intensität des ausgewählten RGBA-Kanals aus der Verschiebungsbitmap, die das Eingabebild in X-Richtung zurückdrängt.  
*YChannelSelector die* Intensität des ausgewählten RGBA-Kanals aus der Verschiebungsbitmap, die das Eingabebild in Y-Richtung zurückdrängt.  
</dl>

Der Effekt verwendet das Eingabebild entsprechend der Skalierungseigenschaft und der Intensität des Verschiebungsbilds neu. Sie verwendet die bilineare Interpolation, wenn die Stichprobenentnahme zwischen Pixeln im Eingabebild durchgeführt wird.

Dieser Effekt funktioniert bei geraden und prämultipliierten Alphabildern. Das Ausgabe alpha-Format ist mit dem Eingabeformat identisch.

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                   | Typ und Standardwert                                                   | BESCHREIBUNG                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Skalieren<br/> D2D1– \_ \_ VERLAGERUNGMAP–PROP-SKALIERUNG \_<br/>                       | GLEITKOMMAZAHL<br/> 0,0f<br/>                                         | Multipliziert die Intensität des ausgewählten Kanals mit dem Verschiebungsbild. Je höher Sie diese Eigenschaft festlegen, desto stärker wirkt sich der Effekt auf die Pixel aus.<br/>                       |
| XChannelSelect<br/> D2D1 \_ – VERLAGERUNGMAP \_ PROP X KANAL \_ \_ \_ AUSWÄHLEN<br/> | \_D2D1-KANALAUSWAHL \_<br/> \_D2D1-KANALAUSWAHL \_ \_ A<br/> | Der Effekt extrahiert die Intensität aus diesem Farbkanal und verwendet sie, um das Bild räumlich in X-Richtung zu überdrängen. Weitere [Informationen finden Sie unter](#color-channels) Farbkanäle.<br/> |
| YChannelSelect<br/> D2D1– \_ 2D1 – PROP \_ \_ \_ Y-KANAL – \_ AUSWÄHLEN<br/> | \_D2D1-KANALAUSWAHL \_<br/> \_D2D1-KANALAUSWAHL \_ \_ A<br/> | Der Effekt extrahiert die Intensität aus diesem Farbkanal und verwendet sie, um das Bild räumlich in Y-Richtung zu überdrängen. Weitere [Informationen finden Sie unter](#color-channels) Farbkanäle.<br/> |



 

## <a name="color-channels"></a>Farbkanäle



| Enumeration                | Beschreibung                                                      |
|----------------------------|------------------------------------------------------------------|
| \_D2D1-KANALAUSWAHL \_ \_ R | Der Effekt extrahiert die Intensitätsausgabe aus dem roten Kanal.   |
| \_D2D1-KANALAUSWAHL \_ \_ G | Der Effekt extrahiert die Intensitätsausgabe aus dem grünen Kanal. |
| \_D2D1-KANALAUSWAHL \_ \_ B | Der Effekt extrahiert die Intensitätsausgabe aus dem blauen Kanal.  |
| \_D2D1-KANALAUSWAHL \_ \_ A | Der Effekt extrahiert die Intensitätsausgabe aus dem Alphakanal. |



 

## <a name="output-bitmap"></a>Ausgabebitmap

Sie können die maximale Größe der Ausgabebitmap mit den folgenden Gleichungen bestimmen:

Ausgabebitmap? Pixels=(Input Bitmap Size?( DIPs)+Scale) \* (Benutzer-DPI/96)

<sub>Ausgabebitmap y</sub> Pixels=(Input Bitmap Size<sub>y</sub>(DIPs) + Scale) \* (User DPI/96)

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

 

