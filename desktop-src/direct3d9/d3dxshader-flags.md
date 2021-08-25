---
description: Die D3DXSHADER-Flags werden zum Analyse-, Kompilieren oder Zusammenstellen von Shadern verwendet.
ms.assetid: 8558d0e9-d09f-4c62-bc89-6080f4e44ff8
title: D3DXSHADER-Flags (D3dx9shader.h)
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
ms.openlocfilehash: 031ae23301b78a9cced683551c9d7220aa66f7e0a48b504fe1a93721fd8d6a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849780"
---
# <a name="d3dxshader-flags"></a>D3DXSHADER-Flags

Die **D3DXSHADER-Flags** werden zum Analyse,Kompilieren oder Zusammenstellen von Shadern verwendet.

**Parserflags**

Analysezeitflags werden vom Effektsystem (vor der Kompilierung von Effekten) nur verwendet, wenn Sie einen Effektcompiler erstellen. Beispielsweise können Sie ein Compilerobjekt mit **D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR** erstellen und dieses Compilerobjekt dann wiederholt mit verschiedenen Compilerflags verwenden, um spezialisierten Code zu generieren.



| Konstante                                                                                                                                                                                                                   | Beschreibung                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_PACKMATRIX_COLUMNMAJOR"></span><span id="d3dxshader_packmatrix_columnmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR**</dt> </dl> | Sofern nicht explizit angegeben, werden Matrizen in spalten wichtiger Reihenfolge gepackt (jeder Vektor ist in einer einzelnen Spalte enthalten), wenn sie an den shader und vom Shader übergeben werden. Dies ist im Allgemeinen effizienter, da die Vektormatrixmultiplikation mit einer Reihe von Punktprodukten durchgeführt werden kann.<br/> |
| <span id="D3DXSHADER_PACKMATRIX_ROWMAJOR"></span><span id="d3dxshader_packmatrix_rowmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ ROWMAJOR**</dt> </dl>          | Sofern nicht explizit angegeben, werden Matrizen in zeilen wichtiger Reihenfolge gepackt (jeder Vektor wird in einer einzelnen Zeile angegeben), wenn sie an den shader oder vom Shader übergeben werden.<br/>                                                                                                                                        |



**Compilerflags**

Der DirectX 10 HLSL-Compiler ist jetzt der Standardcompiler. Weitere [Informationen finden Sie unter Effect-Compiler Tool](../direct3dtools/fxc.md) .

In der folgenden Tabelle sind die flags aufgeführt, die in Direct3D 9 und Direct3D 10 verfügbar sind. Der Wert für das Flag ist die entsprechende fxc-Option.



| Konstante/Wert                                                                                                                                                                                                                                                                                                | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_AVOID_FLOW_CONTROL"></span><span id="d3dxshader_avoid_flow_control"></span><dl> <dt>**D3DXSHADER \_ VERMEIDEN \_ DER \_ FLUSSSTEUERUNG/GFA**</dt> <dt></dt> </dl>                                     | Dies ist ein Hinweis an den Compiler, um die Verwendung von Anweisungen zur Flusssteuerung zu vermeiden.<br/> Direct3D 9 – Ja<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ DEBUG**</dt> <dt>/Zi</dt> </dl>                                                                               | Fügen Sie während der Shader-Kompilierung Debugdateiname, Zeilennummern sowie Typ- und Symbolinformationen ein.<br/> Direct3D 9 – Ja<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dxshader_enable_backwards_compatibility"></span><dl> <dt>**D3DXSHADER \_ ENABLE \_ BACKWARDS \_ COMPATIBILITY**</dt> <dt>/Gec</dt> </dl> | Kompilieren Sie ps \_ 1 \_ x Shader als ps \_ 2 \_ 0. Effekte, die ps 1 x-Ziele angeben, kompilieren stattdessen in ps 2 0-Ziele, da dies die minimale Shaderversion ist, die von der Version des Shadercompilers unterstützt wird, die \_ \_ mit \_ \_ DirectX 10 ausgeliefert wird. Dieses Flag hat keine Auswirkungen, wenn es mit Kompilierungszielen auf höherer Ebene verwendet wird.<br/> Direct3D 9 – nein<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ PS \_ SOFTWARE \_ NOOPT**</dt> <dt>N/A</dt> </dl>                      | Erzwingen Sie, dass der Compiler für das nächste verfügbare Softwareziel für Pixel-Shader kompiliert wird. Dieses Flag deaktiviert auch Optimierungen und das Debuggen.<br/> Direct3D 9 – Ja<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ VS \_ SOFTWARE \_ NOOPT**</dt> <dt>N/A</dt> </dl>                      | Erzwingen Sie, dass der Compiler für das nächste verfügbare Softwareziel für Vertex-Shader kompiliert wird. Dieses Flag deaktiviert auch Optimierungen und das Debuggen.<br/> Direct3D 9 – Ja<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_IEEE_STRICTNESS"></span><span id="d3dxshader_ieee_strictness"></span><dl> <dt>**D3DXSHADER \_ IEEE \_ STRICTNESS**</dt> <dt>/Ieee</dt> </dl>                                               | Deaktivieren Sie Optimierungen, die dazu führen können, dass sich die Ausgabe eines kompilierten Shaderprogramms von der Ausgabe eines Programms unterscheidet, das mit dem DirectX 9-Shadercompiler kompiliert wurde. Dies liegt an kleinen Genauigkeitserros in gleitkomma mathematischen Berechnungen.<br/> Direct3D 9 – nein<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="D3DXSHADER_NO_PRESHADER"></span><span id="d3dxshader_no_preshader"></span><dl> <dt>**D3DXSHADER \_ NO \_ PRESHADER**</dt> <dt>/Op</dt> </dl>                                                         | Deaktiviert Preshader. Der Compiler pullt keine statischen Ausdrücke für die Auswertung auf der Host-CPU. Darüber hinaus wird der Compiler beim Kompilieren eigenständiger Funktionen keine Ausdrücke komilieren.<br/> Direct3D 9 – Ja<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL0"></span><span id="d3dxshader_optimization_level0"></span><dl> <dt>**D3DXSHADER \_ OPTIMIERUNGSSTUFE \_ 0**</dt> <dt>/O0</dt> </dl>                                    | Niedrigste Optimierungsstufe. Kann langsameren Code erzeugen, wird dies jedoch schneller tun. Dies kann in einem hochgradig iterativen Shader-Entwicklungszyklus nützlich sein.<br/> Direct3D 9 – nein<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL1"></span><span id="d3dxshader_optimization_level1"></span><dl> <dt>**D3DXSHADER \_ \_OPTIMIERUNGSSTUFE1**</dt> <dt>/O1</dt> </dl>                                    | Die zweit niedrigste Optimierungsstufe.<br/> Direct3D 9 – nein<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL2"></span><span id="d3dxshader_optimization_level2"></span><dl> <dt>**D3DXSHADER \_ \_OPTIMIERUNGSSTUFE2/O2**</dt> <dt></dt> </dl>                                    | Die zweit höchste Optimierungsstufe.<br/> Direct3D 9 – nein<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL3"></span><span id="d3dxshader_optimization_level3"></span><dl> <dt>**D3DXSHADER \_ OPTIMIERUNGSSTUFE \_ 3/O3**</dt> <dt></dt> </dl>                                    | Höchste Optimierungsstufe. Erzeugt den bestmöglichen Code, kann aber deutlich länger dauern. Dies ist nützlich für endgültige Builds einer Anwendung, bei denen die Leistung der wichtigste Faktor ist.<br/> Direct3D 9 – nein<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_PARTIALPRECISION"></span><span id="d3dxshader_partialprecision"></span><dl> <dt>**D3DXSHADER \_ PARTIALPRECISION**</dt> <dt>/Gpp</dt> </dl>                                             | Erzwingen Sie, dass alle Berechnungen im resultierenden Shader mit teilweiser Genauigkeit ausgeführt werden. Dies kann zu einer schnelleren Auswertung von Shadern auf einigen Hardwarekomponenten führen.<br/> Direct3D 9 – Ja<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="D3DXSHADER_PREFER_FLOW_CONTROL"></span><span id="d3dxshader_prefer_flow_control"></span><dl> <dt>**D3DXSHADER \_ BEVORZUGTER ABLAUFSTEUERUNGS-/Ablaufsteuerungs-/-ZIEH-STEUERELEMENT \_ \_**</dt> <dt></dt> </dl>                                  | Dies ist ein Hinweis an den Compiler, die Verwendung von Anweisungen zur Flusssteuerung zu bevorzugen.<br/> Direct3D 9 – Ja<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DXSHADER_SKIPOPTIMIZATION"></span><span id="d3dxshader_skipoptimization"></span><dl> <dt>**D3DXSHADER \_ SKIPOPTIMIZATION**</dt> <dt>/Od</dt> </dl>                                              | Weisen Sie den Compiler an, optimierungsschritte während der Codegenerierung zu überspringen. Die Verwendung dieser Option wird nicht empfohlen, es sei denn, Sie versuchen, ein Problem im Code zu isolieren und den Compiler zu vermuten.<br/> Direct3D 9 – Ja<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ SKIPVALIDATION**</dt> <dt>/Vd</dt> </dl>                                                    | Überprüfen Sie den generierten Code nicht anhand bekannter Funktionen und Einschränkungen. Diese Option wird nur empfohlen, wenn Sie Shader kompilieren, die bekanntert funktionieren (d. h. Shader, die zuvor ohne diese Option kompiliert wurden). Shader werden immer von der Runtime überprüft, bevor sie auf das Gerät festgelegt werden.<br/> Direct3D 9 – Ja<br/> Direct3D 10 – Ja<br/>                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_USE_LEGACY_D3DX9_31_DLL"></span><span id="d3dxshader_use_legacy_d3dx9_31_dll"></span><dl> <dt>**D3DXSHADER \_ USE \_ LEGACY \_ D3DX9 \_ 31 \_ DLL**</dt> <dt>/LD</dt> </dl>                     | Aktivieren Sie die Verwendung des ursprünglichen Direct3D 9 HLSL-Compilers. OCT2006 \_ d3dx9 \_ 31x86.cab oder \_ OCT2006 \_ d3dx9 \_ 31x64.cab müssen als Teil der \_ Redist-Anwendung enthalten sein. Dieses Flag ist erforderlich, um ps 1 x-Shader zu kompilieren, ohne das -Promotionflag zu \_ \_ ps \_ 2 \_ 0 zu verwenden. Die Angabe dieses Flags beim Abrufen einer [**ID3DXEffectCompiler-Schnittstelle**](id3dxeffectcompiler.md) bewirkt, dass nachfolgende Aufrufe von [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) und [**CompileShader**](id3dxeffectcompiler--compileshader.md) über dieses Objekt den Legacycompiler verwenden.<br/> Direct3D 9 – Ja<br/> Direct3D 10 – nein<br/> |



**Assemblerflags**

Assemblerflags werden vom Effektsystem verwendet, um Shader- und Effekt-Assemblycode zu optimieren.



| Konstante                                                                                                                                                                                                                        | Beschreibung                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ DEBUG**</dt> </dl>                                                          | Fügen Sie während der Shader-Kompilierung Debugdateiname, Zeilennummern sowie Typ- und Symbolinformationen ein.<br/>                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ PS \_ SOFTWARE \_ NOOPT**</dt> </dl> | Erzwingen Sie, dass der Compiler für das nächste verfügbare Softwareziel für Pixel-Shader kompiliert wird. Dieses Flag deaktiviert auch Optimierungen und das Debuggen.<br/>                                                                                                                                                  |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ VS \_ SOFTWARE \_ NOOPT**</dt> </dl> | Erzwingen Sie, dass der Compiler für das nächste verfügbare Softwareziel für Vertex-Shader kompiliert wird. Dieses Flag deaktiviert auch Optimierungen und das Debuggen.<br/>                                                                                                                                                 |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ SKIPVALIDATION**</dt> </dl>                               | Überprüfen Sie den generierten Code nicht anhand bekannter Funktionen und Einschränkungen. Diese Option wird nur empfohlen, wenn Sie Shader kompilieren, die bekanntert funktionieren (d. h. Shader, die zuvor ohne diese Option kompiliert wurden). Shader werden immer von der Runtime überprüft, bevor sie auf das Gerät festgelegt werden.<br/> |



## <a name="remarks"></a>Hinweise

Das Effektsystem verwendet **Parserflags, wenn** es von den folgenden Funktionen aufgerufen wird:

-   [**D3DXCompileShader**](d3dxcompileshader.md)
-   [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
-   [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md)

Das Effektsystem verwendet **Compilerflags,** wenn es von den folgenden Funktionen aufgerufen wird:

-   [**D3DXCompileShader**](d3dxcompileshader.md) (oder [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md) oder [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md))
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) (oder [**CompileShader**](id3dxeffectcompiler--compileshader.md))

Darüber hinaus können  Sie Compilerflags verwenden, wenn Sie einen Effekt erstellen, indem Sie [**D3DXCreateEffect**](d3dxcreateeffect.md) (oder [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) oder [**D3DXCreateEffectFromResource) aufrufen.**](d3dxcreateeffectfromresource.md)

-   Wenn Sie eine nicht kompilierte FX-Datei übergeben, verwendet das Effektsystem den Flageingabeparameter während der Kompilierung.
-   Wenn Sie einen kompilierten Effekt übergeben, ignoriert das Effektsystem die Compilerflags, da sie zum Laden des Effekts nicht erforderlich sind.

Das Effektsystem verwendet **Assemblerflags, wenn** es von den folgenden Funktionen aufgerufen wird:

-   [**D3DXAssembleShader**](d3dxassembleshader.md)
-   [**D3DXAssembleShaderFromFile**](d3dxassembleshaderfromfile.md)
-   [**D3DXAssembleShaderFromResource**](d3dxassembleshaderfromresource.md)

Das **Anwenden von Compilerflags** **oder Assemblerflags** auf die falsche API ist bei der Shaderüberprüfung nicht erfolgreich. Überprüfen Sie den Rückgabewert des Direct3D-Fehlercodes aus der Funktion mit dem DirectX Error Lookup Tool (DXErr.exe), um diesen Fehler zu finden. Sie können sich DXErr.exe DirectX SDK darüber informieren. Informationen zum DirectX SDK finden Sie unter [Wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Konstanten](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 
