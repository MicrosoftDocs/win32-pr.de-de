---
title: Perspektivischer 3D-Transformationseffekt
description: Verwenden Sie den 3D-Perspektiventransformationseffekt, um das Bild in 3 Dimensionen zu drehen, als ob es aus einer Entfernung betrachtet würde.
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- 3D-perspektivischer Transformationseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513d48a38e948f1255afa0cad3972a626c1e5b9039c9285c9c49b4180a5791d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079644"
---
# <a name="3d-perspective-transform-effect"></a>Perspektivischer 3D-Transformationseffekt

Verwenden Sie den 3D-Perspektiventransformationseffekt, um das Bild in 3 Dimensionen zu drehen, als ob es aus einer Entfernung betrachtet würde.

Die 3D-Perspektiventransformation ist praktischer als der 3D-Transformationseffekt, macht aber nur eine Teilmenge der Funktionalität verfügbar. Sie können eine vollständige 3D-Transformationsmatrix berechnen und mithilfe des [3D-Transformationseffekts](3d-transform.md) eine willkürlichere Transformationsmatrix auf ein Bild anwenden.

Die CLSID für diesen Effekt ist CLSID \_ D2D13DPerspectiveTransform.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Interpolationsmodi](#interpolation-modes)
-   [Rahmenmodi](#border-modes)
-   [Ausgabebitmap](#output-bitmap)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                               |
|----------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)           |
| Danach                                                                |
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



## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interpolationmode<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ INTERPOLATION \_ MODE<br/> | Der Interpolationsmodus, den der Effekt für das Bild verwendet. Es gibt fünf Skalierungsmodi, die in Qualität und Geschwindigkeit reichen.<br/> Typ: D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE<br/> Der Standardwert ist D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ LINEAR.<br/>              |
| BorderMode<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ BORDER \_ MODE<br/>               | Der Modus, der zum Berechnen des Rahmens des Bilds verwendet wird( soft oder hard). Weitere Informationen finden Sie unter [Border modes (Rahmenmodi).](https://www.bing.com/search?q=Border+modes)<br/> Typ: D2D1 \_ BORDER \_ MODE<br/> Der Standardwert ist D2D1 \_ BORDER \_ MODE \_ SOFT.<br/>                                                              |
| Tiefe<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ DEPTH<br/>                           | Der Abstand von *PerspectiveOrigin* zur Projektionsebene. Der in DIPs angegebene Wert muss größer als 0 sein.<br/> Typ: FLOAT<br/> Der Standardwert ist 1000.0f.<br/>                                                                                               |
| PerspectiveOrigin<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ PERSPECTIVE \_ ORIGIN<br/> | Die X- und Y-Position des Viewers in der 3D-Szene. Diese Eigenschaft ist ein D2D1 \_ VECTOR \_ 2F, der wie folgt definiert ist: (Punkt X, Punkt Y). Die Einheiten befinden sich in DIPs.<br/> Sie legen den Z-Wert mit der *Depth-Eigenschaft* fest.<br/> Typ: D2D1 \_ VECTOR \_ 2F.<br/> Der Standardwert ist {0.0f, 0.0f}.<br/> |
| LocalOffset<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ LOCAL \_ OFFSET<br/>             | Eine Übersetzung, die der Effekt vor der Drehung der Projektionsebene ausführt. Diese Eigenschaft ist ein D2D1 \_ VECTOR \_ 3F, der wie folgt definiert ist: (X, Y, Z). Die Einheiten befinden sich in DIPs.<br/> Typ: D2D1 \_ VECTOR \_ 3F.<br/> Der Standardwert ist {0.0f, 0.0f, 0.0f}.<br/>                                        |
| GlobalOffset<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ GLOBAL \_ OFFSET<br/>           | Eine Übersetzung, die der Effekt ausführt, nachdem die Projektionsebene gedreht wurde. Diese Eigenschaft ist ein D2D1 \_ VECTOR \_ 3F, der wie folgt definiert ist: (X, Y, Z). Die Einheiten befinden sich in DIPs.<br/> Typ: D2D1 \_ VECTOR \_ 3F.<br/> Der Standardwert ist {0.0f, 0.0f, 0.0f}.<br/>                                         |
| RotationOrigin<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ ROTATION \_ ORIGIN<br/>       | Der Mittelpunkt der Drehung, die der Effekt ausführt. Diese Eigenschaft ist ein D2D1 \_ VECTOR \_ 3F, der wie folgt definiert ist: (X, Y, Z). Die Einheiten befinden sich in DIPs.<br/> Typ: D2D1 \_ VECTOR \_ 3F.<br/> Der Standardwert ist {0.0f, 0.0f, 0.0f}.<br/>                                                            |
| Drehung<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ ROTATION<br/>                     | Die Drehwinkel für jede Achse. Diese Eigenschaft ist ein D2D1 \_ VECTOR \_ 3F, der wie folgt definiert ist: (X, Y, Z). Die Einheiten sind in Grad.<br/> Typ: D2D1 \_ VECTOR \_ 3F.<br/> Der Standardwert ist {0.0f, 0.0f, 0.0f}.<br/>                                                                         |



 

## <a name="interpolation-modes"></a>Interpolationsmodi



| Enumeration                                                              | Beschreibung                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR     | Probieren Sie den nächstgelegenen einzelnen Punkt aus, und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das Bild mit der niedrigsten Qualität aus.                                 |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ LINEAR                | Verwendet eine Vier-Punkt-Stichprobe und lineare Interpolation. Dieser Modus verwendet mehr Verarbeitungszeit als der nächste Nachbarmodus, gibt jedoch ein Bild höherer Qualität aus. |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ KUBISCH                 | Verwendet einen kubischen Kernel mit 16 Beispielen für die Interpolation. Dieser Modus verwendet die meiste Verarbeitungszeit, gibt jedoch ein Bild höherer Qualität aus.                              |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für ein gutes Edge-Antialiasing. Dieser Modus eignet sich gut für das Herunterskalierung um kleine Mengen auf Bildern mit wenigen Pixeln.    |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ ANISOTROP           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap abzubilden.                                                           |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird standardmäßig D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE LINEAR \_ verwendet.

 

> [!Note]  
> Der Anisotropiemodus generiert bei der Skalierung Mipmaps. Wenn Sie jedoch die **Cached-Eigenschaft** für die Effekte, die für diesen Effekt eingegeben werden, auf TRUE festlegen, werden die Mipmaps nicht jedes Mal für ausreichend kleine Bilder generiert.

 

## <a name="border-modes"></a>Rahmenmodi



| Name                     | BESCHREIBUNG                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ BORDER \_ MODE \_ SOFT | Der Effekt auflagert das Bild bei der Interpolation mit transparenten schwarzen Pixeln, was zu einem weichen Rand führt.<br/> |
| D2D1– \_ \_ RAHMENMODUS \_ FEST | Der Effekt klammert die Ausgabe an die Größe des Eingabebilds. <br/>                                         |



 

## <a name="output-bitmap"></a>Ausgabebitmap

Die Größe der Ausgabebitmap hängt von der Transformationsmatrix ab, die auf das Bild angewendet wird.

Der Effekt führt den Transformationsvorgang aus und wendet dann ein Begrenzungsfeld um das Ergebnis an. Die Ausgabebitmap ist die Größe des Begrenzungsfelds.

## <a name="requirements"></a>Requirements (Anforderungen)



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

 

