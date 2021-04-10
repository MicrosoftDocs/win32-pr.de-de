---
title: Kachel Effekt
description: Verwenden Sie den Kachel Effekt, um den angegebenen Bereich des Bilds zu wiederholen.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- Kachel Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5def48ab30cadb28673179f6eec5d7ffa7e19e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040688"
---
# <a name="tile-effect"></a>Kachel Effekt

Verwenden Sie den Kachel Effekt, um den angegebenen Bereich des Bilds zu wiederholen.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Tile.

## <a name="example-image"></a>Beispielbild



| Vorher                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| Nach                                                      |
| ![das Bild nach der Transformation.](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                | Typ und Standardwert                                              | BESCHREIBUNG                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Rect<br/> D2D1- \_ Kachel- \_ Prop- \_ Rect<br/> | D2D1 \_ Vector \_ 4f<br/> {0,0 f, 0,0 f, 100,0 f, 100,0 f}<br/> | Der Bereich des Bilds, das gekachelt werden soll. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 4f, definiert als: (Links, oben, rechts, unten). Die Einheiten befinden sich in Dips.<br/> |



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Dieser Effekt generiert eine Bitmap mit logischer unbegrenzter groß.

Sie können ein Bildkacheln und eine bestimmte Größe ohne zusätzliche Effekte ausgeben, indem Sie die Größe beim Abrufen von [**ID2D1DeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode))festlegen.

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

 

