---
title: Pixel-Shader-Phase
description: Die Pixel-Shader-Stufe (PS) ermöglicht umfassende Schattierungs Techniken wie z. b. pro Pixel-Beleuchtung und Nachbearbeitung.
ms.assetid: 09831B10-4FD1-41E7-8D81-5AA63DC90020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57142e9c32919a6959a7fac14bf544cca1dacd79
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102083"
---
# <a name="pixel-shader-stage"></a>Pixel-Shader-Phase

Die Pixel-Shader-Stufe (PS) ermöglicht umfassende Schattierungs Techniken wie z. b. pro Pixel-Beleuchtung und Nachbearbeitung. Ein Pixelshader ist ein Programm, das Konstante Variablen, Textur Daten, interpoliert pro Scheitelpunkt Werte und andere Daten kombiniert, um pro-Pixel-Ausgaben zu liefern. Die Raster-Stufe Ruft einen Pixel-Shader einmal für jedes Pixel auf, das von einem primitiven abgedeckt wird. es ist jedoch möglich, einen **null** -Shader anzugeben, um das Ausführen eines Shaders zu vermeiden.

## <a name="the-pixel-shader"></a>Der Pixelshader.

Beim multisamplinggrad einer Textur wird ein Pixelshader einmal pro abgedecktem Pixel aufgerufen, während bei jedem behandelten Multisample ein tiefen-/Schablone-Test erfolgt. Beispiele, die den tiefen-/Schablone-Test bestehen, werden mit der Pixel-Shader-Ausgabe Farbe aktualisiert.

Die intrinsischen Funktionen des Pixel-Shaders liefern oder verwenden Ableitungen von Mengen in Bezug auf den Bildschirmbereich x und y. Die häufigste Verwendung von Ableitungen ist die Berechnung von Detail Berechnungen für die Textur Stichprobe und im Fall von anisotrope Filterung, indem Beispiele entlang der Achse von Anisotropie ausgewählt werden. In der Regel führt eine Hardware Implementierung einen Pixel-Shader auf mehreren Pixeln (z. b. ein 2 x 2-Raster) gleichzeitig aus, sodass Ableitungen von Mengen, die im Pixelshader berechnet werden, als Delta der Werte zum gleichen Zeitpunkt der Ausführung in angrenzenden Pixeln angleichen können.

### <a name="inputs"></a>Eingaben

Wenn die Pipeline ohne einen Geometry-Shader konfiguriert ist, ist ein Pixelshader auf 16, 32-Bit, 4-komponenteneingaben beschränkt. Andernfalls kann ein Pixelshader bis zu 32, 32-Bit, 4-komponenteneingaben annehmen.

Die Pixel-Shader-Eingabedaten enthalten Scheitelpunkt Attribute (die mit oder ohne Perspektiven Korrektur interpoliert werden können) oder als primitive Konstanten behandelt werden können. Pixel-shadereingaben werden aus den Vertex-Attributen des primitiven, das auf der Grundlage des deklarierten Interpolations Modus basiert, interpoliert. Wenn ein primitiver vor der rasterisierung abgeschnitten wird, wird der Interpolations Modus während des clippingprozesses ebenfalls berücksichtigt.

Vertex-Attribute werden an Pixel-Shader-Mittelpunkt Positionen interpoliert (oder ausgewertet). Pixelshader-Attribut Interpolations Modi werden in einer Eingabe Register Deklaration in einer pro-Element-Basis in einem [Argument](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters) oder einer [Eingabe Struktur](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-struct)deklariert. Attribute können linear oder mit [Schwerpunkt-Sampling](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)interpoliert werden. Die Centroid-Auswertung ist nur bei der multisamplinggrad relevant, um Fälle abzudecken, in denen ein Pixel durch ein primitiv abgedeckt ist, ein Pixel Center jedoch möglicherweise nicht ist. die Schwerpunkt Auswertung erfolgt so nah wie möglich im (nicht abgedeckten) Pixel Center.

Eingaben können auch mit einer [System Wert Semantik](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)deklariert werden, die einen Parameter markiert, der von anderen Pipeline Stufen verwendet wird. Beispielsweise sollte eine Pixelposition mit der SV- \_ Positions Semantik gekennzeichnet werden. Die IA-Phase kann einen Skalarwert für einen PixelShader (mit \_ der SV primitiveid) erzeugen; die Raster-Stufe kann auch einen Skalarwert für einen PixelShader generieren (mithilfe von SV \_ isfrontface).

### <a name="outputs"></a>Ausgaben

Ein Pixelshader kann bis zu 8, 32-Bit, 4-Komponentenfarben oder keine Farbe ausgeben, wenn das Pixel verworfen wird. Die Pixel-Shader-Ausgabe Register Komponenten müssen deklariert werden, bevor Sie verwendet werden können. jedem Register ist eine eindeutige Ausgabe-/Schreibmaske gestattet.

Verwenden Sie den Status "Tiefe-Write-Enable" (in der Ausgabe-Fusion-Phase), um zu steuern, ob die Tiefendaten in einen tiefen Puffer geschrieben werden (oder verwenden Sie die Verwerfungs Anweisung, um Daten für dieses Pixel zu verwerfen). Ein Pixelshader kann auch einen optionalen 32-Bit-, 1-Component-, Gleit Komma-und Tiefen Wert für tiefen Tests ausgeben (mit der SV- \_ tiefen Semantik). Der tiefen Wert wird im otiefe-Register ausgegeben und ersetzt den interinterpolated-tiefen Wert für tiefen Tests (vorausgesetzt, die tiefen Tests sind aktiviert). Es gibt keine Möglichkeit, dynamisch zwischen der Verwendung der tiefen Tiefe oder der Shader-otiefe zu wechseln.

Ein Pixelshader kann einen Schablonen Wert nicht ausgeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafik Pipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipeline Stufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 