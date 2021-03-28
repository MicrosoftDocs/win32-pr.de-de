---
title: Variablensyntax
description: Verwenden Sie die folgenden Syntax Regeln, um HLSL-Variablen zu deklarieren.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, Variable Syntax (DirectX HLSL)
- nointerpolations, Variablen Syntax (DirectX HLSL)
- Shared, Variable Syntax (DirectX HLSL)
- groupshared, Variablen Syntax (DirectX HLSL)
- static, Variable Syntax (DirectX HLSL)
- Uniform, Variable Syntax (DirectX HLSL)
- volatile, Variable Syntax (DirectX HLSL)
- genaue Variable Syntax (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6e63bafa62a9857af678e0848c81237dcd0d585
ms.sourcegitcommit: 4e0bde7dfa48a0b60bca4a5230eb2b05be3778d3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2020
ms.locfileid: "104993646"
---
# <a name="variable-syntax"></a>Variablensyntax

Verwenden Sie die folgenden Syntax Regeln, um HLSL-Variablen zu deklarieren.



|                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[*Speicher \_* \] \[ *Klassentyp \_ Modifizierer* \] *Typname* \[ *Index* \] \[ *: Semantik* \] \[ *: packoffset* \] \[ *: Register* \] ;    \[  \] Anmerkungen \[ *= Anfänglich \_ Wert*                    \] |



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Speicher \_ Klasse* 
</dt> <dd>

Optionale Speicherklassenmodifizierer, die dem Compiler Hinweise zum Gültigkeitsbereich und zur Lebensdauer von Variablen die modifiziererer können in beliebiger Reihenfolge angegeben werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>extern</strong></td>
<td>Markieren Sie eine globale Variable als externe Eingabe für den Shader. Dies ist die Standard Markierung für alle globalen Variablen. Kann nicht mit <strong>static</strong>kombiniert werden.</td>
</tr>
<tr class="even">
<td><strong>nointerpolations</strong></td>
<td>Interpolieren Sie die Ausgaben eines Vertex-Shaders nicht, bevor Sie Sie an einen PixelShader übergeben.</td>
</tr>
<tr class="odd">
<td><strong>sesten</strong></td>
<td>Wenn <strong>das Schlüsselwort</strong> für eine Variable angewendet wird, werden alle Berechnungen, die für die Erstellung des Werts der Variablen verwendet werden, auf folgende Weise eingeschränkt:

*   Separate Vorgänge werden getrennt beibehalten. Wenn beispielsweise eine mul und ein Hinzufügevorgang in einen Mad-Vorgang unterteilt worden wären, erzwingt <strong>präzise</strong> , dass die Vorgänge getrennt bleiben. Stattdessen müssen Sie die intrinsische Funktion "Mad" explizit verwenden.
*   Die Reihenfolge der Vorgänge wird beibehalten. Wenn die Reihenfolge der Anweisungen zum Verbessern der Leistung gemischt wurde, stellt <strong>präzise</strong> sicher, dass der Compiler die Bestellung wie geschrieben beibehält.
*   Unsichere IEEE-Vorgänge sind eingeschränkt. Wenn der Compiler möglicherweise schnelle mathematische Vorgänge verwendet hat, die keine Nan-(not a Number) und INF-Werte (unendlich) berücksichtigen, erzwingt <strong>präzise</strong> die IEEE-Anforderungen bezüglich der Nan-und INF-Werte, die beachtet werden müssen. Ohne <strong>genaue</strong>Sicherheit sind diese Optimierungen und mathematischen Vorgänge nicht IEEE-sicher.
*   Wenn Sie eine Variable <strong>genau</strong> qualifizieren, werden keine Vorgänge durchführt, die die Variable <strong>genau</strong>verwenden. Da die <strong>genaue</strong> Verteilung nur an Vorgänge durchführt, die zu den Werten beitragen, die der <strong>exakten</strong>qualifizierten Variablen zugewiesen sind, kann das korrekte Ausführen gewünschter Berechnungen knifflig sein. Daher empfiehlt <strong>es sich,</strong> die Shader-Ausgaben <strong>genau</strong> direkt zu markieren, wenn Sie Sie deklarieren, und zwar unabhängig davon, ob es sich um ein Strukturfeld oder einen Output-Parameter handelt.

Die Möglichkeit, Optimierungen auf diese Weise zu steuern, behält die Ergebnis Invarianz für die geänderte Ausgabevariable bei, indem Optimierungen deaktiviert werden, die die endgültigen Ergebnisse aufgrund von Unterschieden in kumulierten Genauigkeits unterschieden beeinflussen können. Es ist nützlich, wenn Shader für Mosaik Vorgänge Wasser strenge patchnähte oder Übereinstimmungs Werte über mehrere Durchgänge beibehalten möchten.

[Beispielcode](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl): 
```HLSL
matrix g_mWorldViewProjection;
void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position)
{
  // operation is precise because it contributes to the precise parameter OutPos
  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );
}
```
</td>
</tr>
<tr class="even">
<td><strong>Genu</strong></td>
<td>Markieren einer Variablen für die Freigabe zwischen Effekten Dies ist ein Hinweis für den Compiler.</td>
</tr>
<tr class="odd">
<td><strong>groupshared</strong></td>
<td>Markieren Sie eine Variable für den Thread Gruppen freigegebenen Arbeitsspeicher für Compute-Shader. In d3d10 ist die maximale Gesamtgröße aller Variablen mit der groupshared-Speicher Klasse 16 KB. in D3D11 beträgt die maximale Größe 32 KB. Siehe Beispiele.</td>
</tr>
<tr class="even">
<td><strong>static</strong></td>
<td>Markieren Sie eine lokale Variable, sodass Sie einmal initialisiert wird und zwischen Funktionsaufrufen besteht. Wenn die Deklaration keinen Initialisierer enthält, wird der Wert auf 0 (null) festgelegt. Eine globale Variable, die als <strong>statisch</strong> gekennzeichnet ist, ist für eine Anwendung nicht sichtbar.</td>
</tr>
<tr class="odd">
<td><strong>uniform-Variable</strong></td>
<td>Markieren einer Variablen, deren Daten während der Ausführung eines Shaders konstant sind (z. b. eine Material Farbe in einem Scheitelpunkt-Shader); globale Variablen werden standardmäßig als <strong>einheitlich</strong> betrachtet.</td>
</tr>
<tr class="even">
<td><strong>volatile</strong></td>
<td>Markieren einer Variablen, die häufig geändert wird; Dies ist ein Hinweis für den Compiler. Dieser Speicherklassenmodifizierer gilt nur für eine lokale Variable.<br/>
<blockquote>
[!Note]<br />
Der HLSL-Compiler ignoriert zurzeit diesen Speicherklassenmodifizierer.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*\_Typmodifizierer*
</dt> <dd>

Optionaler Modifizierer vom Typ "Variable".



| Wert             | BESCHREIBUNG                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const**         | Markieren Sie eine Variable, die nicht von einem Shader geändert werden kann. Daher muss Sie in der Variablen Deklaration initialisiert werden. Globale Variablen werden standardmäßig als **konstant** erachtet (unterdrücken Sie dieses Verhalten, indem Sie dem Compiler das/GEC-Flag bereitstellen). |
| **\_Hauptzeile**    | Markieren Sie eine Variable, die vier Komponenten in einer einzelnen Zeile speichert, sodass Sie in einem einzelnen Konstanten Register gespeichert werden können.                                                                                                                             |
| **\_Haupt Spalte** | Markieren Sie eine Variable, die vier Komponenten in einer einzelnen Spalte speichert, um die mathematische Matrix zu optimieren.                                                                                                                                                         |



 

> [!Note]  
> Wenn Sie keinen Typmodifiziererwert angeben, verwendet der Compiler die **Spalte \_ Major** als Standardwert.

 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Sorte*
</dt> <dd>

Jeder in den [Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)aufgeführte HLSL-Typ.

</dd> <dt>

<span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name* \[ *Index*\]
</dt> <dd>

Eine ASCII-Zeichenfolge, die eine Shader-Variable eindeutig identifiziert. Um ein optionales Array zu definieren, verwenden Sie den **Index** für die Array Größe, die eine positive Ganzzahl = 1 ist.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Tischer*
</dt> <dd>

Optionale Parameter Verwendungs Informationen, die vom Compiler verwendet werden, um shadereingaben und-Ausgaben zu verknüpfen. Es gibt mehrere vordefinierte [Semantik](dx-graphics-hlsl-semantics.md) für Scheitelpunkt-und Pixel-Shader. Der Compiler ignoriert Semantik, es sei denn, Sie sind für eine globale Variable deklariert, oder ein Parameter, der an einen Shader übergeben wird.

</dd> <dt>

<span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*
</dt> <dd>

Optionales Schlüsselwort zum manuellen Packen von shaderkonstanten. Siehe [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).

</dd> <dt>

<span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Sich*
</dt> <dd>

Optionales Schlüsselwort zum manuellen Zuweisen einer shadervariablen zu einem bestimmten Register. Weitere Informationen finden Sie unter [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).

</dd> <dt>

<span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Anmerkung (e)*
</dt> <dd>

Optionale Metadaten in Form einer Zeichenfolge, die an eine globale Variable angefügt sind. Eine Anmerkung wird vom Effect-Framework verwendet und von HLSL ignoriert. Ausführlichere Informationen finden Sie unter [Anmerkung-Syntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).

</dd> <dt>

<span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Anfangs \_ Wert*
</dt> <dd>

Optionaler Anfangswert (en); die Anzahl der Werte sollte mit der Anzahl der Komponenten im *Typ* identisch sein. Jede globale Variable, die als **extern** gekennzeichnet ist, muss mit einem Literalwert initialisiert werden. jede Variable, die als **statisch** gekennzeichnet ist, muss mit einer-Konstante initialisiert werden.

Globale Variablen, die nicht als **statisch** oder **extern** gekennzeichnet sind, werden nicht in den Shader kompiliert. Der Compiler legt die Standardwerte für globale Variablen nicht automatisch fest und kann nicht in Optimierungen verwendet werden. Um diesen Typ globaler Variablen zu initialisieren, verwenden Sie Reflektion, um den Wert zu erhalten, und kopieren Sie dann den Wert in einen konstanten Puffer. Beispielsweise können Sie die [**ID3D11ShaderReflection:: getvariablebyname**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) -Methode zum Aufrufen der Variablen verwenden, die [**ID3D11ShaderReflectionVariable:: getdesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) -Methode verwenden, um die Beschreibung der shadervariablen abzurufen, und den Anfangswert aus dem **DefaultValue** -Member der [**D3D11 \_ Shader- \_ Variablen \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) -Struktur erhalten. Um den Wert in den konstanten Puffer zu kopieren, müssen Sie sicherstellen, dass der Puffer mit CPU-Schreibzugriff ([**D3D11 \_ CPU \_ Access \_ Write**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)) erstellt wurde. Weitere Informationen zum Erstellen eines konstanten Puffers finden Sie unter Gewusst [wie: Erstellen eines konstanten Puffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).

Sie können auch das [Effects-Framework](../direct3d11/d3d11-graphics-programming-guide-effects.md) verwenden, um die Spiegelung automatisch zu verarbeiten und den Anfangswert festzulegen. Beispielsweise können Sie die [**ID3DX11EffectPass:: apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) -Methode verwenden.

</dd> </dl>

## <a name="examples"></a>Beispiele

Im folgenden finden Sie einige Beispiele für Shader-Variable-Deklarationen.


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a>Gruppe freigegeben

Mit HLSL können Threads eines Compute-Shaders Werte über gemeinsam genutzten Arbeitsspeicher austauschen. HLSL bietet Barriere, wie z. b. [**groupmemorybarrierwithgroupsync**](groupmemorybarrierwithgroupsync.md), usw., um die korrekte Reihenfolge von Lese-und Schreibvorgängen im Shader zu gewährleisten und Daten Rassen zu vermeiden.

> [!Note]  
> Hardware führt Threads in Gruppen (Warps oder Wave-Fronts) aus, und die Sperrungs Synchronisierung kann manchmal ausgelassen werden, um die Leistung zu erhöhen, wenn nur die Synchronisierung von Threads, die derselben Gruppe angehören, korrekt ist. Diese Auslassung wird jedoch aus folgenden Gründen dringend davon abgeraten:
>
> -   Diese Auslassung führt zu nicht portablen Code, der möglicherweise nicht auf Hardware funktioniert und auf Software-rasterizern, die in der Regel Threads in kleineren Gruppen ausführen, nicht funktioniert.
> -   Die Leistungsverbesserungen, die mit dieser Unterstreichung erzielt werden können, sind im Vergleich zur Verwendung der gesamten Thread Barriere geringfügig.

 

In Direct3D 10 gibt es beim Schreiben in **groupshared** keine Synchronisierung von Threads. Dies bedeutet, dass jeder Thread auf eine einzelne Position in einem Array zum Schreiben beschränkt ist. Verwenden Sie den System Wert [SV \_ groupIndex](dx-graphics-hlsl-semantics.md) , um beim Schreiben in dieses Array zu indizieren, um sicherzustellen, dass keine zwei Threads miteinander kollidieren können. Im Hinblick auf den Lesevorgang haben alle Threads Zugriff auf das gesamte Array zum Lesen.


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a>Verpacken

Pack-unter Komponenten von Vektoren und skalaren, deren Größe groß genug ist, um das Überschreiten von Register boundarys zu verhindern. Diese sind z. b. gültig:


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



Verpackungstypen können nicht gemischt werden.

Wie das Register Schlüsselwort kann ein packoffset als Ziel spezifisch festgelegt werden. Die unter Komponenten Verpackung ist nur mit dem packoffset-Schlüsselwort, nicht mit dem Register-Schlüsselwort verfügbar. Innerhalb einer cBuffer-Deklaration wird das Register-Schlüsselwort für Direct3D 10-Ziele ignoriert, da es für plattformübergreifende Kompatibilität angenommen wird.

Gepackte Elemente können sich überlappen, und der Compiler gibt keinen Fehler oder keine Warnung aus. In diesem Beispiel überlappen sich Element2 und Element3 mit Element1. x und Element1. y.


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



Ein Beispiel, in dem packoffset verwendet wird: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Variablen (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

