---
title: rcp – vs
description: Berechnet den Kehrwert des Quellskalars. | rcp – vs
ms.assetid: be638a42-b693-461d-ab0a-3a6c0fa1acfc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d9ec2c011e4f365f7cedc1191522836db098da976c4ce3c5153169a1d87f180d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672300"
---
# <a name="rcp---vs"></a>rcp – vs

Berechnet den Kehrwert des Quellskalars.

## <a name="syntax"></a>Syntax



| rcp dst, src |
|--------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister. Das Quellregister erfordert die explizite Verwendung von "replicate swizzle", d.h. genau eine der .x-, .y-, .z-, .w swizzle-Komponenten (oder die Entsprechungen .r, .g, .b, .a) muss angegeben werden.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| rcp                    | x    | x    | x    | x     | x    | x     |



 

Das folgende Codefragment zeigt die ausgeführten Vorgänge.


```
float f = src0;
if(f == 0.0f)
{
    f = FLT_MAX;
}
else 
{
    if(f != 1.0)
    {
        f = 1/f;
    }
}

dest = f;
```



Die Ausgabe muss genau 1,0 sein, wenn die Eingabe genau 1,0 ist. Eine Quelle von 0,0 ergibt unendlich.

Die Genauigkeit sollte mindestens 1,0/(2): absoluter Fehler über dem Bereich (1,0, 2,0) sein, da allgemeine Implementierungen Mantisse und Exponent trennen.

Wenn die Quelle keine Unterskripts enthält, wird die x-Komponente verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




