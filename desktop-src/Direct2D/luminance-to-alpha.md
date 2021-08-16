---
title: Leuchtdichte zu Alphaeffekt
description: Verwenden Sie die Leuchtdichte für den Alphaeffekt, um den Alphakanal auf die Leuchtdichte des Bilds festzulegen, und legen Sie die Farbkanäle auf 0 fest.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- Leuchtdichte zu Alphaeffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803070fea76b47c1334803a4e7f8fef510cc77c8b3bc05c8477b572cb0451670
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825258"
---
# <a name="luminance-to-alpha-effect"></a>Leuchtdichte zu Alphaeffekt

Verwenden Sie die Leuchtdichte für den Alphaeffekt, um den Alphakanal auf die Leuchtdichte des Bilds festzulegen, und legen Sie die Farbkanäle auf 0 fest. Sie können die Ausgabe dieses Effekts verwenden, um eine semitransparente Überlagerung basierend auf der Helligkeit des Eingabebilds zu erstellen. Sie können es auch verwenden, um eine Bildmaske zu erstellen.

> [!Note]  
> Dieser Effekt hat keine Eigenschaften.

 

Die CLSID für diesen Effekt ist CLSID \_ D2D1LuminanceToAlpha.

## <a name="example-image"></a>Beispielbild

Dieses Beispiel zeigt die Ausgabe der Leuchtdichte für den Alphaeffekt, die über einer weißen Oberfläche zusammengesetzt ist, um Deckkraft anzuzeigen.



| Vorher                                                            |
|-------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)        |
| Danach                                                             |
| ![das Bild nach der Transformation.](images/18-luminancetoalpha.png) |



 


```C++
ComPtr<ID2D1Effect> luminanceToAlphaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LuminanceToAlpha, &luminanceToAlphaEffect);

luminanceToAlphaEffect->SetInput(0, bitmap);

// LuminanceToAlpha result is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);
floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, luminanceToAlphaEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



Dieser Effekt legt den Alphakanal der Ausgabe mithilfe dieser Farbmatrix auf die Leuchtdichte des Eingabebilds fest.

![Die Farbmatrix, die der Effekt verwendet, um den Alphakanal festzulegen.](images/luminance-to-alpha-math1.png)

Dieser Effekt nutzt und gibt prämultipliierte Alphabilder aus. Der Effekt funktioniert nur bei alphangeraden Bildern, wenn sie vollständig deckend sind.

> [!Note]
>
> Da Bilder in einem Gammakompensierungsformat gespeichert werden, sollten Sie vor dem Berechnen der Leuchtdichte für ein Bild zuerst eine umgekehrte Gammakorrektur durchführen, um die tatsächlichen Farbwerte für das Bild abzurufen. Da Bilder normalerweise bei 2,2 Gamma gespeichert werden, können Sie den Gammaübertragungseffekt mit einem Exponenten von (1/2.2) verwenden und dann die Ausgabe dieses Effekts verwenden.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects.h                                                                      |
| Bibliothek                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="output-bitmap"></a>Ausgabebitmap

Die Ausgabe hat die gleiche Größe wie das Eingabebild.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
