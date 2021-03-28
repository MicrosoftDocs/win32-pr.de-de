---
title: for-Anweisung
description: Führt iterativ eine Reihe von-Anweisungen basierend auf der Auswertung des bedingten Ausdrucks aus.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- für Anweisungs-HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50f8c18ebc23455563b4b3e6bfee72bfa9d3ec4c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100890"
---
# <a name="for-statement"></a>for-Anweisung

Führt iterativ eine Reihe von-Anweisungen basierend auf der Auswertung des bedingten Ausdrucks aus.



|                                                                                       |
|---------------------------------------------------------------------------------------|
| \[*Attribut* \] for ( *Initialisierer; Conditional Iterator* ) { *Anweisungs Block*;} |



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Versehen*
</dt> <dd>

Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird. Wenn kein Attribut angegeben wird, versucht der Compiler zunächst, eine gerollerte Version der Schleife auszugeben. wenn dies nicht der Fall ist, oder wenn bei der Ausführung der Schleife ein Fehler auftritt, wird auf eine nicht rollende Version der Schleife zurückgegriffen.



| attribute             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aufheben der Registrierung (x)             | Entsperren Sie die Schleife, bis die Ausführung beendet ist. Optional können Sie angeben, wie oft die Schleife maximal ausgeführt werden soll. Nicht kompatibel mit dem **\[ Schleifen \]** Attribut.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| loop                  | Generieren Sie Code, der die Fluss Steuerung verwendet, um jede Iterations Schleife auszuführen. Nicht kompatibel mit dem Attribut " **\[ Auflösen \]** ".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| fastopt               | Verringert die Kompilierzeit, erzeugt jedoch weniger aggressive Optimierungen. Wenn Sie dieses Attribut verwenden, entlädt der Compiler keine Schleifen.<br/> Dieses Attribut wirkt sich nur auf shadermodellziele aus, die [unterbrechungsanweisungen](dx-graphics-hlsl-break.md) unterstützen Dieses Attribut ist im Shader-Modell [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [Shader Model 3](dx-graphics-hlsl-sm3.md) und höher verfügbar. Dies ist besonders nützlich, [](dx-graphics-hlsl-sm4.md) wenn der Compiler Schleifen kompiliert. Der Compiler simuliert standardmäßig Schleifen, um auszuwerten, ob er die Registrierung aufheben kann. Verwenden Sie dieses Attribut, um die Kompilierzeit zu verkürzen, wenn der Compiler keine Schleifen aufheben soll. <br/> |
| \_UAV- \_ Bedingung zulassen | Ermöglicht, dass die Beendigungs Bedingung einer COMPUTE-Shader-Schleife auf einem UAV-Lesevorgang basiert. Die Schleife darf keine systeminternen Synchronisierungs Funktionen enthalten.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initialisierer*
</dt> <dd>

Der Anfangswert des Schleifenzählers.

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*
</dt> <dd>

Ein bedingter [Ausdruck](dx-graphics-hlsl-expressions.md). Wenn für den bedingten Ausdruck true ausgewertet wird, wird der Anweisungsblock ausgeführt. Die Schleife endet, wenn der Ausdruck zu false ausgewertet wird.

</dd> <dt>

<span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*
</dt> <dd>

Aktualisieren Sie den Wert des Schleifen Zählers.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungs Block*
</dt> <dd>

Mindestens eine [HLSL-Anweisung](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Attribute " **\[ Auflösen \]** " und " **\[ Loop \]** " schließen sich gegenseitig aus und generieren Compilerfehler, wenn beide angegeben werden.

Die Attribute **\[ fastopt \]** und **\[ \_ UAV \_ - \]** **\[ \]** Bedingung zulassen werden ignoriert, wenn die Option zum Aufheben der Registrierung angegeben wird.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Fluss Steuerung](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





