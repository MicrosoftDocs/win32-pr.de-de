---
title: Compilerfunktionen (HLSL-Referenz)
description: Dieser Abschnitt enthält Informationen zu den folgenden Direct3D HLSL-Compilerfunktionen.
ms.assetid: aacc5207-3ec8-4031-b5c9-f7c0fb7b7095
keywords:
- functions, Compiler
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 43d9bf2feb572d7b410d702dbc456af7c18be0ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465807"
---
# <a name="compiler-functions-hlsl-reference"></a>Compilerfunktionen (HLSL-Referenz)

Dieser Abschnitt enthält Informationen zu den folgenden Direct3D HLSL-Compilerfunktionen:

## <a name="in-this-section"></a>In diesem Abschnitt




| Thema | BESCHREIBUNG | 
|-------|-------------|
| <a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a><br /> | Ruft einen Zeiger auf eine Reflektionsschnittstelle ab.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a><br /> | Kompilieren Sie HLSL-Code oder eine Effektdatei in Bytecode für ein bestimmtes Ziel.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a><br /> | Kompiliert HLSL-Code (High Level Shader Language) von Microsoft in Bytecode für ein bestimmtes Ziel.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a><br /> | <blockquote>[!Note]<br />Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können sie nicht in Apps verwenden, die Sie an die Windows Store. Weitere Informationen finden Sie im Abschnitt "Kompilieren von Shadern für UWP" in den Anmerkungen zu <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</blockquote><br /> Kompiliert HLSL-Code in Bytecode für ein bestimmtes Ziel.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a><br /> | <blockquote>[!Note]<br />Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können sie nicht in Apps verwenden, die Sie an die Windows Store.</blockquote><br /> Komprimiert eine Gruppe von Shadern in eine kompaktere Form. <br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a><br /> | Erstellt einen Puffer.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a><br /> | Erstellt eine Schnittstelle für Funktionsverknüpfungsdiagramme. <br /><blockquote>[!Note]<br />Diese Funktion ist Teil der HLSL-Shader-Verknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und zur Laufzeit in vollständige Shader zu verknüpfen.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a><br /> | Erstellt eine Linkerschnittstelle. <br /><blockquote>[!Note]<br />Diese Funktion ist Teil der HLSL-Shader-Verknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und zur Laufzeit in vollständige Shader zu verknüpfen.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a><br /> | <blockquote>[!Note]<br />Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können sie nicht in Apps verwenden, die Sie an die Windows Store.</blockquote><br /> Dekomprimiert einen oder mehrere Shader aus einem komprimierten Satz. <br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a><br /> | Disassembliert kompilierten HLSL-Code.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a><br /> | Disassembliert kompilierten HLSL-Code aus einem Direct3D10-Effekt.<br /> | 
| <a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a><br /> | Disassembliert einen Abschnitt des kompilierten HLSL-Codes, der durch Shader-Ablaufverfolgungsschritte angegeben wird.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a><br /> | Disassembliert einen bestimmten Bereich kompilierten HLSL-Codes.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a><br /> | Ruft einen bestimmten Teil aus einem Kompilierungsergebnis ab.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a><br /> | <blockquote>[!Note]<br />Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können sie nicht in Apps verwenden, die Sie an die Windows Store.</blockquote><br /> Ruft Shaderdebuginformationen ab.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a><br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> kann geändert werden oder ist für Releases nach der Windows 8.1. Verwenden Sie <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>stattdessen D3DGetBlobPart mit</strong></a> dem <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> Wert.</blockquote><br /> Ruft die Eingabe- und Ausgabesignaturen aus einem Kompilierungsergebnis ab.<br /> | 
| [<strong>D3DGetInputSignatureBlob</strong>](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)<br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> kann geändert werden oder ist für Releases nach der Windows 8.1. Verwenden Sie <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>stattdessen D3DGetBlobPart mit</strong></a> dem <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> Wert.</blockquote><br /> Ruft die Eingabesignatur aus einem Kompilierungsergebnis ab.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a><br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> kann geändert werden oder ist für Releases nach der Windows 8.1. Verwenden Sie <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>stattdessen D3DGetBlobPart mit</strong></a> <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>dem</strong></a> D3D_BLOB_OUTPUT_SIGNATURE_BLOB Wert.</blockquote><br /> Ruft die Ausgabesignatur aus einem Kompilierungsergebnis ab.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a><br /> | Ruft die Byteoffsets für Anweisungen innerhalb eines Abschnitts des Shadercodes ab.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a><br /> | Erstellt eine Shadermodulschnittstelle aus Quelldaten für das Shadermodul. <br /><blockquote>[!Note]<br />Diese Funktion ist Teil der HLSL-Shader-Verknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und zur Laufzeit in vollständige Shader zu verknüpfen.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a><br /> | Vorverarbeitet nicht kompilierten HLSL-Code.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a><br /> | <blockquote>[!Note]<br />Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können sie nicht in Apps verwenden, die Sie an die Windows Store.</blockquote><br /> Liest eine Datei, die sich auf dem Datenträger befindet, in den Arbeitsspeicher.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a><br /> | Ruft einen Zeiger auf eine Reflektionsschnittstelle ab.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a><br /> | Erstellt eine Bibliothekslektionsschnittstelle aus Quelldaten, die eine HLSL-Funktionsbibliothek enthält. <br /><blockquote>[!Note]<br />Diese Funktion ist Teil der HLSL-Shader-Verknüpfungstechnologie, die Sie auf allen Direct3D 11-Plattformen verwenden können, um vorkompilierte HLSL-Funktionen zu erstellen, in Bibliotheken zu packen und zur Laufzeit in vollständige Shader zu verknüpfen.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a><br /> | Legt Informationen in einem Kompilierungsergebnis fest.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a><br /> | Entfernt unerwünschte Blobs aus einem Kompilierungsergebnis.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a><br /> | <blockquote>[!Note]<br />Sie können diese API verwenden, um Ihre Windows Store-Apps zu entwickeln, aber Sie können sie nicht in Apps verwenden, die Sie an die Windows Store.</blockquote><br /> Schreibt ein Speicherblob in eine Datei auf dem Datenträger.<br /> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DCompiler-Referenz](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

