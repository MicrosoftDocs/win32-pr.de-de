---
title: 3D-Transformationseffekt
description: Mit dem 3D-Transformations Effekt können Sie eine beliebige 4X4-Transformationsmatrix auf ein Bild anwenden.
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- 3D--Transformations Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104559862"
---
# <a name="3d-transform-effect"></a>3D-Transformationseffekt

Mit dem 3D-Transformations Effekt können Sie eine beliebige 4X4-Transformationsmatrix auf ein Bild anwenden.

Dieser Effekt wendet die von Ihnen bereitgestellte Matrix (M?) auf die eckscheitel Punkte des Quell Bilds ( \[ x y z 1) an, \] indem diese Berechnung verwendet wird:

\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \] = \[ x y z 1 \] \* M?

Die CLSID für diesen Effekt ist CLSID \_ D2D13DTransform.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
    -   [Interpolations Modi](#interpolation-modes)
    -   [Rahmen Modi](#border-modes)
-   [4X4-Transformations Matrix Klasse](#4x4-transform-matrix-class)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                        |
|---------------------------------------------------------------|
| ![das Bild vor der Transformation.](images/default-before.jpg) |
| Nach                                                         |
| ![das Bild nach der Transformation.](images/24-3dtransform.png)  |



 


```C++
ComPtr<ID2D1Effect> D2D13DTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DTransform, &D2D13DTransformEffect);

D2D13DTransformEffect->SetInput(0, bitmap);

// You can use the helper methods in D2D1::Matrix4x4F to create common matrix transformations.
D2D1_MATRIX_4X4_F matrix = 
    D2D1::Matrix4x4F::Translation(0.0f, -192.0f, 0.0f) *
    D2D1::Matrix4x4F::RotationY(30.0f) *
    D2D1::Matrix4x4F::Translation(0.0f, 192.0f, 0.0f);

D2D13DTransformEffect->SetValue(D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(D2D13DTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effekt Eigenschaften



<table>
<thead>
<tr class="header">
<th>Anzeige Name und indexenumeration</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>InterpolationMode<br/> D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE<br/></td>
<td>Der Interpolations Modus, den der Effekt für das Bild verwendet. Es gibt fünf Skalierungs Modi, die die Qualität und Geschwindigkeit unterliegen.<br/> Der Typ ist D2D1_3DTRANSFORM_INTERPOLATION_MODE.<br/> Der Standardwert ist D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
<tr class="even">
<td>Bordermode<br/> D2D1_3DTRANSFORM_PROP_BORDER_MODE<br/></td>
<td>Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart. Weitere Informationen finden Sie unter <a href="https://www.bing.com/search?q=Border+modes">Border Modes</a> .<br/> Der Typ ist D2D1_BORDER_MODE.<br/> Der Standardwert ist D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="odd">
<td>TransformMatrix<br/> D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX<br/></td>
<td>Eine 4X4-Transformationsmatrix, die auf die Projektionsebene angewendet wird. Die folgende Matrix Berechnung wird verwendet, um Punkte von einem 3D-Koordinatensystem zum transformierten 2D-Koordinatensystem zuzuordnen. <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" />Hierbei gilt:<dl> X, Y, Z = Eingabe Projektions Ebenen-Koordinaten<br />
M<sub>x, y</sub> = Transformations Matrix Elemente<br />
X, Y, Z = Koordinaten der Ausgabe Projektionsebene<br />
</dl> <br/> Die einzelnen Matrix Elemente sind nicht gebunden und sind unitless. <br/> Der Typ ist D2D1_MATRIX_4X4_F.<br/> Der Standardwert ist Matrix4x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).<br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a>Interpolations Modi



| Enumeration                                                   | Beschreibung                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 3dtransform- \_ Interpolations \_ Modus \_ Nächster \_ Nachbar     | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.                                 |
| D2D1 \_ 3dtransform- \_ Interpolations \_ Modus \_ linear                | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. Dieser Modus verwendet mehr Verarbeitungszeit als der nächstgelegene Nachbar Modus, gibt aber ein Image mit höherer Qualität aus. |
| D2D1 \_ 3dtransform- \_ Interpolations \_ Modus ( \_ kubisch)                 | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.                              |
| D2D1 \_ 3dtransform \_ Interpolations \_ Modus \_ \_ Multisample \_ linear | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing. Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.    |
| D2D1 \_ 3dtransform- \_ Interpolations \_ Modus \_ anisotrope           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.                                                           |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1 \_ 3dtransform- \_ Interpolations \_ Modus linear festgelegt \_ .

 

> [!Note]  
> Der anisotrope-Modus generiert bei der Skalierung Mipmaps. Wenn Sie jedoch die **zwischengespeicherte** Eigenschaft für die Effekte, die für diesen Effekt eingegeben werden, auf true festlegen, werden die Mipmaps bei ausreichend kleinen Bildern nicht jedes Mal generiert.

 

### <a name="border-modes"></a>Rahmen Modi



| Name                     | BESCHREIBUNG                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ Border \_ Mode \_ Soft | Der Effekt füllt das Bild mit transparenten schwarzen Pixeln, während es interpoliert, was zu einem weichen Rand führt.<br/> |
| D2D1 \_ Rahmen \_ Modus \_ hart | Der Effekt bindet die Ausgabe an die Größe des Eingabe Bilds. <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a>4X4-Transformations Matrix Klasse

Direct2D stellt eine 4X4-Matrix Klasse zum Bereitstellen von Hilfsfunktionen zum Transformieren des Bilds in drei Dimensionen bereit. Weitere Informationen und eine Beschreibung aller Klassenmember finden Sie im Thema [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) .



| Funktion                                | BESCHREIBUNG                                                                                    | Matrix                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Matrix4x4F:: Scale (X, Y, Z)              | Generiert eine Transformationsmatrix, die die Projektionsebene in der X-, Y-und/oder Z-Richtung skaliert. | ![scale3d-Matrix](images/3d-transform-matrix2.png)     |
| Schrägt (X)                                | Generiert eine Transformationsmatrix, die die Projektionsebene in der X-Richtung verzippt.               | ![Zeigt eine schiefe Matrix in der X-Richtung an.](images/matrix4x4-skewx.png)             |
| Schief (Y)                                | Generiert eine Transformationsmatrix, die die Projektionsebene in der Y-Richtung verzippt.               | ![Schiefe Matrix](images/matrix4x4-skewy.png)             |
| Übersetzung (X, Y, Z)                    | Generiert eine Transformationsmatrix, die die Projektionsebene in der X-, Y-oder Z-Richtung übersetzt. | ![Matrix übersetzen](images/3d-transform-matrix4.png)   |
| RotationX (X)                            | Generiert eine Transformationsmatrix, die die Projektionsebene um die X-Achse dreht.               | ![x-Matrix drehen](images/3d-transform-matrix5.png)    |
| RotationY (Y)                            | Generiert eine Transformationsmatrix, die die Projektionsebene um die Y-Achse dreht.               | ![y-Matrix drehen](images/3d-transform-matrix6.png)    |
| RotationZ (z)                            | Generiert eine Transformationsmatrix, die die Projektionsebene um die Z-Achse dreht.               | ![z-Matrix drehen](images/3d-transform-matrix7.png)    |
| PerspectiveProjection (D)                | Eine perspektivische Transformation mit einem tiefen Wert von D.                                          | ![Perspektiven Matrix](images/3d-transform-matrix8.png) |
| Rotationarbiaryaxis (X, Y, Z, Grad) | Dreht die Projektionsebene um die von Ihnen angegebene Achse.                                       |                                                        |



 

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

 

