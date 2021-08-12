---
description: HLSL-Kompilierungsoptionen.
ms.assetid: vs|directx_sdk|~\d3d10_shader.htm
title: D3D10_SHADER Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e965c050d3643e80b493875b27ba5a9b774b351487e191584f40297819758f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303523"
---
# <a name="d3d10_shader-constants"></a>\_D3D10-SHADER-Konstanten

HLSL-Kompilierungsoptionen.



| \#Definieren                                        | Beschreibung                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10-SHADER \_ VERMEIDEN \_ DER \_ \_ FLUSSSTEUERUNG             | Teilen Sie dem Compiler mit, dass die Flusssteuerung (wenn möglich) nicht zulässig ist.                                                                                                                                                                                       |
| D3D10 \_ SHADER \_ DEBUG                            | Fügen Sie Debugdatei-/Zeilen-/Typ-/Symbolinformationen ein.                                                                                                                                                                                                |
| D3D10 \_ SHADER ENABLE STRICTNESS (D3D10-SHADER \_ AKTIVIEREN DER \_ STRENGE)               | Standardmäßig deaktiviert der HLSL-Compiler die Strenge der veralteten Syntax. Die Angabe dieses Flags ermöglicht Strenge, die möglicherweise keine Legacysyntax zu lässt.                                                                                         |
| D3D10-SHADER \_ \_ AKTIVIEREN DER \_ \_ ABWÄRTSKOMPATIBILITÄT | Dadurch können ältere Shader auf 4 \_ 0 Ziele kompiliert werden.                                                                                                                                                                                         |
| D3D10 \_ SHADER \_ FORCE \_ VS \_ SOFTWARE \_ NO \_ OPT     | Kompilieren Sie einen Vertex-Shader für das höchste Shaderprofil. Mit dieser Option wird das Debuggen aktiviert (und Optimierungen deaktiviert).                                                                                                                           |
| D3D10 \_ SHADER \_ FORCE \_ PS \_ SOFTWARE \_ NO \_ OPT     | Kompilieren Sie einen Pixel-Shader für das höchste Shaderprofil. Mit dieser Option wird das Debuggen aktiviert (und Optimierungen deaktiviert).                                                                                                                            |
| IEEE STRICTNESS DES \_ D3D10-SHADERS \_ \_                 | Aktiviert IEEE-Strenge.                                                                                                                                                                                                                       |
| D3D10-SHADER \_ \_ KEIN \_ PRESHADER                    | Deaktiviert Preshaders. Wenn Sie dieses Flag verwenden, wird der Compiler keinen statischen Ausdruck zur Auswertung herausziehen.                                                                                                                                 |
| D3D10 \_ SHADER \_ OPTIMIZATION \_ LEVEL0             | Niedrigste Optimierungsstufe. Kann langsameren Code erzeugen, wird dies aber schneller tun. Dies kann in einem hochgradig iterativen Shader-Entwicklungszyklus nützlich sein.                                                                                             |
| D3D10 \_ SHADER \_ OPTIMIZATION \_ LEVEL1             | Die zweit niedrigste Optimierungsstufe.                                                                                                                                                                                                              |
| D3D10 \_ SHADER \_ OPTIMIZATION \_ LEVEL2             | Die zweit höchste Optimierungsstufe.                                                                                                                                                                                                             |
| D3D10 \_ SHADER \_ OPTIMIZATION \_ LEVEL3             | Höchste Optimierungsstufe. Erzeugt den bestmöglichen Code, kann aber deutlich länger dauern. Dies ist nützlich für endgültige Builds einer Anwendung, bei denen die Leistung der wichtigste Faktor ist.                                 |
| D3D10 \_ SHADER \_ PACK \_ MATRIX \_ ROW \_ MAJOR         | Sofern nicht explizit angegeben, werden Matrizen in Zeilen-Hauptreihen-Reihenfolge für die Eingabe und Ausgabe des Shaders gepackt.                                                                                                                                   |
| D3D10 \_ SHADER \_ PACK \_ MATRIX \_ COLUMN \_ MAJOR      | Sofern nicht explizit angegeben, werden Matrizen in Spaltenmatrizen nach Eingabe und Ausgabe des Shaders gepackt. Dies ist im Allgemeinen effizienter, da sie die Vektormatrixmultiplikation mit einer Reihe von Punktprodukten ermöglicht. |
| TEILGENAUIGKEIT DES \_ D3D10-SHADERS \_ \_               | Erzwingen, dass alle Berechnungen mit teilweiser Genauigkeit durchgeführt werden; dies kann auf einigen Hardwarekomponenten schneller ausgeführt werden.                                                                                                                                                |
| D3D10-SHADER \_ \_ BEVORZUGEN \_ \_ FLUSSSTEUERUNG            | Informieren Sie den Compiler, die Flusssteuerung zu verwenden (wenn möglich).                                                                                                                                                                                             |
| D3D10 \_ SHADER \_ SKIP \_ OPTIMIZATION               | Überspringen der Optimierung während der Codegenerierung; wird im Allgemeinen nur für das Debuggen empfohlen.                                                                                                                                                                |
| D3D10-SHADER \_ – \_ ÜBERPRÜFUNG \_ ÜBERSPRINGEN                 | Überprüfen Sie den generierten Code nicht anhand bekannter Funktionen und Einschränkungen. Verwenden Sie dies nur mit Shadern, die in der Vergangenheit erfolgreich kompiliert wurden. Shader werden immer von DirectX überprüft, bevor sie auf das Gerät festgelegt werden.         |
| \_D3D10-SHADERWARNUNGEN \_ \_ SIND \_ FEHLER            | Informieren Sie den HLSL-Compiler, alle Warnungen beim Kompilieren des Shadercodes als Fehler zu behandeln. Für neuen Shadercode sollten Sie diese Option verwenden, um alle Warnungen aufzulösen und so sicherzustellen, dass möglichst wenig schwer zu findende Codefehler angezeigt werden.             |



 

Diese Konstanten werden in d3d10shader.h als Makros definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shaderkonst constants (Shaderkonst constants)](d3d10-graphics-reference-d3d10-shader-constants.md)
</dt> </dl>

 

 



