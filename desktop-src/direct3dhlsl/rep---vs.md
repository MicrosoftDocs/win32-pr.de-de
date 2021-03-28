---
title: Rep-vs
description: Rep starten... ENDREP-Block.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5441d5d134ee2d60e14db9f273ec374323f93902
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389524"
---
# <a name="rep---vs"></a>Rep-vs

Rep starten... [ENDREP](endrep---vs.md) -Block.

## <a name="syntax"></a>Syntax



| Rep i\# |
|---------|



 

\#dabei handelt es sich um ein ganzzahliges Register, das die Wiederholungs Anzahl in der. x-Komponente angibt. Siehe [konstanter ganzzahliges Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Sprecherin                    |      | x    | x    | x     | x    | x     |



 

-   i \# . x gibt die Iterations Anzahl an. Der zulässige Bereich ist \[ 0, 255 \] . Beachten Sie, dass diese Anweisung den Wert von i. x nicht Inkrement oder Dekrement erhöht \# .
-   i \# . yzw wird nicht vom Wiederholungs Block verwendet.
-   Wiederholungs Blöcke können eingebettet werden. Siehe Schachtelungs [Limits der Fluss Steuerung](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
-   Wiederholungs Blöcke dürfen sich entweder vollständig innerhalb eines if- \* Blocks oder vollständig umschließen. Es sind keine überspannen zulässig.
-   Die Verwendung desselben i \# -Codes für verschiedene oder schllige Rep-Anweisungen ist in Ordnung. jede Schleife wird basierend auf der angegebenen Anzahl durchlaufen.

## <a name="example"></a>Beispiel


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




