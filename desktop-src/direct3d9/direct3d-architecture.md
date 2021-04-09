---
description: 'Dieses Thema enthält zwei allgemeine Ansichten der Architektur von Direct3D:'
ms.assetid: ed08b4c8-fdd9-46fb-a2be-c2fb15af2dc6
title: Direct3D-Architektur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e557b7a36aadcaa8b96899047a721741ecef2156
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124501"
---
# <a name="direct3d-architecture-direct3d-9"></a>Direct3D-Architektur (Direct3D 9)

Dieses Thema enthält zwei allgemeine Ansichten der Architektur von Direct3D:

-   [Direct3D graphics Pipeline](#direct3d-graphics-pipeline) : eine Ansicht der internen Verarbeitungs Architektur des Direct3D-Renderingsystems.
-   [Direct3D System Integration](#direct3d-system-integration) : eine Ansicht, wie Direct3D zwischen einer Anwendung und der Grafikhardware mediiert.

## <a name="direct3d-graphics-pipeline"></a>Direct3D-Grafik Pipeline

Die Grafik Pipeline ermöglicht die effiziente Verarbeitung und renderingDirect3D Szenen in einer Anzeige und nutzt die verfügbare Hardware. Das folgende Diagramm zeigt die Bausteine der Pipeline:

![Diagramm der Direct3D-Grafik Pipeline](images/blockdiag-graphics.png)



| Pipeline Komponente  | BESCHREIBUNG                                                                                                                                                                                      | Verwandte Themen                                                                                                                                                                                             |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Scheitelpunkt Daten         | Nicht transformierte Modell Scheitel Punkte werden in Scheitelpunkt Speicher Puffern gespeichert.                                                                                                                                | [Vertex-Puffer (Direct3D 9)](vertex-buffers.md), [ **IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)                                                                                                |
| Primitive Daten      | Auf geometrische Primitive, einschließlich Punkten, Linien, Dreiecke und Polygone, wird in den Scheitelpunkt Daten mit Index Puffern verwiesen.                                                                    | [Index Puffer (Direct3D 9)](index-buffers.md), [**IDirect3DIndexBuffer9**](/windows/desktop/api), [primitive](primitives.md), [höherwertige primitive (Direct3D 9)](higher-order-primitives.md) |
| Mosaik        | Die tesselator-Einheit konvertiert primitive in höherer Reihenfolge, Verschiebungs Zuordnungen und mespatches in Scheitelpunkt Positionen und speichert diese Speicherorte in Scheitelpunkt Puffern.                                      | [Mosaik (Direct3D 9)](tessellation.md)                                                                                                                                                              |
| Vertexverarbeitung   | Direct3D-Transformationen werden auf Vertices angewendet, die im Vertex-Puffer gespeichert sind.                                                                                                                    | [Scheitelpunkt Pipeline (Direct3D 9)](vertex-pipeline.md)                                                                                                                                                        |
| Geometrie Verarbeitung | Clipping, Hintergrund-Culling, Attribut Auswertung und rasterisierung werden auf die transformierten Scheitel Punkte angewendet.                                                                                    | [Pixel Pipeline (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Strukturierte Oberfläche    | Texturkoordinaten für Direct3D-Oberflächen werden für Direct3D über die [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle bereitgestellt.                                                         | [Direct3D Texturen (Direct3D 9)](direct3d-textures.md), [ **IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)                                                                                                    |
| Textur Sampler     | Die Textur Ebene der Detail Filterung wird auf Eingabe Textur Werte angewendet.                                                                                                                            | [Direct3D-Texturen (Direct3D 9)](direct3d-textures.md)                                                                                                                                                    |
| Pixel Verarbeitung    | Pixel-Shader-Vorgänge verwenden Geometry-Daten, um die Vertex-und Textur Daten der Eingabe zu ändern, sodass Ausgabe Pixel-Farbwerte                                                                           | [Pixel Pipeline (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Pixel Rendering     | Abschließende renderingprozesse ändern Pixel Farbwerte durch Alpha, Tiefe oder Schablonen Tests oder durch Anwenden von Alpha Mischungen oder Nebel. Alle resultierenden Pixelwerte werden der Ausgabe Anzeige angezeigt. | [Pixel Pipeline (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |



 

## <a name="direct3d-system-integration"></a>Direct3D-System Integration

Das folgende Diagramm zeigt die Beziehungen zwischen einer Fenster Anwendung, Direct3D, GDI und der Hardware:

![Diagramm der Beziehung zwischen Direct3D und anderen Systemkomponenten](images/d3dsysint.png)

Direct3D macht eine geräteunabhängige Schnittstelle für eine Anwendung verfügbar. Direct3D-Anwendungen können neben GDI-Anwendungen vorhanden sein, und beide haben Zugriff auf die Grafikhardware des Computers über den Gerätetreiber für die Grafikkarte. Im Gegensatz zu GDI können Direct3D die Hardware Features nutzen, indem Sie ein HAL-Gerät erstellen.

Ein HAL-Gerät ermöglicht die Hardwarebeschleunigung an Grafik Pipeline Funktionen, basierend auf der von der Grafikkarte unterstützten featuremenge. Direct3D-Methoden werden bereitgestellt, um zur Laufzeit Geräte Anzeigefunktionen abzurufen. (Siehe [**IDirect3DDevice9:: getde vicecaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).) Wenn eine Funktion nicht von der Hardware bereitgestellt wird, wird Sie von der HAL nicht als Hardware Funktion gemeldet.

Weitere Informationen zu hal und Referenz Geräten, die von Direct3D unterstützt werden, finden Sie unter [Gerätetypen (Direct3D 9)](device-types.md).

## <a name="related-topics"></a>Zugehörige Themen

[Erste Schritte](getting-started.md)
