---
title: Variablensyntax
description: Verwenden Sie die folgenden Syntaxregeln, um HLSL-Variablen zu deklarieren.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, Variablensyntax (DirectX HLSL)
- nointerpolation, Variable Syntax (DirectX HLSL)
- freigegebene Variablensyntax (DirectX HLSL)
- groupshared, Variable Syntax (DirectX HLSL)
- static, Variable Syntax (DirectX HLSL)
- uniform, Variable Syntax (DirectX HLSL)
- volatile, Variable Syntax (DirectX HLSL)
- präzise Variable Syntax (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f81868e289fd2914da20e33ccc373ba9bd7df43bfb4bd123a2dcfa88fdb452ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744750"
---
# <a name="variable-syntax"></a>Variablensyntax

Verwenden Sie die folgenden Syntaxregeln, um HLSL-Variablen zu deklarieren.

\[*Storage \_ Type* \] \[ *\_ Modifier* \] *Type Name* \[ *Index* der \] \[ *Klasse: Semantic*: \] \[ *Packoffset*: \] \[ *Register* \] ;    \[  \] Anmerkungen \[ *= Initial \_ Wert*                    \]



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*\_Storage Klasse* 
</dt> <dd>

Optionale Speicherklassenmodifizierer, die dem Compiler Hinweise zum Variablenbereich und zur Lebensdauer geben; Die Modifizierer können in beliebiger Reihenfolge angegeben werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>extern</strong></td>
<td>Markieren sie eine globale Variable als externe Eingabe für den Shader. Dies ist die Standardmarkierung für alle globalen Variablen. Kann nicht mit <strong>statischem</strong>kombiniert werden.</td>
</tr>
<tr class="even">
<td><strong>Nointerpolation</strong></td>
<td>Interpolieren Sie die Ausgaben eines Vertex-Shaders nicht, bevor Sie sie an einen Pixel-Shader übergeben.</td>
</tr>
<tr class="odd">
<td><strong>Präzise</strong></td>
<td>Das <strong>genaue</strong> Schlüsselwort, wenn es auf eine Variable angewendet wird, schränkt alle Berechnungen ein, die verwendet werden, um den Wert zu erzeugen, der dieser Variablen zugewiesen ist, auf folgende Weise:

*   Separate Vorgänge werden getrennt gehalten. Wenn z. B. ein Mul- und Add-Vorgang möglicherweise in einen wilden Vorgang integriert wurde, erzwingt <strong>präzise,</strong> dass die Vorgänge getrennt bleiben. Stattdessen müssen Sie explizit die intrinsische Funktion "toll" verwenden.
*   Die Reihenfolge der Vorgänge wird beibehalten. Wenn die Reihenfolge der Anweisungen möglicherweise gemischt wurde, um die Leistung zu verbessern, stellt <strong>präzise</strong> sicher, dass der Compiler die Reihenfolge beim Schreiben bei behält.
*   UNSICHERE IEEE-Vorgänge sind eingeschränkt. Wenn der Compiler möglicherweise schnelle mathematische Operationen verwendet hat, die keine NaN- (keine Zahl) und INF-Werte (unendlich) berücksichtigen, erzwingt <strong>die genaue</strong> Einhaltung von IEEE-Anforderungen in Bezug auf NaN- und INF-Werte. Ohne <strong>präzise</strong>sind diese Optimierungen und mathematischen Operationen nicht IEEE-sicher.
*   Das Qualifizieren einer <strong>Variablen präzise</strong> macht keine Vorgänge, die die Variable <strong>präzise</strong>verwenden. Da <strong>präzise</strong> nur an Vorgänge weitergegeben wird, die zu den Werten beitragen, die der <strong>präzisen</strong>-qualified-Variablen zugewiesen sind, <strong>kann</strong> es schwierig sein, die gewünschten Berechnungen korrekt präzise zu machen. Daher wird empfohlen, die Shaderausgaben <strong>direkt</strong> an der Stelle zu markieren, an der Sie sie deklarieren, unabhängig davon, ob sich dies in einem Strukturfeld oder in einem Ausgabeparameter oder dem Rückgabetyp der Eingabefunktion ergibt.

Die Möglichkeit, Optimierungen auf diese Weise zu steuern, behält die Ergebnisinvarianz für die geänderte Ausgabevariable bei, indem Optimierungen deaktiviert werden, die sich aufgrund von Unterschieden bei der akkumulierten Genauigkeit auf die Endergebnisse auswirken können. Dies ist hilfreich, wenn Shader für das Mosaik wasserdichte Patchn nahthalten oder Tiefenwerte über mehrere Durchläufe abgleichen sollen.

[Beispielcode:](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl) 
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
<td><strong>geteilt</strong></td>
<td>Markieren sie eine Variable für die Gemeinsame Nutzung zwischen Effekten. Dies ist ein Hinweis für den Compiler.</td>
</tr>
<tr class="odd">
<td><strong>groupshared</strong></td>
<td>Markieren Sie eine Variable für thread-group-shared memory für Compute-Shader. In D3D10 beträgt die maximale Gesamtgröße aller Variablen mit der groupshared-Speicherklasse 16 KB, in D3D11 beträgt die maximale Größe 32 KB. Weitere Informationen finden Sie unter Beispiele.</td>
</tr>
<tr class="even">
<td><strong>static</strong></td>
<td>Markieren Sie eine lokale Variable so, dass sie einmal initialisiert wird und zwischen Funktionsaufrufen beibehalten wird. Wenn die Deklaration keinen Initialisierer enthält, wird der Wert auf 0 (null) festgelegt. Eine als <strong>statisch</strong> markierte globale Variable ist für eine Anwendung nicht sichtbar.</td>
</tr>
<tr class="odd">
<td><strong>uniform-Variable</strong></td>
<td>Markieren sie eine Variable, deren Daten während der Ausführung eines Shaders konstant sind (z. B. eine Materialfarbe in einem Scheitelpunkt-Shader). globale Variablen werden standardmäßig als <strong>einheitlich</strong> betrachtet.</td>
</tr>
<tr class="even">
<td><strong>volatile</strong></td>
<td>Markieren sie eine Variable, die sich häufig ändert. Dies ist ein Hinweis für den Compiler. Dieser Speicherklassenmodifizierer gilt nur für eine lokale Variable.<br/>
<blockquote>
[!Note]<br />
Der HLSL-Compiler ignoriert diesen Speicherklassenmodifizierer derzeit.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*\_Typmodifizierer*
</dt> <dd>

Optionaler Variablentypmodifizierer.



| Wert             | Beschreibung                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const**         | Markieren Sie eine Variable, die nicht von einem Shader geändert werden kann. Daher muss sie in der Variablendeklaration initialisiert werden. Globale Variablen werden standardmäßig als **const** betrachtet (unterdrücken Sie dieses Verhalten, indem Sie dem Compiler das /Gec-Flag bereitstellen). |
| **\_Zeilen-Hauptversion**    | Markieren Sie eine Variable, die vier Komponenten in einer einzelnen Zeile speichert, sodass sie in einem einzigen Konstantenregister gespeichert werden können.                                                                                                                             |
| **\_Spaltenhauptspalte** | Markieren Sie eine Variable, die 4 Komponenten in einer einzelnen Spalte speichert, um die Matrixberechnung zu optimieren.                                                                                                                                                         |



 

> [!Note]  
> Wenn Sie keinen Typmodifiziererwert angeben, verwendet der Compiler **\_ spaltenhaupt** als Standardwert.

 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Typ*
</dt> <dd>

Alle HLSL-Typen, die unter [Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)aufgeführt sind.

</dd> <dt>

<span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name* \[ *Index*\]
</dt> <dd>

ASCII-Zeichenfolge, die eine Shadervariable eindeutig identifiziert. Um ein optionales Array zu definieren, verwenden Sie **den Index** für die Arraygröße, die eine positive ganze Zahl = 1 ist.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantische*
</dt> <dd>

Optionale Parameterverwendungsinformationen, die vom Compiler zum Verknüpfen von Shadereingaben und -ausgaben verwendet werden. Es gibt mehrere vordefinierte [Semantik](dx-graphics-hlsl-semantics.md) für Vertex- und Pixel-Shader. Der Compiler ignoriert die Semantik, es sei denn, sie werden für eine globale Variable oder einen Parameter deklariert, der an einen Shader übergeben wird.

</dd> <dt>

<span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*
</dt> <dd>

Optionales Schlüsselwort zum manuellen Packen von Shaderkonstanten. Siehe [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).

</dd> <dt>

<span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Registrieren*
</dt> <dd>

Optionales Schlüsselwort zum manuellen Zuweisen einer Shadervariable zu einem bestimmten Register. Siehe [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).

</dd> <dt>

<span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Anmerkungen*
</dt> <dd>

Optionale Metadaten in Form einer Zeichenfolge, die an eine globale Variable angefügt sind. Eine Anmerkung wird vom Effektframework verwendet und von HLSL ignoriert. Eine ausführlichere Syntax finden Sie unter [Anmerkungssyntax.](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax)

</dd> <dt>

<span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*\_Anfangswert*
</dt> <dd>

Optionale Anfangswerte; Die Anzahl der Werte sollte mit der Anzahl der Komponenten in *Typ* übereinstimmen. Jede globale Variable, die **als extern** markiert ist, muss mit einem Literalwert initialisiert werden. Jede variable, **die als statisch** markiert ist, muss mit einer Konstante initialisiert werden.

Globale Variablen, die nicht als **statisch** oder **extern** gekennzeichnet sind, werden nicht in den Shader kompiliert. Der Compiler legt nicht automatisch Standardwerte für globale Variablen fest und kann sie nicht in Optimierungen verwenden. Um diesen Typ von globaler Variable zu initialisieren, verwenden Sie Reflektion, um ihren Wert abzurufen, und kopieren Sie den Wert dann in einen konstanten Puffer. Beispielsweise können Sie die [**ID3D11ShaderReflection::GetVariableByName-Methode**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) verwenden, um die Variable abzurufen, die [**ID3D11ShaderReflectionVariable::GetDesc-Methode**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) verwenden, um die Shadervariablenbeschreibung abzurufen, und den Anfangswert aus dem **DefaultValue-Member** der [**D3D11 \_ SHADER \_ VARIABLE \_ DESC-Struktur**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) abrufen. Um den Wert in den konstanten Puffer zu kopieren, müssen Sie sicherstellen, dass der Puffer mit CPU-Schreibzugriff erstellt wurde ([**D3D11 \_ CPU \_ ACCESS \_ WRITE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)). Weitere Informationen zum Erstellen eines Konstantenpuffers finden Sie unter [Vorgehensweise: Erstellen eines Konstantenpuffers.](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)

Sie können auch das [Effektframework](../direct3d11/d3d11-graphics-programming-guide-effects.md) verwenden, um die reflektion automatisch zu verarbeiten und den Anfangswert festzulegen. Beispielsweise können Sie die [**ID3DX11EffectPass::Apply-Methode**](/windows/desktop/direct3d11/id3dx11effectpass-apply) verwenden.

</dd> </dl>

## <a name="examples"></a>Beispiele

Im Folgenden finden Sie einige Beispiele für Shadervariablendeklarationen.


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



### <a name="group-shared"></a>Freigegebene Gruppe

HLSL ermöglicht Threads eines Compute-Shaders den Austausch von Werten über freigegebenen Arbeitsspeicher. HLSL stellt Barriereprimitiven wie [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md)usw. bereit, um die richtige Reihenfolge von Lese- und Schreibvorgängen im freigegebenen Speicher im Shader sicherzustellen und Datenschwund zu vermeiden.

> [!Note]  
> Hardware führt Threads in Gruppen aus (Warps oder Wellenfronten), und die Barrieresynchronisierung kann manchmal weggelassen werden, um die Leistung zu erhöhen, wenn nur die Synchronisierung von Threads, die zur gleichen Gruppe gehören, korrekt ist. Aus folgenden Gründen raten wir jedoch dringend von dieser Auslassung ab:
>
> -   Diese Auslassung führt zu nicht portierbaren Code, der möglicherweise auf einigen Hardwarekomponenten nicht funktioniert und nicht auf Softwarerasterizern funktioniert, die in der Regel Threads in kleineren Gruppen ausführen.
> -   Die Leistungsverbesserungen, die Sie mit dieser Auslassung erzielen können, sind im Vergleich zur Verwendung der Allthreadbarriere geringfügig.

 

In Direct3D 10 gibt es keine Synchronisierung von Threads beim Schreiben in **groupshared.** Dies bedeutet, dass jeder Thread zum Schreiben auf einen einzelnen Speicherort in einem Array beschränkt ist. Verwenden Sie den [SV \_ GroupIndex-Systemwert,](dx-graphics-hlsl-semantics.md) um beim Schreiben in dieses Array zu indizieren, um sicherzustellen, dass keine zwei Threads kollidieren können. Beim Lesen haben alle Threads Zugriff auf das gesamte Array zum Lesen.


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



### <a name="packing"></a>Verpackung

Packen Sie Unterkomponenten von Vektoren und Skalaren, deren Größe groß genug ist, um das Überschreiten von Registerbegrenzungen zu verhindern. Dies sind beispielsweise alle gültig:


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



Packtypen können nicht gemischt werden.

Genau wie das register-Schlüsselwort kann ein packoffset zielspezifisch sein. Das Packen von Unterkomponenten ist nur mit dem Schlüsselwort packoffset und nicht mit dem Registerschlüsselwort verfügbar. Innerhalb einer cbuffer-Deklaration wird das Register-Schlüsselwort für Direct3D 10-Ziele ignoriert, da es aus Plattform-übergreifender Kompatibilität angenommen wird.

Gepackte Elemente können sich überlappen, und der Compiler gibt keinen Fehler oder keine Warnung aus. In diesem Beispiel überschneiden sich Element2 und Element3 mit Element1.x und Element1.y.


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



Ein Beispiel, das packoffset verwendet, [ist: HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Variablen (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

