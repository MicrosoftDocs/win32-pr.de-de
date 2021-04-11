---
title: Auswirkung der Verschiebungs Zuordnung
description: Verwenden Sie den Verschiebungs Zuordnungs Effekt, um die Pixel des Eingabe Bilds anhand der Intensität der Werte eines zweiten Eingabe Bilds zu übertragen.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- Auswirkung der Verschiebungs Zuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ad2deb0c584ccc9c55faebd60f803d66efa42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102951"
---
# <a name="displacement-map-effect"></a>Auswirkung der Verschiebungs Zuordnung

Verwenden Sie den Verschiebungs Zuordnungs Effekt, um die Pixel des Eingabe Bilds anhand der Intensität der Werte eines zweiten Eingabe Bilds zu übertragen.

Die CLSID für diesen Effekt ist CLSID \_ D2D1DisplacementMap.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Farbkanäle](#color-channels)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                           |
|------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)       |
| Nach                                                            |
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



Die Speicherorte der Pixel in der Ausgabe werden mithilfe der folgenden Formel bestimmt:

C ' (x, y) = c (x + Skala \* (xchannelselector (Verschiebungs Bitmap (x, y))-0,5), y + Skala \* (ychannelselector (Verschiebungs Bitmap (x, y))-0,5))

Hierbei gilt:<dl> *C (x, y)* ist das Ausgabe Pixel bei (x, y).  
*C (x, y)* ist das Eingabe Pixel bei (x, y).  
Die *Verschiebungs Bitmap (x, y)* ist die Verschiebungs Pixel Intensität an den angegebenen Koordinaten.  
*Xchannelselector* die Intensität des ausgewählten RGBA-Kanals aus der Verschiebungs Bitmap, die das Eingabebild in der X-Richtung verschiebt.  
*Ychannelselector* die Intensität des ausgewählten RGBA-Kanals aus der Verschiebungs Bitmap, die das Eingabebild in der Y-Richtung verschiebt.  
</dl>

Der Effekt zeigt das Eingabebild anhand der Skalierungs Eigenschaft und der Intensität des Verschiebungs Bilds neu an. Sie verwendet die bilineare interpolung, wenn eine Stichprobenentnahme zwischen Pixeln im Eingabebild erfolgt.

Dieser Effekt kann bei geraden und vorab multiplizierten Alpha Bildern verwendet werden. Das Alpha Format der Ausgabe ist mit dem Eingabeformat identisch.

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                   | Typ und Standardwert                                                   | BESCHREIBUNG                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Skalieren<br/> D2D1 \_ Verschiebungen der Verschiebungen \_ \_<br/>                       | GLEITKOMMAZAHL<br/> 0,0 f<br/>                                         | Multipliziert die Intensität des ausgewählten Kanals vom Verschiebungs Bild. Je höher Sie diese Eigenschaft festlegen, desto mehr werden die Pixel durch die Auswirkung verlagert.<br/>                       |
| Xchannelselect<br/> D2D1 \_ Verschiebungen in der \_ X- \_ Kanal-Prop \_ \_ auswählen<br/> | D2D1 \_ - \_ kanalselektor<br/> D2D1 \_ \_ kanalselektor \_ A<br/> | Der Effekt extrahiert die Intensität aus diesem Farbkanal und verwendet diese, um das Bild in der X-Richtung räumlich zu verzahnen. Weitere Informationen finden Sie unter [Color Channels](#color-channels) .<br/> |
| Ychannelselect<br/> D2D1 \_ Verschiebungen der Zuordnung für \_ Y- \_ \_ Kanal \_ auswählen<br/> | D2D1 \_ - \_ kanalselektor<br/> D2D1 \_ \_ kanalselektor \_ A<br/> | Der Effekt extrahiert die Intensität aus diesem Farbkanal und verwendet diese, um das Bild in der Y-Richtung räumlich zu verzahnen. Weitere Informationen finden Sie unter [Color Channels](#color-channels) .<br/> |



 

## <a name="color-channels"></a>Farbkanäle



| Enumeration                | Beschreibung                                                      |
|----------------------------|------------------------------------------------------------------|
| D2D1 \_ - \_ kanalselektor \_ R | Der Effekt extrahiert die Intensität der Ausgabe des roten Kanals.   |
| D2D1 \_ Kanal \_ Auswahl \_ G | Der Effekt extrahiert die Intensität der Ausgabe aus dem grünen Kanal. |
| D2D1 \_ - \_ kanalselektor \_ B | Der Effekt extrahiert die Intensität der Ausgabe aus dem blauen Kanal.  |
| D2D1 \_ \_ kanalselektor \_ A | Der Effekt extrahiert die Intensität der Ausgabe aus dem Alphakanal. |



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Sie können die maximale Größe der Ausgabe Bitmap mit den folgenden Gleichungen ermitteln:

Ausgabe Bitmap? Pixel = (Eingabe Bitmapgröße?) ( Dips) + Skalierung \* (Benutzer dpi/96)

Ausgabe Bitmap<sub>y</sub> Pixel = (Eingabe Bitmapgröße<sub>y</sub>(Dips) + Skala) \* (Benutzer dpi/96)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Header                   | d2d1effects. h                                                                      |
| Bibliothek                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

