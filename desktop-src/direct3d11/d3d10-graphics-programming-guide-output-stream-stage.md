---
title: Stream-Output Phase
description: Der Zweck der Stream-Output-Phase besteht darin, Vertexdaten fortlaufend aus der Geometrie-Shader-Stufe (oder der Vertex-Shader-Phase, wenn die Geometrie-shaderstufe inaktiv ist) in einen oder mehrere Puffer im Arbeitsspeicher auszugeben (oder zu streamen) (Weitere Informationen finden Sie unter Getting Started with the Stream-Output Stage).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- Stream-Ausgabestufe (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0879cde2ba2f1bb3ed9cc6121aaf378cd4af312
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474685"
---
# <a name="stream-output-stage"></a>Stream-Output Phase

Der Zweck der Stream-Output-Phase besteht darin, Vertexdaten fortlaufend aus der Geometrie-Shader-Stufe (oder der Vertex-Shader-Phase, wenn die Geometrie-shaderstufe inaktiv ist) in einen oder mehrere Puffer im Arbeitsspeicher auszugeben (oder zu streamen) (Weitere Informationen finden Sie unter [Getting Started with the Stream-Output Stage](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).

Die Stream-Output-Phase (also) befindet sich in der Pipeline direkt hinter der Geometrie-Shader-Phase und unmittelbar vor der rasterisierungsphase, wie im folgenden Diagramm dargestellt.

![Diagramm des Speicher Orts der Stream-Ausgabestufe in der Pipeline](images/d3d10-pipeline-stages-so.png)

Daten, die in den Arbeitsspeicher gestreamt werden, können in einem nachfolgenden Renderingdurchlauf wieder in die Pipeline eingelesen werden oder in eine stagingressource kopiert werden (damit Sie von der CPU gelesen werden kann). Die Menge der Daten, die gestreamt werden, kann variieren. die [**Verknüpfung id3d11devicecontext aus::D rawauto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) -API ist so konzipiert, dass die Daten verarbeitet werden, ohne dass die Menge der geschriebenen Daten (GPU) abgefragt werden muss.

Wenn ein Dreieck oder ein Zeilen Streifen an die Eingabe-Assembler-Phase gebunden ist, wird jeder Strip in eine Liste konvertiert, bevor diese gestreamt werden. Scheitel Punkte werden immer als umfassende primitive geschrieben (z. b. 3 Scheitel Punkte gleichzeitig für Dreiecke); unvollständige primitive werden niemals gestreamt. Primitive Typen mit der Konsistenz verwerfen vor dem Streamen von Daten die Daten der Daten.

Es gibt zwei Möglichkeiten, Datenstrom Ausgabedaten in die Pipeline zu übermitteln:

-   Stream-Ausgabedaten können wieder in die Eingabe-Assembler-Phase eingegeben werden.
-   Stream-Ausgabedaten können von programmierbaren Shadern mithilfe von Ladefunktionen (z. b. [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)) gelesen werden.

Wenn Sie einen Puffer als Stream-Output-Ressource verwenden möchten, erstellen Sie den Puffer mit dem [**D3D11 \_ Bind- \_ \_ Ausgabe**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) Kennzeichen. Die Stream-Output-Stufe unterstützt bis zu 4 Puffer gleichzeitig.

-   Wenn Sie Daten in mehrere Puffer streamen, kann jeder Puffer nur ein einzelnes Element (bis zu 4 Komponenten) von pro-Vertex-Daten erfassen, wobei ein impliziter Daten Sprung gleich der Elementbreite in den einzelnen Puffern ist (kompatibel mit der Art und Weise, wie einzelne Element Puffer für Eingaben in Shader-Stufen gebunden werden können). Wenn die Puffer über unterschiedliche Größen verfügen, wird der Schreibvorgang beendet, sobald ein Puffer voll ist.
-   Wenn Sie Daten in einen einzelnen Puffer streamen, kann der Puffer bis zu 64 skalare Komponenten von pro-Vertex-Daten (256 Bytes oder weniger) erfassen, oder der Scheitelpunkt Schritt kann bis zu 2048 Byte betragen.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                               | BESCHREIBUNG                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Ersten Einstieg in die Stream-Output Phase](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | In diesem Abschnitt wird beschrieben, wie ein Geometry-Shader mit der Stream-Ausgabestufe verwendet wird.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafik Pipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipeline Stufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

