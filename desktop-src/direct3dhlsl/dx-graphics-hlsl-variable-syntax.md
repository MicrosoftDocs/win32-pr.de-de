---
title: Variablensyntax
description: Verwenden Sie die folgenden Syntaxregeln, um HLSL-Variablen zu deklarieren.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, Variable Syntax (DirectX HLSL)
- nointerpolation, Variable Syntax (DirectX HLSL)
- shared, Variable Syntax (DirectX HLSL)
- groupshared, Variable Syntax (DirectX HLSL)
- static, Variable Syntax (DirectX HLSL)
- Uniform, Variable Syntax (DirectX HLSL)
- volatile, Variable Syntax (DirectX HLSL)
- precise, Variable Syntax (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 446444e09b0b6aff3e0ba8ca8b12cfbf6dc94128
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826068"
---
# <a name="variable-syntax"></a>Variablensyntax

Verwenden Sie die folgenden Syntaxregeln, um HLSL-Variablen zu deklarieren.

\[*Speicher \_* \] \[ *Typnamenindex \_ des* \] *Klassentypmodifizierers* \[  \] \[ *: Semantik* \] \[ *: Packoffset* \] \[ *: Register* \] ;    \[  \] Anmerkungen \[ *= Initial \_ Wert*                    \]



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*\_Storage-Klasse* 
</dt> <dd>

Optionale Speicherklassenmodifizierer, die dem Compiler Hinweise zum Variablenbereich und zur Lebensdauer geben; die Modifizierer können in beliebiger Reihenfolge angegeben werden.



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
<td>Markieren Sie eine globale Variable als externe Eingabe für den Shader. dies ist die Standardmarkierung für alle globalen Variablen. Kann nicht mit statischem <strong>kombiniert werden.</strong></td>
</tr>
<tr class="even">
<td><strong>nointerpolation</strong></td>
<td>Interpolieren Sie die Ausgaben eines Vertex-Shaders nicht, bevor Sie sie an einen Pixel-Shader übergeben.</td>
</tr>
<tr class="odd">
<td><strong>Präzise</strong></td>
<td>Das <strong>genaue</strong> Schlüsselwort, wenn es auf eine Variable angewendet wird, schränkt alle Berechnungen ein, die verwendet werden, um den dieser Variablen zugewiesenen Wert auf folgende Weise zu erzeugen:

*   Separate Vorgänge werden getrennt gehalten. Wenn z. B. ein mul- und add-Vorgang <strong></strong> in einen unsinnigen Vorgang verschlangen wurde, zwingt präzise die Vorgänge, getrennt zu bleiben. Stattdessen müssen Sie explizit die intrinsische Funktion "mad" verwenden.
*   Die Reihenfolge der Vorgänge wird beibehalten. Wenn die Reihenfolge der Anweisungen möglicherweise gemischt wurde, um die Leistung zu <strong>verbessern,</strong> stellt präzise sicher, dass der Compiler die Reihenfolge wie geschrieben beibwahrt.
*   Unsichere IEEE-Vorgänge sind eingeschränkt. Wenn der Compiler möglicherweise schnelle mathematische Operationen verwendet hat, die keine NaN-Werte (keine Zahl) und INF-Werte (unendlich) <strong>berücksichtigen,</strong> erzwingt präzise die Einhaltung von IEEE-Anforderungen in Bezug auf NaN- und INF-Werte. Ohne <strong>präzise</strong>sind diese Optimierungen und mathematischen Operationen nicht IEEE-sicher.
*   Wenn Sie eine Variable <strong>präzise qualifizieren,</strong> werden Vorgänge, die die Variable verwenden, nicht <strong>präzise.</strong> Da <strong></strong> präzise nur an Vorgänge weitergibt, die zu den <strong></strong>Werten beitragen, die der genau <strong></strong> qualifizierten Variablen zugewiesen sind, kann es schwierig <strong></strong> sein, die gewünschten Berechnungen richtig zu bestimmen. Daher wird empfohlen, die Shader-Ausgaben direkt dort zu markieren, wo Sie sie deklarieren, unabhängig davon, ob es sich um ein Strukturfeld, einen Ausgabeparameter oder den Rückgabetyp der Eingabefunktion handelt.

Die Möglichkeit, Optimierungen auf diese Weise zu steuern, behält die Ergebnisinvarianz für die geänderte Ausgabevariable bei, indem Optimierungen deaktiviert werden, die sich aufgrund von Unterschieden bei akkumulierten Genauigkeitsunterschieden auf Endergebnisse auswirken können. Dies ist hilfreich, wenn Shader für Mosaik die wasserdichten Patchnähte bzw. die Übereinstimmung von Tiefenwerten über mehrere Durchläufe hinweg verwenden möchten.

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
<td>Markieren Sie eine Variable für die Freigabe zwischen Effekten. dies ist ein Hinweis an den Compiler.</td>
</tr>
<tr class="odd">
<td><strong>groupshared</strong></td>
<td>Markieren Sie eine Variable für freigegebenen Threadgruppenspeicher für Compute-Shader. In D3D10 beträgt die maximale Gesamtgröße aller Variablen mit der groupshared-Speicherklasse 16 KB, in D3D11 beträgt die maximale Größe 32 KB. Siehe Beispiele.</td>
</tr>
<tr class="even">
<td><strong>static</strong></td>
<td>Markieren Sie eine lokale Variable so, dass sie einmal initialisiert wird und zwischen Funktionsaufrufen beibehalten wird. Wenn die Deklaration keinen Initialisierer enthält, wird der Wert auf 0 (null) festgelegt. Eine als statisch <strong>markierte globale Variable</strong> ist für eine Anwendung nicht sichtbar.</td>
</tr>
<tr class="odd">
<td><strong>uniform-Variable</strong></td>
<td>Markieren Sie eine Variable, deren Daten während der ausführung eines Shaders konstant sind (z. B. eine Materialfarbe in einem Vertex-Shader). globale Variablen werden standardmäßig <strong>als einheitlich</strong> betrachtet.</td>
</tr>
<tr class="even">
<td><strong>volatile</strong></td>
<td>Markieren Sie eine Variable, die sich häufig ändert. dies ist ein Hinweis an den Compiler. Dieser Speicherklassenmodifizierer gilt nur für eine lokale Variable.<br/>
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
| **const**         | Markieren Sie eine Variable, die nicht von einem Shader geändert werden kann. Daher muss sie in der Variablendeklaration initialisiert werden. Globale Variablen werden standardmäßig als **const** betrachtet (unterdrücken Sie dieses Verhalten, indem Sie das Flag /Gec an den Compiler übergeben). |
| **\_Zeilen-Hauptzeile**    | Markieren Sie eine Variable, die vier Komponenten in einer einzelnen Zeile speichert, damit sie in einem einzelnen konstanten Register gespeichert werden können.                                                                                                                             |
| **\_Spalten-Hauptspalte** | Markieren Sie eine Variable, die 4 Komponenten in einer einzelnen Spalte speichert, um die Matrixmatrizen zu optimieren.                                                                                                                                                         |



 

> [!Note]  
> Wenn Sie keinen Typmodifiziererwert angeben, verwendet der Compiler **die \_ Spalten-Hauptspalte** als Standardwert.

 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Typ*
</dt> <dd>

Alle HLSL-Typen, die unter [Datentypen (DirectX HLSL) aufgeführt sind.](dx-graphics-hlsl-data-types.md)

</dd> <dt>

<span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name* \[ *Index*\]
</dt> <dd>

ASCII-Zeichenfolge, die eine Shadervariable eindeutig identifiziert. Um ein optionales Array zu definieren, verwenden Sie **index** für die Arraygröße, bei der es sich um eine positive ganze Zahl = 1 handelt.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantische*
</dt> <dd>

Optionale Parameterverwendungsinformationen, die vom Compiler verwendet werden, um Shadereingaben und -ausgaben zu verknüpfen. Es gibt mehrere vordefinierte [Semantik für](dx-graphics-hlsl-semantics.md) Vertex- und Pixel-Shader. Der Compiler ignoriert die Semantik, es sei denn, sie werden für eine globale Variable deklariert oder ein Parameter, der an einen Shader übergeben wird.

</dd> <dt>

<span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*
</dt> <dd>

Optionales Schlüsselwort zum manuellen Packen von Shaderkonst constants. Weitere Informationen [finden Sie unter packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)

</dd> <dt>

<span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Registrieren*
</dt> <dd>

Optionales Schlüsselwort zum manuellen Zuweisen einer Shadervariablen zu einem bestimmten Register. Weitere [Informationen finden Sie unter register (DirectX HLSL).](dx-graphics-hlsl-variable-register.md)

</dd> <dt>

<span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Anmerkungen*
</dt> <dd>

Optionale Metadaten in Form einer Zeichenfolge, die an eine globale Variable angefügt sind. Eine Anmerkung wird vom Effektframework verwendet und von HLSL ignoriert. Eine ausführlichere Syntax finden Sie unter [Anmerkungssyntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).

</dd> <dt>

<span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*\_Anfangswert*
</dt> <dd>

Optionale Anfangswert(en); Die Anzahl der Werte sollte mit der Anzahl der Komponenten im Typ *übereinstimmen.* Jede globale Variable, die **als extern markiert** ist, muss mit einem Literalwert initialisiert werden. Jede als **statisch markierte** Variable muss mit einer Konstante initialisiert werden.

Globale Variablen, die nicht als **statisch oder** **extern** gekennzeichnet sind, werden nicht in den Shader kompiliert. Der Compiler setzt nicht automatisch Standardwerte für globale Variablen und kann sie nicht in Optimierungen verwenden. Um diesen Typ einer globalen Variablen zu initialisieren, verwenden Sie reflektion, um ihren Wert zu erhalten, und kopieren Sie den Wert dann in einen konstanten Puffer. Beispielsweise können Sie die [**ID3D11ShaderReflection::GetVariableByName-Methode**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) verwenden, um die Variable zu erhalten, die [**ID3D11ShaderReflectionVariable::GetDesc-Methode**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) verwenden, um die Beschreibung der Shadervariablen zu erhalten, und den Anfangswert aus dem **DefaultValue-Element** der [**D3D11 \_ SHADER \_ VARIABLE \_ DESC-Struktur**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) erhalten. Um den Wert in den Konstantenpuffer zu kopieren, müssen Sie sicherstellen, dass der Puffer mit CPU-Schreibzugriff [**(D3D11 \_ CPU \_ ACCESS \_ WRITE) erstellt wurde.**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag) Weitere Informationen zum Erstellen eines konstanten Puffers finden Sie unter [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).

Sie können auch das [Effektframework verwenden,](../direct3d11/d3d11-graphics-programming-guide-effects.md) um das reflektierende automatisch zu verarbeiten und den Anfangswert zu setzen. Beispielsweise können Sie die [**ID3DX11EffectPass::Apply-Methode**](/windows/desktop/direct3d11/id3dx11effectpass-apply) verwenden.

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

HLSL ermöglicht Threads eines Compute-Shaders den Austausch von Werten über freigegebenen Arbeitsspeicher. HLSL stellt Barriereprimitiven wie [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md)und so weiter zur Verfügung, um die richtige Reihenfolge von Lese- und Schreibvorgängen in freigegebenen Speicher im Shader sicherzustellen und Datenprobleme zu vermeiden.

> [!Note]  
> Die Hardware führt Threads in Gruppen aus (Warps oder Wellenfronten), und die Barrieresynchronisierung kann manchmal weggelassen werden, um die Leistung zu erhöhen, wenn nur die Synchronisierung von Threads, die derselben Gruppe angehören, korrekt ist. Wir raten jedoch dringend davon ab, diese Auslassung aus folgenden Gründen zu vermeiden:
>
> -   Diese Auslassung führt zu nicht portablem Code, der auf einigen Hardwarekomponenten möglicherweise nicht funktioniert und nicht für Softwarerasterizer funktioniert, die in der Regel Threads in kleineren Gruppen ausführen.
> -   Die Leistungsverbesserungen, die Sie mit dieser Auslassung erzielen können, sind im Vergleich zur Verwendung der Allthread-Barriere geringfügig.

 

In Direct3D 10 erfolgt beim Schreiben in **groupshared** keine Synchronisierung von Threads. Dies bedeutet, dass jeder Thread zum Schreiben auf einen einzelnen Speicherort in einem Array beschränkt ist. Verwenden Sie den [Systemwert SV \_ GroupIndex,](dx-graphics-hlsl-semantics.md) um beim Schreiben in dieses Array zu indizieren, um sicherzustellen, dass keine zwei Threads miteinander in Konflikt treten können. Im Hinblick auf das Lesen haben alle Threads Zugriff auf das gesamte Array zum Lesen.


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

Packen Sie Unterkomponenten von Vektoren und Skalaren, deren Größe groß genug ist, um das Überschreiten von Registergrenzen zu verhindern. Dies sind z. B. alle gültig:


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



Komprimierungstypen können nicht kombiniert werden.

Wie das Schlüsselwort register kann ein packoffset zielspezifisch sein. Das Packen von Unterkomponenten ist nur mit dem Schlüsselwort packoffset und nicht mit dem Schlüsselwort register verfügbar. Innerhalb einer cbuffer-Deklaration wird das Registerschlüsselwort für Direct3D 10-Ziele ignoriert, da es aus Gründen der plattformübergreifenden Kompatibilität angenommen wird.

Gepackte Elemente können sich überlappen, und der Compiler gibt keinen Fehler oder keine Warnung aus. In diesem Beispiel überlappen sich Element2 und Element3 mit Element1.x und Element1.y.


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



Ein Beispiel, das packoffset verwendet, [ist: HLSLWithoutFX10-Beispiel.](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Variablen (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

