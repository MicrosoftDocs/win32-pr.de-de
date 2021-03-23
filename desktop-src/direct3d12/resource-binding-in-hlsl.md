---
title: Ressourcen Bindung in HLSL
description: In diesem Thema werden einige spezifische Features der Verwendung des HLSL-Shader-Modells 5,1 (High Level Shader Language) mit Direct3D 12 beschrieben.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 749fed319f9ffe840f2b06512e337efa28081e24
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548710"
---
# <a name="resource-binding-in-hlsl"></a>Ressourcen Bindung in HLSL

In diesem Thema werden einige spezifische Features der Verwendung des HLSL- [Shader-Modells 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1) (High Level Shader Language) mit Direct3D 12 beschrieben. Alle Direct3D 12-Hardware unterstützt das Shader-Modell 5,1. die Unterstützung für dieses Modell hängt daher nicht von der Hardware Funktionsebene ab.

-   [Ressourcentypen und Arrays](#resource-types-and-arrays)
-   [Deskriptorarrays und Textur Arrays](#descriptor-arrays-and-texture-arrays)
-   [Ressourcen Aliasing](#resource-aliasing)
-   [Abweichung und Ableitungen](#divergence-and-derivatives)
-   [UAVs in Pixel-Shadern](#uavs-in-pixel-shaders)
-   [Konstantenpuffer](#constant-buffers)
-   [Bytecode-Änderungen in SM 5.1](#bytecode-changes-in-sm51)
-   [Beispiele für HLSL-Deklarationen](#example-hlsl-declarations)
-   [Verwandte Themen](#related-topics)

## <a name="resource-types-and-arrays"></a>Ressourcentypen und Arrays

Die Ressourcen Syntax von Shader Model 5 (SM 5.0) verwendet das- `register` Schlüsselwort, um wichtige Informationen über die Ressource an den HLSL-Compiler weiterzugeben. Die folgende Anweisung deklariert z. b. ein Array aus vier Texturen, die an Slots T3, T4, T5 und T6 gebunden sind. T3 ist der einzige in der-Anweisung angezeigte Registrierungs Slot, der einfach der erste im Array von vier ist.

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

Die Ressourcen Syntax von Shader Model 5,1 (SM 5.1) in HLSL basiert auf der vorhandenen Register Resource-Syntax, um das Portieren zu vereinfachen. Direct3D 12-Ressourcen in HLSL sind an virtuelle Register innerhalb logischer Register Plätze gebunden:

-   t – für Shader-Ressourcen Sichten (SRV)
-   s – für Samplern
-   u – für ungeordnete Zugriffs Sichten (UAV)
-   b – für konstantenpuffersichten (CBV)

Die Stamm Signatur, die auf den Shader verweist, muss mit den deklarierten Register Slots kompatibel sein. Der folgende Teil einer Stamm Signatur ist beispielsweise mit der Verwendung von Textur Slots T3 bis T6 kompatibel, da er eine Deskriptortabelle mit Slots t0 bis T98 beschreibt.

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

Eine Ressourcen Deklaration kann ein Skalar, ein 1D-Array oder ein mehrdimensionales Array sein:

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

SM 5.1 verwendet dieselben Ressourcentypen und Elementtypen wie SM 5.0. Die SM 5.1-Deklarations Limits sind flexibler und werden nur durch die Lauf Zeit-/Hardwarelimits eingeschränkt. Das `space` Schlüsselwort gibt an, an welchen logischen Register Bereich die deklarierte Variable gebunden ist. Wenn das `space` Schlüsselwort weggelassen wird, wird der standardmäßige Speicherplatz Index 0 implizit dem Bereich zugewiesen (sodass sich der `tex2` obige Bereich in befindet `space0` ). `register(t3,  space0)` führt niemals zu einem Konflikt mit `register(t3,  space1)` und mit einem Array in einem anderen Bereich, das T3 enthalten kann.

Eine Array Ressource kann eine unbegrenzte Größe aufweisen, die durch Angabe der ersten zu lefenden Dimension deklariert wird, oder 0:

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

Die entsprechende Deskriptortabelle könnte wie folgt lauten:

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

Ein ungebundenes Array in HLSL entspricht einer festgelegten Anzahl von `numDescriptors` in der Deskriptortabelle, und eine festgelegte Größe im HLSL entspricht einer ungebundenen Deklaration in der Deskriptortabelle.

Mehrdimensionale Arrays, einschließlich einer unbegrenzten Größe, sind zulässig. Diese mehrdimensionalen Arrays werden im Register Bereich reduziert.

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

Das Aliasing von Ressourcen Bereichen ist nicht zulässig. Mit anderen Worten: für jeden Ressourcentyp (t, s, u, b) dürfen sich deklarierte Register Bereiche nicht überlappen. Dies schließt auch unbegrenzte Bereiche ein. Bereiche, die in verschiedenen Register Bereichen deklariert werden, überlappen sich niemals Beachten Sie, dass `tex2` sich die unbegrenzte (oben) in befindet `space0` , während sich die unbegrenzte Grenze `tex3` in befindet `space1` , sodass Sie sich nicht überlappen.

Der Zugriff auf Ressourcen, die als Arrays deklariert wurden, ist so einfach wie die Indizierung.

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

Es gibt eine wichtige Standard Beschränkung für die Verwendung der Indizes ( `myMaterialID` und `samplerID` im obigen Code) darin, dass Sie innerhalb einer [Welle](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology)nicht variieren dürfen. Sogar das Ändern des Indexes auf der Grundlage der instanziierungsanzahl als unterschiedlich.

Wenn Sie den Index variieren müssen, geben Sie den `NonUniformResourceIndex` Qualifizierer für den Index an, z. b.:

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

Bei bestimmter Hardware generiert die Verwendung dieses Qualifizierers zusätzlichen Code, um die Richtigkeit (auch Thread übergreifend) zu erzwingen, jedoch geringfügige Leistungseinbußen. Wenn ein Index ohne diesen Qualifizierer geändert wird und innerhalb eines zeichnen/dispatchvorgangs die Ergebnisse nicht definiert sind.

## <a name="descriptor-arrays-and-texture-arrays"></a>Deskriptorarrays und Textur Arrays

Textur Arrays sind seit DirectX 10 verfügbar. Textur Arrays erfordern einen Deskriptor, aber alle Array Slices müssen das gleiche Format, Breite, Höhe und MIP-Anzahl aufweisen. Außerdem muss das Array einen zusammenhängenden Bereich im virtuellen Adressraum belegen. Der folgende Code zeigt ein Beispiel für den Zugriff auf ein Textur Array aus einem Shader.

``` syntax
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

In einem Textur Array kann der Index frei variieren, ohne dass Qualifizierer wie z. b `NonUniformResourceIndex` . erforderlich sind.

Das entsprechende deskriptorarray wäre wie folgt:

``` syntax
Texture2D<float4> myTex2DArray[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

Beachten Sie, dass die umständliche Verwendung eines float-Arrays für den Array Index durch ersetzt wird `myTex2D[2]` . Außerdem bieten deskriptorarrays mehr Flexibilität in Bezug auf die Dimensionen. Der-Typ, `Texture2D` ist dieses Beispiel, kann nicht variieren, aber das Format, die Breite, die Höhe und die MIP-Anzahl können bei jedem Deskriptor variieren.

Es ist legitim, ein deskriptorarray von Textur Arrays zu haben:

``` syntax
Texture2DArray<float4> myTex2DArrayOfArrays[2] : register(t0);
```

Es ist nicht legitim, ein Array von Strukturen zu deklarieren, jede Struktur mit Deskriptoren, z. b. der folgende Code wird nicht unterstützt.

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

Dies hätte das Speicher Layout **abcab.**.., aber eine sprach Einschränkung und wird nicht unterstützt. Eine unterstützte Methode hierfür wäre wie folgt, obwohl das Speicher Layout in diesem Fall **AAA ist... BBB... CCC...**

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

Um das Layout " **abcabcabc....** Memory" zu erreichen, verwenden Sie eine Deskriptortabelle, ohne die-Struktur zu verwenden `myStruct` .

## <a name="resource-aliasing"></a>Ressourcen Aliasing

Die in den HLSL-Shadern angegebenen Ressourcen Bereiche sind logische Bereiche. Sie werden zur Laufzeit über den Stamm Signatur Mechanismus an konkrete Heap Bereiche gebunden. Normalerweise wird ein logischer Bereich einem Heap Bereich zugeordnet, der sich nicht mit anderen Heap Bereichen überlappt. Der root Signature-Mechanismus ermöglicht jedoch das Alias (Überlappung) von Heap Bereichen kompatibler Typen. Beispielsweise `tex2` können und `tex3` Bereiche aus dem obigen Beispiel dem gleichen (oder überlappenden) Heap Bereich zugeordnet werden, der die Auswirkungen von Aliasing Texturen im HLSL-Programm hat. Wenn ein solches Alias gewünscht ist, muss der Shader mit der Option d3d10 \_ Shader \_ Resources \_ \_ Alias Alias kompiliert werden, die mithilfe der Option */Res \_ May \_ Alias* für das [Effekt-Compilertool](/windows/desktop/direct3dtools/fxc) (FXC) festgelegt wird. Die-Option bewirkt, dass der Compiler korrekten Code erzeugt, indem bestimmte Lade-/Speicheroptimierungen unter der Annahme vermieden werden, dass Ressourcen Alias sein dürfen.

## <a name="divergence-and-derivatives"></a>Abweichung und Ableitungen

SM 5.1 weist keine Einschränkungen für den Ressourcen Index auf. Das heißt, ` tex2[idx].Sample(…)` – der Index IDX kann eine Literalkonstante, eine cBuffer-Konstante oder ein interinterpolated-Wert sein. Obwohl das Programmiermodell eine sehr hohe Flexibilität bietet, müssen Probleme beachtet werden:

-   Wenn der Index über ein vierfache abweicht, sind die von der Hardware berechnete Ableitung und abgeleiteten Mengen wie Lod möglicherweise nicht definiert. Der HLSL-Compiler unternimmt den besten Aufwand, in diesem Fall eine Warnung auszugeben, verhindert jedoch nicht, dass ein Shader kompiliert wird. Dieses Verhalten ähnelt dem Berechnen von Ableitungen in einer abweichenden Ablauf Steuerung.
-   Wenn der Ressourcen Index abweicht, wird die Leistung im Vergleich zur Groß-/Kleinschreibung eines einheitlichen Indexes verringert, da die Hardware Vorgänge für mehrere Ressourcen ausführen muss. Ressourcen Indizes, die abweichen können, müssen mit der- `NonUniformResourceIndex` Funktion im HLSL-Code gekennzeichnet werden. Andernfalls sind die Ergebnisse nicht definiert.

## <a name="uavs-in-pixel-shaders"></a>UAVs in Pixel-Shadern

SM 5.1 erzwingt keine Einschränkungen für UAV-Bereiche in Pixel-Shadern, wie es bei SM 5.0 der Fall war.

## <a name="constant-buffers"></a>Konstantenpuffer

Die cBuffer-Syntax (SM 5.1 Constant Buffers) wurde von SM 5.0 geändert, damit Entwickler Konstante Puffer indizieren können. Um indizierbare Konstante Puffer zu aktivieren, führt SM 5.1 das `ConstantBuffer` "Template"-Konstrukt ein:

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

Der vorangehende Code deklariert die Konstante Puffer Variable `myCB1` vom Typ `Foo` und die Größe 6 und eine skalare Konstante Puffer Variable `myCB2` . Eine Konstante Puffer Variable kann nun wie folgt im Shader indiziert werden:

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

Die Felder "a" und "b" werden nicht zu globalen Variablen, sondern müssen als Felder behandelt werden. Aus Gründen der Abwärtskompatibilität unterstützt SM 5.1 das alte cBuffer-Konzept für skalare cbuffers. Mit der folgenden Anweisung werden "a" und "b" globale, schreibgeschützte Variablen als in SM 5.0 definiert. Ein solcher cBuffer im alten Stil kann jedoch nicht indizierbar sein.

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

Der Shader-Compiler unterstützt derzeit `ConstantBuffer` nur die Vorlage für benutzerdefinierte Strukturen.

Aus Kompatibilitätsgründen kann der HLSL-Compiler automatisch Ressourcen Register für in deklarierte Bereiche zuweisen `space0` . Wenn "Space" in der Register-Klausel weggelassen wird, wird der Standardwert `space0` verwendet. Der Compiler verwendet zum Zuweisen der Register die Heuristik zum Zuweisen der Registerkarte. Die Zuweisung kann über die reflektionsapi abgerufen werden, die erweitert wurde, um das Feld " *Space* " für Leerzeichen hinzuzufügen, während das Feld " *bindpoint* " die untere Grenze des Ressourcen Registrierungs Bereichs angibt.

## <a name="bytecode-changes-in-sm51"></a>Bytecode-Änderungen in SM 5.1

Mit SM 5.1 wird die Deklaration von Ressourcen Registern und die referenzierte Verwendung in Anweisungen geändert. Die Syntax umfasst das Deklarieren einer Register "Variablen", ähnlich wie bei Gruppen Shared Memory-Registern:

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

Dies wird Disassemblierung zu:

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim    ID   HLSL Bind     Count
// ------------------------------ ---------- ------- ----------- -----   --------- ---------
// samp0                             sampler      NA          NA     S0    a5            1
// tex0                              texture  float4          2d     T0    t5            1
// tex1[0][5][3]                     texture  float4          2d     T1   t10        unbounded
// tex2[8]                           texture  float4          2d     T2    t0.space1     8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots are used.
```

Jeder Shader-Ressourcenbereich verfügt jetzt über eine ID (Name), die für den Shader-Bytecode eindeutig ist. Beispielsweise wird das tex1 (T10)-Textur Array im Shader-Bytecode zu 't 1 '. Das Erteilen von eindeutigen IDs für jeden Ressourcenbereich ermöglicht zwei Dinge:

-   Identifizieren Sie eindeutig den Ressourcenbereich (siehe DCL \_ Resource \_ Texture2D), der in einer Anweisung indiziert wird (siehe Beispiel Anweisung).
-   Anfügen eines Satzes von Attributen an die Deklaration, z. b. Elementtyp, Stride-Größe, Raster Betriebsmodus usw.

Beachten Sie, dass die ID des Bereichs nicht mit der HLSL-Deklaration in der unteren Grenze verknüpft ist.

Die Reihenfolge der reflektionsressourcenbindungen (im oberen Bereich) und der Shader-Deklarations Anweisungen (DCL \_ \* ) sind die gleichen, die Sie beim Identifizieren der Entsprechung zwischen HLSL-Variablen und Bytecode-IDs unterstützen.

Jede Deklarations Anweisung in SM 5.1 verwendet einen 3D-Operanden, um Folgendes zu definieren: Range ID, Lower und Upper Bounds. Ein zusätzliches Token wird ausgegeben, um den Register Bereich anzugeben. Andere Token können ebenfalls ausgegeben werden, um zusätzliche Eigenschaften des Bereichs zu übermitteln, z. b. die cBuffer-Anweisung oder die strukturierte Puffer Deklarations Anweisung, die die Größe des cBuffer oder der Struktur ausgibt. Die genauen Codierungs Details finden Sie in d3d12TokenizedProgramFormat. h und **D3D10ShaderBinary:: cshadercodeparser**.

In den Anweisungen von SM 5.1 werden im Rahmen der Anweisung (wie in SM 5.0) keine zusätzlichen Ressourcen Operanden Informationen ausgegeben. Diese Informationen befinden sich nun in den Deklarations Anweisungen. In SM 5.0 erforderte das Indizieren von Ressourcen, dass Ressourcen Attribute in erweiterten Opcode-Token beschrieben werden müssen, da die Indizierung die Zuordnung zur Deklaration verdeckt hat. In SM 5.1 ist jede ID (z. b. 't 1 ') eindeutig einer einzelnen Deklaration zugeordnet, die die erforderlichen Ressourcen Informationen beschreibt. Daher werden die erweiterten Opcode-Token, die für Anweisungen zum Beschreiben von Ressourcen Informationen verwendet werden, nicht mehr ausgegeben.

In nicht Deklarations Anweisungen ist ein Ressourcen Operand für Samplers, Srvs und UAVs ein 2D-Operand. Der erste Index ist eine Literalkonstante, die die Bereichs-ID angibt. Der zweite Index stellt den linearisierten Wert des Indexes dar. Der Wert wird relativ zum Anfang des entsprechenden Register Bereichs (nicht relativ zum Anfang des logischen Bereichs) berechnet, um die Korrelation mit der Stamm Signatur zu verbessern und die Treiber-compilerlast für die Anpassung des Indexes zu verringern.

Ein Ressourcen Operand für cbvs ist ein 3D-Operand, der Folgendes enthält: literalid des Bereichs, Index des Konstanten Puffers, Offset in der jeweiligen Instanz des Konstanten Puffers.

## <a name="example-hlsl-declarations"></a>Beispiele für HLSL-Deklarationen

HLSL-Programme müssen nichts über Stamm Signaturen wissen. Sie können dem virtuellen "Register"-Bindungs Bereich (t \# für Srvs, u \# für UAVs, b \# für cbvs, s \# für Samplers) Bindungen zuweisen, oder Sie müssen sich auf den Compiler stützen, um Zuweisungen auszuwählen (und die resultierenden Zuordnungen mithilfe der Shader-Reflektion später abzufragen). Die Stamm Signatur ordnet deskriptortabellen, Stamm Deskriptoren und Stamm Konstanten diesem virtuellen Register Bereich zu.

Im folgenden sind einige Beispiel Deklarationen dargestellt, die ein HLSL-Shader aufweisen kann. Beachten Sie, dass es keine Verweise auf Stamm Signaturen oder deskriptortabellen gibt.

``` syntax
Texture2D foo[5] : register(t2);
Buffer bar : register(t7);
RWBuffer dataLog : register(u1);

Sampler samp : register(s0);

struct Data
{
    UINT index;
    float4 color;
};
ConstantBuffer<Data> myData : register(b0);

Texture2D terrain[] : register(t8); // Unbounded array
Texture2D misc[] : register(t0,space1); // Another unbounded array 
                                        // space1 avoids overlap with above t#

struct MoreData
{
    float4x4 xform;
};
ConstantBuffer<MoreData> myMoreData : register(b1);

struct Stuff
{
    float2 factor;
    UINT drawID;
};
ConstantBuffer<Stuff> myStuff[][3][8]  : register(b2, space3)
```

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Dynamische Indizierung mit HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[Effekt-Compilertool](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[HLSL-Shader-Modell 5,1 Features für Direct3D 12](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Geordnete Ansichten des Rasterizers](rasterizer-order-views.md)
</dt> <dt>

[Ressourcen Bindung](resource-binding.md)
</dt> <dt>

[Stamm Signaturen](root-signatures.md)
</dt> <dt>

[Shadermodell 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Von Shader angegebener Schablone-Verweis Wert](shader-specified-stencil-reference-value.md)
</dt> <dt>

[Angeben von Stamm Signaturen in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 