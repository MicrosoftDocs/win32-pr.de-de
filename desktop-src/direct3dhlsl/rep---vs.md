---
title: rep – im Vergleich zu
description: Starten eines Mitarbeiters... endrep-Block.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e800f2ef313cd5c9a4fc90d7205502db5532ae24f51ec0f1255d05cc9a589bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853790"
---
# <a name="rep---vs"></a>rep – im Vergleich zu

Starten eines Mitarbeiters... [endrep-Block.](endrep---vs.md)

## <a name="syntax"></a>Syntax



| rep i\# |
|---------|



 

dabei ist i \# ein ganzzahliges Register, das die Wiederholungsanzahl in der X-Komponente angibt. Weitere Informationen finden Sie unter [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Rep                    |      | x    | x    | x     | x    | x     |



 

-   i \# .x gibt die Iterationsanzahl an. Der rechtliche Bereich ist \[ 0, 255 \] . Beachten Sie, dass diese Anweisung den Wert von i .x nicht erhöht oder dekrementiert. \#
-   i \# .yzw werden nicht vom Wiederholungsblock verwendet.
-   Wiederholungsblöcke können geschachtelt sein. Weitere Informationen finden Sie [unter Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
-   Wiederholungsblöcke dürfen sich entweder vollständig innerhalb eines \* if-Blocks oder vollständig um ihn herum befinden. Es ist kein Umschließen zulässig.
-   Die Verwendung des gleichen i \# für verschiedene oder geschachtelte Rep-Anweisungen ist in Ordnung. Jede Schleife wird basierend auf der angegebenen Anzahl durchlaufen.

## <a name="example"></a>Beispiel


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




