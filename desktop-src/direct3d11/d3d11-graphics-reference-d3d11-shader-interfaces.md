---
title: 'Shaderschnittstellen (Direct3D 11-Grafiken) '
description: Dieser Abschnitt enthält Informationen zu den Shaderschnittstellen.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- Schnittstellen, Direct3D 11-Shader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fcecdff6f35b634ecbbeca0b85bc5ba42fd1e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479456"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a>Shaderschnittstellen (Direct3D 11-Grafiken) 

Dieser Abschnitt enthält Informationen zu den Shaderschnittstellen.

Jede dieser Shaderschnittstellen verwaltet einen kompilierten Shader. Die -Schnittstelle wird erstellt, wenn ein Shader kompiliert wird, und dann an verschiedene APIs übergeben, die Zugriff auf einen kompilierten Shader benötigen. z. B. beim Binden eines Shaders an eine Pipelinephase oder beim Abrufen einer Shadersignatur.


## <a name="in-this-section"></a>In diesem Abschnitt




| Thema | BESCHREIBUNG | 
|-------|-------------|
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a><br /> | Diese Schnittstelle kapselt eine HLSL-Klasse.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a><br /> | Diese Schnittstelle kapselt eine dynamische HLSL-Verknüpfung.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a><br /> | Eine Compute-Shader-Schnittstelle verwaltet ein ausführbares Programm (einen Compute-Shader), das die Compute-Shader-Stufe steuert.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a><br /> | Eine Domänen-Shader-Schnittstelle verwaltet ein ausführbares Programm (einen Domänen-Shader), das die Domänen-Shader-Phase steuert.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a><br /> | Eine Schnittstelle für Funktionsverknüpfungsdiagramme wird verwendet, um Shader zu erstellen, die aus einer Sequenz von vorkompilierten Funktionsaufrufen bestehen, die Werte aneinander übergeben. <br /><blockquote>[!Note]<br />Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und zur Laufzeit in vollständige Shader zu verknüpfen.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a><br /> | Eine Funktionslektionsschnittstelle greifen auf Funktionsinformationen zu. <br /><blockquote>[!Note]<br />Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und zur Laufzeit in vollständige Shader zu verknüpfen.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a><br /> | Eine Funktionsparameter-Reflektionsschnittstelle greifen auf Funktionsparameterinformationen zu. <br /><blockquote>[!Note]<br />Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und zur Laufzeit in vollständige Shader zu verknüpfen.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a><br /> | Eine geometry-shader-Schnittstelle verwaltet ein ausführbares Programm (einen Geometrie-Shader), das die Geometry-Shader-Stufe steuert.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a><br /> | Eine Hülle-Shader-Schnittstelle verwaltet ein ausführbares Programm (einen Hüllen-Shader), das die Hüllen-Shader-Stufe steuert.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a><br /> | Eine Bibliothekslektionsschnittstelle greifen auf Bibliotheksinformationen zu. <br /><blockquote>[!Note]<br />Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und zur Laufzeit in vollständige Shader zu verknüpfen.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a><br /> | Eine Linkerschnittstelle wird verwendet, um ein Shadermodul zu verknüpfen. <br /><blockquote>[!Note]<br />Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und zur Laufzeit in vollständige Shader zu verknüpfen.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a><br /> | Eine Verknüpfungsknotenschnittstelle wird für Shaderverknüpfungen verwendet. <br /><blockquote>[!Note]<br />Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und zur Laufzeit in vollständige Shader zu verknüpfen.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a><br /> | Eine Modulschnittstelle erstellt eine Instanz eines Moduls, das für die Erneute Bindung von Ressourcen verwendet wird. <br /><blockquote>[!Note]<br />Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und zur Laufzeit in vollständige Shader zu verknüpfen.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a><br /> | Eine Modulinstanzschnittstelle wird für die Erneute Bindung von Ressourcen verwendet. <br /><blockquote>[!Note]<br />Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und zur Laufzeit in vollständige Shader zu verknüpfen.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a><br /> | Eine Pixel-Shader-Schnittstelle verwaltet ein ausführbares Programm (einen Pixel-Shader), das die Pixel-Shader-Stufe steuert.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a><br /> | Eine Shader-Reflektionsschnittstelle greifen auf Shaderinformationen zu.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a><br /> | Diese Shader-Reflektionsschnittstelle ermöglicht den Zugriff auf einen konstanten Puffer.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a><br /> | Diese Shader-Reflektionsschnittstelle ermöglicht den Zugriff auf den Variablentyp.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a><br /> | Diese Shader-Reflektionsschnittstelle ermöglicht den Zugriff auf eine Variable.<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a><br /> | Eine <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace-Schnittstelle</strong></a> implementiert Methoden zum Abrufen von Ablaufverfolgungen von Shaderausführungen.<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a><br /> | Eine <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory-Schnittstelle</strong></a> implementiert eine Methode zum Generieren von Shader-Ablaufverfolgungsinformationsobjekten.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a><br /> | Eine Vertex-Shader-Schnittstelle verwaltet ein ausführbares Programm (einen Vertex-Shader), das die Vertex-Shader-Stufe steuert.<br /> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Referenz](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

