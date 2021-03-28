---
title: Primitive Topologien
description: Direct3D 10 und höher unterstützen verschiedene primitive Typen (oder Topologien), die durch den \_ \_ enumerierten Typ D3D primitiver Topologie dargestellt werden. Diese Typen definieren, wie Vertices interpretiert und von der Pipeline gerendert werden.
ms.assetid: 357ad085-fd91-4420-abc3-1c57e8cbb517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e83f901d4d91d01a3cffedddb343fde7b50c20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315218"
---
# <a name="primitive-topologies"></a>Primitive Topologien

Direct3D 10 und höher unterstützen verschiedene primitive Typen (oder Topologien), die durch den enumerierten Typ [**D3D \_ primitiver \_ Topologie**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) dargestellt werden. Diese Typen definieren, wie Vertices interpretiert und von der Pipeline gerendert werden.

-   [Grundlegende primitive Typen](#basic-primitive-types)
-   [Primitive Nähe](#primitive-adjacency)
-   [Richtung und führende Scheitelpunkt Positionen](#winding-direction-and-leading-vertex-positions)
-   [Erzeugen mehrerer Striche](#generating-multiple-strips)
-   [Zugehörige Themen](#related-topics)

## <a name="basic-primitive-types"></a>Grundlegende primitive Typen

Die folgenden grundlegenden primitiven Typen werden unterstützt:

-   [Punkt Liste](/windows/desktop/direct3d9/point-lists)
-   [Zeilen Liste](/windows/desktop/direct3d9/line-lists)
-   [Zeilen Streifen](/windows/desktop/direct3d9/line-strips)
-   [Dreiecks Liste](/windows/desktop/direct3d9/triangle-lists)
-   [Trip Range](/windows/desktop/direct3d9/triangle-strips)

Eine Visualisierung der einzelnen primitiven Typen finden Sie im Diagramm weiter unten in diesem Thema in der [Richtung "Richtung" und führenden Scheitelpunkt Positionen](#winding-direction-and-leading-vertex-positions).

Die Eingabe-Assembler-Phase liest Daten aus Scheitel Punkten und Index Puffern, assembliert die Daten in diese primitiven und sendet die Daten dann an die restlichen Pipeline Stufen. (Sie können die [**Verknüpfung id3d11devicecontext aus:: iasetprimitivetopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology) -Methode verwenden, um den primitiven Typ für die Eingabe-Assembler-Phase anzugeben.)

## <a name="primitive-adjacency"></a>Primitive Nähe

Alle Typen von Direct3D 10 und höher (mit Ausnahme der Punkt Liste) stehen in zwei Versionen zur Verfügung: ein primitiver Typ mit der Nähe und ein primitiver Typ ohne Unterschied. Primitive mit einer bestimmten Konsistenz enthalten einige der umgebenden Scheitel Punkte, während primitive ohne die unter Verwendung nur die Scheitel Punkte des zielprimitives enthalten. Beispielsweise verfügt die primitive Zeilen Liste (dargestellt durch den **\_ \_ \_ LineList-Wert D3D primitive Topologie** ) über eine entsprechende Zeilen Listen primitive, die die Bedeutung (dargestellt durch den Wert der " **D3D \_ primitive \_ Topology \_ LineList \_ ADJ** ") enthält.

Angrenzende primitive dienen dazu, weitere Informationen über die Geometrie bereitzustellen, die nur über einen Geometry-Shader sichtbar sind. Die Verwendung ist nützlich für Geometry-Shader, die die Silhouette-Erkennung, die Schatten Volumeverschlüsselung usw. verwenden.

Nehmen Sie z. b. an, Sie möchten eine Dreiecks Liste mit Informationen zeichnen. Eine Dreiecks Liste, die 36 Scheitel Punkte (mit der Konsistenz) enthält, ergibt 6 abgeschlossene primitive. Primitive mit der Verwendung (mit Ausnahme von Zeilen Streifen) enthalten genau doppelt so viele Scheitel Punkte wie die äquivalente primitive, wobei jeder weitere Scheitelpunkt ein angrenzender Scheitelpunkt ist.

## <a name="winding-direction-and-leading-vertex-positions"></a>Richtung und führende Scheitelpunkt Positionen

Wie in der folgenden Abbildung dargestellt, ist ein führender Scheitelpunkt der erste nicht benachbarte Scheitelpunkt in einem primitiven. Für einen primitiven Typ können mehrere führende Vertices definiert werden, sofern jeder für einen anderen primitiven verwendet wird. Bei einem Dreiecks Streifen mit der Sicherheit sind die führenden Scheitel Punkte 0, 2, 4, 6 usw. Bei einem Zeilen Streifen mit der Sicherheit sind die führenden Vertices 1, 2, 3 usw. Ein angrenzender primitiv hat andererseits keinen führenden Scheitelpunkt.

Die folgende Abbildung zeigt die Scheitelpunkt Anordnung für alle primitiven Typen, die vom Eingabe Assembler erzeugt werden können.

![Diagramm der Scheitelpunkt Anordnung für primitive Typen](images/d3d10-primitive-topologies.png)

Die Symbole in der vorangehenden Abbildung werden in der folgenden Tabelle beschrieben.



| Symbol                                                                                   | name              | BESCHREIBUNG                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Symbol für einen Scheitelpunkt](images/d3d10-primitive-topologies-vertex.png)                     | Scheitelpunkt            | Ein Punkt im 3D-Raum.                                                                                                                                                                               |
| ![Symbol für die Richtung der Richtung](images/d3d10-primitive-topologies-winding-direction.png) | Richtung | Die Scheitelpunkt Reihenfolge beim Assemblieren eines primitiven. Kann im Uhrzeigersinn oder gegen den Uhrzeigersinn stehen; Geben Sie dies durch Aufrufen von [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)an. |
| ![Symbol für führenden Scheitelpunkt](images/d3d10-primitive-topologies-leading-vertex.png)       | Führender Scheitelpunkt    | Der erste nicht benachbarte Scheitelpunkt in einem primitiven, der Daten pro Konstante enthält.                                                                                                                      |



 

## <a name="generating-multiple-strips"></a>Erzeugen mehrerer Striche

Sie können mehrere Striche durch die Bereichs Bearbeitung generieren. Sie können einen Strip-Cut ausführen, indem Sie die Funktion [restartstrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) HLSL explizit aufrufen oder einen speziellen Indexwert in den Index Puffer einfügen. Dieser Wert ist – 1, d. h. 0xFFFFFFFF für 32-Bit-Indizes oder 0xFFFF für 16-Bit-Indizes. Ein Index von – 1 gibt einen expliziten ' Cut ' oder ' restart ' des aktuellen Streifens an. Der vorherige Index schließt den vorherigen primitiven oder Strip ab, und der nächste Index startet einen neuen primitiven oder Strip. Weitere Informationen zum Erstellen mehrerer Striche finden Sie unter [Geometry-Shader-Stufe](/previous-versions//bb205146(v=vs.85)).

> [!Note]  
> Sie benötigen die Hardware auf [Featureebene](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 oder höher, da nicht alle 10 Level9-Hardware diese Funktionalität implementiert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ersten Einstieg in die Input-Assembler Phase](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> <dt>

[Pipeline Stufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 