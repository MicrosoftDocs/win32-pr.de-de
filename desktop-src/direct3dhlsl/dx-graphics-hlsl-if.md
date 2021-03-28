---
title: if-Anweisung
description: Führen Sie bedingt eine Reihe von-Anweisungen basierend auf der Auswertung des bedingten Ausdrucks aus.
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
ms.openlocfilehash: 8e8a3c20e73b9783d39b4f4cbdb7c0be5b75fcda
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104038490"
---
# <a name="if-statement"></a>if-Anweisung

Führen Sie bedingt eine Reihe von-Anweisungen basierend auf der Auswertung des bedingten Ausdrucks aus.



|                                                               |
|---------------------------------------------------------------|
| \[*Attribut* \] if ( *Conditional* ) { *Statement Block*;} |



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Versehen*
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
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Verzweigung</td>
<td>Wertet nur eine Seite der if-Anweisung aus, abhängig von der angegebenen Bedingung.
<blockquote>
[!Note]<br />
Wenn Sie das <a href="dx-graphics-hlsl-sm2.md">Shadermodell 2. x</a> oder das <a href="dx-graphics-hlsl-sm3.md">Shader-Modell 3,0</a>verwenden, verwenden Sie jedes Mal, wenn Sie dynamische Verzweigungen verwenden, Ressourcen. Wenn Sie also die dynamische Verzweigung übermäßig verwenden, wenn Sie diese Profile als Ziel verwenden, können Sie Kompilierungsfehler erhalten.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Vereinfachen</td>
<td>Evaluieren Sie beide Seiten der if-Anweisung, und wählen Sie zwischen den beiden resultierenden Werten aus.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*
</dt> <dd>

Ein bedingter [Ausdruck](dx-graphics-hlsl-expressions.md). Der Ausdruck wird ausgewertet, und wenn true, wird der Anweisungsblock ausgeführt.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungs Block*
</dt> <dd>

Mindestens eine [HLSL-Anweisung](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn der Compiler die branchmethode zum Kompilieren einer if-Anweisung verwendet, wird Code generiert, der die Auswertung einer Seite der if-Anweisung abhängig von der angegebenen Bedingung durchführt. Beispielsweise in der if-Anweisung:


```
[branch] if(x)
{
    x = sqrt(x);
}
```



Die **if** -Anweisung verfügt über einen impliziten Else-Block, der x = x entspricht. Da der Compiler die branchmethode mit dem vorangehenden Verzweigungs Attribut verwendet hat, wertet der kompilierte Code x aus und führt nur die Seite aus, die ausgeführt werden soll. Wenn x 0 (null) ist, wird die **else** -Seite ausgeführt, und wenn Sie ungleich NULL ist, wird die Seite **dann** ausgeführt.

Wenn das **vereinfachen** -Attribut verwendet wird, wertet der kompilierte Code beide Seiten der **if** -Anweisung aus und wählt zwischen den beiden resultierenden Werten aus, wobei der ursprüngliche Wert von x verwendet wird. Im folgenden finden Sie ein Beispiel für die Verwendung des vereinfachen-Attributs:


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



Es gibt bestimmte Fälle, in denen die Verwendung der Verzweigungen oder der vereinfachen Attribute einen Kompilierungsfehler erzeugen kann. Das Branch-Attribut schlägt möglicherweise fehl, wenn eine Seite der if-Anweisung eine Farbverlaufs Funktion enthält, z. b. [**tex2D**](dx-graphics-hlsl-tex2d.md). Beim vereinfachen-Attribut tritt möglicherweise ein Fehler auf, wenn beide Seiten der if-Anweisung eine Stream anfügen-Anweisung oder eine andere Anweisung mit Nebeneffekten enthalten.

Eine **if** -Anweisung kann auch einen optionalen Else-Block verwenden. Wenn der **if** -Ausdruck true ist, wird der Code im Anweisungsblock verarbeitet, der der if-Anweisung zugeordnet ist. Andernfalls wird der dem optionalen Else-Block zugeordnete Anweisungsblock verarbeitet.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Fluss Steuerung](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





