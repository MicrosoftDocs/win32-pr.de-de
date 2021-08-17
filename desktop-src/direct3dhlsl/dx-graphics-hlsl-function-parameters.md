---
title: Funktionsargumente
description: Eine Funktion verwendet mindestens ein Eingabeargument. Verwenden Sie die folgende Syntax, um jedes Argument zu deklarieren.
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7a2f2fdb656917ccf9dc57f06713fe01d77398d35776ac0c479b7d088281bc0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514763"
---
# <a name="function-arguments"></a>Funktionsargumente

Eine Funktion verwendet mindestens ein Eingabeargument. Verwenden Sie die folgende Syntax, um jedes Argument zu deklarieren.



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| **\[\]InputModifier-Typname: \[ Semantic \] \[ InterpolationModifier \] \[ = Initializers\]** |



 

\[Modifizierertypname \] : Semantic \[ : \] \[ Interpolationsmodifizierer = \] \[ Initialisierer\]

Wenn mehrere Funktionsargumente vorhanden sind, werden sie durch Kommas getrennt.

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
<td><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong><br/></td>
<td>Optionaler Begriff, der ein Argument als Eingabe, Ausgabe oder beides identifiziert.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Wert</td>
<td>Beschreibung</td>
</tr>
<tr class="even">
<td><strong>in</strong></td>
<td>Nur Eingabe</td>
</tr>
<tr class="odd">
<td><strong>Inout</strong></td>
<td>Eingabe und Ausgabe</td>
</tr>
<tr class="even">
<td><strong>out</strong></td>
<td>Nur Ausgabe</td>
</tr>
<tr class="odd">
<td><strong>uniform-Variable</strong></td>
<td>Eingabe nur konstanter Daten</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Parameter werden immer als Wert übergeben. in gibt an, dass der Wert des Parameters aus der aufrufenden Anwendung kopiert werden soll, bevor die Funktion beginnt. out gibt an, dass der letzte Wert des Parameters kopiert und an die aufrufende Anwendung zurückgegeben werden soll, wenn die Funktion zurückgegeben wird. inout ist eine Kurzform für die Angabe beider Angaben.</p>
<p>Ein einheitlicher Wert stammt aus einem konstanten Register. Jeder Aufruf von Vertex-Shadern oder Pixel-Shadern sieht den gleichen Anfangswert für eine einheitliche Variable. Globale Variablen werden so behandelt, als wären sie als einheitlich deklariert. Für Nicht-Funktionen der obersten Ebene ist uniform synonym mit <strong>in</strong>. Wenn keine Parameterverwendung angegeben wird, wird davon ausgegangen, dass sich die Parameterverwendung <strong>in befindet.</strong></p></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Typ</strong></p></td>
<td><p>Der Argumenttyp; kann ein beliebiger gültiger <a href="dx-graphics-hlsl-data-types.md">HLSL-Typ</a>sein.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Namen</strong></p></td>
<td><p>Eine ASCII-Zeichenfolge, die den Namen der Shaderfunktion eindeutig identifiziert.</p></td>
</tr>
<tr class="even">
<td><p><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semantische</strong></p></td>
<td><p>Optionale Zeichenfolge, die die beabsichtigte Verwendung der Daten angibt (siehe <a href="dx-graphics-hlsl-semantics.md">Semantik (DirectX HLSL)</a>).</p></td>
</tr>
<tr class="odd">
<td><p><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></p></td>
<td><p>Optionaler <a href="dx-graphics-hlsl-struct.md">Interpolationsmodifizierer,</a> der es einem Shader ermöglicht, die Interpolationsmethode zu bestimmen. Ein Interpolationsmodifizierer für ein Funktionsargument gilt nur für ein Argument, das als Eingabe für eine Pixelshaderfunktion verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Initialisierungen</strong></p></td>
<td><p>Optionale Werte für die Initialisierung; mehrere Werte sind erforderlich, um Datentypen mit mehreren Komponenten zu initialisieren.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Hinweise

Funktionsargumente werden in einer durch Kommas getrennten Argumentliste in einer Funktionsdeklaration aufgeführt. Wie bei C-Funktionen müssen für jedes Argument ein Parametername und ein Typ deklariert sein. Ein Argument für eine HLSL-Funktion kann optional eine Semantik, einen Anfangswert und eine Pixel-Shadereingabe einen Interpolationstyp enthalten.

Der *Typ* eines Funktionsarguments kann eine -Struktur sein, die einen Pro-Member-Interpolationsmodifizierer enthalten kann. Wenn das Funktionsargument auch über einen Interpolationsmodifizierer verfügt, überschreibt der Funktionsargumentmodifizierer Interpolationsmodifizierer, die innerhalb des Typs deklariert sind.

## <a name="examples"></a>Beispiele

Dieses Beispiel (aus dem [BasicHLSL10-Beispiel)](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)veranschaulicht einheitliche und nicht einheitliche Eingaben für eine Vertex-Shaderfunktion.


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



In diesem Beispiel (aus dem [ContentStreaming-Beispiel)](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)wird eine Eingabestruktur verwendet, um Argumente an eine Pixelshaderfunktion zu übergeben.


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

 

 





