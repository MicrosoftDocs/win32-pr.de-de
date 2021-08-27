---
description: Die programmierbare Direct3D 10-Pipeline ist für die Generierung von Grafiken für Echtzeit-Gaminganwendungen konzipiert. Das folgende Diagramm zeigt den Datenfluss von der Eingabe zur Ausgabe durch jede der programmierbaren Phasen.
ms.assetid: 3ead6c7c-c7cc-48f1-81d5-b4b67326d610
title: Pipelinestufen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942e2594f1f2eeb83f92b3ee517804a68b6074d85bf5c9205828a08e024112df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119975"
---
# <a name="pipeline-stages-direct3d-10"></a>Pipelinestufen (Direct3D 10)

Die programmierbare Direct3D 10-Pipeline ist für die Generierung von Grafiken für Echtzeit-Gaminganwendungen konzipiert. Das folgende Diagramm zeigt den Datenfluss von der Eingabe zur Ausgabe durch jede der programmierbaren Phasen.

![Diagramm des Datenflusses in der programmierbaren Direct3d 10-Pipeline](images/d3d10-pipeline-stages.png)

Alle Phasen können mithilfe der API konfiguriert werden. Phasen mit gängigen Shaderkernen (die abgerundeten rechteckigen Blöcke) können mithilfe der HLSL-Programmiersprache programmiert werden. Wie Sie sehen werden, ist die Pipeline dadurch äußerst flexibel und anpassbar. Der Zweck der einzelnen Phasen ist unten aufgeführt.

-   [Eingabe-Assembler-Stufe:](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) Die Eingabe-Assembler-Stufe ist für die Bereitstellung von Daten (Dreiecke, Linien und Punkte) für die Pipeline verantwortlich.
-   [Vertex-Shader-Stufe](https://www.bing.com/search?q=Vertex-Shader+Stage). Die Vertex-Shader-Stufe verarbeitet Scheitelpunkte und führt dabei in der Regel Vorgänge wie Transformationen, das Anwenden von Skins und Beleuchtung aus. Ein Vertex-Shader verarbeitet immer einen einzigen Eingabescheitelpunkt und erzeugt daraus einen einzigen Ausgabescheitelpunkt.
-   [Geometry-Shader-Phase:](https://www.bing.com/search?q=Geometry-Shader+Stage) Die Geometry-Shader-Stufe verarbeitet ganze Primitive. Die Eingabe ist ein vollständiger Grundtyp (drei Scheitelpunkte für ein Dreieck, zwei Scheitelpunkte für eine Linie oder ein einzelner Scheitelpunkt für einen Punkt). Darüber hinaus kann jede Primitive auch die Scheitelpunktdaten für alle an den Rand angrenzenden Primitiven enthalten. Dies kann bis zu drei weitere Scheitelungen für ein Dreieck oder zwei weitere Scheitelstriche für eine Linie umfassen. Der Geometrie-Shader unterstützt auch eingeschränkte Geometrievergrößerung und -entschärfung. Bei einer Eingabeprimitive kann der Geometry-Shader den Primitiven verwerfen oder einen oder mehrere neue Primitive aus geben.
-   [Streamausgabephase:](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md) Die Streamausgabephase ist für das Streamen primitiver Daten aus der Pipeline in den Arbeitsspeicher auf dem Weg zum Rasterizer konzipiert. Daten können "ausgestreamt" und/oder in den Rasterizer übergeben werden. In den Arbeitsspeicher gestreamte Daten können als Eingabedaten wieder der Pipeline zugeführt oder von der CPU eingelesen werden.
-   [Rasterizer-Stufe:](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md) Der Rasterizer ist für das Beschneiden von Primitiven, das Vorbereiten von Primitiven für den Pixel-Shader und das Bestimmen des Aufrufs von Pixel-Shadern verantwortlich.
-   [Pixelshader-Stufe](https://www.bing.com/search?q=Pixel-Shader+Stage). Die Pixelshader-Stufe empfängt interpolierte Daten für einen Grundtyp und generiert Pro-Pixel-Daten (z. B. die Farbe).
-   [Ausgabe-Merger-Phase:](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) Die Ausgabe-Merger-Phase ist dafür verantwortlich, verschiedene Typen von Ausgabedaten (Pixel-Shaderwerte, Tiefen- und Schabloneninformationen) mit dem Inhalt des Renderziels und den Tiefen-/Schablonenpuffern zu kombinieren, um das endgültige Pipelineergebnis zu generieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
