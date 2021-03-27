---
title: 'Shaderschnittstellen (Direct3D 11-Grafiken) '
description: Dieser Abschnitt enthält Informationen zu den Shader-Schnittstellen.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- Schnittstellen, Direct3D 11-Shader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d55e591d56442b641482a76a4ec93c0055029fc0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391407"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a>Shaderschnittstellen (Direct3D 11-Grafiken) 

Dieser Abschnitt enthält Informationen zu den Shader-Schnittstellen.

Jede dieser shaderschnittstellen verwaltet einen kompilierten Shader. Die-Schnittstelle wird erstellt, wenn ein Shader kompiliert wird, und wird dann an verschiedene APIs weitergegeben, die Zugriff auf einen kompilierten Shader benötigen. Dies ist beispielsweise der Fall, wenn ein Shader an eine Pipeline Phase gebunden oder eine shadersignatur erhalten wird.


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
<td>Eine COMPUTE-Shader-Schnittstelle verwaltet ein ausführbares Programm (ein Compute-Shader), das die Compute-Shader-Stufe steuert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a><br/></td>
<td>Eine Domänen-Shader-Schnittstelle verwaltet ein ausführbares Programm (einen Domänen-Shader), das die Domäne-Shader-Stufe steuert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a><br/></td>
<td>Eine Function-Linking-Graph-Schnittstelle wird zum Erstellen von Shadern verwendet, die aus einer Sequenz von vorkompilierten Funktionsaufrufen bestehen, von denen Werte an einander übergeben werden. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a><br/></td>
<td>Eine Funktions Reflektionsschnittstelle greift auf Funktions Informationen zu. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a><br/></td>
<td>Eine Funktionsparameter-Reflektionsschnittstelle greift auf Funktionsparameter Informationen zu. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a><br/></td>
<td>Eine Geometry-Shader-Schnittstelle verwaltet ein ausführbares Programm (ein Geometry-Shader), das die Geometrie-Shader-Stufe steuert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a><br/></td>
<td>Eine Hull-Shader-Schnittstelle verwaltet ein ausführbares Programm (ein Hull-Shader), das die Hülle-Shader-Stufe steuert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a><br/></td>
<td>Eine Bibliothek-reflektionseschnittstelle greift auf Bibliotheksinformationen zu. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a><br/></td>
<td>Eine Linker-Schnittstelle wird verwendet, um ein shadermodul zu verknüpfen. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a><br/></td>
<td>Eine Schnittstelle für den Verknüpfungs Knoten wird für Shader-Verknüpfungen verwendet. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a><br/></td>
<td>Eine Modulschnittstelle erstellt eine Instanz eines Moduls, das für die erneute Ressourcen Bindung verwendet wird. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a><br/></td>
<td>Eine modulinstanzschnittstelle wird für die erneute Ressourcen Bindung verwendet. <br/>
<blockquote>
[!Note]<br />
Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a><br/></td>
<td>Eine Pixel-Shader-Schnittstelle verwaltet ein ausführbares Programm (ein Pixelshader), das die Pixel-Shader-Stufe steuert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a><br/></td>
<td>Eine Shader-Reflection-Schnittstelle greift auf Shader-Informationen zu.<br/></td>
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
<td>Eine <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> -Schnittstelle implementiert Methoden zum Abrufen von Ablauf Verfolgungen von shaderausführungen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a><br/></td>
<td>Eine <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> -Schnittstelle implementiert eine Methode zum Erstellen von Shader-Ablauf Verfolgungs Informationsobjekten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a><br/></td>
<td>Eine Vertex-Shader-Schnittstelle verwaltet ein ausführbares Programm (ein Vertex-Shader), das die Vertex-Shader-Stufe steuert.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Referenz](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

