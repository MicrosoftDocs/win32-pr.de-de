---
title: 2D-affiner Transformationseffekt
description: Der 2D-affine Transformationseffekt wendet eine räumliche Transformation auf ein Bild basierend auf einer 3X2-Matrix mithilfe der Direct2D-Matrixtransformation und einem von sechs Interpolationsmodi an.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- 2D-affiner Transformationseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 337168db7a422a8a22785316d2af1960e3a78b2f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478096"
---
# <a name="2d-affine-transform-effect"></a>2D-affiner Transformationseffekt

Der 2D-affine Transformationseffekt wendet eine räumliche Transformation auf ein Bild basierend [](direct2d-transforms-overview.md) auf einer 3X2-Matrix mithilfe der Direct2D-Matrixtransformation und einem von sechs Interpolationsmodi an. Sie können diesen Effekt verwenden, um ein Bild zu drehen, zu skalieren, zu verskalieren oder zu übersetzen. Sie können diese Vorgänge auch kombinieren. Affine Übertragungen behalten parallele Linien und das Verhältnis der Abstände zwischen drei beliebigen Punkten in einem Bild bei.

Die CLSID für diesen Effekt ist CLSID \_ D2D12DAffineTransform.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Rahmenmodi](#border-modes)
-   [Interpolationsmodi](#interpolation-modes)
-   [Ausgabebitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                             |
|--------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)         |
| Danach                                                              |
| ![das Bild nach der Transformation.](images/21-2daffinetransform.png) |



 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInput(0, bitmap);

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,   0.1f, 0.9f,   8.0f, 45.0f);

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



Dieser Effekt führt diesen Matrixvorgang aus:

![affine Matrixoperation](images/affine-matrix-calculation.png)

Obwohl die Eingabematrix als 3x2-Matrix definiert ist, wird die letzte Spalte mit 0, 0 und 1 aufschlossen, um eine quadratische Matrix zu erzeugen. Dies ermöglicht eine Matrixmultiplikation, sodass Transformationen zu einer einzelnen Matrix verkettet werden können.

## <a name="effect-properties"></a>Effect-Eigenschaften




| Anzeigename und Indexenumeration | BESCHREIBUNG | 
|------------------------------------|-------------|
| Interpolationmode<br /> D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE<br /> | Der Interpolationsmodus, der zum Skalieren des Bilds verwendet wird. Es gibt 6 Skalierungsmodi, die in Qualität und Geschwindigkeit reichen.<br /> Der Typ ist D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.<br /> Der Standardwert ist D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.<br /> | 
| BorderMode<br /> D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE<br /> | Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, soft oder hard. Weitere <a href="https://www.bing.com/search?q=Border+modes">Informationen finden Sie</a> unter Rahmenmodi. <br /> Typ ist D2D1_BORDER_MODE.<br /> Der Standardwert ist D2D1_BORDER_MODE_SOFT.<br /> | 
| TransformMatrix<br /> D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX<br /> | Die 3x2-Matrix zum Transformieren des <a href="direct2d-transforms-overview.md"></a>Bilds mithilfe der Direct2D-Matrixtransformation . <br /> Typ ist D2D1_MATRIX_3X2_F.<br /> Der Standardwert ist Matrix3x2F::Identity().<br /> | 
| Schärfe<br /> D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS<br /> | Im kubischen Interpolationsmodus mit hoher Qualität wird die Schärfe des Skalierungsfilters als Gleitkomma zwischen 0 und 1 angezeigt. Die Werte sind einheitslos. Sie können die Schärfe verwenden, um die Qualität eines Bilds anzupassen, wenn Sie das Bild skalieren.<br /> Der Schärfefaktor wirkt sich auf die Form des Kernels aus. Je höher der Schärfefaktor, desto kleiner der Kernel. <br /><blockquote>[!Note]<br />Diese Eigenschaft wirkt sich nur auf den kubischen Interpolationsmodus mit hoher Qualität aus.</blockquote><br /> Typ: FLOAT<br /> Der Standardwert ist 1,0f.<br /> | 




 

## <a name="border-modes"></a>Rahmenmodi



| Name                     | BESCHREIBUNG                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ BORDER \_ MODE \_ SOFT | Der Effekt auflagert das Bild bei der Interpolation mit transparenten schwarzen Pixeln, was zu einem weichen Rand führt.<br/> |
| D2D1– \_ \_ RAHMENMODUS \_ FEST | Der Effekt klammert die Ausgabe an die Größe des Eingabebilds. <br/>                                         |



 

## <a name="interpolation-modes"></a>Interpolationsmodi



| Enumeration                                                         | Beschreibung                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 2DAFFINETRANSFORM \_ \_ INTERPOLATIONSMODUS \_ NÄCHSTER \_ NACHBAR     | Stichprobenentnahme für den nächstgelegenen einzelnen Punkt und Verwendung dieses Punkts. Dieser Modus verbraucht weniger Verarbeitungszeit, gibt jedoch das Image mit der niedrigsten Qualität aus.                                                                           |
| D2D1 \_ 2DAFFINETRANSFORM \_ \_ INTERPOLATIONSMODUS \_ LINEAR                | Verwendet eine Stichprobe mit vier Punkt und eine lineare Interpolation. Dieser Modus verwendet mehr Verarbeitungszeit als der nächste Nachbarmodus, gibt jedoch ein Bild mit höherer Qualität aus.                                           |
| D2D1 \_ 2DAFFINETRANSFORM \_ \_ INTERPOLATIONSMODUS \_ KUBISCH                 | Verwendet einen kubischen 16-Beispielkernel für die Interpolation. Dieser Modus verwendet die meiste Verarbeitungszeit, gibt jedoch ein Image mit höherer Qualität aus.                                                                        |
| D2D1 \_ 2DAFFINETRANSFORM \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für ein gutes Edge-Antialiasing. Dieser Modus ist gut für das herunterskalieren um kleine Mengen auf Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ 2DAFFINETRANSFORM \_ \_ INTERPOLATIONSMODUS \_ ANISOTROP           | Verwendet die anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu beproben.                                                                                                     |
| D2D1 \_ 2DAFFINETRANSFORM \_ INTERPOLATION \_ MODE HIGH \_ \_ QUALITY \_ KUBISCH  | Verwendet einen kubischen Kernel mit hoher Qualität in variabler Größe, um ein Vorabskalieren des Images durchzuführen, wenn eine Downskalierung an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolationsmodus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf D2D1 \_ 2DAFFINETRANSFORM \_ INTERPOLATION \_ MODE LINEAR \_ festgelegt.

 

> [!Note]  
> Im anisotropen Modus werden bei der Skalierung Mipmaps generiert. Wenn Sie jedoch die **Cached-Eigenschaft** auf TRUE für die Effekte festlegen, die für diesen Effekt eingegeben werden, werden die Mipmaps nicht jedes Mal für ausreichend kleine Bilder generiert.

 

## <a name="output-bitmap"></a>Ausgabebitmap

Die Größe der Ausgabebitmap hängt von der Transformationsmatrix ab, die auf das Bild angewendet wird.

Der Effekt führt den Transformationsvorgang aus und wendet dann ein Begrenzungsfeld um das Ergebnis an. Die Ausgabebitmap ist die Größe des Begrenzungsfelds.

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

 

