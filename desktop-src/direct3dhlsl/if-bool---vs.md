---
title: if bool – vs
description: Startet eine , wenn... oder... endif – vs block.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b113c806342d786d258713128bc2cadcbb000235c2639f49e5b57ce3fa3bd2e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986530"
---
# <a name="if-bool---vs"></a>if bool – vs

Startet eine , wenn... [else](else---vs.md)... [endif – vs](endif---vs.md) block.

## <a name="syntax"></a>Syntax



| , wenn bool |
|---------|



 

dabei ist bool eine bool-Registernummer. Weitere Informationen finden Sie unter [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| , wenn bool                |      | x    | x    | x     | x    | x     |



 

Wenn der boolesche Quellregister in der if-Anweisung TRUE ist, wird der in der if-Anweisung eingeschlossene Code und der entsprechende andere Code ausgeführt. Andernfalls der Code, der von der [else](else---vs.md)... [endif: Vs-Anweisungen](endif---vs.md) werden ausgeführt. Diese Anweisung verwendet einen Anweisungsslot.

, wenn Blöcke geschachtelt werden können.

Ein if-Block kann sich nicht über einen Schleifenblock erstreckt.

## <a name="example"></a>Beispiel

Diese Anweisung stellt eine bedingte statische Flusssteuerung bereit.


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

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[else – im Vergleich zu](else---vs.md)
</dt> <dt>

[endif – im Vergleich zu](endif---vs.md)
</dt> </dl>

 

 




