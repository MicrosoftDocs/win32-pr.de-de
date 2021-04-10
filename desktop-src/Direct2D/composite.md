---
title: Zusammengesetzter Effekt
description: Verwenden Sie den zusammengesetzten Effekt, um zwei oder mehr Bilder zu kombinieren. Dieser Effekt hat 13 verschiedene zusammengesetzte Modi.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- zusammengesetzter Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9872a66d031e8307f911ec7270af81397a80276
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956616"
---
# <a name="composite-effect"></a>Zusammengesetzter Effekt

Verwenden Sie den zusammengesetzten Effekt, um zwei oder mehr Bilder zu kombinieren. Dieser Effekt hat 13 verschiedene zusammengesetzte Modi. T

Der zusammengesetzte Effekt akzeptiert mindestens zwei Eingaben. Wenn Sie 2 Bilder angeben, ist Destination die erste Eingabe (Index 0), und die Quelle ist die zweite Eingabe (Index 1). Wenn Sie mehr als 2 Eingaben angeben, werden die Bilder zusammengesetzt, beginnend mit der ersten Eingabe und der zweiten, usw.

Dieser Effekt implementiert alle Modi mit der Mischungs Einheit der Grafikverarbeitungseinheit (Graphics Processing Unit, GPU).

Die CLSID für diesen Effekt ist CLSID \_ D2D1Composite.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Modustypen](#mode-types)
-   [Beispielcode](#sample-code)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das Bild hier zeigt zwei abgerundete Rechtecke mit der gleichen Größe, die sich überlappen. Das blaue Rechteck ist die Quelle, und das rote Rechteck ist das Ziel. Die Bilder wurden mit dem Quell-über-Modus zusammengesetzt.

![ein Beispiel Bild, das zwei abgerundete Rechtecke mit der gleichen Größe anzeigt, die sich über die Quelle über den Modus überlappen.](images/composite-over.png)

Im folgenden finden Sie ein weiteres Beispiel für die Verwendung des Standardmodus.



| Vor Bild 1                                                          |
|-------------------------------------------------------------------------|
| ![das erste Quell Bild vor dem Effekt.](images/default-before.jpg) |
| Vor Abbildung 2                                                          |
| ![Das zweite Bild vor dem Effekt.](images/3-composite(2of2).png)    |
| Nach                                                                   |
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



## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                     | Typ und Standardwert                                                          | BESCHREIBUNG                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| Mode<br/> D2D1- \_ Verbund- \_ Prop- \_ Modus<br/> | D2D1- \_ Verbund \_ Modus<br/> D2D1-Quelle für den zusammen \_ gesetzten \_ Modus \_ \_<br/> | Der für den Effekt verwendete Modus. |



 

## <a name="mode-types"></a>Modustypen

In der hier aufgeführten Tabelle werden die Modi dieses Effekts angezeigt. Die in der Tabelle aufgeführten Gleichungen verwenden die folgenden Elemente:

-   O = Ausgabe
-   S = Quelle
-   Sa = quellalpha
-   D = Ziel
-   Da = zielalpha



| Enumeration                                  | Gleichung                          | Größe der Ausgabe Bitmap                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| D2D1-Quelle für den zusammen \_ gesetzten \_ Modus \_ \_          | O = S + (1 SA) \* D             | Union von Quell-und Ziel Bitmaps                                                                 |
| D2D1 \_ - \_ \_ Ziel im Verbund Modus \_ über     | O = (1 da) \* S + D             | Union von Quell-und Ziel Bitmaps                                                                 |
| D2D1 \_ \_ Quelle im zusammengesetzten Modus \_ \_ in            | O = da \* S                       | Schnittmenge von Quell-und Ziel Bitmaps                                                          |
| D2D1 \_ - \_ \_ Ziel im Verbund Modus \_ in       | O = SA \* D                       | Schnittmenge von Quell-und Ziel Bitmaps                                                          |
| D2D1-Quelle für zusammen \_ gesetzten \_ Modus \_ \_           | O = (1-da) \* S                 | Der Bereich der Quell Bitmap.                                                                             |
| D2D1-Ziel für den zusammen \_ gesetzten \_ Modus \_ \_      | O = (1-SA) \* D                 | Der Bereich der Ziel Bitmap.                                                                        |
| D2D1-Quelle im zusammen \_ gesetzten \_ Modus \_ \_          | O = da \* S + (1-SA) \* D       | Der Bereich der Ziel Bitmap.                                                                        |
| D2D1-Ziel für den \_ Verbund \_ Modus oberhalb \_ \_     | O = (1-da) \* S + SA \* D       | Der Bereich der Quell Bitmap.                                                                             |
| D2D1 im zusammen \_ gesetzten \_ Modus- \_ Xor                   | O = (1-da) \* S + (1-SA) \* D | Union von Quell-und Ziel Bitmaps                                                                 |
| D2D1 \_ Composite- \_ Modus \_ Plus                  | O = S + D                         | Union von Quell-und Ziel Bitmaps                                                                 |
| D2D1 \_ - \_ \_ Quell \_ Kopie im zusammengesetzten Modus          | O = S                             | Der Bereich der Quell Bitmap.                                                                             |
| D2D1 \_ \_ \_ gebundene \_ Quell \_ Kopie im zusammengesetzten Modus | O = S (nur, wenn Quelle vorhanden ist)  | Union von Quell-und Ziel Bitmaps. Das Ziel wird nicht überschrieben, wenn die Quelle nicht vorhanden ist. |
| D2D1-Maske im zusammen \_ gesetzten \_ Modus \_ \_ umkehren          | O = (1 D) \* S + (1 SA) \* D  | Union von Quell-und Ziel Bitmaps. Die Alpha Werte sind unverändert.                                 |



 

Die Abbildung zeigt ein Beispiel für jeden der Modi mit Bildern mit einer Deckkraft von 1,0 oder 0,5.

![ein Beispiel Bild für jeden Modus, bei dem die Deckkraft auf 1,0 oder 0,5 festgelegt ist.](images/composite-types.png)

## <a name="sample-code"></a>Beispielcode

Um ein Beispiel für diesen Effekt zu erhalten, laden Sie das [Beispiel Direct2D Composite Effect Modes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample)herunter.

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

 

