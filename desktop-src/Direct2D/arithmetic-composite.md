---
title: Arithmetischer zusammengesetzter Effekt
description: Verwenden Sie die arithmetischen zusammengesetzten Effekte, um 2 Bilder mit einer gewichteten Summe von Pixeln aus den Eingabe Bildern zu kombinieren.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- arithmetischer zusammengesetzter Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c235ecb024c6b9e7adbce31c9f0cd65bc36cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956938"
---
# <a name="arithmetic-composite-effect"></a>Arithmetischer zusammengesetzter Effekt

Verwenden Sie die arithmetischen zusammengesetzten Effekte, um 2 Bilder mit einer gewichteten Summe von Pixeln aus den Eingabe Bildern zu kombinieren.

Die CLSID für diesen Effekt ist CLSID \_ D2D1ArithmeticComposite.

-   [Formel](#formula)
-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="formula"></a>Formel

Die hier verwendete Formel wird verwendet, um diesen Effekt zu berechnen.

Ausgabe<sub>RGBA</sub> = C1 \* Quelle<sub>RGBA</sub> \* Ziel<sub>RGBA</sub> + C2 \* Quelle<sub>RGBA</sub> + C3 \* Ziel<sub>RGBA</sub> + C4

Dabei sind C1, C2, C3, C4 Koeffizienten, die Sie festgelegt haben.

Die Koeffizienten entsprechen den Werten in einem D2D1 \_ Vector \_ 4f (x, y, z, w):

-   x = C1
-   j = C2
-   z = C3
-   w = C4

## <a name="example-image"></a>Beispielbild

Ein einfaches Beispiel besteht darin, die Quell-und Ziel Pixel hinzuzufügen. Im Beispiel werden zwei abgerundete Rechtecke zusammengeführt. Das Quell Rechteck ist blau, und das Ziel ist rot.

Das folgende Bild zeigt die Ausgabe des zusammengesetzten arithmetischen Effekts mit den Koeffizienten der Gleichung, die auf die hier aufgeführten Werte festgelegt sind.

-   C1 = 0
-   C2 = 1
-   C3 = 1
-   C4 = 0

![ein Beispiel Bild, das zwei abgerundete Rechtecke der gleichen Größe anzeigt, die sich mithilfe des arithmetischen zusammengesetzten Effekts überlappen.](images/arithmetic-50-percent.png)

Das Ergebnis ist, dass die Pixelwerte für Quelle und Ziel hinzugefügt werden. Die Bereiche, in denen sich die Rechtecke nicht überlappen, sind alle 0. Wenn sich die Rechtecke überlappen, ist der Wert Magenta, da R-und B-Werte beide den Höchstwert haben.

Im folgenden finden Sie ein weiteres Beispiel Bild mit Code.



| Vor Bild 1                                                             |
|----------------------------------------------------------------------------|
| ![das erste Quell Bild vor dem Effekt.](images/default-before.jpg)    |
| Vor Abbildung 2                                                             |
| ![Das zweite Bild vor dem Effekt.](images/4-arthimetic-composite2.jpg) |
| Nach                                                                      |
| ![das Bild nach der Transformation.](images/4-arithmeticcomposite.png)        |



 


```C++
ComPtr<ID2D1Effect> arithmeticCompositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &arithmeticCompositeEffect);

arithmeticCompositeEffect->SetInput(0, bitmap);
arithmeticCompositeEffect->SetInput(1, bitmapTwo);
arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, D2D1::Vector4F(0.0f, 0.5f, 0.5f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(arithmeticCompositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Koeffizienten<br/> D2D1 \_ arithmeticcomposite- \_ Prop \_ -Koeffizienten<br/> | Die Koeffizienten für die Gleichung, die verwendet werden, um die beiden Eingabe Bilder zusammenzusetzen. Die Koeffizienten sind unitless und unbegrenzt. Typ: D2D1 \_ Vector \_ 4f<br/> Der Standardwert ist {1.0 f, 0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                                                                 |
| Klamme Ausgabe<br/> D2D1 \_ arithmeticcomposite- \_ Prop- \_ Klammer \_ Ausgabe<br/> | Der Effekt klemmt Farbwerte auf zwischen 0 und 1, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt. <br/> Wenn Sie diese Einstellung auf "true" festlegen, werden die Werte durch die Auswirkung fixiert. Wenn Sie diese Einstellung auf "false" festlegen, werden die Farbwerte durch die Auswirkung nicht fixiert, aber andere Effekte und die Ausgabe Oberfläche können die Werte einspannen, wenn Sie nicht über eine hohe Genauigkeit verfügen.<br/> Der Typ ist "bool".<br/> Der Standardwert ist false.<br/> |



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Die Ausgabe Bitmap hängt von den Koeffizienten-Werten ab. Dies sind die möglichen Ausgabe Bitmapgrößen.

-   Wenn C1 der einzige Koeffizient ungleich NULL ist, ist die Ausgabegröße die Schnittmenge der Eingabe Rechtecke.
-   Wenn C2 der einzige Koeffizient ungleich NULL ist, entspricht die Ausgabegröße der Größe des Quell Rechtecks.
-   Wenn C3 der einzige Koeffizient ungleich NULL ist, entspricht die Ausgabegröße der Größe des Ziel Rechtecks.
-   Wenn alle Koeffizienten NULL sind, ist die Ausgabegröße ein leeres Rechteck.
-   Für alle anderen Koeffizienten-Werte ist die Ausgabegröße die Vereinigung der Eingabe Rechtecke.

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

 

