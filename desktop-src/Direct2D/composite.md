---
title: Zusammengesetzter Effekt
description: Verwenden Sie den zusammengesetzten Effekt, um 2 oder mehr Bilder zu kombinieren. Dieser Effekt verfügt über 13 verschiedene zusammengesetzte Modi.
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

Verwenden Sie den zusammengesetzten Effekt, um 2 oder mehr Bilder zu kombinieren. Dieser Effekt verfügt über 13 verschiedene zusammengesetzte Modi. T

Der zusammengesetzte Effekt akzeptiert 2 oder mehr Eingaben. Wenn Sie zwei Bilder angeben, ist das Ziel die erste Eingabe (Index 0) und die Quelle die zweite Eingabe (Index 1). Wenn Sie mehr als zwei Eingaben angeben, werden die Bilder zusammengesetzt, beginnend mit der ersten Eingabe und der zweiten usw.

Dieser Effekt implementiert alle Modi mithilfe der Mischungseinheit der Grafikverarbeitungseinheit (GRAPHICS Processing Unit, GPU).

Die CLSID für diesen Effekt ist CLSID \_ D2D1Composite.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Modustypen](#mode-types)
-   [Beispielcode](#sample-code)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Die Abbildung hier zeigt zwei abgerundete Rechtecke derselben Größe, die sich überlappen. Das blaue Rechteck ist die Quelle, und das rote Rechteck ist das Ziel. Die Bilder wurden mit dem Modus Quellüberlauf zusammengesetzt.

![Ein Beispielbild, das zwei abgerundete Rechtecke der gleichen Größe zeigt, die sich mithilfe des Quellmodus überlappen.](images/composite-over.png)

Im Folgenden finden Sie ein weiteres Beispiel für die Verwendung des Standardmodus.



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
| Mode<br/> D2D1– \_ \_ ZUSAMMENGESETZTER \_ PROP-MODUS<br/> | ZUSAMMENGESETZTER \_ \_ D2D1-MODUS<br/> QUELLE DES \_ ZUSAMMENGESETZTEN D2D1-MODUS \_ \_ \_ ÜBER<br/> | Der für den Effekt verwendete Modus. |



 

## <a name="mode-types"></a>Modustypen

Die folgende Tabelle zeigt die Modi dieses Effekts. Die in der Tabelle aufgeführten Gleichungen verwenden die folgenden Elemente:

-   O = Ausgabe
-   S = Quelle
-   SA = Source Alpha
-   D = Ziel
-   DA = Ziel alpha



| Enumeration                                  | Gleichung                          | Ausgabebitmapgröße                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| QUELLE DES \_ ZUSAMMENGESETZTEN D2D1-MODUS \_ \_ \_ ÜBER          | O = S + (1 SA) \* D             | Union von Quell- und Zielbitmaps                                                                 |
| D2D1 \_ COMPOSITE MODE DESTINATION OVER \_ (D2D1-ZIEL IM ZUSAMMENGESETZTEN MODUS \_ \_ ÜBER)     | O = (1 DA) \* S + D             | Union von Quell- und Zielbitmaps                                                                 |
| QUELLE DES \_ ZUSAMMENGESETZTEN D2D1-MODUS \_ \_ \_ IN            | O = DA \* S                       | Schnittmenge von Quell- und Zielbitmaps                                                          |
| \_ \_ D2D1-ZIEL IM ZUSAMMENGESETZTEN MODUS \_ \_ IN       | O = SA \* D                       | Schnittmenge von Quell- und Zielbitmaps                                                          |
| QUELLE IM \_ ZUSAMMENGESETZTEN D2D1-MODUS \_ \_ \_ OUT           | O = (1 - DA) \* S                 | Bereich der Quellbitmap                                                                             |
| D2D1 \_ COMPOSITE \_ MODE \_ DESTINATION \_ OUT      | O = (1 - SA) \* D                 | Bereich der Zielbitmap                                                                        |
| QUELLE IM \_ ZUSAMMENGESETZTEN D2D1-MODUS \_ \_ \_ ATOP          | O = DA \* S + (1 - SA) \* D       | Bereich der Zielbitmap                                                                        |
| \_D2D1– \_ ZIEL IM ZUSAMMENGESETZTEN MODUS \_ \_ ATOP     | O = (1 - DA) \* S + SA \* D       | Bereich der Quellbitmap                                                                             |
| D2D1 \_ COMPOSITE \_ MODE \_ XOR                   | O = (1 - DA) \* S + (1 - SA) \* D | Union von Quell- und Zielbitmaps                                                                 |
| D2D1 \_ COMPOSITE \_ MODE \_ PLUS                  | O = S + D                         | Union von Quell- und Zielbitmaps                                                                 |
| QUELLKOPIE IM \_ ZUSAMMENGESETZTEN D2D1-MODUS \_ \_ \_          | O = S                             | Bereich der Quellbitmap                                                                             |
| D2D1– \_ ZUSAMMENGESETZTER \_ MODUS – \_ \_ BEGRENZUNGSQUELLKOPIE \_ | O = S (nur dort, wo die Quelle vorhanden ist)  | Union von Quell- und Zielbitmaps. Das Ziel wird nicht überschrieben, wenn die Quelle nicht vorhanden ist. |
| D2D1 \_ COMPOSITE \_ MODE \_ MASK \_ INVERT          | O = (1 D) \* S + (1 SA) \* D  | Union von Quell- und Zielbitmaps. Die Alphawerte sind unverändert.                                 |



 

Die folgende Abbildung zeigt ein Beispiel für jeden der Modi mit Bildern mit einer Deckkraft von 1,0 oder 0,5.

![Ein Beispielbild der einzelnen Modi mit Durchlässigkeit, die auf 1,0 oder 0,5 festgelegt ist.](images/composite-types.png)

## <a name="sample-code"></a>Beispielcode

Laden Sie für ein Beispiel für diesen Effekt das [Direct2D-Beispiel für zusammengesetzte Effektmodi](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample)herunter.

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

 

