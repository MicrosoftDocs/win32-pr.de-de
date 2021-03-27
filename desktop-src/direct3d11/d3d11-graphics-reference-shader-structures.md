---
title: Shaderstrukturen (Direct3D 11-Grafiken)
description: Strukturen werden verwendet, um Shaders zu erstellen und zu verwenden.
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- Strukturen, Direct3D 11-Shader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14739e3db38c075e19e58a90b12bbf7d06b48a4e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739592"
---
# <a name="shader-structures-direct3d-11-graphics"></a>Shaderstrukturen (Direct3D 11-Grafiken)

Strukturen werden verwendet, um Shaders zu erstellen und zu verwenden.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                       | BESCHREIBUNG                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**D3D11- \_ Klassen \_ Instanz \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | Beschreibt eine HLSL-Klasseninstanz.<br/>                           |
| [**D3D11-Ablauf \_ Verfolgung für Compute- \_ Shader \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | Beschreibt eine Instanz eines Compute-Shaders für die Ablauf Verfolgung.<br/>         |
| [**D3D11 \_ Domänen- \_ Shader-Ablauf \_ Verfolgung \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | Beschreibt eine Instanz eines Domänen-Shaders für die Ablauf Verfolgung.<br/>          |
| [**D3D11- \_ Funktion \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | Beschreibt eine Funktion.<br/>                                       |
| [**D3D11 \_ Geometry- \_ Shader- \_ \_ Ablaufverfolgungs-Debugger**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | Beschreibt eine Instanz eines Geometry-Shaders für die Ablauf Verfolgung.<br/>        |
| [**D3D11 \_ Hull- \_ Shader- \_ \_ Ablaufverfolgungs-Debugger**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | Beschreibt eine Instanz eines Hull-Shaders für die Ablauf Verfolgung.<br/>            |
| [**D3D11- \_ Bibliothek \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | Beschreibt eine Bibliothek.<br/>                                        |
| [**D3D11- \_ Parameter \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | Beschreibt einen Funktionsparameter. <br/>                            |
| [**D3D11 \_ Pixel- \_ Shader- \_ \_ Ablaufverfolgungs-Debugger**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | Beschreibt eine Instanz eines Pixelshaders für die Ablauf Verfolgung.<br/>           |
| [**D3D11- \_ Shader- \_ Puffer \_ Absteigend**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | Beschreibt einen Shader-Konstantenpuffer.<br/>                         |
| [**D3D11- \_ Shader- \_ Debugger**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | Beschreibt einen Shader.<br/>                                         |
| [**D3D11 \_ Shader \_ input \_ Bind \_ Debug**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | Beschreibt, wie eine Shaderressource an eine Shadereingabe gebunden wird.<br/> |
| [**D3D11- \_ Shader- \_ \_ Ablaufverfolgungs-Debug**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | Beschreibt ein Shader-Trace-Objekt.<br/>                            |
| [**D3D11 \_ \_ shadertyp \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | Beschreibt einen Shader-Variablentyp.<br/>                           |
| [**D3D11- \_ Shader- \_ Variable wird \_ deaktiviert**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | Beschreibt eine shadervariable.<br/>                                |
| [**D3D11 \_ Signatur \_ Parameter \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | Beschreibt eine shadersignatur.<br/>                               |
| [**D3D11-Ablauf \_ Verfolgungs \_ Register**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | Beschreibt ein Ablauf Verfolgungs Register.<br/>                                 |
| [**D3D11-Ablauf \_ Verfolgungs \_ Statistik**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | Gibt Statistiken zu einer Ablauf Verfolgung an.<br/>                         |
| [**D3D11-Ablauf \_ Verfolgungs \_ Schritt**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | Beschreibt einen Ablauf Verfolgungs Schritt, bei dem es sich um eine Anweisung handelt.<br/>            |
| [**D3D11-Ablauf \_ Verfolgungs \_ Wert**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | Beschreibt einen Ablauf Verfolgungs Wert.<br/>                                    |
| [**D3D11 \_ Vertex- \_ Shader-Ablauf \_ Verfolgung \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | Beschreibt eine Instanz eines Vertex-Shaders für die Ablauf Verfolgung.<br/>          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Referenz](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





