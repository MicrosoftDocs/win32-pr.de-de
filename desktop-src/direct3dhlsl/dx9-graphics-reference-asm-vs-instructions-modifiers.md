---
title: Anweisungsmodifiziererer (HLSL vs-Referenz)
description: Anweisungs Modifizierer
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 573f2ef618c4cd29092fb38fb4c805bdeeecc219
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104472076"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a>Anweisungsmodifiziererer (HLSL vs-Referenz)

Anweisungsmodifiziererer wirken sich auf das Ergebnis der Anweisung aus, bevor Sie in das Ziel Register geschrieben wird.

## <a name="_sat"></a>\_gesetzt

Füllt das Anweisungs Ergebnis (oder bindet es) \[ \] vor dem Schreiben in das Ziel Register in 0, 1 Bereich.

Beispiel:


```
add_sat dst, src0, src1
```



Hierbei gilt:

DST = Klammer \_ zwischen \_ 0 \_ und \_ 1 (src0 + Quelle1)

Der \_ Sat-Anweisungs Modifizierer kostet keine zusätzlichen Anweisungs Slots.

Wenn unterstützt, \_ kann der Sat-anweisungsmodifizierer mit einer beliebigen Anweisung verwendet werden, mit Ausnahme von: [FRC-vs](frc---vs.md), [SinCos-vs](sincos---vs.md)und [texldl-vs](texldl---vs.md).



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| \_gesetzt                  |      |      |      |       | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




