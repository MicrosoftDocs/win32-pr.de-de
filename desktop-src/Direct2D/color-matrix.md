---
title: Farbmatrix Effekt
description: Verwenden Sie den Farbmatrix Effekt, um die RGBA-Werte einer Bitmap zu ändern.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- Farbmatrix Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1078b1858bc68396546e1036c717e01acb1069c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040484"
---
# <a name="color-matrix-effect"></a>Farbmatrix Effekt

Verwenden Sie den Farbmatrix Effekt, um die RGBA-Werte einer Bitmap zu ändern.

Sie können diesen Effekt für Folgendes verwenden:

-   Entfernen eines Farbkanals aus einem Bild.
-   Reduzieren Sie die Farbe in einem Bild.
-   Farbkanäle austauschen.
-   Farbkanäle kombinieren.

Viele integrierte Effekte sind Spezialisierungs Farben von Farb Matrizen, die für die beabsichtigte Verwendung der Effekte optimiert sind. Beispiele hierfür sind [Sättigung](saturation.md), [Farbton Drehung](hue-rotate.md),- [Pia](sepia-effect.md)und [Temperatur und Tönungs](temperature-and-tint-effect.md).

Die CLSID für diesen Effekt ist CLSID \_ D2D1ColorMatrix.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Alpha-Modi](#alpha-modes)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das Beispiel zeigt die Eingabe-und Ausgabe Bilder des Farbmatrix Effekts, der die roten und blauen Kanäle vertauscht.



| Vorher                                                       |
|--------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)   |
| Nach                                                        |
| ![das Bild nach der Transformation.](images/15-colormatrix.png) |



 


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect);

colorMatrixEffect->SetInput(0, bitmap);
D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



Dieser Effekt multipliziert die RGBA-Werte des Bilds mit einer 5 x 4-Spalten hauptmatrix, wie in dieser Gleichung gezeigt.

![eine Beispiel Matrix Definition.](images/color-matrix-formula.png)

Dieser Effekt kann bei geraden und vorab multiplizierten Alpha Bildern verwendet werden.

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ColorMatrix<br/> D2D1 \_ ColorMatrix \_ - \_ Farb \_ Matrix<br/> | Eine 5X4-Matrix von float-Werten. Die Elemente in der Matrix sind nicht gebunden und sind unitless.<br/> Der Standardwert ist die Identitätsmatrix.<br/> Der Typ ist D2D1 \_ Matrix \_ 5X4 \_ F.<br/> Der Standardwert ist Matrix5x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0). <br/>                                                                                                                                                                                                                        |
| Alpha AMODE<br/> D2D1 \_ ColorMatrix- \_ Prop- \_ alpha- \_ Modus<br/>     | Der Alpha-Modus der Ausgabe. Weitere Informationen finden Sie unter [Alpha-Modi](#alpha-modes) . <br/> Der Typ ist der D2D1 \_ ColorMatrix \_ alpha- \_ Modus.<br/> Der Standardwert ist "D2D1 \_ ColorMatrix \_ Alpha Mode" ( \_ \_ vorab multipliziert).<br/>                                                                                                                                                                                                                                                                                                    |
| Klamme Ausgabe<br/> D2D1 \_ ColorMatrix- \_ Prop- \_ Klemm \_ Ausgabe<br/> | Gibt an, ob der Effekt Farbwerte auf zwischen 0 und 1 zeigt, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt. Der Effekt bindet die Werte, bevor die Alpha-angezeigt werden.<br/> Wenn Sie diese Einstellung auf "true" festlegen, werden die Werte durch die Auswirkung fixiert. Wenn Sie diese Einstellung auf "false" festlegen, werden die Farbwerte durch die Auswirkung nicht fixiert, aber andere Effekte und die Ausgabe Oberfläche können die Werte einspannen, wenn Sie nicht über eine hohe Genauigkeit verfügen.<br/> Der Typ ist "bool".<br/> Der Standardwert ist FALSE.<br/> |



 

## <a name="alpha-modes"></a>Alpha-Modi



| Name                                          | BESCHREIBUNG                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| D2D1 \_ ColorMatrix- \_ alpha \_ Modus ist \_ vorab multipliziert | Der Effekt bewirkt, dass die Eingabe nicht vorab multipliziert wird, wendet die Farbmatrix an und führt die Ausgabe vorab aus.<br/> |
| D2D1 \_ ColorMatrix- \_ alpha \_ Modus \_ direkt      | Der Effekt wendet die Farbmatrix direkt auf die Eingabe an und führt keine vorab Multiplikation der Ausgabe aus.<br/> |



 

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

 

