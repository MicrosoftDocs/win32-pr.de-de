---
title: 2D-affiner Transformationseffekt
description: Der 2D-affine Transformations Effekt wendet eine räumliche Transformation auf ein Bild an, das auf einer 3x2-Matrix basiert, indem die Direct2D-Matrix Transformation und alle sechs Interpolations Modi verwendet werden.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- 2D-affiner Transformationseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3017992d34cd98095f01192ea948684a6b52e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106563"
---
# <a name="2d-affine-transform-effect"></a>2D-affiner Transformationseffekt

Der 2D-affine Transformations Effekt wendet eine räumliche Transformation auf ein Bild an, das auf einer 3x2-Matrix basiert, indem die Direct2D-Matrix [Transformation](direct2d-transforms-overview.md) und alle sechs Interpolations Modi verwendet werden. Mit diesem Effekt können Sie ein Bild drehen, skalieren, neigen oder übersetzen. Sie können diese Vorgänge auch kombinieren. Affine-Übertragungen behalten parallele Zeilen und das Verhältnis von Entfernungen zwischen drei Punkten eines Bilds bei.

Die CLSID für diesen Effekt ist CLSID \_ D2D12DAffineTransform.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Rahmen Modi](#border-modes)
-   [Interpolations Modi](#interpolation-modes)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                             |
|--------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)         |
| Nach                                                              |
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



Dieser Vorgang führt diesen Matrix Vorgang aus:

![affine Matrix Vorgang](images/affine-matrix-calculation.png)

Obwohl die Eingabe Matrix als 3 x 2-Matrix definiert ist, wird die letzte Spalte mit 0, 0 und 1 aufgefüllt, um eine quadratische Matrix zu bilden. Dies ermöglicht die Matrix Multiplikation, sodass Transformationen in eine einzelne Matrix verkettet werden können.

## <a name="effect-properties"></a>Effekt Eigenschaften



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Anzeige Name und indexenumeration</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>InterpolationMode<br/> D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE<br/></td>
<td>Der Interpolations Modus, der zum Skalieren des Bilds verwendet wird. Es gibt sechs Skalierungs Modi mit hoher Qualität und Geschwindigkeit.<br/> Der Typ ist D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.<br/> Der Standardwert ist D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
<tr class="even">
<td>Bordermode<br/> D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE<br/></td>
<td>Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart. Weitere Informationen finden Sie unter <a href="https://www.bing.com/search?q=Border+modes">Border Modes</a> . <br/> Der Typ ist D2D1_BORDER_MODE.<br/> Der Standardwert ist D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="odd">
<td>TransformMatrix<br/> D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX<br/></td>
<td>Die 3 x 2-Matrix zum Transformieren des Bilds mithilfe der Direct2D Matrix <a href="direct2d-transforms-overview.md">Transformation</a>. <br/> Der Typ ist D2D1_MATRIX_3X2_F.<br/> Der Standardwert ist Matrix3x2F:: Identity ().<br/></td>
</tr>
<tr class="even">
<td>Schärfe<br/> D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS<br/></td>
<td>Im hochwertigen kubischen Interpolations Modus ist die Schärfe des Skalierungs Filters ein Gleit Komma Wert zwischen 0 und 1. Die Werte sind unitless. Mit der Schärfe können Sie die Qualität eines Bilds anpassen, wenn Sie das Bild skalieren.<br/> Der Schärfe Faktor wirkt sich auf die Form des Kernels aus. Je höher der Schärfe Faktor, desto kleiner der Kernel. <br/>
<blockquote>
[!Note]<br />
Diese Eigenschaft wirkt sich nur auf den hochwertigen kubischen Interpolations Modus aus.
</blockquote>
<br/> Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="border-modes"></a>Rahmen Modi



| Name                     | BESCHREIBUNG                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ Border \_ Mode \_ Soft | Der Effekt füllt das Bild mit transparenten schwarzen Pixeln, während es interpoliert, was zu einem weichen Rand führt.<br/> |
| D2D1 \_ Rahmen \_ Modus \_ hart | Der Effekt bindet die Ausgabe an die Größe des Eingabe Bilds. <br/>                                         |



 

## <a name="interpolation-modes"></a>Interpolations Modi



| Enumeration                                                         | Beschreibung                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 2daffinetransform- \_ Interpolations \_ Modus \_ Nächster \_ Nachbar     | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.                                                                           |
| D2D1 \_ 2daffinetransform- \_ Interpolations \_ Modus \_ linear                | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. Dieser Modus verwendet mehr Verarbeitungszeit als der nächstgelegene Nachbar Modus, gibt aber ein Image mit höherer Qualität aus.                                           |
| D2D1 \_ 2daffinetransform- \_ Interpolations \_ Modus ( \_ kubisch)                 | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.                                                                        |
| D2D1 \_ 2daffinetransform \_ Interpolations \_ Modus \_ \_ Multisample \_ linear | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing. Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ 2daffinetransform- \_ Interpolations \_ Modus \_ anisotrope           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.                                                                                                     |
| D2D1 \_ 2daffinetransform \_ Interpolations \_ Modus \_ High \_ Quality \_ kubisch  | Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1 \_ 2daffinetransform- \_ Interpolations \_ Modus \_ linear.

 

> [!Note]  
> Der anisotrope-Modus generiert bei der Skalierung Mipmaps. Wenn Sie jedoch die **zwischengespeicherte** Eigenschaft für die Effekte, die für diesen Effekt eingegeben werden, auf true festlegen, werden die Mipmaps bei ausreichend kleinen Bildern nicht jedes Mal generiert.

 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Die Größe der Ausgabe Bitmap hängt von der Transformationsmatrix ab, die auf das Bild angewendet wird.

Der Effekt führt den Transformations Vorgang aus und wendet dann ein Begrenzungs Rahmen um das Ergebnis an. Die Ausgabe Bitmap ist die Größe des umgebenden Felds.

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

 

