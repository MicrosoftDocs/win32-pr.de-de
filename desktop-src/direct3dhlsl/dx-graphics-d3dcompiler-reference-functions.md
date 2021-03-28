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
# <a name="compiler-functions-hlsl-reference"></a>Compilerfunktionen (HLSL-Referenz)

Dieser Abschnitt enthält Informationen zu den folgenden Direct3D HLSL-Compilerfunktionen:

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
<td><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a><br/></td>
<td>Ruft einen Zeiger auf eine reflektionseschnittstelle ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a><br/></td>
<td>Kompilieren Sie den HLSL-Code oder eine Effekt Datei in Bytecode für ein bestimmtes Ziel.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a><br/></td>
<td>Kompiliert den Microsoft High Level Shader Language (HLSL)-Code für ein bestimmtes Ziel in Bytecode.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können Sie nicht in Apps verwenden, die Sie an den Windows Store übermitteln. Weitere Informationen finden Sie &quot; im Abschnitt Kompilieren von Shadern für UWP &quot; in den Hinweisen zu <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.
</blockquote>
<br/> Kompiliert HLSL-Code für ein bestimmtes Ziel in Bytecode.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können Sie nicht in Apps verwenden, die Sie an den Windows Store übermitteln.
</blockquote>
<br/> Komprimiert eine Reihe von Shadern in eine kompaktere Form. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a><br/></td>
<td>Erstellt einen Puffer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a><br/></td>
<td>Erstellt eine funktionsverknüpfungs-Graph-Schnittstelle. <br/>
<blockquote>
[!Note]<br />
Diese Funktion ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken zu verpacken und Sie zur Laufzeit in vollständige Shader zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a><br/></td>
<td>Erstellt eine Linker-Schnittstelle. <br/>
<blockquote>
[!Note]<br />
Diese Funktion ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken zu verpacken und Sie zur Laufzeit in vollständige Shader zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können Sie nicht in Apps verwenden, die Sie an den Windows Store übermitteln.
</blockquote>
<br/> Decomiert einen oder mehrere Shader aus einer komprimierten Gruppe. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a><br/></td>
<td>Disassembliert kompilierten HLSL-Code.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a><br/></td>
<td>Disassembliert den kompilierten HLSL-Code aus einem Direct3D10-Effekt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a><br/></td>
<td>Disassembliert einen Abschnitt des kompilierten HLSL-Codes, der durch Shader-Ablauf Verfolgungs Schritte angegeben wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a><br/></td>
<td>Disassembliert einen bestimmten Bereich von kompiliertem HLSL-Code.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a><br/></td>
<td>Ruft einen bestimmten Teil aus einem Kompilierungs Ergebnis ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können Sie nicht in Apps verwenden, die Sie an den Windows Store übermitteln.
</blockquote>
<br/> Ruft Shader-Debuginformationen ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> kann nach Windows 8.1 geändert werden oder für Releases nicht verfügbar sein. Verwenden Sie stattdessen <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> mit dem <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> Wert.
</blockquote>
<br/> Ruft die Eingabe-und Ausgabe Signaturen aus einem Kompilierungs Ergebnis ab.<br/></td>
</tr>
<tr class="odd">
<td>[<strong>D3DGetInputSignatureBlob</strong>] (/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)<br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> kann nach Windows 8.1 geändert werden oder für Releases nicht verfügbar sein. Verwenden Sie stattdessen <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> mit dem <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> Wert.
</blockquote>
<br/> Ruft die Eingabe Signatur aus einem Kompilierungs Ergebnis ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> kann nach Windows 8.1 geändert werden oder für Releases nicht verfügbar sein. Verwenden Sie stattdessen <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> mit dem <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> Wert.
</blockquote>
<br/> Ruft die Ausgabe Signatur aus einem Kompilierungs Ergebnis ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a><br/></td>
<td>Ruft die Byte Offsets für Anweisungen in einem Abschnitt des Shader-Codes ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a><br/></td>
<td>Erstellt eine Shader-Modulschnittstelle aus den Quelldaten für das Shader-Modul. <br/>
<blockquote>
[!Note]<br />
Diese Funktion ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken zu verpacken und Sie zur Laufzeit in vollständige Shader zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a><br/></td>
<td>Vorverarbeitet nicht kompilierten HLSL-Code.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können Sie nicht in Apps verwenden, die Sie an den Windows Store übermitteln.
</blockquote>
<br/> Liest eine Datei auf dem Datenträger in den Arbeitsspeicher.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a><br/></td>
<td>Ruft einen Zeiger auf eine reflektionseschnittstelle ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a><br/></td>
<td>Erstellt eine Bibliothek Reflektionsschnittstelle aus Quelldaten, die eine HLSL-Bibliotheks Bibliothek enthält. <br/>
<blockquote>
[!Note]<br />
Diese Funktion ist Teil der HLSL-Shader-Verknüpfungs Technologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, Sie in Bibliotheken zu verpacken und Sie zur Laufzeit in vollständige Shader zu verknüpfen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a><br/></td>
<td>Legt Informationen in einem Kompilierungs Ergebnis fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a><br/></td>
<td>Entfernt unerwünschte blobergebnisse aus einem Kompilierungs Ergebnis.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können Sie nicht in Apps verwenden, die Sie an den Windows Store übermitteln.
</blockquote>
<br/> Schreibt ein speicherblob in eine Datei auf dem Datenträger.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DCompiler-Referenz](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

