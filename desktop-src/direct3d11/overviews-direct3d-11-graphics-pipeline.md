---
title: Grafik Pipeline
description: In diesem Abschnitt wird die programmierbare Pipeline Direct3D 11 beschrieben.
ms.assetid: 8e7a6f64-0a2b-4ea5-a6a6-7bfb87e27dcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8e6b0b4d249c46dafe960f4f25a9a7598d6e2c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391236"
---
# <a name="graphics-pipeline"></a>Grafik Pipeline

Die programmierbare Pipeline Direct3D 11 dient zum Erstellen von Grafiken für echt Zeit Spiele Anwendungen. In diesem Abschnitt wird die programmierbare Pipeline Direct3D 11 beschrieben. Das folgende Diagramm zeigt den Datenfluss von der Eingabe zur Ausgabe in den einzelnen programmierbaren Phasen.

![Diagramm des Datenflusses in der programmierbaren Direct3D 11-Pipeline](images/d3d11-pipeline-stages.jpg)

Die Grafik Pipeline für Microsoft Direct3D 11 unterstützt die gleichen Phasen wie die [Direct3D 10-Grafik Pipeline](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)mit zusätzlichen Stufen, um erweiterte Funktionen zu unterstützen.

Sie können die Direct3D 11-API verwenden, um alle Phasen zu konfigurieren. Phasen mit allgemeinen shaderkernen (die abgerundeten rechteckigen Blöcke) können mithilfe der [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) -Programmiersprache Programmiersprache verwendet werden. Wie Sie sehen werden, ist die Pipeline äußerst flexibel und anpassbar.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Eingabe-Assembler-Phase](d3d10-graphics-programming-guide-input-assembler-stage.md)<br/> | Die API Direct3D 10 und höher trennt funktionale Bereiche der Pipeline in Phasen. die erste Phase in der Pipeline ist die Eingabe-Assembler-Phase (IA).<br/>                                                                                                                                                                                                                                                                                                                             |
| [Vertex-Shader-Phase](vertex-shader-stage.md)<br/>                                      | Die Vertex-Shader (VS)-Phase verarbeitet Scheitel Punkte vom Eingabe Assembler und führt Vorgänge pro Scheitelpunkt aus, z. b. Transformationen, Skinning, morphung und pro-Vertex-Beleuchtung. Vertex-Shader arbeiten immer auf einem einzelnen Eingabe Scheitelpunkt und liefern einen einzelnen Ausgabe Scheitelpunkt. Die Vertex-Shader-Stufe muss immer aktiv sein, damit die Pipeline ausgeführt werden muss. Wenn keine Scheitelpunkt Änderung oder-Transformation erforderlich ist, muss ein Pass-Through-Vertex-Shader erstellt und auf die Pipeline festgelegt werden.<br/> |
| [Mosaik Phasen](direct3d-11-advanced-stages-tessellation.md)<br/>                 | Die Direct3D 11-Laufzeit unterstützt drei neue Phasen, die das Mosaik implementieren, das untergeordnete Oberflächen auf niedriger Detailebene in die GPU konvertiert. Mosaik Kacheln (oder unterbrechen) hoch geordnete Oberflächen in geeignete Strukturen zum Rendern.<br/>                                                                                                                                                                                                                 |
| [Geometry-Shader-Phase](geometry-shader-stage.md)<br/>                                  | Die Geometry-Shader-Phase (GS) führt den von der Anwendung angegebenen Shader-Code mit Vertices als Eingabe und die Möglichkeit zum Generieren von Scheitel Punkten bei der Ausgabe aus.<br/>                                                                                                                                                                                                                                                                                                                                          |
| [Stream-Ausgabe Phase](d3d10-graphics-programming-guide-output-stream-stage.md)<br/>     | Der Zweck der Stream-Output-Phase besteht darin, Vertexdaten fortlaufend aus der Geometrie-Shader-Stufe (oder der Vertex-Shader-Phase, wenn die Geometrie-shaderstufe inaktiv ist) in einen oder mehrere Puffer im Arbeitsspeicher auszugeben (oder zu streamen) (Weitere Informationen finden Sie unter [Getting Started with the Stream-Output Stage](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)). <br/>                                                                                                                       |
| [Stufe des Rasterizers](d3d10-graphics-programming-guide-rasterizer-stage.md)<br/>           | Die Rasterung-Phase konvertiert Vektor Informationen (bestehend aus Formen oder primitiven) in ein Rasterbild (bestehend aus Pixeln), um Echt Zeit 3D-Grafiken anzuzeigen. <br/>                                                                                                                                                                                                                                                                                                 |
| [Pixel-Shader-Phase](pixel-shader-stage.md)<br/>                                        | Die Pixel-Shader-Stufe (PS) ermöglicht umfassende Schattierungs Techniken wie z. b. pro Pixel-Beleuchtung und Nachbearbeitung. Ein Pixelshader ist ein Programm, das Konstante Variablen, Textur Daten, interpoliert pro Scheitelpunkt Werte und andere Daten kombiniert, um pro-Pixel-Ausgaben zu liefern. Die Raster-Stufe Ruft einen Pixel-Shader einmal für jedes Pixel auf, das von einem primitiven abgedeckt wird. es ist jedoch möglich, einen **null** -Shader anzugeben, um das Ausführen eines Shaders zu vermeiden.<br/>                                          |
| [Ausgabe-Fusion-Phase](d3d10-graphics-programming-guide-output-merger-stage.md)<br/>     | In der Output-Fusion (OM)-Phase wird die endgültige gerenderte Pixelfarbe mithilfe einer Kombination aus dem Pipeline Status, den von den Pixel-Shadern generierten Pixeldaten, dem Inhalt der Renderingziele und dem Inhalt der tiefen/Schablonen Puffer generiert. Der OM-Schritt ist der letzte Schritt, um zu bestimmen, welche Pixel sichtbar sind (mit tiefen Schablone-Tests) und wie die endgültigen Pixel Farben gemischt werden.<br/>                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Compute-Shader](direct3d-11-advanced-stages-compute-shader.md)
</dt> <dt>

[Programmieranleitung für Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

