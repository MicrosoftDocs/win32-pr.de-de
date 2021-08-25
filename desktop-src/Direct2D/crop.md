---
title: Zuschneideeffekt
description: Verwenden Sie den Zuschneideeffekt, um einen angegebenen Bereich eines Bilds auszugeben.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- Zuschneideeffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e342bdef882fbff89d4c67c3accfbff7287a2ad9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472930"
---
# <a name="crop-effect"></a>Zuschneideeffekt

Verwenden Sie den Zuschneideeffekt, um einen angegebenen Bereich eines Bilds auszugeben.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Crop.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Ausgabebitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| Danach                                                      |
| ![das Bild nach der Transformation.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effekteigenschaften




| Anzeigename und Indexenumeration | Typ und Standardwert | BESCHREIBUNG | 
|------------------------------------|------------------------|-------------|
| Rect<br /> | D2D1_VECTOR_4F<br /> | Der Bereich, der als Vektor im Formular (links, oben, Breite, Höhe) angegeben werden soll.<br /> | 
| D2D1_CROP_PROP_RECT<br /> | {-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}<br /> | Die Einheiten befinden sich in DIPs. <br /><blockquote><p>[!Note]</p><p>Der Rect wird abgeschnitten, wenn er die Randgrenzen des Eingabebilds überlappt.<br /></p></blockquote><br /> | 
| D2D1_CROP_PROP_BORDER_MODE<br /> | D2D1_BORDER_MODE <br /> D2D1_BORDER_MODE_SOFT <br /> | <ul><li>D2D1_BORDER_MODE_SOFT : Wenn das Zuschneiderechteck auf Dezimalpixelkoordinaten fällt, wendet der Effekt Antialiasing an, was zu einem weichen Rand führt.</li><li>D2D1_BORDER_MODE_HARD: Wenn das Zuschneiderechteck auf Dezimalpunktkoordinaten fällt, wird der Effekt klammern, was zu einem harter Rand führt.</li></ul> | 




 

## <a name="output-bitmap"></a>Ausgabebitmap

Die Ausgabe dieses Effekts ist die Größe der Rect-Eigenschaft. Länge und Breite werden berechnet.

Mithilfe der hier beschriebenen Formeln: <dl> Ausgabelänge in Pixels=(Rect.Right-Rect.Left) \* (DPI/96 des Benutzers)  
Ausgabehöhe in Pixel=(Rect.Bottom-Rect.Top) \* (DPI/96 des Benutzers)  
</dl>

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

 

