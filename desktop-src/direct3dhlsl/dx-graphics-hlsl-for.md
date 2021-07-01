---
title: for-Anweisung
description: Führt basierend auf der Auswertung des bedingten Ausdrucks iterativ eine Reihe von Anweisungen aus.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- for Statement HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cbcf06f28a327e18aa9f31b417dc1911411d0c9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119076"
---
# <a name="for-statement"></a>for-Anweisung

Führt basierend auf der Auswertung des bedingten Ausdrucks iterativ eine Reihe von Anweisungen aus.

\[*Attribut* \] for ( *Initialisierer; Bedingt; Iterator* ) { *Anweisungsblock*; }



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*
</dt> <dd>

Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird. Wenn kein Attribut angegeben wird, versucht der Compiler zunächst, eine rollierte Version der Schleife auszugeben. Wenn dies fehlschlägt oder einige Vorgänge einfacher wären, wenn die Schleife nicht ausgeführt wurde, wird auf eine nichtrollierte Version der Schleife zurückgesetzt.



| attribute             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| unroll(x)             | Entrollt die Schleife, bis sie nicht mehr ausgeführt wird. Kann optional angeben, wie oft die Schleife maximal ausgeführt werden soll. Nicht kompatibel mit dem **\[ \]** Schleifenattribut.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| loop                  | Generieren Sie Code, der die Flusssteuerung verwendet, um jede Iteration der Schleife auszuführen. Nicht kompatibel mit dem **\[ \] Unroll-Attribut.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| fastopt               | Reduziert die Kompilierzeit, erzeugt aber weniger aggressive Optimierungen. Wenn Sie dieses Attribut verwenden, wird der Compiler die Registrierung von Schleifen nicht aufheben.<br/> Dieses Attribut wirkt sich nur auf Shadermodellziele aus, die [Unterbrechungsanweisungen](dx-graphics-hlsl-break.md) unterstützen. Dieses Attribut ist im Shadermodell [im Vergleich \_ zu 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [im Shadermodell 3](dx-graphics-hlsl-sm3.md) und höher verfügbar. Dies ist besonders nützlich im [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höher, wenn der Compiler Schleifen kompiliert. Der Compiler simuliert standardmäßig Schleifen, um auszuwerten, ob die Registrierung aufheben werden kann. Wenn der Compiler die Registrierung von Schleifen nicht aufheben soll, verwenden Sie dieses Attribut, um die Kompilierzeit zu verkürzen. <br/> |
| \_UAV-Bedingung zulassen \_ | Ermöglicht, dass die Beendigungsbedingung einer Compute-Shaderschleife auf einem UAV-Lesezustand basiert. Die Schleife darf keine systeminternen Synchronisierungsfunktionen enthalten.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

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

Eine oder mehrere [HLSL-Anweisungen.](dx-graphics-hlsl-statement-blocks.md)

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\[ Unroll- \]** und **\[ Schleifenattribute \]** schließen sich gegenseitig aus und generieren Compilerfehler, wenn beide angegeben werden.

Die Attribute **\[ fastopt \]** und **\[ allow \_ uav \_ condition \]** werden ignoriert, wenn die **\[ Registrierung \]** angegeben wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Flusssteuerung](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





