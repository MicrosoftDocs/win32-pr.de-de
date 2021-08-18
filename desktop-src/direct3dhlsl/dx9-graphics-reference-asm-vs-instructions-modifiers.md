---
title: Anweisungsmodifizierer (HLSL VS-Referenz)
description: Anweisungsmodifizierer
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2bdad90d13fe960c0d7a5cabfbb508d8abba890e8114c6d4ae1e47d1977e7d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119694"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a>Anweisungsmodifizierer (HLSL VS-Referenz)

Anweisungsmodifizierer beeinflussen das Ergebnis der Anweisung, bevor sie in das Zielregister geschrieben wird.

## <a name="_sat"></a>\_sat

Saturiert (oder klammscht) das Anweisungsergebnis auf \[ 0,1 \] Bereich, bevor in das Zielregister geschrieben wird.

Beispiel:


```
add_sat dst, src0, src1
```



Hierbei gilt:

dst = Klammer \_ zwischen \_ 0 \_ und \_ 1(src0 + src1)

Der \_ Sat-Anweisungsmodifizierer kostet keine zusätzlichen Anweisungsslots.

Falls unterstützt, kann der \_ Sat-Anweisungsmodifizierer mit einer beliebigen Anweisung verwendet werden, mit Ausnahme von [frc - vs](frc---vs.md), [sincos - vs](sincos---vs.md)und [texldl - vs](texldl---vs.md).



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| \_sat                  |      |      |      |       | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




