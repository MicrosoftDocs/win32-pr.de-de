---
title: Kacheleffekt
description: Verwenden Sie den Kacheleffekt, um den angegebenen Bereich des Bilds zu wiederholen.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- Kacheleffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0df10143a727fb8ce6585264b65b6db46d75c731070f2ea46ff8e7dffd59dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430494"
---
# <a name="tile-effect"></a>Kacheleffekt

Verwenden Sie den Kacheleffekt, um den angegebenen Bereich des Bilds zu wiederholen.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Tile.

## <a name="example-image"></a>Beispielbild



| Vorher                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| Danach                                                      |
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



## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                | Typ und Standardwert                                              | Beschreibung                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Rect<br/> D2D1 \_ TILE \_ PROP \_ RECT<br/> | D2D1 \_ VECTOR \_ 4F<br/> {0.0f, 0.0f, 100.0f, 100.0f}<br/> | Der Bereich des Bilds, das gekachelt werden soll. Diese Eigenschaft ist ein D2D1 \_ VECTOR \_ 4F, der wie: (links, oben, rechts, unten) definiert ist. Die Einheiten befinden sich in DIPs.<br/> |



 

## <a name="output-bitmap"></a>Ausgabebitmap

Dieser Effekt generiert eine Bitmap mit logisch unendlicher Größe.

Sie können ein Bild kacheln und eine bestimmte Größe ohne zusätzliche Auswirkungen ausgegeben, indem Sie die Größe festlegen, wenn Sie [**ID2D1DeviceContext::D rawImage aufrufen.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode))

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

 

