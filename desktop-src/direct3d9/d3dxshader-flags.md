---
description: Die D3DXSHADER-Flags werden zum Auswerten, kompilieren oder Assemblieren von Shadern verwendet.
ms.assetid: 8558d0e9-d09f-4c62-bc89-6080f4e44ff8
title: D3DXSHADER-Flags (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_PACKMATRIX_COLUMNMAJOR
- D3DXSHADER_PACKMATRIX_ROWMAJOR
- D3DXSHADER_AVOID_FLOW_CONTROL
- D3DXSHADER_DEBUG
- D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_IEEE_STRICTNESS
- D3DXSHADER_NO_PRESHADER
- D3DXSHADER_OPTIMIZATION_LEVEL0
- D3DXSHADER_OPTIMIZATION_LEVEL1
- D3DXSHADER_OPTIMIZATION_LEVEL2
- D3DXSHADER_OPTIMIZATION_LEVEL3
- D3DXSHADER_PARTIALPRECISION
- D3DXSHADER_PREFER_FLOW_CONTROL
- D3DXSHADER_SKIPOPTIMIZATION
- D3DXSHADER_SKIPVALIDATION
- D3DXSHADER_USE_LEGACY_D3DX9_31_DLL
- D3DXSHADER_DEBUG
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_SKIPVALIDATION
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 6f5d35f8c3bdf556e188c2cab8ff2684449b226f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366633"
---
# <a name="d3dxshader-flags"></a>D3DXSHADER-Flags

Die **D3DXSHADER** -Flags werden zum Auswerten, kompilieren oder Assemblieren von Shadern verwendet.

**Parserflags**

Analysezeit-Flags werden nur vom Effektsystem (vor der Auswirkung der Kompilierung) verwendet, wenn Sie einen Effekt Compiler erstellen. Sie können z. b. ein Compilerobjekt mit **D3DXSHADER \_ packmatrix \_ ColumnMajor** erstellen und dieses Compilerobjekt wiederholt mit unterschiedlichen Compilerflags verwenden, um spezialisierten Code zu generieren.



| Konstante                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_PACKMATRIX_COLUMNMAJOR"></span><span id="d3dxshader_packmatrix_columnmajor"></span><dl> <dt>**D3DXSHADER \_ packmatrix- \_ ColumnMajor**</dt> </dl> | Wenn die Matrizen nicht explizit angegeben werden, werden Sie in der Spalte-Haupt Reihenfolge verpackt (jeder Vektor wird in einer einzelnen Spalte angezeigt), wenn Sie an den Shader und an den Shader geleitet werden Dies ist im Allgemeinen effizienter, da es die Verwendung von Vektor Matrix mit einer Reihe von Punkt Produkten ermöglicht.<br/> |
| <span id="D3DXSHADER_PACKMATRIX_ROWMAJOR"></span><span id="d3dxshader_packmatrix_rowmajor"></span><dl> <dt>**D3DXSHADER \_ packmatrix- \_ rowmajor**</dt> </dl>          | Wenn die Matrizen nicht explizit angegeben werden, werden Sie in der Reihenfolge der Zeilen (jeder Vektor wird in einer einzelnen Zeile angezeigt) verpackt, wenn Sie an oder aus dem Shader übermittelt werden.<br/>                                                                                                                                        |



**Compilerflags**

Der DirectX 10 HLSL-Compiler ist jetzt der Standard Compiler. Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .

In der folgenden Tabelle werden die in Direct3D 9 und Direct3D 10 verfügbaren Flags ausführlich erläutert. Der Wert für das-Flag ist die entsprechende FXC-Option.



| Konstante/Wert                                                                                                                                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_AVOID_FLOW_CONTROL"></span><span id="d3dxshader_avoid_flow_control"></span><dl> <dt>**D3DXSHADER \_ Vermeiden der \_ Fluss \_ Steuerung**</dt> <dt>/GFA</dt> </dl>                                     | Dies ist ein Hinweis für den Compiler, um die Verwendung von Anweisungen zur Fluss Steuerung zu vermeiden.<br/> Direct3D 9-Ja<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ /Zi Debuggen**</dt> <dt></dt> </dl>                                                                               | Fügen Sie während der shaderkompilierung debugdateiname, Zeilennummern und Typ-und Symbol Informationen ein.<br/> Direct3D 9-Ja<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dxshader_enable_backwards_compatibility"></span><dl> <dt>**D3DXSHADER \_ Abwärts \_ \_ Kompatibilität aktivieren**</dt> <dt>/GEC</dt> </dl> | Kompilieren von PS \_ 1 \_ x-Shadern als PS \_ 2 \_ 0. Effekte, die PS \_ 1 \_ x-Ziele angeben, werden stattdessen zu PS \_ 2 0-Zielen kompiliert, \_ da dies die minimale shaderversion ist, die von der Version des Shader-Compilers unterstützt wird, der mit DirectX 10 ausgeliefert wird Dieses Flag hat keine Auswirkung, wenn es Kompilierungs Ziele auf höherer Ebene verwendet.<br/> Direct3D 9-Nein<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ Erzwingen von \_ PS- \_ Software \_ noopt**</dt> <dt>N/v</dt> </dl>                      | Erzwingen Sie, dass der Compiler mit dem nächsthöchsten verfügbaren Software Ziel für Pixel-Shader kompiliert wird. Dieses Flag deaktiviert auch Optimierungen und Debuggen.<br/> Direct3D 9-Ja<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ Erzwingen von \_ vs- \_ Software \_ noopt**</dt> <dt>N/v</dt> </dl>                      | Erzwingen Sie, dass der Compiler mit dem nächsthöchsten verfügbaren Software Ziel für Vertexshader kompiliert wird. Dieses Flag deaktiviert auch Optimierungen und Debuggen.<br/> Direct3D 9-Ja<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_IEEE_STRICTNESS"></span><span id="d3dxshader_ieee_strictness"></span><dl> <dt>**D3DXSHADER \_ IEEE \_ strictness**</dt> <dt>/GIS</dt> </dl>                                               | Deaktivieren von Optimierungen, die dazu führen können, dass sich die Ausgabe eines kompilierten shaderprogramms von der Ausgabe eines mit dem DirectX 9-Shader-Compiler kompilierten Programms aufgrund kleiner Genauigkeits-Fehlern in der Gleit Komma Mathematik unterscheidet.<br/> Direct3D 9-Nein<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="D3DXSHADER_NO_PRESHADER"></span><span id="d3dxshader_no_preshader"></span><dl> <dt>**D3DXSHADER \_ Kein \_ preshader**</dt> <dt>/op</dt> </dl>                                                         | Deaktiviert preshaders. Der Compiler führt keine statischen Ausdrücke zur Auswertung auf der Host-CPU aus. Darüber hinaus werden beim Kompilieren von eigenständigen Funktionen vom Compiler keine-Ausdrücke durch ein-/aus-.<br/> Direct3D 9-Ja<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL0"></span><span id="d3dxshader_optimization_level0"></span><dl> <dt>**D3DXSHADER \_ Optimierung \_ LEVEL0**</dt> <dt>/o0</dt> </dl>                                    | Niedrigste Optimierungs Ebene. Erzeugt möglicherweise langsameren Code, führt dies jedoch schneller aus. Dies kann bei einem hochgradig iterativen shaderentwicklungsprozess nützlich sein.<br/> Direct3D 9-Nein<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL1"></span><span id="d3dxshader_optimization_level1"></span><dl> <dt>**D3DXSHADER \_ Optimierung \_ Level1**</dt> <dt>/O1</dt> </dl>                                    | Die zweite niedrigste Optimierungs Ebene.<br/> Direct3D 9-Nein<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL2"></span><span id="d3dxshader_optimization_level2"></span><dl> <dt>**D3DXSHADER \_ Optimierung \_ Level2**</dt> <dt>/O2</dt> </dl>                                    | Die zweithöchste Optimierungs Ebene.<br/> Direct3D 9-Nein<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL3"></span><span id="d3dxshader_optimization_level3"></span><dl> <dt>**D3DXSHADER \_ Optimierung \_ LEVEL3**</dt> <dt>/O3</dt> </dl>                                    | Höchste Optimierungs Ebene. Erzeugt einen bestmöglichen Code, kann aber erheblich länger dauern. Dies ist nützlich für endgültige Builds einer Anwendung, bei der die Leistung der wichtigste Faktor ist.<br/> Direct3D 9-Nein<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_PARTIALPRECISION"></span><span id="d3dxshader_partialprecision"></span><dl> <dt>**D3DXSHADER \_ Partialprecision**</dt> <dt>/GPP</dt> </dl>                                             | Erzwingen, dass alle Berechnungen im resultierenden Shader mit teilweiser Genauigkeit auftreten. Dies kann zu einer schnelleren Auswertung von Shadern auf Hardware führen.<br/> Direct3D 9-Ja<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="D3DXSHADER_PREFER_FLOW_CONTROL"></span><span id="d3dxshader_prefer_flow_control"></span><dl> <dt>**D3DXSHADER \_ \_Fluss \_ Steuerung bevorzugen**</dt> <dt>/GFP</dt> </dl>                                  | Dies ist ein Hinweis für den Compiler, die Anweisungen zur Fluss Steuerung bevorzugen.<br/> Direct3D 9-Ja<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DXSHADER_SKIPOPTIMIZATION"></span><span id="d3dxshader_skipoptimization"></span><dl> <dt>**D3DXSHADER \_ Skipoptimization**</dt> <dt>/od</dt> </dl>                                              | Weisen Sie den Compiler an, während der Codegenerierung Optimierungsschritte zu überspringen. Wenn Sie versuchen, ein Problem im Code zu isolieren, und Sie den Compiler vermuten, wird die Verwendung dieser Option nicht empfohlen.<br/> Direct3D 9-Ja<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ Skipvalidation**</dt> <dt>/VD</dt> </dl>                                                    | Validieren Sie den generierten Code nicht mit bekannten Funktionen und Einschränkungen. Diese Option wird nur beim Kompilieren von Shadern empfohlen, die bekanntermaßen funktionieren (d. h. Shader, die zuvor ohne diese Option kompiliert wurden). Shader werden immer von der Laufzeit überprüft, bevor Sie auf das Gerät festgelegt werden.<br/> Direct3D 9-Ja<br/> Direct3D 10-Ja<br/>                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_USE_LEGACY_D3DX9_31_DLL"></span><span id="d3dxshader_use_legacy_d3dx9_31_dll"></span><dl> <dt>**D3DXSHADER \_ \_Ältere \_ D3DX9 31 \_ - \_ dll verwenden**</dt> <dt>/LD</dt> </dl>                     | Aktivieren Sie die Verwendung des ursprünglichen Direct3D 9 HLSL-Compilers. OCT2006 \_ d3dx9 \_ 31 \_x86.cab oder OCT2006 \_ d3dx9 \_ 31 \_x64.cab muss als Teil des Redist der Anwendungen enthalten sein. Dieses Flag ist erforderlich, um PS \_ 1 \_ x-Shader zu kompilieren, ohne das promotionflag für PS \_ 2 0 zu verwenden \_ . Wenn Sie dieses Flag beim Abrufen einer [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) -Schnittstelle angeben, bewirkt dies, dass nachfolgende Aufrufe von [**compileeffect**](id3dxeffectcompiler--compileeffect.md) und [**compileshader**](id3dxeffectcompiler--compileshader.md) über dieses Objekt den Legacy Compiler verwenden.<br/> Direct3D 9-Ja<br/> Direct3D 10-Nein<br/> |



**AssemblyFlags**

AssemblyFlags werden vom Effektsystem verwendet, um den shadercode zu optimieren und den Code zu beeinflussen.



| Konstante                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ Debuggen**</dt> </dl>                                                          | Fügen Sie während der shaderkompilierung debugdateiname, Zeilennummern und Typ-und Symbol Informationen ein.<br/>                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ Force \_ PS \_ Software \_ noopt**</dt> </dl> | Erzwingen Sie, dass der Compiler mit dem nächsthöchsten verfügbaren Software Ziel für Pixel-Shader kompiliert wird. Dieses Flag deaktiviert auch Optimierungen und Debuggen.<br/>                                                                                                                                                  |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ Force \_ vs \_ Software \_ noopt**</dt> </dl> | Erzwingen Sie, dass der Compiler mit dem nächsthöchsten verfügbaren Software Ziel für Vertexshader kompiliert wird. Dieses Flag deaktiviert auch Optimierungen und Debuggen.<br/>                                                                                                                                                 |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ skipvalidation**</dt> </dl>                               | Validieren Sie den generierten Code nicht mit bekannten Funktionen und Einschränkungen. Diese Option wird nur beim Kompilieren von Shadern empfohlen, die bekanntermaßen funktionieren (d. h. Shader, die zuvor ohne diese Option kompiliert wurden). Shader werden immer von der Laufzeit überprüft, bevor Sie auf das Gerät festgelegt werden.<br/> |



## <a name="remarks"></a>Bemerkungen

Das Effektsystem verwendet **parserflags** , wenn die folgenden Funktionen aufgerufen werden:

-   [**D3DXCompileShader**](d3dxcompileshader.md)
-   [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
-   [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
-   [**Compileeffect**](id3dxeffectcompiler--compileeffect.md)

Das Effektsystem verwendet **Compilerflags** , wenn die folgenden Funktionen aufgerufen werden:

-   [**D3DXCompileShader**](d3dxcompileshader.md) (oder [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md) oder [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md))
-   [**Compileeffect**](id3dxeffectcompiler--compileeffect.md) (oder [**compileshader**](id3dxeffectcompiler--compileshader.md))

Außerdem können Sie **Compilerflags** verwenden, wenn Sie einen Effekt durch Aufrufen von [**D3DXCreateEffect**](d3dxcreateeffect.md) (oder [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) oder [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)) erzeugen.

-   Wenn Sie eine nicht kompilierte FX-Datei übergeben, verwendet das Effect-System den Flag-Eingabeparameter während der Kompilierung.
-   Wenn Sie einen kompilierten Effekt übergeben, ignoriert das Effektsystem die Compilerflags, da Sie zum Laden des Effekts nicht benötigt werden.

Das Effektsystem verwendet **AssemblyFlags** , wenn die folgenden Funktionen aufgerufen werden:

-   [**D3DXAssembleShader**](d3dxassembleshader.md)
-   [**D3DXAssembleShaderFromFile**](d3dxassembleshaderfromfile.md)
-   [**D3DXAssembleShaderFromResource**](d3dxassembleshaderfromresource.md)

Das Anwenden von **Compilerflags** oder **AssemblyFlags** auf die falsche API schlägt die Shader-Validierung fehl. Überprüfen Sie den Rückgabewert des Direct3D-Fehlercodes aus der Funktion mit dem DirectX-Fehler Such Tool (DXErr.exe), um diesen Fehler zu ermitteln. Sie erhalten DXErr.exe und erfahren mehr über das DirectX SDK. Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Konstanten](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 
