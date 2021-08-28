---
title: Direktionaler Weichreffekt
description: Der direktionale Weichdeeffekt ähnelt gaußschen Weichungen, mit der Ausnahme, dass Sie den Weich weicher in eine bestimmte Richtung verzerren können.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- Richtungsunschärfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a43dcaa60f8627473444572ec36a13c3949e9430c9befbb5c064b51d7813bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260434"
---
# <a name="directional-blur-effect"></a>Direktionaler Weichreffekt

Der direktionale Weichmereffekt ähnelt [Gaußs'schen](gaussian-blur.md)Weichungen, mit der Ausnahme, dass Sie die Weichde in eine bestimmte Richtung verzerren können. Sie können diesen Effekt verwenden, um ein Bild so aussehen zu lassen, als ob es sich in Bewegung befindet, oder um ein animiertes Bild zu hervorheben.

Die CLSID für diesen Effekt ist CLSID \_ D2D1DirectionalBlur.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Optimierungsmodi](#optimization-modes)
-   [Rahmenmodi](#border-modes)
-   [Ausgabebitmap](#output-bitmap)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                          |
|-----------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)      |
| Danach                                                           |
| ![das Bild nach der Transformation.](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation (Standardabweichung)<br/> D2D1 \_ DIRECTIONALBLUR \_ PROP \_ STANDARD \_ DEVIATION<br/> | Die Auf das Bild anzuwendende Weichbildmenge. Sie können den Weichderadius des Kernels berechnen, indem Sie die Standardabweichung mit 3 multiplizieren. Die Einheiten der Standardabweichung und des Weicherradius sind DIPs. Dieser Effekt wird durch den Wert 0 DIPs deaktiviert. Der Typ ist FLOAT.<br/> Der Standardwert ist 3,0f.<br/>                                                                            |
| Angle<br/> D2D1 \_ DIRECTIONALBLUR \_ PROP \_ ANGLE<br/>                           | Der Winkel der Weichansicht relativ zur x-Achse in der gegen den Uhrzeigersinn weisenden Richtung. Die Einheiten werden in Grad angegeben.<br/> Der Weichdekernel wird zuerst mit demselben Prozess wie für den [Gaußschen Weichdeeffekt](gaussian-blur.md) generiert. Die Kernelwerte werden dann entsprechend dem weicheren Winkel transformiert.<br/> Der Typ ist FLOAT.<br/> Der Standardwert ist 0,0f.<br/> |
| Optimization<br/> D2D1 \_ DIRECTIONALBLUR \_ PROP \_ OPTIMIZATION<br/>             | Der Optimierungsmodus. Weitere [Informationen finden Sie](#optimization-modes) unter Optimierungsmodi.<br/> Der Typ ist D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION.<br/> Der Standardwert ist D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ BALANCED. <br/>                                                                                                                                                         |
| BorderMode<br/> D2D1 \_ DIRECTIONALBLUR \_ PROP \_ BORDER \_ MODE<br/>               | Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, soft oder hard. Weitere [Informationen finden Sie](#border-modes) unter Rahmenmodi.<br/> Der Typ ist D2D1 \_ BORDER \_ MODE.<br/> Der Standardwert ist D2D1 \_ BORDER \_ MODE \_ SOFT.<br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a>Optimierungsmodi



| Name                                          | Beschreibung                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ SPEED    | Wendet interne Optimierungen an, z. B. die Vorskalierung bei relativ kleinen Radien. Verwendet lineare Filterung.                                  |
| D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ BALANCED | Verwendet dieselben Optimierungsschwellenwerte wie im Geschwindigkeitsmodus, verwendet jedoch die trilineare Filterung.                                                    |
| D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ QUALITY  | Verwendet nur interne Optimierungen mit großen weicheren Radien, bei denen Näherungen weniger wahrscheinlich sichtbar sind. Verwendet die trilineare Filterung. |



 

## <a name="border-modes"></a>Rahmenmodi



| Name                     | Beschreibung                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ BORDER \_ MODE \_ SOFT | Der Effekt padt das Bild mit transparenten schwarzen Pixeln, wenn der Weichheitskernel angewendet wird, was zu einem weichen Rand führt. <br/>                                                                                             |
| D2D1– \_ \_ RAHMENMODUS \_ FEST | Der Effekt klammert die Ausgabe an die Größe des Eingabebilds. Wenn der Effekt den weicheren Kernel an wendet, erweitert er das Eingabebild um eine Rahmentransformation vom Spiegeltyp für Stichproben außerhalb der Eingabegrenze.<br/> |



 

## <a name="output-bitmap"></a>Ausgabebitmap

Die Größe der Ausgabebitmap nimmt basierend auf der Standardabweichung, dem Winkel des Effekts und dem Rahmenmodus zu. Wenn der Rahmenmodus auf D2D1 BORDER MODE SOFT festgelegt ist, erhöht sich die Größe der Ausgabebitmap um die Größe des weicheren Kernels, dargestellt \_ \_ in \_ Pixel. Diese Gleichungen können verwendet werden, um die Größe der Ausgabebitmap zu berechnen.



| Anforderung | Wert |
|------------------------|-------------------------------------------------------------------|
| Output Bitmap Growth X | StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* cos(Angle)) |
| Output Bitmap Growth Y | StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* sin(Angle)) |



 

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

 

