---
title: Stream-Output Stage
description: Der Zweck der Streamausgabephase besteht in der kontinuierlichen Ausgabe (oder dem Streamen) von Scheitelpunktdaten aus der Geometry-Shader-Stufe (oder der Vertex-Shader-Stufe, wenn die Geometry-Shader-Phase inaktiv ist) in mindestens einem Puffer im Arbeitsspeicher (siehe Erste Schritte mit der Stream-Output-Phase).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- Streamausgabephase (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f630208b60b107b211f8bb6f6ee0f1efac3ed736c96756dbe1e95e24032b02f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538574"
---
# <a name="stream-output-stage"></a>Stream-Output Stage

Der Zweck der Streamausgabephase besteht in der kontinuierlichen Ausgabe (oder dem Streamen) von Scheitelpunktdaten aus der Geometry-Shader-Stufe (oder der Vertex-Shader-Stufe, wenn die Geometry-Shader-Phase inaktiv ist) in mindestens einem Puffer im Arbeitsspeicher (siehe Erste Schritte mit [der Stream-Output-Phase).](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)

Die Streamausgabephase (Stream-Output Stage, SO) befindet sich in der Pipeline direkt nach der Geometry-Shader-Phase und direkt vor der Rasterungsphase, wie im folgenden Diagramm dargestellt.

![Diagramm des Speicherorts der Streamausgabephase in der Pipeline](images/d3d10-pipeline-stages-so.png)

Daten, die in den Arbeitsspeicher gestreamt werden, können in einem nachfolgenden Rendering-Durchlauf zurück in die Pipeline gelesen oder in eine Stagingressource kopiert werden (damit sie von der CPU gelesen werden können). Die Menge der aus dem Stream übertragenen Daten kann variieren. Die [**ID3D11DeviceContext::D rawAuto-API**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) wurde entwickelt, um die Daten zu verarbeiten, ohne dass (gpu) die Menge der geschriebenen Daten abfragen muss.

Wenn ein Dreiecks- oder Linienstreifen an die Eingabe-Assembler-Stufe gebunden ist, wird jeder Strip in eine Liste konvertiert, bevor er herausgestreamt wird. Scheitelungen werden immer als vollständige Primitive geschrieben (z. B. 3 Scheiteltices gleichzeitig für Dreiecke); Unvollständige Primitive werden nie gestreamt. Primitive Typen mit Adjacency verwerfen die Adjacency-Daten, bevor Daten gestreamt werden.

Es gibt zwei Möglichkeiten, Streamausgabedaten in die Pipeline zu übertragen:

-   Streamausgabedaten können wieder in die Eingabe-Assembler-Phase eingespeist werden.
-   Streamausgabedaten können von programmierbaren Shadern mithilfe von Ladefunktionen (z. B. [Laden) gelesen werden.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)

Um einen Puffer als Streamausgaberessource zu verwenden, erstellen Sie den Puffer mit dem [**Flag D3D11 \_ BIND STREAM \_ \_ OUTPUT.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) Die Streamausgabephase unterstützt bis zu 4 Puffer gleichzeitig.

-   Wenn Sie Daten in mehrere Puffer streamen, kann jeder Puffer nur ein einzelnes Element (bis zu 4 Komponenten) von Pro-Scheitelpunkt-Daten erfassen, mit einem impliziten Datenschritt, der der Elementbreite in jedem Puffer entspricht (kompatibel mit der Art und Weise, wie Einzelne Elementpuffer für die Eingabe in Shaderstufen gebunden werden können). Wenn die Puffer unterschiedliche Größen haben, wird das Schreiben beendet, sobald einer der Puffer voll ist.
-   Wenn Sie Daten in einen einzelnen Puffer streamen, kann der Puffer bis zu 64 Skalarkomponenten von Daten pro Scheitelpunkt (256 Byte oder weniger) erfassen, oder der Scheitelpunkt-Stride kann bis zu 2048 Bytes betragen.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                               | Beschreibung                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Erste Schritte mit der Stream-Output Stage](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | In diesem Abschnitt wird beschrieben, wie Sie einen Geometrie-Shader mit der Streamausgabephase verwenden.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafikpipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipelinestufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

