---
title: Helligkeits Effekt
description: Verwenden Sie den Helligkeits Effekt, um die Helligkeit des Bilds zu steuern.
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- Helligkeits Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dd9797aa125e7099ba4a706bac730a30715f6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104554065"
---
# <a name="brightness-effect"></a>Helligkeits Effekt

Verwenden Sie den Helligkeits Effekt, um die Helligkeit des Bilds zu steuern.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Brightness.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                      |
|-------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)  |
| Nach                                                       |
| ![das Bild nach der Transformation.](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name der Eigenschaft                                                 | Typ und Standardwert                              | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WhitePoint<br/> D2D1 Helligkeit-Trennzeichen \_ \_ \_ \_<br/> | D2D1 \_ Vector \_ 2F<br/> {1.0 f, 1.0 f}<br/> | Der obere Teil der Helligkeits Übertragungs Kurve. Der weiße Punkt passt die Darstellung der helleren Teile des Bilds an. Diese Eigenschaft gilt für den x-Wert und den y-Wert in dieser Reihenfolge. Jeder Wert dieser Eigenschaft liegt zwischen 0 und 1 (einschließlich). |
| Blackpoint<br/> D2D1 Helligkeit-Trennzeichen \_ \_ \_ schwarz \_ Punkt<br/> | D2D1 \_ Vector \_ 2F<br/> {0,0 f, 0,0 f}<br/> | Der untere Teil der Helligkeits Übertragungs Kurve. Der schwarze Punkt passt die Darstellung der dunkleren Teile des Bilds an. Diese Eigenschaft gilt für den x-Wert und den y-Wert in dieser Reihenfolge. Jeder Wert dieser Eigenschaft liegt zwischen 0 und 1 (einschließlich).   |



 

Dieser Effekt verwendet die angegebenen weißen und schwarzen Punkte, um eine Übertragungsfunktion zu generieren, mit der die Bitmap angepasst wird. In der nächsten Gleichung wird die Übertragungsfunktion beschrieben. Die Eingabe Intensitäten werden zwischen 0 und 1 definiert.

![Helligkeits Algorithmus](images/brightness-formula1.png)

Der Effekt Algorithmus implementiert eine Gleichung, die die Übertragungsfunktion erstellt. Mit dieser Funktion werden die Bild Pixel angepasst. Der x-und der y-Wert des schwarzen Punkts und der weiße Punkt sind die Koordinaten in zwei Dimensionen, die mit der Transformation verbunden sind. Jeder Teil der endgültigen Ausgabe Gleichung:

1.  Konvertiert die Bilddaten aus dem linearen Raum mithilfe dieser Gleichung in einen nichtlinearen Raum:![Hilfsfunktion 1](images/brightness-formula2.png)

2.  Passt das Bild entsprechend den folgenden Werten an:
    -   *Input* ist die Pixel Intensität der Eingabebild Werte zwischen 0 und 1.

    -   *White PT. (x, y)* der Speicherort der Transformations Kurve für hellere Pixel Intensitäten.

    -   *Schwarz PT. (x, y)* ist der Speicherort der Transformations Kurve für schwächer-Pixel Intensitäten.

3.  Konvertiert die Bilddaten mit dieser Gleichung zurück in den linearen Raum: ![Hilfsfunktion 2](images/brightness-formula3.png)

Hier werden die endgültige Ausgabe Gleichung und die Komponenten Teile angezeigt.

![die gesamten Berechnungen für die Helligkeitsanpassung](images/brightness-formula4.png)

## <a name="output-bitmap"></a>Ausgabe Bitmap

Die Größe der Ausgabe Bitmap entspricht der Größe der Eingabe Bitmap.

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

 

