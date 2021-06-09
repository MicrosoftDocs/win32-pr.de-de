---
title: while-Anweisung
description: Führt einen Anweisungsblock aus, bis der bedingte Ausdruck fehlschlägt.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- while Statement HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bf1f0049ac474e7840753a8cfe05c972aa346c1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826673"
---
# <a name="while-statement"></a>while-Anweisung

Führt einen Anweisungsblock aus, bis der bedingte Ausdruck fehlschlägt.

\[*Attribut* \] while ( *Conditional* ) { *Statement Block*; }



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*
</dt> <dd>

Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.



| attribute             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| unroll(x)             | Entrollt die Schleife, bis sie nicht mehr ausgeführt wird. Optional können Sie angeben, wie oft die Schleife maximal ausgeführt werden kann.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| loop                  | Verwenden Sie Flusssteuerungsanweisungen im kompilierten Shader. Die Schleife darf nicht entladen werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| fastopt               | Reduziert die Kompilierzeit, erzeugt aber weniger aggressive Optimierungen. Wenn Sie dieses Attribut verwenden, wird der Compiler die Registrierung von Schleifen nicht aufheben.<br/> Dieses Attribut wirkt sich nur auf Shadermodellziele aus, die [Unterbrechungsanweisungen](dx-graphics-hlsl-break.md) unterstützen. Dieses Attribut ist im Shadermodell [im Vergleich \_ zu 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [im Shadermodell 3](dx-graphics-hlsl-sm3.md) und höher verfügbar. Dies ist besonders nützlich in [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höher, wenn der Compiler Schleifen kompiliert. Der Compiler simuliert standardmäßig Schleifen, um zu bewerten, ob sie die Registrierung aufheben können. Wenn der Compiler die Registrierung von Schleifen nicht aufheben soll, verwenden Sie dieses Attribut, um die Kompilierzeit zu verkürzen.<br/> |
| \_UAV-Bedingung zulassen \_ | Ermöglicht, dass die Beendigungsbedingung einer Compute-Shaderschleife auf einem UAV-Lesezustand basiert. Die Schleife darf keine systeminternen Synchronisierungsfunktionen enthalten.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Bedingte*
</dt> <dd>

Ein bedingter [Ausdruck.](dx-graphics-hlsl-expressions.md) Wenn der Ausdruck als TRUE ausgewertet wird, wird der Anweisungsblock ausgeführt. Die Schleife endet, wenn der Ausdruck als FALSE ausgewertet wird.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungsblock*
</dt> <dd>

Mindestens eine [-Anweisungen.](dx-graphics-hlsl-statement-blocks.md)

</dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Flusssteuerung](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





