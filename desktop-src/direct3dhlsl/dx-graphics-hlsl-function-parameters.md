---
title: Funktionsargumente
description: Eine Funktion nimmt mindestens ein Eingabe Argument an. Verwenden Sie die folgende Syntax, um jedes Argument zu deklarieren.
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ba35ad04b20b67e45550644e842d69209ca5088
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389797"
---
# <a name="function-arguments"></a>Funktionsargumente

Eine Funktion nimmt mindestens ein Eingabe Argument an. Verwenden Sie die folgende Syntax, um jedes Argument zu deklarieren.



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| **\[Typname des inputmodifiers \] \[ : Semantic \] \[ interpolationmodifier \] \[ = Initialisierer\]** |



 

\[\]Modifizierertypname \[ : Semantic \] \[ : Interpolations Modifizierer \] \[ = Initialisierer (s)\]

Wenn mehrere Funktionsargumente vorhanden sind, werden diese durch Kommas getrennt.

## <a name="parameters"></a>Parameter



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>Input-Modifizierer</strong><br/></td>
<td>Optionaler Begriff, der ein Argument als Eingabe, Ausgabe oder beides bezeichnet.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Wert</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td><strong>in</strong></td>
<td>Nur Eingabe</td>
</tr>
<tr class="odd">
<td><strong>INOUT</strong></td>
<td>Eingabe und Ausgabe</td>
</tr>
<tr class="even">
<td><strong>out</strong></td>
<td>Nur Ausgabe</td>
</tr>
<tr class="odd">
<td><strong>uniform-Variable</strong></td>
<td>Nur konstante Daten eingeben</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Parameter werden immer als Wert übermittelt. in gibt an, dass der Wert des-Parameters aus der aufrufenden Anwendung kopiert werden soll, bevor die-Funktion beginnt. out gibt an, dass der letzte Wert des-Parameters kopiert und an die aufrufende Anwendung zurückgegeben werden soll, wenn die Funktion zurückgibt. "INOUT" ist eine Kurzzeit zum Angeben von beidem.</p>
<p>Ein einheitlicher Wert stammt aus einem konstanten Register. jeder Scheitelpunkt-Shader oder Pixel-Shader-Aufruf hat denselben Anfangswert für eine einheitliche Variable. Globale Variablen werden so behandelt, als wären Sie als einheitlich deklariert. Bei Funktionen, die nicht auf oberster Ebene stehen, ist Uniform gleichbedeutend mit <strong>in</strong>. Wenn keine Parameter Verwendung angegeben ist, wird davon ausgegangen, dass die Parameter Verwendung <strong>in</strong>erfolgt.</p></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Sorte</strong></p></td>
<td><p>Der Argumenttyp. kann ein beliebiger gültiger HLSL- <a href="dx-graphics-hlsl-data-types.md">Typ</a>sein.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Benennen</strong></p></td>
<td><p>Eine ASCII-Zeichenfolge, die den Namen der Shader-Funktion eindeutig identifiziert.</p></td>
</tr>
<tr class="even">
<td><p><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Tischer</strong></p></td>
<td><p>Optionale Zeichenfolge, die die beabsichtigte Verwendung der Daten identifiziert (siehe <a href="dx-graphics-hlsl-semantics.md">Semantik (DirectX HLSL)</a>).</p></td>
</tr>
<tr class="odd">
<td><p><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>Interpolationmodifier</strong></p></td>
<td><p>Optionaler <a href="dx-graphics-hlsl-struct.md">Interpolations Modifizierer</a> , der es einem Shader ermöglicht, die Interpolationsmethode zu bestimmen. Ein Interpolations Modifizierer für ein Funktions Argument gilt nur für ein Argument, das als Eingabe für eine pixelshaderfunktion verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Initialisierer</strong></p></td>
<td><p>Optionale Werte für die Initialisierung. zum Initialisieren von Datentypen mit mehreren Komponenten sind mehrere Werte erforderlich.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Funktionsargumente werden in einer durch Trennzeichen getrennten Argumentliste in einer Funktionsdeklaration aufgelistet. Wie bei C-Funktionen muss jedes Argument einen Parameternamen und einen Typ deklarieren. ein Argument für eine HLSL-Funktion kann optional eine Semantik, einen Anfangswert und eine Pixel-Shadereingabe enthalten, die einen Interpolationstyp enthalten können.

Der *Typ* eines Funktionsarguments könnte eine Struktur sein, die einen Interpolations Modifizierer pro Member enthalten könnte. Wenn das Funktions Argument auch einen Interpolations Modifizierer aufweist, überschreibt der funktionsargumentmodifizierer Interpolations Modifizierer, die innerhalb des Typs deklariert werden.

## <a name="examples"></a>Beispiele

In diesem Beispiel (aus dem [BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)-Beispiel) werden einheitliche und nicht einheitliche Eingaben für eine Vertex-Shader-Funktion veranschaulicht.


```
VS_OUTPUT RenderSceneVS( 
  float4 vPos : POSITION,
  float3 vNormal : NORMAL,
  float2 vTexCoord0 : TEXCOORD,
  uniform int nNumLights,
  uniform bool bTexture,
  uniform bool bAnimate )
{
  ...
}
```



In diesem Beispiel (aus dem [contentstreaming-Beispiel](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) wird eine Eingabe Struktur verwendet, um Argumente an eine Pixel-Shader-Funktion zu übergeben.


```
VSBasicIn input
struct VSBasicIn
{
  float4 Pos    : POSITION;
  float3 Norm   : NORMAL;
  float2 Tex    : TEXCOORD0;
};

PSBasicIn VSBasic(VSBasicIn input)
{
  ...
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Funktionen (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





