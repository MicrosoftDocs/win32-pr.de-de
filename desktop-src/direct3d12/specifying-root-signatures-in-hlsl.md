---
title: Festlegen von Stammsignaturen in HLSL
description: Die Angabe von Stammsignaturen im HLSL-Shadermodell 5.1 ist eine Alternative zur Angabe in C++-Code.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad0da9f84d68fc1acbf53332d1cae4075f0faa
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492282"
---
# <a name="specifying-root-signatures-in-hlsl"></a>Festlegen von Stammsignaturen in HLSL

Das Angeben von Stammsignaturen im HLSL-Shadermodell 5.1 ist eine Alternative zur Angabe in C++-Code.

-   [Ein Beispiel für eine HLSL-Stammsignatur](#an-example-hlsl-root-signature)
    -   [Root Signature Version 1.0](#root-signature-version-10)
    -   [Stammsignatur, Version 1.1](#root-signature-version-11)
-   [RootFlags](#rootflags)
-   [Stammkonst constants](#root-constants)
-   [Sichtbarkeit](#visibility)
-   [CBV auf Stammebene](#root-level-cbv)
-   [SRV auf Stammebene](#root-level-srv)
-   [UAV auf Stammebene](#root-level-uav)
-   [Deskriptortabelle](#descriptor-table)
-   [Statischer Sampler](#static-sampler)
-   [Kompilieren einer HLSL-Stammsignatur](#compiling-an-hlsl-root-signature)
-   [Bearbeiten von Stammsignaturen mit dem FXC-Compiler](#manipulating-root-signatures-with-the-fxc-compiler)
-   [Hinweise](#notes)
-   [Zugehörige Themen](#related-topics)

## <a name="an-example-hlsl-root-signature"></a>Beispiel für eine HLSL-Stammsignatur

Eine Stammsignatur kann in HLSL als Zeichenfolge angegeben werden. Die Zeichenfolge enthält eine Auflistung von durch Komma getrennten Klauseln, die die Komponenten der Stammsignatur beschreiben. Die Stammsignatur sollte über Shader hinweg für jedes Pipelinezustandsobjekt (PSO) identisch sein. Beispiel:

### <a name="root-signature-version-10"></a>Root Signature Version 1.0

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

Diese Definition würde die folgende Stammsignatur enthalten, und es wird Folgendes notieren:

-   Die Verwendung von Standardparametern.
-   b0 und (b0, space=1) verursachen keinen Konflikt
-   u0 ist nur für den Geometrie-Shader sichtbar.
-   u4 und u5 werden mit dem gleichen Deskriptor in einem Heap als Alias verwendet.

![Eine Stammsignatur, die mithilfe der Shadersprache auf hoher Ebene angegeben wird](images/hlsl-root-signature.png)

### <a name="root-signature-version-11"></a>Stammsignatur, Version 1.1

[Root Signature Version 1.1](root-signature-version-1-1.md) ermöglicht Treiberoptimierungen für Stammsignaturdeskriptoren und -daten.

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

Die HLSL-Stammsignatursprache entspricht eng den C++-Stammsignatur-APIs und verfügt über eine entsprechende Ausdrucksstärke. Die Stammsignatur wird als Sequenz von Klauseln angegeben, die durch Kommas getrennt sind. Die Reihenfolge der Klauseln ist wichtig, da die Reihenfolge der Analyse die Slotposition in der Stammsignatur bestimmt. Jede Klausel nimmt einen oder mehrere benannte Parameter an. Die Reihenfolge der Parameter ist jedoch nicht wichtig.

## <a name="rootflags"></a>RootFlags

Die optionale *RootFlags-Klausel* verwendet entweder 0 (der Standardwert, um keine Flags anzugeben) oder einen oder mehrere vordefinierte Stammflagswerte, die über den \| OR ''-Operator verbunden sind. Die zulässigen Stammflagwerte werden durch [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)definiert.

Beispiel:

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a>Stammkonstanten

Die *RootConstants-Klausel* gibt Stammkonstanten in der Stammsignatur an. Zwei obligatorische Parameter sind: *num32BitConstants* und *bReg* (das Register, das *BaseShaderRegister* in C++-APIs entspricht) des *Cbuffers*. Die Parameter space (*RegisterSpace* in C++-APIs) und visibility (*ShaderVisibility* in C++) sind optional, und die Standardwerte lauten:

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

Beispiel:

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a>Sicht

Visibility ist ein optionaler Parameter, der einen der Werte aus [**D3D12 \_ SHADER \_ VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)aufweisen kann.

SHADER \_ VISIBILITY \_ ALL überträgt die Stammargumente an alle Shader. Bei einigen Hardwarekomponenten sind dies keine Kosten, aber auf anderer Hardware entstehen Kosten für das Verzweigen der Daten in alle Shaderstufen. Durch festlegen einer der Optionen, z. B. SHADER VISIBILITY VERTEX, wird das Stammargument auf \_ \_ eine einzelne Shaderstufe beschränkt.

Das Festlegen von Stammargumenten auf einzelne Shaderstufen ermöglicht die Verwendung desselben Bindungsnamens in verschiedenen Phasen. Beispielsweise wäre eine SRV-Bindung von `t0,SHADER_VISIBILITY_VERTEX` und eine SRV-Bindung `t0,SHADER_VISIBILITY_PIXEL` von gültig. Wenn die Sichtbarkeitseinstellung jedoch `t0,SHADER_VISIBILITY_ALL` für eine der Bindungen verwendet wird, wäre die Stammsignatur ungültig.

## <a name="root-level-cbv"></a>CBV auf Stammebene

Die `CBV` -Klausel (konstante Pufferansicht) gibt einen konstanten Puffer auf Stammebene an, der den Reg-Eintrag b-register enthält. Beachten Sie, dass dies ein skalarer Eintrag ist. Es ist nicht möglich, einen Bereich für die Stammebene anzugeben.

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a>SRV auf Stammebene

Die `SRV` -Klausel (Shaderressourcenansicht) gibt einen SRV-Eintrag auf Stammebene t-register Reg an. Beachten Sie, dass dies ein skalarer Eintrag ist. Es ist nicht möglich, einen Bereich für die Stammebene anzugeben.

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a>UAV auf Stammebene

Die `UAV` -Klausel (ungeordnete Zugriffsansicht) gibt einen UAV-u-register Reg-Eintrag auf Stammebene an. Beachten Sie, dass dies ein skalarer Eintrag ist. Es ist nicht möglich, einen Bereich für die Stammebene anzugeben.

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Beispiel:

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a>Deskriptortabelle

Die -Klausel selbst ist eine Liste von durch Komma getrennten Deskriptortabellenklauseln sowie ein `DescriptorTable` optionaler Sichtbarkeitsparameter. Die *DescriptorTable-Klauseln* umfassen CBV, SRV, UAV und Sampler. Beachten Sie, dass sich ihre Parameter von denen der Klauseln auf Stammebene unterscheiden.

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

Die Deskriptortabelle `CBV` hat die folgende Syntax:

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Beispiel:

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

Der obligatorische Parameter *bReg* gibt den Start-Reg des cbuffer-Bereichs an. Der *numDescriptors-Parameter* gibt die Anzahl der Deskriptoren im zusammenhängenden Cbufferbereich an. Der Standardwert ist 1. Der Eintrag deklariert einen Cbufferbereich, ` [Reg, Reg + numDescriptors - 1]` wenn *numDescriptors* eine Zahl ist. Wenn *numDescriptors* gleich "unbounded" ist, lautet der Bereich `[Reg, UINT_MAX]` , was bedeutet, dass die App sicherstellen muss, dass sie nicht auf einen Bereich außerhalb der Grenzen verweist. Das *Offsetfeld* stellt den *OffsetInDescriptorsFromTableStart-Parameter* in den C++-APIs dar, d. h. den Offset (in Deskriptoren) vom Anfang der Tabelle. Wenn der Offset auf DESCRIPTOR \_ RANGE \_ OFFSET APPEND \_ (Standardeinstellung) festgelegt ist, bedeutet dies, dass der Bereich direkt nach dem vorherigen Bereich liegt. Durch die Eingabe bestimmter Offsets können sich Bereiche jedoch überlappen, sodass Registeraliasing möglich ist.

Die Deskriptortabelle `SRV` weist die folgende Syntax auf:

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Dies ähnelt dem `CBV` Deskriptortabelleneintrag, mit dem Unterschied, dass der angegebene Bereich für Shaderressourcenansichten gilt.

Die Deskriptortabelle `UAV` weist die folgende Syntax auf:

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Dies ähnelt dem `CBV` Deskriptortabelleneintrag, mit dem Unterschied, dass der angegebene Bereich für unsortierte Zugriffsansichten gilt.

Die Deskriptortabelle `Sampler` weist die folgende Syntax auf:

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

Dies ähnelt dem `CBV` Deskriptortabelleneintrag, mit dem Unterschied, dass der angegebene Bereich für Shader-Sampler gilt. Beachten Sie, dass Sampler nicht mit anderen Deskriptortypen in derselben Deskriptortabelle kombiniert werden können (da sie sich in einem separaten Deskriptorheap befinden).

## <a name="static-sampler"></a>Statischer Sampler

Der statische Sampler stellt die [**D3D12 \_ STATIC \_ SAMPLER \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) dar. Der obligatorische Parameter für *StaticSampler* ist ein Skalar, Sampler s-register Reg. Andere Parameter sind mit den unten gezeigten Standardwerten optional. Die meisten Felder akzeptieren einen Satz vordefinierter Enumerationen.

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

Beispiel:

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

Die Parameteroptionen ähneln den C++-API-Aufrufen sehr, mit Ausnahme von *borderColor*, das auf eine Enumeration in HLSL beschränkt ist.

Das Filterfeld kann eines von [**D3D12 \_ FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)sein.

Die Adressfelder können jeweils eines von [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode)sein.

Die Vergleichsfunktion kann eine von [**D3D12 \_ COMPARISON \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)sein.

Das Rahmenfarbfeld kann [**D3D12 \_ STATIC BORDER COLOR \_ \_ sein.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color)

Sichtbarkeit kann [**D3D12 \_ SHADER \_ VISIBILITY sein.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)

## <a name="compiling-an-hlsl-root-signature"></a>Kompilieren einer HLSL-Stammsignatur

Es gibt zwei Mechanismen zum Kompilieren einer HLSL-Stammsignatur. Erstens ist es möglich, eine Stammsignaturzeichenfolge über das *RootSignature-Attribut* an einen bestimmten Shader anfügen (im folgenden Beispiel mithilfe des **MyRS1-Einstiegspunkts):**

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

Der Compiler erstellt und überprüft das Stammsignaturblob für den Shader und bettet es zusammen mit dem Shader-Bytecode in das Shaderblob ein. Der Compiler unterstützt die Stammsignatursyntax für Shadermodell 5.0 und höher. Wenn eine Stammsignatur in einen Shadermodell 5.0-Shader eingebettet ist und dieser Shader im Gegensatz zu D3D12 an die D3D11-Runtime gesendet wird, wird der Stammsignaturteil automatisch von D3D11 ignoriert.

Der andere Mechanismus besteht in der Erstellung eines eigenständigen Stammsignaturblobs, um es möglicherweise mit einer großen Gruppe von Shadern wiederzuverwenden, um Speicherplatz zu sparen. Das [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) unterstützt **sowohl rootsig \_ 1 \_ 0-** als auch **rootsig \_ 1 1-Shadermodelle. \_** Der Name der definierenden Zeichenfolge wird über das übliche /E-Argument angegeben. Beispiel:

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

Beachten Sie, dass die Definition der Stammsignaturzeichenfolge auch über die Befehlszeile übergeben werden kann, z.B. /D MyRS1="...".

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a>Bearbeiten von Stammsignaturen mit dem FXC-Compiler

Der FXC-Compiler erstellt Shader-Bytecode aus HLSL-Quelldateien. Es gibt viele optionale Parameter für diesen Compiler. Weitere Informationen finden Sie im [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc).

Die folgende Tabelle enthält einige Beispiele für die Verwendung von FXC für die Verwaltung von von HLSL-Stammsignaturen.



| Linie | Befehlszeile                                                                 | Beschreibung                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | Kompiliert einen Shader für das Pixel-Shader 5.1-Ziel. Die Shaderquelle befindet sich in der Datei shaderWithRootSig.hlsl, die eine Stammsignatur enthält. Der Shader und die Stammsignatur werden als separate Blobs in der Binärdatei rs1.fxo kompiliert.    |
| 2    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | Extrahiert die Stammsignatur aus der von Zeile 1 erstellten Datei, sodass die Datei rs1.rs.fxo nur eine Stammsignatur enthält.                                                                                                                      |
| 3    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | Entfernt die Stammsignatur aus der durch Zeile 1 erstellten Datei, sodass die Datei rs1.stripped.fxo einen Shader ohne Stammsignatur enthält.                                                                                                       |
| 4    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | Kombiniert einen Shader und eine Stammsignatur, die sich in separaten Dateien befinden, in einer Binärdatei, die beide Blobs enthält. In diesem Beispiel wäre rs1.new.fx0 mit rs1.fx0 in Zeile 1 identisch.                                                           |
| 5    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | Erstellt eine eigenständige Stammsignaturbinärdatei aus einer Quelle, die mehr als nur eine Stammsignatur enthalten kann. Beachten Sie das \_ Rootig 1 \_ 0-Ziel, und dass RS1 der Name der Stammsignatur \# (definieren) Makrozeichenfolge in der HLSL-Datei ist. |



 

Die über FXC verfügbare Funktionalität ist auch programmgesteuert mithilfe der [**D3DCompile-Funktion**](/windows/desktop/direct3dhlsl/d3dcompile) verfügbar. Mit diesem Aufruf wird ein Shader mit einer Stammsignatur oder einer eigenständigen Stammsignatur kompiliert (wobei das \_ Rootig-Ziel auf 1 0 festgelegt \_ wird). [**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) und [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) können Stammsignaturen extrahieren und an ein vorhandenes Blob anfügen.  D3D \_ BLOB ROOT SIGNATURE wird \_ \_ verwendet, um den Stammsignatur-Blobteiltyp anzugeben. [**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) entfernt die Stammsignatur (mithilfe des D3DCOMPILER \_ STRIP \_ ROOT \_ SIGNATURE-Flags) aus dem Blob.

## <a name="notes"></a>Hinweise

> [!Note]  
> Während die Offlinekompilierung von Shadern dringend empfohlen wird, wenn Shader zur Laufzeit kompiliert werden müssen, lesen Sie die Hinweise für [**D3DCompile2.**](/windows/desktop/direct3dhlsl/d3dcompile2)

 

> [!Note]  
> Vorhandene HLSL-Ressourcen müssen nicht geändert werden, um Stammsignaturen zu verarbeiten, die mit ihnen verwendet werden sollen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dynamische Indizierung mit HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[HLSL Shader Model 5.1 Features for Direct3D 12 (HLSL-Shadermodell 5.1-Features für Direct3D 12)](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Ressourcenbindung](resource-binding.md)
</dt> <dt>

[Ressourcenbindung in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Stammsignaturen](root-signatures.md)
</dt> <dt>

[Shadermodell 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Von Shader festgelegter Schablonenreferenzwert](shader-specified-stencil-reference-value.md)
</dt> <dt>

[Typisiertes Laden von ungeordneten Zugriffsansichten](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 
