---
title: Shader-Schnittstellen (Direct3D 12-Grafiken)
description: D3d12shader. h deklariert die folgenden Schnittstellen.
ms.assetid: 791d2c91-3791-47fe-b887-8117ecc798ba
keywords:
- Schnittstellen, Direct3D 12-Shader
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f111572aacca36f12600b0cf334895684064e5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340960"
---
# <a name="shader-interfaces-direct3d-12-graphics"></a><span data-ttu-id="4e8d3-104">Shader-Schnittstellen (Direct3D 12-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="4e8d3-104">Shader Interfaces (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="4e8d3-105">d3d12shader. h deklariert die folgenden Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4e8d3-105">d3d12shader.h declares the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4e8d3-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4e8d3-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e8d3-107">Thema</span><span class="sxs-lookup"><span data-stu-id="4e8d3-107">Topic</span></span></th>
<th><span data-ttu-id="4e8d3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e8d3-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4e8d3-109"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e8d3-109"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="4e8d3-110">Eine Funktionsparameter-Reflektionsschnittstelle greift auf Funktionsparameter Informationen zu.</span><span class="sxs-lookup"><span data-stu-id="4e8d3-110">A function-parameter-reflection interface accesses function-parameter info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4e8d3-111">Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 12-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="4e8d3-111">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e8d3-112"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e8d3-112"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="4e8d3-113">Eine Funktions Reflektionsschnittstelle greift auf Funktions Informationen zu.</span><span class="sxs-lookup"><span data-stu-id="4e8d3-113">A function-reflection interface accesses function info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4e8d3-114">Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 12-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="4e8d3-114">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e8d3-115"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e8d3-115"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="4e8d3-116">Eine Bibliothek-reflektionseschnittstelle greift auf Bibliotheksinformationen zu.</span><span class="sxs-lookup"><span data-stu-id="4e8d3-116">A library-reflection interface accesses library info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4e8d3-117">Diese Schnittstelle ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 12-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken Verpacken und diese zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="4e8d3-117">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e8d3-118"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e8d3-118"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="4e8d3-119">Eine Shader-Reflection-Schnittstelle greift auf Shader-Informationen zu.</span><span class="sxs-lookup"><span data-stu-id="4e8d3-119">A shader-reflection interface accesses shader information.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e8d3-120"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e8d3-120"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a></span></span><br/></td>
<td><span data-ttu-id="4e8d3-121">Diese Shader-Reflektionsschnittstelle ermöglicht den Zugriff auf einen konstanten Puffer.</span><span class="sxs-lookup"><span data-stu-id="4e8d3-121">This shader-reflection interface provides access to a constant buffer.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e8d3-122"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e8d3-122"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a></span></span><br/></td>
<td><span data-ttu-id="4e8d3-123">Diese Shader-Reflektionsschnittstelle ermöglicht den Zugriff auf den Variablentyp.</span><span class="sxs-lookup"><span data-stu-id="4e8d3-123">This shader-reflection interface provides access to variable type.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e8d3-124"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a></span><span class="sxs-lookup"><span data-stu-id="4e8d3-124"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a></span></span><br/></td>
<td><span data-ttu-id="4e8d3-125">Diese Shader-Reflektionsschnittstelle ermöglicht den Zugriff auf eine Variable.</span><span class="sxs-lookup"><span data-stu-id="4e8d3-125">This shader-reflection interface provides access to a variable.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4e8d3-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e8d3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e8d3-127">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="4e8d3-127">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="4e8d3-128">Shader-Referenz</span><span class="sxs-lookup"><span data-stu-id="4e8d3-128">Shader Reference</span></span>](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





