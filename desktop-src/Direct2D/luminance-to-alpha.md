---
title: Leuchtkraft zum Alpha Effekt
description: Legen Sie den Alpha-Kanal mit der Leuchtkraft des Bilds fest, und legen Sie die Farbkanäle auf 0 fest.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- Leuchtkraft zum Alpha Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb4c6fb78a1d49498b2adab6716d41e93d30deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104553037"
---
# <a name="luminance-to-alpha-effect"></a>Leuchtkraft zum Alpha Effekt

Legen Sie den Alpha-Kanal mit der Leuchtkraft des Bilds fest, und legen Sie die Farbkanäle auf 0 fest. Sie können die Ausgabe dieses Effekts verwenden, um einen semitransparenten Overlay basierend auf der Helligkeit des Eingabe Bilds zu erstellen. Oder Sie können Sie verwenden, um eine Bildmaske zu erstellen.

> [!Note]  
> Dieser Effekt hat keine Eigenschaften.

 

Die CLSID für diesen Effekt ist CLSID \_ D2D1LuminanceToAlpha.

## <a name="example-image"></a>Beispielbild

Dieses Beispiel zeigt die Ausgabe des Leuchtkraft-und Alpha Effekts, der über einer weißen Oberfläche zusammengesetzt wird, um Deckkraft anzuzeigen.



| Vorher                                                            |
|-------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)        |
| Nach                                                             |
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



Durch diesen Effekt wird der Alphakanal der Ausgabe mit dieser Farbmatrix auf die Leuchtkraft des Eingabe Bilds festgelegt.

![die Farbmatrix, die der Effekt zum Festlegen des Alphakanals verwendet.](images/luminance-to-alpha-math1.png)

Diese Auswirkung verarbeitet und gibt vorab multiplizierte Alpha Bilder aus. Der Effekt funktioniert nicht bei geraden Alpha Bildern, es sei denn, Sie sind vollständig undurchsichtig.

> [!Note]
>
> Da Bilder in einem Gamma kompensierten Format gespeichert werden, sollten Sie vor dem Berechnen der Leuchtkraft für ein Bild zuerst eine umgekehrte Gammakorrektur durchführen, um die tatsächlichen Farbwerte für das Bild zu erhalten. Da Images normalerweise in 2,2 Gamma gespeichert werden, können Sie den Gamma-Übertragungs Effekt mit einem Exponenten von (1/2.2) verwenden und dann die Ausgabe dieses Effekts verwenden.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Header                   | d2d1effects. h                                                                      |
| Bibliothek                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Die Ausgabe entspricht der Größe des Eingabe Bilds.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
