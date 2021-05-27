---
title: Ressourcenbindung in HLSL
description: In diesem Thema werden einige spezifische Features der Verwendung des HLSL-Shadermodells 5.1 (High Level Shader Language) mit Direct3D 12 beschrieben.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 711ccdee71ff916445be68d03b84b7621aa04cf3
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550385"
---
# <a name="resource-binding-in-hlsl"></a>Ressourcenbindung in HLSL

In diesem Thema werden einige spezifische Features der Verwendung des [HLSL-Shadermodells 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) (High Level Shader Language) mit Direct3D 12 beschrieben. Alle Direct3D 12-Hardware unterstützt shader Model 5.1, sodass die Unterstützung für dieses Modell nicht von der Hardwarefeatureebene abhängig ist.

## <a name="resource-types-and-arrays"></a>Ressourcentypen und Arrays

Die Ressourcensyntax des Shaders Model 5 (SM5.0) verwendet das Schlüsselwort , um wichtige Informationen zur Ressource an den `register` HLSL-Compiler weiter zu übergeben. Die folgende Anweisung deklariert beispielsweise ein Array von vier Texturen, die an den Slots t3, t4, t5 und t6 gebunden sind. t3 ist der einzige Registerslot, der in der -Anweisung angezeigt wird und einfach der erste im Array von vier ist.

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

Die Ressourcensyntax des Shadermodells 5.1 (SM5.1) in HLSL basiert auf der vorhandenen Syntax für Registerressourcen, um eine einfachere Portierung zu ermöglichen. Direct3D 12-Ressourcen in HLSL sind an virtuelle Register innerhalb logischer Registerräume gebunden:

-   t – für Shaderressourcenansichten (SRV)
-   s – für Sampler
-   u – für ungeordnete Zugriffsansichten (UAV)
-   b – für konstante Pufferansichten (CBV)

Die Stammsignatur, die auf den Shader verweisen soll, muss mit den deklarierten Registerslots kompatibel sein. Beispielsweise wäre der folgende Teil einer Stammsignatur mit der Verwendung von Texturslots t3 bis t6 kompatibel, da er eine Deskriptortabelle mit den Slots t0 bis t98 beschreibt.

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

Eine Ressourcendeklaration kann ein Skalar, ein 1D-Array oder ein mehrdimensionales Array sein:

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

SM5.1 verwendet dieselben Ressourcentypen und Elementtypen wie SM5.0. SM5.1-Deklarationsgrenzwerte sind flexibler und nur durch die Laufzeit-/Hardwaregrenzwerte eingeschränkt. Das `space` Schlüsselwort gibt an, an welchen logischen Registerraum die deklarierte Variable gebunden ist. Wenn das `space` Schlüsselwort ausgelassen wird, wird der Standardspeicherplatzindex von 0 implizit dem Bereich zugewiesen (sodass sich der `tex2` obige Bereich in `space0` befindet). `register(t3,  space0)` tritt niemals ein Konflikt mit `register(t3,  space1)` oder einem Array in einem anderen Bereich auf, das t3 enthalten kann.

Eine Arrayressource kann eine unbegrenzte Größe aufweisen, die deklariert wird, indem die erste Dimension als leer angegeben wird, oder 0:

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

Die entsprechende Deskriptortabelle kann folgende sein:

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

Ein ungebundenes Array in HLSL entspricht einer festen Zahl, `numDescriptors` die mit in der Deskriptortabelle festgelegt ist, und eine feste Größe in der HLSL stimmt mit einer ungebundenen Deklaration in der Deskriptortabelle überein.

Mehrdimensionale Arrays sind zulässig, einschließlich einer unbegrenzten Größe. Diese mehrdimensionalen Arrays werden im Registerbereich flacher.

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

Das Aliasing von Ressourcenbereichen ist nicht zulässig. Anders ausgedrückt: Für jeden Ressourcentyp (t, s, u, b) dürfen deklarierte Registerbereiche nicht überlappen. Dies schließt auch nicht gebundene Bereiche ein. Bereiche, die in unterschiedlichen Registerräumen deklariert werden, überlappen sich nie. Beachten Sie, dass sich "unbounded" `tex2` (oben) in befindet, während sich `space0` "unbounded" `tex3` in `space1` befindet, sodass sie sich nicht überlappen.

Der Zugriff auf Ressourcen, die als Arrays deklariert wurden, ist so einfach wie das Indizieren.

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

Es gibt eine wichtige Standardeinschränkung für die Verwendung der Indizes ( `myMaterialID` und `samplerID` im obigen Code), da sie innerhalb einer [Welle](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology)nicht variieren dürfen. Selbst das Ändern des Indexes basierend auf der Instanziierung zählt als variierend.

Wenn der Index variieren muss, geben Sie den `NonUniformResourceIndex` Qualifizierer für den Index an, z. B.:

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

Bei einigen Hardwarekomponenten generiert die Verwendung dieses Qualifizierers zusätzlichen Code, um die Richtigkeit (einschließlich threadübergreifender) zu erzwingen, jedoch mit geringen Leistungskosten. Wenn ein Index ohne diesen Qualifizierer und innerhalb eines Zeichnens/Dispatchs geändert wird, sind die Ergebnisse nicht definiert.

## <a name="descriptor-arrays-and-texture-arrays"></a>Deskriptorarrays und Texturarrays

Texturarrays sind seit DirectX 10 verfügbar. Texturarrays erfordern einen Deskriptor, aber alle Arrayslices müssen das gleiche Format, die gleiche Breite, Höhe und MIP-Anzahl aufweisen. Außerdem muss das Array einen zusammenhängenden Bereich im virtuellen Adressraum belegen. Der folgende Code zeigt ein Beispiel für den Zugriff auf ein Texturarray über einen Shader.

``` syntax
Texture2DArray<float4> myTex2DArray : register(t0); // t0
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

In einem Texturarray kann der Index frei variiert werden, ohne dass Qualifizierer wie benötigt `NonUniformResourceIndex` werden.

Das entsprechende Deskriptorarray wäre:

``` syntax
Texture2D<float4> myArrayOfTex2D[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myArrayOfTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

Beachten Sie, dass die umwendliche Verwendung eines float für den Arrayindex durch ersetzt `myArrayOfTex2D[2]` wird. Auch Deskriptorarrays bieten mehr Flexibilität bei den Dimensionen. Der Typ , ist dieses Beispiel, kann nicht variieren, aber Format, Breite, Höhe und MIP-Anzahl können je nach `Texture2D` Deskriptor variieren.

Es ist legitim, über ein Deskriptorarray von Texturarrays zu verfügen:

``` syntax
Texture2DArray<float4> myArrayOfTex2DArrays[2] : register(t0);
```

Es ist nicht legitim, ein Array von -Strukturen zu deklarieren. Jede -Struktur, die Deskriptoren enthält, wird beispielsweise nicht unterstützt.

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

Dies hätte das Speicherlayout **abcabcabc....** zugelassen, ist jedoch eine Sprachbeschränkung und wird nicht unterstützt. Eine unterstützte Methode wäre die folgende, obwohl das Speicherlayout in diesem Fall **aaa ist... Bbb... ...**.

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

Um das **Speicherlayout abcabcabc....** zu erreichen, verwenden Sie eine Deskriptortabelle ohne Verwendung der `myStruct` -Struktur.

## <a name="resource-aliasing"></a>Ressourcenaliasing

Die in den HLSL-Shadern angegebenen Ressourcenbereiche sind logische Bereiche. Sie werden zur Laufzeit über den Stammsignaturmechanismus an konkrete Heapbereiche gebunden. Normalerweise wird ein logischer Bereich einem Heapbereich zuordnungen, der sich nicht mit anderen Heapbereichen überschneidet. Der Stammsignaturmechanismus ermöglicht es jedoch, Heapbereiche kompatibler Typen mit Aliasen (Überlappungen) zu überlappen. Beispielsweise können die Bereiche und aus dem obigen Beispiel dem gleichen (oder überlappenden) Heapbereich zugeordnet werden, was den Effekt hat, dass Texturen im `tex2` `tex3` HLSL-Programm aliasing werden. Wenn ein solches Aliasing gewünscht ist, muss der Shader mit der OPTION D3D10 SHADER RESOURCES MAY ALIAS kompiliert \_ \_ \_ \_ werden, die mit der Option */res \_ may \_ alias* für das [Effect-Compiler Tool](../direct3dtools/fxc.md) (FXC) festgelegt wird. Die Option bewirkt, dass der Compiler richtigen Code erzeugt, indem bestimmte Lade-/Speicheroptimierungen unter der Annahme verhindert werden, dass Ressourcen alias verwendet werden können.

## <a name="divergence-and-derivatives"></a>Abweichungen und Ableitungen

SM5.1 erzwingt keine Einschränkungen für den Ressourcenindex. Das heißt, ` tex2[idx].Sample(…)` der Index-IDX kann eine Literalkonstante, eine Cbufferkonstante oder ein interpolierter Wert sein. Das Programmiermodell bietet zwar so große Flexibilität, aber es gibt Probleme, die Sie beachten sollten:

-   Wenn der Index auf einem Quader abweicht, sind die hardwareerschlossene Ableitung und abgeleitete Mengen wie LOD möglicherweise nicht definiert. Der HLSL-Compiler versucht in diesem Fall, eine Warnung auszugeben, verhindert jedoch nicht die Kompilierung eines Shaders. Dieses Verhalten ähnelt dem Berechnen von Ableitungen bei der ablaufweisen Ablaufsteuerung.
-   Wenn der Ressourcenindex uneinheitlich ist, verringert sich die Leistung im Vergleich zum Fall eines einheitlichen Indexes, da die Hardware Vorgänge für mehrere Ressourcen ausführen muss. Ressourcenindizes, die möglicherweise unausweichlich sind, müssen mit der `NonUniformResourceIndex` -Funktion im HLSL-Code gekennzeichnet werden. Andernfalls sind Die Ergebnisse nicht definiert.

## <a name="uavs-in-pixel-shaders"></a>UAVs in Pixel-Shadern

SM5.1 erzwingt keine Einschränkungen für UAV-Bereiche in Pixel-Shadern, wie dies bei SM5.0 der Fall war.

## <a name="constant-buffers"></a>Konstantenpuffer

Die Syntax der SM5.1-Konstantenpuffer (cbuffer) wurde von SM5.0 geändert, um Entwicklern das Indizieren konstanter Puffer zu ermöglichen. Sm5.1 führt das Konstrukt "template" ein, um indizierbare Konstantenpuffer zu `ConstantBuffer` aktivieren:

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

Der vorangehende Code deklariert eine konstante Puffervariable `myCB1` vom Typ und der Größe `Foo` 6 sowie eine skalare konstante Puffervariable `myCB2` . Eine konstante Puffervariable kann jetzt im Shader wie die folgende indiziert werden:

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

Die Felder "a" und "b" werden nicht zu globalen Variablen, sondern müssen als Felder behandelt werden. Aus Gründen der Abwärtskompatibilität unterstützt SM5.1 das alte Cbufferkonzept für skalare Cbuffer. Die folgende Anweisung macht "a" und "b" zu globalen, schreibgeschützten Variablen wie in SM5.0. Ein solches Cbuffer im alten Stil kann jedoch nicht indiziert werden.

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

Derzeit unterstützt der Shadercompiler die `ConstantBuffer` Vorlage nur für benutzerdefinierte Strukturen.

Aus Kompatibilitätsgründen kann der HLSL-Compiler automatisch Ressourcenregister für Bereiche zuweisen, die in deklariert `space0` sind. Wenn "space" in der register-Klausel weggelassen wird, wird der `space0` Standardwert verwendet. Der Compiler verwendet die Heuristik first-fits, um die Register zu zuweisen. Die Zuweisung kann über die Reflektions-API abgerufen  werden, die erweitert wurde, um das Feld Space für den Raum hinzuzufügen, während das *BindPoint-Feld* die untere Grenze des Ressourcenregisterbereichs angibt.

## <a name="bytecode-changes-in-sm51"></a>Bytecodeänderungen in SM5.1

SM5.1 ändert, wie Ressourcenregister deklariert und in anweisungen referenziert werden. Die Syntax umfasst das Deklarieren einer Registervariablen, ähnlich wie bei Gruppen-Shared Memory-Registern:

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

Dadurch wird die Disassemblierung für:

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

Jeder Shaderressourcenbereich verfügt jetzt über eine ID (einen Namen), die für den Shader-Bytecode eindeutig ist. Beispielsweise wird das Texturarray tex1 (t10) im Shader-Bytecode zu "T1". Die Angabe eindeutiger IDs für jeden Ressourcenbereich ermöglicht zwei Dinge:

-   Identifizieren Sie eindeutig, welcher Ressourcenbereich (siehe dcl resource texture2d) in einer Anweisung indiziert wird \_ \_ (siehe Beispielanweisung).
-   Anfügen einer Gruppe von Attributen an die Deklaration, z. B. Elementtyp, Stridegröße, Rasterbetriebsmodus usw.

Beachten Sie, dass die ID des Bereichs nicht mit der HLSL-Untergrenze-Deklaration verknüpft ist.

Die Reihenfolge der Reflektionsressourcenbindungen (auflistung oben) und anweisungen für die Shaderdeklaration (dcl) ist identisch, um die Übereinstimmung zwischen \_ \* HLSL-Variablen und Bytecode-IDs zu identifizieren.

Jede Deklarationsanweisung in SM5.1 verwendet einen 3D-Operanden, um die Bereichs-ID, die untere und die obere Grenze zu definieren. Ein zusätzliches Token wird ausgegeben, um den Registerbereich anzugeben. Es können auch andere Token ausgegeben werden, um zusätzliche Eigenschaften des Bereichs zu vermitteln, z. B. gibt die Cbuffer- oder structured buffer declaration-Anweisung die Größe des Cbuffers oder der Struktur aus. Die genauen Details der Codierung finden Sie unter d3d12TokenizedProgramFormat.h und **D3D10ShaderBinary::CShaderCodeParser**.

SM5.1-Anweisungen geben keine zusätzlichen Ressourcenoperndeninformationen als Teil der Anweisung aus (wie in SM5.0). Diese Informationen sind jetzt in den Deklarationsanweisungen enthalten. In SM5.0 erforderten Anweisungen zum Indizieren von Ressourcen, dass Ressourcenattribute in erweiterten Opcodetoken beschrieben werden mussten, da die Indizierung die Zuordnung zur Deklaration verschleierte. In SM5.1 ist jede ID (z.B. "t1") eindeutig einer einzelnen Deklaration zugeordnet, die die erforderlichen Ressourceninformationen beschreibt. Daher werden die erweiterten Opcodetoken, die in Anweisungen zum Beschreiben von Ressourceninformationen verwendet werden, nicht mehr ausgegeben.

In Anweisungen ohne Deklaration ist ein Ressourcenopernd für Sampler, SRVs und UAVs ein 2D-Operand. Der erste Index ist eine Literalkonstante, die die Bereichs-ID angibt. Der zweite Index stellt den linearisierten Wert des Indexes dar. Der Wert wird relativ zum Anfang des entsprechenden Registerraums (nicht relativ zum Anfang des logischen Bereichs) berechnet, um eine bessere Korrelation mit der Stammsignatur zu erreichen und die Treibercompilerlast durch das Anpassen des Indexes zu reduzieren.

Ein Ressourcenopernd für CBVs ist ein 3D-Operand, der Folgendes enthält: Literal-ID des Bereichs, Index des Konstantenpuffers, Offset in die jeweilige Instanz des konstanten Puffers.

## <a name="example-hlsl-declarations"></a>HLSL-Beispieldeklarationen

HLSL-Programme müssen nichts über Stammsignaturen wissen. Sie können Bindungen dem virtuellen "Register"-Bindungsbereich zuweisen, t \# für SRVs, u \# für UAVs, b \# für CBVs, s \# für Sampler oder auf den Compiler, um Zuweisungen zu wählen (und anschließend die resultierenden Zuordnungen mithilfe von Shaderreflektion abzufragen). Die Stammsignatur ordnet Deskriptortabellen, Stammdeskriptoren und Stammkonstanten diesem virtuellen Registerbereich zu.

Im Folgenden finden Sie einige Beispieldeklarationen, die ein HLSL-Shader möglicherweise hat. Beachten Sie, dass es keine Verweise auf Stammsignaturen oder Deskriptortabellen gibt.

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

## <a name="related-topics"></a>Zugehörige Themen

* [Dynamische Indizierung mit HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
* [Effect-Compiler-Tool](../direct3dtools/fxc.md)
* [HLSL-Shadermodell 5.1-Features für Direct3D 12](../direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12.md)
* [Geordnete Rasterizeransichten](rasterizer-order-views.md)
* [Ressourcenbindung](resource-binding.md)
* [Stammsignaturen](root-signatures.md)
* [Shadermodell 5.1](../direct3dhlsl/shader-model-5-1.md)
* [Von Shader festgelegter Schablonenreferenzwert](shader-specified-stencil-reference-value.md)
* [Festlegen von Stammsignaturen in HLSL](specifying-root-signatures-in-hlsl.md)