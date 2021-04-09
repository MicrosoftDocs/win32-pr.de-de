---
title: Perspektivischer 3D-Transformationseffekt
description: Verwenden Sie den 3D-perspektivischen Transformations Effekt, um das Bild in drei Dimensionen so zu drehen, als ob es aus einer Entfernung
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- 3D--Perspektiven Transformations Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859321"
---
# <a name="3d-perspective-transform-effect"></a>Perspektivischer 3D-Transformationseffekt

Verwenden Sie den 3D-perspektivischen Transformations Effekt, um das Bild in drei Dimensionen so zu drehen, als ob es aus einer Entfernung

Die 3D-perspektivische Transformation ist einfacher als der 3D-Transformations Effekt, macht aber nur eine Teilmenge der Funktionalität verfügbar. Sie können eine vollständige 3D-Transformationsmatrix berechnen und mithilfe des [3D-](3d-transform.md) Transformations Effekts eine willkürlichere Transformationsmatrix auf ein Bild anwenden.

Die CLSID für diesen Effekt ist CLSID \_ D2D13DPerspectiveTransform.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Interpolations Modi](#interpolation-modes)
-   [Rahmen Modi](#border-modes)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                               |
|----------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)           |
| Nach                                                                |
| ![das Bild nach dem Effekt.](images/23-3dperspectivetransform.png) |



 


```C++
ComPtr<ID2D1Effect> perspectiveTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DPerspectiveTransform, &perspectiveTransformEffect);

perspectiveTransformEffect->SetInput(0, bitmap);

perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1::Vector3F(0.0f, 192.0f, 0.0f));
perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1::Vector3F(0.0f, 30.0f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(perspectiveTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolationMode<br/> D2D1 \_ 3dperspectivetransform- \_ Prop- \_ Interpolations \_ Modus<br/> | Der Interpolations Modus, den der Effekt für das Bild verwendet. Es gibt fünf Skalierungs Modi, die die Qualität und Geschwindigkeit unterliegen.<br/> Type ist der D2D1 \_ 3dperspectivetransform \_ Interpolations \_ Modus.<br/> Der Standardwert ist der D2D1 \_ 3dperspectivetransform- \_ Interpolations \_ Modus \_ linear.<br/>              |
| Bordermode<br/> D2D1 \_ 3dperspectivetransform-Rahmen \_ \_ \_ Modus<br/>               | Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart. Weitere Informationen finden Sie unter [Border Modes](https://www.bing.com/search?q=Border+modes) .<br/> Typ: D2D1 \_ Border \_ Mode<br/> Der Standardwert ist D2D1 \_ Border \_ Mode \_ Soft.<br/>                                                              |
| Tiefe<br/> D2D1 \_ 3dperspectivetransform- \_ Prop- \_ Tiefe<br/>                           | Der Abstand zwischen *perspectiveorigin* und Projektionsebene. Der in Dips angegebene Wert muss größer als 0 (null) sein.<br/> Der Typ ist "float".<br/> Der Standardwert ist 1000.0 f.<br/>                                                                                               |
| Perspectiveorigin<br/> D2D1 \_ 3dperspectivetransform \_ Prop \_ Perspective- \_ Ursprung<br/> | Der X-und Y-Speicherort des Viewers in der 3D-Szene. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 2F, definiert als: (Punkt X, Punkt Y). Die Einheiten befinden sich in Dips.<br/> Sie legen den Z-Wert mit der Eigenschaft *Tiefe* fest.<br/> Typ: D2D1 \_ Vector \_ 2F<br/> Der Standardwert ist {0,0 f, 0,0 f}.<br/> |
| Localoffset<br/> D2D1 \_ 3dperspectivetransform- \_ Prop ( \_ lokaler \_ Offset)<br/>             | Eine Übersetzung, die den Effekt ausführt, bevor die Projektionsebene gedreht wird. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 3F, definiert als: (X, Y, Z). Die Einheiten befinden sich in Dips.<br/> Type ist D2D1 \_ Vector \_ 3f.<br/> Der Standardwert ist {0,0 f, 0,0 f, 0,0 f}.<br/>                                        |
| Globaloffset<br/> D2D1 \_ 3dperspectivetransform \_ - \_ globaler \_ Offset<br/>           | Eine Übersetzung, die den Effekt nach dem Drehen der Projektionsebene ausführt. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 3F, definiert als: (X, Y, Z). Die Einheiten befinden sich in Dips.<br/> Type ist D2D1 \_ Vector \_ 3f.<br/> Der Standardwert ist {0,0 f, 0,0 f, 0,0 f}.<br/>                                         |
| Rotationorigin<br/> D2D1 \_ 3dperspectivetransform- \_ Prop- \_ Rotation- \_ Ursprung<br/>       | Der Mittelpunkt der Drehung, die der Effekt ausführt. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 3F, definiert als: (X, Y, Z). Die Einheiten befinden sich in Dips.<br/> Type ist D2D1 \_ Vector \_ 3f.<br/> Der Standardwert ist {0,0 f, 0,0 f, 0,0 f}.<br/>                                                            |
| Drehung<br/> D2D1 \_ 3dperspectivetransform- \_ Prop- \_ Drehung<br/>                     | Die Winkel der Drehung für jede Achse. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 3F, definiert als: (X, Y, Z). Die Einheiten liegen in Grad.<br/> Type ist D2D1 \_ Vector \_ 3f.<br/> Der Standardwert ist {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                         |



 

## <a name="interpolation-modes"></a>Interpolations Modi



| Enumeration                                                              | Beschreibung                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 3dperspectivetransform- \_ Interpolations \_ Modus \_ Nächster \_ Nachbar     | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.                                 |
| D2D1 \_ 3dperspectivetransform- \_ Interpolations \_ Modus \_ linear                | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. Dieser Modus verwendet mehr Verarbeitungszeit als der nächstgelegene Nachbar Modus, gibt aber ein Image mit höherer Qualität aus. |
| D2D1 \_ 3dperspectivetransform- \_ Interpolations \_ Modus ( \_ kubisch)                 | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.                              |
| D2D1 \_ 3dperspectivetransform \_ Interpolations \_ Modus \_ \_ Multisample \_ linear | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing. Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.    |
| D2D1 \_ 3dperspectivetransform- \_ Interpolations \_ Modus \_ anisotrope           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.                                                           |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1 \_ 3dperspectivetransform- \_ Interpolations \_ Modus linear festgelegt \_ .

 

> [!Note]  
> Der anisotrope-Modus generiert bei der Skalierung Mipmaps. Wenn Sie jedoch die **zwischengespeicherte** Eigenschaft für die Effekte, die für diesen Effekt eingegeben werden, auf true festlegen, werden die Mipmaps bei ausreichend kleinen Bildern nicht jedes Mal generiert.

 

## <a name="border-modes"></a>Rahmen Modi



| Name                     | BESCHREIBUNG                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ Border \_ Mode \_ Soft | Der Effekt füllt das Bild mit transparenten schwarzen Pixeln, während es interpoliert, was zu einem weichen Rand führt.<br/> |
| D2D1 \_ Rahmen \_ Modus \_ hart | Der Effekt bindet die Ausgabe an die Größe des Eingabe Bilds. <br/>                                         |



 

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

 

