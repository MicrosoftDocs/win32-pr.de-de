---
title: Pixel-Shader-Stufe
description: Die Pixel-Shader-Stufe (PS) ermöglicht umfassende Schattierungstechniken wie pixelbasierte Beleuchtung und Nachbearbeitung.
ms.assetid: 09831B10-4FD1-41E7-8D81-5AA63DC90020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd58bbc55bbc2fb7d590036bceb061f2a304c0be16ff058d04f226021dfe3cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988160"
---
# <a name="pixel-shader-stage"></a>Pixel-Shader-Stufe

Die Pixel-Shader-Stufe (PS) ermöglicht umfassende Schattierungstechniken wie pixelbasierte Beleuchtung und Nachbearbeitung. Ein Pixel-Shader ist ein Programm, das konstante Variablen, Texturdaten, interpolierte Werte pro Scheitelpunkt und andere Daten kombiniert, um Pixelausgaben zu erzeugen. Die Rasterizerphase ruft einen Pixel-Shader einmal für jedes Pixel auf, das von einem Primitiven abgedeckt wird. Es ist jedoch möglich, einen **NULL-Shader** anzugeben, um die Ausführung eines Shaders zu vermeiden.

## <a name="the-pixel-shader"></a>Der Pixel-Shader

Beim Multisampling einer Textur wird ein Pixelshader einmal pro abgedeckten Pixel aufgerufen, während für jedes abgedeckte Multisample ein Tiefen-/Schablonentest durchgeführt wird. Beispiele, die den Tiefen-/Schablonentest bestehen, werden mit der Ausgabefarbe des Pixelshader aktualisiert.

Die systeminternen Funktionen des Pixelshader erzeugen oder verwenden Ableitungen von Mengen in Bezug auf den Bildschirmbereich x und y. Die häufigste Verwendung für Ableitungen ist das Berechnen von Detailberechnungen für die Textursampling und im Fall der Anisotropiefilterung die Auswahl von Stichproben entlang der Achse der Anisotropie. In der Regel führt eine Hardwareimplementierung einen Pixel-Shader auf mehreren Pixeln (z. B. einem 2x2-Raster) gleichzeitig aus, sodass Ableitungen von Mengen, die im Pixelshader berechnet werden, als Deltas der Werte an demselben Ausführungspunkt in angrenzenden Pixeln relativ geschätzt werden können.

### <a name="inputs"></a>Eingaben

Wenn die Pipeline ohne geometriebasierten Shader konfiguriert ist, ist ein Pixel-Shader auf Eingaben mit 16, 32 Bit und 4 Komponenten beschränkt. Andernfalls kann ein Pixel-Shader eingaben mit bis zu 32, 32 Bit und 4 Komponenten dauern.

Pixel-Shadereingabedaten enthalten Scheitelpunktattribute (die mit oder ohne perspektivische Korrektur interpoliert werden können) oder können als primitive Konstanten behandelt werden. Pixel-Shadereingaben werden basierend auf dem deklarierten Interpolationsmodus aus den Scheitelpunktattributen des Primitiven interpoliert, der gerastet wird. Wenn ein Primitiv vor der Rasterung abgeschnitten wird, wird der Interpolationsmodus auch während des Clippingprozesses berücksichtigt.

Scheitelpunktattribute werden an Pixel-Shader-Mittelpunkten interpoliert (oder ausgewertet). Die Interpolationsmodi des Pixelshaderattributs werden in einer Eingaberegisterdeklaration auf Elementbasis entweder in einem [Argument](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters) oder in einer [Eingabestruktur](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-struct)deklariert. Attribute können linear oder mit [schwerpunktmäßiger Stichprobenentnahme](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)interpoliert werden. Die Schwerpunktauswertung ist nur während des Multisamplings relevant, um Fälle abzudecken, in denen ein Pixel von einem Primitiven abgedeckt wird, aber ein Pixelmittelpunkt möglicherweise nicht ist. Die Schwerpunktauswertung erfolgt so nah wie möglich am (nicht abgedeckten) Pixelmittelpunkt.

Eingaben können auch mit einer [Systemwertsemantik](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)deklariert werden, die einen Parameter markiert, der von anderen Pipelinephasen verwendet wird. Beispielsweise sollte eine Pixelposition mit der \_ SV-Positionssemantik markiert werden. Die IA-Stufe kann einen Skalar für einen Pixel-Shader erzeugen (mit SV \_ PrimitiveID). Die Rasterizerphase kann auch einen Skalar für einen Pixelshader generieren (mit SV \_ IsFrontFace).

### <a name="outputs"></a>Ausgaben

Ein Pixel-Shader kann bis zu 8, 32 Bit, 4-Komponenten-Farben oder keine Farbe ausgeben, wenn das Pixel verworfen wird. Pixel-Shader-Ausgaberegisterkomponenten müssen deklariert werden, bevor sie verwendet werden können. Für jedes Register ist eine unterschiedliche Ausgabe-/Schreibmaske zulässig.

Verwenden Sie den Zustand "Depth-Write-Enable" (in der Ausgabezusammenführungsphase), um zu steuern, ob Tiefendaten in einen Tiefenpuffer geschrieben werden (oder verwenden Sie die Anweisung discard, um Daten für dieses Pixel zu verwerfen). Ein Pixel-Shader kann auch einen optionalen 32-Bit-, 1-Komponenten-, Gleitkomma- und Tiefenwert für Tiefentests ausgeben (mithilfe der \_ SV-Tiefensemantik). Der Tiefenwert wird im oDepth-Register ausgegeben und ersetzt den interpolierten Tiefenwert für Tiefentests (vorausgesetzt, tiefentests sind aktiviert). Es gibt keine Möglichkeit, zwischen der Verwendung von fester Funktionstiefe oder dem Shader oDepth dynamisch zu wechseln.

Ein Pixel-Shader kann keinen Schablonenwert ausgeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafikpipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipelinestufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 