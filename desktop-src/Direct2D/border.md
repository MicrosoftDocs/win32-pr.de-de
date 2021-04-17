---
title: Rahmen-Effekt
description: Verwenden Sie den Rahmen Effekt, um ein Bild von den Rändern zu erweitern.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- Rahmen Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fb43ae8b3e9c4eb449a8231f8b4ffcacf7658b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104530413"
---
# <a name="border-effect"></a>Rahmen-Effekt

Verwenden Sie den Rahmen Effekt, um ein Bild von den Rändern zu erweitern. Mit diesem Effekt können Sie die Pixel von den Rändern des Bilds wiederholen, die Pixel vom umgekehrten Ende des Bilds umschließen oder die Pixel über den bitmaprahmen hinweg spiegeln, um den Bitmapbereich zu erweitern.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Border.

## <a name="example-images"></a>Beispiel Bilder

In den Beispielen wird die Ausgabe des Rahmen Effekts mithilfe der einzelnen Modi veranschaulicht. Die Ausgabegröße ist unendlich, aber diese Beispiel Bilder werden auf die doppelte Größe zugeschnitten.

### <a name="mirror"></a>Spiegel



| Vorher                                                    |
|-----------------------------------------------------------|
| ![Screenshot, der das Bild vor dem Effekt zeigt.](images/border-before.jpg) |
| Nach                                                     |
| ![Screenshot, der das Bild nach der Transformation anzeigt.](images/10-border.png)   |



 

### <a name="clamp"></a>Clamp



| Vorher                                                        |
|---------------------------------------------------------------|
| ![Screenshot, der das Bild vor dem Effekt einer Klammer anzeigt.](images/border-before.jpg)     |
| Nach                                                         |
| ![Screenshot, der das Bild nach der Transformation für eine Klammer anzeigt.](images/10-border-clamp.png) |



 

### <a name="wrap"></a>Umschließen



| Vorher                                                       |
|--------------------------------------------------------------|
| ![Screenshot, der das Bild vor dem Effekt für einen Umbruch anzeigt.](images/border-before.jpg)    |
| Nach                                                        |
| ![Screenshot, der das Bild nach der Transformation für einen Umbruch anzeigt.](images/10-border-wrap.png) |



 


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



## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                  | BESCHREIBUNG                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Edgemodus X<br/> D2D1 \_ Border \_ Prop \_ Edge \_ Mode \_ X<br/> | Der edgemodus in der X-Richtung für den Effekt. Sie können diese Einstellung auf Klammer, Umbruch oder Spiegelung festlegen. Weitere Informationen finden Sie unter [Edge-Modi](#edge-modes) .<br/> Der Typ ist D2D1 \_ Border \_ Edge \_ Mode.<br/> Der Standardwert ist D2D1 \_ Border \_ Edge \_ Mode \_ Clamp.<br/> |
| Edgemodus Y<br/> D2D1 \_ Border \_ Prop \_ Edge \_ Mode \_ Y<br/> | Der edgemodus in der Y-Richtung für den Effekt. Sie können diese Einstellung auf Klammer, Umbruch oder Spiegelung festlegen. Weitere Informationen finden Sie unter [Edge-Modi](#edge-modes) .<br/> Der Typ ist D2D1 \_ Border \_ Edge \_ Mode.<br/> Der Standardwert ist D2D1 \_ Border \_ Edge \_ Mode \_ Clamp.<br/> |



 

## <a name="edge-modes"></a>Edge-Modi



| Anzeige Name und indexenumeration                            | BESCHREIBUNG                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| Clamp<br/> D2D1 \_ Border \_ Edge \_ Mode- \_ Klammer<br/>   | Wiederholt die Pixel von den Rändern des Bilds.      |
| Umschließen<br/> D2D1 \_ Border \_ Edge- \_ Modus \_ umschließen<br/>     | Verwendet Pixel vom gegenüberliegenden Endrand des Bilds. |
| Spiegel<br/> D2D1 \_ - \_ \_ randmodusspiegelung \_<br/> | Gibt Pixel über den Rand des Bilds wieder.         |



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Die Größe der Ausgabe Bitmap ist für alle Eingaben unbegrenzt, außer bei einem Eingabebild mit der Größe 0 (null). Wenn die Höhe oder die Breite eines Eingabe Bilds 0 beträgt, ist die Ausgabegröße 0.

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

 

