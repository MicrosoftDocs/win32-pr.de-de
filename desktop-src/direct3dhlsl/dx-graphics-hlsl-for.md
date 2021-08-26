---
title: for-Anweisung
description: Führt iterativ eine Reihe von -Anweisungen basierend auf der Auswertung des bedingten Ausdrucks aus.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- for-Anweisung HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 001683c612aefb56d8257977ce7efe99d162a0919d39c678ee4074128a019a31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068190"
---
# <a name="for-statement"></a>for-Anweisung

Führt iterativ eine Reihe von -Anweisungen basierend auf der Auswertung des bedingten Ausdrucks aus.

\[*Attribut* \] for ( *Initialisierer; Bedingt; Iterator* ) { *Anweisungsblock;*}



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*
</dt> <dd>

Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird. Wenn kein Attribut angegeben ist, versucht der Compiler zunächst, eine rollierte Version der Schleife aus zu geben. Wenn dies fehlschlägt oder einige Vorgänge einfacher wären, wenn die Schleife entrollt wurde, wird auf eine nicht gerollte Version der Schleife zurückgesetzt.



| attribute             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| unroll(x)             | Entrollt die Schleife, bis die Ausführung beendet wird. Kann optional angeben, wie oft die Schleife maximal ausgeführt werden soll. Nicht kompatibel mit dem **\[ \] Schleifenattribut.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| loop                  | Generiert Code, der die Flusssteuerung verwendet, um jede Iteration der Schleife auszuführen. Nicht kompatibel mit dem **\[ \] Unroll-Attribut.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| fastopt               | Reduziert die Kompilierzeit, erzeugt jedoch weniger aggressive Optimierungen. Wenn Sie dieses Attribut verwenden, werden die Schleifen vom Compiler nicht gerollt.<br/> Dieses Attribut wirkt sich nur auf Shadermodellziele aus, die [Break-Anweisungen](dx-graphics-hlsl-break.md) unterstützen. Dieses Attribut ist im Shadermodell im Vergleich [ \_ zu 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [Shadermodell 3 und](dx-graphics-hlsl-sm3.md) höher verfügbar. Dies ist besonders nützlich in [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höher, wenn der Compiler Schleifen kompiliert. Der Compiler simuliert standardmäßig Schleifen, um zu bewerten, ob er deren Registrierung wieder aufzeilen kann. Wenn sie nicht möchten, dass der Compiler Schleifen aufrollt, verwenden Sie dieses Attribut, um die Kompilierzeit zu reduzieren. <br/> |
| \_UAV-Bedingung \_ zulassen | Ermöglicht es, dass eine Beendigungsbedingung für eine Compute-Shaderschleife auf einem UAV-Lese-Wert basiert. Die Schleife darf keine systeminternen Synchronisierungseinstellungen enthalten.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initialisierung*
</dt> <dd>

Der Anfangswert des Schleifenzählers.

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Bedingte*
</dt> <dd>

Ein bedingter [Ausdruck.](dx-graphics-hlsl-expressions.md) Wenn der bedingte Ausdruck als TRUE ausgewertet wird, wird der Anweisungsblock ausgeführt. Die Schleife endet, wenn der Ausdruck als FALSE ausgewertet wird.

</dd> <dt>

<span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*
</dt> <dd>

Aktualisieren Sie den Wert des Schleifenzählers.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungsblock*
</dt> <dd>

Mindestens eine [HLSL-Anweisung.](dx-graphics-hlsl-statement-blocks.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\[ Attribute \] "unroll"** **\[ und "loop" \]** schließen sich gegenseitig aus und generieren Compilerfehler, wenn beide angegeben werden.

Die **\[ Attribute \] fastopt** und **\[ allow \_ uav \_ \] condition** werden ignoriert, wenn **\[ unroll \]** angegeben wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Flow Steuerung](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





