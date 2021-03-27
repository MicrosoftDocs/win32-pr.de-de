---
title: Shader-Modell 5
description: Dieser Abschnitt enthält die Referenzseiten für HLSL-Shader-Modell 5.
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f379301008190367a40959a319d01cfad127f6b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390513"
---
# <a name="shader-model-5"></a>Shader-Modell 5

Dieser Abschnitt enthält die Referenzseiten für HLSL-Shader-Modell 5.

Shader Model 5 ist eine supermenge der untergeordneten Funktionen in [Shader Model 4](dx-graphics-hlsl-sm4.md). Es wurde mithilfe eines gemeinsamen Shader-Kerns entworfen, der einen gemeinsamen Satz von Features für alle programmierbaren Shader bereitstellt, die nur mit HLSL programmierbar sind.



| Feature                   | Funktion                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Instruktionssatz           | [**Intrinsische HLSL-Funktionen**](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| Vertex-Shader Max         | Keine Einschränkung                                                                                                                                         |
| Pixel-Shader max.          | Keine Einschränkung                                                                                                                                         |
| Neue shaderprofile hinzugefügt | CS \_ 4 \_ 0, GS \_ 4 \_ 0 \* , PS \_ 4 \_ 0 \* , vs \_ 4 \_ 0 \* , CS \_ 4 \_ 1, GS \_ 4 \_ 1 \* , PS \_ 4 \_ 1 \* , vs \_ 4 \_ 1 \* , CS \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 \_ 0, vs \_ 5 \_ 0 |



 

\* -GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 und vs \_ 4 \_ 1 wurden im Shader-Modell 4,0 eingeführt. DirectX 11 fügt jedoch Unterstützung für [strukturierte Puffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) und Byte Adress Puffer für Shader Model 4, die auf DirectX 10-Hardware ausgeführt wird, hinzu.

Shader Model 5 führt den [Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) ein, der hoch Geschwindigkeits Computing für allgemeine Zwecke bereitstellt.

Eine ausführlichere Liste der Shader Model 5-Features finden Sie in einer Auflistung der [Direct3D 11-Features](/windows/desktop/direct3d11/direct3d-11-features).

Im Abschnitt [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) werden die Assemblyanweisungen beschrieben, die das Shadermodell 5 unterstützt.

## <a name="in-this-section"></a>In diesem Abschnitt



| Element                                                                                                                                                                                                                                                        | BESCHREIBUNG                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Shader Model 5-Attribute](d3d11-graphics-reference-sm5-attributes.md)<br/>                                     | Referenzseiten für Shader Model 5-Attribute.<br/>          |
| <span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Intrinsische Funktionen von Shader Model 5](d3d11-graphics-reference-sm5-intrinsics.md)<br/> | Referenzseiten für intrinsische Shader Model 5-Funktionen.<br/> |
| <span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Shader Model 5-Objekte](d3d11-graphics-reference-sm5-objects.md)<br/>                                                    | Referenzseiten für Shader Model 5-Objekte und-Methoden.<br/> |
| <span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Shader-Modell 5-System Werte](d3d11-graphics-reference-sm5-system-values.md)<br/>                      | Referenzseiten für Shader Model 5-System Werte.<br/>       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Modelle vs shaderprofile](dx-graphics-hlsl-models.md)
</dt> </dl>

 

