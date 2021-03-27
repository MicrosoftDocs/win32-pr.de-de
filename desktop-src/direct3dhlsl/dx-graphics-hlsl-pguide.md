---
title: Programmier Handbuch für HLSL
description: Daten werden als Datenstrom von primitiven in die Grafik Pipeline eingegeben und von den Shader-Stufen verarbeitet.
ms.assetid: 4894e085-30e7-4cc5-8ae6-a84b601e4ce3
ms.topic: article
ms.date: 02/21/2019
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cd242efaaf3cdb44f424a603f2fc522dda540ec8
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2021
ms.locfileid: "104980976"
---
# <a name="programming-guide-for-hlsl"></a>Programmier Handbuch für HLSL

Daten werden als Datenstrom von primitiven in die Grafik Pipeline eingegeben und von den Shader-Stufen verarbeitet. Die eigentlichen Shader-Stufen sind von der Direct3D-Version abhängig, sind aber sicherlich in den Phasen Scheitelpunkt, Pixel und Geometrie enthalten. Zu den anderen Phasen gehören die Hülle und die Domänen-Shader für Mosaik und der COMPUTE-Shader. Diese Phasen sind vollständig programmierbar, indem die High Level Shading Language ([HLSL](dx-graphics-hlsl-reference.md)) verwendet wird.

HLSL-Shader können zur Laufzeit oder zur Laufzeit kompiliert und zur Laufzeit in die entsprechende Pipeline Phase festgelegt werden. Direct3D 9-Shader können mit [Shadermodell 1](dx-graphics-hlsl-sm1.md), [Shader Model 2](dx-graphics-hlsl-sm2.md) und [Shader Model 3](dx-graphics-hlsl-sm3.md)entworfen werden. Direct3D 10-Shader können nur auf [Shadermodell 4](dx-graphics-hlsl-sm4.md)ausgelegt werden. Direct3D 11-Shader können auf [Shader-Modell 5](d3d11-graphics-reference-sm5.md)entworfen werden. Direct3D 11,3 und Direct3D 12 können auf [Shader-Modell 5,1](shader-model-5-1.md)entworfen werden, und Direct3D 12 kann auch auf [Shader-Modell 6](shader-model-6-0.md)entworfen werden.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [Verwenden der Shader-Verknüpfung](using-shader-linking.md) | Wir zeigen, wie vorkompilierte HLSL-Funktionen erstellt, in Bibliotheken Verpacken und zur Laufzeit mit vollständigen Shadern verknüpft werden. |
| [Schreiben von HLSL-Shadern in Direct3D 9](dx-graphics-hlsl-writing-shaders-9.md) | |
| [Verwenden von Shadern in Direct3D 9](dx-graphics-hlsl-using-shaders-9.md) | |
| [Verwenden von Shadern in Direct3D 10](dx-graphics-hlsl-using-shaders-10.md) | |
| [Optimieren von HLSL-Shadern](dx-graphics-hlsl-optimize.md) | |
| [Debuggen von Shadern in Visual Studio](dx-graphics-hlsl-debug-visual-studio.md) | Das aktuellste Tool zum Debuggen von Shadern ist nun als Feature in Microsoft Visual Studio enthalten, das als Visual Studio-Grafik Debugger bezeichnet wird.  |
| [Kompilieren von Shadern](dx-graphics-hlsl-part1.md) | Sehen wir uns nun verschiedene Möglichkeiten zum Kompilieren Ihres shadercodes und Konventionen für Dateierweiterungen für Shader-Code an. |
| [Angeben von compilerzielen](specifying-compiler-targets.md) | Hier werden die Ziele für verschiedene Profile aufgelistet, die von den Funktionen **D3DCompile \** _ und dem HLSL-Compiler unterstützt werden. |
| [Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung](dx-graphics-hlsl-unpacking-packing-dxgi-format.md) | |
| [Verwenden der minimalen Genauigkeit von HLSL](using-hlsl-minimum-precision.md) | Ab Windows 8 können Grafiktreiber minimale Genauigkeit der [HLSL-Skalardatentypen](dx-graphics-hlsl-scalar.md) implementieren, indem Sie eine beliebige Genauigkeit angeben, die größer oder gleich der angegebenen bitgenauigkeit ist.  |
| [HLSL-Shader-Modell 5](overviews-direct3d-11-hlsl.md) | |
| [HLSL-Shader-Modell 5,1](hlsl-shader-model-5-1-features-for-direct3d-12.md) | In diesem Abschnitt werden die Features des Shader-Modells 5,1 beschrieben, die in der Praxis auf D3D12 und D3D 11.3 zutreffen. Die gesamte DirectX 12-Hardware unterstützt das Shader-Modell 5,1. |
| [HLSL-Shader-Modell 6,0](hlsl-shader-model-6-0-features-for-direct3d-12.md) | Beschreibt die systeminternen Wellen Vorgangs Funktionen, die dem HLSL-Shader-Modell 6,0 hinzugefügt werden. |
| [HLSL-Shader-Modell 6,4](hlsl-shader-model-6-4-features-for-direct3d-12.md) | Beschreibt die Machine Learning-systeminternen Funktionen, die dem HLSL-Shadermodell 6,4 hinzugefügt werden. |

## <a name="related-topics"></a>Zugehörige Themen

_ [HLSL](dx-graphics-hlsl.md)
* [Verweis für HLSL](dx-graphics-hlsl-reference.md)
