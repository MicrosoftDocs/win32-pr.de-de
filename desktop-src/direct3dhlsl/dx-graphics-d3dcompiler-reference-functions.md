---
title: Compilerfunktionen (HLSL-Referenz)
description: Dieser Abschnitt enthält Informationen zu den folgenden Direct3D HLSL-Compilerfunktionen.
ms.assetid: aacc5207-3ec8-4031-b5c9-f7c0fb7b7095
keywords:
- Funktionen, Compiler
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee63fa17cc9216fdb92f69fed4d77bc65bb49048
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "104982828"
---
# <a name="compiler-functions-hlsl-reference"></a><span data-ttu-id="5799a-104">Compilerfunktionen (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="5799a-104">Compiler functions (HLSL reference)</span></span>

<span data-ttu-id="5799a-105">Dieser Abschnitt enthält Informationen zu den folgenden Direct3D HLSL-Compilerfunktionen:</span><span class="sxs-lookup"><span data-stu-id="5799a-105">This section contains information about the following Direct3D HLSL compiler functions:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5799a-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5799a-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5799a-107">Thema</span><span class="sxs-lookup"><span data-stu-id="5799a-107">Topic</span></span></th>
<th><span data-ttu-id="5799a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5799a-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5799a-109"><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-109"><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-110">Ruft einen Zeiger auf eine reflektionseschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="5799a-110">Gets a pointer to a reflection interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5799a-111"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-111"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-112">Kompilieren Sie den HLSL-Code oder eine Effekt Datei in Bytecode für ein bestimmtes Ziel.</span><span class="sxs-lookup"><span data-stu-id="5799a-112">Compile HLSL code or an effect file into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5799a-113"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-113"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-114">Kompiliert den Microsoft High Level Shader Language (HLSL)-Code für ein bestimmtes Ziel in Bytecode.</span><span class="sxs-lookup"><span data-stu-id="5799a-114">Compiles Microsoft High Level Shader Language (HLSL) code into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5799a-115"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-115"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="5799a-116">Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können Sie nicht in Apps verwenden, die Sie an den Windows Store übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5799a-116">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span> <span data-ttu-id="5799a-117">Weitere Informationen finden Sie &quot; im Abschnitt Kompilieren von Shadern für UWP &quot; in den Hinweisen zu <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5799a-117">Refer to the section, &quot;Compiling shaders for UWP&quot;, in the remarks for <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="5799a-118">Kompiliert HLSL-Code für ein bestimmtes Ziel in Bytecode.</span><span class="sxs-lookup"><span data-stu-id="5799a-118">Compiles HLSL code into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5799a-119"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-119"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="5799a-120">Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können Sie nicht in Apps verwenden, die Sie an den Windows Store übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5799a-120">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="5799a-121">Komprimiert eine Reihe von Shadern in eine kompaktere Form.</span><span class="sxs-lookup"><span data-stu-id="5799a-121">Compresses a set of shaders into a more compact form.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5799a-122"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-122"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-123">Erstellt einen Puffer.</span><span class="sxs-lookup"><span data-stu-id="5799a-123">Creates a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5799a-124"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-124"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-125">Erstellt eine funktionsverknüpfungs-Graph-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5799a-125">Creates a function-linking-graph interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5799a-126">Diese Funktion ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken zu verpacken und Sie zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="5799a-126">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5799a-127"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-127"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-128">Erstellt eine Linker-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5799a-128">Creates a linker interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5799a-129">Diese Funktion ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken zu verpacken und Sie zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="5799a-129">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5799a-130"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-130"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="5799a-131">Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können Sie nicht in Apps verwenden, die Sie an den Windows Store übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5799a-131">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="5799a-132">Decomiert einen oder mehrere Shader aus einer komprimierten Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5799a-132">Decompresses one or more shaders from a compressed set.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5799a-133"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-133"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-134">Disassembliert kompilierten HLSL-Code.</span><span class="sxs-lookup"><span data-stu-id="5799a-134">Disassembles compiled HLSL code.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5799a-135"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-135"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-136">Disassembliert den kompilierten HLSL-Code aus einem Direct3D10-Effekt.</span><span class="sxs-lookup"><span data-stu-id="5799a-136">Disassembles compiled HLSL code from a Direct3D10 effect.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5799a-137"><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-137"><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-138">Disassembliert einen Abschnitt des kompilierten HLSL-Codes, der durch Shader-Ablauf Verfolgungs Schritte angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5799a-138">Disassembles a section of compiled HLSL code that is specified by shader trace steps.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5799a-139"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-139"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-140">Disassembliert einen bestimmten Bereich von kompiliertem HLSL-Code.</span><span class="sxs-lookup"><span data-stu-id="5799a-140">Disassembles a specific region of compiled HLSL code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5799a-141"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-141"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-142">Ruft einen bestimmten Teil aus einem Kompilierungs Ergebnis ab.</span><span class="sxs-lookup"><span data-stu-id="5799a-142">Retrieves a specific part from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5799a-143"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-143"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="5799a-144">Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können Sie nicht in Apps verwenden, die Sie an den Windows Store übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5799a-144">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="5799a-145">Ruft Shader-Debuginformationen ab.</span><span class="sxs-lookup"><span data-stu-id="5799a-145">Gets shader debug information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5799a-146"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-146"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="5799a-147">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> kann nach Windows 8.1 geändert werden oder für Releases nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="5799a-147">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="5799a-148">Verwenden Sie stattdessen <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> mit dem <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> Wert.</span><span class="sxs-lookup"><span data-stu-id="5799a-148">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="5799a-149">Ruft die Eingabe-und Ausgabe Signaturen aus einem Kompilierungs Ergebnis ab.</span><span class="sxs-lookup"><span data-stu-id="5799a-149">Gets the input and output signatures from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5799a-150">[<strong>D3DGetInputSignatureBlob</strong>] (/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)</span><span class="sxs-lookup"><span data-stu-id="5799a-150">[<strong>D3DGetInputSignatureBlob</strong>](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)</span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="5799a-151">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> kann nach Windows 8.1 geändert werden oder für Releases nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="5799a-151">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="5799a-152">Verwenden Sie stattdessen <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> mit dem <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> Wert.</span><span class="sxs-lookup"><span data-stu-id="5799a-152">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="5799a-153">Ruft die Eingabe Signatur aus einem Kompilierungs Ergebnis ab.</span><span class="sxs-lookup"><span data-stu-id="5799a-153">Gets the input signature from a compilation result.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5799a-154"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-154"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="5799a-155">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> kann nach Windows 8.1 geändert werden oder für Releases nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="5799a-155">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="5799a-156">Verwenden Sie stattdessen <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> mit dem <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> Wert.</span><span class="sxs-lookup"><span data-stu-id="5799a-156">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="5799a-157">Ruft die Ausgabe Signatur aus einem Kompilierungs Ergebnis ab.</span><span class="sxs-lookup"><span data-stu-id="5799a-157">Gets the output signature from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5799a-158"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-158"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-159">Ruft die Byte Offsets für Anweisungen in einem Abschnitt des Shader-Codes ab.</span><span class="sxs-lookup"><span data-stu-id="5799a-159">Retrieves the byte offsets for instructions within a section of shader code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5799a-160"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-160"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-161">Erstellt eine Shader-Modulschnittstelle aus den Quelldaten für das Shader-Modul.</span><span class="sxs-lookup"><span data-stu-id="5799a-161">Creates a shader module interface from source data for the shader module.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5799a-162">Diese Funktion ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken zu verpacken und Sie zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="5799a-162">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5799a-163"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-163"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-164">Vorverarbeitet nicht kompilierten HLSL-Code.</span><span class="sxs-lookup"><span data-stu-id="5799a-164">Preprocesses uncompiled HLSL code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5799a-165"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-165"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="5799a-166">Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können Sie nicht in Apps verwenden, die Sie an den Windows Store übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5799a-166">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="5799a-167">Liest eine Datei auf dem Datenträger in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5799a-167">Reads a file that is on disk into memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5799a-168"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-168"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-169">Ruft einen Zeiger auf eine reflektionseschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="5799a-169">Gets a pointer to a reflection interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5799a-170"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-170"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-171">Erstellt eine Bibliothek Reflektionsschnittstelle aus Quelldaten, die eine HLSL-Bibliotheks Bibliothek enthält.</span><span class="sxs-lookup"><span data-stu-id="5799a-171">Creates a library-reflection interface from source data that contains an HLSL library of functions.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5799a-172">Diese Funktion ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken zu verpacken und Sie zur Laufzeit in vollständige Shader zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="5799a-172">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5799a-173"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-173"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-174">Legt Informationen in einem Kompilierungs Ergebnis fest.</span><span class="sxs-lookup"><span data-stu-id="5799a-174">Sets information in a compilation result.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5799a-175"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-175"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="5799a-176">Entfernt unerwünschte blobergebnisse aus einem Kompilierungs Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="5799a-176">Removes unwanted blobs from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5799a-177"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="5799a-177"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="5799a-178">Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können Sie nicht in Apps verwenden, die Sie an den Windows Store übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5799a-178">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="5799a-179">Schreibt ein speicherblob in eine Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="5799a-179">Writes a memory blob to a file on disk.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="5799a-180">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5799a-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5799a-181">D3DCompiler-Referenz</span><span class="sxs-lookup"><span data-stu-id="5799a-181">D3DCompiler Reference</span></span>](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

