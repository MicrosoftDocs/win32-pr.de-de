---
title: Angeben von Stamm Signaturen in HLSL
description: Das Angeben von Stamm Signaturen im HLSL-Shader-Modell 5,1 ist eine Alternative zur Angabe in C++-Code.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236876e22c3e1e0bb849ec1e1bc7d45692c900d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548641"
---
# <a name="specifying-root-signatures-in-hlsl"></a>Angeben von Stamm Signaturen in HLSL

Das Angeben von Stamm Signaturen im HLSL-Shader-Modell 5,1 ist eine Alternative zur Angabe in C++-Code.

-   [Ein Beispiel für eine HLSL-Stamm Signatur](#an-example-hlsl-root-signature)
    -   [Stamm Signatur Version 1,0](#root-signature-version-10)
    -   [Stamm Signatur Version 1,1](#root-signature-version-11)
-   [RootFlags](#rootflags)
-   [Stamm Konstanten](#root-constants)
-   [Sichtbarkeit](#visibility)
-   [CBV auf Stamm Ebene](#root-level-cbv)
-   [SRV auf Stamm Ebene](#root-level-srv)
-   [UAV auf Stamm Ebene](#root-level-uav)
-   [Deskriptortabelle](#descriptor-table)
-   [Statischer Sampler](#static-sampler)
-   [Kompilieren einer HLSL-Stamm Signatur](#compiling-an-hlsl-root-signature)
-   [Manipulieren von Stamm Signaturen mit dem FXC-Compiler](#manipulating-root-signatures-with-the-fxc-compiler)
-   [Hinweise](#notes)
-   [Verwandte Themen](#related-topics)

## <a name="an-example-hlsl-root-signature"></a>Ein Beispiel für eine HLSL-Stamm Signatur

Eine Stamm Signatur kann in HLSL als Zeichenfolge angegeben werden. Die Zeichenfolge enthält eine Auflistung von durch Kommas getrennten Klauseln, die Komponenten der Stamm Signatur Komponenten beschreiben. Die Stamm Signatur sollte für alle einzelnen Pipeline Zustands Objekte (PSO) über Shader hinweg identisch sein. Beispiel:

### <a name="root-signature-version-10"></a>Stamm Signatur Version 1,0

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

### <a name="root-signature-version-11"></a>Stamm Signatur Version 1,1

Die Stamm [Signatur Version 1,1](root-signature-version-1-1.md) ermöglicht Treiber Optimierungen für Stamm Signatur Deskriptoren und-Daten.

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

Diese Definition hat die folgende Stamm Signatur:

-   Die Verwendung von Standardparametern.
-   B0 und (B0, Space = 1) treten nicht in Konflikt
-   U0 ist nur für den Geometry-Shader sichtbar.
-   U4 und U5 werden mit dem gleichen Deskriptor in einem Heap versehen

![eine mit der High-Level-Shader-Sprache angegebene Stamm Signatur](images/hlsl-root-signature.png)

Die HLSL-Stamm Signatur Sprache entspricht eng den C++-Stamm Signatur-APIs und verfügt über äquivalente Ausdrucksstärke. Die Stamm Signatur wird als Sequenz von Klauseln angegeben, die durch Kommas getrennt sind. Die Reihenfolge der Klauseln ist wichtig, da die Reihenfolge der Verarbeitung die slotposition in der Stamm Signatur bestimmt. Jede Klausel nimmt einen oder mehrere benannte Parameter an. Die Reihenfolge der Parameter ist jedoch nicht wichtig.

## <a name="rootflags"></a>RootFlags

Die optionale *rootFlags* -Klausel nimmt entweder 0 (der Standardwert, um keine Flags anzugeben) oder einen oder mehrere vordefinierte stammflags-Werte an, die über den-Operator oder den-Operator verbunden sind \| . Die zulässigen stammflag-Werte werden durch [**D3D12 \_ root \_ Signature- \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)definiert.

Beispiel:

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a>Stamm Konstanten

Die *rootconstants* -Klausel gibt Stamm Konstanten in der Stamm Signatur an. Zwei obligatorische Parameter sind: *num32BitConstants* und *Breg* (das Register, das *baseshaderregister* in C++-APIs entspricht) des *cBuffer*. Die Parameter Space (*registerspace* in C++ APIs) und Visibility (*shadervisibility* in C++) sind optional, und die Standardwerte lauten:

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

Beispiel:

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a>Sicht

Visibility ist ein optionaler Parameter, der einen der Werte aus [**D3D12 \_ Shader \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)aufweisen kann.

Shader \_ Visibility \_ überträgt alle Stamm Argumente an alle Shader. Bei manchen Hardwarekosten fallen keine Kosten an, aber auf anderer Hardware entstehen Kosten für die Verzweigung der Daten in allen shaderphasen. Wenn Sie eine der Optionen festlegen, z. b. Shader \_ Visibility \_ Vertex, schränkt das Root-Argument auf eine einzelne Shader-Stufe ein.

Durch das Festlegen von Stamm Argumenten auf einzelne Shader-Stufen kann derselbe Bindungs Name in verschiedenen Phasen verwendet werden. Beispielsweise wäre eine SRV-Bindung von `t0,SHADER_VISIBILITY_VERTEX` und SRV-Bindung von `t0,SHADER_VISIBILITY_PIXEL` gültig. Wenn die Sichtbarkeits Einstellung jedoch `t0,SHADER_VISIBILITY_ALL` für eine der Bindungen gilt, wäre die Stamm Signatur ungültig.

## <a name="root-level-cbv"></a>CBV auf Stamm Ebene

Die `CBV` (Konstante Puffer Ansicht)-Klausel gibt einen konstanten Puffer b-Register-reg-Eintrag auf Stamm Ebene an. Beachten Sie, dass es sich hierbei um einen skalaren Eintrag handelt. Es ist nicht möglich, einen Bereich für die Stamm Ebene anzugeben.

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a>SRV auf Stamm Ebene

Die `SRV` (Shader Resource View)-Klausel gibt einen SRV t-Register-reg-Eintrag auf Stamm Ebene an. Beachten Sie, dass es sich hierbei um einen skalaren Eintrag handelt. Es ist nicht möglich, einen Bereich für die Stamm Ebene anzugeben.

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a>UAV auf Stamm Ebene

Die `UAV` (unsortierter Zugriffs Ansicht)-Klausel gibt einen UAV-Registrierungs Eintrag auf Stamm Ebene an. Beachten Sie, dass es sich hierbei um einen skalaren Eintrag handelt. Es ist nicht möglich, einen Bereich für die Stamm Ebene anzugeben.

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

Die- `DescriptorTable` Klausel ist selbst eine Liste von durch Trennzeichen getrennten deskriptortabellenklauseln und ein optionaler Visibility-Parameter. Die *deskriptortable* -Klauseln umfassen CBV, SRV, UAV und Sampler. Beachten Sie, dass sich Ihre Parameter von denen der Klauseln der Stamm Ebene unterscheiden.

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

Die Deskriptortabelle `CBV` weist die folgende Syntax auf:

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Beispiel:

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

Der obligatorische Parameter *Breg* gibt die Start-reg des cBuffer-Bereichs an. Der *numdescriptors* -Parameter gibt die Anzahl der Deskriptoren im zusammenhängenden cBuffer-Bereich an. der Standardwert ist 1. Der-Eintrag deklariert einen cBuffer-Bereich ` [Reg, Reg + numDescriptors - 1]` , wenn *numdescriptors* eine Zahl ist. Wenn *numdescriptors* gleich "unbegrenzt" ist, ist der Bereich. dies `[Reg, UINT_MAX]` bedeutet, dass die APP sicherstellen muss, dass Sie nicht auf einen Out-of-Bounds-Bereich verweist. Das *Offset* Feld stellt den *offsetindescriptorsfromtablestart* -Parameter in den C++-APIs dar, d. h. den Offset (in den Deskriptoren) vom Beginn der Tabelle. Wenn der Offset auf den Wert des deskriptorbereichoffsets angefügt wird \_ \_ \_ (Standardeinstellung), bedeutet dies, dass sich der Bereich direkt hinter dem vorherigen Bereich befindet. Durch die Eingabe bestimmter Offsets können sich Bereiche jedoch untereinander überlappen, was das Registrieren von Aliasing ermöglicht.

Die Deskriptortabelle `SRV` weist die folgende Syntax auf:

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Dies ähnelt dem `CBV` deskriptortabelleneintrag, mit dem Unterschied, dass der angegebene Bereich für Shader-Ressourcen Sichten gilt.

Die Deskriptortabelle `UAV` weist die folgende Syntax auf:

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Dies ähnelt dem `CBV` deskriptortabelleneintrag, mit dem Unterschied, dass der angegebene Bereich für ungeordnete Zugriffs Sichten gilt.

Die Deskriptortabelle `Sampler` weist die folgende Syntax auf:

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

Dies ähnelt dem `CBV` deskriptortabelleneintrag, mit dem Unterschied, dass der angegebene Bereich für Shader-Samplers ist. Beachten Sie, dass Samplers nicht mit anderen Typen von Deskriptoren in derselben Deskriptortabelle gemischt werden können (da Sie sich in einem separaten deskriptorheap befinden).

## <a name="static-sampler"></a>Statischer Sampler

Der statische Sampler stellt die [**statische D3D12- \_ \_ \_ samplerstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) dar. Der obligatorische Parameter für *staticsampler* ist ein Skalar, Sampler s-Register reg. Andere Parameter sind optional, wobei die Standardwerte unten angezeigt werden. Die meisten Felder akzeptieren eine Reihe vordefinierter enums.

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

Die Parameter Optionen ähneln den C++-API-aufrufen, ausgenommen *BorderColor*, das auf eine Enumeration in HLSL beschränkt ist.

Das Filter Feld kann einen der [**\_ Filter "D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)" aufweisen.

Die Adressfelder können jeweils einen der [**D3D12- \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode)aufweisen.

Bei der Vergleichsfunktion kann es sich um einen [**D3D12 \_ Vergleichs \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)handeln.

Das Rahmen Farbfeld kann eine der [**statischen Rahmen \_ \_ \_ Farben D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color)sein.

Sichtbarkeit kann eine der [**D3D12- \_ Shader- \_ Sichtbarkeit**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)sein.

## <a name="compiling-an-hlsl-root-signature"></a>Kompilieren einer HLSL-Stamm Signatur

Es gibt zwei Mechanismen zum Kompilieren einer HLSL-Stamm Signatur. Zunächst ist es möglich, eine Stamm Signatur Zeichenfolge über das *rootsignature* -Attribut an einen bestimmten Shader anzufügen (im folgenden Beispiel mit dem **MyRS1** -Einstiegspunkt):

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

Der Compiler erstellt und überprüft das Stamm Signatur-BLOB für den Shader und bettet ihn zusammen mit dem Shader-Bytecode in das Shader-BLOB ein. Der Compiler unterstützt die Stamm Signatur Syntax für das Shader-Modell 5,0 und höher. Wenn eine Stamm Signatur in ein Shader-Modell 5,0-Shader eingebettet ist und dieser Shader an die D3D11-Laufzeit gesendet wird (im Gegensatz zu D3D12), wird der Stamm Signatur Teil von D3D11 automatisch ignoriert.

Der andere Mechanismus besteht darin, einen eigenständigen Stamm Signatur-BLOB zu erstellen, um ihn ggf. mit einem großen Satz von Shadern wiederzuverwenden und Speicherplatz zu sparen. Das [Effekt-Compilertool](/windows/desktop/direct3dtools/fxc) (FXC) unterstützt sowohl **rootsig \_ 1 \_ 0** -als auch **rootsig \_ 1 \_ 1** -shadermodelle. Der Name der definierenden Zeichenfolge wird über das übliche/E-Argument angegeben. Beispiel:

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

Beachten Sie, dass die Definition der Stamm Signatur Zeichenfolge auch in der Befehlszeile weitergegeben werden kann, z. b./D MyRS1 = "...".

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a>Manipulieren von Stamm Signaturen mit dem FXC-Compiler

Der FXC-Compiler erstellt Shader-Bytecode aus HLSL-Quelldateien. Es gibt zahlreiche optionale Parameter für diesen Compiler. Weitere Informationen finden Sie im [Tool "Effect-Compiler](/windows/desktop/direct3dtools/fxc)".

In der folgenden Tabelle finden Sie einige Beispiele für die Verwendung von FXC zum Verwalten von erstellten HLSL-Stamm Signaturen.



| Linie | Befehlszeile                                                                 | Beschreibung                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | Kompiliert einen Shader für das Pixel-Shader 5,1-Ziel, die Shader-Quelle befindet sich in der Datei "shaderwithrootsig. HLSL", die eine Stamm Signatur enthält. Der Shader und die Stamm Signatur werden als separate BLOBs in der Binärdatei "RS1. FXO" kompiliert.    |
| 2    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | Extrahiert die Stamm Signatur aus der von Zeile 1 erstellten Datei, sodass die Datei "RS1. Rs. FXO" nur eine Stamm Signatur enthält.                                                                                                                      |
| 3    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | Entfernt die Stamm Signatur aus der von Zeile 1 erstellten Datei, sodass die Datei "RS1. entfernt. FXO" einen Shader ohne Stamm Signatur enthält.                                                                                                       |
| 4    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | Kombiniert einen Shader und eine Stamm Signatur in separaten Dateien zu einer Binärdatei, die beide BLOB-Dateien enthält. In diesem Beispiel ist "RS1. New. fx0" mit "RS1. fx0" in Zeile 1 identisch.                                                           |
| 5    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | Erstellt eine eigenständige Stamm Signatur-Binärdatei aus einer Quelle, die möglicherweise mehr als nur eine Stamm Signatur enthält. Beachten Sie das Ziel "rootsig \_ 1 \_ 0", und "RS1" ist der Name der Stamm Signatur ( \# define)-Makro Zeichenfolge in der HLSL-Datei. |



 

Die über FXC verfügbare Funktionalität ist auch Programm gesteuert mithilfe der [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) -Funktion verfügbar. Dieser Befehl kompiliert einen Shader mit einer Stamm Signatur oder einer eigenständigen Stamm Signatur (durch Festlegen des rootsig \_ 1 \_ 0-Ziels). [**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) und [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) können Stamm Signaturen extrahieren und an ein vorhandenes BLOB anfügen.Die D3D- \_ BLOB-Stamm \_ \_ Signatur wird verwendet, um den teittyp der Stamm Signatur-BLOB anzugeben. [**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) entfernt die Stamm Signatur (mit dem D3DCOMPILER \_ Strip \_ root \_ Signature-Flag) aus dem BLOB.

## <a name="notes"></a>Hinweise

> [!Note]  
> Die Offline Kompilierung von Shadern wird dringend empfohlen, wenn Shader zur Laufzeit kompiliert werden müssen, lesen Sie die Hinweise zu [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).

 

> [!Note]  
> Vorhandene HLSL-Assets müssen nicht geändert werden, um die zu verwendenden Stamm Signaturen zu verarbeiten.

 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Dynamische Indizierung mit HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[HLSL-Shader-Modell 5,1 Features für Direct3D 12](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Ressourcen Bindung](resource-binding.md)
</dt> <dt>

[Ressourcen Bindung in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Stamm Signaturen](root-signatures.md)
</dt> <dt>

[Shadermodell 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Von Shader angegebener Schablone-Verweis Wert](shader-specified-stencil-reference-value.md)
</dt> <dt>

[Typisierte nicht geordnete zugriffsansichts Ladungen](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 