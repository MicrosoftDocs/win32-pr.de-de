---
title: Zusammengesetzter Effekt
description: Verwenden Sie den zusammengesetzten Effekt, um 2 oder mehr Bilder zu kombinieren. Dieser Effekt hat 13 verschiedene zusammengesetzte Modi.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- Zusammengesetzter Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8cf326e5d0bfb33b3dc927ba7366eb6d2b343a1a50db462de58fac8ef648bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826590"
---
# <a name="composite-effect"></a>Zusammengesetzter Effekt

Verwenden Sie den zusammengesetzten Effekt, um 2 oder mehr Bilder zu kombinieren. Dieser Effekt hat 13 verschiedene zusammengesetzte Modi. T

Der zusammengesetzte Effekt akzeptiert 2 oder mehr Eingaben. Wenn Sie 2 Bilder angeben, ist das Ziel die erste Eingabe (Index 0), und die Quelle ist die zweite Eingabe (Index 1). Wenn Sie mehr als zwei Eingaben angeben, werden die Bilder beginnend mit der ersten Eingabe und der zweiten Eingabe zusammengesetzt.

Dieser Effekt implementiert alle Modi mithilfe der Mischungseinheit der Grafikprozessor (Graphics Processing Unit, GPU).

Die CLSID für diesen Effekt ist CLSID \_ D2D1Composite.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Modustypen](#mode-types)
-   [Beispielcode](#sample-code)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Die Abbildung zeigt zwei abgerundete Rechtecke derselben Größe, die sich überlappen. Das blaue Rechteck ist die Quelle, und das rote Rechteck ist das Ziel. Die Bilder wurden mit dem Source Over-Modus zusammengesetzt.

![Ein Beispielbild, das zwei abgerundete Rechtecke derselben Größe zeigt, die sich mithilfe des Quellmodus überlappen.](images/composite-over.png)

Hier ist ein weiteres Beispiel mit dem Standardmodus.



| Vor Abbildung 1                                                          |
|-------------------------------------------------------------------------|
| ![das erste Quellbild vor dem Effekt.](images/default-before.jpg) |
| Vor Abbildung 2                                                          |
| ![das zweite Bild vor dem Effekt.](images/3-composite(2of2).png)    |
| Danach                                                                   |
| ![das Bild nach der Transformation.](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                     | Typ und Standardwert                                                          | BESCHREIBUNG                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| Mode<br/> ZUSAMMENGESETZTER \_ \_ D2D1-PROP-MODUS \_<br/> | ZUSAMMENGESETZTER \_ D2D1-MODUS \_<br/> QUELLE IM ZUSAMMENGESETZTEN MODUS D2D1 \_ \_ \_ \_ ÜBER<br/> | Der für den Effekt verwendete Modus. |



 

## <a name="mode-types"></a>Modustypen

In der folgenden Tabelle sind die Modi dieses Effekts aufgeführt. Die in der Tabelle aufgeführten Gleichungen verwenden die folgenden Elemente:

-   O = Ausgabe
-   S = Quelle
-   SA = Quell alpha
-   D = Ziel
-   DA = Ziel alpha



| Enumeration                                  | Gleichung                          | Ausgabebitmapgröße                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| QUELLE IM ZUSAMMENGESETZTEN MODUS D2D1 \_ \_ \_ \_ ÜBER          | O = S + (1 SA) \* D             | Union von Quell- und Zielbitmaps                                                                 |
| ZIEL FÜR ZUSAMMENGESETZTEN D2D1-MODUS \_ \_ \_ \_ ÜBER     | O = (1 DA) \* S + D             | Union von Quell- und Zielbitmaps                                                                 |
| QUELLE FÜR ZUSAMMENGESETZTEN D2D1-MODUS \_ \_ \_ \_ IN            | O = DA \* S                       | Schnittmenge von Quell- und Zielbitmaps                                                          |
| ZIEL FÜR ZUSAMMENGESETZTEN D2D1-MODUS \_ \_ \_ \_ IN       | O = SA \* D                       | Schnittmenge von Quell- und Zielbitmaps                                                          |
| D2D1 \_ COMPOSITE \_ MODE \_ SOURCE \_ OUT           | O = (1 - DA) \* S                 | Bereich der Quellbitmap                                                                             |
| D2D1 \_ COMPOSITE \_ MODE \_ DESTINATION \_ OUT      | O = (1 – SA) \* D                 | Bereich der Zielbitmap                                                                        |
| D2D1 \_ COMPOSITE \_ MODE \_ SOURCE \_ ATOP          | O = DA \* S + (1 – SA) \* D       | Bereich der Zielbitmap                                                                        |
| D2D1 \_ COMPOSITE \_ MODE \_ DESTINATION \_ ATOP     | O = (1 - DA) \* S + SA \* D       | Bereich der Quellbitmap                                                                             |
| D2D1 \_ COMPOSITE \_ MODE \_ XOR                   | O = (1 - DA) \* S + (1 - SA) \* D | Union von Quell- und Zielbitmaps                                                                 |
| ZUSAMMENGESETZTER D2D1-MODUS \_ \_ \_ PLUS                  | O = S + D                         | Union von Quell- und Zielbitmaps                                                                 |
| QUELLKOPIE IM ZUSAMMENGESETZTEN MODUS D2D1 \_ \_ \_ \_          | O = S                             | Bereich der Quellbitmap                                                                             |
| D2D1 \_ COMPOSITE \_ MODE \_ BOUNDED \_ SOURCE \_ COPY | O = S (nur wenn die Quelle vorhanden ist)  | Union von Quell- und Zielbitmaps. Das Ziel wird nicht überschrieben, wenn die Quelle nicht vorhanden ist. |
| D2D1 \_ COMPOSITE \_ MODE \_ MASK \_ INVERT          | O = (1 D) \* S + (1 SA) \* D  | Union von Quell- und Zielbitmaps. Die Alphawerte bleiben unverändert.                                 |



 

Die Abbildung hier zeigt ein Beispiel für jeden Der Modi mit Bildern, die eine Deckkraft von 1,0 oder 0,5 haben.

![Ein Beispielbild der einzelnen Modi, bei dem die Deckkraft auf 1,0 oder 0,5 festgelegt ist.](images/composite-types.png)

## <a name="sample-code"></a>Beispielcode

Ein Beispiel für diesen Effekt finden Sie im [Beispiel für zusammengesetzte Direct2D-Effektmodi.](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample)

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

 

