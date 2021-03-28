---
title: High-Level-Shaderprogrammiersprache (HLSL)
description: HLSL ist die C-ähnliche High-Level-Shader-Sprache, die Sie mit programmierbaren Shadern in DirectX verwenden.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: c0876cda302d4c6215b640c210e880795273cd6c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104981041"
---
# <a name="high-level-shader-language-hlsl"></a>High-Level-Shaderprogrammiersprache (HLSL)

HLSL ist die C-ähnliche High-Level-Shader-Sprache, die Sie mit programmierbaren Shadern in DirectX verwenden.

Beispielsweise können Sie HLSL zum Schreiben eines [Scheitel](../direct3d11/vertex-shader-stage.md)Punkt-Shader oder eines [Pixelshaders](../direct3d11/pixel-shader-stage.md)verwenden und diese Shader in der Implementierung des Renderers in Ihrer [Direct3D](../direct3d12/directx-12-programming-guide.md) -Anwendung verwenden.

Oder Sie können HLSL zum Schreiben eines Compute-Shaders verwenden, vielleicht um eine Physik Simulation zu implementieren. Wenn Sie z. b. einen eigenen Konvolution-Operator (für die Bildverarbeitung) als HLSL in einem Compute-Shader schreiben möchten, erzielen Sie in diesem Szenario eine bessere Leistung, wenn Sie stattdessen [Direct Machine Learning (directml)](../direct3d12/dml.md) verwenden.

HLSL wurde erstellt (beginnend mit DirectX 9), um die programmierbare 3D- [Pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md)einzurichten. Sie können die gesamte Pipeline mit HLSL-Anweisungen programmieren.

## <a name="where-to-go-next"></a>Nächste Schritt

* [Programmier Handbuch für HLSL](./dx-graphics-hlsl-pguide.md)
* [Verweis für HLSL](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a>Programmier Handbuch für HLSL

Eine konzeptionelle Einführung in HLSL finden Sie im [Programmier Handbuch für HLSL](./dx-graphics-hlsl-pguide.md).

Im Programmier Handbuch werden die unterschiedlichen Arten von Shader-Stufen erläutert, und es wird erläutert, wie Shaders erstellt, kompiliert, optimiert, gebunden und verknüpft werden.

Dort finden Sie auch Übersichten und Anmerkungen zu den aufeinander folgenden Generierungen der shadermodellversion, die veröffentlicht wurden, bis hin zu HLSL-Shader-Modell 5.

### <a name="reference-for-hlsl"></a>Verweis für HLSL

Die HLSL-Referenz Dokumentation finden Sie in der [Referenz für HLSL](./dx-graphics-hlsl-reference.md).

Der Referenz Abschnitt enthält eine komplette Liste der Sprachsyntax und der intrinsischen Funktionen, die in HLSL integriert sind, um Ihre Codierungs Anforderungen zu vereinfachen.

Außerdem finden Sie eine Erörterung von shadermodellen und Profilen, und der Shader-Modell Verweis Inhalt wird so weit wie das HLSL-Shader-Modell 1 zurückkehren. Es gibt auch Inhalte, die Assemblyanweisungen, das D3DCompiler-Tool und Informationen zu den Fehlern und Warnungen enthält, die ein Shader zurückgeben kann.