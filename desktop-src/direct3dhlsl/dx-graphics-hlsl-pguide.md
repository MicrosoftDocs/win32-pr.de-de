---
title: Programmierhandbuch für HLSL
description: Daten werden als Datenstrom primitiver Typen in die Grafikpipeline übertragen und von den Shaderstufen verarbeitet.
ms.assetid: 4894e085-30e7-4cc5-8ae6-a84b601e4ce3
ms.topic: article
ms.date: 02/21/2019
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca0b1f93b3c5f56cd7a074571ec6657cedc924688606e3612a66ef0f9e40d51e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726069"
---
# <a name="programming-guide-for-hlsl"></a>Programmierhandbuch für HLSL

Daten werden als Datenstrom primitiver Typen in die Grafikpipeline übertragen und von den Shaderstufen verarbeitet. Die tatsächlichen Shaderstufen hängen von der Version von Direct3D ab, enthalten jedoch sicherlich die Scheitelpunkt-, Pixel- und Geometriestufen. Andere Phasen umfassen die Hülle und Domänen-Shader für Mosaik und den Compute-Shader. Diese Phasen sind mithilfe der High Level Shading Language[(HLSL) vollständig programmierbar.](dx-graphics-hlsl-reference.md)

HLSL-Shader können zur Erstellungszeit oder zur Laufzeit kompiliert und zur Laufzeit in die entsprechende Pipelinephase festgelegt werden. Direct3D 9-Shader können mit [Shadermodell 1,](dx-graphics-hlsl-sm1.md) [Shadermodell 2](dx-graphics-hlsl-sm2.md) und [Shadermodell 3 entworfen werden.](dx-graphics-hlsl-sm3.md) Direct3D 10-Shader können nur auf [Shadermodell 4 entworfen werden.](dx-graphics-hlsl-sm4.md) Direct3D 11-Shader können auf [Shadermodell 5 entworfen werden.](d3d11-graphics-reference-sm5.md) Direct3D 11.3 und Direct3D 12 können auf [Shadermodell 5.1](shader-model-5-1.md)und Direct3D 12 auch auf [Shadermodell 6](shader-model-6-0.md)entworfen werden.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [Verwenden der Shaderverknüpfung](using-shader-linking.md) | Wir zeigen, wie Sie vorkompilierte HLSL-Funktionen erstellen, diese in Bibliotheken packen und zur Laufzeit mit vollständigen Shadern verknüpfen. |
| [Schreiben von HLSL-Shadern in Direct3D 9](dx-graphics-hlsl-writing-shaders-9.md) | |
| [Verwenden von Shadern in Direct3D 9](dx-graphics-hlsl-using-shaders-9.md) | |
| [Verwenden von Shadern in Direct3D 10](dx-graphics-hlsl-using-shaders-10.md) | |
| [Optimieren von HLSL-Shadern](dx-graphics-hlsl-optimize.md) | |
| [Debuggen von Shadern in Visual Studio](dx-graphics-hlsl-debug-visual-studio.md) | Das neueste Tool zum Debuggen von Shadern ist jetzt als Feature in Microsoft Visual Studio, das als Visual Studio-Debugger bezeichnet wird.  |
| [Kompilieren von Shadern](dx-graphics-hlsl-part1.md) | Sehen wir uns nun verschiedene Möglichkeiten zum Kompilieren Ihres Shadercodes und konventionen für Dateierweiterungen für Shadercode an. |
| [Angeben von Compilerzielen](specifying-compiler-targets.md) | Hier werden die Ziele für verschiedene Profile aufgeführt, die von **den \* D3DCompile-Funktionen** und dem HLSL-Compiler unterstützt werden. |
| [Entpacken und Packen des \_ DXGI-FORMATS für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md) | |
| [Verwenden der minimalen Genauigkeit von HLSL](using-hlsl-minimum-precision.md) | Ab Windows 8 können Grafiktreiber HLSL-Skalardatentypen mit minimaler Genauigkeit implementieren, indem sie eine beliebige Genauigkeit verwenden, die größer oder gleich der angegebenen Bitgenauigkeit ist. [](dx-graphics-hlsl-scalar.md)  |
| [HLSL-Shadermodell 5](overviews-direct3d-11-hlsl.md) | |
| [HLSL-Shadermodell 5.1](hlsl-shader-model-5-1-features-for-direct3d-12.md) | In diesem Abschnitt werden die Features des Shadermodells 5.1 beschrieben, die in der Praxis für D3D12 und D3D11.3 gelten. Alle DirectX 12-Hardware unterstützt ShaderModell 5.1. |
| [HLSL Shader Model 6.0](hlsl-shader-model-6-0-features-for-direct3d-12.md) | Beschreibt die systeminternen Wellenvorgang-Funktion, die hlsl-Shadermodell 6.0 hinzugefügt wurde. |
| [HLSL-Shadermodell 6.4](hlsl-shader-model-6-4-features-for-direct3d-12.md) | Beschreibt die systeminternen Machine Learning-Eigenschaften, die dem HLSL-Shadermodell 6.4 hinzugefügt wurden. |

## <a name="related-topics"></a>Zugehörige Themen

* [Hlsl](dx-graphics-hlsl.md)
* [Referenz zu HLSL](dx-graphics-hlsl-reference.md)
