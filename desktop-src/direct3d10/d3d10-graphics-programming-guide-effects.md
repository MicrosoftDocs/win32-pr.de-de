---
description: Ein DirectX-Effekt ist eine Auflistung von Pipeline Zuständen, die durch in HLSL geschriebene Ausdrücke und eine bestimmte, für das Effect-Framework spezifische Syntax festgelegt ist.
ms.assetid: db4c7651-b6a1-4bc3-bcf8-a5cb56c7563e
title: Effekte (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e08d0c79a6f7f52982a74d5127da70d7b82f84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344373"
---
# <a name="effects-direct3d-10"></a>Effekte (Direct3D 10)

Ein DirectX-Effekt ist eine Auflistung von Pipeline Zuständen, die durch in [HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) geschriebene Ausdrücke und eine bestimmte, für das Effect-Framework spezifische Syntax festgelegt ist. Verwenden Sie nach dem Kompilieren eines Effekts die Effekt-Framework-APIs zum Rendering. Die Auswirkung der Funktionalität kann von etwas einfacher sein wie ein Vertexshader, der Geometrie transformiert, und ein Pixelshader, der eine voll Tonfarbe ausgibt, an eine renderingtechnik, die mehrere Durchgänge erfordert, jede Phase der Grafik Pipeline verwendet und den shaderzustand und den Pipeline Zustand, der den programmierbaren Shadern nicht zugeordnet ist, ändert.

Der erste Schritt besteht darin, den Zustand zu organisieren, den Sie steuern möchten. Dies schließt den Shader-Status (Scheitelpunkt, Geometrie und Pixel-Shader), den von den Shadern verwendeten Textur-und samplerzustand und anderen nicht programmierbaren Pipeline Status ein. Sie können einen Effekt im Arbeitsspeicher als Text Zeichenfolge erstellen, aber in der Regel ist die Größe so groß, dass es praktisch ist, den Effekt Zustand in einer Effekt Datei zu speichern (eine Textdatei, die auf eine FX-Erweiterung endet). Um einen Effekt zu erzielen, müssen Sie ihn kompilieren (um die HLSL-Syntax und die Effekt-Framework-Syntax zu überprüfen), den Effekt Zustand über API-Aufrufe initialisieren und die Renderingschleife ändern, um die Rendering-APIs aufzurufen.

-   [Anordnen des Zustands eines Effekts](d3d10-graphics-programming-guide-effects-organize.md)
-   [System Schnittstellen des Effekts](d3d10-graphics-programming-guide-effects-interfaces.md)
-   [Spezialisierte Schnittstellen](d3d10-graphics-reference-effect-specializing.md)
-   [Rendern eines Effekts](d3d10-graphics-programming-guide-effects-render.md)

Ein Effekt kapselt den gesamten renderzustand, der für einen bestimmten Effekt erforderlich ist, in eine einzelne Renderingfunktion, die als Technik bezeichnet wird. Ein Durchlauf ist eine Teilmenge einer Technik, die den renderzustand enthält. Implementieren Sie einen oder mehrere Durchgänge innerhalb eines Verfahrens, um einen Multipass-renderingeffekt zu implementieren. Angenommen, Sie möchten eine Geometrie mit einem Satz von tiefen-/Schablone-Puffern rendern und dann einige Sprites darauf zeichnen. Sie könnten das Geometrie Rendering im ersten Durchlauf und die Sprite-Zeichnung im zweiten Durchlauf implementieren. Um den Effekt zu rendereinigen, werden Sie einfach beide Pass-in der Renderschleife Render. Sie können eine beliebige Anzahl von Techniken in Kraft setzen. Natürlich ist die Anzahl der Techniken umso größer als die Kompilierzeit für den Effekt. Eine Möglichkeit, diese Funktionalität auszunutzen, ist das Erstellen von Effekten mit Techniken, die auf unterschiedlichen Hardware ausgeführt werden sollen. Dies ermöglicht es einer Anwendung, die Leistung basierend auf den erkannten Hardwarefunktionen ordnungsgemäß herabzusetzen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
