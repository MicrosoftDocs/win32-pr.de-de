---
title: Eingabe-Assembler-Stufe
description: Die API Direct3D 10 und höher trennt funktionale Bereiche der Pipeline in Phasen. die erste Phase in der Pipeline ist die Eingabe-Assembler-Phase (IA).
ms.assetid: 71141a5e-2d79-4b02-8370-c0cbc8618908
keywords:
- Eingabe Assembler-Stufe (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121d98ca66bbe42f6eaa3023150203ce0538445b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391265"
---
# <a name="input-assembler-stage"></a>Eingabe-Assembler-Stufe

Die API Direct3D 10 und höher trennt funktionale Bereiche der Pipeline in Phasen. die erste Phase in der Pipeline ist die Eingabe-Assembler-Phase (IA).

Der Zweck der Eingabe-Assembler-Phase ist das Lesen primitiver Daten (Punkte, Linien und/oder Dreiecke) aus vom Benutzer gefüllten Puffern und Assemblieren der Daten in primitive, die von den anderen Pipeline Stufen verwendet werden. In der IA-Phase können Vertices in mehreren unterschiedlichen [primitiven Typen](d3d10-graphics-programming-guide-primitive-topologies.md) (z. b. Linien Listen, Dreiecks Streifen oder primitive) zusammengestellt werden. Neue primitive Typen (z. b. eine Zeilen Liste mit Informationen oder eine Dreiecks Liste mit der Nähe) wurden hinzugefügt, um den Geometry-Shader zu unterstützen.

Informationen zu Informationen sind für eine Anwendung nur in einem Geometry-Shader sichtbar. Wenn ein Geometry-Shader mit einem Dreieck aufgerufen wurde (z. a. die Nähe), enthalten die Eingabedaten beispielsweise drei Scheitel Punkte für jedes Dreieck und drei Scheitel Punkte für Daten pro Dreieck.

Wenn die Eingabe-Assembler-Phase angefordert wird, um Daten zu erhalten, müssen die Eingabedaten Informationen zu den Daten enthalten. Hierfür ist möglicherweise ein dummyscheitel Punkt (aus einem degenerierten Dreieck) erforderlich, oder Sie können in einem der Scheitelpunkt Attribute kennzeichnen, ob der Scheitelpunkt vorhanden ist oder nicht. Dies müsste auch von einem Geometry-Shader erkannt und behandelt werden, obwohl die Erkennung degenerierter Geometrie in der Raster-Stufe stattfindet.

Beim Zusammenstellen von primitiven besteht der sekundäre Zweck der IA darin, vom [systemgenerierte Werte](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) anzufügen, damit Shader effizienter werden. Vom System generierte Werte sind Text Zeichenfolgen, die auch als Semantik bezeichnet werden. Alle drei Shader-Stufen werden aus einem gemeinsamen Shader-Kern erstellt, und der Shader-Kern verwendet vom systemgenerierte Werte (z. b. eine primitive ID, eine Instanz-ID oder eine Scheitelpunkt-ID), damit eine Shader-Stufe die Verarbeitung nur auf die primitiven, Instanzen oder Scheitel Punkte reduzieren kann, die noch nicht verarbeitet wurden.

Wie im [Pipeline Blockdiagramm](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)gezeigt, werden die Daten in der [Vertexshader-Stufe](/previous-versions//bb205146(v=vs.85))ausgegeben, sobald die IA-Phase Daten aus dem Arbeitsspeicher liest (die Daten in primitive assembliert und vom systemgenerierte Werte anfügt).


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ersten Einstieg in die Input-Assembler Phase](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)<br/> | Zum Initialisieren der Eingabe-Assembler-Phase (IA) müssen einige Schritte ausgeführt werden. Beispielsweise müssen Sie Puffer Ressourcen mit den Vertex-Daten erstellen, die von der Pipeline benötigt werden, und Sie können die IA-Phase, in der die Puffer sind, und die Art der Daten angeben, die aus den Daten zusammengestellt werden sollen.<br/> |
| [Primitive Topologien](d3d10-graphics-programming-guide-primitive-topologies.md)<br/>                                            | Direct3D 10 und höher unterstützen verschiedene primitive Typen (oder Topologien), die durch den enumerierten Typ [**D3D \_ primitiver \_ Topologie**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) dargestellt werden. Diese Typen definieren, wie Vertices interpretiert und von der Pipeline gerendert werden.<br/>                                                          |
| [Verwenden der Input-Assembler-Phase ohne Puffer](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md)<br/>     | Das Erstellen und Binden von Puffern ist nicht erforderlich, wenn die Shader keine Puffer erfordern. Dieser Abschnitt enthält ein Beispiel für einfache Vertex-und Pixel-Shader, die ein einzelnes Dreieck zeichnen.<br/>                                                                                                                                  |
| [Verwenden von System-Generated Werten](d3d10-graphics-programming-guide-input-assembler-stage-using.md)<br/>                            | Vom System generierte Werte werden von der IA-Phase (basierend auf der vom Benutzer bereitgestellten Eingabe [Semantik](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) generiert, um bestimmte Effizienz bei shadervorgängen zu ermöglichen. <br/>                                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafik Pipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipeline Stufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

