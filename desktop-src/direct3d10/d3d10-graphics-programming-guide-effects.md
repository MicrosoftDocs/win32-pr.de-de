---
description: Erfahren Sie mehr über Direct3D 10-Effekte. Ein Effekt ist der Pipelinezustand, der durch in HLSL geschriebene Ausdrücke und eine syntaxspezifische Syntax für das Effektframework festgelegt wird.
ms.assetid: db4c7651-b6a1-4bc3-bcf8-a5cb56c7563e
title: Effekte (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70a9a863fd34c5bb99389139d09860812b16b4fa
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010913"
---
# <a name="effects-direct3d-10"></a>Effekte (Direct3D 10)

Ein DirectX-Effekt ist eine Auflistung des Pipelinezustands, der durch in [HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) geschriebene Ausdrücke und eine syntaxspezifische Syntax für das Effektframework festgelegt wird. Verwenden Sie nach dem Kompilieren eines Effekts die Effektframework-APIs zum Rendern. Die Effektfunktionalität kann so einfach sein wie ein Vertex-Shader, der geometrie transformiert, und ein Pixel-Shader, der eine Volltonfarbe ausgibt, bis hin zu einer Renderingtechnik, die mehrere Durchläufe erfordert, jede Phase der Grafikpipeline verwendet und den Shaderzustand sowie den Pipelinezustand bearbeitet, der nicht den programmierbaren Shadern zugeordnet ist.

Der erste Schritt besteht im Organisieren des Zustands, den Sie in einem Effekt steuern möchten. Dies schließt shader state (vertex, geometry and pixel shaders), texture and sampler state used by the shaders und other non-programmable pipeline state(Shaderzustand (Vertex-, Geometrie- und Pixel-Shader), textur- und sampler-Zustand, der von den Shadern verwendet wird, und andere nicht programmierbare Pipelinestatus ein. Sie können einen Effekt im Arbeitsspeicher als Textzeichenfolge erstellen, aber in der Regel wird die Größe so groß, dass es praktisch ist, den Effektzustand in einer Effektdatei (einer Textdatei, die mit der Erweiterung .fx endet) zu speichern. Um einen Effekt zu verwenden, müssen Sie ihn kompilieren (um die HLSL-Syntax sowie die Effektframeworksyntax zu überprüfen), den Effektzustand über API-Aufrufe initialisieren und die Renderschleife so ändern, dass die Rendering-APIs aufrufen.

-   [Organisieren des Zustands in einem Effekt](d3d10-graphics-programming-guide-effects-organize.md)
-   [Effect-Systemschnittstellen](d3d10-graphics-programming-guide-effects-interfaces.md)
-   [Spezielle Schnittstellen](d3d10-graphics-reference-effect-specializing.md)
-   [Rendern eines Effekts](d3d10-graphics-programming-guide-effects-render.md)

Ein Effekt kapselt den render-Zustand, der für einen bestimmten Effekt erforderlich ist, in einer einzelnen Renderingfunktion, die als Technik bezeichnet wird. Ein Durchgang ist ein Teilsatz einer Technik, die den Renderzustand enthält. Implementieren Sie einen oder mehrere Durchläufe innerhalb einer Technik, um einen Multiple-Pass-Renderingeffekt zu implementieren. Beispiel: Sie möchten eine Geometrie mit einem Satz von Tiefen-/Schablonenpuffern rendern und dann einige Sprites darauf zeichnen. Sie können das Geometrierendering im ersten Durchgang und die Sprite-Zeichnung im zweiten Durchgang implementieren. Um den Effekt zu rendern, rendern Sie einfach beide Durchläufe in der Renderschleife. Sie können eine beliebige Anzahl von Techniken in einem Effekt implementieren. Je größer die Anzahl der Techniken, desto größer ist die Kompilierzeit für den Effekt. Eine Möglichkeit, diese Funktionalität zu nutzen, besteht in der Erstellung von Effekten mit Techniken, die für die Ausführung auf unterschiedlicher Hardware entwickelt wurden. Dadurch kann eine Anwendung die Leistung basierend auf den erkannten Hardwarefunktionen ordnungsgemäß herabstufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
