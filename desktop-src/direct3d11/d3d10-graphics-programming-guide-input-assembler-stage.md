---
title: Eingabe-Assembler-Stufe
description: Die Direct3D 10- und höher-API trennt Funktionsbereiche der Pipeline in Phasen. Die erste Phase in der Pipeline ist die Phase des Eingabeassemblierers (Input-Assembler, IA).
ms.assetid: 71141a5e-2d79-4b02-8370-c0cbc8618908
keywords:
- Eingabeassembliererphase (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e16a419dfe57dac5b16562b234a7a60d417c071fcd6214f3defa84bcbe8b4ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408380"
---
# <a name="input-assembler-stage"></a>Eingabe-Assembler-Stufe

Die Direct3D 10- und höher-API trennt Funktionsbereiche der Pipeline in Phasen. Die erste Phase in der Pipeline ist die Phase des Eingabeassemblierers (Input-Assembler, IA).

Der Zweck der Eingabeassembliererphase besteht darin, primitive Daten (Punkte, Linien und/oder Dreiecke) aus vom Benutzer gefüllten Puffern zu lesen und die Daten zu Primitiven zusammenzustellen, die von den anderen Pipelinestufen verwendet werden. Die IA-Stufe kann Scheitelpunkte in mehreren verschiedenen [primitiven Typen](d3d10-graphics-programming-guide-primitive-topologies.md) zusammensetzen (z. B. Linienlisten, Dreiecksstreifen oder Primitive mit Adjazenz). Neue primitive Typen (z. B. eine Linienliste mit Adjazenz oder eine Dreiecksliste mit Adjazenz) wurden hinzugefügt, um den Geometrie-Shader zu unterstützen.

Adjazenzinformationen sind für eine Anwendung nur in einem Geometry-Shader sichtbar. Wenn beispielsweise ein Geometrie-Shader mit einem Dreieck mit Adjazenz aufgerufen wird, enthalten die Eingabedaten 3 Scheitelpunkte für jedes Dreieck und drei Scheitelpunkte für Ad/Ency-Daten pro Dreieck.

Wenn die Eingabeassembliererphase angefordert wird, Adjazenzdaten auszugeben, müssen die Eingabedaten Adjazenzdaten enthalten. Dies kann die Bereitstellung eines Dummy-Scheitelpunkts (das ein degenerates Dreieck bildet) oder das Kennzeichnen in einem der Scheitelpunktattribute erfordern, unabhängig davon, ob der Scheitelpunkt vorhanden ist oder nicht. Dies muss auch von einem Geometrie-Shader erkannt und behandelt werden, obwohl die Culling der degenerierten Geometrie in der Rasterizerphase erfolgt.

Beim Zusammenstellen von Primitiven besteht ein sekundärer Zweck der IA darin, [vom System generierte Werte](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) anzufügen, um Shader effizienter zu machen. Vom System generierte Werte sind Textzeichenfolgen, die auch als Semantik bezeichnet werden. Alle drei Shaderstufen werden aus einem gemeinsamen Shaderkern erstellt, und der Shaderkern verwendet vom System generierte Werte (z. B. eine primitive ID, eine Instanz-ID oder eine Scheitelpunkt-ID), sodass eine Shaderphase die Verarbeitung nur auf primitive Typen, Instanzen oder Scheitelpunkte reduzieren kann, die noch nicht verarbeitet wurden.

Wie im [Pipelineblockdiagramm](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)gezeigt, werden die Daten an die [Vertex-Shaderphase](/previous-versions//bb205146(v=vs.85))ausgegeben, sobald die IA-Stufe Daten aus dem Arbeitsspeicher liest (die Daten zu Primitiven zusammenfügt und systemgenerierte Werte anfügt).


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erste Schritte mit der Input-Assembler Stage](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)<br/> | Es sind einige Schritte erforderlich, um die Phase des Eingabeassemblierers (Input-Assembler, IA) zu initialisieren. Beispielsweise müssen Sie Pufferressourcen mit den von der Pipeline benötigten Scheitelpunktdaten erstellen, der IA-Phase mitteilen, wo sich die Puffer befinden und welche Art von Daten sie enthalten, und den Typ der Primitive angeben, die aus den Daten zusammengesetzt werden sollen.<br/> |
| [Primitive Topologien](d3d10-graphics-programming-guide-primitive-topologies.md)<br/>                                            | Direct3D 10 und höher unterstützt mehrere primitive Typen (oder Topologien), die durch den [**D3D \_ PRIMITIVE \_ TOPOLOGY-Enumerationstyp**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) dargestellt werden. Diese Typen definieren, wie Scheitelpunkte von der Pipeline interpretiert und gerendert werden.<br/>                                                          |
| [Verwenden der Input-Assembler Phase ohne Puffer](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md)<br/>     | Das Erstellen und Binden von Puffern ist nicht erforderlich, wenn Ihre Shader keine Puffer benötigen. Dieser Abschnitt enthält ein Beispiel für einfache Vertex- und Pixel-Shader, die ein einzelnes Dreieck zeichnen.<br/>                                                                                                                                  |
| [Verwenden von System-Generated Werten](d3d10-graphics-programming-guide-input-assembler-stage-using.md)<br/>                            | Vom System generierte Werte werden von der IA-Phase generiert (basierend auf der vom Benutzer [bereitgestellten Eingabesemantik),](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)um bestimmte Effizienz bei Shadervorgängen zu ermöglichen. <br/>                                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafikpipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipelinestufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

