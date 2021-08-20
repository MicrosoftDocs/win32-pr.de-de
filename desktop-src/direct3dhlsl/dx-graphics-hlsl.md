---
title: High-Level-Shaderprogrammiersprache (HLSL)
description: HLSL ist die C-fähige Shadersprache auf hoher Ebene, die Sie mit programmierbaren Shadern in DirectX verwenden.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: 9f518102b7b3305103ed85231a791c542418a04c
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812896"
---
# <a name="high-level-shader-language-hlsl"></a>High-Level-Shaderprogrammiersprache (HLSL)

HLSL ist die C-fähige Shadersprache auf hoher Ebene, die Sie mit programmierbaren Shadern in DirectX verwenden.

Beispielsweise können Sie HLSL verwenden, um einen [Vertex-Shader](../direct3d11/vertex-shader-stage.md)oder einen Pixel-Shader zu schreiben und diese [Shader](../direct3d11/pixel-shader-stage.md)in der Implementierung des Renderers in Ihrer [Direct3D-Anwendung zu](../direct3d12/directx-12-programming-guide.md) verwenden.

Oder Sie können HLSL verwenden, um einen Compute-Shader zu schreiben, z. B. um eine physikalische Simulation zu implementieren. Wenn Sie z. B. versuchen, Ihren eigenen Convolution-Operator (für die Bildverarbeitung) als HLSL in einem Compute-Shader zu schreiben, erhalten Sie in diesem Szenario eine bessere Leistung, wenn Sie stattdessen [Direct Machine Learning (DirectML)](/windows/ai/directml/dml) verwenden.

HLSL wurde (ab DirectX 9) erstellt, um die programmierbare 3D-Pipeline [zu einrichten.](../direct3d11/overviews-direct3d-11-graphics-pipeline.md) Sie können die gesamte Pipeline mit HLSL-Anweisungen programmieren.

## <a name="where-to-go-next"></a>Nächste Schritte

* [Programmierhandbuch für HLSL](./dx-graphics-hlsl-pguide.md)
* [Referenz zu HLSL](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a>Programmierhandbuch für HLSL

Eine konzeptionelle Einführung in HLSL finden Sie im [Programmierhandbuch für HLSL.](./dx-graphics-hlsl-pguide.md)

Im Programmierhandbuch werden die verschiedenen Arten von Shaderstufen sowie das Erstellen, Kompilieren, Optimieren, Binden und Verknüpfen von Shadern erläutert.

Dort finden Sie auch Übersichten und Versionshinweise zu den nachfolgenden Generationen von Shadermodellversionen, die veröffentlicht wurden, bis hin zum HLSL-Shadermodell 5.

### <a name="reference-for-hlsl"></a>Referenz zu HLSL

Die HLSL-Referenzdokumentation finden Sie in der [Referenz zu HLSL.](./dx-graphics-hlsl-reference.md)

Der Referenzabschnitt enthält eine vollständige Liste der Sprachsyntax und der systeminternen Funktionen, die in HLSL integriert sind, um Ihre Codierungsanforderungen zu vereinfachen.

Dort finden Sie auch eine Erörterung von Shadermodellen im Vergleich zu Profilen und Referenzinhalt des Shadermodells bis hin zum HLSL-Shadermodell 1. Es gibt auch Inhalt, der Assemblyanweisungen, das D3DCompiler-Tool und Informationen zu den Fehlern und Warnungen enthält, die ein Shader zurückgeben kann.