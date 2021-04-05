---
title: Anbau Effekt
description: Verwenden Sie den Anbau Effekt, um einen angegebenen Bereich eines Bilds auszugeben.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- Anbau Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ceaf4cf8b5922fe05e151c1639269f3169b57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858874"
---
# <a name="crop-effect"></a>Anbau Effekt

Verwenden Sie den Anbau Effekt, um einen angegebenen Bereich eines Bilds auszugeben.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Crop.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| Nach                                                      |
| ![das Bild nach der Transformation.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effekt Eigenschaften



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Anzeige Name und indexenumeration</th>
<th>Typ und Standardwert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Rect<br/></td>
<td>D2D1_VECTOR_4F<br/></td>
<td>Der Bereich, der als Vektor im Formular (Links, oben, Breite, Höhe) festgelegt werden soll.<br/></td>
</tr>
<tr class="even">
<td>D2D1_CROP_PROP_RECT<br/></td>
<td>{-FLT_MAX,-FLT_MAX, FLT_MAX, FLT_MAX}<br/></td>
<td>Die Einheiten befinden sich in Dips. <br/>
<blockquote>
<p>[!Note]</p>
<p>Der Rect wird abgeschnitten, wenn die Randgrenzen des Eingabe Bilds überlappt werden.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D2D1_CROP_PROP_BORDER_MODE<br/></td>
<td>D2D1_BORDER_MODE <br/> D2D1_BORDER_MODE_SOFT <br/></td>
<td><ul>
<li>D2D1_BORDER_MODE_SOFT: Wenn das Zuweisungs Rechteck in Bruch Komma Koordinaten fällt, wendet der Effekt das Antialiasing an, das zu einem Soft Edge führt.</li>
<li>D2D1_BORDER_MODE_HARD: Wenn das Zuweisungs Rechteck auf Pixelkoordinaten mit Bruchteilen fällt, wird der Effekt durch einen festen Rand fest.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Die Ausgabe dieses Effekts ist die Größe der Rect-Eigenschaft. Länge und Breite sind Calc

mithilfe der Gleichungen in der folgenden Abbildung dargestellt: <dl> Ausgabe Länge in Pixel = (Rect. Right-Rect. Left) \* (dpi/96 des Benutzers)  
Ausgabe Höhe in Pixel = (Rect. Bottom-Rect.Top) \* (dpi/96 des Benutzers)  
</dl>

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

 

