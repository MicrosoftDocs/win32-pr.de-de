---
title: Skalierungseffekt
description: Verwenden Sie diesen Effekt, um ein Bild nach oben oder unten zu skalieren. Der Effekt verfügt über sechs Skalierungsmodi, die dem nächsten Nachbarn, linear, kubisch, multistichund linear, anisotrop und kubisch in hoher Qualität sind.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- Skalierungseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3a4ef93fcdd2e93580157e0bb73b172975fe4a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472931"
---
# <a name="scale-effect"></a>Skalierungseffekt

Verwenden Sie diesen Effekt, um ein Bild nach oben oder unten zu skalieren. Der Effekt hat sechs Skalierungsmodi: nächster Nachbar, linear, kubisch, multisamplingline, anisotrop und kubisch hoher Qualität.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Scale.

-   [Beispielbild](#example-image)
-   [Effekteigenschaften](#effect-properties)
    -   [Rahmenmodi](#border-modes)
-   [Interpolationsmodi](#interpolation-modes)
-   [Ausgabebitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Dieses Beispiel zeigt den Skalierungseffekt, der das Zweifache der Eingabe vergrößert und auf die ursprüngliche Größe zugeschnitten wird.



| Vorher                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| Danach                                                      |
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



## <a name="effect-properties"></a>Effekteigenschaften




| Anzeigename und Indexenumeration | BESCHREIBUNG | 
|------------------------------------|-------------|
| Skalieren<br /> D2D1_SCALE_PROP_SCALE<br /> | Die Skalierungsmenge in X- und Y-Richtung als Verhältnis der Ausgabegröße zur Eingabegröße. Diese Eigenschaft D2D1_VECTOR_2Fdefined wie: (X-Skalierung, Y-Skalierung). Die Skalierungsbeträge sind FLOAT, einheitenlos und müssen positiv oder 0 sein.<br /> Der Typ ist D2D1_VECTOR_2F.<br /> Der Standardwert ist {1.0f, 1.0f}.<br /> | 
| CenterPoint<br /> D2D1_SCALE_PROP_CENTER_POINT<br /> | Der Mittelpunkt der Bildskalierung. Diese Eigenschaft ist ein D2D1_VECTOR_2F definiert als : (Punkt X, Punkt Y). Die Einheiten befinden sich in DIPs.<br /> Verwenden Sie die Eigenschaft Mittelpunkt, um einen anderen Punkt als die linke obere Ecke zu skalieren.<br /> Der Typ ist D2D1_VECTOR_2F.<br /> Der Standardwert ist {0.0f, 0.0f}.<br /> | 
| BorderMode<br /> D2D1_SCALE_PROP_BORDER_MODE<br /> | Der Modus, der zum Berechnen des Rahmens des Bilds verwendet wird( soft oder hard). Weitere Informationen finden Sie unter <a href="#border-modes">Border modes (Rahmenmodi).</a> <br /> Der Typ ist D2D1_BORDER_MODE.<br /> Der Standardwert ist D2D1_BORDER_MODE_SOFT.<br /> | 
| Schärfe<br /> D2D1_SCALE_PROP_SHARPNESS<br /> | Im kubischen Interpolationsmodus von hoher Qualität die Schärfestufe des Skalierungsfilters als Gleitkommawert zwischen 0 und 1. Die Werte sind einheitenlos. Sie können die Schärfe verwenden, um die Qualität eines Bilds anzupassen, wenn Sie das Bild herunterskalieren.<br /> Der Schärfefaktor wirkt sich auf die Form des Kernels aus. Je höher der Schärfefaktor, desto kleiner der Kernel.<br /><blockquote>[!Note]<br />Diese Eigenschaft wirkt sich nur auf den kubischen Interpolationsmodus hoher Qualität aus.</blockquote><br /> Der Typ ist FLOAT.<br /> Der Standardwert ist 0,0f.<br /> | 
| Interpolationmode<br /> D2D1_SCALE_PROP_INTERPOLATION_MODE<br /> | Der Interpolationsmodus, den der Effekt zum Skalieren des Bilds verwendet. Es gibt sechs Skalierungsmodi, die in Qualität und Geschwindigkeit reichen. Weitere Informationen finden Sie <a href="#interpolation-modes">unter Interpolationsmodi.</a> <br /> Der Typ ist D2D1_SCALE_INTERPOLATION_MODE.<br /> Der Standardwert ist D2D1_SCALE_INTERPOLATION_MODE_LINEAR.<br /> | 




 

### <a name="border-modes"></a>Rahmenmodi



| Name                     | BESCHREIBUNG                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ BORDER \_ MODE \_ SOFT | Durch den Effekt wird das Eingabebild mit transparenten schwarzen Pixeln für Stichproben außerhalb der Eingabegrenzen aufgefüllt, wenn der Konvolutionskernel angewendet wird. Dadurch wird ein weicher Rand für das Bild erstellt, und im Prozess wird die Ausgabebitmap um die Größe des Kernels erweitert.<br/> |
| D2D1 \_ BORDER \_ MODE \_ HARD | Der Effekt erweitert das Eingabebild um eine Rahmentransformation des Spiegeltyps für Stichproben außerhalb der Eingabegrenzen. Die Größe der Ausgabebitmap entspricht der Größe der Eingabebitmap.<br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a>Interpolationsmodi



| Enumeration                                             | Beschreibung                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1– \_ \_ SKALIERUNGSINTERPOLATIONSMODUS \_ \_ NÄCHSTER \_ NACHBAR     | Probieren Sie den nächstgelegenen einzelnen Punkt aus, und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das Bild mit der niedrigsten Qualität aus.                                                                           |
| D2D1– \_ \_ SKALIERUNGSINTERPOLATIONSMODUS \_ \_ LINEAR                | Verwendet eine Vier-Punkt-Stichprobe und lineare Interpolation. Dieser Modus verwendet mehr Verarbeitungszeit als der nächste Nachbarmodus, gibt jedoch ein Bild höherer Qualität aus.                                           |
| \_ \_ D2D1–SKALIERUNGSINTERPOLATIONSMODUS \_ \_ KUBISCH                 | Verwendet einen kubischen Kernel mit 16 Beispielen für die Interpolation. Dieser Modus verwendet die meiste Verarbeitungszeit, gibt jedoch ein Bild höherer Qualität aus.                                                                        |
| D2D1 \_ SCALE \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für ein gutes Edge-Antialiasing. Dieser Modus eignet sich gut für das Herunterskalierung um kleine Mengen auf Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ SCALE \_ INTERPOLATION MODE \_ \_ ANISOTROP           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap abzubilden.                                                                                                     |
| D2D1 \_ SCALE \_ INTERPOLATION MODE HIGH QUALITY \_ \_ \_ \_ KUBISCH  | Verwendet einen kubischen Kernel variabler Größe, um das Bild vorab herunterzuskalieren, wenn die Transformationsmatrix eine Downskalierung umfasst. Verwendet dann den kubischen Interpolationsmodus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, lautet der Effekt standardmäßig D2D1 \_ SCALE \_ INTERPOLATION \_ MODE \_ LINEAR.

 

> [!Note]  
> Im Anisotropiemodus werden bei der Skalierung Mipmaps generiert. Wenn Sie jedoch die **Cached-Eigenschaft** für die Effekte, die für diesen Effekt eingegeben werden, auf TRUE festlegen, werden die Mipmaps nicht jedes Mal für ausreichend kleine Bilder generiert.

 

## <a name="output-bitmap"></a>Ausgabebitmap

Die Position und Größe der Ausgabebitmap hängt vom angegebenen Skalierungsfaktor und dem Mittelpunkt ab.

Sie können die Größe der Ausgabebitmap mithilfe dieser Gleichung berechnen:<dl> BitmapSize? (Pixel)=Skalieren? \* Ursprüngliche Bitmapgröße? (DIPs) \* (UserDPI/96)  
BitmapSize<sub>y</sub>(Pixels)=Scale<sub>y</sub> \* Original Bitmap Size<sub>y</sub> (DIPs) \* (UserDPI/96)  
</dl>

Der Effekt rundet Bruchteile von Pixeln auf das nächste ganze Pixel auf.

Die Position der Bitmap ist (0, 0) oder der Wert der Mittelpunkteigenschaft.

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

 

