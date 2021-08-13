---
title: Shaderstrukturen (Direct3D 11-Grafiken)
description: Strukturen werden verwendet, um Shader zu erstellen und zu verwenden.
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- structures, Direct3D 11 Shaders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f5f5c346e4f46b1ca108200a88ae8b2ad3540585fd1a4bfc73b1dafe2b2b16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408190"
---
# <a name="shader-structures-direct3d-11-graphics"></a>Shaderstrukturen (Direct3D 11-Grafiken)

Strukturen werden verwendet, um Shader zu erstellen und zu verwenden.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                       | BESCHREIBUNG                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**D3D11-KLASSENINSTANZ \_ \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | Beschreibt eine HLSL-Klasseninstanz.<br/>                           |
| [**D3D11 \_ COMPUTE \_ SHADER \_ TRACE \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | Beschreibt eine Instanz eines zu verfolgenden Compute-Shaders.<br/>         |
| [**D3D11 \_ DOMAIN \_ SHADER \_ TRACE \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | Beschreibt eine Instanz eines Zu verfolgenden Domänen-Shaders.<br/>          |
| [**D3D11 \_ FUNCTION \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | Beschreibt eine Funktion.<br/>                                       |
| [**D3D11 \_ GEOMETRY \_ SHADER \_ TRACE \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | Beschreibt eine Instanz eines zu verfolgenden Geometrie-Shaders.<br/>        |
| [**D3D11 \_ – ABLAUFVERFOLGUNGS-DESC \_ FÜR DEN HÜLLEN-SHADER \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | Beschreibt eine Instanz eines zu verfolgenden Hüllen-Shaders.<br/>            |
| [**D3D11 \_ LIBRARY \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | Beschreibt eine Bibliothek.<br/>                                        |
| [**D3D11 \_ PARAMETER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | Beschreibt einen Funktionsparameter. <br/>                            |
| [**D3D11 \_ PIXEL \_ SHADER \_ TRACE \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | Beschreibt eine Instanz eines zu verfolgenden Pixel-Shaders.<br/>           |
| [**D3D11 \_ SHADER \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | Beschreibt einen Shader-Konstantenpuffer.<br/>                         |
| [**D3D11 \_ SHADER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | Beschreibt einen Shader.<br/>                                         |
| [**D3D11 \_ SHADER \_ INPUT \_ BIND \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | Beschreibt, wie eine Shaderressource an eine Shadereingabe gebunden wird.<br/> |
| [**D3D11 \_ SHADER \_ TRACE \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | Beschreibt ein Shader-Ablaufverfolgungsobjekt.<br/>                            |
| [**D3D11 \_ SHADER \_ TYPE \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | Beschreibt einen Shadervariablentyp.<br/>                           |
| [**D3D11 \_ SHADER \_ VARIABLE \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | Beschreibt eine Shadervariable.<br/>                                |
| [**D3D11 \_ SIGNATURE \_ PARAMETER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | Beschreibt eine Shadersignatur.<br/>                               |
| [**D3D11 – \_ ABLAUFVERFOLGUNGSREGISTER \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | Beschreibt ein Ablaufverfolgungsregister.<br/>                                 |
| [**D3D11 \_ TRACE \_ STATS**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | Gibt Statistiken zu einer Ablaufverfolgung an.<br/>                         |
| [**ABLAUFVERFOLGUNGSSCHRITT D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | Beschreibt einen Ablaufverfolgungsschritt, bei dem es sich um eine Anweisung handelt.<br/>            |
| [**D3D11 \_ TRACE \_ VALUE**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | Beschreibt einen Ablaufverfolgungswert.<br/>                                    |
| [**D3D11 \_ VERTEX \_ SHADER \_ TRACE \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | Beschreibt eine Instanz eines vertex-Shaders für die Ablaufverfolgung.<br/>          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Referenz](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





