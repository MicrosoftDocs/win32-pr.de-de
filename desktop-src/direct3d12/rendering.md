---
title: Rendering (Direct3D 12-Grafiken)
description: Dieser Abschnitt enthält Informationen zu Renderingfunktionen, die in Direct3D 12 (und Direct3D 11.3) neu sind.
ms.assetid: 5BF1440E-E4D8-43C8-BF0E-F02FEFE79C93
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c1abb8e8d1d645149652e5c1cd429fb4e4b2e0b1e079eda13956f5ab8279b3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123467"
---
# <a name="rendering-direct3d-12-graphics"></a>Rendering (Direct3D 12-Grafiken)

Dieser Abschnitt enthält Informationen zu Renderingfunktionen, die in Direct3D 12 (und Direct3D 11.3) neu sind.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                               | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Konservative Rasterung](conservative-rasterization.md)<br/>                             | Die konservative Rasterung erhöht die Sicherheit beim Pixelrendering, was insbesondere bei Algorithmen zur Erkennung von Kollisionen hilfreich ist.<br/>                                                                                                                                                                                                                                              |
| [Indirektes Zeichnen](indirect-drawing.md)<br/>                                                 | Indirektes Zeichnen ermöglicht das Verschoben von Szenendurchlauf und Culling von der CPU zur GPU, wodurch die Leistung verbessert werden kann. Der Befehlspuffer kann von der CPU oder GPU generiert werden.<br/>                                                                                                                                                                                              |
| [Geordnete Rasterizeransichten](rasterizer-order-views.md)<br/>                                   | Rasterizer-geordnete Ansichten (ROVs) ermöglichen es Pixel-Shadercode, UAV-Bindungen mit einer Deklaration zu markieren, die die normalen Anforderungen für die Reihenfolge der Grafikpipelineergebnisse für UAVs ändert. Dies ermöglicht die Funktion von OIT-Algorithmen (Order Independent Transparency), die wesentlich bessere Renderingergebnisse liefern, wenn mehrere transparente Objekte in einer Ansicht miteinander in Einklang stehen. <br/> |
| [Von Shader festgelegter Schablonenreferenzwert](shader-specified-stencil-reference-value.md)<br/> | Wenn Pixel-Shader den Schablonenverweiswert anstelle des von der API angegebenen Werts aus geben, wird eine sehr präzise Steuerung von Schablonenvorgängen ermöglicht.<br/>                                                                                                                                                                                                              |
| [Swapchains](swap-chains.md)<br/>                                                           | Austauschketten steuern die Hintergrundpufferrotation und bilden die Grundlage der Grafikanimation.<br/>                                                                                                                                                                                                                                                                                            |



 

Die folgenden Themen sind auch neu in Direct3D 12 und Direct3D 11.3:

-   [Standardtexturzuordnung](default-texture-mapping.md)
-   [Typierte ungeordnete Zugriffsansichtslasten](typed-unordered-access-view-loads.md)
-   [Menge gekachelter Ressourcen](volume-tiled-resources.md)

## <a name="high-dynamic-range-and-wide-color-gamut"></a>High Dynamic Range und Breite Farbskala

Weitere Informationen finden Sie in der Unterstützung für High Dynamic Range (erhöhter Unterschied zwischen den hellsten weißen und dunkelsten Schwarzen) und Wide Color Gamut (10 Bits anstelle von 8 Bits pro Farbe), die in [DXGI 1.5 Improvements](/windows/desktop/direct3ddxgi/dxgi-1-5-improvements)beschrieben sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 12-Programmieranleitung](directx-12-programming-guide.md)
</dt> </dl>

 

