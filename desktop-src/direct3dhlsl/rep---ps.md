---
title: Rep-PS
description: Rep starten... ENDREP-PS-Block.
ms.assetid: vs|directx_sdk|~\rep___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6873a6aee9e31b1f28ba2755b1869cddb177306
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719386"
---
# <a name="rep---ps"></a>Rep-PS

Rep starten... [ENDREP-PS-](endrep---ps.md) Block.

## <a name="syntax"></a>Syntax



| Rep i\# |
|---------|



 

\#dabei handelt es sich um ein ganzzahliges Register, das die Wiederholungs Anzahl in der. x-Komponente angibt. Siehe [konstanter ganzzahliges Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Sprecherin                   |      |      |      |      |      | x    | x     | x    | x     |



 

-   i \# . x gibt die Iterations Anzahl an. Der zulässige Bereich ist \[ 0, 255 \] . Beachten Sie, dass diese Anweisung den Wert von i. x nicht Inkrement oder Dekrement erhöht \# .
-   i \# . yzw wird nicht vom Wiederholungs Block verwendet.
-   Wiederholungs Blöcke können eingebettet werden. Siehe [Fluss Steuerungs Einschränkungen](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
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

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




