---
title: D3DX-Funktionen (Direct3D 11-Grafiken)
description: Dieser Abschnitt enthält Informationen zu den Funktionen von D3DX 11.
ms.assetid: 7548c02e-c8c2-4629-95ac-d21ca7a39f0a
keywords:
- Functions, DirectX 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b76c1764f464461b4800a9161ac37dcff8c539a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391350"
---
# <a name="d3dx-functions-direct3d-11-graphics"></a><span data-ttu-id="825be-104">D3DX-Funktionen (Direct3D 11-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="825be-104">D3DX Functions (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="825be-105">Dieser Abschnitt enthält Informationen zu den Funktionen von D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="825be-105">This section contains information about the D3DX 11 functions.</span></span>

> [!Note]  
> <span data-ttu-id="825be-106">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 


## <a name="in-this-section"></a><span data-ttu-id="825be-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="825be-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="825be-108">Thema</span><span class="sxs-lookup"><span data-stu-id="825be-108">Topic</span></span></th>
<th><span data-ttu-id="825be-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="825be-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="825be-110"><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-110"><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-111">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-111">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-112">Anstatt diese Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mithilfe des Befehlszeilen Compilers Fxc.exe oder eine der HLSL-Kompilierungs-APIs wie die <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> -API verwenden.</span><span class="sxs-lookup"><span data-stu-id="825be-112">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-113">Kompilieren Sie einen Shader oder einen Effekt aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="825be-113">Compile a shader or an effect from a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-114"><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-114"><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-115">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-115">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-116">Anstatt diese Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mithilfe des Befehlszeilen Compilers Fxc.exe oder eine der HLSL-Kompilierungs-APIs wie die <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> -API verwenden.</span><span class="sxs-lookup"><span data-stu-id="825be-116">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-117">Kompilieren Sie einen Shader oder einen Effekt, der in den Arbeitsspeicher geladen wird.</span><span class="sxs-lookup"><span data-stu-id="825be-117">Compile a shader or an effect that is loaded in memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-118"><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-118"><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-119">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-119">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-120">Anstatt diese Funktion zu verwenden, empfiehlt es sich, <a href="/windows/desktop/menurc/resources-functions">Ressourcen Funktionen</a>zu verwenden und dann mithilfe des Befehlszeilen Compilers von Fxc.exe offline zu kompilieren oder eine der HLSL-Kompilierungs-APIs wie die <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="825be-120">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-121">Kompilieren Sie einen Shader oder einen Effekt aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="825be-121">Compile a shader or an effect from a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-122"><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-122"><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-123">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-123">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-124">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek " <strong>computenormalmap</strong>" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="825be-124">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>ComputeNormalMap</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-125">Konvertiert eine Höhen Zuordnung in eine normale Karte.</span><span class="sxs-lookup"><span data-stu-id="825be-125">Converts a height map into a normal map.</span></span> <span data-ttu-id="825be-126">Die Komponenten (x, y, z) der einzelnen normalen werden den Kanälen (r, g, b) der Ausgabe Textur zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="825be-126">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-127"><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-127"><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-128">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-128">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="825be-129">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="825be-129">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-130">Erstellen eines asynchronen Daten Prozessors für einen Shader.</span><span class="sxs-lookup"><span data-stu-id="825be-130">Create an asynchronous-data processor for a shader.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-131"><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-131"><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-132">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-132">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="825be-133">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="825be-133">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-134">Erstellen Sie ein asynchrones Datei Lade Modul.</span><span class="sxs-lookup"><span data-stu-id="825be-134">Create an asynchronous-file loader.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-135"><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-135"><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-136">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-136">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="825be-137">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="825be-137">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-138">Erstellen Sie ein Lade Modul für asynchrone Speicher.</span><span class="sxs-lookup"><span data-stu-id="825be-138">Create an asynchronous-memory loader.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-139"><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-139"><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-140">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-140">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="825be-141">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="825be-141">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-142">Erstellen Sie ein asynchrones Ressourcen Lade Modul.</span><span class="sxs-lookup"><span data-stu-id="825be-142">Create an asynchronous-resource loader.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-143"><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-143"><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-144">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-144">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="825be-145">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="825be-145">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-146">Erstellen Sie einen Datenprozessor für einen Shader asynchron.</span><span class="sxs-lookup"><span data-stu-id="825be-146">Create a data processor for a shader asynchronously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-147"><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-147"><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-148">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-148">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="825be-149">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="825be-149">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-150">Erstellen Sie einen Datenprozessor, der mit einem <a href="id3dx11threadpump.md"><strong>threadpump</strong></a>verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="825be-150">Create a data processor to be used with a <a href="id3dx11threadpump.md"><strong>thread pump</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-151"><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-151"><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-152">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-152">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="825be-153">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="825be-153">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-154">Erstellen Sie einen Datenprozessor, der mit einem <a href="id3dx11threadpump.md"><strong>threadpump</strong></a>verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="825be-154">Create a data processor to be used with a <a href="id3dx11threadpump.md"><strong>thread pump</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-155"><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-155"><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-156">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-156">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="825be-157">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="825be-157">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-158">Erstellen Sie einen Datenprozessor, der eine Ressource lädt, und erstellen Sie dann eine Shader-Ressourcen Ansicht dafür.</span><span class="sxs-lookup"><span data-stu-id="825be-158">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="825be-159">Datenprozessoren sind eine Komponente der Funktion zum asynchronen Laden von Daten in Bibliothek d3dx11, die <a href="id3dx11threadpump.md"><strong>Thread-Pumpen</strong></a>verwendet.</span><span class="sxs-lookup"><span data-stu-id="825be-159">Data processors are a component of the asynchronous data loading feature in D3DX11 that uses <a href="id3dx11threadpump.md"><strong>thread pumps</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-160"><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-160"><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-161">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-161">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="825be-162">Anstatt diese Funktion zu verwenden, empfiehlt es sich, diese zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="825be-162">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="825be-163"><a href="https://github.com/Microsoft/DirectXTK">Directxtk</a> -Bibliothek (Laufzeit), " <strong>kreatexxxtexturefromfile</strong> " (wobei xxx DDS oder WIC ist)</span><span class="sxs-lookup"><span data-stu-id="825be-163"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromFile</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="825be-164"><a href="https://github.com/Microsoft/DirectXTex">Directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxfile</strong> (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " <strong>kreateshaderresourceview</strong> "</span><span class="sxs-lookup"><span data-stu-id="825be-164"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="825be-165">Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="825be-165">Create a shader-resource view from a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-166"><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-166"><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-167">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-167">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="825be-168">Anstatt diese Funktion zu verwenden, empfiehlt es sich, diese zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="825be-168">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="825be-169"><a href="https://github.com/Microsoft/DirectXTK">Directxtk</a> - <strong>Bibliothek (Runtime), "</strong> ", "", "", "", "", "", "".</span><span class="sxs-lookup"><span data-stu-id="825be-169"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="825be-170"><a href="https://github.com/Microsoft/DirectXTex">Directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxmemory</strong> (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " <strong>kreateshaderresourceview</strong> "</span><span class="sxs-lookup"><span data-stu-id="825be-170"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="825be-171">Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Datei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="825be-171">Create a shader-resource view from a file in memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-172"><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-172"><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-173">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-173">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="825be-174">Anstatt diese Funktion zu verwenden, empfiehlt es sich, <a href="/windows/desktop/menurc/resources-functions">Ressourcen Funktionen</a>zu verwenden, die dann folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="825be-174">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then these:</span></span></p>
<ul>
<li><span data-ttu-id="825be-175"><a href="https://github.com/Microsoft/DirectXTK">Directxtk</a> - <strong>Bibliothek (Runtime), "</strong> ", "", "", "", "", "", "".</span><span class="sxs-lookup"><span data-stu-id="825be-175"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="825be-176"><a href="https://github.com/Microsoft/DirectXTex">Directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxmemory</strong> (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " <strong>kreateshaderresourceview</strong> "</span><span class="sxs-lookup"><span data-stu-id="825be-176"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="825be-177">Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="825be-177">Create a shader-resource view from a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-178"><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-178"><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-179">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-179">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="825be-180">Anstatt diese Funktion zu verwenden, empfiehlt es sich, diese zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="825be-180">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="825be-181"><a href="https://github.com/Microsoft/DirectXTK">Directxtk</a> -Bibliothek (Laufzeit), " <strong>kreatexxxtexturefromfile</strong> " (wobei xxx DDS oder WIC ist)</span><span class="sxs-lookup"><span data-stu-id="825be-181"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromFile</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="825be-182"><a href="https://github.com/Microsoft/DirectXTex">Directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxfile</strong> (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " <strong>kreatetexture</strong> "</span><span class="sxs-lookup"><span data-stu-id="825be-182"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="825be-183">Erstellen Sie eine Textur Ressource aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="825be-183">Create a texture resource from a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-184"><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-184"><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-185">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-185">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="825be-186">Anstatt diese Funktion zu verwenden, empfiehlt es sich, diese zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="825be-186">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="825be-187"><a href="https://github.com/Microsoft/DirectXTK">Directxtk</a> - <strong>Bibliothek (Runtime), "</strong> ", "", "", "", "", "", "".</span><span class="sxs-lookup"><span data-stu-id="825be-187"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="825be-188"><a href="https://github.com/Microsoft/DirectXTex">Directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxmemory</strong> (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " <strong>kreatetexture</strong> "</span><span class="sxs-lookup"><span data-stu-id="825be-188"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="825be-189">Erstellen Sie eine Textur Ressource aus einer Datei, die sich im Systemspeicher befindet.</span><span class="sxs-lookup"><span data-stu-id="825be-189">Create a texture resource from a file residing in system memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-190"><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-190"><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-191">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-191">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="825be-192">Anstatt diese Funktion zu verwenden, empfiehlt es sich, <a href="/windows/desktop/menurc/resources-functions">Ressourcen Funktionen</a>zu verwenden, die dann folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="825be-192">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then these:</span></span></p>
<ul>
<li><span data-ttu-id="825be-193"><a href="https://github.com/Microsoft/DirectXTK">Directxtk</a> - <strong>Bibliothek (Runtime), "</strong> ", "", "", "", "", "", "".</span><span class="sxs-lookup"><span data-stu-id="825be-193"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="825be-194"><a href="https://github.com/Microsoft/DirectXTex">Directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxmemory</strong> (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " <strong>kreatetexture</strong> "</span><span class="sxs-lookup"><span data-stu-id="825be-194"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="825be-195">Erstellen Sie eine Textur aus einer anderen Ressource.</span><span class="sxs-lookup"><span data-stu-id="825be-195">Create a texture from another resource.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-196"><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-196"><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-197">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-197">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="825be-198">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="825be-198">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-199">Erstellen Sie ein Thread-Pump.</span><span class="sxs-lookup"><span data-stu-id="825be-199">Create a thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-200"><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-200"><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-201">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-201">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-202">Anstatt diese Funktion zu verwenden, wird empfohlen, dass Sie die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek, <strong>generatemipmaps</strong> und <strong>GenerateMipMaps3D</strong>verwenden.</span><span class="sxs-lookup"><span data-stu-id="825be-202">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GenerateMipMaps</strong> and <strong>GenerateMipMaps3D</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-203">Generiert eine MipMap-Kette mithilfe eines bestimmten Textur Filters.</span><span class="sxs-lookup"><span data-stu-id="825be-203">Generates mipmap chain using a particular texture filter.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-204"><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-204"><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-205">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-205">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-206">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek <strong>GetMetadataFromXXXFile</strong> (wobei xxx für WIC, DDS oder TGA verwendet wird) zu verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).</span><span class="sxs-lookup"><span data-stu-id="825be-206">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GetMetadataFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-207">Ruft Informationen zu einer angegebenen Bilddatei ab.</span><span class="sxs-lookup"><span data-stu-id="825be-207">Retrieves information about a given image file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-208"><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-208"><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-209">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-209">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-210">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek <strong>GetMetadataFromXXXMemory</strong> (wobei xxx für WIC, DDS oder TGA verwendet wird) zu verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).</span><span class="sxs-lookup"><span data-stu-id="825be-210">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GetMetadataFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-211">Sie erhalten Informationen zu einem bereits in den Arbeitsspeicher geladenen Image.</span><span class="sxs-lookup"><span data-stu-id="825be-211">Get information about an image already loaded into memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-212"><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-212"><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-213">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-213">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-214">Anstatt diese Funktion zu verwenden, empfiehlt es sich, <a href="/windows/desktop/menurc/resources-functions">Ressourcen Funktionen</a>zu verwenden und anschließend die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek (Tools), <strong>loadfromxxxmemory</strong> (wobei xxx für WIC, DDS oder TGA steht) zu verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).</span><span class="sxs-lookup"><span data-stu-id="825be-214">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then use <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-215">Ruft Informationen zu einem angegebenen Bild in einer Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="825be-215">Retrieves information about a given image in a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-216"><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-216"><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-217">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-217">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-218">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek zu verwenden, die <strong>Größe zu ändern</strong>, zu <strong>konvertieren</strong>, zu <strong>komprimieren</strong>, zu <strong>dekomprimieren</strong>und/oder <strong>copyrechteck</strong>.</span><span class="sxs-lookup"><span data-stu-id="825be-218">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>Resize</strong>, <strong>Convert</strong>, <strong>Compress</strong>, <strong>Decompress</strong>, and/or <strong>CopyRectangle</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-219">Lädt eine Textur aus einer Textur.</span><span class="sxs-lookup"><span data-stu-id="825be-219">Load a texture from a texture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-220"><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-220"><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-221">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-221">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-222">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="825be-222">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-223">Erstellen Sie einen Shader aus einer Datei, ohne ihn zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="825be-223">Create a shader from a file without compiling it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-224"><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-224"><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-225">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-225">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-226">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="825be-226">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-227">Erstellen Sie einen Shader aus dem Arbeitsspeicher, ohne ihn zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="825be-227">Create a shader from memory without compiling it.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-228"><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-228"><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-229">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-229">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-230">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="825be-230">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-231">Erstellen Sie einen Shader aus einer Ressource, ohne ihn zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="825be-231">Create a shader from a resource without compiling it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-232"><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-232"><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-233">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-233">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-234">Anstatt diese Funktion zu verwenden, empfiehlt es sich, dass Sie die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek <strong>capturetexture</strong> und <strong>savetoxxxfile</strong> verwenden (wobei xxx gleich WIC, DDS oder TGA ist). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).</span><span class="sxs-lookup"><span data-stu-id="825be-234">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>CaptureTexture</strong> then <strong>SaveToXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span> <span data-ttu-id="825be-235">Für das vereinfachte Szenario der Erstellung eines Screenshots aus einer renderzieltextur empfiehlt es sich, die <a href="https://github.com/Microsoft/DirectXTK">directxtk</a> -Bibliothek " <strong>saveddstexturedefile</strong> " oder " <strong>savewictexturedefile</strong>" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="825be-235">For the simplified scenario of creating a screen shot from a render target texture, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library, <strong>SaveDDSTextureToFile</strong> or <strong>SaveWICTextureToFile</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-236">Speichert eine Textur in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="825be-236">Save a texture to a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-237"><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-237"><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-238">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-238">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-239">Anstatt diese Funktion zu verwenden, empfiehlt es sich, dass Sie die <a href="https://github.com/Microsoft/DirectXTex">directxtex</a> -Bibliothek <strong>capturetexture</strong> , dann <strong>savetoxxxmemory</strong> (xxx ist WIC, DDS oder TGA) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).</span><span class="sxs-lookup"><span data-stu-id="825be-239">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>CaptureTexture</strong> then <strong>SaveToXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-240">Speichert eine Textur im Speicher.</span><span class="sxs-lookup"><span data-stu-id="825be-240">Save a texture to memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="825be-241"><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-241"><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-242">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-242">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-243">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die für die <strong>spprojectcubemap</strong>verwendete <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">sphärischen Harmonics</a> -Bibliothek zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="825be-243">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">Spherical Harmonics Math</a> library, <strong>SHProjectCubeMap</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-244">Projiziert eine in einer cubemap dargestellte Funktion in sphärischen Harmonics.</span><span class="sxs-lookup"><span data-stu-id="825be-244">Projects a function represented in a cube map into spherical harmonics.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="825be-245"><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a></span><span class="sxs-lookup"><span data-stu-id="825be-245"><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="825be-246">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="825be-246">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="825be-247">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>Verknüpfung id3d11devicecontext aus:: clearstate</strong></a> -Methode zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="825be-247">Instead of using this function, we recommend that you use the <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>ID3D11DeviceContext::ClearState</strong></a> method.</span></span>
</blockquote>
<br/> <span data-ttu-id="825be-248">Entfernt alle Ressourcen vom Gerät, indem die Zeiger auf <strong>null</strong>festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="825be-248">Removes all resources from the device by setting their pointers to <strong>NULL</strong>.</span></span> <span data-ttu-id="825be-249">Dies sollte beim Herunterfahren der Anwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="825be-249">This should be called during shutdown of your application.</span></span> <span data-ttu-id="825be-250">Dadurch wird sichergestellt, dass alle Ressourcen freigegeben werden, die nicht an das Gerät gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="825be-250">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="825be-251">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="825be-251">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="825be-252">Referenz zu D3DX 11</span><span class="sxs-lookup"><span data-stu-id="825be-252">D3DX 11 Reference</span></span>](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

