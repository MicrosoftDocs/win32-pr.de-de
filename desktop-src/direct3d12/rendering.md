---
title: Rendering (Direct3D 12-Grafiken)
description: Dieser Abschnitt enthält Informationen zu den Renderingfunktionen, die für Direct3D 12 (und Direct3D 11,3) neu sind.
ms.assetid: 5BF1440E-E4D8-43C8-BF0E-F02FEFE79C93
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ad70a054881e9472ff27a76a62dca62fdf3653
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548716"
---
# <a name="rendering-direct3d-12-graphics"></a>Rendering (Direct3D 12-Grafiken)

Dieser Abschnitt enthält Informationen zu den Renderingfunktionen, die für Direct3D 12 (und Direct3D 11,3) neu sind.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                               | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Konservative rasterisierung](conservative-rasterization.md)<br/>                             | Die konservative rasterisierung sorgt für ein gewisses Maß an Sicherheit für das Pixel Rendering. Dies ist insbesondere bei Algorithmen zum Erkennen von Kollisionen hilfreich.<br/>                                                                                                                                                                                                                                              |
| [Indirektes zeichnen](indirect-drawing.md)<br/>                                                 | Indirektes zeichnen ermöglicht das Verschieben von Szenen Durchlauf und-Daten aus der CPU auf die GPU, wodurch die Leistung verbessert werden kann. Der Befehls Puffer kann von der CPU oder GPU generiert werden.<br/>                                                                                                                                                                                              |
| [Geordnete Ansichten des Rasterizers](rasterizer-order-views.md)<br/>                                   | Mithilfe geordneter Ansichten von Rasterizer (ROVs) kann der Pixel-Shader-Code UAV-Bindungen mit einer Deklaration markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert. Dadurch können OIT-Algorithmen (Order Independent Transparenz) funktionieren, die deutlich bessere renderingergebnisse bieten, wenn mehrere transparente Objekte in einer Ansicht aufeinander zueinander stehen. <br/> |
| [Von Shader angegebener Schablone-Verweis Wert](shader-specified-stencil-reference-value.md)<br/> | Wenn Sie Pixel-Shader ermöglichen, den Schablonen Verweis Wert auszugeben, anstatt die API-Angabe zu verwenden, ist eine sehr präzise Steuerung von Schablone-Vorgängen möglich.<br/>                                                                                                                                                                                                              |
| [Austausch Ketten](swap-chains.md)<br/>                                                           | Austausch Ketten steuern die Hintergrund Puffer Drehung und bilden die Grundlage der Grafik Animation.<br/>                                                                                                                                                                                                                                                                                            |



 

Die folgenden Themen sind ebenfalls neu in Direct3D 12 und Direct3D 11,3:

-   [Standard Textur Zuordnung](default-texture-mapping.md)
-   [Typisierte nicht geordnete zugriffsansichts Ladungen](typed-unordered-access-view-loads.md)
-   [Menge an Kacheln](volume-tiled-resources.md)

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Hoher dynamischer Bereich und breite Farbpalette

Weitere Informationen finden Sie unter Unterstützung für einen hohen dynamischen Bereich (erhöhter Unterschied zwischen den hellsten weißen und den dunkelsten schwarzen) und der Breite der Farbpalette (10 Bits, anstelle von 8 Bits, pro Farbe), die unter [DXGI 1,5-Verbesserungen](/windows/desktop/direct3ddxgi/dxgi-1-5-improvements)beschrieben werden.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Direct3D 12-Programmier Handbuch](directx-12-programming-guide.md)
</dt> </dl>

 

