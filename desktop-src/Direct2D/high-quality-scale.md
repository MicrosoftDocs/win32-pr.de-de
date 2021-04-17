---
title: Skalierungseffekt
description: Verwenden Sie diesen Effekt, um ein Bild nach oben oder unten zu skalieren. Der Effekt hat sechs Skalierungs Modi nächster Nachbar, linear, kubisch, Multisample linear, anisotrope und High Quality kubisch.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- Skalierungs Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3af77bc24db387fff0854e0432c270fa2ce6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391830"
---
# <a name="scale-effect"></a>Skalierungseffekt

Verwenden Sie diesen Effekt, um ein Bild nach oben oder unten zu skalieren. Der Effekt hat sechs Skalierungs Modi: nächster Nachbar, linear, kubisch, Multisample linear, anisotrope und High Quality kubisch.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Scale.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
    -   [Rahmen Modi](#border-modes)
-   [Interpolations Modi](#interpolation-modes)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Dieses Beispiel zeigt, wie der Skalierungs Effekt in den 2fachen der Eingabe vergrößert wird und auf die ursprüngliche Größe zugreift.



| Vorher                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| Nach                                                      |
| ![das Bild nach der Transformation.](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



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
<td>Skalieren<br/> D2D1_SCALE_PROP_SCALE<br/></td>
<td>Der Skalierungs Betrag in der X-und Y-Richtung als Verhältnis zwischen der Ausgabegröße und der Eingabe Größe. Diese Eigenschaft ist eine D2D1_VECTOR_2Fdefined wie: (X Scale, Y Scale). Die Skalierungs Beträge sind float, unitless und müssen positiv oder 0 sein.<br/> Der Typ ist D2D1_VECTOR_2F.<br/> Der Standardwert ist {1.0 f, 1.0 f}.<br/></td>
</tr>
<tr class="even">
<td>CenterPoint<br/> D2D1_SCALE_PROP_CENTER_POINT<br/></td>
<td>Der Mittelpunkt der Bildskalierung. Diese Eigenschaft ist eine D2D1_VECTOR_2F, die wie folgt definiert ist: (Punkt X, Punkt Y). Die Einheiten befinden sich in Dips.<br/> Verwenden Sie die Mittelpunkt Eigenschaft, um einen anderen Punkt als die linke obere Ecke zu skalieren.<br/> Der Typ ist D2D1_VECTOR_2F.<br/> Der Standardwert ist {0,0 f, 0,0 f}.<br/></td>
</tr>
<tr class="odd">
<td>Bordermode<br/> D2D1_SCALE_PROP_BORDER_MODE<br/></td>
<td>Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart. Weitere Informationen finden Sie unter <a href="#border-modes">Border Modes</a> . <br/> Der Typ ist D2D1_BORDER_MODE.<br/> Der Standardwert ist D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="even">
<td>Schärfe<br/> D2D1_SCALE_PROP_SHARPNESS<br/></td>
<td>Im hochwertigen kubischen Interpolations Modus ist die Schärfe des Skalierungs Filters ein Gleit Komma Wert zwischen 0 und 1. Die Werte sind unitless. Mit der Schärfe können Sie die Qualität eines Bilds anpassen, wenn Sie das Bild nach unten skalieren.<br/> Der Schärfe Faktor wirkt sich auf die Form des Kernels aus. Je höher der Schärfe Faktor, desto kleiner der Kernel.<br/>
<blockquote>
[!Note]<br />
Diese Eigenschaft wirkt sich nur auf den hochwertigen kubischen Interpolations Modus aus.
</blockquote>
<br/> Der Typ ist "float".<br/> Der Standardwert ist 0,0 f.<br/></td>
</tr>
<tr class="odd">
<td>InterpolationMode<br/> D2D1_SCALE_PROP_INTERPOLATION_MODE<br/></td>
<td>Der Interpolations Modus, den der Effekt zum Skalieren des Bilds verwendet. Es gibt sechs Skalierungs Modi mit hoher Qualität und Geschwindigkeit. Weitere Informationen finden Sie unter <a href="#interpolation-modes">Interpolations Modi</a> . <br/> Der Typ ist D2D1_SCALE_INTERPOLATION_MODE.<br/> Der Standardwert ist D2D1_SCALE_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="border-modes"></a>Rahmen Modi



| Name                     | BESCHREIBUNG                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ Border \_ Mode \_ Soft | Der Effekt füllt das Eingabebild mit transparenten schwarzen Pixeln für Stichproben außerhalb der Eingabe Grenzen auf, wenn es den zuordnerkerntyp anwendet. Dadurch wird ein weicher Edge für das Bild erstellt, und im Prozess wird die Ausgabe Bitmap um die Größe des Kernels erweitert.<br/> |
| D2D1 \_ Rahmen \_ Modus \_ hart | Die Auswirkung erweitert das Eingabebild durch eine Spiegelungs Typen-Rahmen Transformation für Beispiele außerhalb der Eingabe Grenzen. Die Größe der Ausgabe Bitmap entspricht der Größe der Eingabe Bitmap.<br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a>Interpolations Modi



| Enumeration                                             | Beschreibung                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ Scale \_ Interpolations \_ Modus \_ Nächster \_ Nachbar     | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.                                                                           |
| D2D1 \_ - \_ Interpolations \_ Modus \_ linear                | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. Dieser Modus verwendet mehr Verarbeitungszeit als der nächstgelegene Nachbar Modus, gibt aber ein Image mit höherer Qualität aus.                                           |
| D2D1 \_ - \_ Skalierungs Modus für Interpolations \_ Modus \_                 | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.                                                                        |
| D2D1 \_ Scale \_ Interpolations \_ Modus \_ \_ Multisample \_ linear | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing. Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ Scale \_ Interpolations \_ Modus \_ anisotrope           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.                                                                                                     |
| D2D1 \_ Scale- \_ Interpolations \_ Modus \_ High \_ Quality \_ kubisch  | Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1 \_ Scale \_ Interpolations \_ Modus \_ linear.

 

> [!Note]  
> Der anisotrope-Modus generiert bei der Skalierung Mipmaps. Wenn Sie jedoch die **zwischengespeicherte** Eigenschaft für die Effekte, die für diesen Effekt eingegeben werden, auf true festlegen, werden die Mipmaps bei ausreichend kleinen Bildern nicht jedes Mal generiert.

 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Der Speicherort und die Größe der Ausgabe Bitmap sind abhängig vom angegebenen Skalierungsfaktor und dem Mittelpunkt.

Mit dieser Formel können Sie die Größe der Ausgabe Bitmap berechnen:<dl> Bitmapsize? (Pixel) = Skalieren? \* Ursprüngliche Bitmapgröße? (Dips) \* (Userdpi/96)  
Bitmapsize<sub>y</sub>(Pixel) =<sub>y</sub> \* ursprüngliche Bitmapgröße skalieren<sub>y</sub> (Dips) \* (userdpi/96)  
</dl>

Der Effekt rundet Bruchteile von Pixeln auf das nächste ganze Pixel ab.

Der Speicherort der Bitmap ist (0,0) oder der Wert der Mittelpunkt Eigenschaft.

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

 

