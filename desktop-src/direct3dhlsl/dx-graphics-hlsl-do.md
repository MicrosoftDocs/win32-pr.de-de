---
title: Do-Anweisung (ocidl. h)
description: Führen Sie eine Reihe von Anweisungen kontinuierlich aus, bis der bedingte Ausdruck fehlschlägt.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- Do-Anweisung HLSL
topic_type:
- apiref
api_name:
- do Statement
api_location:
- ocidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c0ced3c9747f0bfbdf01847b21350a45b68aa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219503"
---
# <a name="do-statement"></a>Do-Anweisung

Führen Sie eine Reihe von Anweisungen kontinuierlich aus, bis der bedingte Ausdruck fehlschlägt.



|                                                                     |
|---------------------------------------------------------------------|
| \[*Attribut* \] Do { *Statement Block*;} while ( *bedingt* ); |



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Versehen*
</dt> <dd>

Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.



| attribute | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fastopt   | Verringert die Kompilierzeit, erzeugt jedoch weniger aggressive Optimierungen. Wenn Sie dieses Attribut verwenden, entlädt der Compiler keine Schleifen.<br/> Dieses Attribut wirkt sich nur auf shadermodellziele aus, die [unterbrechungsanweisungen](dx-graphics-hlsl-break.md) unterstützen Dieses Attribut ist im Shader-Modell [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [Shader Model 3](dx-graphics-hlsl-sm3.md) und höher verfügbar. Dies ist besonders nützlich, [](dx-graphics-hlsl-sm4.md) wenn der Compiler Schleifen kompiliert. Der Compiler simuliert standardmäßig Schleifen, um auszuwerten, ob er die Registrierung aufheben kann. Verwenden Sie dieses Attribut, um die Kompilierzeit zu verkürzen, wenn der Compiler keine Schleifen aufheben soll.<br/> |



 

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungs Block*
</dt> <dd>

Eine oder mehrere- [Anweisungen](dx-graphics-hlsl-statement-blocks.md).

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*
</dt> <dd>

Ein bedingter [Ausdruck](dx-graphics-hlsl-expressions.md). Der Anweisungsblock wird ausgeführt, bevor der Ausdruck ausgewertet wird. Die Schleife wird beendet, wenn der Ausdruck zu false ausgewertet wird.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>"Ocidl. h"</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Fluss Steuerung](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





