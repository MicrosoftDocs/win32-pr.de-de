---
title: Stufe des Rasterizers
description: Die Rasterung-Phase konvertiert Vektor Informationen (bestehend aus Formen oder primitiven) in ein Rasterbild (bestehend aus Pixeln), um Echt Zeit 3D-Grafiken anzuzeigen.
ms.assetid: efd3f819-7c63-4e1a-9923-8e7198354ec6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e746c5ace3512f36f9b9ad34d34a3ea578e1de36
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949248"
---
# <a name="rasterizer-stage"></a>Stufe des Rasterizers

Die Rasterung-Phase konvertiert Vektor Informationen (bestehend aus Formen oder primitiven) in ein Rasterbild (bestehend aus Pixeln), um Echt Zeit 3D-Grafiken anzuzeigen.

Während der rasterisierung wird jedes primitive in Pixel konvertiert, während pro-Scheitelpunkt Werte zwischen den einzelnen primitiven interpolieren werden. Die rasterisierung umfasst Clipping-Scheitel Punkte für die Ansicht "Frustum", eine Division durch z, um Perspektiven bereitzustellen, primitive einem 2D-Viewport zuzuordnen und zu bestimmen, wie der Pixelshader aufgerufen wird. Die Verwendung eines Pixelshaders ist optional, aber die Raster-Stufe führt immer Clipping aus, eine perspektivische Teilung zum Transformieren der Punkte in homogenen Raum und ordnet die Scheitel Punkte dem Viewport zu.

Bei Scheitel Punkten (x, y, z, w), die sich in der Raster-Phase befinden, wird davon ausgegangen, dass es sich um einen homogenen Clip Bereich handelt. In diesem Koordinaten Bereich zeigt die X-Achse nach rechts, Y zeigt nach oben und Z Punkte von der Kamera.

Sie können die rasterisierung deaktivieren, indem Sie der Pipeline mitteilen, dass kein Pixelshader vorhanden ist (legen Sie die Pixel-Shader-Phase mit [**Verknüpfung id3d11devicecontext aus::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)auf **null** fest), und deaktivieren Sie Tiefe und Schablonen Tests (legen Sie **depthenable** und **stencilenable** auf **false** in der [**D3D11- \_ tiefen \_ Schablone \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)) fest. Wenn die Rasterung deaktiviert ist, werden damit zusammenhängende Pipelinezähler nicht aktualisiert. Außerdem gibt es eine umfassende Beschreibung der [rasterisierungsregeln](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).

Auf Hardware, die hierarchische Z-Puffer Optimierungen implementiert, können Sie das vorab Laden des z-Puffers aktivieren, indem Sie die Pixel-Shader-Stufe auf **null** festlegen, während Sie Tiefe und Schablonen Tests aktivieren.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Einstieg in die Rasterizer-Phase](d3d10-graphics-programming-guide-rasterizer-stage-getting-started.md)<br/> | In diesem Abschnitt wird das Festlegen des Viewports, des Scheren Rechtecks, des Status des Rasterizers und der mehrfach Stichproben Erstellung beschrieben.<br/>                                                                                                                                                                                                |
| [Rasterisierungsregeln](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)<br/>                                 | Rasterisierungsregeln definieren, wie Vektordaten in Rasterdaten zugeordnet werden. Die Rasterdaten werden an ganzzahlige Speicherorte angedockt, die dann durch ein-und abgeschnitten werden (um die Mindestanzahl von Pixeln zu zeichnen), und pro Pixel-Attribute werden interpoliert (von pro-Vertex-Attributen), bevor Sie an einen PixelShader übergeben werden.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafik Pipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipeline Stufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

