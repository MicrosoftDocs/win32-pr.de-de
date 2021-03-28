---
title: Wenn bool-vs
description: Startet eine, wenn... else... der umdif-vs-Block.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ff572cbaf519cc0099f3ab68d1a0becca706f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038306"
---
# <a name="if-bool---vs"></a>Wenn bool-vs

Startet eine, wenn... [else](else---vs.md)... der [umdif-vs-](endif---vs.md) Block.

## <a name="syntax"></a>Syntax



| Wenn bool |
|---------|



 

Dabei ist bool eine boolesche Registernummer. Siehe [konstantes boolesches Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Wenn bool                |      | x    | x    | x     | x    | x     |



 

Wenn das boolesche Quell Konto in der if-Anweisung "true" ist, wird der Code, der von der if-Anweisung und dem entsprechenden anderen eingeschlossen wird, ausgeführt. Andernfalls wird der Code, der von der [else](else---vs.md)... [EndIf-vs-](endif---vs.md) Anweisungen werden ausgeführt. Diese Anweisung verwendet einen Anweisungs Slot.

, wenn Blöcke eingefügt werden können.

Ein If-Block kann einen Schleifen Block nicht verspannen.

## <a name="example"></a>Beispiel

Diese Anweisung stellt bedingte statische Fluss Steuerung bereit.


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[Else-vs](else---vs.md)
</dt> <dt>

[umdif-vs](endif---vs.md)
</dt> </dl>

 

 




