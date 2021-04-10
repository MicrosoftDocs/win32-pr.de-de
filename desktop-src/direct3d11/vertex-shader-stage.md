---
title: Vertex-Shader-Phase
description: Die Vertex-Shader (VS)-Phase verarbeitet Scheitel Punkte vom Eingabe Assembler und führt Vorgänge pro Scheitelpunkt aus, z. b. Transformationen, Skinning, morphung und pro-Vertex-Beleuchtung.
ms.assetid: C6A39F48-A243-4049-8AED-0B521BEDFA76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19a291b4abed572da54f9a2616ce19e926e1c6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039018"
---
# <a name="vertex-shader-stage"></a>Vertex-Shader-Phase

Die Vertex-Shader (VS)-Phase verarbeitet Scheitel Punkte vom Eingabe Assembler und führt Vorgänge pro Scheitelpunkt aus, z. b. Transformationen, Skinning, morphung und pro-Vertex-Beleuchtung. Vertex-Shader arbeiten immer auf einem einzelnen Eingabe Scheitelpunkt und liefern einen einzelnen Ausgabe Scheitelpunkt. Die Vertex-Shader-Stufe muss immer aktiv sein, damit die Pipeline ausgeführt werden muss. Wenn keine Scheitelpunkt Änderung oder-Transformation erforderlich ist, muss ein Pass-Through-Vertex-Shader erstellt und auf die Pipeline festgelegt werden.

## <a name="the-vertex-shader"></a>Der Vertex-Shader

Jeder Scheitelpunkt für Scheitelpunkt-Shader-Eingaben kann aus bis zu 16 32-Bit-Vektoren (jeweils bis zu 4 Komponenten) bestehen, und jeder Ausgabe Scheitelpunkt kann aus bis zu 16 32-Bit-vier-Komponenten-Vektoren bestehen. Alle Vertex-Shader müssen mindestens eine Eingabe und eine Ausgabe aufweisen, die nur einen skalaren Wert aufweisen kann.

Die Vertex-Shader-Phase kann zwei vom systemgenerierte Werte aus dem Eingabe Assembler nutzen: vertexid und InstanceId (siehe System Werte und Semantik). Da vertexid und InstanceId auf einer Scheitelpunkt Ebene aussagekräftig sind und von der Hardware generierte IDs nur in die erste Phase eingespeist werden können, die Sie versteht, können diese ID-Werte nur in die Vertex-Shader-Phase eingespeist werden.

Vertex-Shader werden immer auf allen Scheitel Punkten ausgeführt, einschließlich angrenzender Scheitel Punkte in eingegebenen primitiven Topologien. Die Häufigkeit, mit der der Vertex-Shader ausgeführt wurde, kann mithilfe der Pipeline Statistik der vsinvocations von der CPU abgefragt werden.

Ein Vertex-Shader kann Lade-und Textur-samplingvorgänge ausführen, bei denen keine Bildschirmspeicher Ableitungen erforderlich sind (mit systeminternen HLSL-Funktionen: [Sample (DirectX HLSL Texture Object)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-sample), [samplecmplevelzero (DirectX HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero)Texture Object) und [samplegrad (DirectX HLSL Texture Object)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplegrad)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafik Pipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipeline Stufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 