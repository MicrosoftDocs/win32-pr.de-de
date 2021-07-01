---
title: if-Anweisung
description: Führen Sie basierend auf der Auswertung des bedingten Ausdrucks eine Reihe von Anweisungen bedingt aus.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- if-Anweisung HLSL
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4a1f049526422f39c3529395481548943c7e84
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118955"
---
# <a name="if-statement"></a>if-Anweisung

Führen Sie basierend auf der Auswertung des bedingten Ausdrucks eine Reihe von Anweisungen bedingt aus.

\[*Attribut* \] if ( *Bedingt* ) { *Anweisungsblock*; }



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*
</dt> <dd>

Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Verzweigung</td>
<td>Werten Sie abhängig von der angegebenen Bedingung nur eine Seite der if-Anweisung aus.
<blockquote>
[!Note]<br />
Wenn Sie <a href="dx-graphics-hlsl-sm2.md">ShaderModell 2.x</a> oder <a href="dx-graphics-hlsl-sm3.md">Shadermodell 3.0</a>verwenden, nutzen Sie jedes Mal, wenn Sie dynamische Verzweigung verwenden, Ressourcen. Wenn Sie also die dynamische Verzweigung übermäßig verwenden, wenn Sie diese Profile als Ziel verwenden, können Kompilierungsfehler auftreten.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Vereinfachen</td>
<td>Werten Sie beide Seiten der if-Anweisung aus, und wählen Sie zwischen den beiden resultierenden Werten aus.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Bedingte*
</dt> <dd>

Ein bedingter [Ausdruck.](dx-graphics-hlsl-expressions.md) Der Ausdruck wird ausgewertet, und wenn true, wird der Anweisungsblock ausgeführt.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungsblock*
</dt> <dd>

Eine oder mehrere [HLSL-Anweisungen.](dx-graphics-hlsl-statement-blocks.md)

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn der Compiler die branch-Methode zum Kompilieren einer if-Anweisung verwendet, generiert er Code, der abhängig von der angegebenen Bedingung nur eine Seite der if-Anweisung auswertet. Beispiel: in der if-Anweisung:


```
[branch] if(x)
{
    x = sqrt(x);
}
```



Die **if-Anweisung** verfügt über einen impliziten else-Block, der x = x entspricht. Da wir dem Compiler mitgeteilt haben, die Branchmethode mit dem vorangehenden Branchattribut zu verwenden, wertet der kompilierte Code x aus und führt nur die Seite aus, die ausgeführt werden soll. Wenn x 0 (null) ist, wird die **else-Seite** ausgeführt, und wenn es ungleich 0 (null) ist, wird die **seite ausgeführt.**

Wenn dagegen das **vereinfachte** Attribut verwendet wird, wertet der kompilierte Code beide Seiten der **if-Anweisung** aus und wählt unter Verwendung des ursprünglichen Werts x zwischen den beiden resultierenden Werten aus. Hier sehen Sie ein Beispiel für die Verwendung des Flatten-Attributs:


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



Es gibt bestimmte Fälle, in denen die Verwendung des Branch- oder flatten-Attributs einen Kompilierungsfehler generieren kann. Das Branchattribut schlägt möglicherweise fehl, wenn eine Seite der if-Anweisung eine Farbverlaufsfunktion wie [**tex2D**](dx-graphics-hlsl-tex2d.md)enthält. Das Vereinfachungsattribut kann fehlschlagen, wenn eine Seite der if-Anweisung eine Stream Append-Anweisung oder eine andere Anweisung mit Nebeneffekten enthält.

Eine **if-Anweisung** kann auch einen optionalen else-Block verwenden. Wenn der **if-Ausdruck** TRUE ist, wird der Code im Anweisungsblock verarbeitet, der der if-Anweisung zugeordnet ist. Andernfalls wird der Anweisungsblock verarbeitet, der dem optionalen else-Block zugeordnet ist.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Flusssteuerung](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





