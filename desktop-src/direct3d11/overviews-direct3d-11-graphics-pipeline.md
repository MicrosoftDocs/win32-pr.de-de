---
title: Grafikpipeline
description: In diesem Abschnitt wird die programmierbare Direct3D 11-Pipeline beschrieben.
ms.assetid: 8e7a6f64-0a2b-4ea5-a6a6-7bfb87e27dcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b3872fbfaf63a53a07c8c06246088a5eec1791f98be867adbe56ae1d9c7724
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565570"
---
# <a name="graphics-pipeline"></a>Grafikpipeline

Die programmierbare Direct3D 11-Pipeline ist für die Generierung von Grafiken für Echtzeit-Gaminganwendungen konzipiert. In diesem Abschnitt wird die programmierbare Direct3D 11-Pipeline beschrieben. Das folgende Diagramm zeigt den Datenfluss von der Eingabe zur Ausgabe durch jede der programmierbaren Phasen.

![Diagramm des Datenflusses in der programmierbaren Direct3d 11-Pipeline](images/d3d11-pipeline-stages.jpg)

Die Grafikpipeline für Microsoft Direct3D 11 unterstützt die gleichen Phasen wie die [Direct3D 10-Grafikpipeline](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)mit zusätzlichen Phasen zur Unterstützung erweiterter Features.

Sie können Direct3D 11API verwenden, um alle Phasen zu konfigurieren. Phasen, die allgemeine Shaderkerne (die abgerundeten rechteckigen Blöcke) verwenden, können mithilfe der [HLSL-Programmiersprache](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) programmiert werden. Wie Sie sehen werden, ist die Pipeline dadurch äußerst flexibel und anpassbar.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Eingabe-Assembler-Phase](d3d10-graphics-programming-guide-input-assembler-stage.md)<br/> | Die Direct3D 10- und höhere API trennt Funktionsbereiche der Pipeline in Phasen. Die erste Phase in der Pipeline ist die IA-Phase (Input-Assembler).<br/>                                                                                                                                                                                                                                                                                                                             |
| [Vertex-Shaderphase](vertex-shader-stage.md)<br/>                                      | Die Vertex-Shader-Phase (VS) verarbeitet Scheitelpunkte aus dem Eingabe-Assembler und verarbeitet scheitelpunktspezifische Vorgänge wie Transformationen, Skinning, Morphing und Beleuchtung pro Scheitelpunkt. Vertex-Shader arbeiten immer mit einem einzelnen Eingabevertex und erzeugen einen einzelnen Ausgabevertex. Die Vertex-Shaderphase muss immer aktiv sein, damit die Pipeline ausgeführt werden kann. Wenn keine Scheitelpunktänderung oder -transformation erforderlich ist, muss ein Pass-Through-Vertex-Shader erstellt und auf die Pipeline festgelegt werden.<br/> |
| [Mosaikstufen](direct3d-11-advanced-stages-tessellation.md)<br/>                 | Die Direct3D 11-Runtime unterstützt drei neue Phasen, die Mosaik implementieren, wodurch Unterteilungsoberflächen mit geringem Detail in primitivere Detailtypen auf der GPU konvertiert werden. Mosaikkacheln (oder unterbricht) hochwertige Oberflächen in geeignete Strukturen für das Rendering.<br/>                                                                                                                                                                                                                 |
| [Geometry Shader Stage](geometry-shader-stage.md)<br/>                                  | Die Geometry-Shader-Phase (GS) führt anwendungsspezifischen Shadercode mit Scheiteltices als Eingabe und der Möglichkeit aus, Scheitelungen bei der Ausgabe zu generieren.<br/>                                                                                                                                                                                                                                                                                                                                          |
| [Streamausgabephase](d3d10-graphics-programming-guide-output-stream-stage.md)<br/>     | Der Zweck der Streamausgabephase besteht in der kontinuierlichen Ausgabe (oder dem Streamen) von Scheitelpunktdaten aus der Geometry-Shader-Stufe (oder der Vertex-Shader-Stufe, wenn die Geometry-Shader-Phase inaktiv ist) in mindestens einem Puffer im Arbeitsspeicher (siehe Erste Schritte mit [der Stream-Output-Phase).](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md) <br/>                                                                                                                       |
| [Stufe des Rasterizers](d3d10-graphics-programming-guide-rasterizer-stage.md)<br/>           | Die Rasterungsphase konvertiert Vektorinformationen (bestehend aus Formen oder Primitiven) in ein Rasterbild (bestehend aus Pixeln), um 3D-Echtzeitgrafiken anzuzeigen. <br/>                                                                                                                                                                                                                                                                                                 |
| [Pixel-Shader-Stufe](pixel-shader-stage.md)<br/>                                        | Die Pixel-Shader-Stufe (PIXEL-Shader Stage, PS) ermöglicht umfassende Schattierungstechniken, z. B. Beleuchtung pro Pixel und Nachbearbeitung. Ein Pixel-Shader ist ein Programm, das konstante Variablen, Texturdaten, interpolierte Werte pro Scheitelpunkt und andere Daten kombiniert, um Ausgaben pro Pixel zu erzeugen. Die Rasterizerphase ruft einen Pixel-Shader einmal für jedes Pixel auf, das  von einem Primitiv abgedeckt wird. Es ist jedoch möglich, einen NULL-Shader anzugeben, um die Ausführung eines Shaders zu vermeiden.<br/>                                          |
| [Ausgabe-Merger-Phase](d3d10-graphics-programming-guide-output-merger-stage.md)<br/>     | Die Ausgabe-Merger-Phase (OM) generiert die endgültige gerenderte Pixelfarbe mithilfe einer Kombination aus Pipelinezustand, den von den Pixel-Shadern generierten Pixeldaten, dem Inhalt der Renderziele und dem Inhalt der Tiefen-/Schablonenpuffer. Die OM-Phase ist der letzte Schritt zum Bestimmen der sichtbaren Pixel (mit Tiefen-Schablonentests) und zum Mischen der endgültigen Pixelfarben.<br/>                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Compute-Shader](direct3d-11-advanced-stages-compute-shader.md)
</dt> <dt>

[Programmieranleitung für Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

