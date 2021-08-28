---
description: 'Dieses Thema bietet zwei übergeordnete Ansichten der Architektur von Direct3D:'
ms.assetid: ed08b4c8-fdd9-46fb-a2be-c2fb15af2dc6
title: Direct3D-Architektur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d288cbf7896b276824f358364bede519e778375d1d3f8c9915108cbfadf8486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791489"
---
# <a name="direct3d-architecture-direct3d-9"></a>Direct3D-Architektur (Direct3D 9)

Dieses Thema bietet zwei übergeordnete Ansichten der Architektur von Direct3D:

-   [Direct3D-Grafikpipeline:](#direct3d-graphics-pipeline) Eine Ansicht der internen Verarbeitungsarchitektur des Direct3D-Renderingsystems.
-   [Direct3D-Systemintegration:](#direct3d-system-integration) Eine Ansicht, wie Direct3D zwischen einer Anwendung und der Grafikhardware vermittelt.

## <a name="direct3d-graphics-pipeline"></a>Direct3D-Grafikpipeline

Die Grafikpipeline bietet die Leistung, Direct3D-Szenen effizient zu verarbeiten und auf einer Anzeige zu rendern, wobei die Vorteile der verfügbaren Hardware genutzt werden. Das folgende Diagramm zeigt die Bausteine der Pipeline:

![Diagramm der Direct3d-Grafikpipeline](images/blockdiag-graphics.png)



| Pipelinekomponente  | Beschreibung                                                                                                                                                                                      | Verwandte Themen                                                                                                                                                                                             |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Scheitelpunktdaten         | Nicht transformierte Modellvertices werden in Vertexspeicherpuffern gespeichert.                                                                                                                                | [Vertexpuffer (Direct3D 9),](vertex-buffers.md) [ **IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)                                                                                                |
| Primitive Daten      | Auf geometrische Grundtypen, einschließlich Punkten, Linien, Dreiecken und Polygonen, wird in den Scheitelpunktdaten mit Indexpuffern verwiesen.                                                                    | [Indexpuffer (Direct3D 9),](index-buffers.md) [**IDirect3DIndexBuffer9,**](/windows/desktop/api) [Primitive,](primitives.md) [Primitive höherer Ordnung (Direct3D 9)](higher-order-primitives.md) |
| Mosaik        | Die Mosaikeinheit konvertiert Primitive höherer Ordnung, Verschiebungszuordnungen und Gitternetzpatches in Scheitelpunktpositionen und speichert diese Positionen in Scheitelpunktpuffern.                                      | [Mosaik (Direct3D 9)](tessellation.md)                                                                                                                                                              |
| Vertexverarbeitung   | Direct3D-Transformationen werden auf Scheitelpunkte angewendet, die im Scheitelpunktpuffer gespeichert sind.                                                                                                                    | [Vertexpipeline (Direct3D 9)](vertex-pipeline.md)                                                                                                                                                        |
| Geometrieverarbeitung | Clipping, Back Face Culling, Attributauswertung und Rasterung werden auf die transformierten Scheitelpunkte angewendet.                                                                                    | [Pixelpipeline (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Texturierte Oberfläche    | Texturkoordinaten für Direct3D-Oberflächen werden direct3D über die [**IDirect3DTexture9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) bereitgestellt.                                                         | [Direct3D Textures (Direct3D 9)](direct3d-textures.md), [ **IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)                                                                                                    |
| Textur-Sampler     | Die Filterung auf Texturebene wird auf Eingabetexturwerte angewendet.                                                                                                                            | [Direct3D-Texturen (Direct3D 9)](direct3d-textures.md)                                                                                                                                                    |
| Pixelverarbeitung    | Pixel-Shadervorgänge verwenden Geometriedaten, um Eingabevertex- und Texturdaten zu ändern und Ausgabepixelfarbwerte zu erhalten.                                                                           | [Pixelpipeline (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Pixelrendering     | Endgültige Renderingprozesse ändern Pixelfarbwerte mit Alpha-, Tiefen- oder Schablonentests oder durch Anwenden von Alphablending oder Blending. Alle resultierenden Pixelwerte werden der Ausgabeanzeige angezeigt. | [Pixelpipeline (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |



 

## <a name="direct3d-system-integration"></a>Direct3D-Systemintegration

Das folgende Diagramm zeigt die Beziehungen zwischen einer Window-Anwendung, Direct3D, GDI und der Hardware:

![Diagramm der Beziehung zwischen direct3d und anderen Systemkomponenten](images/d3dsysint.png)

Direct3D macht eine geräteunabhängige Schnittstelle für eine Anwendung verfügbar. Direct3D-Anwendungen können zusammen mit GDI-Anwendungen vorhanden sein, und beide haben über den Gerätetreiber für die Grafikkarte Zugriff auf die Grafikhardware des Computers. Im Gegensatz zu GDI kann Direct3D hardwarefeatures nutzen, indem ein -Gerät erstellt wird.

Ein Speichergerät bietet Hardwarebeschleunigung für Grafikpipelinefunktionen basierend auf dem von der Grafikkarte unterstützten Featuresatz. Direct3D-Methoden werden bereitgestellt, um Geräteanzeigefunktionen zur Laufzeit abzurufen. (Siehe [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).) Wenn eine Funktion nicht von der Hardware bereitgestellt wird, wird sie nicht als Hardwarefunktion berichtet.

Weitere Informationen zu -Geräten und Referenzgeräten, die von Direct3D unterstützt werden, finden Sie unter [Gerätetypen (Direct3D 9).](device-types.md)

## <a name="related-topics"></a>Zugehörige Themen

[Erste Schritte](getting-started.md)
