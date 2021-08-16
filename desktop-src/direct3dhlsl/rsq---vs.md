---
title: rsq – vs
description: Berechnet die reziproke Quadratwurzel (nur positiv) des Quellskalars. | rsq – vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 937f89a018943d9ab8f74a4a328316d5d68dca7d48730a06b80814dacbd8ed68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510907"
---
# <a name="rsq---vs"></a>rsq – vs

Berechnet die reziproke Quadratwurzel (nur positiv) des Quellskalars.

## <a name="syntax"></a>Syntax



| rsq dst, src |
|--------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister. Das Quellregister erfordert die explizite Verwendung von "replicate swizzle", d.h. genau eine der .x-, .y-, .z-, .w swizzle-Komponenten (oder die Entsprechungen .r, .g, .b, .a) muss angegeben werden.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| rsq                    | x    | x    | x    | x     | x    | x     |



 

Das folgende Codefragment zeigt die ausgeführten Vorgänge.


```
float f = abs(src0);
if (f == 0)
    f = FLT_MAX
else
{
    if (f != 1.0)
        f = 1.0/(float)sqrt(f);
}

dest.z = dest.y = dest.z = dest.w = f;
```



Der absolute Wert wird vor der Verarbeitung übernommen.

Die Genauigkeit sollte mindestens 1,0/(2): absoluter Fehler über dem Bereich (1,0, 4,0) sein, da allgemeine Implementierungen Mantisse und Exponent trennen.

Wenn source keine Unterskripts enthält, wird die x-Komponente verwendet. Die Ausgabe muss genau 1,0 sein, wenn die Eingabe genau 1,0 ist. Eine Quelle von 0,0 ergibt unendlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




