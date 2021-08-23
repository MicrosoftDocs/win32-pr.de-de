---
title: Shadermodell 5
description: Dieser Abschnitt enthält die Referenzseiten für HLSL Shader Model 5.
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a252c8ad3cc12c443506fbcc3802d9f1f7c15cfbe8cc62d937fcb9ca8723a8da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119371460"
---
# <a name="shader-model-5"></a>Shadermodell 5

Dieser Abschnitt enthält die Referenzseiten für HLSL Shader Model 5.

Shader Model 5 ist eine Obermenge der Funktionen in [Shader Model 4](dx-graphics-hlsl-sm4.md). Es wurde mit einem gemeinsamen Shaderkern entworfen, der einen gemeinsamen Satz von Features für alle programmierbaren Shader bietet, die nur mit HLSL programmierbar sind.



| Feature                   | Funktion                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Instruktionssatz           | [**Systeminterne HLSL-Funktionen**](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| Vertex-Shader Max.         | Keine Einschränkung                                                                                                                                         |
| Max. Pixel-Shader          | Keine Einschränkung                                                                                                                                         |
| Neue Shaderprofile hinzugefügt | cs \_ 4 \_ 0, gs \_ 4 \_ 0 \* , ps \_ 4 \_ 0 , vs \* \_ 4 \_ 0 , cs \* \_ 4 \_ 1, gs \_ 4 \_ 1 , ps \* \_ 4 \_ 1 , vs \* \_ 4 \_ 1 , cs \* \_ 5 \_ 0, ds \_ 5 \_ 0, gs \_ 5 \_ 0, hs \_ 5 \_ 0, ps \_ 5 \_ 0, vs \_ 5 \_ 0 |



 

\*– gs \_ 4 \_ 0, gs \_ 4 \_ 1, ps \_ 4 \_ 0, ps \_ 4 \_ 1, vs \_ 4 0 und vs \_ 4 1 wurden in \_ \_ Shader Model 4.0 eingeführt. DirectX 11 [](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) fügt jedoch Unterstützung für strukturierte Puffer und Byteadressenpuffer zu Shader Model 4 hinzu, das auf DirectX 10-Hardware ausgeführt wird.

Shader Model 5 führt den [Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) ein, der high-speed General Purpose Computing bietet.

Eine vollständige Liste der Features von Shader Model 5 ist in einer Liste der [Direct3D 11-Features enthalten.](/windows/desktop/direct3d11/direct3d-11-features)

Im [Abschnitt Shader Model 5 Assembly (Shadermodell 5-Assembly)](shader-model-5-assembly--directx-hlsl-.md) werden die Assemblyanweisungen beschrieben, die das Shadermodell 5 unterstützt.

## <a name="in-this-section"></a>In diesem Abschnitt



| Element                                                                                                                                                                                                                                                        | BESCHREIBUNG                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Shader Model 5-Attribute](d3d11-graphics-reference-sm5-attributes.md)<br/>                                     | Referenzseiten für Shader Model 5-Attribute.<br/>          |
| <span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Systeminterne Shadermodell 5-Funktionen](d3d11-graphics-reference-sm5-intrinsics.md)<br/> | Referenzseiten für systeminterne Shader Model 5-Funktionen.<br/> |
| <span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[ShaderModell 5-Objekte](d3d11-graphics-reference-sm5-objects.md)<br/>                                                    | Referenzseiten für Shader Model 5-Objekte und -Methoden.<br/> |
| <span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[ShaderModell 5– Systemwerte](d3d11-graphics-reference-sm5-system-values.md)<br/>                      | Referenzseiten für Shader Model 5-Systemwerte.<br/>       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodelle im Vergleich zu Shaderprofilen](dx-graphics-hlsl-models.md)
</dt> </dl>

 

