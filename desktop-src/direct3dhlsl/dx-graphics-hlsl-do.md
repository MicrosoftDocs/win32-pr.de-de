---
title: do-Anweisung (Ocidl.h)
description: Führen Sie eine Reihe von Anweisungen kontinuierlich aus, bis der bedingte Ausdruck fehlschlägt.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- do-Anweisung HLSL
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
ms.openlocfilehash: a1f019af77ef0021ad0574bf703ff2a2a52ac0f6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118785"
---
# <a name="do-statement"></a>do-Anweisung

Führen Sie eine Reihe von Anweisungen kontinuierlich aus, bis der bedingte Ausdruck fehlschlägt.

\[*Attribut* \] do { *Statement Block*; } while( *Conditional* );



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*
</dt> <dd>

Ein optionaler Parameter, der steuert, wie die Anweisung kompiliert wird.



| attribute | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fastopt   | Reduziert die Kompilierzeit, erzeugt jedoch weniger aggressive Optimierungen. Wenn Sie dieses Attribut verwenden, werden die Schleifen vom Compiler nicht gerollt.<br/> Dieses Attribut wirkt sich nur auf Shadermodellziele aus, die [Break-Anweisungen](dx-graphics-hlsl-break.md) unterstützen. Dieses Attribut ist im Shadermodell im Vergleich [ \_ zu 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) und [Shadermodell 3 und](dx-graphics-hlsl-sm3.md) höher verfügbar. Dies ist besonders nützlich in [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höher, wenn der Compiler Schleifen kompiliert. Der Compiler simuliert standardmäßig Schleifen, um zu bewerten, ob er deren Registrierung wieder aufzeilen kann. Wenn sie nicht möchten, dass der Compiler Schleifen aufrollt, verwenden Sie dieses Attribut, um die Kompilierzeit zu reduzieren.<br/> |



 

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Anweisungsblock*
</dt> <dd>

Mindestens eine [-Anweisung.](dx-graphics-hlsl-statement-blocks.md)

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Bedingte*
</dt> <dd>

Ein bedingter [Ausdruck.](dx-graphics-hlsl-expressions.md) Der Anweisungsblock wird ausgeführt, bevor der Ausdruck ausgewertet wird. Die Schleife wird beendet, wenn der Ausdruck zu FALSE ausgewertet wird.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ocidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Flusssteuerung](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





