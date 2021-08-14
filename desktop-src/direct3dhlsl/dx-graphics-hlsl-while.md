---
title: while-Anweisung
description: Führt einen Anweisungsblock aus, bis der bedingte Ausdruck fehlschlägt.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- while-Anweisung HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4e9ae7dc0d8280c9b9823d77dcfe5968243a1ddebdaf78e76b03651ee465034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983160"
---
# <a name="while-statement"></a>while-Anweisung

Führt einen Anweisungsblock aus, bis der bedingte Ausdruck fehlschlägt.

\[*Attribut* \] while ( *Bedingt* ) { *Anweisungsblock;*}



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*
</dt> <dd>

Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.



| attribute             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| unroll(x)             | Entrollt die Schleife, bis die Ausführung beendet wird. Optional können Sie angeben, wie oft die Schleife maximal ausgeführt werden kann.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| loop                  | Verwenden Sie Flow-Control-Anweisungen im kompilierten Shader. Die Schleife wird nicht gerollt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| fastopt               | Reduziert die Kompilierzeit, erzeugt jedoch weniger aggressive Optimierungen. Wenn Sie dieses Attribut verwenden, werden die Schleifen vom Compiler nicht gerollt.<br/> Dieses Attribut wirkt sich nur auf Shadermodellziele aus, die [Break-Anweisungen](dx-graphics-hlsl-break.md) unterstützen. Dieses Attribut ist im Shadermodell im Vergleich [ \_ zu 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [Shadermodell 3 und](dx-graphics-hlsl-sm3.md) höher verfügbar. Dies ist besonders nützlich in [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höher, wenn der Compiler Schleifen kompiliert. Der Compiler simuliert standardmäßig Schleifen, um zu bewerten, ob er deren Registrierung wieder aufzeilen kann. Wenn sie nicht möchten, dass der Compiler Schleifen aufrollt, verwenden Sie dieses Attribut, um die Kompilierzeit zu reduzieren.<br/> |
| \_UAV-Bedingung \_ zulassen | Ermöglicht es, dass eine Beendigungsbedingung für eine Compute-Shaderschleife auf einem UAV-Lese-Wert basiert. Die Schleife darf keine systeminternen Synchronisierungseinstellungen enthalten.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Bedingte*
</dt> <dd>

Ein bedingter [Ausdruck.](dx-graphics-hlsl-expressions.md) Wenn der Ausdruck zu TRUE ausgewertet wird, wird der Anweisungsblock ausgeführt. Die Schleife endet, wenn der Ausdruck als FALSE ausgewertet wird.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungsblock*
</dt> <dd>

Mindestens eine [Anweisung](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Flow Steuerung](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





