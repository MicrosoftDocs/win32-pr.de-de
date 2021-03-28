---
title: while-Anweisung
description: Führt einen Anweisungsblock aus, bis der bedingte Ausdruck fehlschlägt.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- While-Anweisung HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 190d5474b5e016b41426db67a0c96d98787f79ff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037856"
---
# <a name="while-statement"></a>while-Anweisung

Führt einen Anweisungsblock aus, bis der bedingte Ausdruck fehlschlägt.



|                                                                  |
|------------------------------------------------------------------|
| \[*Attribut* \] while ( *Conditional* ) { *Statement Block*;} |



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Versehen*
</dt> <dd>

Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.



| attribute             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aufheben der Registrierung (x)             | Entsperren Sie die Schleife, bis die Ausführung beendet ist. Optional können Sie angeben, wie oft die Schleife maximal ausgeführt werden kann.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| loop                  | Verwenden von Fluss Steuerungs Anweisungen im kompilierten Shader; Heben Sie die rollforwardschleife nicht auf.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| fastopt               | Verringert die Kompilierzeit, erzeugt jedoch weniger aggressive Optimierungen. Wenn Sie dieses Attribut verwenden, entlädt der Compiler keine Schleifen.<br/> Dieses Attribut wirkt sich nur auf shadermodellziele aus, die [unterbrechungsanweisungen](dx-graphics-hlsl-break.md) unterstützen Dieses Attribut ist im Shader-Modell [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [Shader Model 3](dx-graphics-hlsl-sm3.md) und höher verfügbar. Dies ist besonders nützlich, [](dx-graphics-hlsl-sm4.md) wenn der Compiler Schleifen kompiliert. Der Compiler simuliert standardmäßig Schleifen, um auszuwerten, ob er die Registrierung aufheben kann. Verwenden Sie dieses Attribut, um die Kompilierzeit zu verkürzen, wenn der Compiler keine Schleifen aufheben soll.<br/> |
| \_UAV- \_ Bedingung zulassen | Ermöglicht, dass die Beendigungs Bedingung einer COMPUTE-Shader-Schleife auf einem UAV-Lesevorgang basiert. Die Schleife darf keine systeminternen Synchronisierungs Funktionen enthalten.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*
</dt> <dd>

Ein bedingter [Ausdruck](dx-graphics-hlsl-expressions.md). Wenn der Ausdruck als "true" ausgewertet wird, wird der Anweisungsblock ausgeführt. Die Schleife endet, wenn der Ausdruck zu false ausgewertet wird.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungs Block*
</dt> <dd>

Eine oder mehrere- [Anweisungen](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Fluss Steuerung](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





