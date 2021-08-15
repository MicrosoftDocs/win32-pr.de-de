---
title: mova im Vergleich zu
description: Verschieben Sie Daten aus einem Gleitkommaregister in das Adressregister, a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dec849009ee47b4aaef1bc3766e2b141a8a6ccf5e17b16a370c6ea8284eaf957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986330"
---
# <a name="mova---vs"></a>mova im Vergleich zu

Verschieben Sie Daten aus einem Gleitkommaregister in [das Adressregister](dx9-graphics-reference-asm-vs-registers-address.md), a0.

## <a name="syntax"></a>Syntax



| mova dst, src |
|---------------|



 

where

-   dst muss das [Adressregister](dx9-graphics-reference-asm-vs-registers-address.md), a0 sein.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Mova                   |      | x    | x    | x     | x    | x     |



 

Verschiebt Gleitkommadaten in ein Ganzzahlregister. Die Werte werden von Gleitkommawerten mithilfe einer Rundung in die nächste konvertiert.

Das Adressregister ist das einzige zulässige Zielregister.

Das folgende Codefragment zeigt die ausgeführten Vorgänge.


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



Für Die Versionen 2 \_ x und höher ist das Adressregister ein Komponentenvektor. Daher ist jede Schreibmaske zulässig.


```
mova a0.xz, r0
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




