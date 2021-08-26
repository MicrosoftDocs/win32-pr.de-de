---
title: Gaußischer Weichreffekt
description: Verwenden Sie den Gaußschen Weichfunktionseffekt, um eine Weichfunktion zu erstellen, die auf der Gauß-Funktion für das gesamte Eingabebild basiert.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Gaußsche Weichde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b759ed0f5f70c4fc11ad902c7a45db3b3059847ce6895d25c3dbb9c9eee8330
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967084"
---
# <a name="gaussian-blur-effect"></a>Gaußischer Weichreffekt

Verwenden Sie den Gaußschen Weichfunktionseffekt, um eine Weichfunktion zu erstellen, die auf der Gauß-Funktion für das gesamte Eingabebild basiert.

Sie können diesen Effekt verwenden, um Leuchteffekten [](composite.md) und Schlagschatten zu erstellen und den zusammengesetzten Effekt zu verwenden, um das Ergebnis auf das ursprüngliche Bild anzuwenden. Dies ist nützlich bei der Fotoverarbeitung für Filter wie Highlights und Schatten. Sie können die Ausgabe dieses Effekts für die Eingabe in Beleuchtungseffekte wie [specular Lighting](specular-lighting.md) oder [Diffuse Lighting](diffuse-lighting.md) verwenden, da der Alphakanal ebenfalls unscharf ist und Beleuchtungseffekte den Alphakanal verwenden, um die Oberflächengeometrie als Höhenkarte zu bestimmen.

Dieser Effekt wird vom integrierten [Schatteneffekt](drop-shadow.md) verwendet.

Die CLSID für diesen Effekt ist CLSID \_ D2D1AuswertungssianBlur.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Optimierungsmodi](#optimization-modes)
-   [Rahmenmodi](#border-modes)
-   [Ausgabebitmap](#output-bitmap)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                       |
|--------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)   |
| Danach                                                        |
| ![das Bild nach der Transformation.](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation (Standardabweichung)<br/> D2D1 \_ GAUßSCHEBLUR-STANDARDABWEICHUNG \_ \_ \_<br/> | Die Auf das Bild anzuwendende Weichbildmenge. Sie können den Weichderadius des Kernels berechnen, indem Sie die Standardabweichung mit 3 multiplizieren. Die Einheiten der Standardabweichung und des Weicherradius sind DIPs. Ein Wert von 0 (null) DIPs deaktiviert diesen Effekt vollständig. Der Typ ist FLOAT.<br/> Der Standardwert ist 3,0f.<br/> |
| Optimization<br/> D2D1 \_ GAUßSSIANBLUR-PROP-OPTIMIERUNG \_ \_<br/>             | Der Optimierungsmodus. Weitere [Informationen finden Sie](#optimization-modes) unter Optimierungsmodi. Der Typ ist "D2D1 \_ GAUßSSIANBLUR \_ OPTIMIZATION".<br/> Der Standardwert ist D2D1 \_ GAUßSSIANBLUR \_ OPTIMIZATION \_ BALANCED.<br/>                                                                                                            |
| BorderMode<br/> D2D1 \_ GAUßSIANBLUR \_ \_ PROP-RAHMENMODUS \_<br/>               | Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, soft oder hard. Weitere [Informationen finden Sie](#border-modes) unter Rahmenmodi. <br/> Der Typ ist D2D1 \_ GAUßSSIANBLUR-RAHMENMODUS. \_ \_<br/> Der Standardwert ist D2D1 \_ BORDER \_ MODE \_ SOFT.<br/>                                                                                   |



 

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

Die Ausgabe dieses Effekts kann größer sein als die Eingabebitmap basierend auf dem Weicherradius und dem Rahmenmodus. Wenn der Rahmenmodus auf D2D1 BORDER MODE SOFT festgelegt ist, erhöht sich die Größe der Ausgabebitmap um die Größe des weicheren Kernels, dargestellt \_ \_ in \_ Pixel. Diese Tabelle enthält eine Gleichung, mit der Sie die Ausgabebitmap berechnen können.

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

Wenn sich die Bildgröße also in jeder Richtung um 10 Pixel erhöht, befindet sich die obere linke Ecke des Bilds bei (-5, -5), während die untere rechte Seite bei (105, 105) liegt.

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

 

