---
title: Farbmatrixeffekt
description: Verwenden Sie den Farbmatrixeffekt, um die RGBA-Werte einer Bitmap zu ändern.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- Farbmatrixeffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8bb461698e4f8b39eef3bed57fc21947f3cc1175c1bdf4f990629db87e1c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653304"
---
# <a name="color-matrix-effect"></a>Farbmatrixeffekt

Verwenden Sie den Farbmatrixeffekt, um die RGBA-Werte einer Bitmap zu ändern.

Sie können diesen Effekt verwenden, um:

-   Entfernen eines Farbkanals aus einem Bild.
-   Reduzieren sie die Farbe in einem Bild.
-   Tauschen Sie Farbkanäle aus.
-   Kombinieren sie Farbkanäle.

Viele integrierte Effekte sind Spezialisierungen der Farbmatrix, die für die beabsichtigte Verwendung der Effekte optimiert sind. Beispiele hierfür sind [Sättigung,](saturation.md) [Farbtonrotierung,](hue-rotate.md) [Sepia](sepia-effect.md)und [Temperatur und Tönung.](temperature-and-tint-effect.md)

Die CLSID für diesen Effekt ist CLSID \_ D2D1ColorMatrix.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Alphamodi](#alpha-modes)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das folgende Beispiel zeigt die Ein- und Ausgabebilder des Farbmatrixeffekts, der die roten und blauen Kanäle austauscht.



| Vorher                                                       |
|--------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)   |
| Danach                                                        |
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



Dieser Effekt multipliziert die RGBA-Werte des Bilds mit einer 5x4-Spaltenhauptmatrix, wie in dieser Gleichung dargestellt.

![eine Beispielmatrixdefinition.](images/color-matrix-formula.png)

Dieser Effekt funktioniert bei geraden und prämultiplizierten Alphabildern.

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Colormatrix<br/> D2D1 \_ COLORMATRIX \_ PROP \_ COLOR \_ MATRIX<br/> | Eine 5x4-Matrix von float-Werten. Die Elemente in der Matrix sind nicht begrenzt und unitlos.<br/> Der Standardwert ist die Identitätsmatrix.<br/> Der Typ ist D2D1 \_ MATRIX \_ 5X4 \_ F.<br/> Der Standardwert ist Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0). <br/>                                                                                                                                                                                                                        |
| AlphaMode<br/> D2D1 \_ COLORMATRIX \_ PROP \_ ALPHA \_ MODE<br/>     | Der Alphamodus der Ausgabe. Weitere Informationen finden Sie [unter Alphamodi.](#alpha-modes) <br/> Der Typ ist D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE.<br/> Der Standardwert ist D2D1 \_ COLORMATRIX \_ ALPHA MODE \_ \_ PREMULTIPLIED.<br/>                                                                                                                                                                                                                                                                                                    |
| ClampOutput<br/> D2D1 \_ COLORMATRIX \_ \_ PROP-KLAMMERAUSGABE \_<br/> | Gibt an, ob der Effekt Farbwerte zwischen 0 und 1 zusammenbindet, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt. Der Effekt klammert die Werte, bevor er das Alpha vormultipliziert.<br/> Wenn Sie diese Einstellung auf TRUE festlegen, werden die Werte durch den Effekt klammern. Wenn Sie diese Einstellung auf FALSE festlegen, bindet der Effekt die Farbwerte nicht, aber andere Effekte und die Ausgabeoberfläche können die Werte klammern, wenn sie nicht hoch genug präzise sind.<br/> Der Typ ist BOOL.<br/> Der Standardwert ist FALSE.<br/> |



 

## <a name="alpha-modes"></a>Alphamodi



| Name                                          | Beschreibung                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE \_ PREMULTIPLIED | Der Effekt entfällt die Prämultiplizierung der Eingabe, wendet die Farbmatrix an und multipliziert die Ausgabe.<br/> |
| D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE \_ STRAIGHT      | Der Effekt wendet die Farbmatrix direkt auf die Eingabe an und stellt die Ausgabe nicht vor.<br/> |



 

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

 

