---
title: Rahmen-Effekt
description: Verwenden Sie den Rahmeneffekt, um ein Bild von den Rändern zu erweitern.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- Border-Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce125a96730ee59f63b18cfd1a08abd2432af6f3fdc6b5f06cfc2e9272a7a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928996"
---
# <a name="border-effect"></a>Rahmen-Effekt

Verwenden Sie den Rahmeneffekt, um ein Bild von den Rändern zu erweitern. Mit diesem Effekt können Sie die Pixel von den Rändern des Bilds wiederholen, die Pixel vom gegenüberliegenden Ende des Bilds umschließen oder die Pixel über den Bitmap-Rahmen spiegeln, um den Bitmapbereich zu erweitern.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Border.

## <a name="example-images"></a>Beispielbilder

Die Beispiele hier zeigen die Ausgabe des Rahmeneffekts mit jedem Modus. Die Ausgabegröße ist unendlich, aber diese Beispielbilder werden auf das Doppelte der Größe zugeschnitten.

### <a name="mirror"></a>Spiegel



| Vorher                                                    |
|-----------------------------------------------------------|
| ![Screenshot, der das Bild vor dem Effekt zeigt.](images/border-before.jpg) |
| Danach                                                     |
| ![Screenshot, der das Bild nach der Transformation zeigt.](images/10-border.png)   |



 

### <a name="clamp"></a>Clamp



| Vorher                                                        |
|---------------------------------------------------------------|
| ![Screenshot, der das Bild vor dem Effekt für eine Klammer zeigt.](images/border-before.jpg)     |
| Danach                                                         |
| ![Screenshot, der das Bild nach der Transformation für eine Klammer zeigt.](images/10-border-clamp.png) |



 

### <a name="wrap"></a>Umschließen



| Vorher                                                       |
|--------------------------------------------------------------|
| ![Screenshot, der das Bild vor dem Effekt für einen Wrap zeigt.](images/border-before.jpg)    |
| Danach                                                        |
| ![Screenshot, der das Bild nach der Transformation für einen Wrap zeigt.](images/10-border-wrap.png) |



 


```C++
ComPtr<ID2D1Effect> borderEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Border, &borderEffect);

borderEffect->SetInput(0, bitmap);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_EDGE_MODE_MIRROR);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_Y, D2D1_BORDER_EDGE_MODE_MIRROR);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(borderEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                  | BESCHREIBUNG                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Edgemodus X<br/> D2D1 \_ BORDER \_ PROP \_ EDGE \_ MODE \_ X<br/> | Der Edgemodus in X-Richtung für den Effekt. Sie können dies auf "Klammern", "Umschließen" oder "Spiegel" festlegen. Weitere Informationen finden Sie unter [Edgemodi.](#edge-modes)<br/> Der Typ ist "D2D1 \_ BORDER \_ EDGE \_ MODE".<br/> Der Standardwert ist D2D1 \_ BORDER \_ EDGE MODE \_ \_ CLAMP.<br/> |
| Edgemodus Y<br/> D2D1 \_ BORDER \_ PROP \_ EDGE \_ MODE \_ Y<br/> | Der Edgemodus in Y-Richtung für den Effekt. Sie können dies auf "Klammern", "Umschließen" oder "Spiegel" festlegen. Weitere Informationen finden Sie unter [Edgemodi.](#edge-modes)<br/> Der Typ ist "D2D1 \_ BORDER \_ EDGE \_ MODE".<br/> Der Standardwert ist D2D1 \_ BORDER \_ EDGE MODE \_ \_ CLAMP.<br/> |



 

## <a name="edge-modes"></a>Edgemodi



| Anzeigename und Indexenumeration                            | BESCHREIBUNG                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| Clamp<br/> D2D1 \_ BORDER \_ EDGE \_ MODE \_ CLAMP<br/>   | Wiederholt die Pixel von den Rändern des Bilds.      |
| Umschließen<br/> D2D1 \_ BORDER \_ EDGE \_ MODE \_ WRAP<br/>     | Verwendet Pixel vom gegenüberliegenden Endrand des Bilds. |
| Spiegel<br/> D2D1 \_ BORDER \_ EDGE \_ MODE \_ MIRROR<br/> | Spiegelt Pixel über den Rand des Bilds wider.         |



 

## <a name="output-bitmap"></a>Ausgabebitmap

Die Ausgabebitmapgröße ist für alle Eingaben unendlich, mit Ausnahme eines Eingabebilds mit einer Größe von 0. Wenn die Höhe oder Breite eines Eingabebilds 0 beträgt, beträgt die Ausgabegröße 0.

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

 

