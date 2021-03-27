---
title: Direct3D 11,3-Features
description: In den folgenden Abschnitten wird beschrieben, wie die Funktionalität in Direct3D 11,3 hinzugefügt wurde. Diese Features sind auch in Direct3D 12 verfügbar.
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc256b9b85dd807e2e6c923affdec496fe92e075
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391261"
---
# <a name="direct3d-113-features"></a>Direct3D 11,3-Features

In den folgenden Abschnitten wird beschrieben, wie die Funktionalität in Direct3D 11,3 hinzugefügt wurde. Diese Features sind auch in Direct3D 12 verfügbar.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Konservative Rasterung](conservative-rasterization.md)<br/>                             | Die konservative rasterisierung sorgt für ein gewisses Maß an Sicherheit für das Pixel Rendering. Dies ist insbesondere bei Algorithmen zum Erkennen von Kollisionen hilfreich.<br/>                                                                                                                                                                                                                                              |
| [Standard Textur Zuordnung](default-texture-mapping.md)<br/>                                   | Die Verwendung der standardtextur Zuordnung reduziert das Kopieren und die Arbeitsspeicher Auslastung bei der Freigabe von Bilddaten zwischen GPU und CPU. Es sollte jedoch nur in bestimmten Situationen verwendet werden. Das standardmäßige Swizzle-Layout vermeidet das Kopieren oder Schwenken von Daten in mehreren Layouts.<br/>                                                                                                               |
| [Reihen folgen Ansichten für Rasterizer](rasterizer-order-views.md)<br/>                                     | Mithilfe geordneter Ansichten von Rasterizer (ROVs) kann der Pixel-Shader-Code UAV-Bindungen mit einer Deklaration markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert. Dadurch können OIT-Algorithmen (Order Independent Transparenz) funktionieren, die deutlich bessere renderingergebnisse bieten, wenn mehrere transparente Objekte in einer Ansicht aufeinander zueinander stehen. <br/> |
| [Von Shader festgelegter Schablonenreferenzwert](shader-specified-stencil-reference-value.md)<br/> | Wenn Sie Pixel-Shader ermöglichen, den Schablonen Verweis Wert auszugeben, anstatt die API-Angabe zu verwenden, ist eine sehr präzise Steuerung von Schablone-Vorgängen möglich.<br/>                                                                                                                                                                                                              |
| [Typisierte nicht geordnete zugriffsansichts Ladungen](typed-unordered-access-view-loads.md)<br/>               | Die gegebene UAV-Auslastung (unsortierter Zugriffs Ansicht) ist die Fähigkeit eines Shaders, aus einer UAV mit einem bestimmten DXGI-Format zu lesen \_ .<br/>                                                                                                                                                                                                                                                               |
| [Einheitliche Speicherarchitektur](unified-memory-architecture.md)<br/>                           | Die Abfrage, ob eine einheitliche Speicherarchitektur (UMA) unterstützt wird, kann Ihnen dabei helfen zu bestimmen, wie einige Ressourcen behandelt werden.<br/>                                                                                                                                                                                                                                                              |
| [Menge gekachelter Ressourcen](volume-tiled-resources.md)<br/>                                     | Volumessourcen (3D) können als Kachel Ressourcen verwendet werden, wobei festgestellt wird, dass die Kachel Auflösung dreidimensional ist.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Neuerungen in Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





