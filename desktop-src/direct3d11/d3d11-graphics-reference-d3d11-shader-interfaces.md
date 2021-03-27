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
# <a name="shader-interfaces-direct3d-11-graphics"></a><span data-ttu-id="cc1fe-104">Shaderschnittstellen (Direct3D 11-Grafiken) </span><span class="sxs-lookup"><span data-stu-id="cc1fe-104">Shader Interfaces (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="cc1fe-105">Dieser Abschnitt enthält Informationen zu den Shader-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-105">This section contains information about the shader interfaces.</span></span>

<span data-ttu-id="cc1fe-106">Jede dieser shaderschnittstellen verwaltet einen kompilierten Shader.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-106">Each of these shader interfaces manages a compiled shader.</span></span> <span data-ttu-id="cc1fe-107">Die-Schnittstelle wird erstellt, wenn ein Shader kompiliert wird, und wird dann an verschiedene APIs weitergegeben, die Zugriff auf einen kompilierten Shader benötigen. Dies ist beispielsweise der Fall, wenn ein Shader an eine Pipeline Phase gebunden oder eine shadersignatur erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-107">The interface is created when a shader is compiled, and is then passed to various APIs that need access to a compiled shader; such as when binding a shader to a pipeline stage or getting a shader signature.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="cc1fe-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cc1fe-108">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cc1fe-109">Thema</span><span class="sxs-lookup"><span data-stu-id="cc1fe-109">Topic</span></span></th>
<th><span data-ttu-id="cc1fe-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc1fe-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc1fe-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-112">Diese Schnittstelle kapselt eine HLSL-Klasse.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-112">This interface encapsulates an HLSL class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc1fe-113"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-113"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-114">Diese Schnittstelle kapselt eine dynamische HLSL-Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-114">This interface encapsulates an HLSL dynamic linkage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc1fe-115"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-115"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-116">Eine COMPUTE-Shader-Schnittstelle verwaltet ein ausführbares Programm (ein Compute-Shader), das die Compute-Shader-Stufe steuert.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-116">A compute-shader interface manages an executable program (a compute shader) that controls the compute-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc1fe-117"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-117"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-118">Eine Domänen-Shader-Schnittstelle verwaltet ein ausführbares Programm (einen Domänen-Shader), das die Domäne-Shader-Stufe steuert.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-118">A domain-shader interface manages an executable program (a domain shader) that controls the domain-shader stage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc1fe-119"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-119"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-120">Eine Function-Linking-Graph-Schnittstelle wird zum Erstellen von Shadern verwendet, die aus einer Sequenz von vorkompilierten Funktionsaufrufen bestehen, von denen Werte an einander übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-120">A function-linking-graph interface is used for constructing shaders that consist of a sequence of precompiled function calls that pass values to each other.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc1fe-121">Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-121">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc1fe-122"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-122"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-123">Eine Funktions Reflektionsschnittstelle greift auf Funktions Informationen zu.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-123">A function-reflection interface accesses function info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc1fe-124">Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-124">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc1fe-125"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-125"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-126">Eine Funktionsparameter-Reflektionsschnittstelle greift auf Funktionsparameter Informationen zu.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-126">A function-parameter-reflection interface accesses function-parameter info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc1fe-127">Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-127">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc1fe-128"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-128"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-129">Eine Geometry-Shader-Schnittstelle verwaltet ein ausführbares Programm (ein Geometry-Shader), das die Geometrie-Shader-Stufe steuert.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-129">A geometry-shader interface manages an executable program (a geometry shader) that controls the geometry-shader stage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc1fe-130"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-130"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-131">Eine Hull-Shader-Schnittstelle verwaltet ein ausführbares Programm (ein Hull-Shader), das die Hülle-Shader-Stufe steuert.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-131">A hull-shader interface manages an executable program (a hull shader) that controls the hull-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc1fe-132"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-132"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-133">Eine Bibliothek-reflektionseschnittstelle greift auf Bibliotheksinformationen zu.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-133">A library-reflection interface accesses library info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc1fe-134">Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-134">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc1fe-135"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-135"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-136">Eine Linker-Schnittstelle wird verwendet, um ein shadermodul zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-136">A linker interface is used to link a shader module.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc1fe-137">Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-137">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc1fe-138"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-138"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-139">Eine Schnittstelle für den Verknüpfungs Knoten wird für Shader-Verknüpfungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-139">A linking-node interface is used for shader linking.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc1fe-140">Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-140">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc1fe-141"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-141"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-142">Eine Modulschnittstelle erstellt eine Instanz eines Moduls, das für die erneute Ressourcen Bindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-142">A module interface creates an instance of a module that is used for resource rebinding.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc1fe-143">Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-143">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc1fe-144"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-144"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-145">Eine modulinstanzschnittstelle wird für die erneute Ressourcen Bindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-145">A module-instance interface is used for resource rebinding.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc1fe-146">Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-146">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc1fe-147"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-147"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-148">Eine Pixel-Shader-Schnittstelle verwaltet ein ausführbares Programm (ein Pixelshader), das die Pixel-Shader-Stufe steuert.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-148">A pixel-shader interface manages an executable program (a pixel shader) that controls the pixel-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc1fe-149"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-149"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-150">Eine Shader-Reflection-Schnittstelle greift auf Shader-Informationen zu.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-150">A shader-reflection interface accesses shader information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc1fe-151"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-151"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-152">Diese Shader-Reflektionsschnittstelle ermöglicht den Zugriff auf einen konstanten Puffer.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-152">This shader-reflection interface provides access to a constant buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc1fe-153"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-153"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-154">Diese Shader-Reflektionsschnittstelle ermöglicht den Zugriff auf den Variablentyp.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-154">This shader-reflection interface provides access to variable type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc1fe-155"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-155"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-156">Diese Shader-Reflektionsschnittstelle ermöglicht den Zugriff auf eine Variable.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-156">This shader-reflection interface provides access to a variable.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc1fe-157"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-157"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-158">Eine <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> -Schnittstelle implementiert Methoden zum Abrufen von Ablauf Verfolgungen von shaderausführungen.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-158">An <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> interface implements methods for obtaining traces of shader executions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc1fe-159"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-159"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-160">Eine <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> -Schnittstelle implementiert eine Methode zum Erstellen von Shader-Ablauf Verfolgungs Informationsobjekten.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-160">An <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> interface implements a method for generating shader trace information objects.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc1fe-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc1fe-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="cc1fe-162">Eine Vertex-Shader-Schnittstelle verwaltet ein ausführbares Programm (ein Vertex-Shader), das die Vertex-Shader-Stufe steuert.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-162">A vertex-shader interface manages an executable program (a vertex shader) that controls the vertex-shader stage.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="cc1fe-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc1fe-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc1fe-164">Shader-Referenz</span><span class="sxs-lookup"><span data-stu-id="cc1fe-164">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

