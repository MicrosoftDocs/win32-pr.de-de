---
title: Arithmetischer zusammengesetzter Effekt
description: Verwenden Sie den arithmetischen zusammengesetzten Effekt, um zwei Bilder mit einer gewichteten Summe von Pixeln aus den Eingabebildern zu kombinieren.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- Arithmetischer zusammengesetzter Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45976d577299bda7dfcef9bf20eff4980cc67ac105cb14fa793065d7ce1857f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641963"
---
# <a name="arithmetic-composite-effect"></a>Arithmetischer zusammengesetzter Effekt

Verwenden Sie den arithmetischen zusammengesetzten Effekt, um zwei Bilder mit einer gewichteten Summe von Pixeln aus den Eingabebildern zu kombinieren.

Die CLSID für diesen Effekt ist CLSID \_ D2D1ArithmeticComposite.

-   [Formel](#formula)
-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Ausgabebitmap](#output-bitmap)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="formula"></a>Formel

Die formel hier wird verwendet, um diesen Effekt zu berechnen.

Ausgabe<sub>rgba</sub> = C1 \* Quelle<sub>rgba</sub> \* Ziel<sub>rgba</sub> + C2 \* Quelle<sub>rgba</sub> + C3 \* Ziel<sub>rgba</sub> + C4

Wobei C1, C2, C3, C4 Koeffizienten sind, die Sie festlegen.

Die Koeffizienten werden den Werten in einem D2D1 \_ VECTOR \_ 4F (x, y, z, w) zugeordnet:

-   x = C1
-   y = C2
-   z = C3
-   w = C4

## <a name="example-image"></a>Beispielbild

Ein einfaches Beispiel ist das Hinzufügen der Quell- und Zielpixel. Im Beispiel werden zwei abgerundete Rechtecke zusammengesetzt. Das Quellrechteck ist blau und das Ziel rot.

Die Abbildung hier ist die Ausgabe des Arithmetischen Zusammengesetzt-Effekts mit den Koeffizienten der Gleichung, die hier auf die Werte festgelegt sind.

-   C1 = 0
-   C2 = 1
-   C3 = 1
-   C4 = 0

![Ein Beispielbild, das zwei abgerundete Rechtecke der gleichen Größe zeigt, die sich mithilfe des arithmetischen zusammengesetzten Effekts überlappen.](images/arithmetic-50-percent.png)

Das Ergebnis ist, dass die Pixelwerte für die Quelle und das Ziel hinzugefügt werden. Die Bereiche, in denen sich die Rechtecke nicht mit den RGBA-Werten überschneiden, sind alle 0. Wenn die Rechtecke die Farbe überlappen, ist magenta, da die R- und B-Werte maximal sind.

Hier sehen Sie ein weiteres Beispielbild mit Code.



| Vor Abbildung 1                                                             |
|----------------------------------------------------------------------------|
| ![das erste Quellbild vor dem Effekt.](images/default-before.jpg)    |
| Vor Abbildung 2                                                             |
| ![das zweite Bild vor dem Effekt.](images/4-arthimetic-composite2.jpg) |
| Danach                                                                      |
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



## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                               | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Koeffizienten<br/> D2D1 \_ ARITHMETICCOMPOSITE \_ PROP \_ COEFFICIENTS<br/> | Die Koeffizienten für die Gleichung, die zum Zusammengesetzten der beiden Eingabebilder verwendet wird. Die Koeffizienten sind einheitenlos und ungebunden. Typ: D2D1 \_ VECTOR \_ 4F.<br/> Der Standardwert ist {1.0f, 0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                                                                 |
| ClampOutput<br/> AUSGABE DER \_ D2D1-ARITHMETICCOMPOSITE-PROP-KLAMMER \_ \_ \_<br/> | Der Effekt bindet Farbwerte auf zwischen 0 und 1, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt. <br/> Wenn Sie diese Einstellung auf TRUE festlegen, werden die Werte durch den Effekt klammern. Wenn Sie diese Einstellung auf FALSE festlegen, bindet der Effekt die Farbwerte nicht, aber andere Effekte und die Ausgabeoberfläche können die Werte klammern, wenn sie nicht hoch genug präzise sind.<br/> Typ: BOOL<br/> Der Standardwert ist FALSE.<br/> |



 

## <a name="output-bitmap"></a>Ausgabebitmap

Die Ausgabebitmap hängt von den Koeffizientenwerten ab. Dies sind die möglichen Ausgabebitmapgrößen.

-   Wenn C1 der einzige Koeffizienten ungleich 0 (null) ist, ist die Ausgabegröße die Schnittmenge der Eingaberechtecke.
-   Wenn C2 der einzige Koeffizienten ungleich 0 (null) ist, entspricht die Ausgabegröße der Größe des Quellrechtecks.
-   Wenn C3 der einzige Koeffizienten ungleich 0 (null) ist, entspricht die Ausgabegröße der Größe des Zielrechtecks.
-   Wenn alle Koeffizienten null sind, ist die Ausgabegröße ein leeres Rechteck.
-   Für alle anderen Koeffizientenwerte ist die Ausgabegröße die Vereinigung der Eingaberechtecke.

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

 

