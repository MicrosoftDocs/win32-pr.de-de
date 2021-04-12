---
description: HLSL-Kompilierungsoptionen.
ms.assetid: vs|directx_sdk|~\d3d10_shader.htm
title: D3D10_SHADER Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16480e2aceada7f5ed05912eca59cc88886ac9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483582"
---
# <a name="d3d10_shader-constants"></a>D3d10- \_ Shader-Konstanten

HLSL-Kompilierungsoptionen.



| \#definieren                                        | BESCHREIBUNG                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3d10- \_ Shader \_ Vermeidung der \_ Fluss \_ Steuerung             | Weisen Sie den Compiler an, die Fluss Steuerung nicht zuzulassen (sofern möglich).                                                                                                                                                                                       |
| D3d10- \_ Shader \_ Debuggen                            | Fügt Debugdatei/Zeilen-/Typ-/Symbolinformationen ein.                                                                                                                                                                                                |
| D3d10- \_ Shader " \_ \_ strictness" aktivieren               | Standardmäßig deaktiviert der HLSL-Compiler die strenge in der veralteten Syntax. Wenn Sie dieses Flag angeben, wird eine strenge ermöglicht, die möglicherweise keine Legacy Syntax zulässt.                                                                                         |
| D3d10- \_ Shader-abwärts \_ \_ \_ Kompatibilität aktivieren | Dadurch können ältere Shader in 4- \_ 0-Ziele kompilieren.                                                                                                                                                                                         |
| D3d10 \_ Shader \_ Force \_ vs \_ Software \_ No \_ Opt     | Kompilieren Sie einen Vertex-Shader für das nächsthöhere Shader-Profil. Mit dieser Option wird das Debugging aktiviert (und Optimierungen deaktiviert).                                                                                                                           |
| D3d10 \_ Shader \_ Force \_ PS \_ Software \_ No \_ Opt     | Kompilieren Sie einen PixelShader für das nächste höchste Shader-Profil. Mit dieser Option wird das Debugging aktiviert (und Optimierungen deaktiviert).                                                                                                                            |
| D3d10 \_ Shader \_ IEEE \_ strictness                 | Aktiviert IEEE-strenge.                                                                                                                                                                                                                       |
| D3d10- \_ Shader \_ kein \_ preshader                    | Deaktiviert preshaders. Die Verwendung dieses Flags bewirkt, dass der Compiler keinen statischen Ausdruck für die Auswertung abruft.                                                                                                                                 |
| D3d10- \_ \_ shaderoptimierung \_ LEVEL0             | Niedrigste Optimierungs Ebene. Erzeugt möglicherweise langsameren Code, führt dies jedoch schneller aus. Dies kann bei einem hochgradig iterativen shaderentwicklungsprozess nützlich sein.                                                                                             |
| D3d10- \_ \_ shaderoptimierung \_ Level1             | Die zweite niedrigste Optimierungs Ebene.                                                                                                                                                                                                              |
| D3d10- \_ \_ shaderoptimierung \_ Level2             | Die zweithöchste Optimierungs Ebene.                                                                                                                                                                                                             |
| D3d10- \_ \_ shaderoptimierung \_ LEVEL3             | Höchste Optimierungs Ebene. Erzeugt einen bestmöglichen Code, kann aber erheblich länger dauern. Dies ist nützlich für endgültige Builds einer Anwendung, bei der die Leistung der wichtigste Faktor ist.                                 |
| D3d10 \_ Shader \_ Pack \_ Matrix \_ Zeile \_ Haupt         | Sofern nicht explizit angegeben, werden Matrizen in der Reihenfolge der Zeilen in der Reihenfolge der Eingaben und Ausgaben des Shaders verpackt.                                                                                                                                   |
| D3d10 \_ Shader \_ Pack \_ Matrix \_ Spalte \_ Major      | Wenn die Matrizen nicht explizit angegeben werden, werden Sie in der Spalte in der Reihenfolge der Eingabe und Ausgabe des Shaders verpackt. Dies ist in der Regel effizienter, da Sie die Multiplikation von Vektor Matrizen mithilfe einer Reihe von Punkt Produkten ermöglicht. |
| Teil Genauigkeit der d3d10- \_ Shader \_ \_               | Erzwingen, dass alle Berechnungen mit teilweiser Genauigkeit durchgeführt werden. Dies kann auf Hardware möglicherweise schneller ausgeführt werden.                                                                                                                                                |
| D3d10- \_ Shader \_ bevorzugt \_ Fluss \_ Steuerung            | Weisen Sie den Compiler an, die Fluss Steuerung (sofern möglich) zu verwenden.                                                                                                                                                                                             |
| D3d10 \_ Shader \_ Skip- \_ Optimierung               | Optimierung während der Codegenerierung überspringen; wird im Allgemeinen nur für Debuggen empfohlen.                                                                                                                                                                |
| D3d10 \_ Shader-über \_ Prüfung überspringen \_                 | Validieren Sie den generierten Code nicht mit bekannten Funktionen und Einschränkungen. Verwenden Sie dies nur für Shader, die in der Vergangenheit erfolgreich kompiliert wurden. Shader werden immer von DirectX überprüft, bevor Sie auf das Gerät festgelegt werden.         |
| D3d10- \_ Shader- \_ Warnungen \_ sind \_ Fehler            | Informieren Sie den HLSL-Compiler, dass beim Kompilieren des Shader-Codes alle Warnungen als Fehler behandelt werden. Für neuen Shader-Code sollten Sie diese Option verwenden, um alle Warnungen zu beheben und möglichst wenige schwer zu suchende Code Fehler zu ermitteln.             |



 

Diese Konstanten werden in d3d10shader. h als Makros definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shaderkonstanten](d3d10-graphics-reference-d3d10-shader-constants.md)
</dt> </dl>

 

 



