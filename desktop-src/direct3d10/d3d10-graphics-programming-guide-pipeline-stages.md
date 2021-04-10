---
description: Die programmierbare Pipeline Direct3D 10 dient zum Erstellen von Grafiken für echt Zeit Spiele Anwendungen. Das folgende Diagramm zeigt den Datenfluss von der Eingabe zur Ausgabe in den einzelnen programmierbaren Phasen.
ms.assetid: 3ead6c7c-c7cc-48f1-81d5-b4b67326d610
title: Pipeline Stufen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78bf6e904051fcac255a5bf1b99ca0f7d43ca3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126559"
---
# <a name="pipeline-stages-direct3d-10"></a>Pipeline Stufen (Direct3D 10)

Die programmierbare Pipeline Direct3D 10 dient zum Erstellen von Grafiken für echt Zeit Spiele Anwendungen. Das folgende Diagramm zeigt den Datenfluss von der Eingabe zur Ausgabe in den einzelnen programmierbaren Phasen.

![Diagramm des Datenflusses in der programmierbaren Direct3D 10-Pipeline](images/d3d10-pipeline-stages.png)

Alle Stufen können mithilfe der-API konfiguriert werden. Phasen mit allgemeinen shaderkernen (die abgerundeten rechteckigen Blöcke) können mithilfe der HLSL-Programmiersprache programmiert werden. Wie Sie sehen werden, ist die Pipeline äußerst flexibel und anpassbar. Der Zweck der einzelnen Stufen ist unten aufgeführt.

-   [Eingabe-Assembler-Phase](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) : die Eingabe-Assembler-Phase ist für die Bereitstellung von Daten (Dreiecke, Linien und Punkten) an die Pipeline zuständig.
-   [Vertex-Shader-Stufe](https://www.bing.com/search?q=Vertex-Shader+Stage). Die Vertex-Shader-Stufe verarbeitet Scheitelpunkte und führt dabei in der Regel Vorgänge wie Transformationen, das Anwenden von Skins und Beleuchtung aus. Ein Vertex-Shader verarbeitet immer einen einzigen Eingabescheitelpunkt und erzeugt daraus einen einzigen Ausgabescheitelpunkt.
-   [Geometry-Shader-Stufe](https://www.bing.com/search?q=Geometry-Shader+Stage) : die Geometry-Shader-Stufe verarbeitet ganze primitive. Die Eingabe ist ein vollständiger primitiver Typ (bei dem es sich um drei Vertices für ein Dreieck, zwei Scheitel Punkte für eine Linie oder einen einzelnen Scheitelpunkt handelt). Darüber hinaus kann jedes primitive auch die Scheitelpunkt Daten für beliebige Rand angrenzende primitive enthalten. Dies kann höchstens einen zusätzlichen drei Scheitel Punkte für ein Dreieck oder eine zusätzliche zwei Scheitel Punkte für eine Linie enthalten. Der Geometry-Shader unterstützt auch die eingeschränkte Geometrie Verstärkung und die Aufhebung der deverstärkung. Wenn ein Eingabe primitiv angegeben ist, kann der Geometry-Shader den primitiven verwerfen oder eine oder mehrere neue primitive ausgeben.
-   [Stream-Output-Phase](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md) : die Stream-Output-Phase dient zum Streamen primitiver Daten aus der Pipeline in den Arbeitsspeicher auf der Grundlage des Rasterizers. Daten können "ausgestreamt" und/oder in den Rasterizer übergeben werden. In den Arbeitsspeicher gestreamte Daten können als Eingabedaten wieder der Pipeline zugeführt oder von der CPU eingelesen werden.
-   [Raster-Stufe](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md) : der Raster ist verantwortlich für das Abschneiden von primitiven, das Vorbereiten von primitiven für den Pixelshader und das Festlegen des Aufrufs von Pixel-Shadern.
-   [Pixelshader-Stufe](https://www.bing.com/search?q=Pixel-Shader+Stage). Die Pixelshader-Stufe empfängt interpolierte Daten für einen Grundtyp und generiert Pro-Pixel-Daten (z. B. die Farbe).
-   [Ausgabe-Fusion-Phase](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) : die Phase "Output-Merger" ist für die Kombination verschiedener Arten von Ausgabedaten (Pixel-shaderwerte, tiefen-und Schablonen Informationen) mit dem Inhalt des Renderziels und der tiefen/Schablonen Puffer zum Generieren des endgültigen Pipeline Ergebnisses verantwortlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
