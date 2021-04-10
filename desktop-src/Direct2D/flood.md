---
title: Überflutungseffekt
description: Verwenden Sie den überflutungseffekt, um eine Bitmap basierend auf der angegebenen Farbe und dem angegebenen Alpha Wert zu generieren. Sie können diesen Effekt verwenden, wenn Sie eine bestimmte Farbe als Eingabe für einen Effekt verwenden möchten, z. b. eine Hintergrundfarbe.
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- überflutungseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956851"
---
# <a name="flood-effect"></a>Überflutungseffekt

Verwenden Sie den überflutungseffekt, um eine Bitmap basierend auf der angegebenen Farbe und dem angegebenen Alpha Wert zu generieren. Sie können diesen Effekt verwenden, wenn Sie eine bestimmte Farbe als Eingabe für einen Effekt verwenden möchten, z. b. eine Hintergrundfarbe.

> [!Note]  
> Der Effekt wird an den angegebenen Farbwert weitergeleitet, wie angegeben. Sie müssen die Werte manuell vorab multiplizieren, wenn Sie beabsichtigen, die Ausgabe an Effekte zu übergeben, die eine vorab multiplizierte Eingabe erwarten.

 

Die CLSID für diesen Effekt ist CLSID \_ D2D1Flood.

Der überflutungseffekt hat kein Eingabebild.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

![Beispiel Bild des Überflutungs Effekts aus grün.](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color<br/> D2D1- \_ Überflutungs \_ \_ Farbe<br/> | Die Farbe und die Deckkraft der Bitmap. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 4f. Die einzelnen Werte für die einzelnen Kanäle sind vom Typ float, ungebunden und unitless. Der Effekt ändert nicht die Werte für die Kanäle.<br/> Die RGBA-Werte für jeden Kanal reichen von 0 bis 1.<br/> Der Typ ist "D2D1 \_ Vector \_ 4f".<br/> Der Standardwert ist {0,0 f, 0,0 f, 0,0 f, 1.0 f}.<br/> |



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Dieser Effekt generiert eine Bitmap mit logischer unbegrenzter groß.

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

 

