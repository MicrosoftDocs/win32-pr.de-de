---
title: 3D-Transformationseffekt
description: Verwenden Sie den 3D-Transformationseffekt, um eine beliebige 4x4-Transformationsmatrix auf ein Bild anzuwenden.
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- 3D-Transformationseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32a9c8fedca3be0d96a44047ac1b226d83309cf657f2cdc223a342e9d38880b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758219"
---
# <a name="3d-transform-effect"></a>3D-Transformationseffekt

Verwenden Sie den 3D-Transformationseffekt, um eine beliebige 4x4-Transformationsmatrix auf ein Bild anzuwenden.

Dieser Effekt wendet die Matrix (M?) an, die Sie mithilfe dieser Berechnung auf die Eckvertices des Quellbilds \[ (x y z \] 1) bereitstellen:

\[x<sub>r</sub> y<sub>r</sub> z<sub>r 1</sub> \] = \[ x y z 1 \] \* M?

Die CLSID für diesen Effekt ist CLSID \_ D2D13DTransform.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
    -   [Interpolationsmodi](#interpolation-modes)
    -   [Rahmenmodi](#border-modes)
-   [4x4 Transform Matrix-Klasse](#4x4-transform-matrix-class)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                        |
|---------------------------------------------------------------|
| ![das Bild vor der Transformation.](images/default-before.jpg) |
| Danach                                                         |
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



## <a name="effect-properties"></a>Effect-Eigenschaften



<table>
<thead>
<tr class="header">
<th>Anzeigename und Indexenumeration</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Interpolationmode<br/> D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE<br/></td>
<td>Der Interpolationsmodus, den der Effekt auf dem Bild verwendet. Es gibt fünf Skalierungsmodi, die in Qualität und Geschwindigkeit reichen.<br/> Der Typ ist D2D1_3DTRANSFORM_INTERPOLATION_MODE.<br/> Der Standardwert ist D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
<tr class="even">
<td>BorderMode<br/> D2D1_3DTRANSFORM_PROP_BORDER_MODE<br/></td>
<td>Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, soft oder hard. Weitere <a href="https://www.bing.com/search?q=Border+modes">Informationen finden Sie</a> unter Rahmenmodi.<br/> Typ ist D2D1_BORDER_MODE.<br/> Der Standardwert ist D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="odd">
<td>TransformMatrix<br/> D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX<br/></td>
<td>Eine 4x4-Transformationsmatrix, die auf die Projektionsebene angewendet wird. Die folgende Matrixberechnung wird verwendet, um Punkte aus einem 3D-Koordinatensystem dem transformierten 2D-Koordinatensystem zu zuordnen. <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" />Hierbei gilt:<dl> X, Y, Z = Koordinaten der Eingabeprojektionsebene<br />
M<sub>x,y</sub> = Matrixelemente transformieren<br />
X, Y, Z = Koordinaten der Ausgabeprojektionsebene<br />
</dl> <br/> Die einzelnen Matrixelemente sind nicht gebunden und sind einheitslos. <br/> Typ ist D2D1_MATRIX_4X4_F.<br/> Der Standardwert ist Matrix4x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).<br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a>Interpolationsmodi



| Enumeration                                                   | Beschreibung                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 3DTRANSFORM \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR     | Stichprobenentnahme für den nächstgelegenen einzelnen Punkt und Verwendung dieses Punkts. Dieser Modus verbraucht weniger Verarbeitungszeit, gibt jedoch das Image mit der niedrigsten Qualität aus.                                 |
| D2D1 \_ 3DTRANSFORM \_ \_ INTERPOLATIONSMODUS \_ LINEAR                | Verwendet eine Stichprobe mit vier Punkt und eine lineare Interpolation. Dieser Modus verwendet mehr Verarbeitungszeit als der nächste Nachbarmodus, gibt jedoch ein Bild mit höherer Qualität aus. |
| D2D1 \_ 3DTRANSFORM \_ \_ INTERPOLATIONSMODUS \_ KUBISCH                 | Verwendet einen kubischen 16-Beispielkernel für die Interpolation. Dieser Modus verwendet die meiste Verarbeitungszeit, gibt jedoch ein Image mit höherer Qualität aus.                              |
| D2D1 \_ 3DTRANSFORM \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für ein gutes Edge-Antialiasing. Dieser Modus ist gut für das herunterskalieren um kleine Mengen auf Bildern mit wenigen Pixeln.    |
| D2D1 \_ 3DTRANSFORM \_ INTERPOLATION \_ MODE \_ ANISOTROPIC           | Verwendet die anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu beproben.                                                           |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf D2D1 \_ 3DTRANSFORM \_ INTERPOLATION \_ MODE LINEAR \_ festgelegt.

 

> [!Note]  
> Im anisotropen Modus werden bei der Skalierung Mipmaps generiert. Wenn Sie jedoch die **Cached-Eigenschaft** auf TRUE für die Effekte festlegen, die für diesen Effekt eingegeben werden, werden die Mipmaps nicht jedes Mal für ausreichend kleine Bilder generiert.

 

### <a name="border-modes"></a>Rahmenmodi



| Name                     | Beschreibung                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ BORDER \_ MODE \_ SOFT | Der Effekt auflagert das Bild bei der Interpolation mit transparenten schwarzen Pixeln, was zu einem weichen Rand führt.<br/> |
| D2D1– \_ \_ RAHMENMODUS \_ FEST | Der Effekt klammert die Ausgabe an die Größe des Eingabebilds. <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a>4x4 Transform Matrix-Klasse

Direct2D stellt eine 4x4-Matrixklasse zur Verfügung, um Hilfsfunktionen zum Transformieren des Bilds in 3 Dimensionen zur Verfügung zu stellen. Weitere Informationen und eine Beschreibung aller Klassenmitglieder finden Sie im Thema [**Matrix4x4F.**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f)



| Funktion                                | Beschreibung                                                                                    | Matrix                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Matrix4x4F::Scale(X, Y, Z)              | Generiert eine Transformationsmatrix, die die Projektionsebene in X-, Y- und/oder Z-Richtung skaliert. | ![scale3d-Matrix](images/3d-transform-matrix2.png)     |
| SkewX(X)                                | Generiert eine Transformationsmatrix, die die Projektionsebene in X-Richtung verzerrt.               | ![Zeigt eine Schiefematrix in X-Richtung an.](images/matrix4x4-skewx.png)             |
| Skewy(Y)                                | Generiert eine Transformationsmatrix, die die Projektionsebene in Y-Richtung verzerrt.               | ![Schiefe Matrix](images/matrix4x4-skewy.png)             |
| Translation(X, Y, Z)                    | Generiert eine Transformationsmatrix, die die Projektionsebene in X-, Y- oder Z-Richtung übersetzt. | ![Übersetzen der Matrix](images/3d-transform-matrix4.png)   |
| RotationX(X)                            | Generiert eine Transformationsmatrix, die die Projektionsebene um die X-Achse dreht.               | ![X-Matrix drehen](images/3d-transform-matrix5.png)    |
| RotationY(Y)                            | Generiert eine Transformationsmatrix, die die Projektionsebene um die Y-Achse dreht.               | ![y-Matrix drehen](images/3d-transform-matrix6.png)    |
| RotationZ(Z)                            | Generiert eine Transformationsmatrix, die die Projektionsebene um die Z-Achse dreht.               | ![Z-Matrix drehen](images/3d-transform-matrix7.png)    |
| PerspectiveProjection(D)                | Eine perspektivische Transformation mit dem Tiefenwert D.                                          | ![Perspektivenmatrix](images/3d-transform-matrix8.png) |
| RotationArbitraryAxis(X, Y, Z, Degrees) | Rotiert die Projektionsebene um die angegebene Achse.                                       |                                                        |



 

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

 

