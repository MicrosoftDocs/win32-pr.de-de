---
title: 'Shaderschnittstellen (Direct3D 11-Grafiken) '
description: Dieser Abschnitt enthält Informationen zu den Shaderschnittstellen.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- Schnittstellen, Direct3D 11 Shader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6c3d628f83747831dae0e98bd604f88f9ee0946aeb56a38c9734df30ba0d67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988480"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a>Shaderschnittstellen (Direct3D 11-Grafiken) 

Dieser Abschnitt enthält Informationen zu den Shaderschnittstellen.

Jede dieser Shaderschnittstellen verwaltet einen kompilierten Shader. Die Schnittstelle wird erstellt, wenn ein Shader kompiliert wird, und wird dann an verschiedene APIs übergeben, die Zugriff auf einen kompilierten Shader benötigen. z. B. beim Binden eines Shaders an eine Pipelinephase oder beim Abrufen einer Shadersignatur.


## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a><br/></td>
<td>Diese Schnittstelle kapselt eine HLSL-Klasse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a><br/></td>
<td>Diese Schnittstelle kapselt eine dynamische HLSL-Verknüpfung.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a><br/></td>
<td>Eine Compute-Shader-Schnittstelle verwaltet ein ausführbares Programm (einen Compute-Shader), das die Compute-Shader-Stufe steuert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a><br/></td>
<td>Eine Domänen-Shader-Schnittstelle verwaltet ein ausführbares Programm (einen Domänen-Shader), das die Domänen-Shader-Stufe steuert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a><br/></td>
<td>Eine Funktionsverknüpfungs-Graph-Schnittstelle wird zum Erstellen von Shadern verwendet, die aus einer Sequenz von vorkompilierten Funktionsaufrufen bestehen, die Werte aneinander übergeben. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shaderverknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und sie zur Laufzeit mit vollständigen Shadern zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a><br/></td>
<td>Eine Funktionsreflektionsschnittstelle greift auf Funktionsinformationen zu. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shaderverknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und sie zur Laufzeit mit vollständigen Shadern zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a><br/></td>
<td>Eine Funktionsparameter-Reflektionsschnittstelle greift auf Funktionsparameterinformationen zu. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shaderverknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und sie zur Laufzeit mit vollständigen Shadern zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a><br/></td>
<td>Eine geometry-shader-Schnittstelle verwaltet ein ausführbares Programm (einen Geometrie-Shader), das die Geometry-Shader-Stufe steuert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a><br/></td>
<td>Eine Hüllen-Shader-Schnittstelle verwaltet ein ausführbares Programm (einen Hüllen-Shader), das die Hüllen-Shader-Stufe steuert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a><br/></td>
<td>Eine Bibliothek-Reflektionsschnittstelle greift auf Bibliotheksinformationen zu. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shaderverknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und sie zur Laufzeit mit vollständigen Shadern zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a><br/></td>
<td>Eine Linkerschnittstelle wird verwendet, um ein Shadermodul zu verknüpfen. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shaderverknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und sie zur Laufzeit mit vollständigen Shadern zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a><br/></td>
<td>Eine Verknüpfungsknotenschnittstelle wird für die Shaderverknüpfung verwendet. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shaderverknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und sie zur Laufzeit mit vollständigen Shadern zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a><br/></td>
<td>Eine Modulschnittstelle erstellt eine Instanz eines Moduls, das für die erneute Bindung von Ressourcen verwendet wird. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shaderverknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und sie zur Laufzeit mit vollständigen Shadern zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a><br/></td>
<td>Für die erneute Bindung von Ressourcen wird eine Modulinstanzschnittstelle verwendet. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shaderverknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und sie zur Laufzeit mit vollständigen Shadern zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a><br/></td>
<td>Eine Pixel-Shader-Schnittstelle verwaltet ein ausführbares Programm (einen Pixel-Shader), das die Pixel-Shader-Stufe steuert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a><br/></td>
<td>Eine Shader-Reflektionsschnittstelle greift auf Shaderinformationen zu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a><br/></td>
<td>Diese Shader-Reflektionsschnittstelle ermöglicht den Zugriff auf einen konstanten Puffer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a><br/></td>
<td>Diese Shader-Reflektionsschnittstelle ermöglicht den Zugriff auf den Variablentyp.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a><br/></td>
<td>Diese Shader-Reflektionsschnittstelle ermöglicht den Zugriff auf eine Variable.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a><br/></td>
<td>Eine <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace-Schnittstelle</strong></a> implementiert Methoden zum Abrufen von Ablaufverfolgungen von Shaderausführungen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a><br/></td>
<td>Eine <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory-Schnittstelle</strong></a> implementiert eine Methode zum Generieren von Shader-Ablaufverfolgungsinformationsobjekten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a><br/></td>
<td>Eine Vertex-Shader-Schnittstelle verwaltet ein ausführbares Programm (einen Vertex-Shader), das die Vertex-Shader-Stufe steuert.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Referenz](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

