---
title: Vertex-Shaderphase
description: Die Vertex-Shader-Phase (VS) verarbeitet Scheitelpunkte aus dem Eingabe-Assembler und verarbeitet scheitelpunktspezifische Vorgänge wie Transformationen, Skinning, Morphing und Beleuchtung pro Scheitelpunkt.
ms.assetid: C6A39F48-A243-4049-8AED-0B521BEDFA76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3815f4c26c97e68ac0b4b20b72849052710f2f6adc0722bb3e42f5c8bf7a1c89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530408"
---
# <a name="vertex-shader-stage"></a>Vertex-Shaderphase

Die Vertex-Shader-Phase (VS) verarbeitet Scheitelpunkte aus dem Eingabe-Assembler und verarbeitet scheitelpunktspezifische Vorgänge wie Transformationen, Skinning, Morphing und Beleuchtung pro Scheitelpunkt. Vertex-Shader arbeiten immer mit einem einzelnen Eingabevertex und erzeugen einen einzelnen Ausgabevertex. Die Vertex-Shaderphase muss immer aktiv sein, damit die Pipeline ausgeführt werden kann. Wenn keine Scheitelpunktänderung oder -transformation erforderlich ist, muss ein Pass-Through-Vertex-Shader erstellt und auf die Pipeline festgelegt werden.

## <a name="the-vertex-shader"></a>Vertex-Shader

Jeder Vertex-Shader-Eingabevertex kann aus bis zu 16 32-Bit-Vektoren (bis zu 4 Komponenten) bestehen, und jeder Ausgabevertex kann aus bis zu 16 32-Bit-4-Komponentenvektoren bestehen. Alle Vertex-Shader müssen mindestens eine Eingabe und eine Ausgabe haben, die so wenig wie ein Skalarwert sein kann.

Die Vertex-Shader-Stufe kann zwei vom System generierte Werte des Eingabe-Assemblers nutzen: VertexID und InstanceID (siehe Systemwerte und Semantik). Da VertexID und InstanceID auf Scheitelpunktebene sinnvoll sind und von Hardware generierte IDs nur in die erste Stufe eingespeist werden können, die sie versteht, können diese ID-Werte nur in die Vertex-Shader-Stufe eingespeist werden.

Vertex-Shader werden immer auf allen Scheitelpunkte ausgeführt, einschließlich benachbarter Scheitelpunkte in primitiven Eingabetopologien mit Adjakenz. Die Anzahl der Ausführungen des Scheitelpunkt-Shaders kann mithilfe der VSInvocations-Pipelinestatistik von der CPU abgefragt werden.

Ein Vertex-Shader kann Auslastungs- und Texturstastingvorgänge ausführen, bei denen keine Ableitungen des Bildschirmraums erforderlich sind (mit systeminternen HLSL-Funktionen: [Sample (DirectX HLSL Texture Object)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-sample), [SampleCmpLevelZero (DirectX HLSL Texture Object)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero)und [SampleGrad (DirectX HLSL Texture Object)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplegrad)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafikpipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipelinestufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 